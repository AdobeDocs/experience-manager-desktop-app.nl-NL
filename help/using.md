---
title: Adobe Experience Manager-bureaubladtoepassing gebruiken
description: Leer hoe u de Adobe Experience Manager-bureaubladtoepassing installeert en gebruikt, zodat u direct vanaf uw Win- of Mac-bureaublad met Adobe Experience Manager DAM-middelen kunt werken. Kennis van de beste praktijken en het oplossen van problemeninformatie.
uuid: 55057617-89de-43cd-8419-1252a42ab2fb
contentOwner: AG
products: SG_EXPERIENCEMANAGER/6.3/ASSETS
discoiquuid: 39d7bcad-d7b0-4978-a790-4cb68b8a7d6a
mini-toc-levels: 1
translation-type: tm+mt
source-git-commit: ac4be2cb69a112f393ec76d5d95987634d0c9c46

---


# Adobe Experience Manager-bureaubladtoepassing gebruiken {#use-aem-desktop-app-v2}

Met de Adobe Experience Manager (AEM)-bureaubladtoepassing hebt u eenvoudig toegang tot de Adobe Experience Manager DAM-middelen op uw lokale bureaublad en kunt u deze middelen gebruiken in alle bureaubladtoepassingen. U kunt de middelen in Desktoptoepassingen openen en de activa plaatselijk uitgeven - upload de veranderingen terug naar de Manager van de Ervaring met versiecontrole, om de updates met andere gebruikers te delen. U kunt ook nieuwe bestanden en maphiërarchieën uploaden naar Experience Manager, mappen maken en elementen of mappen verwijderen uit Experience Manager DAM.

Dankzij de integratie kunnen verschillende rollen in de organisatie de elementen centraal beheren in de middelen van Experience Manager en hebben ze toegang tot de middelen op het lokale bureaublad in de systeemeigen toepassingen op Windows of Mac OS.

Wanneer u de toepassing opent nadat u zich hebt afgemeld of voor het eerst, geeft u de URL van de server van Experience Manager op. Klik op Verbinding maken. Geef uw referenties op om de toepassing te verbinden met de server.

De belangrijkste taken die u uitvoert met de Experience Manager-bureaubladtoepassing zijn:

![Workflows en taken die u kunt uitvoeren met Experience Manager-bureaublad](assets/aem_desktop_app_usecases_v2.png "appWorkflows en taken die u kunt uitvoeren met de Adobe Experience Manager-bureaubladtoepassing")Download [dit](assets/aem_desktop_app_usecases_print.pdf) PDF-bestand dat klaar is voor afdrukken.

## Hoe desktop app werkt {#how-app-works2}

Voordat u de toepassing gaat gebruiken, moet u weten [hoe de app werkt](release-notes.md#how-app-works). Zorg ook dat u bekend bent met de volgende termen:

* **[!UICONTROL Desktop Actions]**: Vanuit de webinterface Middelen kunt u vanuit een browser de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw native desktoptoepassing. Deze acties zijn beschikbaar via de webinterface en gebruiken de functionaliteit van de bureaubladtoepassing. Zie [hoe u Desktophandelingen](using.md#desktopactions-v2)kunt inschakelen.

* Bestandsstatus is **[!UICONTROL Cloud Only]**: Dergelijke middelen worden niet op de lokale computer gedownload en zijn alleen beschikbaar op de server van Experience Manager.

* Bestandsstatus is **[!UICONTROL Available locally]**: De middelen worden gedownload en beschikbaar op de lokale computer zoals is. De elementen worden niet gewijzigd.

* Bestandsstatus is **[!UICONTROL Edited locally]**: Dergelijke elementen worden lokaal gewijzigd en de wijzigingen worden nog steeds geüpload naar de Experience Manager-server. Nadat u het uploadt, verandert de status in [!UICONTROL Available locally]. Zie Elementen [](using.md#edit-assets-upload-updated-assets)bewerken.

* Bestandsstatus is **[!UICONTROL Editing conflict]**: Als u en andere gebruikers tegelijkertijd een element wijzigen, geeft de app aan dat er een bewerkingsconflict is opgetreden. De app biedt ook opties om uw wijzigingen te behouden of te negeren. Zie [hoe u bewerkingsconflicten](using.md#adv-workflow-collaborate-avoid-conflicts)voorkomt.

* Bestandsstatus is **[!UICONTROL Modified remotely]**: De app geeft aan of een element dat u hebt gedownload, is gewijzigd op de Experience Manager-server. De app biedt ook de optie om de nieuwste versie te downloaden en uw lokale kopie bij te werken. Zie [hoe u bewerkingsconflicten](using.md#adv-workflow-collaborate-avoid-conflicts)voorkomt.

* **[!UICONTROL Check-out]**: Als u een bestand bewerkt of van plan bent een bestand te bewerken, schakelt u de status in of uit. Er wordt een vergrendelingspictogram toegevoegd aan het element in de app en de AEM-webinterface. Met het vergrendelingspictogram kunnen andere gebruikers voorkomen dat hetzelfde element tegelijk wordt bewerkt, omdat dit tot een bewerkingsconflict leidt.

* **[!UICONTROL Check-in]**: Markeer het element als veilig voor andere gebruikers om het te bewerken zonder een bewerkingsconflict te veroorzaken. Wanneer u uw wijzigingen uploadt, wordt het vergrendelingspictogram automatisch verwijderd. Als u de incheck-status inschakelt, wordt ook het vergrendelingspictogram verwijderd. U wordt echter aangeraden dit niet handmatig in te checken zonder de wijzigingen te uploaden. Als u de wijzigingen verwijdert, schakelt u het inchecken handmatig in of uit.

* **[!UICONTROL Open]** handeling: Open gewoon het element om er een voorvertoning van weer te geven in de oorspronkelijke toepassing. Het wordt afgeraden het element met deze handeling te bewerken, omdat het element niet wordt uitgecheckt en andere gebruikers bewerkingen kunnen uitvoeren die tot bewerkingsconflicten leiden.

* **[!UICONTROL Edit]** handeling: Gebruik de handeling om de afbeelding te wijzigen. Als u op [!UICONTROL Edit] Handeling klikt, wordt het element automatisch uitgecheckt en wordt een vergrendelingspictogram toegevoegd aan het element. Klik op Bewerken als u het element niet wilt bewerken en klik vervolgens op [!UICONTROL Toggle check-in]. Als u elementen in de AEM DAM-maphiërarchie wilt verwijderen, hernoemen of verplaatsen, gebruikt u de acties van de AEM-webinterface en niet de handeling Bewerken.

* **[!UICONTROL Download]** handeling: Download het middel naar uw lokale computer. U kunt de elementen nu downloaden en later bewerken. werk offline en upload de wijzigingen later. Elementen worden gedownload in een cachemap op uw bestandssysteem.

* **[!UICONTROL Reveal File]** of **[!UICONTROL Reveal Folder]** actie: Terwijl de elementen naar een lokale cachemap worden gedownload, bootst de toepassing een lokale netwerkschijf na en biedt deze een lokaal pad voor elk element. Als u dit pad wilt weten, gebruikt u de desbetreffende openingsoptie in de app. Actie tonen is vereist om middelen in de Creative Cloud-toepassing te plaatsen. Zie Elementen [plaatsen](using.md#place-assets-in-native-documents).

* **[!UICONTROL Open In Web]** handeling: Open het element in de webinterface van AEM om het element weer te geven. U kunt meer workflows starten vanuit de AEM-interface, zoals het bijwerken van metagegevens of het detecteren van elementen.

* **[!UICONTROL Delete]** handeling: Verwijder het element uit de AEM DAM-opslagplaats. Met de handeling wordt de oorspronkelijke kopie van het element op de AEM-server verwijderd. Zie Wijzigingen [](using.md#edit-assets-upload-updated-assets)negeren als u alleen wijzigingen in het lokale element wilt negeren.

* **[!UICONTROL Upload Changes]**: De bureaubladtoepassing uploadt het bijgewerkte element alleen wanneer u het expliciet uploadt naar de AEM-server. Wanneer u uw bewerkingen opslaat, worden de wijzigingen alleen op uw lokale computer opgeslagen. Tijdens het uploaden wordt het element automatisch ingecheckt en wordt het vergrendelingspictogram verwijderd. Zie Elementen [](using.md#edit-assets-upload-updated-assets)bewerken.

## Desktopacties inschakelen in AEM-webinterface {#desktopactions-v2}

Vanuit de gebruikersinterface Middelen in een browser kunt u de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw desktoptoepassing. Deze opties worden aangeroepen [!UICONTROL Desktop Actions] en zijn niet standaard ingeschakeld. Voer de volgende stappen uit om deze functie in te schakelen.

1. Klik/tik op het **[!UICONTROL User]** pictogram op de werkbalk in de middelenconsole.
1. Klik of tik op het pictogram **[!UICONTROL My Preferences]** om het **[!UICONTROL Preferences]** dialoogvenster weer te geven.
1. Selecteer in het dialoogvenster Gebruikersvoorkeuren **[!UICONTROL Show Desktop Actions For Assets]**. Klik of tik op **[!UICONTROL Accept]**.

   ![Schakel Bureaubladhandelingen weergeven voor elementen in om bureaubladhandelingen in te schakelen](assets/chlimage_1-3.png)

   Inschakelen [!UICONTROL Show Desktop Actions For Assets] van desktophandelingen

## Zoeken, zoeken en voorvertonen van elementen {#browse-search-preview-assets}

U kunt vanuit de bureaubladtoepassing naar de middelen in de AEM-opslagplaats bladeren, deze zoeken en er een voorvertoning van weergeven. Probeer het volgende in de app:

1. Blader naar een map en bekijk basisinformatie over de middelen die beschikbaar zijn in de map, samen met kleine miniaturen van alle elementen.

   ![Door de DAM-bestanden en -](assets/browse_folder_da2.png "mappen bladerenDoor de DAM-bestanden en -mappen bladeren")

1. Klik op de bestandsnaam als u meer informatie en een grotere miniatuur van een afzonderlijk element wilt bekijken.

   ![Een grotere voorvertoning van een element en](assets/large_preview_actions_da2.png "handelingen bekijkenEen grotere voorvertoning van een element en handelingen bekijken")

1. Klik **[!UICONTROL Open]** of **[!UICONTROL Edit]** om het bestand lokaal te downloaden en bekijk het of bewerk het bestand in de oorspronkelijke toepassing.
1. Zoek met behulp van trefwoorden naar verwante middelen in de AEM-opslagplaats. Gebruik `?` en `*` als jokertekens. Deze jokertekens vervangen een enkel teken of meerdere tekens. Filter de resultaten en sorteer deze zo nodig.

   ![Voorbeeld van zoeken met](assets/search_wildcard_da2.png "jokerteken voor sterretjeVoorbeeld met jokerteken voor sterretje")

   ![Een andere voorbeeldzoekopdracht met](assets/search_wildcard2_da2.png "jokerteken voor sterretjesEen andere voorbeeldzoekopdracht met andere plaatsing van jokerteken voor sterretjes")

>[!NOTE]
>
>In de app worden de elementen weergegeven door de zoekcriteria af te stemmen op meerdere metagegevensvelden en niet alleen op de titel van het element of de bestandsnaam.

## Elementen downloaden {#download-assets}

U kunt de elementen downloaden naar uw lokale bestandssysteem. De app haalt de middelen van de AEM-server op en slaat dezelfde kopie op uw lokale bestandssysteem op.

Klik op het pictogram ![](assets/do-not-localize/more2_da2.png) Meer opties voor opties en klik op het pictogram ![](assets/do-not-localize/download_cloud_da2.png) Downloaden om te downloaden.

![Downloadoptie voor een](assets/download_option_da2.png "assetDownload-optie voor een element")

>[!NOTE]
>
>Wanneer u een groot bestand of een groot aantal bestanden downloadt of uploadt, schakelt de toepassing de handelingen voor elementen en mappen uit. De acties zijn beschikbaar wanneer het downloaden of uploaden is voltooid.

Het downloaden van meerdere elementen kan leiden tot slechte prestaties als de wachtrij groot is of als u te maken krijgt met een netwerkprobleem. Het is ook onbekend dat u veel bestanden in de wachtrij plaatst om te downloaden wanneer u een map downloadt. Om lange wachttijden te vermijden, beperkt app het aantal elementen dat in één keer wordt gedownload. Zie Voorkeuren [](install-upgrade.md#set-preferences)instellen voor informatie over het configureren ervan. Zelfs onder deze limiet kan de app soms om bevestiging vragen voordat een ogenschijnlijk grote map wordt gedownload.

![App bevestigt download van relatief groot aantal](assets/download_confirmation_da2.png "middelenApp bevestigt download van relatief groot aantal middelen")

Als er mappen zijn geselecteerd en gedownload, downloadt de toepassing alleen elementen die rechtstreeks in de map(pen) in AEM zijn opgeslagen. Elementen worden niet automatisch uit submappen gedownload.

## Elementen op uw bureaublad openen {#openondesktop-v2}

U kunt de externe middelen openen voor weergave in de oorspronkelijke toepassing. De middelen worden gedownload aan een lokale omslag en gelanceerd in de inheemse toepassing verbonden aan het dossierformaat. U kunt de oorspronkelijke toepassing wijzigen en specifieke bestandstypen (extensies) openen in de Mac of Windows.

Klik **[!UICONTROL Open]** in het menu Middelen. Het element wordt lokaal gedownload en in de oorspronkelijke toepassing geopend. Controleer de voortgang van het downloaden en de overdrachtssnelheid van grote middelen op de statusbalk.
<!-- ![Download progress bar for large-sized assets](assets/download_status_bar_da2.png "Download progress bar for large-sized assets")

-->

>[!NOTE]
>
>Als de verwachte wijzigingen niet worden doorgevoerd in de app, klikt u op het pictogram ![](assets/do-not-localize/refresh.png) Vernieuwen of klikt u met de rechtermuisknop in de interface van de app en klikt u **[!UICONTROL Refresh]**. De acties zijn niet beschikbaar wanneer grotere downloads of uploads worden uitgevoerd.

Als u de lokale downloadmap van een element wilt openen, klikt u op het pictogram ![](assets/do-not-localize/more2_da2.png) Meer handelingen en klikt u op de ![actie Pictogram](assets/do-not-localize/reveal_action2_da2.png) onthullen **[!UICONTROL Reveal File]** .

## Elementen gebruiken of plaatsen in eigen documenten {#place-assets-in-native-documents}

In sommige gevallen, bijvoorbeeld wanneer het plaatsen van activa in een inheems document, hebt u toegang tot een dossier in de Ontdekkingsreiziger van Vensters of de Vinder van MAC. Als u de locatie van het bestandssysteem van het lokaal gedownloade bestand wilt herstellen, gebruikt u de optie ![Pictogram](assets/do-not-localize/reveal_action2_da2.png) onthullen **[!UICONTROL Reveal File]** .

![File-actie onthullen voor een](assets/revealfile_action_da2.png "assetReveal-actie voor een element")

Klik **[!UICONTROL Reveal File]** of **[!UICONTROL Reveal Folder]** op een map om Windows Verkenner of Mac Finder te openen met het bestand of de map die op uw lokale computer is geselecteerd. De optie is handig als u de AEM-bestanden bijvoorbeeld wilt plaatsen in de native toepassingen die het plaatsen of koppelen van lokale bestanden ondersteunen. Zie Afbeeldingen [plaatsen voor informatie over het plaatsen van bestanden in Adobe InDesign](https://helpx.adobe.com/indesign/using/placing-graphics.html).

De **[!UICONTROL Reveal File]** actie opent een lokaal netwerkaandeel, dat slechts de activa toont die plaatselijk - beschikbaar zijn - namelijk het toont activa die, geopend of geopend/uitgegeven gebruikend app werden onthuld. Het lokale netwerkaandeel uploadt geen veranderingen in AEM. Als u de wijzigingen wilt uploaden, gebruikt u expliciet **[!UICONTROL Upload Changes]** of **[!UICONTROL Upload]** actiepunten in de app.

>[!NOTE]
>
>Voor achterwaartse compatibiliteit met AEM desktop app v1.x worden de vrijgegeven bestanden via een lokaal netwerkaandeel gebruikt, waarbij alleen lokaal beschikbare bestanden beschikbaar worden gemaakt. De bureaubladpaden van de onthulde bestanden zijn gelijk aan de paden die door app v1.x worden gemaakt.

>[!CAUTION]
>
>Gebruik geen optie **[!UICONTROL Reveal File]** om elementen te bewerken in native toepassingen. Gebruik in plaats daarvan de **[!UICONTROL Edit]** handelingen. Zie [Geavanceerde workflow voor meer informatie: samen te werken aan dezelfde bestanden en bewerkingsconflicten](#adv-workflow-collaborate-avoid-conflicts)te voorkomen.

## Elementen bewerken en bijgewerkte elementen uploaden naar AEM {#edit-assets-upload-updated-assets}

Open elementen voor bewerking wanneer u wijzigingen wilt aanbrengen en de bijgewerkte elementen naar de AEM-server wilt uploaden. U voorkomt conflicten met bewerkingen door andere gebruikers door met de app een bewerkingssessie te starten. Voordat u begint met bewerken, moet u ervoor zorgen dat er geen vergrendelingspictogram op het element staat, dat wil zeggen dat een andere gebruiker het element niet bewerkt.

Als u een element wilt bewerken, zoekt u het element of bladert u naar de locatie van het element. Klik op ![Meer pictogram](assets/do-not-localize/more2_da2.png) en klik op **[!UICONTROL Edit]**.

Gebruik deze optie **[!UICONTROL Toggle Check-out]** om het element te vergrendelen om conflicten te voorkomen met bewerkingen van andere gebruikers in beide volgende situaties:

* U hebt een middel bewerkt zonder het eerst uit te checken (bijvoorbeeld door het alleen te openen).
* U bent van plan binnenkort met het bewerken van een element te beginnen en wilt niet dat anderen dit bewerken.

Nadat u de wijzigingen hebt aangebracht, geeft de app de **[!UICONTROL Edited Locally]** status voor de gewijzigde elementen weer. Alle wijzigingen die in de elementen zijn opgeslagen, zijn alleen lokaal totdat u de wijzigingen in AEM uploadt. Als u een individu of een paar elementen een voor een wilt uploaden, klikt u op **[!UICONTROL Upload Changes]** de opties voor een element. Er wordt een versie van het element gemaakt in AEM. Met behulp van de webinterface van AEM Assets kunt u de elementgeschiedenis in de [tijdlijnweergave](https://helpx.adobe.com/experience-manager/6-5/assets/using/activity-stream.html)zien.

![De optie Wijzigingen uploaden in de](assets/upload_changes_single1_da2.png "optie voor het uploaden van wijzigingen in de app")

![De optie Wijzigingen uploaden wanneer u een grote voorvertoning van een optie](assets/upload_changes_single2_da2.png "voor het uploaden van middelen weergeeft wanneer u een grote voorvertoning van een element weergeeft")

Zie [Geavanceerde workflow voor de beste werkwijzen voor gezamenlijke bewerking: samen te werken aan dezelfde bestanden en bewerkingsconflicten](#adv-workflow-collaborate-avoid-conflicts)te voorkomen.

In de volgende gevallen kunt u uw wijzigingen en bewerkingen in het lokale element negeren. Klik op **[!UICONTROL Discard Changes]**.

* Als u uw lokale wijzigingen niet in AEM wilt opslaan.
* Breng wijzigingen aan in het oorspronkelijke element nadat u enkele wijzigingen hebt opgeslagen.
* Bewerk het element niet meer omdat dit niet meer nodig is.

Schakel indien nodig het uitchecken in. Het bijgewerkte element wordt verwijderd uit de lokale cachemap en wordt opnieuw gedownload wanneer u het bewerkt of opent.

## Nieuwe elementen uploaden en toevoegen aan AEM {#upload-and-add-new-assets-to-aem}

Gebruikers kunnen nieuwe elementen toevoegen aan de DAM-opslagplaats. U kunt bijvoorbeeld fotograaf of contractant zijn die een groot aantal foto&#39;s van een fotoshoot aan de AEM-opslagplaats wil toevoegen. Als u nieuwe inhoud aan AEM wilt toevoegen, klikt u op het pictogram ![](assets/do-not-localize/upload_to_cloud_da2.png) Uploaden naar cloud in de bovenste balk van de app. Blader naar de elementbestanden in het lokale bestandssysteem en klik op **[!UICONTROL Select]**. De app begint het element te uploaden en geeft onderaan een voortgangsbalk weer als het uploaden van het element langer duurt. Gebruik geen spaties en ongeldige tekens bij het maken of uploaden van mappen. Zie een lijst met tekens in mappen [maken in AEM Assets](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html#Creatingfolders).

<!-- ![Download progress bar for large-sized assets](assets/upload_status_da2.png "Download progress bar for large-sized assets")
-->

U kunt mappen of afzonderlijke bestanden uploaden vanuit uw lokale bestandssysteem. De hiërarchie van een map blijft behouden wanneer deze wordt geüpload. Zie [Bulk uploaden](#bulk-upload-assets)voordat u elementen bulksgewijs uploadt.

Klik op **[!UICONTROL View]** > **[!UICONTROL Assets transfers]**. In de lijst kunt u de bestandsoverdrachten van de huidige sessie weergeven en snel verifiëren.

![Lijst van overgedragen elementen in een bepaalde](assets/assets_transfered_da2.png "sessionList van overgedragen elementen in een bepaalde sessie")

>[!NOTE]
>
>De overdrachtlijst is niet blijvend en is niet beschikbaar als u de app afsluit en opnieuw opent.

>[!NOTE]
>
>Als de bestanden niet kunnen worden geüpload en als u verbinding maakt met de implementatie van AEM 6.5.1 of hoger, raadpleegt u deze informatie over [probleemoplossing](troubleshoot.md#upload-fails).

## Werken met meerdere elementen {#work-with-multiple-assets}

Gebruikers kunnen eenvoudig met meerdere elementen werken en deze beheren door bijvoorbeeld alle bewerkingen in één keer te uploaden of geneste mappen met een paar klikken te uploaden.

### Door grote mappen bladeren {#browse-large-folders}

Als u werkt met mappen die veel elementen bevatten, schuift u om meer elementen weer te geven. Als u met het toetsenbord wilt schuiven, drukt u een paar keer op Tab om het element aan de bovenkant te selecteren. Let op het gemarkeerde element om te weten wanneer het is geselecteerd. Gebruik nu de toets Pijl-omlaag om door de lijst met elementen te gaan.

### Snelle handelingen voor geselecteerde elementen {#quick-actions-for-selected-assets}

Klik op de miniatuur van een paar elementen om de elementen te selecteren. Als u alle elementen wilt selecteren, klikt u op het selectievakje in de bovenste balk van de app. De set handelingen die van toepassing is op alle geselecteerde elementen samen worden weergegeven op een werkbalk onder aan de app.

![De werkbalk onder aan geeft acties weer die relevant zijn voor de geselecteerde](assets/actions_bottom_toolbar1_da2.png "elementen. De werkbalk onder aan het venster toont algemene acties voor de geselecteerde elementen")

![Geen acties op de werkbalk als er geen gemeenschappelijke acties voor de](assets/actions_bottom_toolbar2_da2.png "selectie zijnGeen acties op de werkbalk als er geen gemeenschappelijke acties voor de selectie zijn")

Welke acties beschikbaar zijn op de werkbalk onderaan, is afhankelijk van de status van de geselecteerde bestanden. Als u bijvoorbeeld alleen **[!UICONTROL Edited Locally]** bestanden selecteert, wordt het **[!UICONTROL Upload Changes]** pictogram weergegeven. Als u een combinatie van **[!UICONTROL Edited locally]** en **[!UICONTROL Cloud only]** selecteert, is de **[!UICONTROL Upload Changes]** actie niet beschikbaar.

### Alle bewerkte afbeeldingen zoeken {#find-all-edited-images}

De toepassing biedt een weergave met de naam **[!UICONTROL Edited locally]**, waarmee u snel toegang krijgt tot alle bestanden die u lokaal hebt gedownload (via [!UICONTROL Open] of [!UICONTROL Edit] handelingen) en die u vervolgens wijzigt. Met de app kunt u alle lokaal bewerkte elementen selecteren en de wijzigingen met een paar klikken uploaden. In deze weergave worden ook de lokaal bewerkte elementen weergegeven die een bewerkingsconflict hebben.

![Filter om alle lokaal bewerkte](assets/edited_locally_filter_da2.png "assetsFilter te bekijken om alle lokaal bewerkte middelen te zien, bijvoorbeeld voor het bulkuploaden van bewerkingen")

### Bulkupload-elementen {#bulk-upload-assets}

Gebruikers of organisaties, zoals fotografen of creatieve bureaus, kunnen in scenario&#39;s een groot aantal lokale elementen maken, zoals foto&#39;s, retoucheren of selectie uit een grotere set die buiten AEM wordt uitgevoerd. Ze kunnen deze grote lokale mappen rechtstreeks vanuit de bureaubladtoepassing uploaden naar AEM Assets. De maphiërarchieën blijven behouden en alle geneste submappen en opgenomen elementen worden geüpload. De geüploade elementen zijn direct ook beschikbaar voor andere gebruikers van dezelfde server. Elementen worden op de achtergrond geüpload, dus de bewerking is niet gekoppeld aan een webbrowsersessie.

![Met Bulk kunt u meerdere lokale mappen vanaf uw bureaublad uploaden naar](assets/upload_local_folders_da2.png "AEMBulk meerdere lokale mappen vanaf uw bureaublad uploaden naar AEM")

Als na het uploaden de verwachte wijzigingen niet in de app worden weergegeven, klikt u op het pictogram ![Vernieuwen](assets/do-not-localize/refresh.png).

>[!NOTE]
>
>Gebruik geen uploadfunctionaliteit om elementen over twee AEM-implementaties te migreren. Zie in plaats daarvan de [migratiegids](https://helpx.adobe.com/experience-manager/6-5/assets/using/assets-migration-guide.html).

### Lijst van overgedragen elementen {#list-of-transferred-assets}

Zie Elementen [uploaden naar AEM](#upload-and-add-new-assets-to-aem)voor een overzicht van de elementen die in een bepaalde sessie zijn overgedragen.

## Geavanceerde workflow: starten vanuit de AEM Assets-webinterface {#adv-workflow-start-from-aem-ui}

Start zo nodig uw workflow via de AEM Assets-webinterface. De bureaubladtoepassing integreert met de AEM om op verzoek over te nemen met behulp van desktophandelingen.

Een bijzonder geval van het beginnen van werkschema van de Webinterface is middelenontdekking. De gebruikersinterface van de Omnissearch bar in Assets biedt een rijke en geavanceerde zoekervaring. Wellicht wilt u eerst een gewenst middel op het web zoeken en vervolgens de workflow in de app starten, met [!UICONTROL Desktop Actions]behulp van. Enkele voorbeelden hiervan zijn het filteren van zoekresultaten met gebruik van facetten, het zoeken naar een specifiek middel waarvoor een licentie is verleend in Adobe Stock of een aanpassing die door uw organisatie is geïmplementeerd en waarmee u een betere detectie via de webinterface kunt uitvoeren.

De functionaliteit van de bureaubladtoepassing wordt gebruikt wanneer u de volgende handelingen uitvoert in de webinterface Middelen:

* Het [!UICONTROL Desktop Actions] systeem dat toestaat [!UICONTROL Open], [!UICONTROL Edit]en [!UICONTROL Reveal]
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] or [!UICONTROL check-in]

De acties in de webinterface die beschikbaar zijn voor een middel dat in de app is uitgecheckt, zijn [!UICONTROL Open], [!UICONTROL Reveal]en [!UICONTROL Check-in].

![Bureaubladhandelingen in de AEM-](assets/assets_web_actions_da2.png "webinterfaceDesktophandelingen in de AEM-webinterface")

>[!NOTE]
>
>Mogelijk wordt u door de browser gevraagd het starten van Adobe Experience Manager Desktop toe te staan. Als u wilt genieten van een ononderbroken overdracht van de browser naar de app, schakelt u het desbetreffende selectievakje in zodat de app altijd overneemt.

U kunt de volgende informatie of workflow niet vinden met de webinterface. Gebruik de bureaubladtoepassing omdat de webinterface lokale wijzigingen niet bijhoudt en zich niet bewust is van het volgende:

* Bestanden die lokaal zijn bewerkt.
* Bestanden met een bewerkingsconflict en een manier om dit op te lossen.
* Lokale wijzigingen uploaden naar AEM.
* Verschillende statussen van de lokaal beschikbare bestanden.

Integendeel, u kunt het element in de webinterface openen vanaf de bureaubladtoepassing met de **[!UICONTROL Open In Web]** handeling.

## Geavanceerde workflow: samenwerken aan dezelfde bestanden en bewerkingsconflicten voorkomen {#adv-workflow-collaborate-avoid-conflicts}

In samenwerkingsomgevingen kunnen meerdere gebruikers werken aan dezelfde set elementen die tot versieconflicten kunnen leiden. Volg de volgende aanbevolen procedures om conflicten te voorkomen:

* Bewerk geen elementen door op [!UICONTROL Open]te klikken. Bewerk de lokaal gedownloade elementen niet door deze te openen vanuit de bestandssysteemmap. Andere gebruikers weten niet dat het element wordt bewerkt.
* Als u een element wilt bewerken, klikt u altijd op [!UICONTROL Edit]. Het element wordt geopend in de oorspronkelijke toepassing en er wordt een vergrendelingspictogram toegevoegd aan het element, zodat de andere gebruikers weten dat het element wordt bewerkt.
* Klik [!UICONTROL Toggle Check-in] als u per ongeluk begint met bewerken zonder te klikken [!UICONTROL Edit]. Hiermee voegt u een vergrendelingspictogram toe aan het element. Zelfs als u een element later wilt bewerken, maar u wilt voorkomen dat anderen het bewerken, klikt u [!UICONTROL Toggle Check-in] om het element te vergrendelen.
* Voordat u een element bewerkt, moet u ervoor zorgen dat andere gebruikers het element niet bewerken. Zoek het slotpictogram op de activa.
* Na het voltooien van de bewerkingen uploadt u alle wijzigingen en checkt u het element in.

![Status van het bewerken van](assets/edits_conflicts_status_da2.png "conflictenStatus van het bewerken van conflicten")

Als een lokaal gedownload element wordt bijgewerkt op de AEM-server, geeft de app een **[!UICONTROL Modified remotely]** status weer. U kunt uw lokale kopie verwijderen of de lokale kopie vernieuwen door respectievelijk op [!UICONTROL Remove] of [!UICONTROL Update] te klikken. Via koppelingen in het dialoogvenster kunt u beide versies van het element weergeven.

![Opties om het conflict op te lossen wanneer het element op afstand wordt](assets/modified_remotely_dialog_da2.png "gewijzigdOpties om het conflict op te lossen wanneer het element op afstand wordt gewijzigd")

Als een middel dat u lokaal bewerkt ook zonder uw medeweten op de server wordt bijgewerkt, geeft de app een **[!UICONTROL Editing Conflict]** status weer. U kunt één set wijzigingen behouden. U kunt de updates behouden (klik op **[!UICONTROL Keep Mine]**) en de bewerking van de andere gebruiker verwijderen, of u kunt de updates van de andere gebruiker respecteren en uw (**[!UICONTROL Overwrite Mine]**) verwijderen.

![Opties voor het oplossen van een bewerkingsconflictOpties voor het oplossen van een bewerkingsconflict](assets/editing_conflict_dialog_da2.png "")

## Geavanceerde workflow: elementen in InDesign-bestanden plaatsen en koppelen {#adv-workflow-place-assets-indesign}

Wanneer u de AEM-bureaubladtoepassing gebruikt om bestanden met gekoppelde elementen te openen, worden de elementen vooraf gedownload en in de oorspronkelijke toepassingen geplaatst. Deze workflow werkt alleen als uw oorspronkelijke toepassing ondersteuning biedt voor het plaatsen van koppelingen naar lokale elementen en AEM moet het oplossen van deze koppelingen in binaire bestanden naar verwijzingen naar de server ondersteunen.

De AEM-bureaubladtoepassing ondersteunt deze workflow met een paar geselecteerde Adobe Creative Cloud-bureaubladtoepassingen en -bestandsindelingen - Adobe InDesign, Adobe Illustrator en Adobe Photoshop. Met de workflow kunt u efficiënt werken met de ondersteunde Creative Cloud-bestanden. Dus als gebruiker A een paar elementen in een InDesign-bestand plaatst en deze in AEM controleert, ziet gebruiker B de elementen in het InDesign-bestand, ook al maken de elementen geen deel uit van het bestand. De middelen worden plaatselijk gedownload op de machine van gebruiker B.

>[!NOTE]
>
>De bureaubladtoepassing kan worden toegewezen aan elk station in Windows. Wijzig de standaardstationsletter echter niet voor vloeiende bewerkingen. Als gebruikers van dezelfde organisatie verschillende stationsletters gebruiken, kunnen ze de elementen die door anderen zijn geplaatst, niet zien. De geplaatste elementen worden niet opgehaald wanneer het pad verandert. De geplaatste elementen blijven in het binaire bestand (bijvoorbeeld INDD) staan en worden niet verwijderd.

Als u de beperkingen van deze workflow wilt weten, raadpleegt u de [systeemvereisten en ondersteunde versies](release-notes.md#system-requirements-and-prerequisites-v2).

Voer de volgende stappen uit om deze workflow te testen met een afbeeldingselement en InDesign:

1. Houd een INDD-bestand met geplaatste elementen in AEM bij. Zie [Afbeeldingen](https://helpx.adobe.com/indesign/using/placing-graphics.html)plaatsen voor informatie over het maken van een dergelijk INDD-bestand.
1. Vanuit de bureaubladtoepassing **[!UICONTROL Edit]** het INDD-bestand met geplaatste elementen in AEM.
1. De app downloadt zowel het InDesign-bestand als de gekoppelde elementen. Wanneer InDesign het document opent, worden de koppelingen omgezet, worden de elementen gedownload en worden de elementen weergegeven in het InDesign-document.
1. Als u een nieuwe afbeelding in het InDesign-bestand wilt plaatsen, gebruikt u de **[!UICONTROL Reveal File]** handeling op het element. De actie downloadt plaatselijk activa en opent de lokale plaats van het netwerkaandeel in de Ontdekkingsreiziger van Vensters of de Vinder van MAC.
1. Plaats het onthulde element in het InDesign-document. Hiermee maakt u een koppeling in het document.
1. Nadat u de bewerkingen in het InDesign-document hebt voltooid, slaat u het bestand op en uploadt u het bestand naar AEM met de bureaubladtoepassing.

## Geavanceerde workflow: de elementen lokaal downloaden {#adv-workflow-download-assets-locally}

De app downloadt de middelen van de AEM-server in veel gevallen lokaal op uw bestandssysteem. De downloads verbruiken bandbreedte en schijfruimte. Als u de scenario&#39;s kent, kunt u de wachttijd tot de downloads zijn voltooid, optimaliseren.

U kunt de middelen downloaden vanuit de app op aanvraag. Zie [Elementen](#download-assets)downloaden.

Wanneer u de [!UICONTROL Open] handeling gebruikt om middelen te openen in een native desktoptoepassing, wordt het middel lokaal gedownload als dit nog niet lokaal beschikbaar is. Zie [Elementen](#openondesktop-v2)openen.

Wanneer u de locatie van een middel of een map vanuit de app weergeeft, wordt het middel of de map eerst lokaal gedownload en vervolgens op uw computer geopend in het gedeelde lokale netwerk. Zie [Elementen](#openondesktop-v2)openen.

Wanneer u de [!UICONTROL Edit] actie gebruikt om middelen in een inheemse Desktoptoepassing uit te geven, wordt het middel gedownload plaatselijk als niet reeds beschikbaar plaatselijk. Zie Elementen [bewerken en bijgewerkte elementen uploaden naar AEM](#edit-assets-upload-updated-assets).

Als de app is geïnstalleerd en u mag deze gebruiken, worden de acties voltooid wanneer u deze gebruikt [!UICONTROL Desktop Actions] vanuit de AEM-webinterface. De app downloadt het middel eerst en voltooit de actie.