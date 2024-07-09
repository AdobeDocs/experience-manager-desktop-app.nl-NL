---
title: Opmerkingen bij de release van desktop app v1.10
description: Geef details, verbeteringen, nieuwe functies, compatibiliteit en downloadkoppelingen op voor AEM bureaubladtoepassing versie 1.10.
exl-id: 886864e0-016a-4a17-b3ba-4b18a514214a
source-git-commit: 23719d2f5d92f6031687df18036acdbc04722402
workflow-type: tm+mt
source-wordcount: '3989'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager] Opmerkingen bij de release desktop app v1.10 {#aem-desktop-app-release-notes}

Voor desktop app v1.x release zijn de volgende downloadkoppelingen en AEM compatibiliteitsgegevens beschikbaar.

| Producten | [!DNL Adobe Experience Manager] bureaubladtoepassing |
|--- |--- |
| Versie | 1.10 (1.10.0.6 voor Mac en 1.10.0.3 voor Windows) |
| Type | Minder release |
| Datum | 1.10.0.6 (Mac): 15 april 2020; 1.10.0.3 (Win): 31 augustus 2018 |
| URL&#39;s downloaden | [macOS X 64-bits](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-1.10.0.6.dmg); [Windows 32-bits](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-1.10.0.3.exe); [Windows 64-bits](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-1.10.0.3.exe) |
| Compatibiliteit | AEM 6.5.x; AEM 6.4.x; AEM 6.3 SP2; AEM 6.2 SP1 GVB2+; AEM 6.1 SP2 GVB7+ |

>[!NOTE]
>
>Limiet voor cachegrootte wordt niet afgedwongen. Wanneer de bureaubladtoepassing wordt gestart, wordt de cachegrootte eenmaal berekend en wordt een melding weergegeven als de grootte dicht bij de vooraf gedefinieerde limiet ligt.

## Systeemvereisten en -vereisten {#system-requirements-and-prerequisites}

[!DNL Adobe Experience Manager] bureaubladtoepassing is compatibel met de volgende besturingssystemen:

* macOS X 10.10 of hoger, met de meest recente opgeloste problemen.

* Windows 10 met de recentste de dienstpakken en insectenmoeilijke situaties.

Adobe raadt u aan de nieuwste versie van de AEM-bureaubladtoepassing te gebruiken om ervoor te zorgen dat u de meest recente functionaliteit, de meest recente opgeloste problemen en de best mogelijke prestaties gebruikt.

Voor de versie van AEM bureaubladtoepassing die u op uw lokale computer wilt installeren, is een specifieke AEM serverversie/aanvullende serveronderdelen (servicepakketten, hotfixes of functiepakketten) vereist. Zorg ervoor dat de AEM server correct is geconfigureerd voordat u er voor het eerst verbinding mee maakt. Neem contact op met de AEM als u hulp nodig hebt.

Zie de [gedetailleerde compatibiliteitsmatrix](#compatibilitymatrix) aan het eind van dit document om de eerste vereisten voor uw opstelling te evalueren.

## Nieuw in desktop app v1.10 {#what-s-new-in-aem-desktop-app}

AEM desktop app 1.10 richt zich op het verbeteren van de gebruikerservaring bij grote uploads, informatie over de achtergrondbewerkingen en geoptimaliseerde ervaring bij het openen van elementen met gekoppelde bestanden (zoals InDesign).

>[!NOTE]
>
>Gebruik minimaal versie 1.10.0.6 van de app als u macOS 10.15.4 of hoger gebruikt. Deze pleisterafgifte voldoet aan de [Apple-notariatievereisten](https://developer.apple.com/news/?id=04102019a).

**Lokaal bewerken/Uitchecken**: Automatisch uploaden van wijzigingen die zijn opgeslagen naar elementen kan worden uitgeschakeld in het statusvenster. Op die manier kan de gebruiker aan bestanden blijven werken en wijzigingen opslaan en vervolgens, wanneer deze gereed zijn, besluiten alle wijzigingen te uploaden.

**Venster Vereenvoudigd middelenstatus**. Het statusvenster is vereenvoudigd. De [!UICONTROL Uploads] op het tabblad worden nu zowel de afzonderlijke elementen als de mappen of bulkuploads weergegeven. Het vorige tabblad voor bulkuploads is verwijderd.

**Toepassingspictogram om bulkuploads aan te geven**. Het toepassingspictogram geeft aan dat een bulkupload wordt uitgevoerd door een &quot;transfer&quot;-overlay weer te geven.

**Meldingen voor updateconflicten**. Wanneer de toepassing een conflict tijdens een middelenupdate ontdekt, toont het een bericht, die de gebruiker toestaat om het te herzien zonder het statusvenster te controleren. Bij het opstarten controleert de toepassing op alle conflicten, waardoor de gebruiker deze kan oplossen.

**Betere afhandeling van verbindingsverliezen**. Bulkuploads worden gepauzeerd als er een verbindingsverlies is, en de gebruiker kan later hervatten. A [!UICONTROL Retry] is beschikbaar als u een mislukte upload van een afzonderlijk bestand opnieuw wilt proberen.

## Installatie-instructies {#installation-instructions}

Zie voor gedetailleerde instructies [De AEM bureaubladtoepassing installeren en configureren](install-configure-app-v1.md).

## Verbeteringen in de vorige versies {#enhancements-in-the-previous-versions}

Deze release breidt de vorige versies van de [!DNL Experience Manager] desktop app, die de volgende belangrijke verbeteringen biedt:

* **Versie 1.9 / 1.9.1**: herbruikbare uploads, verbeterd statusvenster, toepassingspictogrammen die de status van de toepassing/verbinding aangeven, vooraf opgehaalde gekoppelde elementen voor InDesigns bestanden.

* **Versie 1.8**: betere controle van cachegrootte voor de gebruiker, verbeterde aanmeldervaring voor SAML/SSO in Windows, ondersteuning voor `.pac` netwerk volmacht op Mac, en klant-gemelde kwesties.

* **Versie 1.7**: verbeteringen in stabiliteit en caching logica, betere steun voor netwerkvolmacht, en capaciteit om interne dossiers na uninstallation schoon te maken.

* **Versie 1.6**: verbeteringen in het aanmeldingsproces voor verschillende AEM beveiligingsconfiguraties en de stabiliteit en prestaties van de toepassing.

* **Versie 1.5**: de stabiliteit van de toepassing en veerkracht tegen diverse voorzien van een netwerkproblemen, betere steunbaarheid.

* **Versie 1.4**: de mogelijkheid om hiërarchische mappen op de achtergrond te uploaden met voortgangscontrole.

* **Versie 1.3**: betere prestaties en stabiliteit bij het benaderen van bestanden en het opslaan van wijzigingen in AEM, met name van desktoptoepassingen in Creatives Cloud, zoals InDesign, Illustrator of Photoshop. Het was bedoeld om gebruikers een meer lokale desktop-achtige ervaring te bieden wanneer het werken met dossiers, terwijl tegelijkertijd de verrichtingen van de netwerkgegevensoverdracht op de achtergrond behandelen.

### Verbeteringen beschikbaar sinds AEM desktop app 1.9 {#Enhancements-Available-Since-AEM-Desktop-App-19x}

[!DNL Adobe Experience Manager] desktop app versie 1.9.1 was een patchrelease. Deze service is ontworpen om belangrijke problemen met klanten aan te pakken met het afrekenen van bedrijfsmiddelen. En, adres het kopiëren van dossiers van een netwerkaandeel aan een lokale folder.

* Assets uitgecheckt door één gebruiker zou niet beschikbaar moeten zijn voor wijziging voor andere gebruikers (CQ-4246009)

* Een kopie van een toegewezen map naar een lokale map ondersteunen wanneer de gebruikersmap zich op een aparte schijfpartitie bevindt (CQ-4243978)

AEM bureaubladtoepassing 1.9 was gericht op het verbeteren van de gebruikerservaring bij grote uploads, informatie over de achtergrondbewerkingen en geoptimaliseerde ervaring bij het openen van elementen met gekoppelde bestanden (zoals InDesign).

**Opnieuw afwerkbare uploads**
Voor uploads, vooral rond grote dossiers, is er een optie om hen in het nieuwe venster van de Status van Activa te pauzeren/te hervatten.

**Verbeterd venster voor middelenstatus**
Een verbeterd venster Asset Status bevat de volgende informatie over elementen.

[!UICONTROL Changes]

* Hier worden wijzigingen in de wachtrij weergegeven.

* Hiermee geeft u uploads tijdens de uitvoering weer met een voortgangsbalk, overdrachtssnelheid, totale bestandsgrootte en de hoeveelheid die tot nu toe is overgedragen.

* Voltooide uploads weergegeven met totale overdracht en eindsnelheid.

* De weergave van geüploade bestanden is mislukt, samen met een foutbericht en overdrachtgegevens, indien beschikbaar.

* Bij uploads die drie keer zijn mislukt, wordt een foutbericht weergegeven.

* Conflicterende bestanden worden weergegeven met een pictogram waarop de gebruiker kan klikken. Klik op het pictogram om een dialoogvenster met een uitleg en twee opties weer te geven:

   * [!UICONTROL Keep Mine] uploadt het bestand onmiddellijk naar de server.

   * [!UICONTROL Overwrite Mine] verwijdert het lokale bestand onmiddellijk en downloadt een nieuwe kopie van de server.

[!UICONTROL Downloads]

* Hiermee worden downloads die momenteel worden uitgevoerd, weergegeven, inclusief een overdrachtsnelheid en de grootte die tot nu toe zijn overgedragen.

* Voltooide downloads worden weergegeven met de totale overdracht, de uiteindelijke snelheid en een pictogram waarmee het bestand wordt geopend wanneer erop wordt geklikt (alleen beschikbaar voor afzonderlijke bestanden).

* Mislukte downloads weergegeven met een foutbericht en overdrachtsinformatie, indien beschikbaar.

* In de voettekst ziet u het totale aantal gedownloade bestanden en de gemiddelde overdrachtsnelheid.

* Als een gebruiker ervoor kiest om meerdere bestanden te openen of te bewerken vanuit de [!DNL Experience Manager Assets] De interface van het Web, worden zij gegroepeerd. Bijvoorbeeld mijnelement.jpeg en 4 andere bestanden.

* Wanneer u vanuit AEM Assets documenten van InDesigns met gekoppelde elementen downloadt, downloadt de bureaubladtoepassing eerst alle gekoppelde elementen voordat het document wordt geopend en wordt de downloadstatus aangegeven. Bijvoorbeeld 5 van 24.

[!UICONTROL Bulk Uploads]

Grote maphiërarchieën uploaden via [!UICONTROL Create] > [!UICONTROL Upload Folder] in AEM Web UI brengt dit dialoogvakje teweeg. Hetzelfde geldt wanneer u &quot;Assets plakken&quot; kopieert en selecteert in Finder of Explorer in het contextmenu van de bureaubladtoepassing.

* Hier worden uploads tijdens de uitvoering weergegeven, inclusief een voortgangsbalk en de naam van het bestand dat momenteel wordt overgedragen.

* Tijdens het uploaden wordt een pictogram weergegeven waarmee het uploaden wordt geannuleerd wanneer erop wordt geklikt. De overdracht wordt gestopt nadat het huidige overdragende dossier voltooit.

* Mislukte overdrachtsprocessen worden weergegeven met een foutbericht (alleen als de volledige overdracht mislukt).

* Als een afzonderlijk bestand niet kan worden overgedragen, wordt dit als een fout op het tabblad weergegeven. Anders worden afzonderlijke bestanden niet op het tabblad * weergegeven als één item voor de volledige upload.

**Pictogrammen om de status van achtergrondbewerkingen aan te geven**

Het toepassingspictogram geeft de toestand van de achtergrondbewerkingen aan, zodat de gebruikers een beter visueel signaal krijgen. Wanneer de toepassing bijvoorbeeld niet met AEM is verbonden, wordt het pictogram grijs weergegeven. Als er een actieve upload is, wordt er een &quot;sync&quot;-overlay weergegeven, enzovoort.

**Ophalen vooraf van Linked Assets**

Om de gebruikerservaring te verbeteren met documenten van het InDesign die verbonden activa bevatten die in AEM worden opgeslagen, de Desktop app pre-haalt deze verbonden dossiers aan het lokale geheime voorgeheugen. Deze stroom vindt plaats voordat het document van het InDesign wordt gedownload en geopend. Op die manier heeft de gebruiker de gekoppelde bestanden lokaal beschikbaar en hoeft hij niet langer te wachten wanneer hij of zij elementen in het InDesign opent (in het deelvenster Koppelingen).
Het vooraf ophalen werkt alleen als AEM de koppelingen aan de serverzijde herkent. Voor een element met herkende koppelingen wordt een lijst met &#39;Referenties&#39; weergegeven in de weergave Eigenschappen van het element InDesign.

### Verbeteringen beschikbaar sinds AEM desktop app 1.8.x {#enhancements-available-since-aem-desktop-app-18x}

AEM desktop app 1.8.1 fast-follow release heeft verbeteringen aangebracht bij het openen van meerdere bestanden tegelijk van AEM gebruikersinterface naar de release 1.8 (CQ-4237747, CQ-4238780). Verbeteringen in AEM desktop app 1.8 zijn:

* Caching: new UI for manage AEM desktop app cache (CQ-4208690), including,

   * huidige cachegrootte weergeven

   * de maximale cachegrootte bepalen voordat een melding wordt verzonden

   * De cachegrootte wordt alleen gecontroleerd bij het starten van de bureaubladtoepassing en er wordt een melding weergegeven als de geconfigureerde limiet is bereikt

   * wissen van de cacheknop is nu beschikbaar in de nieuwe interface

* Aanmelden: (Win) Vaste aanmelding bij AEM instantie geconfigureerd voor gebruik van SAML en SSL (CQ-4216353)

* Netwerk:

   * wanneer een AEM sessie verloopt, wordt de gebruiker nu op de hoogte gesteld en kan hij op het bericht klikken om zich opnieuw aan te melden (CQ-4202028).

   * (Mac) Voeg ondersteuning toe voor het maken van verbinding met AEM via de `.pac` proxyconfiguratie (CQ-4233430).

   * (Win) los problemen op met het dialoogvenster Geavanceerd - URL voor aanmelding (CQ-4236061).

* Bugfixes:

   * Meer informatie over elementen: soms was de actiebalk niet zichtbaar (CQ-4208540).

   * (Win) Het bestand kan nu worden gesynchroniseerd nadat u een eerdere versie hebt hersteld vanuit de gebruikersinterface van AEM Assets (CQ-4216411).

### Verbeteringen beschikbaar sinds AEM desktop app 1.7 {#Enhancements-Available-Since-AEM-Desktop-App-17}

* Stabiliteit:

   * Verbeterde stabiliteit wanneer de AEM desktop-app verbinding maakt met een overbelaste AEM-server (CQ-4224803).

   * Verbeterde stabiliteit wanneer om veel bestanden wordt verzocht (CQ-4224212).

   * Verbeterde assetupdate met extra controle (CQ-4228291).

* Caching:

   * Schijffouten verhelpen en problemen met openen bij het openen van bestanden in Photoshop, InDesign, Finder (CQ-4223993, CQ-4217603, CQ-4223717).

   * Verbeterde plaatsing in cache om binaire bestanden met een grootte van nul te voorkomen (CQ-4216599).

* Aanmelden: verbinding maken met strictSSL uitgeschakeld voor speciale configuraties (zoals lokaal uitgegeven certificaten) (CQ-4223949).

* Netwerken: verbeterde ondersteuning voor verbinding via netwerkproxy (CQ-4223477, CQ-4221280, CQ-4206854).

* Installatie en verwijdering:

   * (Win) Cleaner uninstallation (CQ-4220906).

   * [Windows 32-bits] Het installatieprogramma probeert Microsoft .NET Framework v. 4.5 (CQ-4218084) niet te installeren.

   * (Mac) Handmatig script voor het volledig verwijderen van bureaubladtoepassingsbestanden (CQ-4216489).

>[!NOTE]
>
>Problemen die zich voordoen in AEM desktop app 1.7 bètabelasting die niet aanwezig was in de release 1.6, worden weggelaten in de opmerkingen bij de release.

### Verbeteringen beschikbaar sinds AEM desktop app 1.6 {#Enhancements-Available-Since-AEM-Desktop-App-16}

* Documentatie: nieuw [Aanbevolen werkwijzen voor v1.x-app](/help/using/best-practices-for-v1.md) documentatie.

* Verbeterd aanmeldingsproces voor AEM:

   * Verbeter de behandeling van SAML * ontkoppel regels (CQ-4202781).

   * Voeg mogelijkheden toe om een afzonderlijke login URL in Voorkeur (CQ-4214052, CQ-4214051) te vormen.

* Bruikbaarheid: gebruikers waarschuwen wanneer een middel nog steeds wordt gedownload voor grotere activa (CQ-4216284).

* Netwerken:

   * DNS-caching (CQ-4210176).

   * Verbinding via proxy ondersteunen in Windows (CQ-4206854).

* In cache plaatsen en toegang tot netwerkshare in Finder/Explorer:

   * Het vergrendelingspictogram is nu zichtbaar voor uitgecheckte middelen in Windows 10 (CQ-90957).

   * Mapinhoud kan verdwijnen/opnieuw verschijnen in netwerkshare (CQ-4209160, CQ-4210180).

   * Fout bij het uploaden van een bestand als gevolg van een conflict dat is gemeld in de status van de wachtrij uploaden (CQ-4215727).

   * Bij het openen van meerdere bestanden vanuit de bureaubladtoepassingsmap in PS, worden mogelijk afgebroken of onvolledige berichten weergegeven (CQ-4216276).

* Oplossingen voor stabiliteit en prestaties:

   * Verbeterde prestaties tijdens het bladeren door mappen met veel bestanden (CQ-4214933).

   * De desktop-app 1.5 kan een bureaubladcomputer in de loop der tijd vertragen (CQ-4209159).

   * De statusfunctie voor wachtrij tonen werkt alleen voor de gebruiker die de app heeft geïnstalleerd (CQ-4212199).

   * (Windows) Zorg ervoor dat het 32-bits installatieprogramma geen 64-bits code bevat (CQ-4217406).

* Bepaalde problemen gevonden en opgelost in 1.6 bèta:

   * Hoog CPU-gebruik (CQ-4218070).

   * Sleep bestanden die een fout veroorzaken bij het uploaden naar AEM (CQ-4217/06).

### Verbeteringen beschikbaar sinds AEM desktop app 1.5 {#Enhancements-Available-Since-AEM-Desktop-App-15}

**Versie 1.5.1.5 voor macOS X:** De release 1.5.1.5 biedt de volgende voordelen:

* Nieuwe functies en uitbreiding: voeg de functie Kopiëren/Plakken toe aan de integratie met Finder om rechtstreekse overdracht van desktop naar AEM mogelijk te maken (CQ-4208158).

* Bugfixes:

   * Correctie van fout 43 die soms optrad tijdens het wijzigen van de naam van elementen (CQ-4207900).

   * Als u terugkeert naar een oudere versie van de tijdlijn in AEM, wordt het element niet bijgewerkt in Finder (CQ-4205194).

   * bureaubladtoepassing crasht bij bladeren door grote, geneste mappen (CQ-4208539).

   * Het koppelingspunt voor bureaubladtoepassing is nu /Volumes/DAM en is dus consistent voor alle gebruikers (CQ-4208159).

   * Wanneer u een bestand voor het eerst in InDesign plaatst, wordt een updatewaarschuwing weergegeven (CQ-4207454).

Nota over de Waarschuwingen van de Verbinding: de toepassingen van het Creative Cloud (zoals InDesign) nemen een &quot;momentopname&quot;van de laatste-gewijzigde tijd van het punt op het tijdstip het wordt geplaatst. Als die datum later verandert, meldt de Adobe Creative Cloud-app dat de koppelingen verouderd zijn. Deze informatie wordt op een paar manieren gerapporteerd:

* Wanneer de Adobe Creative Cloud-app wordt gestart, wordt een dialoogvenster weergegeven waarin de gebruiker wordt geïnformeerd dat de gekoppelde elementen verouderd zijn en waarin de gebruiker wordt gevraagd actie te ondernemen.

* Als de Adobe Creative Cloud-app al wordt uitgevoerd, wordt een geel driehoekwaarschuwingspictogram weergegeven op het gekoppelde element.

Dit gedrag is hetzelfde voor elementen op de lokale schijf en elementen in een map die zich op een AEM bureaublad bevindt, met de volgende uitzonderingen:

* Als een andere gebruiker een geplaatst element bewerkt, verschijnt het waarschuwingspictogram de eerste keer dat andere gebruikers een document openen dat het geplaatste element bevat. Deze waarschuwing treedt alleen op als het geplaatste element al in de lokale cache is geplaatst.

* Als een gebruiker een geplaatst element wijzigt via de gekoppelde map van het AEM bureaublad en vervolgens de lokale cache wist, wordt het geplaatste element gerapporteerd als verouderd.

Beide gevallen worden verwacht en zijn neveneffecten van de &quot;vertraagde synchronisatie&quot;-architectuur van AEM desktop.

**Versie 1.5.0.x voor macOS X en Windows:** Deze release van AEM bureaubladtoepassing biedt de volgende voordelen:

* Betere stabiliteit en veerkracht tegen voorzien van een netwerkkwesties.

   * stabielere toewijzing van AEM Assets-mappen (CQ-103276, CQ-4204669, CQ-4203957).

   * Betere verwerking van bestanden in cache (CQ-4204336, CQ-4206263).

   * Verbeterde verwerking van het downloaden/uploaden van grote bestanden van meer dan 2 GB (CQ-4206438).

   * Correctie van &quot;Fout 36&quot; bij het verplaatsen of hernoemen van een groter aantal bestanden in Finder (CQ-4204640).

* Optimalisaties in netwerkcommunicatie met AEM server (CQ-4204974, CQ-100903).

* Betere betrouwbaarheid bij het openen, plaatsen en opslaan van middelen van AEM in Creative Cloud-apps (CQ-4203968, CQ-4205511, CQ-103543, CQ-4207141, CQ-90980).

* Verbeterde ondersteuning: optie om cache te wissen (CQ-4202541), eenvoudige toegang tot logbestanden (CQ-4202340, CQ-4204673).

* Andere correcties:
   * Betere ondersteuning voor elementen en mappen met Japanse tekens in naam/niet-Engelse taalinstellingen (CQ-4195433, CQ-4205793, CQ-4199446).

   * Betere aanmelding met SSL (CQ-4200217).

   * Betere aandelenmontage (CQ-42007-93).

   * Verschillende verbeteringen in de stabiliteit (CQ-4207539, CQ-4200378).

   * Betere verwerking van AEM Assets URL in Voorkeuren (CQ-97388).

### Verbeteringen beschikbaar sinds AEM desktop app 1.4 {#Enhancements-Available-Since-AEM-Desktop-App-14}

* Het eenvoudig uploaden van hiërarchische mappen via de nieuwe handeling Map maken > Uploaden in Touch UI.
   * Met deze handeling wordt een bewerking gestart voor het uploaden van mappen die door de bureaubladtoepassing wordt uitgevoerd.
   * Desktop app doorloopt de opgegeven maphiërarchie op de achtergrond op het bureaublad en uploadt de bestanden naar AEM Assets.
   * De gebruiker kan de vooruitgang in het nieuwe Upload venster van de Status van de Rij voor aan de gang zijnde verrichtingen controleren.
   * De status van de Wachtrij uploaden verstrekt ook betere het oplossen van problemeninformatie (bijvoorbeeld, geen verbinding aan de server).
* Nieuwe handeling Bewerken in Touch-gebruikersinterface waarin bewerkingen voor uitchecken en openen in één handeling worden gecombineerd.
* Geoptimaliseerde groepering van acties die betrekking hebben op het bureaublad in Touch-gebruikersinterface (AEM 6.3).
* Verbeterde compatibiliteit met de nieuwste versies van het besturingssysteem.
* Door de klant gemelde correcties.

### Verbeteringen beschikbaar sinds AEM desktop app 1.3 {#Enhancements-Available-Since-AEM-Desktop-App-13}

* Meer efficiëntie. De gebruikers besteden minder tijd wachtend op netwerkverrichtingen om te voltooien.
* Verbeterde integratie met de Finder, die meer stabiliteit en toegang tot functies, zoals miniaturen, biedt.
* Verbeteringen in cache en prestaties.
* Betere ondersteuning voor het rechtstreeks opslaan van desktopapps (PS, ID, AI, enzovoort).
* Verbeterde integratie met macOS (het lokale protocol van de netwerkaandrijving veranderde van WebDAV in stabielere SMB1).
* De bureaubladtoepassing maakt verbinding met de AEM server via AEM native HTTP RESTful-protocol.
* Bestanden worden eerst lokaal opgeslagen en vervolgens na een vooraf gedefinieerde tijd (30 seconden) weer naar AEM geüpload. Deze workflow verkort de tijd om bestanden op te slaan.
* Betere verwerking van bureaubladtoepassingen die gebruik maken van tussenliggende bestandsbewerkingen om een bestand op te slaan (gedeeltelijke opslag en tijdelijke bestanden), waardoor de tijdlijn van AEM Asset de juiste versie en informatie over het uploaden van middelen kan weergeven.
* Er wordt een dialoogvenster weergegeven waarin de status van uploadtaken op de achtergrond wordt bijgehouden.

## Lijst met wijzigingen {#list-of-changes}

### Onderstelpunt op Mac {#mount-point-on-mac}

Sinds macOS 10.12 (Sierra), heeft Apple de toestemmingen op de /Volumes omslag veranderd die worden gebruikt om netwerkaandrijving en apparaten op te zetten om restrictiever te zijn. Voor het maken van een nieuw koppelingspunt op die locatie zijn beheerrechten vereist. Dit probleem is opgelost in macOS 10.12.5.

Het koppelingspunt van de AEM-bureaubladtoepassing is gewijzigd in versies 1.4 en 1.5. In macOS is de map gewijzigd in een DAM-submap in de lokale map van de gebruiker, die ondersteuning biedt voor gebruikers die geen beheerder zijn (CQ-104183).

Omdat de `/Volumes` voor de map zijn geen beheerrechten meer vereist. Deze wijziging is in 1.5.1 ongedaan gemaakt. Deze wijziging maakt het ook mogelijk om documenten van het InDesign te delen die activa van AEM tussen gebruikers van macOS hebben geplaatst.

### Protocol wijzigen (sinds v1.3) {#protocol-change-since}

* macOS X:
   * Het lokale protocol van de netwerkaandrijving voor OS X Desktopintegratie veranderde in SMB1 van WebDAV.
   * De AEM opslagplaats gekoppeld met de desktop-app is zichtbaar als een `smb` netwerkstation in de Finder, in plaats van een WebDAV-station.
* Windows:
   * Het lokale protocol van de netwerkaandrijving voor de Desktopintegratie van Vensters blijft; AEM wordt opgezet als aandeel WebDAV.
* Voor beide platforms (Windows en Mac):
   * Het protocol om tot activa toegang te hebben/te downloaden en veranderingen in AEM te uploaden is veranderd in het inheemse AEM protocol, dat op HTTP-Gebaseerd op RESTful protocol is. Het verstrekt grotere controle over netwerkverrichtingen en is meer compatibel met de netwerkinfrastructuur.

>[!NOTE]
>
>In macOS X leidt de wijziging van het protocol van de lokale netwerkschijf van WebDAV in SMB1 tot een ander lokaal pad naar hetzelfde middel in de opslagplaats. Deze wijziging kan gevolgen hebben voor koppelingen naar bestanden die via de opdracht Plaatsen in Adobe Creative Cloud-toepassingen zijn geplaatst. Zie de [AEM bureaubladtoepassing gebruiken](use-app-v1.md) voor meer informatie .

### Bestandsbeheer (sinds 1.3) {#file-handling-since}

* Mappen worden automatisch bijgewerkt na een vooraf gedefinieerde vertraging (momenteel dertig jaar).
* Bestanden die door andere gebruikers zijn uitgecheckt, zijn gemarkeerd als alleen-lezen.
* Bestanden worden in twee fasen opgeslagen op een locatie op het netwerkstation die via de bureaubladtoepassing wordt gemonteerd.
* In de eerste fase wordt een bestand lokaal opgeslagen. Op deze manier hoeft de gebruiker die het bestand opslaat, niet te wachten totdat het bestand volledig is overgebracht naar AEM. De gebruiker kan het bestand opnieuw gebruiken zodra het is opgeslagen.
* In de tweede fase uploadt de bureaubladtoepassing een bijgewerkt bestand naar de AEM server na een vooraf gedefinieerde vertraging (bijvoorbeeld 30 seconden). Deze bewerking vindt plaats op de achtergrond. Gebruik de **Synchronisatiestatus achtergrondbestand tonen** om de status van de uploadbewerking weer te geven.

## Belangrijke kennisgevingen {#important-notices}

**Map uploaden.** Adobe raadt u aan de nieuwe mogelijkheid voor het uploaden van mappen te gebruiken om grotere hiërarchische mappen naar AEM te uploaden. Deze benadering wordt geadviseerd in tegenstelling tot het gebruiken van een exemplaar/belemmering-en-daling in een opgezette AEM bewaarplaats van het niveau van de Vinder/van de Ontdekkingsreiziger. Wanneer u de functie voor het uploaden van mappen gebruikt, communiceert de bureaubladtoepassing rechtstreeks met AEM en heeft deze dus veel betere controle over het gehele proces.

**AEM sessie beschikbaar houden.** De AEM bureaubladtoepassing is afhankelijk van een sessie die voor de AEM Assets-server is geopend om de juiste werking te garanderen. Dagelijkse gebruikers dienen de installatie van AEM Assets op het einde van de dag ongedaan te maken en &#39;s ochtends te koppelen om de functionaliteit voor aanmelding en delen van netwerken te garanderen.

**Schakel Pictogramvoorvertoning uit in de Finder.** Als u met Finder wilt bladeren door grote mappen, met name door slechte netwerkconnectiviteit, moet u ervoor zorgen dat zowel &quot;Pictogram&quot; als &quot;Voorvertoning pictogram&quot; zijn uitgeschakeld. Anders downloadt Finder elk element in een map om een kleine voorvertoning te genereren, wat kan leiden tot slechte prestaties en een hoog bandbreedtegebruik (CQ-4219779)

* Ga in Finder naar de gedeelde netwerkmap van AEM Assets
* Klik met de rechtermuisknop op het DAM-koppelingspunt
* Weergaveopties tonen selecteren
* Selectie van Voorvertoning pictogram tonen opheffen
* Klik op &quot;Als standaardwaarden gebruiken&quot;

**Reinig de cache wanneer u verbinding maakt met een nieuwe AEM.** Als de bureaubladtoepassing verbinding maakt met een andere AEM server met dezelfde URL, wordt de cache niet automatisch gewist. Wis de cache handmatig om de juiste bewerkingen te garanderen. Dit proces gebeurt doorgaans tijdens het testen, wanneer AEM installaties kunnen worden vervangen terwijl ze op dezelfde URL worden uitgevoerd (CQ-4216982)

**Gebruik CA-ondertekende SSL-certificaten.** De AEM desktop-app ondersteunt geen zelfondertekende SSL-certificaten wanneer verbinding wordt gemaakt met AEM via een beveiligde HTTPS-verbinding. Voor dergelijke verbindingen is op de server een certificaat met CA-handtekening vereist. (CQ-87941)

## Bekende problemen {#known-issues}

* Algemeen:
   * Server-URL&#39;s moeten zonder pad naar de server verwijzen (bijvoorbeeld `http://server`, `https://server`, `http://server:port`, of `https://server:port`). Contextpaden en andere submappen dan /content/dam worden niet ondersteund (CQ-89343, CQ-87272)
* Bestandsnamen/lokalisatie:
   * Bestands- en mapnamen met gereserveerde tekens worden niet correct verwerkt. Zorg ervoor dat u bestands- en mapnamen gebruikt die voldoen aan AEM vereisten. (CQ-93361, CQ-93308, CQ-89276, CQ-4217183)
   * Sommige toepassingen, zoals Adobe Illustrator, maken mogelijk bestanden met namen die niet worden ondersteund in AEM. Bijvoorbeeld: toevoegen `Converted` nadat u een bestand hebt geconverteerd, zodat het niet meer kan worden geüpload. (CQ-4216985)
   * Assets met internationale namen kan verschijnen en elke paar seconden verdwijnen.
* Inchecken en uitchecken:
   * Een element dat door een gebruiker is uitgecheckt, kan niet door een andere gebruiker worden geopend, door de handeling Openen vanuit de aanraakinterface of rechtstreeks op het bureaublad. Sommige toepassingen melden het als gesloten, maar ook bedorven of zelfs hangen terwijl het proberen te openen. (CQ-4199234)
   * Het gelijktijdig wijzigen van bestanden door meerdere gebruikers kan tot gevolg hebben dat sommige wijzigingen verloren gaan. De oplossing hiervoor is het in- en uitchecken van bestanden te gebruiken om te voorkomen dat meerdere gebruikers hetzelfde bestand wijzigen. (CQ-97035)
   * Bepaalde toepassingen ondersteunen de alleen-lezen markering niet correct, waardoor een gebruiker een bestand kan opslaan dat een andere gebruiker heeft uitgecheckt. Het gewijzigde bestand wordt pas overgedragen wanneer de andere gebruiker het bestand incheckt. Beide wijzigingen zijn beschikbaar in AEM als verschillende versies van het element. (CQ-89551, CQ-87572, CQ-89615)
   * De statussen Uitgecheckt en Alleen-lezen worden afzonderlijk gerapporteerd in de Finder. Deze methode resulteert in twee vergrendelingspictogrammen wanneer een gebruiker een element uitcheckt. (CQ-895/07)
* Integratie van Finder:
   * Wanneer u grote bestanden sleept en neerzet, kan de Finder de tijd uit nemen terwijl de bestanden op de achtergrond worden overgebracht. Deze vertraging leidt tot een `Error - 36`. U kunt dit probleem omzeilen door het element te slepen en neer te zetten of opnieuw te openen. (CQ-4219628)
   * Het handmatig opnieuw laden van mappen werkt niet altijd. Oplossing: wacht dertig seconden tot de map automatisch wordt bijgewerkt. (CQ-97389)
   * Meer informatie over elementen... is beperkt tot één bestandsselectie. (CQ-89542, CQ-87656)
   * Openen in AEM Assets... is beperkt tot één bestand en één map. (CQ-83382)
   * Fout bij het wijzigen van de naam van elementen zonder extensie. (CQ-4218971)
* Kopiëren/plakken-functionaliteit: Plakken is beschikbaar wanneer er geen element naar het klembord is gekopieerd.
* Windows:
   * Bestanden met alternatieve gegevensstromen (ADS) worden alleen volledig ondersteund op NTFS. Wanneer u bestanden naar de WebDAV-share kopieert via de bureaubladtoepassing, wordt er een waarschuwing weergegeven dat bepaalde bestandseigenschappen niet naar de nieuwe locatie kunnen worden overgebracht. Deze waarschuwing is meestal goed omdat de eigenschappen alleen relevant zijn voor een bepaalde toepassing op het bureaublad van de gebruiker en niets te maken hebben met de feitelijke bestandsinhoud. (CQ-103770) (Win)
   * De gebruiker die de bureaubladtoepassing in Windows gebruikt, moet de gebruiker zijn die de toepassing installeert. (CQ-4216389) (Win)
   * De toepassing kan vastlopen wanneer u de [!UICONTROL Retry] op een mislukte upload. Deze crash kan onder bepaalde omstandigheden optreden nadat het uploaden van de batch is hervat wanneer de verbinding wordt verbroken. (CQ-4251884) (Win)

## Nuttige bronnen {#helpful-resources}

* [Documentatie AEM](https://experienceleague.adobe.com/en/docs)
* [AEM desktop app v1.x gebruiken](use-app-v1.md)
* [Aanbevolen werkwijzen voor desktop app v1.x AEM](best-practices-for-v1.md)

## Compatibiliteitsmatrix en voorwaarden {#compatibilitymatrix}

AEM desktop app werkt met verschillende versies van AEM. Zie de compatibiliteitsmatrix voor de ondersteunde versies.

| Versie | Herziening | Releasedatum | Compatibiliteit |
|--- |--- |--- |--- |
| 1,10 | 1.10.0.3 (Mac en Win) | 31 augustus 2018 | AEM 6.5; AEM 6.4 SP1; AEM 6.3 SP2; AEM 6.2 SP1 GVB2+; AEM 6.1 SP2 GVB7+ |
| 1,9 | 1.9.1.1 (Mac en Win) | 21 juni 2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 GVB2+; AEM 6.1 SP2 GVB7+ |
| 1,8 | 1.8.1.0 (Mac en Win) | 28 maart 2018 | AEM 6.4; AEM 6.3 SP1; AEM 6.2 SP1 GVB2+; AEM 6.1 SP2 GVB7+ |
| 1,7 | 1.7.0.3 (Mac en Win) | 10 januari 2018 | AEM 6.3 SP1; AEM 6.2 SP1 GVB2+; AEM 6.1 SP2 GVB7+ |
