---
title: Beste praktijken voor en het oplossen van problemen  [!DNL Adobe Experience Manager]  Desktop app
description: Volg de beste praktijken en los problemen op om de af en toe met installatie, verbetering, configuratie, etc. verband houdende kwesties op te lossen.
exl-id: f388e4ac-907d-4093-ba6f-86ecdafeb015
source-git-commit: a8cb0aaab08f24c83a9b5640a96a5ae8895685d2
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 0%

---

# Troubleshoot [!DNL Adobe Experience Manager] desktop app {#troubleshoot-v2}

[!DNL Adobe Experience Manager] maakt verbinding met een DAM-opslagplaats (Digital Asset Management) van een [!DNL Experience Manager] -implementatie. De app haalt opslaggegevens en zoekresultaten op uw computer op, downloadt en uploadt bestanden en mappen en bevat mogelijkheden om conflicten met de Assets-gebruikersinterface te beheren.

Lees verder om de app problemen op te lossen, de beste werkwijzen te leren en de beperkingen uit te zoeken.

## Aanbevolen procedures {#best-practices-to-prevent-troubles}

Houd u aan de volgende aanbevolen procedures om bepaalde algemene problemen en problemen te voorkomen.

* **Begrijp hoe Desktop app** werkt: Alvorens te beginnen om de toepassing te gebruiken, besteed een paar ogenblikken het kennen van hoe app werkt. U weet hoe u een koppeling tot stand brengt tussen de webinterface van [!DNL Experience Manager] en het bureaublad, de toewijzing van opslagruimten, het in cache plaatsen van elementen, het lokaal opslaan en het uploaden op de achtergrond. Zie [&#x200B; hoe het &#x200B;](release-notes.md#how-app-works) werkt.

* **vermijd niet gesteunde karakters in omslagnamen**: Gebruik geen whitespaces en ongeldige karakters wanneer het creëren van of het uploaden van omslagen. Zie een lijst van karakters bij [&#x200B; leiden omslagen in  [!DNL Adobe Experience Manager Assets] &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-65/content/assets/managing/manage-assets#creating-folders). Niet-ondersteunde tekens in de mapnaam kunnen van invloed zijn op bepaalde gebruiksgevallen van [!DNL Experience Manager] .

* **Beste praktijken om conflicten** te vermijden: Om potentiële conflicten te vermijden wanneer het samenwerken op veelvoudige activa, ga [&#x200B; vermijden het uitgeven conflicten &#x200B;](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts).

* **de omslagupload van het Gebruik voor grote, hiërarchische omslagen**: In plaats van het gebruiken van de het Webinterface van Assets of andere methodes, gebruik [!DNL Experience Manager] Desktop app om grote omslagen te uploaden. De app uploadt de middelen op de achtergrond met registratie en controle. Zie [&#x200B; bulkupload activa &#x200B;](using-desktop-app.md#bulk-upload-assets).

* **Gebruik de recentste versie**: Gebruik de recentste toepassingsversie. Controleer altijd op compatibiliteit voordat u een nieuwe app-versie installeert of voordat u een upgrade naar een nieuwere [!DNL Experience Manager] versie uitvoert. Zie [&#x200B; versienota&#39;s &#x200B;](release-notes.md).

* **gebruik de zelfde aandrijvingsbrief**: Gebruik de zelfde aandrijvingsbrief over een organisatie om aan [!DNL Experience Manager] DAM in kaart te brengen. Als u elementen wilt zien die door andere gebruikers zijn geplaatst, moeten de paden gelijk zijn. Als u dezelfde stationsletter gebruikt, bent u verzekerd van een constant pad naar DAM-middelen. De elementen blijven geplaatst en worden niet verwijderd, zelfs niet als verschillende stationsletters door verschillende gebruikers worden gebruikt.

* **Herinner het netwerk**: De prestaties van het netwerk zijn kritiek aan [!DNL Experience Manager] prestaties van Desktop app. Als u te maken krijgt met een trage reactie op bestandsoverdrachten of bulkbewerkingen, schakelt u de functies of toepassingen uit die veel netwerkverkeer kunnen veroorzaken.

* **Niet gestaafde gebruiksgevallen voor Desktop app**: Gebruik geen app voor activamigratie, aangezien het planning en extra hulpmiddelen vereist. Het is ook niet geschikt voor zware DAM-bewerkingen, zoals het verplaatsen van grote mappen, grote uploads of geavanceerde metagegevenszoekopdrachten. Gebruik de software bovendien niet als een synchronisatieclient, omdat de ontwerpprincipes en gebruikspatronen verschillen van synchronisatieclients zoals Microsoft OneDrive of Adobe Creative Cloud desktop sync.

* **Tijd uit**: Momenteel, heeft Desktop app geen configureerbare onderbrekingswaarde die de verbinding tussen [!DNL Experience Manager] server en Desktop app na een vast tijdinterval losmaakt. Wanneer u grote middelen uploadt en de verbinding na een tijdje wordt verbroken, probeert de toepassing het element een paar keer te uploaden door de time-out van het uploaden te verhogen. Er is geen aanbevolen manier om de standaardtime-outinstellingen te wijzigen.

## Hoe te om problemen op te lossen {#troubleshooting-prep}

Houd rekening met de volgende informatie als u problemen met bureaubladtoepassingen wilt oplossen. Bovendien is het programma klaar om de problemen beter door te geven aan de klantenondersteuning van Adobe als u ervoor kiest om ondersteuning te zoeken.

### Locatie van logbestanden {#check-log-files-v2}

De bureaubladtoepassing van [!DNL Experience Manager] slaat de logbestanden van de toepassing op de volgende locaties op, afhankelijk van het besturingssysteem:

In Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

Op Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

Wanneer u een groot aantal elementen uploadt, raadpleegt u `backend.log` bestand om te zien of het uploaden is mislukt.

>[!NOTE]
>
>Wanneer u met de klantenondersteuning van Adobe werkt aan een ondersteuningsverzoek of -ticket, kunt u worden gevraagd om de logbestanden te delen om het team van Klantenondersteuning te helpen het probleem te begrijpen. Archiveer de volledige map `Logs` en deel deze met uw contactpersoon voor klantenondersteuning.

### Detailniveau in logbestanden wijzigen {#level-of-details-in-log}

U wijzigt als volgt het detailniveau in logbestanden:

1. Zorg ervoor dat de toepassing niet wordt uitgevoerd.

1. Op Windows-systeem:

   1. Open een opdrachtvenster.

   1. Start de bureaubladtoepassing van [!DNL Adobe Experience Manager] met de opdracht:

   ```shell
   set AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe
   ```

   Op Mac-systeem:

   1. Open een terminalvenster.

   1. Start de bureaubladtoepassing van [!DNL Adobe Experience Manager] met de opdracht:

   ```shell
   AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app
   ```

De geldige logboekniveaus zijn DEBUG, INFO, WARN, of FOUT. De breedste logboeken zijn het hoogst in DEBUG en het laagste in FOUT.

### Foutopsporingsmodus inschakelen {#enable-debug-mode}

Als u problemen wilt oplossen, kunt u de foutopsporingsmodus inschakelen en meer informatie in de logboeken opnemen.

>[!NOTE]
>
>Geldige logboekniveaus zijn DEBUG, INFO, WARN, of FOUT. De breedste logboeken zijn het hoogst in DEBUG en het laagste in FOUT.

De toepassing in de foutopsporingsmodus van Mac gebruiken:

1. Open een eindvenster of een bevelherinnering.

1. Start de bureaubladtoepassing van [!DNL Experience Manager] met de volgende opdracht:

   `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`.

De foutopsporingsmodus in Windows inschakelen:

1. Open een opdrachtvenster.

1. Start de bureaubladtoepassing van [!DNL Experience Manager] met de volgende opdracht:

`AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe`.

### De versie van de [!DNL Adobe Experience Manager] desktop-app kennen {#know-app-version-v2}

Het versienummer weergeven:

1. Start de toepassing.

1. Klik op de ellipsen in de rechterbovenhoek, houd de cursor boven [!UICONTROL Help] en klik vervolgens op [!UICONTROL About] .

   Het versienummer wordt weergegeven op dit scherm.

### Cache wissen {#clear-cache-v2}

Voer de volgende stappen uit:

1. Start de toepassing en maak verbinding met een instantie van [!DNL Experience Manager] .

1. Open de voorkeuren van de toepassing door op de ovalen in de rechterbovenhoek te klikken en [!UICONTROL Preferences] te selecteren.

1. Zoek het item met de [!UICONTROL Current Cache Size] . Klik op het prullenbakpictogram naast dit element.

Ga als volgt te werk om de cache handmatig te wissen:

>[!CAUTION]
>
>Deze stappen kunnen een destructieve bewerking zijn. Als er lokale bestandswijzigingen zijn die niet naar [!DNL Adobe Experience Manager] worden geüpload, gaan deze wijzigingen verloren.

De cache wordt gewist door de cachemap van de toepassing te verwijderen. Deze map staat in de voorkeuren van de toepassing.

1. Start de toepassing.

1. Open de voorkeuren van de toepassing door de ovalen in de rechterbovenhoek te selecteren en [!UICONTROL Preferences] te selecteren.

1. Noteer de waarde [!UICONTROL Cache Directory] .

   In deze map staan submappen die naar de gecodeerde [!DNL Adobe Experience Manager] eindpunten worden genoemd. De namen zijn een gecodeerde versie van de beoogde [!DNL Adobe Experience Manager] URL. Als de toepassing bijvoorbeeld `localhost:4502` als doel instelt, is de mapnaam `localhost_4502` .

Als u de cache wilt wissen, verwijdert u de gewenste gecodeerde [!DNL Adobe Experience Manager] Eindpuntmap. Als u de volledige map verwijdert die u in de voorkeuren hebt opgegeven, wordt de cache ook gewist voor alle instanties die door de toepassing zijn gebruikt.

Het wissen van de cache van de [!DNL Adobe Experience Manager] -bureaubladtoepassing is een voorlopige taak voor het oplossen van problemen die verschillende problemen kan oplossen. Wis de cache uit de toepassingsvoorkeuren. Zie [&#x200B; vastgestelde voorkeur &#x200B;](install-upgrade.md#set-preferences). De standaardlocatie van de cachemap is:

## Kan geplaatste elementen niet zien {#placed-assets-missing}

Controleer het volgende als u niet kunt zien welke elementen u of andere creatieve professionals in de ondersteuningsbestanden hebben geplaatst (bijvoorbeeld INDD-bestanden):

* Verbinding maken met de server. De Flash-netwerkconnectiviteit kan het downloaden van bedrijfsmiddelen blokkeren.

* Bestandsgrootte. Het downloaden en weergeven van grote elementen duurt langer.

* Stationsconsistentie. Als u of een andere medewerker de elementen heeft geplaatst terwijl u de [!DNL Experience Manager] DAM toewijst aan een andere stationsletter, worden de geplaatste elementen niet weergegeven.

* Rechten. Neem contact op met de [!DNL Experience Manager] -beheerder om te controleren of u machtigingen hebt om de geplaatste elementen op te halen.

### Bewerkingen aan bestanden in de gebruikersinterface van de bureaubladtoepassing worden niet meteen weerspiegeld in [!DNL Adobe Experience Manager] . {#changes-on-da-not-visible-on-aem}

[!DNL Adobe Experience Manager] laat de gebruiker beslissen wanneer alle bewerkingen van een bestand zijn voltooid. Afhankelijk van de grootte en complexiteit van een bestand duurt het erg lang om de nieuwe versie van een bestand terug te sturen naar [!DNL Adobe Experience Manager] . De toepassing is ontworpen om het aantal bestandsoverdrachten te minimaliseren, in plaats van automatisch bestanden te uploaden op basis van geraden voltooiing van bewerkingen. De gebruiker wordt geadviseerd de overdracht van het bestand terug naar [!DNL Adobe Experience Manager] te starten door de wijzigingen van een bestand te uploaden.

### Problemen bij upgraden op macOS {#issues-when-upgrading-on-macos}

Soms kunnen er problemen optreden wanneer u de [!DNL Experience Manager] -bureaubladtoepassing op macOS upgradet. Deze problemen worden veroorzaakt door verouderde systeemmappen voor de [!DNL Experience Manager] -bureaubladtoepassing. De mappen verhinderen dat nieuwe versies van de bureaubladtoepassing van [!DNL Experience Manager] correct worden geladen. U kunt dit probleem verhelpen door de volgende mappen en bestanden handmatig te verwijderen.

Voordat u de volgende stappen uitvoert, sleept u de `Adobe Experience Manager Desktop` -toepassing van de map macOS Applications naar de prullenmand. Dan open de terminal, stel het volgende bevel in werking, en verstrek uw wachtwoord wanneer ertoe aangezet.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## Kan bestanden niet uploaden {#upload-fails}

Als u de bureaubladtoepassing gebruikt met [!DNL Experience Manager] 6.5.1 of hoger, moet u de S3- of Azure-aansluiting upgraden naar versie 1.10.4 of hoger. Het lost het dossier op uploadt mislukkingskwestie met betrekking tot [&#x200B; OAK-8599 &#x200B;](https://issues.apache.org/jira/browse/OAK-8599). Zie [&#x200B; instructies &#x200B;](install-upgrade.md#install-v2) installeren.

## [!DNL Experience Manager] Verbindingsproblemen met bureaubladtoepassingen {#connection-issues}

Als u algemene connectiviteitsproblemen ondervindt, kunt u op verschillende manieren meer informatie krijgen over wat de [!DNL Experience Manager] -bureaubladtoepassing doet.

**Controle het verzoeklogboek**

De desktop-app van [!DNL Experience Manager] registreert alle aanvragen die het samen met de antwoordcode van elke aanvraag in een toegewezen logbestand verzendt.

1. Open `request.log` in de logmap van de toepassing om deze verzoeken te zien.

1. Elke lijn in het logboek vertegenwoordigt of een verzoek of een reactie. Aanvragen hebben een `>` teken gevolgd door de gewenste URL. Reacties hebben een `<` -teken gevolgd door de antwoordcode en de URL die is aangevraagd. De verzoeken en de Reactie kunnen worden aangepast gebruikend GUID van elke lijn.

**de verzoeken van de Controle die door ingebedde browser van de toepassing** worden geladen

Een meerderheid van de verzoeken van de toepassing wordt gevonden in het verzoeklogboek. Als er echter geen nuttige informatie beschikbaar is, kan het nuttig zijn om te kijken naar de aanvragen die door de ingesloten browser van de toepassing worden verzonden.
Zie de [&#x200B; sectie van SAML &#x200B;](#da-connection-issue-with-saml-aem) voor instructies op hoe te om die verzoeken te bekijken.

### SAML-aanmeldverificatie werkt niet {#da-connection-issue-with-saml-aem}

[!DNL Experience Manager] -bureaubladtoepassing maakt mogelijk geen verbinding met uw SAML-implementatie (SSO-enabled) [!DNL Adobe Experience Manager] . Het ontwerp van de toepassing probeert de variaties en de complexiteit van SSO-verbindingen en -processen aan te passen. Voor een setup is mogelijk aanvullende probleemoplossing vereist.

Soms richt het proces SAML niet terug naar de oorspronkelijk gevraagde weg. De uiteindelijke omleiding is ook naar een andere host dan de host die is geconfigureerd in de bureaubladtoepassing van [!DNL Adobe Experience Manager] . Ga als volgt te werk om te controleren of dit probleem niet het geval is:

1. Open een webbrowser. Open de URL van `https://[aem_server]:[port]/content/dam.json` .

1. Meld u aan bij de implementatie van [!DNL Adobe Experience Manager] .

1. Wanneer login volledig is, bekijk het huidige adres van browser in de adresbar. Deze moet exact overeenkomen met de URL die oorspronkelijk is ingevoerd.

1. Controleer ook of alles voordat `/content/dam.json` overeenkomt met de [!DNL Adobe Experience Manager] target-waarde die is geconfigureerd in de instellingen van de [!DNL Adobe Experience Manager] -bureaubladtoepassing.

**Login het proces van SAML werkt correct volgens de bovengenoemde stappen, maar de gebruikers kunnen nog niet** aanmelden

Het venster binnen de bureaubladtoepassing van [!DNL Adobe Experience Manager] waarin het aanmeldingsproces wordt weergegeven, is gewoon een webbrowser die de webgebruikersinterface van de doelinstantie van [!DNL Adobe Experience Manager] weergeeft:

* De versie van Mac gebruikt a [&#x200B; WebView &#x200B;](https://developer.apple.com/documentation/webkit/webview).

* De versie van Vensters gebruikt op chroom-Gebaseerde [&#x200B; CefSharp &#x200B;](https://cefsharp.github.io/).

Zorg ervoor dat het SAML-proces deze browsers ondersteunt.

Als u meer problemen wilt oplossen, kunt u de exacte URL&#39;s bekijken die de browser probeert te laden. Deze informatie bekijken:

1. Volg de richtingen voor het lanceren van de toepassing op [&#x200B; zuivert wijze &#x200B;](#enable-debug-mode).

1. Reproduceer de login poging.

1. Navigeer aan de [&#x200B; logboekfolder &#x200B;](#check-log-files-v2) van de toepassing.

1. Voor Windows:

   1. Open &quot;aemcompanionlog.txt.&quot;

   1. Zoek naar berichten die met &quot;Login browser adres veranderd in&quot;beginnen. Deze vermeldingen bevatten ook de URL die de toepassing heeft geladen.

   Voor Mac:

   1. In `com.adobe.aem.desktop-nnnnnnnn-nnnnnn.log`, vervangen welke aantallen in het nieuwste dossier zijn - naam **n**.

   1. Zoek naar berichten die met &quot;geladen kader&quot;beginnen. Deze vermeldingen bevatten ook de URL die de toepassing heeft geladen.

Het bekijken van de opeenvolging URL die wordt geladen kan helpen bij het eind van SAML problemen oplossen om te bepalen wat verkeerd is.

### Probleem met SSL-configuratie {#ssl-config-v2}

De bibliotheken die de bureaubladtoepassing van [!DNL Experience Manager] gebruikt voor HTTP-communicatie, maken gebruik van strikte SSL-afgedwongen omzetting. Soms kan een verbinding met een browser slagen, maar mislukt het gebruik van de bureaubladtoepassing van [!DNL Experience Manager] . Installeer het ontbrekende tussentijdse certificaat in Apache om SSL op de juiste wijze te configureren. Zie [&#x200B; hoe te om een Tussentijdse cert van CA in Apache &#x200B;](https://access.redhat.com/solutions/43575) te installeren.

De bibliotheken die de bureaubladtoepassing van [!DNL Experience Manager] gebruikt voor HTTP-communicatie, maken gebruik van strikte SSL-afgedwongen omzetting. Er kunnen zich dus situaties voordoen waarin SSL-verbindingen die via een browser slagen, mislukken met de bureaubladtoepassing van [!DNL Adobe Experience Manager] . Dit resultaat is goed omdat het de juiste configuratie van SSL aanmoedigt en de beveiliging verhoogt, maar het kan frustrerend zijn wanneer de toepassing geen verbinding kan maken.

In dit geval kunt u het beste een hulpprogramma gebruiken om het SSL-certificaat van een server te analyseren en problemen te identificeren zodat deze kunnen worden gecorrigeerd. Er zijn Websites die het certificaat van een server inspecteren door zijn URL te verstrekken.

Als een tijdelijke maatregel, is het mogelijk om strikte SSL handhaving in de [!DNL Adobe Experience Manager] Desktop app onbruikbaar te maken. Deze benadering is geen geadviseerde oplossing op lange termijn, aangezien het veiligheid vermindert door de worteloorzaak van verkeerd gevormde SSL te verbergen. Strikte handhaving uitschakelen:

1. Gebruik de editor van uw keuze om het JavaScript-configuratiebestand van de toepassing te bewerken. Dit bestand bevindt zich standaard op de volgende locaties (afhankelijk van het besturingssysteem):

   Op Mac: `/Applications/Adobe Experience Manager Desktop.app/Contents/Resources/javascript/lib-smb/config.json`

   In Windows: `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop\javascript\config.json`

1. Zoek de volgende sectie in het bestand:

   ```shell
   ...
   "assetRepository": {
       "options": {
   ...
   ```

1. Wijzig de sectie door `"strictSSL": false` als volgt toe te voegen:

   ```shell
   ...
   "assetRepository": {
       "options": {
           "strictSSL": false,
   ...
   ```

1. Sla het bestand op en start de bureaubladtoepassing van [!DNL Adobe Experience Manager] opnieuw.

### Aanmeldingsproblemen bij overschakelen naar een andere server {#cannot-login-cookies-issue}

Wanneer u een [!DNL Experience Manager] -server gebruikt en probeert de verbinding te wijzigen met een andere server, kunnen er aanmeldingsproblemen optreden. Dit is te wijten aan oude cookies die de nieuwe verificatie belemmeren. Een optie in het hoofdmenu die [!UICONTROL Clear Cookies] helpt. Meld u af bij de huidige sessie in de app en selecteer [!UICONTROL Clear Cookies] voordat u verdergaat met het maken van een verbinding.

![&#x200B; Duidelijke koekjes wanneer omschakelingsserver &#x200B;](assets/main_menu_logout_da2.png)

## App reageert niet {#unresponsive}

In zeldzame gevallen reageert de toepassing niet meer, wordt alleen een wit scherm weergegeven of wordt een fout onder aan de interface weergegeven zonder opties in de interface. Probeer het volgende in de volgorde:

* Klik met de rechtermuisknop op de toepassingsinterface en klik op **[!UICONTROL Refresh]** .
* Sluit de toepassing af en open deze opnieuw.

In beide methoden wordt de toepassing gestart in de hoofdmap DAM.

## Verlopen elementen verbergen {#hide-expired-assets}

Wanneer u elementen bladert vanuit de gebruikersinterface van [!DNL Experience Manager] , worden de verlopen elementen niet weergegeven. Beheerders kunnen instellingen configureren om te voorkomen dat verlopen middelen worden weergegeven, gezocht en opgehaald wanneer ze de bureaubladtoepassing en de Asset Link verlaten. Dit zorgt ervoor dat verlopen elementen tijdens deze bewerkingen niet toegankelijk zijn. De configuratie werkt voor alle gebruikers, ongeacht beheerderrechten.

* [&#x200B; Configuratie in Experience Manager 6.5 om verlopen activa &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-65/content/assets/managing/manage-assets#hide-expired-assets-via-acp-api) te verbergen.
* [&#x200B; Configuratie in Experience Manager as a Cloud Service om verlopen activa &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets#hide-expired-assets-via-acp-api) te verbergen.

<!--
### Need additional help with [!DNL Experience Manager] desktop app {#additional-help}

Create Jira ticket with the following information:

* Use `DAM - Companion App` as the [!UICONTROL Component].

* Detailed steps to reproduce the issue in [!UICONTROL Description].

* DEBUG level logs that were captured while reproducing the issue.

* Target Experience Manager version.

* Operating system version.

* [!DNL Adobe Experience Manager] desktop app version. To know your app version, see [finding the desktop app version](#know-app-version-v2).
-->

>[!MORELIKETHIS]
>
>* [&#x200B; Bekende kwesties &#x200B;](release-notes.md#known-issues-v2)
>* [&#x200B; vermijd het uitgeven conflicten &#x200B;](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts)
