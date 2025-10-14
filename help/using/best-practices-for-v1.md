---
title: Aanbevolen werkwijzen voor bureaubladtoepassing v1.10
description: Zeer belangrijke mogelijkheden en geadviseerd gebruik van  [!DNL Adobe Experience Manager]  Desktop app versie 1.10.
exl-id: 5de06b33-c05c-47eb-b884-408b6f9afc94
source-git-commit: 1c7437786a50eeafa884ce92b745f3438b2d2b88
workflow-type: tm+mt
source-wordcount: '1651'
ht-degree: 0%

---

# Aanbevolen werkwijzen AEM desktop app v1.10 {#aem-desktop-app-best-practices}

## Overzicht {#overview}

De bureaubladtoepassing van [!DNL Adobe Experience Manager] koppelt de DAM-oplossing (Digital Asset Management) aan uw bureaublad, zodat u de bestanden die beschikbaar zijn in de AEM webinterface rechtstreeks op het bureaublad kunt openen. Als u middelen van de Desktop bewaarde, wordt het geupload aan AEM bij de aangewezen plaats.

AEM bureaubladtoepassing voorkomt dat u onjuiste lokale kopieën bijwerkt of een verkeerd middel in AEM bijwerkt. De gebruiksvriendelijke workflow van de bureaubladtoepassing wordt ingeschakeld met de technologie voor netwerkdeling die desktopbesturingssystemen bieden.

De bureaubladtoepassing monteert de AEM Assets-opslagplaats als een gedeelde netwerkverbinding op het bureaublad. Daarom worden de mappen en bestanden weergegeven alsof ze lokaal zijn. Het wordt echter afgeraden om bewerkingen voor het beheer van digitale elementen rechtstreeks vanaf het bureaublad uit te voeren in het gekoppelde netwerkaandeel in Finder of Explorer. In plaats daarvan raadt de Adobe u aan de gebruikersinterface van AEM Assets te gebruiken om bewerkingen uit te voeren, zoals het kopiëren of verplaatsen van een groot aantal elementen.

>[!NOTE]
>
>Alvorens dit document te lezen, kunt u de algemene [&#x200B; beste praktijken van de AEM en van de Creative Cloud integratie &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-65/content/assets/administer/aem-cc-integration-best-practices) voor een overzicht op hoger niveau van het onderwerp herzien.

## AEM bureaubladtoepassingsarchitectuur {#aem-desktop-app-architecture}

AEM desktop gebruikt WebDAV (Windows) of SMB (Mac) netwerkshares om netwerkshares te koppelen. Het gekoppelde netwerkaandeel is alleen lokaal. AEM bureaubladtoepassing onderschept de aanroepen (openen, lezen, schrijven) en biedt extra lokale caching. Het vertaalt verre vraag aan de server van AEM Assets aan geoptimaliseerde AEM HTTP- verzoeken. In het volgende diagram wordt de architectuur van de AEM desktop-app weergegeven.

![&#x200B; AEM Desktop app architectuur &#x200B;](assets/arch_v1.png)

*Cijfer: Desktop app architectuur*

Wanneer een bestand wordt opgeslagen, zorgt de extra cache bij het schrijven ervoor dat het eerst lokaal wordt opgeslagen, zodat de gebruiker niet op de netwerkoverdracht hoeft te wachten. Na een vooraf gedefinieerde vertraging (30 seconden) wordt het bestand geüpload naar AEM op de achtergrond en wordt het element vervolgens geüpload naar AEM. AEM bureaubladtoepassing biedt een interface voor het controleren van de status van uploads van achtergrondbestanden.

## Aanbevolen gebruik van AEM bureaubladtoepassing {#recommended-use-of-aem-desktop-app}

De belangrijkste mogelijkheden van de AEM desktop-app zijn:

* **Openend dossiers van het Web UI van AEM Assets op Desktop**. Vanuit de webinterface kunt u elementen op het bureaublad (in Finder, Verkenner) weergeven of een element openen met een bureaubladtoepassing.

* **Controle uit en controleer binnen**. Assets kan worden uitgecheckt voor bewerking. De is gemarkeerd als vergrendeld voor de gebruiker in AEM Assets. Na het bewerken kunt u het element inchecken om het te ontgrendelen.

* **sparen veranderingen in dossiers**. Wijzigingen die u in het gedeelde netwerkbestand opslaat, worden automatisch naar AEM geüpload en er wordt een nieuwe versie gemaakt.

* **Plaats verbonden activa in andere documenten**. In toepassingen, zoals Creative Cloud ([!DNL Adobe Photoshop], [!DNL Adobe InDesign], en [!DNL Adobe Illustrator]), kunt u een extern dossier als verbinding plaatsen. U kunt bijvoorbeeld een afbeelding in een InDesign-document plaatsen. In dit geval kunt u met de netwerkshare-ount elementen van AEM selecteren en zoeken naar plaatsing. Het plaatsen van gekoppelde bestanden werkt ook in bepaalde apps die geen Adobe hebben, zoals MS® Office.

* **resolutie van de Verwijzing in AEM**. Als zowel de geplaatste bestanden als de hoofdbestanden met de koppeling in AEM worden opgeslagen, kan dit automatisch informatie geven over de elementverwijzingen naar de server.

* **heb toegang tot de activa van de Desktop**. In de gekoppelde netwerkshare beschikt een contextueel menu over een dialoogvenster [!UICONTROL More Info] (grotere voorvertoning, belangrijke metagegevens) en de mogelijkheid om elementen te openen in de AEM-interface.

* **Uploading grote, hiërarchische omslagen in bulk**. Als u **gebruikt creeer** > **Omslag uploadt** optie in AEM UI om activa te uploaden, uploadt de AEM Desktop app de geselecteerde omslaghiërarchie aan AEM in de achtergrond. De voortgang van het uploaden wordt gecontroleerd met een speciale gebruikersinterface in de bureaubladtoepassing.

## Ongepast gebruik van AEM bureaubladtoepassing {#inappropriate-use-of-aem-desktop-app}

* Gebruik de AEM desktop-app niet om middelen van het bureaublad te beheren. AEM bureaubladtoepassing is niet ontworpen als vervanging voor netwerkstations. Gebruik in plaats hiervan de volgende mogelijkheden:

   * AEM Assets Web UI voor het beheer van digitale elementen (zoeken of delen van elementen, metagegevens en kopiëren of verplaatsen).

   * AEM bureaubladtoepassing [!UICONTROL Folder Upload] om grote, hiërarchische mappen te uploaden.

* Behandel AEM bureaubladtoepassing niet als een &quot;desktop sync&quot;-client voor AEM Assets. Het belangrijkste voordeel van AEM bureaubladtoepassing is dat deze &#39;virtuele&#39; toegang biedt tot de gehele opslagruimte en dat toepassingen voor desktopsynchronisatie doorgaans alleen elementen synchroniseren die bij één gebruiker horen. AEM desktop-app biedt enige mate van caching en uploaden naar de achtergrond. Toch werkt deze toepassing heel anders dan standaard &quot;Sync&quot;-toepassingen, zoals Adobe Creative Cloud-bureaubladtoepassing of Microsoft OneDrive.

* Gebruik AEM netwerkstations voor bureaubladtoepassingen niet om elementen vaak op te slaan. Alle opslagbewerkingen worden naar AEM Assets verzonden. Daarom is het onpraktisch om intensieve bewerkingen rechtstreeks uit te voeren in de gekoppelde AEM Assets-opslagplaats. Door een element rechtstreeks in de gekoppelde opslagplaats te bewerken, loopt de tijdlijn van het element vast met irrelevante versies en worden extra overheadkosten aan de server opgelegd.

* Gebruik AEM bureaubladtoepassing niet voor het migreren van grote hoeveelheden gegevens van de ene AEM naar de andere. Zie de [&#x200B; Gids van de Migratie &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-65/content/assets/administer/assets-migration-guide) om activa migraties te plannen en uit te voeren. In tegenstelling, steunt Desktop app [&#x200B; bulksgewijs uploaden &#x200B;](use-app-v1.md#bulkupload) groot aantal activa voor het eerst in [!DNL Adobe Experience Manager].

## Recommendations voor geselecteerde gebruiksgevallen {#recommendations-for-selected-use-cases}

### Toegang tot middelen voor creatieve gebruikers {#access-to-assets-for-creative-users}

AEM bureaubladtoepassing biedt virtuele toegang tot de hele DAM-opslagplaats - en het kan lastig zijn voor creatieve gebruikers op desktopcomputers om de juiste middelen op hun bureaublad te vinden en te openen. Gebruik deze beste praktijken om dat voor hen te vereenvoudigen.

* De samenwerkingseigenschappen van het gebruik in de UI van het Web van AEM Assets om directere toegang tot de juiste activa voor de creatieve gebruiker te verlenen. U kunt onder andere mappen of verzamelingen delen, slimme verzamelingen (opgeslagen zoekopdrachten) opgeven of meldingen met aanwijzers naar de juiste elementen verzenden. Creatieve gebruiker kan dan bureaubladacties in de webinterface gebruiken voor snelle toegang tot deze middelen op zijn bureaublad.

* Overweeg de juiste machtigingen voor middelen (toegangsbeheer) om de weergave in de DAM-opslagplaats voor creatieve gebruikers te vereenvoudigen, zodat ze in feite alleen toegang hebben tot de middelen die ze nodig hebben of waarin ze geïnteresseerd zijn:

   * Bepaalde gebieden die niet relevant zijn voor de creatieve gebruikers kunnen worden geweigerd voor hun gebruikersgroepen, om ze uit hun weergave te verwijderen, ook op het bureaublad.

   * De meeste activa in DAM zijn definitief en niet bedoeld om te veranderen - dergelijke activa zouden read-only voor de creatieve gebruikers moeten zijn.

   * Alleen elementen die moeten worden gewijzigd of geretoucheerd, moeten voor creatieve gebruikers zijn ingeschakeld. Sommige organisaties gebruiken AEM Projecten en de omslagen die zij aan gastheeractiva creëren die nog onderworpen aan veranderingen zijn.

### Elementen zoeken {#searching-assets}

Als u wilt zoeken naar een bestand dat u op het bureaublad wilt openen, gaat u als volgt te werk:

* Gebruik de AEM Assets-webinterface om het element te zoeken. Niet alleen is zoekopdracht in AEM Assets krachtig (zoekfacetten, opgeslagen zoekopdrachten), het biedt ook extra mogelijkheden om de juiste middelen te vinden. Deze omvatten extra filters, zoals de capaciteit om activa te zoeken die op status (goedkeuring, vervaldatum) worden gebaseerd, inzamelingen, taken, berichten, en het delen van omslagen/inzamelingen met andere gebruikers/groepen.

* Nadat u het middel hebt gevonden, gebruikt u bureaubladhandelingen in AEM gebruikersinterface om het middel op het bureaublad te openen.

### Elementen bijwerken die zijn geopend met AEM bureaubladtoepassing {#updating-assets-opened-using-aem-desktop-app}

Als u een middel direct op de plaats uitgeeft die van AEM Assets aan een lokaal netwerkaandeel in kaart wordt gebracht, wordt het middel geupload aan AEM telkens als u het op Desktop bewaart. AEM maakt bovendien een versie en genereert uitvoeringen.

Als een in AEM opgeslagen element een update nodig heeft:

* Voor **minder belangrijke updates**, zoals minder belangrijke het retoucheren verzoeken in het goedkeuringsproces:

   * Bekijk het bestand en open het op het bureaublad.

   * Werk het bestand bij.

   * Sla de bijgewerkte versie op. Het element wordt bijgewerkt en de tijdlijn geeft de oorspronkelijke versie weer ter vergelijking.

* Voor **belangrijke updates**, zoals een veranderingsverzoek dat een kleine creatieve cyclus van het WIP vereist:

   * Gebruik de optie Tonen om de juiste map op het bureaublad te openen.

   * Kopieer het bestand naar een WIP-map buiten de toegewezen AEM Assets-share (kopieer het bestand bijvoorbeeld naar een map die is gesynchroniseerd met de Adobe Creative Cloud-bureaubladtoepassing).

   * Werk aan het bestand en sla het bestand op. De wijzigingen worden niet opgeslagen in AEM Assets.

   * Nadat de bewerkingen zijn voltooid, verplaatst, kopieert of slaat u het bestand dat van AEM is toegewezen, op om het te uploaden als een nieuwe versie.

## Netwerkprestaties {#network-performance}

Een goede gebruikerservaring met de AEM desktop-app is afhankelijk van stabiele netwerkconnectiviteit en een goed afgestemde server, met name voor het uploaden en bijwerken van middelen. Deze aanbevelingen zijn voor de netwerk/teams van IT in organisaties.

### Netwerkoverwegingen {#network-considerations}

Om beste praktijken rond het netwerkconfiguratie van AEM Assets te begrijpen, ga [&#x200B; hoe te in bulk migreren activa &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-65/content/assets/administer/assets-migration-guide) document. Enkele belangrijke aspecten die u helpen de AEM bureaubladervaring voor de gebruikers te optimaliseren, zijn:

* **Gebruik behoorlijk gevormde Dispatcher**. Gebruik AEM Dispatcher voor extra veiligheid en zorg ervoor dat het voor [&#x200B; AEM de verbinding van de Desktopapp om achter een Dispatcher wordt gevormd te AEM &#x200B;](install-configure-app-v1.md#connect-to-an-aem-instance-behind-a-dispatcher)

* **sparen bandbreedte**. U kunt de voorvertoning van pictogrammen in Finder op Mac uitschakelen wanneer u in de gekoppelde opslagplaats bladert met Finder. De Finder vraagt elk bestand om een voorvertoning te genereren en zorgt ervoor dat de bureaubladtoepassing het element lokaal downloadt en in de cache plaatst. Terwijl het besparen van bandbreedte, vermindert het ook gebruikerservaring voor de gebruikers op de Desktop, zodat zou het moeten worden gedaan wanneer het werken aan bewaarplaatsen met grote activa of beperkte bandbreedte.

>[!NOTE]
>
>Als u pictogramvoorvertoningen wilt uitschakelen, gaat u in de Finder naar [!UICONTROL View] , selecteert u [!UICONTROL View Options] en schakelt u vervolgens de optie [!UICONTROL Show icon preview] uit. Dit werkt alleen voor de huidige map. Klik op de optie [!UICONTROL Use as default] in hetzelfde dialoogvenster om van deze map een standaardmap te maken.

### Serverprestaties optimaliseren {#optimizing-server-performance}

Om te begrijpen hoe de server van AEM Assets voor prestaties zou moeten worden geoptimaliseerd, ga naar [&#x200B; de Reeksen van Prestaties van AEM Assets &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-65/content/assets/administer/performance-tuning-guidelines). Sommige belangrijke aspecten van de serverprestaties voor AEM bureaubladtoepassing betreffen het optimaliseren van de workflowconfiguratie, zodat deze goed functioneert bij het uploaden van middelen:

* **krachtigere activa uploaden**. Vorm het [&#x200B; AEM de werkschemamodel van de Update van Activa om transient &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-65/content/assets/administer/performance-tuning-guidelines) te zijn.

* **grens serverCpu voor uploads**. Zorg ervoor dat de maximale parameter voor parallelle workflowtaken correct is ingesteld, zodat uploads niet alle CPU uitputten.
