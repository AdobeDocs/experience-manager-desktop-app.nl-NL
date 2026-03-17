---
title: Los Desktop app versie 1.10 problemen op.
description: Los  [!DNL Adobe Experience Manager]  Desktop app versie 1.10 problemen op om de occasionele kwesties met betrekking tot installatie, verbetering, en configuratie op te lossen.
exl-id: 1e1409c2-bf5e-4e2d-a5aa-3dd74166862c
source-git-commit: 19e4b92016670de20474b251cda9f2f5274dbc26
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# Problemen met [!DNL Adobe Experience Manager] bureaubladtoepassing v1.x oplossen {#troubleshoot-aem-desktop-app}

Los de Desktop app van AEM problemen op om de af en toe kwesties met betrekking tot installatie, verbetering, configuratie, etc. op te lossen.

De desktop-app van [!DNL Adobe Experience Manager] bevat hulpprogramma&#39;s waarmee u de AEM Assets-opslagplaats kunt toewijzen als een gedeelde netwerksite op een desktopcomputer (SMB-share op macOS). Het aandeel van het netwerk is een werkend systeemtechnologie die verre bronnen toelaat worden behandeld alsof zij deel van het lokale dossiersysteem van een computer maakten. Voor de bureaubladtoepassing is de externe bestandsbron de DAM-opslagstructuur (Digital Asset Management) van een externe AEM-instantie. In het volgende diagram wordt de topologie van de bureaubladtoepassing beschreven:

![ Desktop app diagram ](assets/aem-desktopapp-architecture.png)

Met deze architectuur onderschept de bureaubladtoepassing bestandssysteemaanroepen (openen, sluiten, lezen, schrijven, enzovoort) naar het gekoppelde netwerkaandeel en zet deze om in native AEM HTTP-aanroepen naar de AEM-server. Bestanden worden lokaal in cache geplaatst. Voor meer details, zie [ Desktop app v1.x van AEM gebruiken ](use-app-v1.md).

## Overzicht van de AEM-bureaubladtoepassing {#desktop-app-component-overview}

De bureaubladtoepassing bevat de volgende componenten:

* **de Desktoptoepassing**: De toepassing bouwt of maakt DAM als ver dossiersysteem op. Het vertaalt de vraag van het dossiersysteem tussen het plaatselijk opgezette netwerkaandeel en de verre instantie van AEM waarmet het verbindt.
* **de cliënt van WebDAV/SMB van het Werkende systeem**: Behandelt communicatie tussen de Ontdekkingsreiziger/de Vinder van Vensters en Desktop app. Als een bestand wordt opgehaald, gemaakt, gewijzigd, verwijderd, verplaatst of gekopieerd, communiceert de WebDAV/SMB-client van het besturingssysteem deze bewerking met de desktop-app. Nadat de communicatie is ontvangen, zet de bureaubladtoepassing deze om in externe API-aanroepen van AEM. Als een gebruiker bijvoorbeeld een bestand maakt in de gekoppelde map, initieert de WebDAV/SMB-client een aanvraag, die de bureaubladtoepassing omzet in een HTTP-aanvraag die het bestand maakt in DAM. De WebDAV/SMB-client is een ingebouwde component van het besturingssysteem. Het is geenszins verbonden met desktop app, AEM of Adobe.
* **instantie van Adobe Experience Manager**: Verleent toegang tot activa die in de bewaarplaats van AEM Assets DAM worden opgeslagen. Bovendien voert het acties uit die door de Desktop app worden gevraagd namens de lokale Desktoptoepassingen die met het opgezette netwerkaandeel interactie aangaan. De AEM-doelinstantie moet AEM versie 6.1 of hoger uitvoeren. Voor AEM-instanties die eerdere AEM-versies uitvoeren, zijn mogelijk extra functiepakketten en hotfixes vereist die zijn geïnstalleerd om volledig te kunnen functioneren.

## Beoogde gebruiksgevallen voor de AEM-bureaubladtoepassing {#intended-use-cases-for-aem-desktop-app}

De AEM-bureaubladtoepassing gebruikt de technologie voor netwerkdeling om een externe AEM-opslagplaats toe te wijzen aan een lokale desktop. Het is echter niet bedoeld als vervanging voor een netwerkshare-holding-assets, waarbij gebruikers digitale middelenbeheerbewerkingen rechtstreeks vanaf hun lokale bureaublad uitvoeren. Dit zijn onder andere het verplaatsen of kopiëren van meerdere bestanden of het rechtstreeks slepen van grote mapstructuren naar het AEM Assets-netwerkaandeel in Finder/Explorer.

De AEM-bureaubladtoepassing biedt een handige manier om DAM-middelen te openen en te bewerken (opslaan) tussen de AEM Assets Touch-gebruikersinterface en het lokale bureaublad. Elementen op de AEM Assets-server worden gekoppeld aan workflows op uw bureaublad.

Het volgende voorbeeld laat zien hoe AEM Desktop moet worden gebruikt:

* Een gebruiker meldt zich aan bij AEM en gebruikt de web-UI om een middel te zoeken.
* Met de actiemogelijkheden van het bureaublad van de AEM-webinterface opent, geeft of bewerkt de gebruiker het middel desgewenst op het bureaublad.
* AEM Desktop opent het element in de standaardeditor voor het bestandstype van het element.
* De gebruiker brengt de gewenste wijzigingen aan in het element.
* Nadat een bestand is gewijzigd, kan de gebruiker de synchronisatiestatus van het bestand weergeven via het statusvenster voor achtergrondsynchronisatie van AEM Desktop.
* Met behulp van het contextmenu van AEM Desktop controleert de gebruiker het middel in of uit, of gaat hij terug naar de DAM-gebruikersinterface.
* Nadat de wijzigingen in het bestand zijn aangebracht, keert de gebruiker terug naar de gebruikersinterface van het AEM-web

Dit scenario is niet het enige gebruiksgeval. Het toont echter aan hoe AEM Desktop een handig mechanisme is om elementen lokaal te openen/bewerken. U wordt aangemoedigd om de DAM-webinterface zoveel mogelijk te gebruiken, omdat deze een betere ervaring biedt. Het biedt Adobe meer flexibiliteit om aan de vereisten van de klant te voldoen.

## Beperkingen {#limitations}

WebDAV/SMB1 netwerkaandeel verstrekt het gemak om met dossiers in een venster van de Ontdekkingsreiziger/van de Vinder te werken. Verkenner/Finder en AEM communiceren echter via een netwerkverbinding met bepaalde beperkingen. De tijd die bijvoorbeeld nodig is om een 1-GB-bestand naar de gekoppelde WebDAV/SMB-map te kopiëren, is ongeveer gelijk aan de tijd die nodig is om een 1-GB-bestand met een webbrowser naar een website te uploaden. In het eerste geval kan de duur langer zijn vanwege inefficiënties van het WebDAV/SMB-protocol en de WebDAV/SMB-clients van het besturingssysteem (met name macOS X).

Er zijn beperkingen aan de typen taken die vanuit een gekoppelde map kunnen worden uitgevoerd. Over het algemeen kan het lastig zijn om met grote bestanden te werken, met name via een slechte/hoge latentie/lage bandbreedte-netwerkverbinding, vooral wanneer u grote bestanden bewerkt.

Adobe raadt u aan een aantal tests met een gebruiksscenario uit te voeren voordat u een client bindt, zodat bepaalde bestandstypen op een efficiënte manier op hun plaats kunnen worden bewerkt vanuit de gekoppelde map.

AEM Desktop is niet geschikt voor intensief bewerken van bestandssystemen, waaronder, maar niet beperkt tot:

* Bestanden en mappen verplaatsen of kopiëren
* Veel middelen toevoegen aan AEM
* Bestanden zoeken en openen via het bestandssysteem, behalve in mappen
* Bestandsarchieven comprimeren of decomprimeren

Vanwege beperkingen in het besturingssysteem geldt voor Windows een maximale bestandsgrootte van 4.294.967.295 bytes (ongeveer 4,29 GB). Dit is te wijten aan een registerinstelling die bepaalt hoe groot een bestand op een netwerkshare kan zijn. De waarde van de registratie het plaatsen is DWORD met een maximumgrootte die het referenced aantal evenaart.

De desktop-app van [!DNL Experience Manager] heeft geen configureerbare time-outwaarde die de verbinding tussen de [!DNL Experience Manager] -server en de desktop-app na een vast tijdsinterval verbreekt. Wanneer u grote middelen uploadt en de verbinding na een tijdje wordt verbroken, probeert de toepassing het element een paar keer te uploaden door de time-out van het uploaden te verhogen. Er is geen aanbevolen manier om de standaardtime-outinstellingen te wijzigen.

## Caching en communicatie met AEM {#caching-and-communication-with-aem}

De AEM-bureaubladtoepassing biedt mogelijkheden voor interne caching en het uploaden naar de achtergrond om de gebruikerservaring te verbeteren. Wanneer u een groot bestand opslaat, wordt het eerst lokaal opgeslagen zodat u kunt doorgaan met werken. Na enige tijd (momenteel 30 seconden) wordt het bestand op de achtergrond naar de AEM-server verzonden.

In tegenstelling tot Creative Cloud Desktop of andere oplossingen voor bestandssynchronisatie, zoals Microsoft One Drive, is de AEM desktop app geen volledige Desktop Sync client. De reden hiervoor is dat het toegang biedt tot de gehele AEM Assets-opslagplaats, die zeer groot kan zijn (honderden gigabytes of terabytes) voor een volledige synchronisatie.

Caching verstrekt de capaciteit om de netwerk/opslagoverheadkosten tot slechts een ondergroep van activa te beperken die voor de gebruiker relevant zijn.

>[!CAUTION]
>
>Adobe raadt u aan miniatuurgeneratie uit te schakelen om sneller te kunnen bladeren. Als u pictogramvoorvertoningen inschakelt, plaatst de app de digitale elementen in de cache wanneer u door de gekoppelde map navigeert. De app downloadt ook elementen die de gebruiker niet kan schelen. Als dusdanig, voegt het lading aan de server toe, verbruikt de bandbreedte van de gebruiker, en gebruikt meer van de schijfruimte van de gebruiker.

Hieronder wordt beschreven hoe de AEM-bureaubladtoepassing caching uitvoert:

* Wanneer u een map opent in de Finder en er miniaturen of voorvertoningen van bestanden worden weergegeven, plaatst de bureaubladtoepassing het bestand binair in de cache. Wanneer u een bestand in een toepassing opent, wordt het bestand ook binair door de toepassing in cache opgeslagen.
* Wanneer u bestanden opslaat in de vorm van Finder of andere bureaubladtoepassingen, wordt het bestand eerst lokaal opgeslagen (in cache geplaatst) en wordt het besturingssysteem op de hoogte gesteld. Het bestand wordt vervolgens in de wachtrij geplaatst voor uploaden naar de server op de achtergrond en wordt uiteindelijk via het netwerk geüpload. Als er een netwerkfout optreedt, probeert de bureaubladtoepassing het gehele bestand maximaal drie keer te uploaden. Als het uploaden van de bestanden mislukt nadat drie keer is geprobeerd, wordt het bestand gemarkeerd als een conflicterend bestand en wordt de status weergegeven via het venster Status wachtrij uploaden op de achtergrond. de bureaubladtoepassing probeert het bestand niet meer bij te werken. De gebruiker moet het bestand bijwerken en opnieuw uploaden nadat de connectiviteit is hersteld

Elke bewerking wordt niet lokaal in het cachegeheugen opgeslagen. Het volgende wordt onmiddellijk zonder lokale caching naar de AEM Server verzonden:

* Alle bewerkingen in mappen, zoals maken, verwijderen, enzovoort
* Met de functie Map uploaden die in versie 1.4 is geïntroduceerd, wordt een lokale maphiërarchie geüpload zonder de bestanden lokaal in de cache te plaatsen

## Individuele verrichtingen {#individual-operations}

Wanneer het oplossen van problemen sub-geoptimaliseerde prestaties voor individuele gebruikers, eerste overzicht [ de toepassingsbeperkingen ](#limitations). De volgende secties bevatten suggesties om de prestaties voor individuele gebruikers te verbeteren.

## Aanbevelingen voor bandbreedte {#bandwidth-recommendations}

De bandbreedte beschikbaar aan een individuele gebruiker speelt een kritieke rol in de prestaties van de cliënt WebDAV/SMB.

Adobe raadt aan dat de uploadsnelheid van een individuele gebruiker dicht bij 10 Mbps ligt. Voor draadloze verbindingen, wordt de bandbreedte vaak gedeeld tussen veelvoudige gebruikers. Als de veelvoudige gebruikers tegelijkertijd taken uitvoeren die netwerkbandbreedte verbruiken, kunnen de prestaties nog verder degraderen. Gebruik een bekabelde verbinding om dergelijke problemen te voorkomen.

<!-- 
AG, 8/18: The Windows KB article is removed by MS now. Giving 404. Also, Win 7 support is gone and the desktop app is also not supported on Win 7. Hiding this content for now.

## Windows-specific configurations {#windows-specific-configurations}

If you use Experience Manager on Windows, you can configure Windows to enhance the performance of the WebDAV client. For more information, go to [https://support.microsoft.com/en-us/kb/2445570](https://support.microsoft.com/en-us/kb/2445570).

On Windows 7, modifying IE settings can improve the performance of WebDAV. For details, see how to [fix slow WebDAV performance in Windows 7](https://oddballupdate.com/2009/12/fix-slow-webdav-performance-in-windows-7/).
-->

## Gelijktijdige bewerkingen {#concurrent-operations}

Wanneer u lokaal met een bestand werkt, controleert AEM Desktop of een nieuwere versie van het bestand beschikbaar is in AEM. Als er een nieuwe versie beschikbaar is, downloadt de toepassing een nieuwe kopie van het bestand naar de lokale cache. AEM Desktop overschrijft een lokaal in de cache opgeslagen bestand echter niet als het is gewijzigd. Met deze functie voorkomt u dat uw werk per ongeluk wordt overschreven.

Wanneer hetzelfde bestand zowel lokaal als in AEM wordt gewijzigd, overschrijft de lokaal gewijzigde versie de versie in AEM. In dit geval is de vorige versie beschikbaar in de tijdlijn van het element. U kunt beide versies controleren en eventuele conflicten oplossen.

Als een lokaal bestand niet overeenkomt met de versie die beschikbaar is op de server, wordt in het statusdialoogvenster voor uploaden op de achtergrond melding gemaakt van het conflict. Open het conflicterende bestand en sla het op om het probleem op te lossen. Als u het bestand opslaat, synchroniseert AEM Desktop uw meest recente lokale wijzigingen met AEM. U kunt vorige versies van het element in de tijdlijn bekijken en eventuele conflicten oplossen.

Houd rekening met extra factoren wanneer meerdere gebruikers proberen te werken in afzonderlijke gekoppelde mappen die hetzelfde AEM-exemplaar als doel hebben. De volgende factoren zijn met name van belang:

* De hoeveelheid bandbreedte beschikbaar op het van gebruikers voortkomende netwerk
* Netwerkconfiguratie, zoals firewalls of proxy&#39;s, van het oorspronkelijke netwerk
* Hoeveelheid beschikbare bandbreedte in het netwerk van de doelinstantie van AEM
* Of een Dispatcher aanwezig is vóór de AEM-doelinstantie
* Huidige belasting op de AEM-doelinstantie

## Aanvullende AEM-configuraties {#additional-aem-configurations}

Als de WebDAV/SMB prestaties drastisch verminderen wanneer de veelvoudige gebruikers gelijktijdig werken, kunt u een paar dingen in AEM vormen, die kunnen helpen prestaties verbeteren.

## Workflows voor middelentransitie bijwerken {#update-asset-transient-workflows}

U kunt de AEM-prestaties verbeteren door tijdelijke workflows in te schakelen voor de DAM Update Asset-workflow. Als u tijdelijke workflows inschakelt, neemt de verwerkingscapaciteit af die nodig is om elementen bij te werken wanneer deze worden gemaakt of gewijzigd in AEM.

1. Navigeer naar `/miscadmin` in de Experience Manager-instantie (`https://[aem_server]:[port]/miscadmin` ).
1. Van de navigatieboom, breid **Hulpmiddelen** uit > **Werkschema** > **Modellen** > **Dam**.
1. Dubbelklik **DAM de Activa van de Update**.
1. Van het het drijven hulpmiddelpaneel, schakelaar aan het **lusje van de Pagina** en klik dan **Eigenschappen van de Pagina**.
1. Selecteer het **Tijdelijke de controlevakje van het Werkschema**, en klik **O.K.**.

### De wachtrij voor voorlopige Granite-werkstroom aanpassen {#adjust-granite-transient-workflow-queue}

Een andere methode om de prestaties van AEM te verbeteren is de waarde van de maximum parallelle banen voor de de baan van de Rij van de Rij van de Werkstroom van de Tijdelijke van Granite te te vormen. De aanbevolen waarde is ongeveer de helft van het aantal beschikbare CPU&#39;s bij de server. Voer de volgende stappen uit om de waarde aan te passen:

1. Navigeer naar `/system/console/configMgr` in de instantie AEM die moet worden geconfigureerd (bijvoorbeeld `https://[aem_server]:[port]/system/console/configMgr` ).
1. Onderzoek naar `QueueConfiguration`, en klik om elke baan te openen tot u van de **Granite 2} baan van de Rij van de Rij van het Werkschema van de Overgang {de plaats bepaalt, en** uitgeeft **klikt.**
1. Verander de `Maximum Parallel Jobs` waarde, en klik **sparen**.

## AWS-configuratie {#aws-configuration}

Vanwege de beperkingen van de netwerkbandbreedte kunnen de prestaties van WebDAV/SMB afnemen wanneer meerdere gebruikers gelijktijdig werken. Adobe raadt aan de AWS-instantie groter te maken voor een AEM-doelinstantie die op AWS wordt uitgevoerd om de prestaties van WebDAV/SMB te verbeteren.

Deze maatregel verhoogt specifiek de hoeveelheid netwerkbandbreedte beschikbaar aan de server. Hier volgen enkele details:

* De hoeveelheid netwerkbandbreedte die aan een instantie van AWS wordt gewijd stijgt aangezien de grootte van de instantie stijgt. Voor informatie over hoeveel bandbreedte voor elke instantiegrootte beschikbaar is, ga naar de [ documentatie van AWS ](https://aws.amazon.com/ec2/instance-types/).
* Bij het oplossen van problemen voor een grote cliënt, vormde Adobe de grootte van zijn instantie van AEM aan c4.8xlarge, hoofdzakelijk voor 4000 Mbps van specifieke bandbreedte die het verstrekt.
* Als er een Dispatcher voor de instantie AEM is, zorg ervoor dat het van aangewezen grootte is. Als de instantie van AEM 4000 Mbps verstrekt maar Dispatcher slechts 500 Mbps verstrekt, is de efficiënte bandbreedte slechts 500 Mbps. Dat komt omdat de Dispatcher een knelpunt in het netwerk maakt.

## Beperkingen van uitgecheckte bestanden {#checked-out-file-limitations}

Er zijn een paar bekende beperkingen in de manier dat u met uitgecheckte dossiers door Ontdekkingsreiziger/Vinder kunt in wisselwerking staan. Als een bestand is uitgecheckt, moet het alleen-lezen zijn voor iedereen behalve de gebruiker die het bestand heeft uitgecheckt. De implementatie van het WebDAV/SMB1-protocol in AEM dwingt deze regel af. Maar WebDAV/SMB-clients van het besturingssysteem communiceren vaak niet netjes met uitgecheckte bestanden. Enkele oddities worden hieronder beschreven.

### Algemeen {#general}

Bij het schrijven naar een uitgecheckt bestand wordt de vergrendeling alleen afgedwongen in de AEM WebDAV-implementatie. Daarom dwingen clients die WebDAV gebruiken, zoals een bureaubladtoepassing, alleen de vergrendeling in. Het slot wordt niet afgedwongen via de AEM-webinterface. In de AEM-interface wordt alleen een vergrendelingspictogram weergegeven in de kaartweergave voor elementen die zijn uitgecheckt. Het pictogram is cosmetisch en heeft geen invloed op het gedrag van AEM.

Over het algemeen gedragen de WebDAV-clients zich niet altijd zoals u had verwacht. Er kunnen nog andere problemen zijn. Het vernieuwen of controleren van het element in AEM is echter een goede manier om te controleren of een element niet wordt gewijzigd. Dit gedrag is typisch voor de OS cliënten WebDAV, die niet onder de controle van Adobe is.

### Windows {#windows}

Het verwijderen van een bestand lijkt te zijn gelukt omdat het bestand verdwijnt uit de bestandsverkenner in Windows. Als u echter de map vernieuwt en controleert in AEM Assets, ziet u dat het bestand nog steeds aanwezig is. Bovendien lijkt het bewerken van bestanden te zijn geslaagd (er worden geen waarschuwingsvensters of foutberichten weergegeven). Als u het bestand echter opnieuw opent of controleert in AEM Assets, wordt duidelijk dat het bestand ongewijzigd blijft.

#### MACOS X {#mac-os-x}

Bij het vervangen van een bestand wordt geen waarschuwing of fout weergegeven, maar bij het controleren van het element in AEM wordt duidelijk dat het bestand ongewijzigd blijft. Vernieuw of controleer het middel in AEM om te verifiëren dat het niet wordt gewijzigd.

## Problemen met het pictogram van de bureaubladtoepassing oplossen (macOS X) {#troubleshooting-desktop-app-icon-issues-mac-os-x}

Nadat u de bureaubladtoepassing hebt geïnstalleerd, verschijnt het pictogram van het menu voor de bureaubladtoepassing in de menubalk. Als het pictogram niet wordt weergegeven, voert u de volgende stappen uit om het probleem op te lossen:

1. Open het eindvenster van het besturingssysteem.
1. Typ het volgende bevel bij de bevelherinnering, en druk dan binnengaan:

   ```shell
    cd ../Library/Caches.
   ```

1. Typ de volgende opdracht en druk op Enter:

   ```shell
   rm -r com.adobe.aem.assetscompanion
   ```

1. Typ de volgende opdracht en druk op Enter:

   ```shell
   cd ~/Library/Preferences
   ```

1. Typ de volgende opdracht en druk op Enter:

   ```shell
   rm com.adobe.aem.assetscompanion.plist
   ```

1. Typ de volgende opdracht en druk op Enter:

   ```shell
   rm ~/Library/Group\ Containers/group.com.adobe.aem.desktop/*
   ```

1. Start het systeem opnieuw.

AEM Desktop probeert een bestand drie keer te synchroniseren. Als het bestand na de derde poging niet kan worden gesynchroniseerd, beschouwt AEM Desktop het bestand als een conflict en wordt u via het statusvenster voor uploaden op de achtergrond op de hoogte gebracht. Een conflictstatus geeft aan dat de laatste wijzigingen nog steeds lokaal beschikbaar zijn, maar niet naar AEM worden gesynchroniseerd. De AEM-bureaubladtoepassing probeert niet meer te synchroniseren.

U kunt deze situatie het eenvoudigst verhelpen door het conflicterende bestand te openen en opnieuw op te slaan. Het dwingt AEM Desktop om synchronisatie nog eens drie keer te proberen. Raadpleeg de onderstaande secties voor meer informatie als het bestand nog steeds niet kan worden gesynchroniseerd.

## AEM Desktop cache wissen {#clearing-aem-desktop-cache}

Het wissen van het cachegeheugen van AEM Desktop is een voorlopige taak voor het oplossen van problemen die verschillende AEM Desktop-problemen kan oplossen.

U kunt de cache wissen door de cachemap van de toepassing op de volgende locaties te verwijderen.
In Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\`

In Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/`

De locatie kan echter veranderen afhankelijk van het geconfigureerde AEM-eindpunt van AEM Desktop. De waarde is een gecodeerde versie van de beoogde URL. Als de toepassing bijvoorbeeld `http://localhost:4502` als doel instelt, is de mapnaam `http%3A%2F%2Flocalhost%3A4502%2F` .

Als u de cache wilt wissen, verwijdert u de map &lt;Encoded AEM Endpoint>.

>[!NOTE]
>
>Als u de AEM Desktop-cache wist, gaan lokale bestandswijzigingen verloren als deze niet naar AEM worden gesynchroniseerd.

>[!NOTE]
>
>Vanaf AEM desktop app versie 1.5 is er een optie in de gebruikersinterface om de cache te wissen.

## AEM Desktop-versie zoeken {#finding-the-aem-desktop-version}

De procedure om de versie van AEM Desktop te controleren is hetzelfde voor zowel Windows als macOS.

Klik het pictogram van de Desktop van AEM, en kies dan **Ongeveer**. Het versienummer wordt op het scherm weergegeven.

## De AEM-bureaubladtoepassing op macOS upgraden {#upgrading-aem-desktop-app-on-macos}

Soms kunnen er problemen optreden wanneer u de AEM-bureaubladtoepassing op macOS upgradet. Deze problemen worden veroorzaakt door verouderde systeemmappen voor de AEM-bureaubladtoepassing. Zo voorkomt u dat nieuwe versies van AEM Desktop correct worden geladen. U kunt dit probleem verhelpen door de volgende mappen en bestanden handmatig te verwijderen.

Voordat u de onderstaande stappen uitvoert, sleept u de toepassing Adobe Experience Manager Desktop van de map macOS Applications naar de prullenmand. Open vervolgens de terminal en voer de volgende opdracht uit, waarbij u uw wachtwoord opgeeft wanneer hierom wordt gevraagd.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## Een bestand opslaan dat door anderen is uitgecheckt {#saving-a-file-checked-out-by-others}

De technische beperkingen van het besturingssysteem verhinderen dat gebruikers een consistente ervaring hebben met het overschrijven van een bestand dat anderen hebben uitgecheckt. De ervaring varieert afhankelijk van de toepassing die wordt gebruikt om het uitgecheckte bestand te bewerken. Soms wordt in de toepassing een foutbericht weergegeven dat een schrijffout van een schijf aangeeft of dat een schijnbaar niet-verwante of algemene fout wordt weergegeven. In andere gevallen wordt geen foutbericht weergegeven en lijkt de bewerking te zijn geslaagd.

In dat geval kan bij het sluiten en opnieuw openen van het bestand blijken dat de inhoud ongewijzigd blijft. Sommige toepassingen kunnen echter een back-up van het bestand opslaan, zodat de wijzigingen kunnen worden toegepast.

Het bestand blijft ongewijzigd wanneer u het incheckt, ongeacht het gedrag. Zelfs als een andere versie van het bestand wordt weergegeven, worden de wijzigingen niet gesynchroniseerd met AEM.

## Problemen met het verplaatsen van bestanden oplossen {#troubleshooting-problems-around-moving-files}

De server-API vereist extra kopballen, x-Bestemming, x-Diepte, en x-Overschrijf, om worden overgegaan voor de beweging en exemplaarverrichtingen om te werken. De Dispatcher geeft deze headers standaard niet door, waardoor deze bewerkingen mislukken. Voor meer informatie, zie [ Verbindend met AEM Achter Dispatcher ](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher).

## Problemen met de AEM Desktop-verbinding oplossen {#troubleshooting-aem-desktop-connection-issues}

### SAML-omleiding {#saml-redirect-issue}

De gemeenschappelijkste reden voor kwesties met de Desktop van AEM die met uw SSO-Toegelaten (SAML) AEM instantie verbinden is dat het proces SAML niet naar het oorspronkelijk gevraagde weg opnieuw richt. De verbinding kan ook worden omgeleid naar een host die niet is geconfigureerd in de AEM-bureaubladtoepassing. Voer de volgende stappen uit om het aanmeldingsproces te verifiëren:

1. Open een webbrowser.
1. Geef in de adresbalk de URL op `/content/dam.json` .
1. Vervang de URL door de AEM-doelinstantie, bijvoorbeeld `https://localhost:4502/content/dam.json` .
1. Meld u aan bij AEM.
1. Controleer na het aanmelden het huidige adres van de browser in de adresbalk. Deze moet overeenkomen met de URL die u oorspronkelijk hebt ingevoerd.
1. Controleer of alles voordat `/content/dam.json` overeenkomt met de AEM-doelwaarde die in AEM Desktop is geconfigureerd.

### Probleem met SSL-configuratie {#ssl-configuration-issue}

De bibliotheken die de AEM-bureaubladtoepassing gebruikt voor HTTP-communicatie, maken gebruik van strikte SSL-handhaving. Soms kan een verbinding met een browser slagen, maar kan de AEM-bureaubladtoepassing niet worden gebruikt. Installeer het ontbrekende tussentijdse certificaat in Apache om SSL op de juiste wijze te configureren. Zie [ hoe te om een Tussentijdse cert van CA in Apache ](https://access.redhat.com/solutions/43575) te installeren.

## AEM Desktop gebruiken met Dispatcher {#using-aem-desktop-with-dispatcher}

AEM Desktop werkt met AEM-implementaties achter een Dispatcher. Dit is een standaard en aanbevolen configuratie voor AEM-servers. AEM-verzenders vóór AEM-ontwerpomgevingen zijn doorgaans geconfigureerd om DAM-elementen in cache over te slaan. Daarom bieden verzenders geen extra caching vanuit het AEM Desktop-standpunt. Zorg ervoor dat de Dispatcher-configuratie is aangepast aan de AEM Desktop. Voor extra details, zie [ Verbindend met AEM met Dispatcher ](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher).

## Controleren op logbestanden {#checking-for-log-files}

Afhankelijk van uw besturingssysteem kunt u de logbestanden voor AEM Desktop op de volgende locaties vinden:

* Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`
* Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`
