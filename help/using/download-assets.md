---
title: De activa van de download gebruikend  [!DNL Experience Manager]  Desktop app
description: De activa van de download gebruikend  [!DNL Adobe Experience Manager]  Desktop app.
feature: Desktop App,Asset Management
source-git-commit: 2947fbd3bfeb15b37a8f1b0118e969b5d70499d0
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---


# Elementen lokaal downloaden {#download-assets-locally}

De toepassing downloadt vaak elementen van de [!DNL Experience Manager] -server naar uw lokale bestandssysteem. De downloads verbruiken bandbreedte en schijfruimte. Als u de scenario&#39;s kent, kunt u de wachttijd tot de downloads zijn voltooid, optimaliseren. U kunt de elementen downloaden naar uw lokale bestandssysteem. De toepassing haalt de elementen op van de [!DNL Experience Manager] -server en slaat dezelfde kopie op uw lokale bestandssysteem op.

Klik **[!UICONTROL More actions]** ![ Meer optiepictogram ](assets/do-not-localize/more2_da2.png) voor opties en klik ![ pictogram van de Download ](assets/do-not-localize/download_cloud_da2.png) om te downloaden.

![ optie van de Download voor een activa ](assets/download_option_da2.png " optie van de Download voor een activa ")

>[!NOTE]
>
>Wanneer u een groot bestand of een groot aantal bestanden downloadt of uploadt, schakelt de toepassing de handelingen voor elementen en mappen uit. De acties zijn beschikbaar wanneer het downloaden of uploaden is voltooid.

Wanneer u de handeling [!UICONTROL Open] gebruikt om middelen te openen in een native bureaubladtoepassing, wordt het element lokaal gedownload als dit nog niet lokaal beschikbaar is. Zie [ Open activa ](#openondesktop-v2).

Wanneer u de locatie van een middel of een map vanuit de app weergeeft, wordt het middel of de map eerst lokaal gedownload en vervolgens op uw computer geopend in het gedeelde lokale netwerk. Zie [ Open activa ](#openondesktop-v2).

Wanneer u de handeling [!UICONTROL Edit] gebruikt om middelen in een native desktoptoepassing te bewerken, wordt het element lokaal gedownload als dit nog niet lokaal beschikbaar is. Zie [ activa uitgeven en bijgewerkte activa aan  [!DNL Experience Manager]](#edit-assets-upload-updated-assets) uploaden.

Als de app is geïnstalleerd en hierop is toegestaan, worden de acties voltooid wanneer u [!UICONTROL Desktop Actions] vanuit de webinterface van [!DNL Experience Manager] gebruikt. De app downloadt het middel eerst en voltooit de actie.

## Meerdere middelen downloaden {#download-multiple-assets}

Het downloaden van meerdere elementen kan leiden tot slechte prestaties als de wachtrij groot is of als u te maken krijgt met een netwerkprobleem. Bovendien kunt u bij het downloaden van een map onbewust veel bestanden in de wachtrij plaatsen. Om lange wachttijden te vermijden, beperkt app het aantal elementen dat in één keer wordt gedownload. Om te weten hoe te om het te vormen, zie [ Vastgestelde voorkeur ](install-upgrade.md#set-preferences). Zelfs onder deze limiet kan de app soms om bevestiging vragen voordat een ogenschijnlijk grote map wordt gedownload.

![ App bevestigt download van vrij groot aantal activa ](assets/download_confirmation_da2.png " App bevestigt download van vrij groot aantal activa ")

Als mappen zijn geselecteerd en gedownload, downloadt de toepassing alleen elementen die rechtstreeks in de mappen in [!DNL Experience Manager] zijn opgeslagen. Elementen worden niet automatisch uit submappen gedownload.

## Volgende stappen {#next-steps}

* [ bekijk een video om met App van de Desktop van Adobe Experience Manager ](https://experienceleague.adobe.com/nl/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app) te beginnen te worden

* Verstrek documentatie terugkoppelt gebruikend [!UICONTROL Edit this page] ![ uitgeeft de pagina ](assets/do-not-localize/edit-page.png) of [!UICONTROL Log an issue] ![ creeer een kwestie GitHub ](assets/do-not-localize/github-issue.png) beschikbaar op juiste sidebar

* De Zorg van de Klant van het contact [&#128279;](https://experienceleague.adobe.com/nl?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [ uploadt activa ](/help/using/upload-assets.md)
>* [ Begrijp het gebruikersinterface ](/help/using/user-interface.md)
>* [Zoeken](/help/using/search.md)

