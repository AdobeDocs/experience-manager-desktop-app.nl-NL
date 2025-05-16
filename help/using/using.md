---
title: 'De Desktop app van het gebruik  [!DNL Experience Manager] '
description: Gebruik  [!DNL Adobe Experience Manager]  Desktop app, om met  [!DNL Adobe Experience Manager]  activa te werken DAM recht van uw Desktop van Win of van Mac en gebruik in andere toepassingen.
mini-toc-levels: 1
feature: Desktop App,Asset Management
exl-id: fa19d819-231a-4a01-bfd2-6bba6fec2f18
source-git-commit: fb11b41020a4c2b2c40e8adcde822c65a7fe8985
workflow-type: tm+mt
source-wordcount: '4734'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager] bureaubladtoepassing gebruiken {#use-aem-desktop-app-v2}

Gebruik de bureaubladtoepassing van [!DNL Adobe Experience Manager] om toegang te krijgen tot digitale elementen die zijn opgeslagen in een [!DNL Adobe Experience Manager] DAM-opslagplaats op uw lokale bureaublad. U kunt deze middelen dan in om het even welke Desktoptoepassingen gebruiken. U kunt de elementen lokaal openen en bewerken in bureaubladtoepassingen. Nadat u wijzigingen hebt aangebracht, uploadt u deze weer naar [!DNL Experience Manager] met versiebeheer om updates met andere gebruikers te delen. U kunt ook nieuwe bestanden en maphiërarchieën uploaden naar [!DNL Experience Manager] , mappen maken en elementen of mappen verwijderen van [!DNL Experience Manager] DAM.

Dankzij deze integratie kunnen verschillende rollen in de organisatie de elementen centraal beheren in [!DNL Experience Manager Assets] en toegang krijgen tot de elementen op het lokale bureaublad in de native toepassingen van Windows of macOS.

Wanneer u de toepassing opent na het afmelden of voor het eerst, geeft u de URL van de [!DNL Experience Manager] -server op in de notatie `https://[aem-server-url]:[port]/` . Selecteer vervolgens de optie [!UICONTROL Connect] . Geef referenties op om de toepassing te verbinden met de server.

De belangrijkste taken die u uitvoert met de bureaubladtoepassing van [!DNL Adobe Experience Manager] zijn:

![ Werkschema&#39;s en taken u kunt verwezenlijken gebruikend [!DNL Experience Manager] Desktop app ](assets/aem_desktop_app_usecases_v2.png " Werkschema&#39;s en taken u het gebruiken van  [!DNL Adobe Experience Manager]  Desktop app ") kunt verwezenlijken

<!--Download [this](assets/aem_desktop_app_usecases_print.pdf) print-ready PDF file.-->

## Hoe desktop app werkt {#how-app-works2}

Alvorens u begint de toepassing te gebruiken, begrijp [ hoe app ](release-notes.md#how-app-works) werkt. Zorg ook dat u bekend bent met de volgende termen:

* **[!UICONTROL Desktop Actions]**: Vanuit de Assets-webinterface kunt u vanuit een browser de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw native desktoptoepassing. Deze acties zijn beschikbaar via de webinterface en maken gebruik van de functionaliteit van de bureaubladtoepassing. Zie [ hoe te om de Acties van de Desktop ](using.md#desktopactions-v2) toe te laten.

* Bestandsstatus is **[!UICONTROL Cloud Only]**: dergelijke elementen worden niet gedownload op de lokale computer en zijn alleen beschikbaar op de [!DNL Experience Manager] -server.

* Bestandsstatus is **[!UICONTROL Available locally]**: de elementen worden gedownload en zijn ongewijzigd beschikbaar op de lokale computer. De elementen worden niet gewijzigd.

* Bestandsstatus is **[!UICONTROL Edited locally]**: Dergelijke elementen worden lokaal gewijzigd en de wijzigingen blijven naar de [!DNL Experience Manager] -server geüpload. Nadat u het uploadt, verandert de status in [!UICONTROL Available locally]. Zie [ activa ](using.md#edit-assets-upload-updated-assets) uitgeven.

* Bestandsstatus is **[!UICONTROL Editing conflict]**: als u en anderen tegelijkertijd een element bewerken, geeft de app aan dat er een bewerkingsconflict is opgetreden. De app biedt ook opties om uw wijzigingen te behouden of te negeren. Zie [ hoe te om het uitgeven conflicten ](using.md#adv-workflow-collaborate-avoid-conflicts) te vermijden.

* Bestandsstatus is **[!UICONTROL Modified remotely]**: de app geeft aan of een element dat u hebt gedownload, is gewijzigd op de [!DNL Experience Manager] -server. De app biedt ook de optie om de nieuwste versie te downloaden en uw lokale kopie bij te werken. Zie [ hoe te om het uitgeven conflicten ](using.md#adv-workflow-collaborate-avoid-conflicts) te vermijden.

* **[!UICONTROL Check-out]**: als u een bestand bewerkt of van plan bent een bestand te bewerken, schakelt u de status in en uit. Er wordt een vergrendelingspictogram toegevoegd aan het element in de app en de [!DNL Experience Manager] webinterface. Met het vergrendelingspictogram kunnen andere gebruikers voorkomen dat hetzelfde element tegelijk wordt bewerkt, omdat dit tot een bewerkingsconflict leidt.

* **[!UICONTROL Check-in]**: Markeer het element als veilig voor andere gebruikers om het te bewerken zonder een bewerkingsconflict te veroorzaken. Wanneer u uw wijzigingen uploadt, wordt het vergrendelingspictogram automatisch verwijderd. Als u de incheckstatus inschakelt, wordt ook het vergrendelingspictogram verwijderd. Adobe raadt u echter aan niet handmatig in te checken zonder de wijzigingen te uploaden. Als u de wijzigingen verwijdert, schakelt u het inchecken handmatig in of uit.

* **[!UICONTROL Open]** Handeling: open het element om er een voorvertoning van te bekijken in de oorspronkelijke toepassing. Adobe raadt u aan het middel niet te bewerken door deze handeling te gebruiken. De reden is dat het actief niet wordt uitgecheckt. Ondertussen kunnen andere gebruikers bewerkingen uitvoeren die tot bewerkingsconflicten leiden.

* **[!UICONTROL Open with]** action: Met de functie &quot;Openen met&quot; kunt u een bestand openen met een andere specifieke toepassing dan de standaardtoepassing. Dit is handig als u een voorkeursprogramma wilt kiezen, bestanden in verschillende indelingen wilt openen, problemen met de standaardtoepassing wilt oplossen of meerdere programma&#39;s wilt gebruiken. Het biedt flexibiliteit doordat u de standaardtoepassing tijdelijk kunt overschrijven zonder instellingen permanent te wijzigen.

* **[!UICONTROL Open In Web]** action: Open het element in de webinterface van [!DNL Experience Manager] om het element weer te geven. U kunt vanuit de interface van [!DNL Experience Manager] meer workflows starten, zoals het bijwerken van metagegevens of het detecteren van elementen.

* **[!UICONTROL Edit]** actie: gebruik de actie om de afbeelding te wijzigen. Als u op [!UICONTROL Edit] klikt, wordt het element uitgecheckt en wordt een vergrendelingspictogram toegevoegd aan het element. Klik op Bewerken als u het element niet wilt bewerken en klik vervolgens op [!UICONTROL Toggle check-in] . Als u elementen in de DAM-maphiërarchie van [!DNL Experience Manager] wilt verwijderen, hernoemen of verplaatsen, gebruikt u de [!DNL Experience Manager] webinterfacehandelingen en niet de bewerkingshandeling.

* **[!UICONTROL Download]** Handeling: Download het element naar uw lokale computer. U kunt de elementen nu downloaden en later bewerken. Werk offline en upload de wijzigingen later. Assets wordt gedownload in een cachemap op uw bestandssysteem.

* **[!UICONTROL Reveal File]** of **[!UICONTROL Reveal Folder]** actie: terwijl de elementen naar een lokale cachemap worden gedownload, navigeert de toepassing een lokale netwerkschijf. Het biedt een lokaal pad voor elk element. Als u dit pad wilt weten, gebruikt u de desbetreffende openingsoptie in de app. Actie tonen is vereist om elementen in de Creative Cloud-toepassing te plaatsen. Zie [ plaatselementen ](using.md#place-assets-in-native-documents).

* **[!UICONTROL Delete]** actie: verwijder het element uit de [!DNL Experience Manager] DAM-opslagplaats. Met de handeling wordt de oorspronkelijke kopie van het element op de Experience Manager-server verwijderd. Als u slechts wijzigingen in het lokale activa wilt verwerpen, zie [ veranderingen ](using.md#edit-assets-upload-updated-assets) verwerpen.

* **[!UICONTROL Upload Changes]**: De bureaubladtoepassing uploadt het bijgewerkte element alleen wanneer u het expliciet uploadt naar de [!DNL Experience Manager] -server. Wanneer u uw bewerkingen opslaat, worden de wijzigingen alleen op uw lokale computer opgeslagen. Wanneer u het element uploadt, wordt het automatisch ingecheckt en wordt het vergrendelingspictogram verwijderd. Zie [ activa ](using.md#edit-assets-upload-updated-assets) uitgeven.

## Bureaubladhandelingen inschakelen in de webinterface van [!DNL Experience Manager] {#desktopactions-v2}

Vanuit de gebruikersinterface van [!DNL Assets] in een browser kunt u de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw desktoptoepassing. Deze opties worden [!UICONTROL Desktop Actions] genoemd en zijn niet standaard ingeschakeld. Voer de volgende stappen uit om deze functie in te schakelen.

1. Klik in de [!DNL Assets] -console op het pictogram **[!UICONTROL User]** op de werkbalk.
1. Klik op **[!UICONTROL My Preferences]** om het dialoogvenster **[!UICONTROL Preferences]** weer te geven.

1. Selecteer **[!UICONTROL Show Desktop Actions For Assets]** in het dialoogvenster [!UICONTROL User Preferences] en klik vervolgens op **[!UICONTROL Accept]** .

   ![ Uitgezochte tonen de Acties van de Desktop voor Assets om Desktopacties toe te laten ](assets/enable_desktop_actions.png)

   *Cijfer: Selecteer [!UICONTROL Show Desktop Actions For Assets] om de Acties van de Desktop toe te laten.*

## Elementen weergeven {#view-assets}

Met AEM Desktop App kunt u elementen weergeven in vier verschillende weergaven:

* **[!UICONTROL Show Assets]:** Staat u toe om alle activa te bekijken.
* **[!UICONTROL Show Collections]:** Hiermee kunt u alle verzamelingen weergeven die in de native AEM-toepassing zijn gemaakt. Zie meer [ inzamelingen ](#collections-desktop-app).
* **[!UICONTROL Edited Locally]:** Hiermee kunt u alle lokaal gewijzigde elementen weergeven. In deze weergave kunt u meerdere elementen toevoegen en uploaden.
* **[!UICONTROL Asset transfers]:** Hiermee kunt u alle elementen weergeven die van de native app naar de lokale of andersom zijn overgebracht.
* **[!UICONTROL Pinned items]:** Hiermee kunt u alle vastgezette items weergeven.

Voer de volgende stappen uit om te kiezen uit de verschillende weergaven van middelen in de AEM Desktop-app:

1. Open AEM Desktop App.

1. Ga naar de vervolgkeuzelijst rechtsboven in het scherm. Kies een van de beschikbare weergaven.

   ![ speld of speld omslag ](assets/view-pinned-assets.png) uit

### Nieuw toegevoegde mappen en bestanden weergeven {#view-newly-added-files-folders}

U kunt nieuw gemaakte middelen uploaden van uw lokale computer naar AEM, waar de centrale opslagplaats is opgeslagen. Als u deze nieuwe elementen lokaal wilt weergeven, gaat u naar het vervolgkeuzemenu **[!UICONTROL View]** en selecteert u **[!UICONTROL Show Assets]** om alle updates met hun tijdlijn en titels weer te geven, of selecteert u **[!UICONTROL Edited Locally]** . Beide opties tonen expliciet de lokaal bewerkte elementen.

## Zoeken, zoeken en voorvertonen van elementen {#browse-search-preview-assets}

U kunt vanuit de bureaubladtoepassing bladeren naar de elementen die beschikbaar zijn in de [!DNL Experience Manager] -opslagplaats, deze zoeken en er een voorvertoning van weergeven. Probeer het volgende in de app:

1. Blader naar een map en bekijk basisinformatie over de middelen die beschikbaar zijn in de map, samen met kleine miniaturen van alle elementen.

   ![ doorblader de dossiers DAM en de omslagen ](assets/browse_folder_da2.png " doorbladeren de dossiers DAM en de omslagen ")

1. Klik op de bestandsnaam als u meer informatie en een grotere miniatuur van een afzonderlijk element wilt bekijken.

   ![ zie een grotere voorproef van activa en acties ](assets/large_preview_actions_da2.png " zien een grotere voorproef van activa en acties ")

1. Klik op **[!UICONTROL Open]** of **[!UICONTROL Edit]** om het bestand lokaal te downloaden en het in respectievelijk de oorspronkelijke toepassing weer te geven of te bewerken.
1. Zoek met behulp van trefwoorden naar een verwant element in de [!DNL Experience Manager] -opslagplaats. Gebruik `?` en `*` als jokertekens. Deze jokertekens vervangen een enkel teken of meerdere tekens. Filter de resultaten en sorteer deze zo nodig.

   ![ Onderzoek van de Steekproef gebruikend het vervangingsonderzoek van de asterisk ](assets/search_wildcard_da2.png " Steekproef gebruikend de vervanging van het asterisk ")

   ![ Een ander steekproefonderzoek gebruikend het vervangingsvervanging van het asterisk ](assets/search_wildcard2_da2.png " Een ander steekproefonderzoek met verschillende plaatsing van het asteriskvervanging ")

>[!NOTE]
>
>In de app worden de elementen weergegeven door de zoekcriteria af te stemmen op meerdere metagegevensvelden en niet alleen op de titel van het element of de bestandsnaam.

## Assets Management {#assets-management}

Middelenbeheer omvat het organiseren, onderhouden en optimaliseren van digitale middelen om workflows te stroomlijnen. Dit omvat taken zoals het dupliceren en hernoemen van bestanden, het vastzetten of verwijderen van mappen voor snelle toegang, en het weergeven van elementen in verschillende lay-outs. Dit verbetert de efficiëntie, vereenvoudigt het bijhouden van bedrijfsmiddelen en zorgt ervoor dat digitale middelen eenvoudig kunnen worden opgehaald en geordend op verschillende platforms.

### Bestanden dupliceren {#duplicate-files}

Wanneer u een origineel bestand wilt behouden en wijzigingen wilt aanbrengen in het vergelijkbare bestand, kunt u bestanden op verschillende locaties (lokaal en in de cloud) tegelijk dupliceren. Dit kan worden bereikt door dubbele bestandsbewerkingen uit te voeren tussen elementen.

Voer de volgende stappen uit om bestanden te dupliceren in AEM Desktop App:

1. Blader naar een map en selecteer het element dat u wilt dupliceren.

   ![ Dubbele dossiers ](assets/more-options.png)

1. Klik **[!UICONTROL More actions]** ![ Meer actiepictogram ](assets/do-not-localize/more2_da2.png) en selecteer ![ dubbel pictogram ](assets/do-not-localize/duplicate.svg) **[!UICONTROL Duplicate File]** actie.

1. Het gedupliceerde bestand wordt gemaakt met dezelfde bestandsnaam en inhoud.

### De naam van een element wijzigen {#rename-asset-title}

Voer de onderstaande stappen uit om de naam van een element te wijzigen:

1. Blader door het element waarvan u de naam wilt wijzigen.

1. Klik **[!UICONTROL More actions]** ![ Meer actiepictogram ](assets/do-not-localize/more2_da2.png) en selecteer **[!UICONTROL Rename]** om uw gewenste titel van een activa toe te voegen.

<!--1. Click **[!UICONTROL More actions]** ![More actions icon](assets/do-not-localize/more2_da2.png) and select **[!UICONTROL open in web]** to open the asset in its native application.

1. Go to asset details. Under [!UICONTROL Basic] tab, go to title and enter the text.-->

### Map vastzetten of vastzetten {#pin-unpin-folder}

Voor snelle toegang kunt u een map vastzetten of vrijmaken door de onderstaande stappen uit te voeren:

1. Blader door het element dat u wilt vastzetten of vrijmaken.

1. Klik **[!UICONTROL More actions]** ![ Meer actiepictogram ](assets/do-not-localize/more2_da2.png) en selecteer [!UICONTROL pin] om de activa of de omslag vast te zetten. U kunt ook op [!UICONTROL unpin] klikken om het vastzetten ongedaan te maken.

   ![ speld of speld omslag ](assets/pin-unpin.png) uit

### Automatisch vernieuwen {#auto-refresh}

Met de functie Automatisch vernieuwen wordt inhoud automatisch in real-time bijgewerkt. Zo weet u zeker dat u altijd de meest recente informatie ziet zonder de pagina handmatig opnieuw te laden. Voer de onderstaande stappen uit om elementen automatisch te vernieuwen om de lijst met bijgewerkte elementen op te halen:

1. Open AEM Desktop App.

1. Klik ![ verfrissen pictogram ](assets/do-not-localize/refresh.png) op de menubar om de updates te krijgen.

## Elementen downloaden {#download-assets}

U kunt de elementen downloaden naar uw lokale bestandssysteem. De toepassing haalt de elementen op van de [!DNL Experience Manager] -server en slaat dezelfde kopie op uw lokale bestandssysteem op.

Klik **[!UICONTROL More actions]** ![ Meer optiepictogram ](assets/do-not-localize/more2_da2.png) voor opties en klik ![ pictogram van de Download ](assets/do-not-localize/download_cloud_da2.png) om te downloaden.

![ optie van de Download voor een activa ](assets/download_option_da2.png " optie van de Download voor een activa ")

>[!NOTE]
>
>Wanneer u een groot bestand of een groot aantal bestanden downloadt of uploadt, schakelt de toepassing de handelingen voor elementen en mappen uit. De acties zijn beschikbaar wanneer het downloaden of uploaden is voltooid.

Het downloaden van meerdere elementen kan leiden tot slechte prestaties als de wachtrij groot is of als u te maken krijgt met een netwerkprobleem. Bovendien kunt u bij het downloaden van een map onbewust veel bestanden in de wachtrij plaatsen. Om lange wachttijden te vermijden, beperkt app het aantal elementen dat in één keer wordt gedownload. Om te weten hoe te om het te vormen, zie [ Vastgestelde voorkeur ](install-upgrade.md#set-preferences). Zelfs onder deze limiet kan de app soms om bevestiging vragen voordat een ogenschijnlijk grote map wordt gedownload.

![ App bevestigt download van vrij groot aantal activa ](assets/download_confirmation_da2.png " App bevestigt download van vrij groot aantal activa ")

Als mappen zijn geselecteerd en gedownload, downloadt de toepassing alleen elementen die rechtstreeks in de mappen in [!DNL Experience Manager] zijn opgeslagen. Elementen worden niet automatisch uit submappen gedownload.

## Elementen op uw bureaublad openen {#openondesktop-v2}

U kunt de externe middelen openen voor weergave in de oorspronkelijke toepassing. De middelen worden gedownload naar een lokale map. Vervolgens worden ze gestart in de oorspronkelijke toepassing die aan de bestandsindeling is gekoppeld. U kunt de oorspronkelijke toepassing wijzigen en specifieke bestandstypen (extensies) openen in uw Mac of Windows.

Klik op **[!UICONTROL Open]** in het menu Middelen. Het element wordt lokaal gedownload en in de oorspronkelijke toepassing geopend. Controleer de voortgang van het downloaden en de overdrachtssnelheid van grote middelen op de statusbalk.

<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")
-->

>[!NOTE]
>
>Als de verwachte veranderingen niet in app worden weerspiegeld, verfrist de klik pictogram ![ vernieuwt pictogram ](assets/do-not-localize/refresh.png) of klikt met de rechtermuisknop in app interface en klikt **[!UICONTROL Refresh]**. De acties zijn niet beschikbaar wanneer grotere downloads of uploads worden uitgevoerd.

Om de lokale downloadomslag van een activa te openen, klik ![ Meer actiepictogram ](assets/do-not-localize/more2_da2.png) en klik ![ onthullen pictogram ](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** actie.

## Verzamelingen {#collections-desktop-app}

AEM App van de Desktop staat u toe om [&#128279;](#view-collections-desktop-app) te bekijken, [ download ](#download-collections-desktop-app) en doorblader inzamelingen die op [!DNL Adobe Experience Manager Assets] toepassing worden gecreeerd.

### Verzamelingen weergeven {#view-collections-desktop-app}

Voer de volgende stappen uit om verzamelingen in de bureaubladtoepassing weer te geven:

1. Open App van de Desktop van AEM en ga naar [ meningsactiva ](#view-assets).

1. Selecteer **[!UICONTROL Show Collections]**. De verzamelingen die beschikbaar zijn in de oorspronkelijke toepassing, worden weergegeven.

   ![ de Desktop van Inzamelingen App ](assets/collections-desktop-app.png)

### Verzamelingen downloaden {#download-collections-desktop-app}

Voer de volgende stappen uit om verzamelingen in de bureaubladtoepassing te downloaden:

1. Volg stappen 1 en 2 zoals aangetoond in [ meningsinzamelingen ](#view-collections-desktop-app).

1. Ga naar meer acties ![ Meer actiepictogram ](assets/do-not-localize/more2_da2.png) op de inzameling die u wilt downloaden.

1. Klik op **[!UICONTROL Download]** om de desbetreffende verzameling te downloaden.

## Map maken met metagegevensschema {#create-folder-with-metadata-schema}

Met de AEM Desktop App kunt u metagegevens toewijzen tijdens het maken van een nieuwe map. Voer daartoe de volgende stappen uit:

1. Ga om folderpictogram tot stand te brengen ![ voeg omslagpictogram ](assets/do-not-localize/add-folder.svg) toe. **[!UICONTROL Create Directory]** wordt weergegeven.

1. Voeg de volgende details toe:
   * **[!UICONTROL Name]** van de map.
   * **[!UICONTROL Folder Metadata Schema]** om een hiërarchie van metagegevens in de map te kiezen of kies **[!UICONTROL none]** als u er geen metagegevens aan wilt koppelen.

1. Klik op **[!UICONTROL OK]** om verder te gaan.

## Elementen gebruiken of plaatsen in eigen documenten {#place-assets-in-native-documents}

In sommige gevallen, bijvoorbeeld wanneer het plaatsen van activa in een inheems document, hebt u toegang tot een dossier in de Ontdekkingsreiziger van Vensters of de Vinder van Mac. Om aan de plaats van het dossiersysteem van het plaatselijk gedownloade dossier te krijgen, gebruik ![ het pictogram ](assets/do-not-localize/reveal_action2_da2.png) **[!UICONTROL Reveal File]** optie onthullen.

![ openbaart de actie van het Dossier voor een activa ](assets/revealfile_action_da2.png " onthullen actie van het Dossier voor een activa ")

Klik op **[!UICONTROL Reveal File]** of **[!UICONTROL Reveal Folder]** in een map om Windows Verkenner of de Finder van Mac te openen met het bestand of de map die vooraf op uw lokale computer is geselecteerd. De optie is bijvoorbeeld handig om de [!DNL Experience Manager] -bestanden te plaatsen in de native toepassingen die het plaatsen of koppelen van lokale bestanden ondersteunen. Om te zien hoe te om dossiers in Adobe InDesign te plaatsen, zie [ Plaatsende grafiek ](https://helpx.adobe.com/indesign/using/placing-graphics.html).

Met de handeling **[!UICONTROL Reveal File]** wordt een lokaal gedeelde netwerk geopend. Alleen de elementen die lokaal beschikbaar zijn, worden weergegeven. Dit betekent dat er elementen worden weergegeven die met de app zijn onthuld, gedownload of geopend/bewerkt. Het lokale netwerkaandeel uploadt geen veranderingen in [!DNL Experience Manager]. Als u de wijzigingen wilt uploaden, gebruikt u expliciet de handelingen **[!UICONTROL Upload Changes]** of **[!UICONTROL Upload]** in de app.

>[!NOTE]
>
>Voor achterwaartse compatibiliteit met [!DNL Experience Manager] desktop app v1.x, worden de vrijgegeven bestanden via een lokaal netwerkaandeel gebruikt, waarbij alleen lokaal beschikbare bestanden beschikbaar worden gemaakt. De bureaubladpaden van de onthulde bestanden zijn gelijk aan de paden die door app v1.x worden gemaakt.

>[!CAUTION]
>
>Gebruik de optie **[!UICONTROL Reveal File]** niet om elementen in native toepassingen te bewerken. Gebruik in plaats daarvan de handelingen **[!UICONTROL Edit]** . Meer weten, zie [ Geavanceerd werkschema: werk aan de zelfde dossiers samen en vermijd het uitgeven conflicten ](#adv-workflow-collaborate-avoid-conflicts).

## Elementen bewerken en bijgewerkte elementen uploaden naar [!DNL Experience Manager] {#edit-assets-upload-updated-assets}

Open elementen voor bewerking wanneer u wijzigingen wilt aanbrengen en de bijgewerkte elementen naar de [!DNL Experience Manager] -server wilt uploaden. U voorkomt conflicten met bewerkingen door andere gebruikers door met de app een bewerkingssessie te starten. Voordat u begint met bewerken, moet u ervoor zorgen dat het element geen vergrendelingspictogram heeft dat aangeeft dat een andere gebruiker het element bewerkt.

Als u een element wilt bewerken, zoekt u het element of bladert u naar de locatie van het element. Klik ![ Meer pictogram ](assets/do-not-localize/more2_da2.png) en klik **[!UICONTROL Edit]**.

Gebruik **[!UICONTROL Toggle Check-out]** om het element te vergrendelen om conflicten te voorkomen met bewerkingen van andere gebruikers in beide volgende situaties:

* U hebt een middel bewerkt zonder het eerst uit te checken (bijvoorbeeld door het alleen te openen).
* U bent van plan binnenkort met het bewerken van een element te beginnen en wilt niet dat anderen dit bewerken.

Nadat u alle bewerkingen hebt uitgevoerd, geeft de app de **[!UICONTROL Edited Locally]** -status voor de gewijzigde elementen weer. Alle wijzigingen die in de elementen zijn opgeslagen, zijn alleen lokaal totdat u de wijzigingen in [!DNL Experience Manager] uploadt. Als u een individu of een paar elementen een voor een wilt uploaden, klikt u op **[!UICONTROL Upload Changes]** in de opties voor een element. Er wordt een versie van het element gemaakt in [!DNL Experience Manager] . Gebruikend de interface van het Web van [!DNL Assets], kunt u activageschiedenis in de [ mening van de Chronologie ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/using/activity-stream) zien.

![ uploadt veranderingsoptie in app ](assets/upload_changes_single1_da2.png " uploadt veranderingsoptie in app ")

![ uploadt veranderingen optie wanneer het bekijken van een grote voorproef van activa ](assets/upload_changes_single2_da2.png " veranderingen uploadt optie wanneer het bekijken van een grote voorproef van activa ")

Voor beste praktijken rond samenwerkings het uitgeven, zie [ Geavanceerd werkschema: werk aan de zelfde dossiers samen en vermijd het uitgeven conflicten ](#adv-workflow-collaborate-avoid-conflicts).

In de volgende gevallen kunt u uw wijzigingen en bewerkingen in het lokale element negeren. Klik op **[!UICONTROL Discard Changes]**.

* Als u uw wijzigingen niet lokaal wilt opslaan in [!DNL Experience Manager] .
* Breng wijzigingen aan in het oorspronkelijke element nadat u enkele wijzigingen hebt opgeslagen.
* Bewerk het element niet meer omdat dit niet meer nodig is.

Schakel indien nodig het uitchecken in. Het bijgewerkte element wordt verwijderd uit de lokale cachemap en wordt opnieuw gedownload wanneer u het bewerkt of opent.

## Nieuwe elementen uploaden en toevoegen aan [!DNL Experience Manager] {#upload-and-add-new-assets-to-aem}

Gebruikers kunnen nieuwe elementen toevoegen aan de DAM-opslagplaats. U kunt bijvoorbeeld een fotograaf of contractant zijn die een groot aantal foto&#39;s van een fotoshoot wil toevoegen aan de [!DNL Experience Manager] -opslagplaats. Om nieuwe inhoud aan [!DNL Experience Manager] toe te voegen, uitgezochte ![ uploadt aan wolkenoptie ](assets/do-not-localize/upload_to_cloud_da2.png) in de top-bar van app. Blader naar de elementbestanden in het lokale bestandssysteem en klik op **[!UICONTROL Select]** . U kunt ook elementen uploaden door de bestanden of mappen naar de toepassingsinterface te slepen. Als u in Windows elementen naar een map in de app sleept, worden de elementen naar de map geüpload. Als het langer duurt om te uploaden, geeft de app een voortgangsbalk weer.

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

U kunt mappen of afzonderlijke bestanden uploaden vanuit uw lokale bestandssysteem. De maphiërarchie blijft behouden wanneer deze wordt geüpload. Alvorens activa in bulk te uploaden, zie [ Bulk uploadt ](#bulk-upload-assets).

Als u de lijst met elementen wilt weergeven die in een bepaalde sessie zijn overgedragen, klikt u op **[!UICONTROL View]** > **[!UICONTROL Assets transfers]** . In de lijst kunt u de bestandsoverdrachten van de huidige sessie weergeven en snel verifiëren.

![ Lijst van overgebrachte activa in een bepaalde zitting ](assets/assets_transfered_da2.png " Lijst van overgebrachte activa in een bepaalde zitting ")

U kunt de uploadsnelheid (versnelling) bepalen in de instelling **[!UICONTROL Preferences]** > **[!UICONTROL Upload acceleration]** . Meer gelijktijdige uitvoering levert doorgaans snellere uploads op, maar kan ook bronintensief zijn en meer verwerkingskracht van de lokale machine verbruiken. Als u een traag systeem ervaart, uploadt u opnieuw met een lagere waarde voor gelijktijdige uitvoering.

>[!NOTE]
>
>De overdrachtlijst is niet blijvend en is niet beschikbaar als u de app afsluit en opnieuw opent.

<!--### Upload local file to AEM {#upload-local-file-to-aem}-->


### Speciale tekens in elementnamen beheren {#special-characters-in-filename}

In de verouderde app behielden de namen van knooppunten die in de repository zijn gemaakt de ruimten en behuizing van de mapnamen die door de gebruiker zijn verschaft. Schakel [!UICONTROL Use legacy conventions when creating nodes for assets and folders] in de [!UICONTROL Preferences] in als de huidige toepassing de regels voor nodenamen van de v1.10-app moet emuleren. Zie [ app voorkeur ](/help/using/install-upgrade.md#set-preferences). Deze oudere voorkeur is standaard uitgeschakeld.

>[!NOTE]
>
>De app wijzigt alleen de knooppuntnamen in de repository met behulp van de volgende naamconventies. De app behoudt de `Title` van het element zoals deze is.

<!-- TBD: Do NOT use this table.

| Where do characters occur | Characters | Legacy preference | Renaming convention | Example |
|---|---|---|---|---|
| In file name extension | `.` | Enabled or disabled | Retained as is | NA |
| File or folder name | `. / : [ ] | *` | Enabled or disabled | Replaced with a `-` (hyphen) | `myimage.jpg` remains as is and `my.image.jpg` changes to `my-image.jpg`. |
| Folder name | `% ; # , + ? ^ { } "` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | `% # ? { } &` | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Whitespaces | Enabled or disabled | Retained as is | NA |
| Folder name | Whitespaces | Disabled | Replaced with a `-` (hyphen) | tbd |
| File name | Uppercase characters | Disabled | Retained as is | tbd |
| Folder name | Uppercase characters | Disabled | Replaced with a `-` (hyphen) | tbd |
-->

| Tekens ‡ | Oudere voorkeur in app | Wanneer voorkomen in bestandsnamen | Indien voorkomend in mapnamen | Voorbeeld |
|---|---|---|---|---|
| `. / : [ ] \| *` | In- of uitgeschakeld | Vervangen door `-` (afbreekstreepje). Een `.` (punt) in de bestandsnaamextensie blijft ongewijzigd. | Vervangen door `-` (afbreekstreepje). | `myimage.jpg` blijft ongewijzigd en `my.image.jpg` verandert in `my-image.jpg` . |
| `% ; # , + ? ^ { } "` en spaties | ![ deselecteert pictogram ](assets/do-not-localize/deselect-icon.png) Gehandicapte | Werkruimten blijven behouden | Vervangen door `-` (afbreekstreepje). | `My Folder.` verandert in `my-folder-` . |
| `# % { } ? & .` | ![ deselecteert pictogram ](assets/do-not-localize/deselect-icon.png) Gehandicapte | Vervangen door `-` (afbreekstreepje). | NA. | `#My New File.` verandert in `-My New File-` . |
| Hoofdletters | ![ deselecteert pictogram ](assets/do-not-localize/deselect-icon.png) Gehandicapte | Trappen blijft ongewijzigd. | Veranderd in kleine letters. | `My New Folder` verandert in `my-new-folder` . |
| Hoofdletters | ![ selectie gecontroleerd pictogram ](assets/do-not-localize/selection-checked-icon.png) Toegelaten | Trappen blijft ongewijzigd. | Trappen blijft ongewijzigd. | NA. |

‡ De lijst met tekens is een lijst met door spaties gescheiden tekens.

<!-- TBD: Check if the following is to be included in the footnote.

Do not use &#92;&#92; in the names of files and &#92;&#116; &#38; in the names of folders. 
-->


<!-- TBD: Securing the below presentation of the same content in a comment.

**File names**

| Characters | Replaced by |
|---|---|
| &#35; &#37; &#123; &#63; &#125; &#38; &#46; &#47; &#58; &#91; &#124; &#93; &#42; | hyphen (-) |
| whitespaces | whitespaces are retained |
| capital case | casing is retained |

>[!CAUTION]
>
>Avoid using &#92;&#92; in file names.

**Folder names**

| Characters | Replaced by |
|---|---|
| Characters | Replaced by |
| &#37; &#59; &#35; &#44; &#43; &#63; &#94; &#123; &#123; &#34; &#46; &#47; &#59; &#91; &#93; &#124; &#42; | hyphen (-) |
| whitespaces | hyphen (-) |
| capital case | lower case |

>[!CAUTION]
>
>Avoid using &#92;&#92; &#92;&#116; &#38; in folder names.

>[!NOTE]
>
>If you enable [!UICONTROL Use legacy conventions when creating nodes for assets and folders] in app [!UICONTROL Preferences], then the app emulates v1.10 app behavior when uploading folders. In v1.10, the node names created in the repository respect spaces and casing of the folder names provided by the user. For more information, see [app Preferences](/help/using/install-upgrade.md#set-preferences).

-->

## Werken met meerdere elementen {#work-with-multiple-assets}

Gebruikers kunnen eenvoudig met meerdere elementen werken en deze beheren door bijvoorbeeld alle bewerkingen in één keer te uploaden of geneste mappen met een paar klikken te uploaden.

### Door grote mappen bladeren {#browse-large-folders}

Als u werkt met mappen die veel elementen bevatten, schuift u naar meer elementen. Als u met het toetsenbord wilt schuiven, drukt u een paar keer op de tab om het element aan de bovenkant te selecteren. Let op het gemarkeerde element om te weten wanneer het is geselecteerd. Gebruik nu de toets Pijl-omlaag om door de lijst met elementen te gaan.

### Snelle handelingen voor geselecteerde elementen {#quick-actions-for-selected-assets}

Klik op de miniatuur van een paar elementen om de elementen te selecteren. Als u alle elementen wilt selecteren, klikt u op het selectievakje in de bovenste balk van de app. De set handelingen die van toepassing is op alle geselecteerde elementen samen worden weergegeven op een werkbalk onder aan de app.

![ Toolbar bij de bodem toont acties relevant voor de geselecteerde activa ](assets/actions_bottom_toolbar1_da2.png " De toolbar bij de bodem toont gemeenschappelijke acties voor de geselecteerde activa ")

![ Geen acties in toolbar wanneer geen gemeenschappelijke acties voor de selectie ](assets/actions_bottom_toolbar2_da2.png " toont de toolbar geen acties wanneer de gemeenschappelijke acties niet voor de selectie beschikbaar zijn.")

Welke acties beschikbaar zijn op de werkbalk onderaan, is afhankelijk van de status van de geselecteerde bestanden. Als u bijvoorbeeld alleen **[!UICONTROL Edited Locally]** bestanden selecteert, wordt het pictogram **[!UICONTROL Upload Changes]** weergegeven. Als u een combinatie van **[!UICONTROL Edited locally]** en **[!UICONTROL Cloud only]** selecteert, is de handeling **[!UICONTROL Upload Changes]** niet beschikbaar.

### Alle bewerkte afbeeldingen zoeken {#find-all-edited-images}

De toepassing biedt een weergave met de naam **[!UICONTROL Edited locally]** , waarmee u snel toegang krijgt tot alle bestanden die u lokaal hebt gedownload (via [!UICONTROL Open] - of [!UICONTROL Edit] -acties) en die u vervolgens wijzigt. Met de app kunt u alle lokaal bewerkte elementen selecteren en de wijzigingen met een paar klikken uploaden. In deze weergave worden ook de lokaal bewerkte elementen weergegeven die een bewerkingsconflict hebben.

![ Filter om alle plaatselijk uitgegeven activa ](assets/edited_locally_filter_da2.png " te zien Bijvoorbeeld, filter om alle plaatselijk uitgegeven activa voor een massa te zien uploadt van uitgeeft ")

### Bulkupload-elementen {#bulk-upload-assets}

Gebruikers of organisaties, zoals fotografen of creatieve bureaus, kunnen een groot aantal lokale elementen maken tijdens activiteiten zoals foto&#39;s, retoucheren of het selecteren van een grotere set. Deze taken worden vaak uitgevoerd buiten [!DNL Experience Manager] . Ze kunnen deze grote lokale mappen rechtstreeks vanuit de bureaubladtoepassing uploaden naar [!DNL Assets] . De maphiërarchieën blijven behouden en alle geneste submappen en opgenomen elementen worden geüpload. De geüploade elementen zijn direct ook beschikbaar voor andere gebruikers van dezelfde server. Assets worden op de achtergrond geüpload, zodat de bewerking niet aan een webbrowsersessie is gekoppeld.

![ Bulk uploadt veelvoudige lokale omslagen van uw Desktop in [!DNL Experience Manager]](assets/upload_local_folders_da2.png " Bulk uploadt veelvoudige lokale omslagen van uw Desktop in Experience Manager ")

Na het uploaden, als de verwachte veranderingen niet in app worden weerspiegeld, klik verfrissen pictogram ![ pictogram ](assets/do-not-localize/refresh.png) verfrissen.

>[!NOTE]
>
>Gebruik geen uploadfunctionaliteit om elementen over twee [!DNL Experience Manager] -implementaties te migreren. In plaats daarvan, zie de [ migratiegids ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide).

### Lijst van overgedragen elementen {#list-of-transferred-assets}

Om de lijst van activa te bekijken die in een bepaalde zitting worden overgebracht, zie [ activa uploaden aan  [!DNL Experience Manager]](#upload-and-add-new-assets-to-aem).

## Geavanceerde workflow: start vanuit de webinterface van [!DNL Assets] {#adv-workflow-start-from-aem-ui}

Start zo nodig uw workflow via de Assets-webinterface. De desktop-app integreert met de [!DNL Experience Manager] die op verzoek kan worden overgenomen met behulp van desktophandelingen.

Een speciaal geval van het beginnen van een werkschema van de interface van het Web is activaontdekking. De bar van het Onderzoek in het gebruikersinterface van Assets biedt een rijke en geavanceerde onderzoekservaring aan. U kunt desgewenst eerst een gewenst middel op het web zoeken en vervolgens de workflow in de app starten met [!UICONTROL Desktop Actions] . Sommige voorbeeldgevallen omvatten het filtreren onderzoeksresultaten gebruikend facetten, het vinden van een specifiek middel in licentie gegeven van Adobe Stock, of een aanpassing die door uw organisatie wordt uitgevoerd die u betere ontdekking van de interface van het Web toestaat.

De functionaliteit van de Desktop-app wordt gebruikt wanneer u de volgende handelingen probeert uit te voeren in de Assets Web-interface:

* De [!UICONTROL Desktop Actions] die [!UICONTROL Open] , [!UICONTROL Edit] en [!UICONTROL Reveal] toestaan
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] of [!UICONTROL check-in]

De acties in de webinterface die beschikbaar zijn voor een element dat is uitgecheckt in de app, zijn bijvoorbeeld [!UICONTROL Open], [!UICONTROL Reveal] en [!UICONTROL Check in] .

![ Acties van de Desktop in de [!DNL Experience Manager] interface van het Web ](assets/assets_web_actions_da2.png " Acties van de Desktop in de interface van het Web van Experience Manager ")

>[!NOTE]
>
>Mogelijk wordt u door de browser gevraagd het starten van [!DNL Adobe Experience Manager] Desktop toe te staan. Als u elke keer een ononderbroken overdracht van de browser naar de app wilt uitvoeren, schakelt u het desbetreffende selectievakje in zodat de app de toepassing kan overnemen.

U kunt niet de volgende informatie of het werkschema vinden gebruikend de interface van het Web. Gebruik de bureaubladtoepassing omdat de webinterface lokale wijzigingen niet bijhoudt en zich niet bewust is van het volgende:

* Bestanden worden lokaal bewerkt.
* Bestanden met een bewerkingsconflict en een manier om dit op te lossen.
* Lokale wijzigingen uploaden naar [!DNL Experience Manager] .
* Verschillende statussen van de lokaal beschikbare bestanden.

Integendeel, u kunt het element met de handeling **[!UICONTROL Open In Web]** openen in de webinterface vanaf de bureaubladtoepassing.

## Geavanceerde workflow: samenwerken aan dezelfde bestanden en bewerkingsconflicten voorkomen {#adv-workflow-collaborate-avoid-conflicts}

In samenwerkingsomgevingen kunnen meerdere gebruikers werken aan dezelfde set elementen die tot versieconflicten kunnen leiden. Volg de volgende aanbevolen procedures om conflicten te voorkomen:

* Bewerk geen elementen door op [!UICONTROL Open] te klikken. Bewerk de lokaal gedownloade elementen niet door deze te openen vanuit de bestandssysteemmap. Andere gebruikers weten niet dat het element wordt bewerkt.
* Als u een element wilt bewerken, klikt u altijd op [!UICONTROL Edit] . Het element wordt geopend in de oorspronkelijke toepassing en er wordt een vergrendelingspictogram toegevoegd aan het element, zodat de andere gebruikers weten dat het element wordt bewerkt.
* Klik op [!UICONTROL Toggle Check-in] als u per ongeluk begint met bewerken zonder op [!UICONTROL Edit] te klikken. Met deze functie voegt u een vergrendelingspictogram toe aan het element. Zelfs als u een element later wilt bewerken, maar u wilt voorkomen dat anderen het bewerken, klikt u op [!UICONTROL Toggle Check-in] om het element te vergrendelen.
* Voordat u een element bewerkt, moet u ervoor zorgen dat andere gebruikers het element niet bewerken. Zoek het slotpictogram op de activa.
* Na het voltooien van de bewerkingen uploadt u alle wijzigingen en checkt u het element in.

![ Statussen van het uitgeven van conflicten ](assets/edits_conflicts_status_da2.png " Statussen van het uitgeven van conflicten ")

Als een lokaal gedownload element wordt bijgewerkt op de [!DNL Experience Manager] -server, geeft de app een **[!UICONTROL Modified remotely]** -status weer. U kunt de lokale kopie verwijderen of de lokale kopie vernieuwen door respectievelijk op [!UICONTROL Remove] of [!UICONTROL Update] te klikken. Met de koppelingen in het dialoogvenster kunt u beide versies van het element weergeven.

![ Opties om het conflict op te lossen wanneer het middel ](assets/modified_remotely_dialog_da2.png " Opties ver wordt gewijzigd om het conflict op te lossen wanneer het middel ver wordt gewijzigd ")

Als een middel dat u lokaal bewerkt ook zonder uw medeweten op de server wordt bijgewerkt, geeft de app een **[!UICONTROL Editing Conflict]** status weer. U kunt één set wijzigingen behouden. U kunt de updates behouden (klik op **[!UICONTROL Keep Mine]** ) en de bewerking van de andere gebruiker verwijderen, of de updates van de andere gebruiker respecteren en uw wijzigingen verwijderen (**[!UICONTROL Overwrite Mine]** ).

![ Opties om een het uitgeven conflict ](assets/editing_conflict_dialog_da2.png " Opties op te lossen om een het uitgeven conflict ") op te lossen

## Geavanceerde workflow: middelen plaatsen en koppelen in InDesign-bestand {#adv-workflow-place-assets-indesign}

Wanneer u de bureaubladtoepassing van [!DNL Experience Manager] gebruikt om bestanden met gekoppelde elementen te openen, worden de elementen vooraf gedownload en in de oorspronkelijke toepassingen geplaatst. Deze workflow werkt alleen als uw oorspronkelijke toepassing het plaatsen van koppelingen naar lokale elementen ondersteunt en [!DNL Experience Manager] het oplossen van deze koppelingen in binaire bestanden naar verwijzingen naar de server ondersteunt.

De bureaubladtoepassing van [!DNL Experience Manager] ondersteunt deze workflow met een aantal geselecteerde Adobe Creative Cloud-bureaubladtoepassingen en -bestandsindelingen - Adobe InDesign, Adobe Illustrator en Adobe Photoshop. Met de workflow kunt u efficiënt werken met de ondersteunde Creative Cloud-bestanden. Als gebruiker A elementen toevoegt aan een InDesign-bestand en dit incheckt in [!DNL Experience Manager] , kan gebruiker B de elementen in het bestand zien, ook al maken deze geen deel uit van het bestand. De middelen worden plaatselijk gedownload op de machine van gebruiker B.

>[!NOTE]
>
>De bureaubladtoepassing kan worden toegewezen aan elk station in Windows. Wijzig de standaardstationsletter echter niet voor vloeiende bewerkingen. Als gebruikers van dezelfde organisatie verschillende stationsletters gebruiken, kunnen ze de elementen die door anderen zijn geplaatst, niet zien. De geplaatste elementen worden niet opgehaald wanneer het pad verandert. De geplaatste elementen blijven in het binaire bestand (bijvoorbeeld INDD) staan en worden niet verwijderd.

Om de beperkingen van dit werkschema te kennen, zie de [ systeemvereisten en gesteunde versies ](release-notes.md).

Voer de volgende stappen uit om deze workflow te testen met een afbeeldingselement en InDesign:

1. Behoud een INDD-bestand met geplaatste elementen in [!DNL Experience Manager]. Om te weten hoe te om zulk een INDD dossier tot stand te brengen, zie [ Plaatsende Grafieken ](https://helpx.adobe.com/indesign/using/placing-graphics.html).
1. Vanuit de bureaubladtoepassing **[!UICONTROL Edit]** wordt het INDD-bestand met elementen in [!DNL Experience Manager] geplaatst.
1. De app downloadt het InDesign-bestand en de gekoppelde middelen. Wanneer InDesign het document opent, worden de koppelingen opgelost, worden de elementen gedownload en worden de elementen weergegeven in het InDesign-document.
1. Als u een nieuwe afbeelding in het InDesign-bestand wilt plaatsen, gebruikt u de handeling **[!UICONTROL Reveal File]** op het element. De actie downloadt plaatselijk activa en opent de lokale plaats van het netwerkaandeel in de Ontdekkingsreiziger van Vensters of de Vinder van Mac.
1. Plaats het onthulde element in het InDesign-document. Hiermee maakt u een koppeling in het document.
1. Nadat u de bewerkingen in het InDesign-document hebt voltooid, slaat u het document op en uploadt u het naar [!DNL Experience Manager] met de bureaubladtoepassing.

## Geavanceerde workflow: download de middelen lokaal {#adv-workflow-download-assets-locally}

De toepassing downloadt vaak elementen van de [!DNL Experience Manager] -server naar uw lokale bestandssysteem. De downloads verbruiken bandbreedte en schijfruimte. Als u de scenario&#39;s kent, kunt u de wachttijd tot de downloads zijn voltooid, optimaliseren.

U kunt de middelen van binnen app downloaden op bestelling. Zie [ activa van de Download ](#download-assets).

Wanneer u de handeling [!UICONTROL Open] gebruikt om middelen te openen in een native bureaubladtoepassing, wordt het element lokaal gedownload als dit nog niet lokaal beschikbaar is. Zie [ Open activa ](#openondesktop-v2).

Wanneer u de locatie van een middel of een map vanuit de app weergeeft, wordt het middel of de map eerst lokaal gedownload en vervolgens op uw computer geopend in het gedeelde lokale netwerk. Zie [ Open activa ](#openondesktop-v2).

Wanneer u de handeling [!UICONTROL Edit] gebruikt om middelen in een native desktoptoepassing te bewerken, wordt het element lokaal gedownload als dit nog niet lokaal beschikbaar is. Zie [ activa uitgeven en bijgewerkte activa aan  [!DNL Experience Manager]](#edit-assets-upload-updated-assets) uploaden.

Als de app is geïnstalleerd en hierop is toegestaan, worden de acties voltooid wanneer u [!UICONTROL Desktop Actions] vanuit de webinterface van [!DNL Experience Manager] gebruikt. De app downloadt het middel eerst en voltooit de actie.
