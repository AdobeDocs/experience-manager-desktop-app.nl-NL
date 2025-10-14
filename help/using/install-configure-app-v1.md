---
title: Desktop-app v1.10 installeren en configureren
description: Installeer en vorm  [!DNL Experience Manager]  Desktop app versie 1.10 om met  [!DNL Assets]  servers te werken en de activa in kaart te brengen om als aandrijving op uw Desktop op te zetten.
exl-id: 7f3bdfb1-d345-4e48-b020-6e06531f46f2
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# [!DNL Experience Manager] desktop app v1.10 installeren en configureren {#install-and-configure-aem-desktop-app}

Met de bureaubladtoepassing van [!DNL Experience Manager] kunt u de elementen in [!DNL Experience Manager] gemakkelijk openen op uw lokale bureaublad en gebruiken in alle bureaubladtoepassingen. Assets kan zichtbaar worden gemaakt in Mac Finder of Windows Verkenner, worden bewerkt in bureaubladtoepassingen en wijzigingen worden opgeslagen naar [!DNL Experience Manager] . Er wordt dan een nieuwe versie gemaakt tijdens het uploaden.

Dankzij deze integratie kunnen verschillende functies bedrijfsmiddelen centraal in de Assets beheren, ze openen in Creative Cloud en andere toepassingen en eenvoudig voldoen aan verschillende standaarden, waaronder branding.

U kunt als volgt de bureaubladtoepassing van [!DNL Experience Manager] gebruiken:

* Controleer of uw [!DNL Experience Manager] -serverversie compatibel is met de bureaubladtoepassing van [!DNL Experience Manager] . Zie de [&#x200B; verenigbaarheidsmatrijs &#x200B;](release-notes-of-v1.md#compatibilitymatrix).

* Download en installeer de toepassing.

* Test de verbinding met behulp van een paar elementen. Zie [&#x200B; Toegang en open activa op uw Desktop &#x200B;](use-app-v1.md#openondesktop).

## Systeemvereisten, vereisten en downloadkoppelingen {#system-requirements-prerequisites-and-download-links}

Voor gedetailleerde informatie, zie de [[!DNL Experience Manager]  nota&#39;s van de de toepassingsversie van de Desktop &#x200B;](release-notes-of-v1.md).

## De toepassing installeren en verbinden met de [!DNL Experience Manager] -server {#install-and-connect-aem-desktop-app-to-aem-server}

Voor details, zie [&#x200B; installeer en verbind  [!DNL Experience Manager]  Desktop app met  [!DNL Experience Manager]  server &#x200B;](use-app-v1.md#installandconnect).

>[!NOTE]
>
>Er kan slechts één exemplaar van de [!DNL Experience Manager] -bureaubladtoepassing worden geïnstalleerd en tegelijk actief zijn.

## Bestandsverwerking {#file-handling}

Wanneer u een bestand wijzigt van een netwerklocatie die is gekoppeld door de bureaubladtoepassing, worden de bestanden in twee fasen op die locatie opgeslagen. In de eerste fase wordt een bestand lokaal opgeslagen. Een gebruiker kan het bestand opslaan en aan het bestand blijven werken, zonder te wachten tot de overdracht is voltooid.

In de tweede fase uploadt de bureaubladtoepassing het bijgewerkte bestand naar de [!DNL Experience Manager] -server na een vooraf gedefinieerde vertraging (bijvoorbeeld dertig jaar). Deze bewerking vindt plaats op de achtergrond. Met de optie Asset Status weergeven kunt u de status van de uploadbewerking weergeven.

1. Middelen uploaden naar Assets.

1. Klik op het pictogram van de bureaubladtoepassing van [!DNL Experience Manager] op de werkbalk.

1. Selecteer in het menu de optie Asset Status weergeven.

1. Controleer in het dialoogvenster de status van de uploadbewerking.

>[!NOTE]
>
>[!DNL Experience Manager] -bureaubladtoepassingen kunnen bestanden van maximaal 40 GB verwerken.

## Verbinding maken met een [!DNL Experience Manager] -instantie achter een Dispatcher {#connect-to-an-aem-instance-behind-a-dispatcher}

Voor de kopieer- en verplaatsingsmethoden in de Assets API moeten de volgende aanvullende headers worden doorgegeven aan [!DNL Experience Manager] :

* X-bestemming
* X-diepte
* X-Overschrijven

[!DNL Experience Manager] maakt verbinding met [!DNL Experience Manager] via een URL die de standaardpoort bevat. Daarom moet de instelling `virtualhosts` in de Dispatcher-configuratie het standaardpoortnummer bevatten. Voor meer informatie rond `virtualhosts` configuratie, zie [&#x200B; virtuele gastheren &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#identifying-virtual-hosts-virtualhosts) identificeren.

Voor extra informatie bij het vormen van Dispatcher om door deze extra kopballen over te gaan, zie [&#x200B; het Specificeren van de Kopballen van HTTP &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration#specifying-the-http-headers-to-pass-through-clientheaders).

### Proxyondersteuning {#proxy-support}

De bureaubladtoepassing [!DNL Experience Manager] gebruikt de vooraf gedefinieerde proxy van het systeem om via HTTPS verbinding te maken met internet. De toepassing kan alleen verbinding maken met een netwerkproxy waarvoor geen extra verificatie is vereist.

Als u de instellingen van de proxyserver voor Windows configureert of wijzigt (Internet-opties > LAN-instellingen), start u de [!DNL Experience Manager] -bureaubladtoepassing opnieuw zodat de wijzigingen van kracht worden.

>[!NOTE]
>
>Proxyconfiguratie wordt alleen toegepast wanneer u de bureaubladtoepassing start. Sluit de app en start de app opnieuw om de wijzigingen door te voeren.

Als uw proxy verificatie vereist, kan het IT-team de Experience Manager Assets URL in de instellingen van de proxyserver toestaan om het toepassingsverkeer door te geven.

## Het dialoogvenster Elementinfo aanpassen {#customize-the-asset-info-dialog}

U kunt het dialoogvenster Elementinfo aanpassen door een van deze componenten of beide te bedekken:

* De gebruikersinterfacepagina van Granite op `/libs/dam/gui/content/assets/moreinfo`.

* De HTML `/css/javascript` -component op `/libs/dam/gui/components/admin/moreinfo` .

Welke component wordt bedekt hangt van de aard van de aanpassing af. Als u wilt wijzigen welke componenten worden weergegeven als onderdeel van het dialoogvenster Asset Info, bedekt u de pagina voor de gebruikersinterface van Granite. Bedek de HTML-component om de HTML-, CSS- of JavaScript-inhoud van het dialoogvenster te wijzigen.

## Cache beheren {#manage-cache}

In Windows bevindt de cache zich op `%LOCALAPPDATA%\Adobe\AssetsCompanion\Cache\` , waar een gecodeerde versie van de [!DNL Experience Manager] -host is geconfigureerd in de bureaubladtoepassing. `http://localhost:4502` wordt bijvoorbeeld weergegeven als `http%3A%2F%2Flocalhost%3A4502%2F` .

In macOS X staat een vergelijkbare map op `~/Library/Group Containers/group.com.adobe.aem.desktop/cache` .

### Optie voor in-app beheren van cache {#in-app-option-to-manage-cache}

U kunt bepalen hoeveel schijfruimte beschikbaar is voor lokale caching-doeleinden. De artefacten van de Assets-server worden lokaal in het cachegeheugen opgeslagen voor een vloeiender ervaring. U kunt de standaardinstellingen aanpassen aan uw wensen. Bovendien kunt u de cache wissen om alle elementen opnieuw op te halen. Klik op het pictogram van de toepassing en klik op **[!UICONTROL Advanced]** > **[!UICONTROL Manage Cache]** om de gewenste opties in te stellen. **&#x200B;**

>[!NOTE]
>
>Als u de cache wist, blijven de niet-opgeslagen wijzigingen behouden. Elementen die niet zijn ingecheckt op de [!DNL Experience Manager] -server, blijven behouden en worden niet verwijderd.

### Locatie van cache in Windows wijzigen {#change-location-of-cache-on-windows}

De standaardlocatie van de cache voor de bureaubladtoepassing van [!DNL Experience Manager] is als volgt:

* In Windows: `%LocalAppData%\Adobe\AssetsCompanion\Cache\EncodedAEMEndpoint` .

* In Mac, `~/Library/Group/Containers/group.com.adobe.aem.desktop/cache/EncodedAEMEndpoint`.

De `EncodedAEMEndpoint` is de geconfigureerde URL voor het [!DNL Experience Manager] eindpunt van de app. De waarde is een gecodeerde versie van de URL voor het opgeven van doelen voor de [!DNL Experience Manager] -server. Als de toepassing bijvoorbeeld `http://localhost:4502` als doel instelt, is de mapnaam `http%3A%2F%2Flocalhost%3A4502` . Het Windows-pad naar de cachemap in dit voorbeeld is `%LocalAppData%\Adobe\AssetsCompanion\Cache\http%3A%2F%2Flocalhost%3A4502` .

Als u de toepassing wilt laten verwijzen naar een andere map of een ander station, bewerkt u het configuratiebestand van de toepassing.

1. Navigeer naar de installatiemap van de app. De standaardlocatie in Windows is `C:\Program Files (x86)\Adobe\Adobe Experience Manager Desktop` .

1. Bewerk het `Adobe Experience Manager Desktop.exe.config` -bestand met een teksteditor.

   Beheerdersrechten zijn vereist om wijzigingen in dit bestand op te slaan.

1. Zoek naar de tekenreeks &quot;ProxyCacheRoot&quot;. U ziet dat de waarde ervan is ingesteld op de cachelocatie `%LocalAppData%\Adobe\AssetsCompanion\Cache` . Wijzig deze waarde in een geldig pad.

   >[!NOTE]
   >
   >De app leidt automatisch tot *&lt;Encoded AEM Endpoint>* subdirectory. Dit gedrag kan niet worden geconfigureerd.

>[!MORELIKETHIS]
>
>* Bekijk een [&#x200B; Inleiding aan  [!DNL Experience Manager]  Desktop app &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-learn/assets/creative-workflows/aem-desktop-app) (5 minuten, 43 seconden).
>* [&#x200B; Desktop app van het Gebruik  [!DNL Experience Manager]  &#x200B;](use-app-v1.md).
>* [&#x200B; het Oplossen van problemen  [!DNL Experience Manager]  Desktop app &#x200B;](troubleshoot-app-v1.md).
