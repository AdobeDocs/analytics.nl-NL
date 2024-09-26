---
title: Verwerkingsregels voor distributiekanalen
description: De de verwerkingsregels van het Kanaal van de marketing bepalen als een bezoeker voldoet aan de criteria die aan een kanaal worden toegewezen. De regels verwerken elke hit die een bezoeker op uw site aanbrengt. Wanneer een regel niet aan de criteria voor een kanaal voldoet, of als de regels niet correct worden gevormd, wijst het systeem de slag aan Geen Geïdentificeerd Kanaal toe.
feature: Marketing Channels
exl-id: 825f70a5-cce3-4b1c-bb42-828388348216
role: Admin
source-git-commit: 09c1484f3f1f1a7f5e25aa24a333dbaabb4dc9d0
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 0%

---

# Verwerkingsregels voor distributiekanalen

Regels voor de verwerking van marketingkanalen bepalen of een bezoeker voldoet aan de criteria die aan een kanaal zijn toegewezen door elke hit die een bezoeker op uw site maakt, te verwerken. De regels worden verwerkt in de volgorde die u opgeeft en wanneer aan een regel wordt voldaan, stopt het systeem met het verwerken van de resterende regels.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Processing Rules]** .

![](assets/buckets_2.png)

Aanvullende opmerkingen over de verwerking:

* De gegevens die met deze regels worden verzameld, zijn permanent. Regels die na gegevensverzameling worden gewijzigd, zijn niet met terugwerkende kracht. Adobe raadt u ten zeerste aan alle omstandigheden te bekijken en te overwegen voordat u [!UICONTROL Marketing Channel Processing Rules] opslaat om te voorkomen dat gegevens die op onjuiste kanalen worden verzameld, worden verzameld.
* U kunt maximaal 25 afzonderlijke marketingkanalen configureren.
* De regels kunnen tot variabelen toegang hebben die VISTA heeft geplaatst, maar kunnen tot geen gegevens toegang hebben die VISTA heeft geschrapt.
* Twee marketingkanalen krijgen nooit krediet voor dezelfde gebeurtenis (zoals aankopen of klikken). Op deze manier verschillen de afzetkanalen van eVars (waar twee eVars kredieten voor dezelfde gebeurtenis kunnen ontvangen).
* Als er een hiaatdekking van uw regels is, kunt u [ Geen Geïdentificeerd Kanaal zien.](/help/components/c-marketing-channels/c-faq.md)

## Vereisten

* Herzie de conceptuele informatie in [ Begonnen het Worden met de Kanalen van de Marketing ](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
* Maak een of meer kanalen zodat u er regels aan kunt toewijzen. Zie [ marketing kanalen ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md) toevoegen.
* Bekijk de aanbevolen procedures voor het gebruik van [!UICONTROL Marketing Channels] met [!UICONTROL Attribution] .

## Verwerkingsregels voor marketingkanalen maken

Maak verwerkingsregels voor marketingkanalen die bepalen of een bezoeker voldoet aan de criteria die aan een kanaal zijn toegewezen.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
2. Selecteer een rapportsuite.

   Als in uw rapportsuite geen kanalen zijn gedefinieerd, wordt de pagina [!UICONTROL Marketing Channels: Auto Setup] weergegeven.

   Zie [ in werking stellen de Automatische Opstelling ](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

3. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Processing Rules]**. Als u de automatische opstelling in werking stelde, werden een reeks kanaal en regels automatisch bepaald voor u.

   ![Stap Resultaat](assets/marketing_channel_rules.png)

4. Als u een regel wilt toevoegen, selecteert u deze in het menu **[!UICONTROL Add New Rule Set]** . Als u een kanaal selecteert, krijgt u een regelmalplaatje en als u Douane selecteert, begint u van een lege plaats. Met beide opties kunt u de regelset naar wens wijzigen.

   ![Stap Resultaat](assets/example_email.png)

5. Klik op **[!UICONTROL Add New Rule SetRule]** om door te gaan met het maken van regels.
6. Als u regels een prioriteit wilt geven, sleept u ze naar de gewenste positie.
7. Klikken **[!UICONTROL Save.]**

### De waarde van het marketingkanaal instellen

**[!UICONTROL Set the channel's value]** definieert de detaildimensie van het marketingkanaal die beschikbaar is voor dat kanaal.

### Regelcriteria

Deze referentietabel definieert de velden, opties en raakkenmerken die u kunt gebruiken om de regels voor de verwerking van marketingkanalen te definiëren.

>[!NOTE]
>
>Om het even welk tekstgebied dat u, zoals de parameter van het vraagkoord of lijsten van waarden bepaalt om tegen aan te passen, wordt geëvalueerd als **case-insensitive** waarden. Als u bijvoorbeeld een regel hebt waarin de parameter van de querytekenreeks `cmp = abc123` voorkomt, komen alle verschillen tussen hoofdletters en kleine letters van zowel `cmp` als `abc123` overeen.

| Term | Definitie |
|--- |--- |
| Alle | Activeert dit kanaal slechts wanneer alle criteria in de regel waar zijn. |
| Alle | Activeert dit kanaal wanneer om het even welke criteria in de regel waar zijn. Deze optie is alleen beschikbaar als de regel meer dan één criterium bevat. |
| AMO-id | De primaire volgcode die wordt gebruikt door de Adobe Advertising- en Advertising Analytics-integratie. Wanneer een van deze integraties is ingeschakeld, kunt u het voorvoegsel van de trackingcode gebruiken om specifieke Advertising-kanalen te identificeren. Gebruik een &#39;AMO-id&#39; die begint met &#39;AL&#39; voor zoeken en sociaal zoeken of &#39;AC&#39; voor weergave. Wanneer de AMO-id wordt gebruikt in marketingkanalen, kunnen de maatstaven voor klikken/kosten/indruk worden toegewezen aan het juiste kanaal. Als de AMO-id niet is geconfigureerd, gaan deze meetgegevens naar Direct of Geen. |
| AMO EF-ID | De secundaire die volgcode door Adobe Advertising wordt gebruikt. Het belangrijkste doel van deze volgcode is als sleutel te dienen voor het terugsturen van gegevens naar Advertising. Het kan, echter, ook worden gebruikt om DisplayClickThroughs en DisplayThroughs als twee afzonderlijke marketing kanalen te identificeren. Hiervoor stelt u de logica voor het marketingkanaal in voor &#39;AMO EF-id&#39; die eindigt met `:d` voor het weergeven van doorklikbewerkingen of voor &#39;AMO EF-id&#39; die eindigt met `:i` voor Display ViewThroughs. Als u Weergave niet in twee kanalen wilt splitsen, gebruikt u in plaats daarvan de dimensie AMO-id. |
| Conversievariabelen | Bestaat uit eVars die voor deze rapportsuite zijn ingeschakeld en alleen van toepassing zijn wanneer deze variabelen via de code van de Adobe op de pagina zijn ingesteld. |
| Exists | Er zijn verschillende selecties beschikbaar, waaronder:<ul><li>**bestaat niet**: Specificeert dat het slagattribuut niet op het verzoek bestaat. Als de gebruiker bijvoorbeeld in een verwijzend domein een URL typt of op een bladwijzer klikt, bestaat het kenmerk van het verwijzende domein niet.</li><li>**is Leeg**: Specificeert dat een klapattribuut bestaat, gewoonlijk een eVar of vraagkoordparameter, maar er is geen waarde verbonden aan de klapattributen.</li><li>**bevat niet**: Laat u specificeren, bijvoorbeeld, dat een verwijzend domein geen specifieke waarde bevat (in tegenstelling tot het gebruiken van de selectie &quot;bevat&quot;.)</li></ul> |
| Het kanaal identificeren als | Koppelt de regel aan een marketingkanaal dat u aan de pagina Kanaalbeheer voor marketing hebt toegevoegd. |
| Komt overeen met regels voor betaalde zoekdetectie | Een betaalde zoekopdracht gevonden door de Adobe. Betaalde zoekopdrachten worden uitgevoerd wanneer bedrijven kosten betalen voor de zoekfunctie om hun site te kunnen aanbieden. Betaalde zoekopdrachten worden meestal boven of rechts in de zoekresultaten weergegeven. |
| Overeenkomsten met de regels voor natuurlijke zoekdetectie | Een niet-betaalde zoekopdracht die wordt gedetecteerd door de rapportage van de Adobe. |
| Referrer komt overeen met interne URL-filters | Een bezoek de waarvan pagina URL een intern filter URL aanpast, zoals die voor de rapportreeks in Hulpmiddelen Admin wordt bepaald. |
| Referrer komt niet overeen met interne URL-filters | De verwijzende URL komt niet overeen met een intern URL-filter, zoals gedefinieerd voor de rapportsuite in Admin Tools. U kunt deze instelling gebruiken met de URL van de pagina en bestaat om een algemene regel voor alle vangsten in te stellen, zodat geen van de bezoeken wordt aangeland in de sectie Geen kanaal geïdentificeerd van het rapport. |
| Sluiten negeren die overeenkomen met interne URL-filters | (Voor referentie) Tracks komen alleen van extern genoemde sites. Laat deze instelling meestal ingeschakeld, tenzij u intern verkeer wilt opnemen. |
| Is de eerste bezoekpagina | De eerste pagina van een bezoek die wordt gedetecteerd door Adobe-rapportage. |
| Pagina | De [ dimensie van de Pagina ](/help/components/dimensions/page.md). |
| Paginadomein | Het domein van de pagina waarop de bezoeker landt, zoals `products.example.com` . |
| Paginadomein en pad | Het domein en pad, zoals `products.example.com/mens/pants/overview.html` . |
| Hoofddomein van pagina (TLD+1) | Het hoofddomein van de pagina waarop de bezoeker landt, zoals example.co.uk. |
| Pagina-URL | De URL van een webpagina op uw site. |
| Referentiedomein | De [ Verwijzende domein ](/help/components/dimensions/referring-domain.md) dimensie |
| Parameter querytekenreeks | Gebruik een individuele parameter van het vraagkoord. U kunt slechts één parameter van het vraagkoord per criterium specificeren. Als u aanvullende parameters voor queryreeksen wilt toevoegen, gebruikt u `ANY` als uw operator en voegt u vervolgens parameters voor queryreeksen aan de regel toe. |
| Referenter | De locatie van de webpagina (volledige URL) waar uw bezoekers zich bevonden voordat ze naar uw site kwamen. Er bestaat een verwijzing buiten het gedefinieerde domein. |
| Refererend Domein en Weg | Een aaneenschakeling van het Verwijzende Domein en weg URL. Voorbeelden zijn:    `www.example.com/products/id/12345` of `ad.example.com/foo` |
| Verwijzen naar parameter | Een parameter van het vraagkoord op referentie URL. Als uw bezoekers bijvoorbeeld uit `example.com/?page=12345&cat=1` komen, zijn pagina en kat de verwijzende parameters. |
| Refererend hoofddomein | Het hoofddomein van de referentie. Er bestaat een verwijzing buiten het gedefinieerde domein. |
| Zoekmachine | Een zoekmachine zoals Google of Yahoo! die bezoekers naar uw site bracht. |
| Trefwoorden zoeken | Een woord dat wordt gebruikt om een zoekopdracht uit te voeren met een zoekmachine. |
| Zoekmachine + trefwoorden | Een samenvoeging van het Sleutelwoord van het Onderzoek en de Motor van het Onderzoek om de onderzoeksmotor uniek te identificeren. Bijvoorbeeld, als u naar de woordcomputer zoekt, worden de onderzoeksmotor en het sleutelwoord geïdentificeerd als volgt: `Search Tracking Code = "<search_type>:<search engine>:<search keyword>" where    search_type = "n" or "p", search_engine = "Google", and search_keyword = "computer"`**Nota:** n = natuurlijk; p = betaald |
| De waarde van het kanaal instellen op | Plaatst de [ dimensie van het Detail van het Kanaal van de Marketing ](/help/components/dimensions/marketing-detail.md). U bepaalt welke waarde het beste zou zijn in de context van de regel. Voorbeelden zijn banneradvertentie-id, zoektrefwoord of e-mailcampagne. |

## Regelvolgorde en definities van marketingkanalen {#channel-rules}

De kanaalregels worden verwerkt in de volgorde die u opgeeft. De Adobe raadt u aan eerst betaalde of beheerde kanalen (zoals betaalde onderzoek, natuurlijk onderzoek, vertoning, of e-mail) te plaatsen zodat zij krediet over biologische kanalen (zoals direct, intern, verwijzende domeinen) ontvangen.

Hieronder ziet u de aanbevolen volgorde voor kanaalregels en voorbeelddefinities:

### Betaalde zoekopdracht {#paid-search}

Betaalde zoekopdracht is een woord of uitdrukking dat u betaalt voor plaatsing in zoekresultaten. Dit kanaal wordt typisch bepaald gebaseerd op de parameter van het vraagkoord (zie het kanaalvoorbeeld van de Vertoning) of betaalde onderzoeksdetectieregels.

#### Betaalde zoekdetectie

Voor de detectie van betaalde zoekopdrachten gebruikt het marketingkanaal instellingen die op de pagina [!UICONTROL Paid Search Detection] zijn geconfigureerd. ( **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Paid Search Detection]** ). De doel-URL komt overeen met de bestaande regel voor betaalde zoekdetectie voor dat zoekprogramma.

Voor de marketingkanaalregel zijn de [!UICONTROL Paid Search] -instellingen als volgt:

![](assets/example_paid_search.png)

Zie [ Betaalde Opsporing van het Onderzoek ](../general/paid-search-detection/paid-search-detection.md) voor meer informatie.

### Natuurlijk zoeken {#natural-search}

Natuurlijk zoeken is wanneer bezoekers uw website vinden via een zoekprogramma en het zoekprogramma heeft uw site gerangschikt zonder dat u voor de aanbieding betaalt.

Adobe bepaalt onderzoeksverkeer dat op een interne raadpleging van onderzoeksmotoren wordt gebaseerd. Als een verwijzer criteria voor een onderzoeksmotor aanpast, bepaalt het dan als het of natuurlijk gebruikend [ Betaalde regels van de Opsporing van het Onderzoek ](../general/paid-search-detection/paid-search-detection.md) wordt betaald die u hebt gevormd. Een hit wordt als een natuurlijke zoekopdracht beschouwd wanneer deze niet overeenkomt met een betaalde zoekdetectieregels.

Voor de regel voor marketingkanalen gelden de volgende instellingen voor Natuurlijk zoeken:

![](assets/example_natural_search.png)

### Weergave {#display}

Deze regel identificeert bezoekers die afkomstig zijn van banneradvertenties. Deze wordt in dit geval geïdentificeerd door een parameter voor een querytekenreeks in de doel-URL *`Ad_01`* . De de koordparameter van de vraag en de waarden het zoekt worden geëvalueerd als case-insensitive waarden.

![](assets/example_display.png)

### E-mail {#email}

Deze regel identificeert bezoekers die afkomstig zijn van e-mailcampagnes. Deze wordt in dit geval door een parameter van een querytekenreeks in de doel-URL geïdentificeerd: *`eml`*

![](assets/example_email.png)

### Affiliates {#afilliates}

Deze regel identificeert bezoekers die uit een gespecificeerde reeks verwijzende domeinen voortkomen. In de regel geeft u als volgt een overzicht van de domeinen van filialen die u wilt bijhouden:

![](assets/example_affiliates.png)

### Overige campagnes {#other-campaigns}

De beste manier is om een kanaal voor &quot;Overige campagnes&quot; op te nemen volgens alle regels voor betaalkanalen. Dit kanaal fungeert als een &#39;catch-all&#39; voor niet-gecategoriseerd betaald verkeer.

![](assets/other-campaigns.png)

### Sociale netwerken {#social-networks}

Deze regel identificeert bezoekers die afkomstig zijn van een sociaal netwerk, zoals Facebook. De naam van het kanaal wordt vaak gewijzigd in Organic Social. De instellingen kunnen als volgt zijn:

![](assets/example_social.png)

### Intern kanaal (Sessie vernieuwen) {#internal}

Deze regel geldt voor bezoekers waarbij hun verwijzings-URL overeenkomt met de interne URL-filters die in de Admin Console zijn ingesteld. Dit betekent dat de bezoeker van de site is gekomen om zijn bezoek te starten. De naam van dit kanaal wordt vaak gewijzigd in Sessie vernieuwen.

![](assets/int-channel1.png)

Zie [ Redenen voor Intern (Zitting verfrist zich) ](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-faq.html#internal) voor meer informatie over waarom dit kanaal voorkomt.

### Direct {#direct}

Deze regel identificeert bezoekers die geen verwijzend domein hebben, dat bezoekers omvat die rechtstreeks naar uw plaats, zoals van een verbinding van Favorieten of door een verbinding in hun browser te kleven komen. De naam van dit kanaal wordt vaak gewijzigd in Direct getypt/Bladwijzer.

![](assets/example_direct.png)

### Verwijzend kanaal Domeinen {#referring-domains}

Het kanaal Refering Domains identificeert bezoekers die een verwijzend domein hebben. Samen, handelen de Interne, Directe, en Verwijzende domeinkanalen als vangst-allen voor alle resterende klappen die nog niet in een kanaal zijn gecategoriseerd.

![](assets/referring-domains.png)
