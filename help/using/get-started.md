---
title: Aan de slag  [!DNL Experience Manager]  Desktop app
description: Leer hoe de  [!DNL Experience Manager]  Desktop app inhoudsverwezenlijking en het publiceren met gestroomlijnde werkschema's en productiviteitseigenschappen verbetert.
feature: Desktop App,Asset Management
exl-id: 6cf29b6a-74e6-4860-a25b-d3e91abbaa9d
source-git-commit: 2bf5ee7454846c288cc1c976d8f69c6bfed8eabf
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 0%

---

# Aan de slag met [!DNL Adobe Experience Manager] Desktop App {#getting-started-desktop-app}

Gebruik de bureaubladtoepassing van [!DNL Adobe Experience Manager] om toegang te krijgen tot digitale elementen die zijn opgeslagen in een [!DNL Adobe Experience Manager] DAM-opslagplaats op uw lokale bureaublad. U kunt deze middelen dan in om het even welke Desktoptoepassingen gebruiken. U kunt de elementen lokaal openen en bewerken in bureaubladtoepassingen. Nadat u wijzigingen hebt aangebracht, uploadt u deze weer naar [!DNL Experience Manager] met versiebeheer om updates met andere gebruikers te delen. U kunt ook nieuwe bestanden en maphiërarchieën uploaden naar [!DNL Experience Manager] , mappen maken en elementen of mappen verwijderen van [!DNL Experience Manager] DAM.

Dankzij deze integratie kunnen verschillende rollen in de organisatie de elementen centraal beheren in [!DNL Experience Manager Assets] en toegang krijgen tot de elementen op het lokale bureaublad in de native toepassingen van Windows of macOS.

Wanneer u de toepassing opent na het afmelden of voor het eerst, geeft u de URL van de [!DNL Experience Manager] -server op in de notatie `https://[aem-server-url]:[port]/` . Selecteer vervolgens de optie [!UICONTROL Connect] . Geef referenties op om de toepassing te verbinden met de server.

>[!VIDEO](https://video.tv.adobe.com/v/28868?quality=12&learn=on){transcript=true}

De belangrijkste taken die u uitvoert met de bureaubladtoepassing van [!DNL Adobe Experience Manager] zijn:

![&#x200B; Werkschema&#39;s en taken u kunt verwezenlijken gebruikend [!DNL Experience Manager] Desktop app &#x200B;](assets/aem_desktop_app_usecases_v2.png)

## Hoe desktop app werkt {#how-app-works2}

Alvorens u begint de toepassing te gebruiken, begrijp [&#x200B; hoe app &#x200B;](release-notes.md#how-app-works) werkt. Zorg ook dat u bekend bent met de volgende termen:

* **[!UICONTROL Desktop Actions]**: Vanuit de Assets-webinterface kunt u vanuit een browser de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw native desktoptoepassing. Deze acties zijn beschikbaar via de webinterface en maken gebruik van de functionaliteit van de bureaubladtoepassing.

* Bestandsstatus is **[!UICONTROL Cloud Only]**: dergelijke elementen worden niet gedownload op de lokale computer en zijn alleen beschikbaar op de [!DNL Experience Manager] -server.

* Bestandsstatus is **[!UICONTROL Available locally]**: de elementen worden gedownload en zijn ongewijzigd beschikbaar op de lokale computer. De elementen worden niet gewijzigd.

* Bestandsstatus is **[!UICONTROL Edited locally]**: Dergelijke elementen worden lokaal gewijzigd en de wijzigingen blijven naar de [!DNL Experience Manager] -server geüpload. Nadat u het uploadt, verandert de status in [!UICONTROL Available locally]. Zie [&#x200B; activa &#x200B;](upload-assets.md#edit-assets-upload-updated-assets) uitgeven.

* Bestandsstatus is **[!UICONTROL Editing conflict]**: als u en anderen tegelijkertijd een element bewerken, geeft de app aan dat er een bewerkingsconflict is opgetreden. De app biedt ook opties om uw wijzigingen te behouden of te negeren. Zie [&#x200B; hoe te om het uitgeven conflicten &#x200B;](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts) te vermijden.

* Bestandsstatus is **[!UICONTROL Modified remotely]**: de app geeft aan of een element dat u hebt gedownload, is gewijzigd op de [!DNL Experience Manager] -server. De app biedt ook de optie om de nieuwste versie te downloaden en uw lokale kopie bij te werken. Zie [&#x200B; hoe te om het uitgeven conflicten &#x200B;](assets-management-tasks.md#adv-workflow-collaborate-avoid-conflicts) te vermijden.

* **[!UICONTROL Check-out]**: als u een bestand bewerkt of van plan bent een bestand te bewerken, schakelt u de status in en uit. Er wordt een vergrendelingspictogram toegevoegd aan het element in de app en de [!DNL Experience Manager] webinterface. Met het vergrendelingspictogram kunnen andere gebruikers voorkomen dat hetzelfde element tegelijk wordt bewerkt, omdat dit tot een bewerkingsconflict leidt.

* **[!UICONTROL Check-in]**: Markeer het element als veilig voor andere gebruikers om het te bewerken zonder een bewerkingsconflict te veroorzaken. Wanneer u uw wijzigingen uploadt, wordt het vergrendelingspictogram automatisch verwijderd. Als u de incheckstatus inschakelt, wordt ook het vergrendelingspictogram verwijderd. Adobe raadt u echter aan niet handmatig in te checken zonder de wijzigingen te uploaden. Als u de wijzigingen verwijdert, schakelt u het inchecken handmatig in of uit.

* **[!UICONTROL Open]** Handeling: open het element om er een voorvertoning van te bekijken in de oorspronkelijke toepassing. Adobe raadt u aan het middel niet te bewerken door deze handeling te gebruiken. De reden is dat het actief niet wordt uitgecheckt. Ondertussen kunnen andere gebruikers bewerkingen uitvoeren die tot bewerkingsconflicten leiden.

* **[!UICONTROL Edit]** actie: gebruik de actie om de afbeelding te wijzigen. Als u op [!UICONTROL Edit] klikt, wordt het element uitgecheckt en wordt een vergrendelingspictogram toegevoegd aan het element. Klik op Bewerken als u het element niet wilt bewerken en klik vervolgens op [!UICONTROL Toggle check-in] . Als u elementen in de DAM-maphiërarchie van [!DNL Experience Manager] wilt verwijderen, hernoemen of verplaatsen, gebruikt u de [!DNL Experience Manager] webinterfacehandelingen en niet de bewerkingshandeling.

* **[!UICONTROL Download]** Handeling: Download het element naar uw lokale computer. U kunt de elementen nu downloaden en later bewerken. Werk offline en upload de wijzigingen later. Assets wordt gedownload in een cachemap op uw bestandssysteem.

* **[!UICONTROL Reveal File]** of **[!UICONTROL Reveal Folder]** actie: terwijl de elementen naar een lokale cachemap worden gedownload, navigeert de toepassing een lokale netwerkschijf. Het biedt een lokaal pad voor elk element. Als u dit pad wilt weten, gebruikt u de desbetreffende openingsoptie in de app. Actie tonen is vereist om elementen in de Creative Cloud-toepassing te plaatsen. Zie [&#x200B; plaatselementen &#x200B;](search.md#place-assets-in-native-documents).

* **[!UICONTROL Open In Web]** action: Open het element in de webinterface van [!DNL Experience Manager] om het element weer te geven. U kunt vanuit de interface van [!DNL Experience Manager] meer workflows starten, zoals het bijwerken van metagegevens of het detecteren van elementen.

* **[!UICONTROL Delete]** actie: verwijder het element uit de [!DNL Experience Manager] DAM-opslagplaats. Met de handeling wordt de oorspronkelijke kopie van het element op de Experience Manager-server verwijderd. Als u slechts wijzigingen in het lokale activa wilt verwerpen, zie [&#x200B; veranderingen &#x200B;](upload-assets.md#edit-assets-upload-updated-assets) verwerpen.

* **[!UICONTROL Upload Changes]**: De bureaubladtoepassing uploadt het bijgewerkte element alleen wanneer u het expliciet uploadt naar de [!DNL Experience Manager] -server. Wanneer u uw bewerkingen opslaat, worden de wijzigingen alleen op uw lokale computer opgeslagen. Wanneer u het element uploadt, wordt het automatisch ingecheckt en wordt het vergrendelingspictogram verwijderd. Zie [&#x200B; activa &#x200B;](upload-assets.md#edit-assets-upload-updated-assets) uitgeven.

## Bureaubladhandelingen inschakelen in de webinterface van [!DNL Experience Manager] {#desktopactions-v2}

Vanuit de gebruikersinterface van [!DNL Assets] in een browser kunt u de middelenlocaties of uitchecken verkennen en het middel openen voor bewerking in uw desktoptoepassing. Deze opties worden [!UICONTROL Desktop Actions] genoemd en zijn niet standaard ingeschakeld. Voer de volgende stappen uit om deze functie in te schakelen.

1. Klik in de [!DNL Assets] -console op het pictogram **[!UICONTROL User]** op de werkbalk.
1. Klik op **[!UICONTROL My Preferences]** om het dialoogvenster **[!UICONTROL Preferences]** weer te geven.

1. Selecteer [!UICONTROL User Preferences] in het dialoogvenster **[!UICONTROL Show Desktop Actions For Assets]** en klik vervolgens op **[!UICONTROL Accept]** .

   ![&#x200B; Uitgezochte tonen de Acties van de Desktop voor Assets om Desktopacties toe te laten &#x200B;](assets/enable_desktop_actions1.png)

## Starten via de [!DNL Assets] webinterface {#adv-workflow-start-from-aem-ui}

Start zo nodig uw workflow via de Assets-webinterface. De desktop-app integreert met de [!DNL Experience Manager] die op verzoek kan worden overgenomen met behulp van desktophandelingen.

Een speciaal geval van het beginnen van een werkschema van de interface van het Web is activaontdekking. De bar van het Onderzoek in het gebruikersinterface van Assets biedt een rijke en geavanceerde onderzoekservaring aan. U kunt desgewenst eerst een gewenst middel op het web zoeken en vervolgens de workflow in de app starten met [!UICONTROL Desktop Actions] . Sommige voorbeeldgevallen omvatten het filtreren onderzoeksresultaten gebruikend facetten, het vinden van een specifiek middel in licentie gegeven van Adobe Stock, of een aanpassing die door uw organisatie wordt uitgevoerd die u betere ontdekking van de interface van het Web toestaat.

De functionaliteit van de Desktop-app wordt gebruikt wanneer u de volgende handelingen probeert uit te voeren in de Assets Web-interface:

* De [!UICONTROL Desktop Actions] die [!UICONTROL Open] , [!UICONTROL Edit] en [!UICONTROL Reveal] toestaan
* [!UICONTROL Upload folder]
* [!UICONTROL Check-out] of [!UICONTROL check-in]

De acties in de webinterface die beschikbaar zijn voor een element dat is uitgecheckt in de app, zijn bijvoorbeeld [!UICONTROL Open], [!UICONTROL Reveal] en [!UICONTROL Check in] .

![&#x200B; Acties van de Desktop in de [!DNL Experience Manager] interface van het Web &#x200B;](assets/assets_web_actions_da2.png " Acties van de Desktop in de interface van het Web van Experience Manager ")

>[!NOTE]
>
>Mogelijk wordt u door de browser gevraagd het starten van [!DNL Adobe Experience Manager] Desktop toe te staan. Als u elke keer een ononderbroken overdracht van de browser naar de app wilt uitvoeren, schakelt u het desbetreffende selectievakje in zodat de app de toepassing kan overnemen.

U kunt niet de volgende informatie of het werkschema vinden gebruikend de interface van het Web. Gebruik de bureaubladtoepassing omdat de webinterface lokale wijzigingen niet bijhoudt en zich niet bewust is van het volgende:

* Bestanden worden lokaal bewerkt.
* Bestanden met een bewerkingsconflict en een manier om dit op te lossen.
* Lokale wijzigingen uploaden naar [!DNL Experience Manager] .
* Verschillende statussen van de lokaal beschikbare bestanden.

Integendeel, u kunt het element met de handeling **[!UICONTROL Open In Web]** openen in de webinterface vanaf de bureaubladtoepassing.

## Volgende stappen {#next-steps}

* [&#x200B; bekijk een video om met App van de Desktop van Adobe Experience Manager &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app) te beginnen te worden

* Verstrek documentatie terugkoppelt gebruikend [!UICONTROL Edit this page] ![&#x200B; uitgeeft de pagina &#x200B;](assets/do-not-localize/edit-page.png) of [!UICONTROL Log an issue] ![&#x200B; creeer een kwestie GitHub &#x200B;](assets/do-not-localize/github-issue.png) beschikbaar op juiste sidebar

* De Zorg van de Klant van het contact [&#128279;](https://experienceleague.adobe.com/nl?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [&#x200B; Begrijp het gebruikersinterface &#x200B;](/help/using/user-interface.md)
>* [&#x200B; de nota&#39;s van de Versie en bekende kwesties &#x200B;](/help/using/release-notes.md)
>* [&#x200B; installeer of bevordert Desktop App &#x200B;](/help/using/install-upgrade.md)
