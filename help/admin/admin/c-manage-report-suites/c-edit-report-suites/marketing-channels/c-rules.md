---
title: Verwerkingsregels voor marketingkanalen
description: De de verwerkingsregels van het Kanaal van de marketing bepalen als een bezoeker voldoet aan de criteria die aan een kanaal worden toegewezen. De regels verwerken elke hit die een bezoeker op uw site aanbrengt. Wanneer een regel niet aan de criteria voor een kanaal voldoet, of als de regels niet correct worden gevormd, wijst het systeem de slag aan Geen Geïdentificeerd Kanaal toe.
feature: Marketing Channels
exl-id: 825f70a5-cce3-4b1c-bb42-828388348216
source-git-commit: b0d264bb8128f805f5bcb194436e357eef4b6987
workflow-type: tm+mt
source-wordcount: '2124'
ht-degree: 1%

---

# Verwerkingsregels voor marketingkanalen

>[!NOTE]
>
> Voor algemene informatie over de Kanalen van de Marketing, zie [Aan de slag met marketingkanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
>
> Om de doeltreffendheid van de Marketing Kanalen voor Attribution IQ en Customer Journey Analytics te maximaliseren, hebben wij sommige gepubliceerd [herziene beste praktijken](/help/components/c-marketing-channels/mchannel-best-practices.md).

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Processing Rules]**.

Regels voor de verwerking van marketingkanalen bepalen of een bezoeker voldoet aan de criteria die aan een kanaal zijn toegewezen door elke hit die een bezoeker op uw site maakt, te verwerken. De regels worden verwerkt in de volgorde die u opgeeft en wanneer aan een regel wordt voldaan, stopt het systeem met het verwerken van de resterende regels.

![](assets/buckets_2.png)

Aanvullende opmerkingen over verwerking:

* De gegevens die met deze regels worden verzameld, zijn 100% permanent en regels die worden gewijzigd nadat gegevens zijn verzameld, zijn niet met terugwerkende kracht. We raden u ten zeerste aan alle omstandigheden te bekijken en in overweging te nemen voordat u het bestand opslaat [!UICONTROL Marketing Channel Processing Rules] om gegevens te beperken die in onjuiste kanalen worden verzameld.
* Het rapport kan tot 25 kanalen tegelijkertijd verwerken.
* De regels kunnen tot variabelen toegang hebben die VISTA heeft geplaatst, maar kunnen tot geen gegevens toegang hebben die VISTA heeft geschrapt.
* Twee marketingkanalen krijgen nooit krediet voor dezelfde gebeurtenis (zoals aankopen of klikken). Op deze manier verschillen de afzetkanalen van eVars (waar twee eVars kredieten voor dezelfde gebeurtenis kunnen ontvangen).
* Als er een hiaatdekking van uw regels is, kunt u zien [Geen kanaal geïdentificeerd.](/help/components/c-marketing-channels/c-faq.md)

## Vereisten

* Bekijk de conceptuele informatie in [Aan de slag met marketingkanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
* Maak een of meer kanalen zodat u er regels aan kunt toewijzen. Zie [Voeg marketingkanalen toe.](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md).
* Bekijk de beste praktijken voor het gebruiken [!UICONTROL Marketing Channels] with [!UICONTROL Attribution IQ].

## Verwerkingsregels voor marketingkanalen maken

Maak verwerkingsregels voor marketingkanalen die bepalen of een bezoeker voldoet aan de criteria die aan een kanaal zijn toegewezen.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
2. Een rapportsuite selecteren.

   Als er in uw rapportsuite geen kanalen zijn gedefinieerd, worden de [!UICONTROL Marketing Channels: Auto Setup] wordt weergegeven.

   Zie [Automatische installatie uitvoeren](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

3. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Processing Rules]**. Als u de automatische opstelling in werking stelde, werden een reeks kanaal en regels automatisch bepaald voor u.

   ![Stap Resultaat](assets/marketing_channel_rules.png)

4. Als u een nieuwe regel wilt toevoegen, selecteert u een van de volgende opties: **[!UICONTROL Add New Rule Set]** -menu. Als u een kanaal selecteert, krijgt u een regelmalplaatje en als u Douane selecteert, begint u van een lege plaats. Met beide opties kunt u de regelset naar wens wijzigen.

   ![Stap Resultaat](assets/example_email.png)

5. Als u regels wilt blijven maken, klikt u op **[!UICONTROL Add New Rule SetRule]**.
6. Als u regels een prioriteit wilt geven, sleept u ze naar de gewenste positie.
7. Klik op **[!UICONTROL Save.]**

Ga verder op deze pagina om aanbevelingen voor de volgorde van de kanaalregels en meer definitievoorbeelden te bekijken.

### De waarde van het marketingkanaal instellen

**[!UICONTROL Set the channel's value]** definieert de detaildimensie van het marketingkanaal die beschikbaar is voor dat kanaal. Hierdoor kunt u de afmetingen van het marketingkanaal afbreken en meer gedetailleerde informatie over het kanaal bekijken.

U wordt aangeraden de kanaalwaarde in te stellen op dezelfde criteria die worden gebruikt om het kanaal zelf te definiëren. Als bijvoorbeeld de parameter van het vraagkoord wordt gebruikt om het kanaal te bepalen, plaats de parameter van het vraagkoord als kanaalwaarde eveneens.

### Regelcriteria

Deze referentietabel definieert de velden, opties en raakkenmerken die u kunt gebruiken om de regels voor de verwerking van marketingkanalen te definiëren.

>[!NOTE]
>
>Elk tekstveld dat u definieert, zoals een querytekenreeksparameter of lijsten met waarden die u wilt gebruiken, worden geëvalueerd als **hoofdlettergevoelig** waarden. Bijvoorbeeld, als u een regel hebt waar de parameter cmp van het vraagkoord = abc123, zullen alle versies van zowel &quot;cmp&quot;als &quot;abc123&quot;de regel aanpassen. U hoeft geen meervoudige hoofdletterversies van deze waarden op te geven.

| Term | Definitie |
|--- |--- |
| Alle | Activeert dit kanaal slechts wanneer alle regels in de genummerde regel waar zijn. |
| Alle | Activeert dit kanaal wanneer om het even welke regels in de regelreeks waar zijn. Deze optie is alleen beschikbaar als de genummerde regel meer dan één regel bevat. |
| AMO-id | De primaire volgcode die wordt gebruikt door de Advertising Cloud- en Advertising Analytics-integratie. Wanneer een van deze integraties is ingeschakeld, kunt u het voorvoegsel van de trackingcode gebruiken om specifieke Advertising Cloud-kanalen te identificeren. Gebruik &#39;AMO-id&#39; om te beginnen met &#39;AL&#39; voor zoeken, &#39;AC&#39; voor weergave of &#39;AO&#39; voor sociaal. Wanneer de AMO-id wordt gebruikt in marketingkanalen, kunnen de maatstaven voor klikken/kosten/indruk worden toegewezen aan het juiste kanaal (wanneer deze niet zijn geconfigureerd, gaan deze meetgegevens naar Direct of Geen). |
| AMO ID | De code voor secundaire tracering die door Advertising Cloud wordt gebruikt. Het belangrijkste doel van deze volgcode is als sleutel te dienen voor het terugsturen van gegevens naar Ad Cloud. Het kan echter ook worden gebruikt om vertoning ClickThroughs vs. display ViewThroughs te identificeren als u deze als twee afzonderlijke marketing kanalen wilt zien. Dit kan worden gedaan door de logica van het marketingkanaal voor &quot;AMO EF ID&quot;einden met &quot;:d&quot;voor Display ClickThroughs of &quot;AMO EF ID&quot;einden met &quot;:i&quot;voor Display ViewThroughs te plaatsen. Als u Weergave niet in twee kanalen wilt splitsen, gebruikt u in plaats daarvan de dimensie AMO-id. |
| Conversievariabelen | Bestaat uit eVars die voor deze rapportsuite zijn ingeschakeld en alleen van toepassing zijn wanneer deze variabelen via de Adobe-code op de pagina zijn ingesteld.  Zie de Implementatiegids. |
| Exists | Er zijn verschillende selecties beschikbaar, waaronder:<ul><li>**Bestaat niet**: Geeft op dat het kenmerk hit niet bestaat in de aanvraag. Als de gebruiker bijvoorbeeld in een verwijzend domein een URL typt of op een bladwijzer klikt, bestaat het kenmerk van het verwijzende domein niet.</li><li>**Is leeg**: Geeft op dat er een hit-kenmerk bestaat, meestal een eVar- of querytekenreeksparameter, maar dat er geen waarde aan het raakkenmerk is gekoppeld.</li><li>**Bevat niet**: Hier kunt u bijvoorbeeld opgeven dat een verwijzend domein geen specifieke waarde bevat (in tegenstelling tot het gebruik van de selectie &quot;Bevat&quot;.)</li></ul> |
| Het kanaal identificeren als | Koppelt de regel aan een marketingkanaal dat u aan de pagina Kanaalbeheer voor marketingdoeleinden hebt toegevoegd.  Zie Marketingkanalen toevoegen. |
| Komt overeen met regels voor betaalde zoekdetectie | Een betaalde zoekopdracht gevonden door Adobe. Betaalde zoekopdrachten worden uitgevoerd wanneer bedrijven kosten betalen voor de zoekfunctie om hun site te kunnen aanbieden. Betaalde zoekopdrachten worden meestal boven of rechts in de zoekresultaten weergegeven. |
| Overeenkomsten met de regels voor natuurlijke zoekdetectie | Een niet-betaalde zoekopdracht aangetroffen door Adobe-rapportage. |
| Referrer komt overeen met interne URL-filters | Een bezoek de waarvan pagina URL een intern filter URL aanpast, zoals die voor de rapportreeks in Hulpmiddelen Admin wordt bepaald. |
| Referrer komt niet overeen met interne URL-filters | De verwijzende URL komt niet overeen met een intern URL-filter, zoals gedefinieerd voor de rapportsuite in Admin Tools. U kunt deze instelling gebruiken met de URL van de pagina en bestaat om een algemene regel voor alle vangsten in te stellen, zodat geen enkele bezoeker aankomt in de sectie Geen kanaal geïdentificeerd van het rapport. |
| Sluiten negeren die overeenkomen met interne URL-filters | (Voor referentie) Tracks komen alleen van extern genoemde sites. Laat deze instelling meestal ingeschakeld, tenzij u intern verkeer wilt opnemen. |
| Is de eerste bezoekpagina | De eerste pagina van een bezoek die wordt gedetecteerd door Adobe-rapportage. |
| Pagina | De paginanaam van een pagina op uw site die is gecodeerd met Adobe van een weboenbaken. Deze waarde is gelijk aan s.pageName. Voorbeelden zijn `Home Page` en `About Us`. |
| Paginadomein | Het domein van de pagina waarop de bezoeker landt, zoals `products.example.co.uk`. |
| Paginadomein en pad | Het domein en pad, zoals `products.example.co.uk/mens/pants/overview.html` . |
| Hoofddomein van pagina (TLD+1) | Het hoofddomein van de pagina waarop de bezoeker landt, zoals example.co.uk. |
| Pagina-URL | De URL van een webpagina op uw site. |
| Referentiedomein | Het domein waar uw bezoekers vandaan kwamen voordat ze uw site bezochten, bijvoorbeeld verwijzingen die afkomstig zijn van `abcsite.com` versus `xyzsite.com`. |
| Parameter querytekenreeks | Als een pagina-URL op uw site er zo uitziet `https://example.com/?page=12345&cat=1`en vervolgens zijn &#39;page&#39; en &#39;cat&#39; beide parameters voor queryreeksen. (Zie `https://en.wikipedia.org/wiki/Query_string`.)  U kunt slechts één parameter van het vraagkoord per regelreeks specificeren. Om extra parameters van het vraagkoord toe te voegen, gebruik `ANY` als uw exploitant, dan voeg nieuwe parameters van het vraagkoord aan de regel toe. Parameters van queryreeksen worden als hoofdlettergevoelig geëvalueerd; Zo zullen &quot;cat&quot; en &quot;CAT&quot; op dezelfde manier worden beoordeeld. |
| Referrer | De locatie van de webpagina (volledige URL) waar uw bezoekers zich bevonden voordat ze naar uw site kwamen. Er bestaat een verwijzing buiten het gedefinieerde domein. |
| Refererend Domein en Weg | Een aaneenschakeling van het Verwijzende Domein en weg URL. Voorbeelden zijn:    `www.example.com/products/id/12345` of `ad.example.com/foo` |
| Verwijzen naar parameter | Een parameter van het vraagkoord op referentie URL. Stel bijvoorbeeld dat uw bezoekers afkomstig zijn van `example.com/?page=12345&cat=1`En dan zijn pagina en kat de verwijzende parameters. |
| Refererend hoofddomein | Het hoofddomein van de referentie. Er bestaat een verwijzing buiten het gedefinieerde domein. |
| Zoekmachine | Een zoekmachine zoals Google of Yahoo! die bezoekers naar uw site bracht. |
| Trefwoorden zoeken | Een woord dat wordt gebruikt om een zoekopdracht uit te voeren met een zoekmachine. |
| Zoekmachine + trefwoorden | Een samenvoeging van het Sleutelwoord van het Onderzoek en de Motor van het Onderzoek om de onderzoeksmotor uniek te identificeren. Als u bijvoorbeeld naar de tekstcomputer zoekt, worden het zoekprogramma en het trefwoord als volgt geïdentificeerd: `Search Tracking Code = "<search_type>:<search engine>:<search keyword>" where    search_type = "n" or "p", search_engine = "Google", and search_keyword = "computer"`**Opmerking:** n = natuurlijk; p = betaald |
| De waarde van het kanaal instellen op | U weet niet alleen welk marketingkanaal een bezoeker naar uw site brengt, maar u kunt ook weten welke banneradvertentie, zoektrefwoord of e-mailcampagne binnen het kanaal krediet opvragen voor de siteactiviteit van een bezoeker. Deze id is een kanaalwaarde die samen met het kanaal wordt opgeslagen. Deze waarde is vaak een campagne-id die is ingesloten in de bestemmingspagina of de verwijzende URL. in andere gevallen is het de zoekengine en combinatie van trefwoorden zoeken, of de verwijzende URL die de bezoeker het meest correct identificeert vanuit een bepaald kanaal. |

## Regelvolgorde en definities van marketingkanalen {#channel-rules}

De kanaalregels worden verwerkt in de volgorde die u opgeeft. Een aanbevolen aanpak voor kanaalbestellingen is om betaalde of beheerde kanalen eerst te plaatsen (bijvoorbeeld betaalde zoekopdrachten, natuurlijke zoekopdrachten, weergave, e-mail), zodat zij kredieten ontvangen, gevolgd door organische kanalen (bijvoorbeeld directe, interne en verwijzende domeinen).

Hieronder ziet u de aanbevolen volgorde voor kanaalregels en voorbeelddefinities:

### Betaalde zoekopdracht {#paid-search}

Betaalde zoekopdracht is een woord of uitdrukking dat u betaalt voor plaatsing in zoekresultaten. Dit kanaal wordt typisch bepaald gebaseerd op de parameter van het vraagkoord (zie het kanaalvoorbeeld van de Vertoning) of betaalde onderzoeksdetectieregels. De beslissing hangt af van de details van het marketingkanaal die u wilt opnemen.

#### Paid search-detectie

Om de betaalde regels van de onderzoeksopsporing aan te passen, gebruikt het marketing kanaal montages die op worden gevormd [!UICONTROL Paid Search Detection] pagina. ( **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Paid Search Detection]**). De doel-URL komt overeen met de bestaande regel voor betaalde zoekdetectie voor dat zoekprogramma.

Voor de regel betreffende het marketingkanaal [!UICONTROL Paid Search] de instellingen zijn als volgt :

![](assets/example_paid_search.png)

Zie [Detectie van betaalde zoekopdracht](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) in Admin voor meer informatie.

### Natuurlijk zoeken {#natural-search}

Een natuurlijk onderzoek komt voor wanneer de bezoekers uw website door een onderzoek van het Web vinden, waar het onderzoeksmotor uw plaats zonder u voor de lijst te betalen rangschikte.

Er is geen natuurlijke onderzoeksopsporing in Analytics. Nadat u de Detectie van het Gesteunde Onderzoek hebt ingesteld, weet het systeem dat als een onderzoeksverwijzer geen betaalde onderzoeksverwijzer was, het een natuurlijke onderzoeksverwijzer moet zijn. Zie [Detectie van betaalde zoekopdracht](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) in Admin voor meer informatie.

Voor de regel voor marketingkanalen gelden de volgende instellingen voor Natuurlijk zoeken:

![](assets/example_natural_search.png)

### Weergave {#display}

Deze regel identificeert bezoekers die afkomstig zijn van banneradvertenties. Het wordt geïdentificeerd door een parameter van het vraagkoord in bestemmingsURL, in dit geval *`Ad_01`*. De de koordparameter van de vraag en de waarden het zoekt worden geëvalueerd als case-insensitive waarden.

![](assets/example_display.png)

### E-mail {#email}

Deze regel identificeert bezoekers die afkomstig zijn van e-mailcampagnes. Het wordt geïdentificeerd door een parameter van het vraagkoord in bestemmingsURL, in dit geval *`eml`*:

![](assets/example_email.png)

### Affiliates {#afilliates}

Deze regel identificeert bezoekers die uit een gespecificeerde reeks verwijzende domeinen voortkomen. In de regel geeft u de domeinen van filialen weer die u wilt bijhouden:

![](assets/example_affiliates.png)

### Overige campagnes {#other-campaigns}

De beste manier is om een kanaal voor &quot;Overige campagnes&quot; op te nemen volgens alle regels voor betaalkanalen. Dit kanaal fungeert als een &#39;catch-all&#39; voor niet-gecategoriseerd betaald verkeer.

![](assets/other-campaigns.png)

### Sociale netwerken {#social-networks}

Deze regel identificeert bezoekers die afkomstig zijn van een sociaal netwerk, zoals Facebook;. De naam van het kanaal wordt vaak gewijzigd in Organic Social. De instellingen kunnen als volgt zijn:

![](assets/example_social.png)

### Intern kanaal (Sessie vernieuwen) {#internal}

Deze regel geldt voor bezoekers waarbij hun verwijzings-URL overeenkomt met de interne URL-filters die in de Admin Console zijn ingesteld. Dit betekent dat de bezoeker van de site is gekomen om zijn bezoek te starten. De naam van dit kanaal wordt vaak gewijzigd in Sessie vernieuwen.

![](assets/int-channel1.png)

Zie [Redenen voor intern (Sessie vernieuwen)](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-faq.html#internal) voor meer informatie over waarom dit kanaal voorkomt.

### Direct {#direct}

Deze regel identificeert bezoekers die geen verwijzend domein hebben, dat bezoekers omvat die rechtstreeks naar uw plaats, zoals van een verbinding van Favorieten of door een verbinding in hun browser te kleven komen. De naam van dit kanaal wordt vaak gewijzigd in Direct getypt/Bladwijzer.

![](assets/example_direct.png)

### Verwijzend kanaal Domeinen {#referring-domains}

Het kanaal Refering Domains identificeert bezoekers die een verwijzend domein hebben. Samen, handelen de Interne, Directe, en Verwijzende domeinkanalen als vangst-allen voor alle resterende klappen die nog niet in een kanaal zijn gecategoriseerd.

![](assets/referring-domains.png)
