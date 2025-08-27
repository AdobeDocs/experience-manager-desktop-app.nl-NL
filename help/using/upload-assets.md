---
title: Upload activa gebruikend  [!DNL Experience Manager]  Desktop app
description: Upload activa gebruikend  [!DNL Adobe Experience Manager]  Desktop app.
feature: Desktop App,Asset Management
exl-id: f082c712-dc04-4bed-bac8-fa78f93de1c7
source-git-commit: db592420ded4d2f7288982a1ea17618484c82537
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# Elementen uploaden {#upload-assets}

Gebruikers van AEM Desktop App die rechten hebben om elementen toe te voegen, kunnen elementen toevoegen (zoals afbeeldingen, documenten, video&#39;s of andere media).

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

## Bulkupload-elementen {#bulk-upload-assets}

Gebruikers of organisaties, zoals fotografen of creatieve bureaus, kunnen een groot aantal lokale elementen maken tijdens activiteiten zoals foto&#39;s, retoucheren of het selecteren van een grotere set. Deze taken worden vaak uitgevoerd buiten [!DNL Experience Manager] . Ze kunnen deze grote lokale mappen rechtstreeks vanuit de bureaubladtoepassing uploaden naar [!DNL Assets] . De maphiërarchieën blijven behouden en alle geneste submappen en opgenomen elementen worden geüpload. De geüploade elementen zijn direct ook beschikbaar voor andere gebruikers van dezelfde server. Assets worden op de achtergrond geüpload, zodat de bewerking niet aan een webbrowsersessie is gekoppeld.

![ Bulk uploadt veelvoudige lokale omslagen van uw Desktop in [!DNL Experience Manager]](assets/upload_local_folders_da2.png " Bulk uploadt veelvoudige lokale omslagen van uw Desktop in Experience Manager ")

Na het uploaden, als de verwachte veranderingen niet in app worden weerspiegeld, klik verfrissen pictogram ![ pictogram ](assets/do-not-localize/refresh.png) verfrissen.

>[!NOTE]
>
>Gebruik geen uploadfunctionaliteit om elementen over twee [!DNL Experience Manager] -implementaties te migreren. In plaats daarvan, zie de [ migratiegids ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-migration-guide).

## Volgende stappen {#next-steps}

* [ bekijk een video om met App van de Desktop van Adobe Experience Manager ](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app) te beginnen te worden

* Verstrek documentatie terugkoppelt gebruikend [!UICONTROL Edit this page] ![ uitgeeft de pagina ](assets/do-not-localize/edit-page.png) of [!UICONTROL Log an issue] ![ creeer een kwestie GitHub ](assets/do-not-localize/github-issue.png) beschikbaar op juiste sidebar

* De Zorg van de Klant van het contact [&#128279;](https://experienceleague.adobe.com/?support-solution=General#support)

>[!MORELIKETHIS]
>
>* [ de activa van de Download ](/help/using/download-assets.md)
>* [ Begrijp het gebruikersinterface ](/help/using/user-interface.md)
>* [Zoeken](/help/using/search.md)
