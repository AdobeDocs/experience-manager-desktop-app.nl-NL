---
title: '[!DNL Adobe Experience Manager] Opmerkingen bij de release van de bureaubladtoepassing'
description: De details, de verhogingen van de versie, nieuwe eigenschappen, verenigbaarheid, en downloadverbindingen voor  [!DNL Adobe Experience Manager]  Desktop app.
mini-toc-levels: 1
feature: Desktop App,Release Information
exl-id: e058e7a2-fcc8-4ad1-899e-20695db6bc72
source-git-commit: b5dace65444ca15d09ec8648deb4c262415f40cf
workflow-type: tm+mt
source-wordcount: '2195'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager] Opmerkingen bij de release van de bureaubladtoepassing {#release-notes-v2}

Hieronder vindt u de releasegegevens voor de nieuwste bureaubladversie 2.3.3. De releasedatum is 16 mei 2025.

De meest recente versie van de bureaubladtoepassing bevat de volgende opgeloste problemen en verbeteringen:

* U kunt nieuw gemaakte elementen van uw lokale computer uploaden naar AEM, waar de centrale opslagplaats is opgeslagen, en deze weergeven in uw Desktop App.
* De functie Automatisch vernieuwen werkt de inhoud automatisch in real-time bij. Zo weet u zeker dat u altijd de meest recente informatie ziet zonder de pagina handmatig opnieuw te laden en de lijst met bijgewerkte elementen op te halen.
* Met de functie voor het vastzetten of vrijmaken van mappen kunt u belangrijke mappen gemakkelijk toegankelijk houden door ze vast te zetten of de weergave te decluteren door ze te verwijderen wanneer ze niet meer nodig zijn.
* Met de functie Naam van element wijzigen kunt u de titel van element eenvoudig bijwerken of wijzigen, zodat u namen nauwkeurig kunt houden en kunt ordenen terwijl de inhoud evolueert.
* U kunt het oorspronkelijke bestand behouden en wijzigingen aanbrengen in een vergelijkbaar bestand door bestanden te dupliceren op lokale en cloudlocaties met behulp van de bewerking voor gedupliceerde bestanden.
* Met de functie voor in- en uitchecken kunt u de bestandstoegang beheren door een bestand te vergrendelen dat u wilt bewerken (uitchecken) en uw wijzigingen op te slaan, terwijl het bestand ook beschikbaar wordt gemaakt voor anderen (inchecken).
* U kunt verzamelingen weergeven, downloaden en doorbladeren.
* U kunt metagegevens toewijzen wanneer u een nieuwe map maakt.

De **gesteunde [!DNL Experience Manager] versies** zijn:

* [!DNL Experience Manager] als een [!DNL Cloud Service] . Zie [ versienota&#39;s ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/home).
* [!DNL Experience Manager] 6.5.0 of hoger, op Adobe Managed Services (AMS) of op locatie. Zie {de versiedetails van het 0} de dienstpak [&#128279;](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/release-notes/release-notes).

[!DNL Adobe Experience Manager] Desktop app is beschikbaar voor de volgende **werkende systemen**:

* macOS X 10.14 of hoger, met de meest recente opgeloste problemen.
* Windows 10 met de recentste de dienstpakken en insectenmoeilijke situaties.

Er zijn twee versies van het Windows-installatieprogramma beschikbaar voor AEM Desktop App versie 2.3.1 en latere versies. Het basisinstallatieprogramma installeert de AEM Desktop App onder de lokale map App Data van de gebruiker. Adobe raadt dit installatieproces aan voor de meeste gebruikers. Er is ook een installatieprogramma voor Enterprise Windows beschikbaar waarmee de AEM Desktop App wordt geïnstalleerd in de map met gedeelde programmabestanden. Deze twee installatieprogramma&#39;s installeren dezelfde versie van de AEM Desktop App, zonder functieverschillen.

De **download URLs** voor gesteund OS zijn:

| Besturingssysteem | [!DNL Experience Manager] als een [!DNL Cloud Service] | [!DNL Experience Manager] 6.x |
|---|---|---|
| macOS (v2.3.3) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.3.3.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.3.3.dmg) |
| macOS Apple Silicon (M1) (v2.3.3) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.3.3.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.3.3.dmg) |
| Windows 64-bits (v2.3.3) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.3.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.3.exe) |
| Windows 64-bits Enterprise (v2.3.3) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.3.msi) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.3.msi) |
| macOS (v2.3.1) | [ Verbinding van de Download ](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081954149%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=mwSX5ilZL0he2raIx8t5ecQ%2FWuizky4MpcCXX3mEN38%3D&amp;reserved=0) | [ Verbinding van de Download ](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-x64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081981239%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=LJH3OCFq7yRykN4wU8HN9%2FBXC%2BjfXLJH4QizeFZfRHE%3D&amp;reserved=0) |
| macOS Apple Silicon (M1) (v2.3.1) | [ Verbinding van de Download ](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081965822%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=2YENn0tDduiucogClt6aBZHDOE6dbzBdigq8VQawIO0%3D&amp;reserved=0) | [ Verbinding van de Download ](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-osx-arm64-2.3.1.dmg&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081986151%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=jCepldg4dMej0%2BrK2mUonXwqsWL8ksE8%2BLMSgsH9qTA%3D&amp;reserved=0) |
| Windows 64-bits (v2.3.1) | [ Verbinding van de Download ](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081970892%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=sRn2UWW%2Bi7SMEvSO74ZGGvJ40vHh1KhLc7zAfKc37Es%3D&amp;reserved=0) | [ Verbinding van de Download ](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.exe&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081991004%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=aQWZtEK%2F3cWX8n8Au%2FwZ5Zd9xPVo5phvk%2FuF%2Be0HRrE%3D&amp;reserved=0) |
| Windows 64-bits Enterprise (v2.3.1) | [ Verbinding van de Download ](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faemcloud.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faemcloud%2Fpublic%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081976350%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=v9C0sLDSkuL%2FMIyae2WkbitJPVgSlAw2BqcaH5Im0uw%3D&amp;reserved=0) | [ Verbinding van de Download ](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fexperience.adobe.com%2F%23%2Fdownloads%2Fcontent%2Fsoftware-distribution%2Fen%2Faem.html%3Fpackage%3D%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Fadobe%2Faem-desktop-app%2Faem-desktop-win-x64-2.3.1.msi&amp;data=05%7C02%7Canujm%40adobe.com%7Cfcf599743bd649c5cd7308dcab9ea5cd%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C638573945081995827%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C0%7C%7C%7C&amp;sdata=2btCh0aIrUBiyeG37K9YorvzTeIJOggbq%2FRauUMn4LY%3D&amp;reserved=0) |
| macOS (v2.3.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.3.0.dmg) |
| macOS Apple Silicon (M1) (v2.3.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.3.0.dmg) |
| Windows 64-bits (v2.3.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.3.0.exe) |
| macOS (v2.2.2) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.2.dmg) |
| macOS Apple Silicon (M1) (v2.2.2) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.2.dmg) |
| Windows 64-bits (v2.2.2) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.2.exe) |
| macOS (v2.2.1) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.1.dmg) |
| macOS Apple Silicon (M1) (v2.2.1) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.1.dmg) |
| Windows 64-bits (v2.2.1) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.1.exe) |
| macOS (v2.2.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-x64-2.2.0.dmg) |
| macOS Apple Silicon (M1) (v2.2.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-arm64-2.2.0.dmg) |
| Windows 64-bits (v2.2.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win-x64-2.2.0.exe) |
| macOS (v2.1.5.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.5.0.dmg) |
| Windows 64-bits (v2.1.5.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.5.0.exe) |
| Windows 32-bits (v2.1.5.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.5.0.exe) |
| macOS (v2.1.4.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.4.0.dmg) |
| Windows 64-bits (v2.1.4.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.4.0.exe) |
| Windows 32-bits (v2.1.4.0) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.4.0.exe) |
| macOS (v2.1.3.4) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-osx-2.1.3.4.dmg) |
| Windows 64-bits (v2.1.3.4) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win64-2.1.3.4.exe) |
| Windows 32-bits (v2.1.3.1) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) | [ Verbinding van de Download ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/adobe/aem-desktop-app/aem-desktop-win32-2.1.3.1.exe) |

## Ondersteuning voor verschillende elementen en bestandstypen {#support-for-file-types}

De toepassing ondersteunt elementen die zijn opgeslagen in [!DNL Experience Manager] en die binair bestand vertegenwoordigen voor basisbewerkingen. Het openen van bestanden in de oorspronkelijke bureaubladtoepassing is afhankelijk van de koppeling van het besturingssysteem van de specifieke bestandstypen, zoals PNG of JPG, aan specifieke toepassingen, zoals Mac Preview of Adobe Photoshop.

Enkele bestandstypen ondersteunen het plaatsen van gekoppelde elementen in het binaire bestand. De toepassing downloadt de gekoppelde elementen vooraf als het element aanwezig is in de [!DNL Experience Manager] -opslagplaats wanneer dergelijke binaire bestanden worden geopend met de bureaubladtoepassing. Momenteel worden de volgende bestandstypen ondersteund:

* [!DNL Adobe InDesign] bestanden (INDD-indeling)
* [!DNL Adobe Illustrator] bestanden (AI-indeling)
* [!DNL Adobe Photoshop] bestanden (PS-indeling)

De functie wordt ondersteund in [!DNL Adobe Creative Cloud] 2018- en [!DNL Adobe Creative Cloud] 2019-versies van de bovenstaande toepassing. De app gebruikt een heuristische, best-match benadering om de lokale bureaubladpaden van gekoppelde elementen toe te wijzen aan URL&#39;s op de [!DNL Experience Manager] -server. Het steunt op een paar veronderstellingen:

* Paden naar geplaatste bestanden in de oorspronkelijke toepassing gebruiken een algemeen desktoppad (geplaatst vanuit het gedeelde lokale netwerk dat met de optie [!UICONTROL Reveal] wordt weergegeven).

* Paden worden door de native app opgeslagen in de XMP-record van het bestand.

* [!DNL Experience Manager] heeft de XMP-record geëxtraheerd met de paden naar de metagegevensrecord van het element.

* De paden kunnen worden aangepast aan elementen in [!DNL Experience Manager] , dat wil zeggen dat de geplaatste bestanden zich ook in [!DNL Experience Manager] onder een overeenkomend pad bevinden.

## Nieuwe functies, verbeteringen en foutoplossingen {#what-is-new}

Om de details te kennen, zie [ wat in v2.0 ](introduction.md#whats-new-v2) nieuw is.

**Updates in app v2.3.1**

* Het nieuwe installatieprogramma voor Windows van Enterprise installeert de toepassing onder Program Files.
* Steun voor **BasisAuthentificatie** tijdens de logins van AEM en van SSO.
* Configureerbaar aantal elementen toegestaan tijdens uploadbewerking

**Updates in app v2.3.0**

* Extra ondersteuning voor IMS-aanmelding. Dankzij de IMS-integratie kan de bureaubladtoepassing de toegangstoken automatisch vernieuwen, zodat de gebruiker zich maximaal 14 dagen kan aanmelden.

* Verbeterde ondersteuning voor zakelijke proxy&#39;s en webfilters.

**Updates in app v2.2.2**

* (Alleen Windows) Nadat de releaseversies 2.2.0 en 2.2.1 zijn geïnstalleerd, wordt een leeg scherm weergegeven in de bureaubladtoepassing.

**Updates in app v2.2.1**

* De bureaubladtoepassing geeft een foutbericht over een sessietime-out weer wanneer u op **[!UICONTROL Sign In]** klikt.

* Problemen tijdens het openen van de bureaubladtoepassing v2.2.0 op macOS.

* De bureaubladtoepassing geeft een foutbericht weer wanneer u elementen sorteert door op **[!UICONTROL Edited Locally]** te klikken.

**Updates in app v2.2.0**

* Ondersteuning voor Apple Silicon (M1).

* Mogelijkheid om de verbindingstekenreeks te onthouden terwijl u zich aanmeldt bij de bureaubladtoepassing.

**Updates in app v2.1.5.0**

* De bureaubladtoepassing reageert niet meer wanneer u bestanden uploadt in een map die Chinese tekens bevat (ASSETS-9237).

* de bureaubladtoepassing vervangt punten door streepjes in bestandsnamen (ASSETS-10955).

**Updates in app v2.1.4.0**

De nieuwe versie van de toepassing biedt oplossingen voor problemen.

**Updates in app v2.1.3.4**

De nieuwe versie van de toepassing biedt een oplossing voor problemen.

**Updates in app v2.1.3.3**

De nieuwe versie van de toepassing biedt een oplossing voor problemen.

**Updates in app v2.1.3.2**

Deze versie van de toepassing biedt een oplossing voor problemen.

**Updates in app v2.1.3.1**

Het probleem dat in deze versie is opgelost, is:

* De snelheid voor het uploaden en downloaden van bedrijfsmiddelen is verbeterd, zelfs bij grote bedrijfsmiddelen. Deze release verholpen een probleem waarbij het uploaden van elementen met [!DNL desktop app] soms mislukte toen zeer grote bestanden werden geüpload.

**Update in app v2.1.2.0**

* Er wordt een nieuwe optie voor [!UICONTROL Clear Cookies] toegevoegd aan het hoofdmenu van de toepassing. Het helpt met potentiële openings van een sessiekwesties, bijvoorbeeld wanneer het veranderen van een verbinding van een server aan een andere. Zie [ duidelijke koekjes alvorens ](/help/using/troubleshoot.md#cannot-login-cookies-issue) te verbinden.

* Er is een nieuwe optie toegevoegd waarmee de app, indien deze is geselecteerd, mappen en bestanden met knooppuntnamen in [!DNL Adobe Experience Manager] kan uploaden die overeenkomen met de lokale bestands- en mapnamen. Dit proces zorgt voor consistentie tussen lokale en geüploade namen.

  Dit gedrag is vergelijkbaar met het standaardgedrag in versie 1 van de bureaubladtoepassing. Als de optie in de huidige versie niet is ingeschakeld, worden witruimten en de tekens `% ; # , + ? ^ { } "` in mapnamen vervangen door streepjes in mappaden. De hoofdletters worden ook omgezet in kleine letters in mappaden. In bestandsnamen worden de tekens `# % { } ? &` echter vervangen door streepjes, maar de witruimten en het hoofdlettergebruik blijven behouden. Voor meer informatie zie, [ app Voorkeur ](/help/using/install-upgrade.md#set-preferences) en [ uploaden en nieuwe activa ](/help/using/using.md#upload-and-add-new-assets-to-aem) toevoegen.

**Update in app v2.1.1.0**

* Met een geavanceerde instelling kan de toepassing het gedrag van de v1.10-app emuleren bij het uploaden van mappen. In v1.10, respecteren de knoopnamen die in de bewaarplaats worden gecreeerd de ruimten en het omhulsel van de omslagnamen die door de gebruiker worden verstrekt. In versie 2.1 is het standaardgedrag ongewijzigd: meerdere spaties in mapnamen worden vervangen door afbreekstreepjes in de naam van de opslagplaats en nodenamen worden omgezet in kleine letters. Zie [ de toepassingsvoorkeur ](/help/using/install-upgrade.md#set-preferences).

**Update in app v2.1.0.0**

* Gebruikers kunnen nu de bestanden of mappen op de interface van de toepassing slepen, rechtstreeks vanuit Windows Verkenner of Mac Finder. Dit proces werkt naast de uploadoptie die beschikbaar is in de toepassing. Zie [ activa ](/help/using/using.md#upload-and-add-new-assets-to-aem) uploaden <!-- CQ-4309527 -->

**Update in app v2.0.3**

Het probleem dat in deze versie is opgelost, is:

* Oplossing voor het aanmeldingsprobleem voor app-gebruikers in Windows die proberen toegang te krijgen tot de DAM-opslagplaats op [!DNL Adobe Experience Manager] 6.5.5.0 .

**Updates in app v2.0.2**

De opgeloste problemen en updates zijn:

* De instelling voor uploadversnelling is nu beschikbaar om de uploadprestaties te verbeteren. Als deze instelling is ingeschakeld, wordt de app sneller geüpload met meer lokale CPU-threads en is de toepassing bronnenintensiever.

* Het element wordt geüpload wanneer de bestandsnamen of paden die bepaalde GB18030-tekens bevatten, vast zijn. <!-- CQ-4283494 -->

* De optie Sorteren op relevantie is beschikbaar na het schakelen naar een ander type in de zoekresultaten. <!-- CQ-4286874 -->

* De bureaubladtoepassing bevat nu submappen zonder dat deze expliciet moeten worden vernieuwd. <!-- CQ-4285711 -->

* (Windows) Probleem met onbruikbare toepassingsinterface op sommige Windows-computers is opgelost. Gebruikers kunnen niet op de toepassingsinterface klikken omdat deze vervormd lijkt te zijn met het klikgebied van interface-elementen &#39;verschoven&#39; zijwaarts. <!-- CQ-4280785 -->

**Updates in app v2.0.1**

De opgeloste problemen en updates zijn:

* Optie toestaan om `%Temp%` directory zo te configureren dat deze overeenkomt met `%APPDATA%` path. <!-- CQ-4282665 -->

* Gebruikers kunnen zich aanmelden bij [!DNL Experience Manager] Auteur via Okta SAML-verificatie. <!-- CQ-4278134 -->

## Installatie-instructies {#installation-instructions-v2}

Om te weten hoe te om app te installeren en te vormen, zie [  [!DNL Experience Manager]  Desktop app ](install-upgrade.md) installeren.

Als u van vorige [!DNL Experience Manager] Desktop app bevordert, moet u deze beste praktijken voor het overgaan volgen die bij [ verbetering van de vorige versie ](install-upgrade.md#upgrade-from-previous-version) worden vermeld.

## Belangrijke informatie over hoe de app werkt {#how-app-works}

Het is belangrijk om het volgende over de toepassing en hoe het werkt te begrijpen.

* De toepassing verstrekt volledige controle over verrichtingen die volledige overdracht van activa binaries van en aan [!DNL Experience Manager] vereisen (**Open**, **geeft uit**, **uploadt Veranderingen**, en **uploadt Assets**).

   * Als u met middelen op Desktop wilt werken, moet u uitdrukkelijk openen, uitgeven, of Download aan uw Desktop, of individueel, in een omslag, of via multi-selectie.

   * Als u lokale wijzigingen in elementen wilt uploaden naar [!DNL Experience Manager] , moet u [!UICONTROL Upload Changes] selecteren, afzonderlijk of via meerdere selecties.

   * De toepassing is geen &#39;synchronisatieclient&#39; die elementen synchroniseert op het bureaublad en [!DNL Experience Manager] .

   * De toepassing biedt geen netwerkshare waarmee de [!DNL Experience Manager] -opslagplaats wordt toegewezen als een virtuele mapstructuur.

* De lijst met elementen die door de toepassing wordt weergegeven, is gebaseerd op de status van de Assets-opslagplaats. Bestanden die lokaal zijn gedownload en vervolgens zijn hernoemd in de lokale bestanden of cachemap, worden niet weergegeven of beheerd met de toepassing.

* Als de app de verwachte resultaten niet weergeeft, klikt u op het pictogram Vernieuwen in de bovenste balk.

* Het lokale netwerkaandeel, dat wordt weergegeven wanneer u de handeling [!UICONTROL Reveal File] gebruikt, toont alleen bestanden (en mappen) die lokaal beschikbaar zijn. [!UICONTROL Reveal File] en [!UICONTROL Reveal Folder] downloadt vooraf elementen om de juiste elementen weer te geven in het gedeelde lokale netwerk.

* Het lokale netwerkaandeel van SMB (Mac) / WebDAV (Win) wordt gebruikt wanneer een Adobe Creative Cloud-app de elementbestanden leest die zijn gekoppeld of in een native bestand van de Creative Cloud-app zijn geplaatst.

Het volgende diagram illustreert de stroom van elementen en bestanden van de cloud naar het lokale bestandssysteem en de omgekeerde manier, zoals wordt geïnitieerd door gebruikershandelingen.

![ stroom van activa van [!DNL Experience Manager] server aan inheemse Desktopapps via Desktop app ](assets/da20_flow_diagram.png)

## Bekende problemen {#known-issues-v2}

**kwesties van het gebruikersinterface:**

* Soms wordt de interface van de bureaubladtoepassing leeg. Klik met de rechtermuisknop en klik op [!UICONTROL Refresh] om de toepassing opnieuw te laden. Nadat u deze vernieuwingen hebt aangebracht, begint u bij de basis van de DAM-opslagplaats. Updates of statussen van uw elementen blijven behouden. <!-- CQ-4270267 -->

* U kunt moeilijk door mappen of zoekresultaten navigeren zonder trackpad of muisaanwijzer. De schuifbalk wordt niet weergegeven bij muisapparaten zonder wiel. <!-- CQ-4269947 -->

* De voortgangsbalk wordt soms niet correct weergegeven wanneer het uploaden van het element wordt gewijzigd.

* Nadat het filter is toegepast en verwijderd om alle lokaal bewerkte elementen te zoeken, leidt de app gebruikers niet naar hun zoekresultaten of mapweergave waarmee de gebruikers zijn gestart. De toepassing geeft de hoofdmap van de DAM-opslagplaats weer.

* Wanneer u verbinding maakt met een URL waarop geen [!DNL Experience Manager] -server wordt uitgevoerd, reageert het verbindingsscherm soms niet. Sluit de toepassing af en start deze opnieuw.

**CRUD (creeer, lees, Update, en schrap) kwesties:**

* Wanneer u wijzigingen in een element met opmerkingen uploadt, worden de opmerkingen met het element opgeslagen in [!DNL Experience Manager] maar zijn ze niet zichtbaar als opmerkingen bij de versie. Dit probleem is opgelost in [!DNL Experience Manager] 6.4.5 en [!DNL Experience Manager] 6.5.1. Adobe raadt u aan de nieuwste servicepakketten te installeren. <!-- CQ-4268990 -->

* Een gebruiker kan de overdracht van elementen niet annuleren. Als u een onbedoelde grote overdracht hebt geactiveerd, sluit u de toepassing af en start u de toepassing opnieuw. <!-- CQ-4278940 -->

**De kwesties van het Platform:**

* In Windows kan de status van een element direct veranderen in [!UICONTROL Edited Locally] nadat het is geopend, ook al hebt u het wellicht niet bewerkt. Klik op [!UICONTROL Refresh] om bij te werken.

>[!MORELIKETHIS]
>
>* [[!DNL Experience Manager]  als a [!DNL Cloud Service]  documentatie ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service)
>* [[!DNL Experience Manager]  als a  [!DNL Cloud Service] [!DNL Assets] documentatie ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview)
>* [ hoe te  [!DNL Experience Manager]  Desktop app ](using.md) gebruiken
>* [ installeer en bevorder Desktop app ](install-upgrade.md)
>* [ Beste praktijken en het oplossen van problemenuiteinden ](troubleshoot.md)
