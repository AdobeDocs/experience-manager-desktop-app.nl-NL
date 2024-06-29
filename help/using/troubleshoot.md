---
title: Aanbevolen werkwijzen voor en probleemoplossing [!DNL Adobe Experience Manager] bureaubladtoepassing
description: Volg de beste praktijken en los problemen op om de af en toe met installatie, verbetering, configuratie, etc. verband houdende kwesties op te lossen.
exl-id: f388e4ac-907d-4093-ba6f-86ecdafeb015
source-git-commit: 5676e7ece8bb43f051dae72d17e15ab1c34caefc
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 0%

---

# Problemen oplossen [!DNL Adobe Experience Manager] bureaubladtoepassing {#troubleshoot-v2}

[!DNL Adobe Experience Manager] bureaubladtoepassing maakt verbinding met een [!DNL Experience Manager] de DAM-opslagplaats (Digital Asset Management) van de implementatie. De app haalt opslaggegevens en zoekresultaten op uw computer op, downloadt en uploadt bestanden en mappen en bevat mogelijkheden om conflicten met de Assets-gebruikersinterface te beheren.

Lees verder om de app problemen op te lossen, de beste werkwijzen te leren en de beperkingen uit te zoeken.

## Aanbevolen procedures {#best-practices-to-prevent-troubles}

Houd u aan de volgende aanbevolen procedures om bepaalde algemene problemen en problemen te voorkomen.

* **Begrijp hoe de bureaubladtoepassing werkt**: Voordat u de toepassing gaat gebruiken, moet u even weten hoe de app werkt. Weet hoe u het verband tussen de [!DNL Experience Manager] webinterface en desktop, repository mapping, asset caching, lokaal opslaan en uploaden op de achtergrond. Zie [hoe het werkt](release-notes.md#how-app-works).

* **Niet-ondersteunde tekens in mapnamen voorkomen**: Gebruik geen spaties en ongeldige tekens bij het maken of uploaden van mappen. Een lijst met tekens bekijken op [Mappen maken in [!DNL Adobe Experience Manager Assets]](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/managing/manage-assets#creating-folders). Niet-ondersteunde tekens in de mapnaam kunnen van invloed zijn op sommige [!DNL Experience Manager] gebruik.

* **Tips en trucs om conflicten te voorkomen**: Ga naar [bewerkingsconflicten vermijden](using.md#adv-workflow-collaborate-avoid-conflicts).

* **Mapupload gebruiken voor grote, hiërarchische mappen**: Gebruik in plaats van de Assets-webinterface of andere methoden de opdracht [!DNL Experience Manager] bureaubladtoepassing om grote mappen te uploaden. De app uploadt de middelen op de achtergrond met registratie en controle. Zie [bulkupload-elementen](using.md#bulk-upload-assets).

* **De nieuwste versie gebruiken**: Gebruik de nieuwste versie van de app. Controleer altijd op compatibiliteit voordat u een nieuwe app-versie installeert of voordat u een upgrade naar een nieuwere [!DNL Experience Manager] versie. Zie [releaseopmerkingen](release-notes.md).

* **Dezelfde stationsletter gebruiken**: Gebruik dezelfde stationsletter in een organisatie om aan de [!DNL Experience Manager] DAM. Als u elementen wilt zien die door andere gebruikers zijn geplaatst, moeten de paden gelijk zijn. Als u dezelfde stationsletter gebruikt, bent u verzekerd van een constant pad naar DAM-middelen. De elementen blijven geplaatst en worden niet verwijderd, zelfs niet als verschillende stationsletters door verschillende gebruikers worden gebruikt.

* **Het netwerk onthouden**: Netwerkprestaties zijn essentieel voor [!DNL Experience Manager] prestaties van de bureaubladtoepassing. Als u te maken krijgt met een trage reactie op bestandsoverdrachten of bulkbewerkingen, schakelt u de functies of toepassingen uit die veel netwerkverkeer kunnen veroorzaken.

* **Niet-ondersteunde gebruiksgevallen voor bureaubladtoepassing**: Gebruik de app niet voor het migreren van bedrijfsmiddelen, omdat hiervoor planning en aanvullende hulpmiddelen nodig zijn. Het is ook niet geschikt voor zware DAM-bewerkingen, zoals het verplaatsen van grote mappen, grote uploads of geavanceerde metagegevenszoekopdrachten. Gebruik de software bovendien niet als een synchronisatieclient, omdat de ontwerpprincipes en gebruikspatronen verschillen van synchronisatieclients zoals Microsoft OneDrive of Adobe Creative Cloud desktop sync.

* **Time-out**: De desktop-app heeft momenteel geen configureerbare time-outwaarde die de verbinding verbreekt tussen [!DNL Experience Manager] de server en de Desktop app na een vast tijdinterval. Wanneer u grote middelen uploadt en de verbinding na een tijdje wordt verbroken, probeert de toepassing het element een paar keer te uploaden door de time-out van het uploaden te verhogen. Er is geen aanbevolen manier om de standaardtime-outinstellingen te wijzigen.

## Hoe te om problemen op te lossen {#troubleshooting-prep}

Houd rekening met de volgende informatie als u problemen met bureaubladtoepassingen wilt oplossen. Bovendien is het programma klaar om de problemen beter door te geven aan de Adobe Klantenondersteuning als u ervoor kiest om ondersteuning te zoeken.

### Locatie van logbestanden {#check-log-files-v2}

De [!DNL Experience Manager] de logbestanden van de bureaubladtoepassing worden op de volgende locaties opgeslagen, afhankelijk van het besturingssysteem:

In Windows: `%LocalAppData%\Adobe\AssetsCompanion\Logs`

Op Mac: `~/Library/Logs/Adobe\ Experience\ Manager\ Desktop`

Als bij het uploaden van een groot aantal elementen sommige bestanden niet worden geüpload, raadpleegt u `backend.log` bestand om de mislukte uploads te identificeren.

>[!NOTE]
>
>Wanneer u met de klantenondersteuning van de Adobe werkt aan een ondersteuningsverzoek of -ticket, kunt u worden gevraagd om de logbestanden te delen om het team van Klantenondersteuning te helpen het probleem te begrijpen. Het gehele archief `Logs` en deze delen met uw contactpersoon voor klantenondersteuning.

### Detailniveau in logbestanden wijzigen {#level-of-details-in-log}

U wijzigt als volgt het detailniveau in logbestanden:

1. Zorg ervoor dat de toepassing niet wordt uitgevoerd.

1. Op Windows-systeem:

   1. Open een opdrachtvenster.

   1. De [!DNL Adobe Experience Manager] bureaubladtoepassing door de opdracht uit te voeren:

   ```shell
   set AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe
   ```

   Op Mac-systeem:

   1. Open een terminalvenster.

   1. De [!DNL Adobe Experience Manager] bureaubladtoepassing door de opdracht uit te voeren:

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

1. De [!DNL Experience Manager] bureaubladtoepassing via de volgende opdracht:

   `AEM_DESKTOP_LOG_LEVEL=DEBUG open /Applications/Adobe\ Experience\ Manager\ Desktop.app`.

De foutopsporingsmodus in Windows inschakelen:

1. Open een opdrachtvenster.

1. De [!DNL Experience Manager] bureaubladtoepassing via de volgende opdracht:

`AEM_DESKTOP_LOG_LEVEL=DEBUG&"C:\Program Files\Adobe\Adobe Experience Manager Desktop.exe`.

### Weet de [!DNL Adobe Experience Manager] bureaubladtoepassingsversie {#know-app-version-v2}

Het versienummer weergeven:

1. Start de toepassing.

1. Klik op de ellips in de rechterbovenhoek, houd de muisaanwijzer boven [!UICONTROL Help]en klik vervolgens op [!UICONTROL About].

   Het versienummer wordt weergegeven op dit scherm.

### Cache wissen {#clear-cache-v2}

Voer de volgende stappen uit:

1. Start de toepassing en maak verbinding met een instantie van [!DNL Experience Manager].

1. Open de voorkeuren van de toepassing door op de ovalen in de rechterbovenhoek te klikken en de optie [!UICONTROL Preferences].

1. Zoek het item met het dialoogvenster [!UICONTROL Current Cache Size]. Klik op het prullenbakpictogram naast dit element.

Ga als volgt te werk om de cache handmatig te wissen:

>[!CAUTION]
>
>Deze stappen kunnen een destructieve bewerking zijn. Als er lokale bestandswijzigingen zijn die niet worden geüpload naar [!DNL Adobe Experience Manager]Dan gaan die wijzigingen verloren.

De cache wordt gewist door de cachemap van de toepassing te verwijderen. Deze map staat in de voorkeuren van de toepassing.

1. Start de toepassing.

1. Open de toepassingsvoorkeuren door de ovalen in de rechterbovenhoek te selecteren en [!UICONTROL Preferences].

1. Noteer de [!UICONTROL Cache Directory] waarde.

   In deze map zijn er submappen die naar de gecodeerde map worden genoemd [!DNL Adobe Experience Manager] Eindpunten. De namen zijn een gecodeerde versie van de doelversie [!DNL Adobe Experience Manager] URL. Als de toepassing zich bijvoorbeeld richt op `localhost:4502`, dan is de mapnaam `localhost_4502`.

Als u de cache wilt wissen, verwijdert u de gewenste codering [!DNL Adobe Experience Manager] Eindpuntmap. Als u de volledige map verwijdert die u in de voorkeuren hebt opgegeven, wordt de cache ook gewist voor alle instanties die door de toepassing zijn gebruikt.

Wissen [!DNL Adobe Experience Manager] het cachegeheugen van de bureaubladtoepassing is een voorbereidende taak voor het oplossen van problemen die verschillende problemen kan oplossen. Wis de cache uit de toepassingsvoorkeuren. Zie [voorkeuren instellen](install-upgrade.md#set-preferences). De standaardlocatie van de cachemap is:

## Kan geplaatste elementen niet zien {#placed-assets-missing}

Controleer het volgende als u niet kunt zien welke elementen u of andere creatieve professionals in de ondersteuningsbestanden hebben geplaatst (bijvoorbeeld INDD-bestanden):

* Verbinding maken met de server. De Flash-netwerkconnectiviteit kan het downloaden van bedrijfsmiddelen blokkeren.

* Bestandsgrootte. Het downloaden en weergeven van grote elementen duurt langer.

* Stationsconsistentie. Als u of een andere medewerker de elementen heeft geplaatst tijdens het toewijzen van de [!DNL Experience Manager] DAM naar een andere stationsletter. De geplaatste elementen worden niet weergegeven.

* Rechten. Als u wilt controleren of u machtigingen hebt om de geplaatste elementen op te halen, neemt u contact op met uw [!DNL Experience Manager] beheerder.

### Bewerkingen aan bestanden in de gebruikersinterface van de bureaubladtoepassing weerspiegelen niet in [!DNL Adobe Experience Manager] onmiddellijk {#changes-on-da-not-visible-on-aem}

[!DNL Adobe Experience Manager] de bureaubladtoepassing laat het aan de gebruiker over om te beslissen wanneer alle bewerkingen van een bestand zijn voltooid. Afhankelijk van de grootte en complexiteit van een bestand duurt het veel tijd om de nieuwe versie van een bestand terug te zetten naar [!DNL Adobe Experience Manager]. De toepassing is ontworpen om het aantal bestandsoverdrachten te minimaliseren, in plaats van automatisch bestanden te uploaden op basis van geraden voltooiing van bewerkingen. De gebruiker wordt geadviseerd de overdracht van het bestand terug te zetten naar [!DNL Adobe Experience Manager] door ervoor te kiezen de wijzigingen van een bestand te uploaden.

### Problemen bij upgraden op macOS {#issues-when-upgrading-on-macos}

Soms kunnen er problemen optreden bij het upgraden van de [!DNL Experience Manager] bureaubladtoepassing op macOS. Verouderde systeemmappen voor de [!DNL Experience Manager] veroorzaakt deze problemen. De mappen voorkomen nieuwe versies van de [!DNL Experience Manager] bureaubladtoepassing om correct te laden. U kunt dit probleem verhelpen door de volgende mappen en bestanden handmatig te verwijderen.

Sleep de knop `Adobe Experience Manager Desktop` van de map macOS Applications naar de prullenmand. Dan open de terminal, stel het volgende bevel in werking, en verstrek uw wachtwoord wanneer ertoe aangezet.

```shell
sudo rm -rf ~/Library/Application\ Support/com.adobe.aem.desktop
sudo rm -rf ~/Library/Preferences/com.adobe.aem.desktop.plist
sudo rm -rf ~/Library/Logs/Adobe\ Experience\ Manager\ Desktop

sudo find /var/folders -type d -name "com.adobe.aem.desktop" | xargs rm -rf
sudo find /var/folders -type d -name "com.adobe.aem.desktop.finderintegration-plugin" | xargs rm -rf
```

## Kan bestanden niet uploaden {#upload-fails}

Als u de bureaubladtoepassing gebruikt met [!DNL Experience Manager] 6.5.1 of hoger, upgrade S3- of Azure-connector naar versie 1.10.4 of hoger. Het probleem met de fout bij het uploaden van bestanden dat te maken heeft met [OAK-8599](https://issues.apache.org/jira/browse/OAK-8599). Zie [installatie-instructies](install-upgrade.md#install-v2).

## [!DNL Experience Manager] verbindingsproblemen met bureaubladapps {#connection-issues}

Als u algemene connectiviteitsproblemen ondervindt, zijn er enkele manieren om meer informatie te krijgen over wat [!DNL Experience Manager] bureaubladtoepassing aan het doen is.

**Controleer het aanvraaglogboek**

De [!DNL Experience Manager] desktop app registreert alle verzoeken die het, samen met de antwoordcode van elk verzoek, in een specifiek logboekdossier verzendt.

1. Openen `request.log` in de het logboekfolder van de toepassing om deze verzoeken te zien.

1. Elke lijn in het logboek vertegenwoordigt of een verzoek of een reactie. Verzoeken hebben een `>` gevolgd door de gewenste URL. Reacties hebben een `<` gevolgd door de antwoordcode en de URL die is aangevraagd. De verzoeken en de Reactie kunnen worden aangepast gebruikend GUID van elke lijn.

**Verzoeken controleren die door de ingesloten browser van de toepassing zijn geladen**

Een meerderheid van de verzoeken van de toepassing wordt gevonden in het verzoeklogboek. Als er echter geen nuttige informatie beschikbaar is, kan het nuttig zijn om te kijken naar de aanvragen die door de ingesloten browser van de toepassing worden verzonden.
Zie de [SAML-sectie](#da-connection-issue-with-saml-aem) voor instructies over hoe te om die verzoeken te bekijken.

### SAML-aanmeldverificatie werkt niet {#da-connection-issue-with-saml-aem}

[!DNL Experience Manager] bureaubladtoepassing maakt mogelijk geen verbinding met uw SSO-toepassing (SAML) [!DNL Adobe Experience Manager] implementatie. Het ontwerp van de toepassing probeert de variaties en de complexiteit van SSO-verbindingen en -processen aan te passen. Voor een setup is mogelijk aanvullende probleemoplossing vereist.

Soms richt het proces SAML niet terug naar de oorspronkelijk gevraagde weg. Of, definitief is omleiden aan een gastheer die verschillend is dan wat in wordt gevormd [!DNL Adobe Experience Manager] bureaubladtoepassing. Ga als volgt te werk om te controleren of dit probleem niet het geval is:

1. Open een webbrowser. Toegang `https://[aem_server]:[port]/content/dam.json` URL.

1. Aanmelden bij de [!DNL Adobe Experience Manager] implementatie.

1. Wanneer login volledig is, bekijk het huidige adres van browser in de adresbar. Deze moet exact overeenkomen met de URL die oorspronkelijk is ingevoerd.

1. Verifieer ook dat alles vóór `/content/dam.json` komt overeen met het doel [!DNL Adobe Experience Manager] waarde geconfigureerd in [!DNL Adobe Experience Manager] de instellingen van de bureaubladtoepassing.

**Het inlogproces van SAML werkt correct volgens de bovenstaande stappen, maar de gebruikers kunnen zich nog niet aanmelden**

Het venster in het [!DNL Adobe Experience Manager] desktop app die het aanmeldingsproces weergeeft, is gewoon een webbrowser die het doel weergeeft [!DNL Adobe Experience Manager] webgebruikersinterface van instantie:

* De Mac-versie gebruikt een [WebView](https://developer.apple.com/documentation/webkit/webview).

* De Windows-versie gebruikt Chromium-gebaseerd [CefSharp](https://cefsharp.github.io/).

Zorg ervoor dat het SAML-proces deze browsers ondersteunt.

Als u meer problemen wilt oplossen, kunt u de exacte URL&#39;s bekijken die de browser probeert te laden. Deze informatie bekijken:

1. Volg de aanwijzingen voor het starten van de toepassing in [foutopsporingsmodus](#enable-debug-mode).

1. Reproduceer de login poging.

1. Ga naar de [logmap](#check-log-files-v2) van de aanvraag.

1. Voor Windows:

   1. Open &quot;aemcompanionlog.txt.&quot;

   1. Zoek naar berichten die met &quot;Login browser adres veranderd in&quot;beginnen. Deze vermeldingen bevatten ook de URL die de toepassing heeft geladen.

   Voor Mac:

   1. In `com.adobe.aem.desktop-nnnnnnnn-nnnnnn.log`, de nummers die zich in de nieuwste bestandsnaam bevinden, vervangen **n**.

   1. Zoek naar berichten die met &quot;geladen kader&quot;beginnen. Deze vermeldingen bevatten ook de URL die de toepassing heeft geladen.

Het bekijken van de opeenvolging URL die wordt geladen kan helpen bij het eind van SAML problemen oplossen om te bepalen wat verkeerd is.

### Probleem met SSL-configuratie {#ssl-config-v2}

De bibliotheken die [!DNL Experience Manager] bureaubladtoepassingen gebruiken voor HTTP-communicatie strikte SSL-handhaving. Soms kan een verbinding slagen gebruikend browser maar ontbreekt wanneer het gebruiken van [!DNL Experience Manager] bureaubladtoepassing. Installeer het ontbrekende tussentijdse certificaat in Apache om SSL op de juiste wijze te configureren. Zie [Hoe te om een MiddenCA cert in Apache te installeren](https://access.redhat.com/solutions/43575).

De bibliotheken die [!DNL Experience Manager] bureaubladtoepassingen gebruiken voor HTTP-communicatie strikte SSL-handhaving. Er kunnen dus instanties zijn waarbij SSL-verbindingen die via een browser slagen, mislukken met de [!DNL Adobe Experience Manager] bureaubladtoepassing. Dit resultaat is goed omdat het de juiste configuratie van SSL aanmoedigt en de beveiliging verhoogt, maar het kan frustrerend zijn wanneer de toepassing geen verbinding kan maken.

In dit geval kunt u het beste een hulpprogramma gebruiken om het SSL-certificaat van een server te analyseren en problemen te identificeren zodat deze kunnen worden gecorrigeerd. Er zijn Websites die het certificaat van een server inspecteren door zijn URL te verstrekken.

Als tijdelijke maatregel is het mogelijk om strikte SSL-handhaving uit te schakelen in de [!DNL Adobe Experience Manager] bureaubladtoepassing. Deze benadering is geen geadviseerde oplossing op lange termijn, aangezien het veiligheid vermindert door de worteloorzaak van verkeerd gevormde SSL te verbergen. Strikte handhaving uitschakelen:

1. Gebruik de editor van uw keuze om het JavaScript-configuratiebestand van de toepassing te bewerken. Dit bestand bevindt zich (standaard) op de volgende locaties (afhankelijk van het besturingssysteem):

   Op Mac: `/Applications/Adobe Experience Manager Desktop.app/Contents/Resources/javascript/lib-smb/config.json`

   In Windows: `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop\javascript\config.json`

1. Zoek de volgende sectie in het bestand:

   ```shell
   ...
   "assetRepository": {
       "options": {
   ...
   ```

1. De sectie wijzigen door deze toe te voegen `"strictSSL": false` als volgt:

   ```shell
   ...
   "assetRepository": {
       "options": {
           "strictSSL": false,
   ...
   ```

1. Sla het bestand op en start de [!DNL Adobe Experience Manager] bureaubladtoepassing.

### Aanmeldingsproblemen bij overschakelen naar een andere server {#cannot-login-cookies-issue}

Nadat u een [!DNL Experience Manager] Wanneer u probeert de verbinding naar een andere server te wijzigen, kunnen er aanmeldingsproblemen optreden. Dit is te wijten aan oude cookies die de nieuwe verificatie belemmeren. Een optie in het hoofdmenu om [!UICONTROL Clear Cookies] helpt. Afmelden van de huidige sessie in de app en selecteren [!UICONTROL Clear Cookies] voordat u verdergaat met verbinden.

![Cookies wissen bij schakelen tussen servers](assets/main_menu_logout_da2.png)

## App reageert niet {#unresponsive}

In zeldzame gevallen reageert de toepassing niet meer, wordt alleen een wit scherm weergegeven of wordt een fout onder aan de interface weergegeven zonder opties in de interface. Probeer het volgende in de volgorde:

* Klik met de rechtermuisknop op de toepassingsinterface en klik op **[!UICONTROL Refresh]**.
* Sluit de toepassing af en open deze opnieuw.

In beide methoden wordt de toepassing gestart in de hoofdmap DAM.

## Verlopen elementen verbergen {#hide-expired-assets}

Wanneer u elementen bladert vanuit de [!DNL Experience Manager] gebruikersinterface, worden de verlopen elementen niet weergegeven. Beheerders kunnen instellingen configureren om te voorkomen dat verlopen middelen worden weergegeven, gezocht en opgehaald wanneer ze de bureaubladtoepassing en de Asset Link verlaten. Dit zorgt ervoor dat verlopen elementen tijdens deze bewerkingen niet toegankelijk zijn. De configuratie werkt voor alle gebruikers, ongeacht beheerderrechten.

* [Configuratie in Experience Manager 6.5 om verlopen elementen te verbergen](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/managing/manage-assets#hide-expired-assets-via-acp-api).
* [Configuratie in Experience Manager as a Cloud Service om verlopen elementen te verbergen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets#hide-expired-assets-via-acp-api).

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
>* [Bekende problemen](release-notes.md#known-issues-v2)
>* [Bewerkingsconflicten voorkomen](using.md#adv-workflow-collaborate-avoid-conflicts)
