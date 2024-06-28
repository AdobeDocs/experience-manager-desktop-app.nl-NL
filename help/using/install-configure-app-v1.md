---
title: Desktop-app v1.10 installeren en configureren
description: Installeren en configureren [!DNL Experience Manager] bureaubladtoepassing versie 1.10 om te werken met [!DNL Assets] -servers en de middelen toewijzen die als een station op uw bureaublad moeten worden gemonteerd.
exl-id: 7f3bdfb1-d345-4e48-b020-6e06531f46f2
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Installeren en configureren [!DNL Experience Manager] desktop app v1.10 {#install-and-configure-aem-desktop-app}

Met de [!DNL Experience Manager] bureaubladtoepassing, de middelen binnen [!DNL Experience Manager] zijn gemakkelijk toegankelijk op uw lokale bureaublad en kunnen in om het even welke Desktoptoepassingen worden gebruikt. Assets kan worden weergegeven in Mac Finder of Windows Verkenner, worden bewerkt in bureaubladtoepassingen en wijzigingen worden opgeslagen in [!DNL Experience Manager], een nieuwe versie maken na het uploaden.

Dankzij deze integratie kunnen verschillende functies bedrijfsmiddelen centraal in de Assets beheren, ze openen in Creative Cloud en andere toepassingen en eenvoudig voldoen aan verschillende standaarden, waaronder branding.

Als u de opdracht [!DNL Experience Manager] bureaubladtoepassing,

* Zorg ervoor dat uw [!DNL Experience Manager] serverversie is compatibel met de [!DNL Experience Manager] bureaubladtoepassing. Zie de [compatibiliteitsmatrix](release-notes-of-v1.md#compatibilitymatrix).

* Download en installeer de toepassing.

* Test de verbinding met behulp van een paar elementen. Zie [Elementen openen en openen op uw bureaublad](use-app-v1.md#openondesktop).

## Systeemvereisten, vereisten en downloadkoppelingen {#system-requirements-prerequisites-and-download-links}

Zie voor meer informatie de [[!DNL Experience Manager] Opmerkingen bij de release bureaubladapp](release-notes-of-v1.md).

## De toepassing installeren en verbinden met [!DNL Experience Manager] server {#install-and-connect-aem-desktop-app-to-aem-server}

Zie voor meer informatie [Installeren en verbinden [!DNL Experience Manager] bureaublad-app naar [!DNL Experience Manager] server](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Slechts één instantie van de [!DNL Experience Manager] bureaubladtoepassing kan worden geïnstalleerd en tegelijk actief zijn.

## Bestandsverwerking {#file-handling}

Wanneer u een bestand wijzigt van een netwerklocatie die is gekoppeld door de bureaubladtoepassing, worden de bestanden in twee fasen op die locatie opgeslagen. In de eerste fase wordt een bestand lokaal opgeslagen. Een gebruiker kan het bestand opslaan en aan het bestand blijven werken, zonder te wachten tot de overdracht is voltooid.

In de tweede fase uploadt de bureaubladtoepassing het bijgewerkte bestand naar de [!DNL Experience Manager] server na een vooraf gedefinieerde vertraging (bijvoorbeeld dertig). Deze bewerking vindt plaats op de achtergrond. Met de optie Asset Status weergeven kunt u de status van de uploadbewerking weergeven.

1. Middelen uploaden naar Assets.

1. Klik op de knop [!DNL Experience Manager] bureaubladtoepassing vanuit de werkbalk.

1. Selecteer in het menu de optie Asset Status weergeven.

1. Controleer in het dialoogvenster de status van de uploadbewerking.

>[!NOTE]
>
>[!DNL Experience Manager] bureaubladtoepassingen kunnen bestanden tot maximaal 40 GB verwerken.

## Verbinding maken met een [!DNL Experience Manager] -instantie achter een Dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

Voor de kopieer- en verplaatsingsmethoden in de Assets API moeten de volgende aanvullende koppen worden doorgegeven aan [!DNL Experience Manager]:

* X-bestemming
* X-diepte
* X-Overschrijven

[!DNL Experience Manager] desktop maakt verbinding met [!DNL Experience Manager] via een URL die de standaardpoort bevat. Daarom `virtualhosts` het plaatsen in de configuratie van Dispatcher zou het standaardhavenaantal moeten omvatten. Voor meer informatie over `virtualhosts` configuratie, zie [virtuele hosts identificeren](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#identifying-virtual-hosts-virtualhosts).

Voor meer informatie bij het vormen van de Dispatcher om door deze extra kopballen over te gaan, zie [De HTTP-headers opgeven](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#specifying-the-http-headers-to-pass-through-clientheaders).

### Proxyondersteuning {#proxy-support}

De [!DNL Experience Manager] bureaubladtoepassing gebruikt de vooraf gedefinieerde proxy van het systeem om via HTTPS verbinding te maken met internet. De toepassing kan alleen verbinding maken met een netwerkproxy waarvoor geen extra verificatie is vereist.

Als u de instellingen van de proxyserver voor Windows configureert of wijzigt (Internet Options > LAN Settings), start u de [!DNL Experience Manager] bureaubladtoepassing voor de wijzigingen die van kracht worden.

>[!NOTE]
>
>Proxyconfiguratie wordt alleen toegepast wanneer u de bureaubladtoepassing start. Sluit de app en start de app opnieuw om de wijzigingen door te voeren.

Als uw proxy verificatie vereist, kan het IT-team de Experience Manager Assets URL in de instellingen van de proxyserver toestaan om het toepassingsverkeer door te geven.

## Het dialoogvenster Elementinfo aanpassen {#customize-the-asset-info-dialog}

U kunt het dialoogvenster Elementinfo aanpassen door een van deze componenten of beide te bedekken:

* De gebruikersinterfacepagina van Granite op `/libs/dam/gui/content/assets/moreinfo`.

* De HTL `/css/javascript` component bij `/libs/dam/gui/components/admin/moreinfo`.

Welke component wordt bedekt hangt van de aard van de aanpassing af. Als u wilt wijzigen welke componenten worden weergegeven als onderdeel van het dialoogvenster Asset Info, bedekt u de pagina voor de gebruikersinterface van Granite. Bedek de HTML-component om de HTML-, CSS- of JavaScript-inhoud van het dialoogvenster te wijzigen.

## Cache beheren {#manage-cache}

In Windows bevindt de cache zich op `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\`, waarbij een gecodeerde versie van de [!DNL Experience Manager] host geconfigureerd in de bureaubladtoepassing. Bijvoorbeeld: `http://localhost:4502` verschijnt zoals `http%3A%2F%2Flocalhost%3A4502%2F`.

In macOS X staat een vergelijkbare map op `~/Library/Group Containers/group.com.adobe.aem.desktop/cache`.

### Optie voor in-app beheren van cache {#in-app-option-to-manage-cache}

U kunt bepalen hoeveel schijfruimte beschikbaar is voor lokale caching-doeleinden. De artefacten van de Assets-server worden lokaal in het cachegeheugen opgeslagen voor een vloeiender ervaring. U kunt de standaardinstellingen aanpassen aan uw wensen. Bovendien kunt u de cache wissen om alle elementen opnieuw op te halen. Als u de gewenste opties wilt instellen, klikt u op het pictogram van de toepassing en klikt u op **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]**. ****

>[!NOTE]
>
>Als u de cache wist, blijven de niet-opgeslagen wijzigingen behouden. Alle elementen die niet zijn geselecteerd in het dialoogvenster [!DNL Experience Manager] server worden behouden en niet verwijderd.

### Locatie van cache in Windows wijzigen {#change-location-of-cache-on-windows}

De standaardlocatie van de cache voor de [!DNL Experience Manager] desktop app is als volgt:

* In Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint`.

* In Mac: `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`.

De `EncodedAEMEndpoint` is de configuratie van de app [!DNL Experience Manager] eindpunt-URL. De waarde is een gecodeerde versie van de URL voor het opgeven van doelen voor het [!DNL Experience Manager] server. Als de toepassing zich bijvoorbeeld richt op `http://localhost:4502`, is de mapnaam `http%3A%2F%2Flocalhost%3A4502`. Het pad van Windows naar de cachemap in dit voorbeeld is `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502`.

Als u de toepassing wilt laten verwijzen naar een andere map of een ander station, bewerkt u het configuratiebestand van de toepassing.

1. Navigeer naar de installatiemap van de app. De standaardlocatie in Windows is `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop`.

1. Bewerk de `Adobe Experience Manager Desktop.exe.config` bestand met een teksteditor.

   Beheerdersrechten zijn vereist om wijzigingen in dit bestand op te slaan.

1. Zoek naar de tekenreeks &quot;ProxyCacheRoot&quot;. U ziet dat de waarde ervan is ingesteld op de cachelocatie `%LocalAppData%\Adobe\AssetsCompanion\Cache`. Wijzig deze waarde in een geldig pad.

   >[!NOTE]
   >
   >De app maakt automatisch een *&lt;encoded aem=&quot;&quot; endpoint=&quot;&quot;>* subdirectory. Dit gedrag kan niet worden geconfigureerd.

>[!MORELIKETHIS]
>
* Kijk naar een [Inleiding tot [!DNL Experience Manager] bureaubladtoepassing](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app) (5 minuten, 43 seconden).
* [Gebruiken [!DNL Experience Manager] bureaubladtoepassing](use-app-v1.md).
* [Problemen oplossen [!DNL Experience Manager] bureaubladtoepassing](troubleshoot-app-v1.md).
