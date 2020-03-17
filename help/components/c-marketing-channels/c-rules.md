---
title: Verwerkingsregels voor distributiekanalen
description: De de verwerkingsregels van het Kanaal van de marketing bepalen als een bezoeker voldoet aan de criteria die aan een kanaal worden toegewezen. De regels verwerken elke hit die een bezoeker op uw site aanbrengt. Wanneer een regel niet aan de criteria voor een kanaal voldoet, of als de regels niet correct worden gevormd, wijst het systeem de slag aan Geen Geïdentificeerd Kanaal toe.
translation-type: tm+mt
source-git-commit: c10a12781a8fe52b7b897cd337dc686aa0bbb240

---


# Verwerkingsregels voor distributiekanalen

De de verwerkingsregels van het Kanaal van de marketing bepalen als een bezoeker voldoet aan de criteria die aan een kanaal worden toegewezen. De regels verwerken elke hit die een bezoeker op uw site aanbrengt. Wanneer een regel niet aan de criteria voor een kanaal voldoet, of als de regels niet correct worden gevormd, wijst het systeem de slag aan Geen Geïdentificeerd Kanaal toe.

Hier volgen belangrijke richtlijnen voor het maken van regels:

* Sorteer de regels in de volgorde waarin u ze wilt verwerken.
* Neem aan het einde van de lijst een algemene regel op, bijvoorbeeld Overige. Deze regel identificeert extern verkeer maar niet intern verkeer.

   Zie [Geen kanaal geïdentificeerd.](/help/components/c-marketing-channels/c-faq.md)

> [!NOTE] Hoewel deze regels geen invloed hebben op de rapportage buiten verkoopkanalen, hebben ze wel invloed op de verzameling van gegevens over marketingkanalen. De gegevens die met deze regels worden verzameld, zijn 100% permanent en regels die worden gewijzigd nadat gegevens zijn verzameld, zijn niet met terugwerkende kracht. Het wordt ten zeerste aanbevolen alle omstandigheden te evalueren en in overweging te nemen voordat u gegevens opslaat [!UICONTROL Marketing Channel Processing Rules] om te voorkomen dat gegevens op onjuiste kanalen worden verzameld.

## Vereisten

* Herzie de conceptuele informatie in Aan de [slag met de Kanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md)van de Marketing.
* Maak een of meer kanalen zodat u er regels aan kunt toewijzen. Zie [Markeringskanalen toevoegen.](/help/components/c-marketing-channels/c-channels.md)

## Verwerkingsregels voor marketingkanalen maken

Maak verwerkingsregels voor marketingkanalen die bepalen of een bezoeker voldoet aan de criteria die aan een kanaal zijn toegewezen.

Deze procedure gebruikt een e-mailregel als voorbeeld. In het voorbeeld wordt ervan uitgegaan dat u een e-mailkanaal hebt toegevoegd aan de lijst met kanalen op de pagina Marketing Channel Manager.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Selecteer een rapportsuite.

   Als er in uw rapportsuite geen kanalen zijn gedefinieerd, wordt de [!UICONTROL Marketing Channels: Auto Setup] pagina weergegeven.

   Zie Automatische installatie [uitvoeren](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Processing Rules]**.

   ![Stap resultaat](assets/marketing_channel_rules.png)

1. Selecteer in het **[!UICONTROL Add New Rule Set]** menu de optie **[!UICONTROL Email]**.

   Hier selecteert u niet uw kanaal, maar een malplaatje dat de regel met een paar noodzakelijke parameters bevolkt.

   ![Stap resultaat](assets/example_email.png)

   Gebruik de Booleaanse logica (if / then statements) om een regel te configureren. Geef in een e-mailkanaalregel bijvoorbeeld de instellingen of informatie op die in de volgende regelinstructie wordt benadrukt:

   `"If **[!UICONTROL All]** or **[!UICONTROL Any]** of the following are true:  **[!UICONTROL Query String Parameter]** *<value>* **[!UICONTROL exists]**...`

   `"Then identify the channel as **[!UICONTROL Email]**...`

   `"Then set the channel's value to **[!UICONTROL Query String Parameter]** *<value>*."`

   In dit voorbeeld *`<value>`* is de parameter van het vraagkoord dat u voor uw e-mailcampagne, zoals *`eml`*. gebruikt.
1. Klik op **[!UICONTROL Add Rule]** om door te gaan met het maken van regels.
1. Als u regels een prioriteit wilt geven, sleept u ze naar de gewenste positie.
1. Klik op **[!UICONTROL Save.]**

>[!MORELIKETHIS]
>
>* [Veelgestelde vragen en voorbeelden](/help/components/c-marketing-channels/c-faq.md)


## Criteria voor de regel voor marketingkanalen

In deze referentietabel worden de velden, opties en raakkenmerken gedefinieerd die u kunt selecteren op de pagina Verwerkingsregels marketingkanaal.

| Term | Definitie |
|--- |--- |
| Alles | Activeert dit kanaal slechts wanneer alle regels in de genummerde regel waar zijn. |
| Alle | Activeert dit kanaal wanneer om het even welke regels in de regelreeks waar zijn. Deze optie is alleen beschikbaar als de genummerde regel meer dan één regel bevat. |
| AMO-id | De primaire trackingcode die wordt gebruikt door de integratie van Advertising Cloud en Advertising Analytics. Wanneer een van deze integraties is ingeschakeld, kunt u het voorvoegsel van de trackingcode gebruiken om specifieke kanalen voor advertenties in de cloud te identificeren. Gebruik &#39;AMO-id&#39; om te beginnen met &#39;AL&#39; voor zoeken, &#39;AC&#39; voor weergave of &#39;AO&#39; voor sociaal. Wanneer de AMO-id wordt gebruikt in marketingkanalen, kunnen de maatstaven voor klikken/kosten/indruk worden toegewezen aan het juiste kanaal (wanneer deze niet zijn geconfigureerd, gaan deze meetgegevens naar Direct of Geen). |
| AMO ID | De code voor secundaire tracering die wordt gebruikt door Advertising Cloud. Het belangrijkste doel van deze code is om als sleutel te dienen voor het terugsturen van gegevens naar Ad Cloud. Het kan echter ook worden gebruikt om vertoning ClickThroughs vs. display ViewThroughs te identificeren als u deze als twee afzonderlijke marketing kanalen wilt zien. Dit kan worden gedaan door de logica van het marketingkanaal voor &quot;AMO EF ID&quot;einden met &quot;:d&quot;voor Display ClickThroughs of &quot;AMO EF ID&quot;einden met &quot;:i&quot;voor Display ViewThroughs te plaatsen. Als u Weergave niet in twee kanalen wilt splitsen, gebruikt u in plaats daarvan de dimensie AMO-id. |
| Conversievariabelen | Bestaat uit eVars die voor deze rapportsuite zijn ingeschakeld en alleen van toepassing zijn wanneer deze variabelen via de Adobe-code op de pagina zijn ingesteld.  Zie de Implementatiegids. |
| Exists | Er zijn verschillende selecties beschikbaar, waaronder:<ul><li>**Bestaat niet**: Geeft op dat het kenmerk hit niet bestaat in de aanvraag. Als de gebruiker bijvoorbeeld in een verwijzend domein een URL typt of op een bladwijzer klikt, bestaat het kenmerk van het verwijzende domein niet.</li><li>**Is leeg**: Geeft op dat er een hit-kenmerk bestaat, meestal een eVar- of querytekenreeksparameter, maar dat er geen waarde aan het raakkenmerk is gekoppeld.</li><li>**Bevat** niet: Hier kunt u bijvoorbeeld opgeven dat een verwijzend domein geen specifieke waarde bevat (in tegenstelling tot het gebruik van de selectie &quot;Bevat&quot;.)</li></ul> |
| Het kanaal identificeren als | Koppelt de regel aan een marketingkanaal dat u aan de pagina Kanaalbeheer voor marketingdoeleinden hebt toegevoegd.  Zie Marketingkanalen toevoegen. |
| Komt overeen met regels voor betaalde zoekdetectie | Een betaalde zoekopdracht gevonden door Adobe. Betaalde zoekopdrachten worden uitgevoerd wanneer bedrijven kosten betalen voor de zoekfunctie om hun site te kunnen aanbieden. Betaalde zoekopdrachten worden meestal boven of rechts in de zoekresultaten weergegeven. |
| Overeenkomsten met de regels voor natuurlijke zoekdetectie | Een niet-betaalde zoekopdracht gevonden door Adobe-rapportage. |
| Referrer komt overeen met interne URL-filters | Een bezoek de waarvan pagina URL een intern filter URL aanpast, zoals die voor de rapportreeks in Hulpmiddelen Admin wordt bepaald. |
| Referrer komt niet overeen met interne URL-filters | De verwijzende URL komt niet overeen met een intern URL-filter, zoals gedefinieerd voor de rapportsuite in Admin Tools. U kunt deze instelling gebruiken met de URL van de pagina en bestaat om een algemene regel voor alle vangsten in te stellen, zodat geen enkele bezoeker aankomt in de sectie Geen kanaal geïdentificeerd van het rapport. |
| Sluiten negeren die overeenkomen met interne URL-filters | (Voor referentie) Tracks komen alleen van extern genoemde sites. Laat deze instelling meestal ingeschakeld, tenzij u intern verkeer wilt opnemen. |
| Is de eerste bezoekpagina | De eerste pagina van een bezoek die door Adobe wordt gedetecteerd. |
| Pagina | De paginanaam van een webpagina op uw site die is gecodeerd met het webbaken van Adobe. Deze waarde is gelijk aan s.pageName. Voorbeelden zijn `Home Page` en `About Us`. |
| Paginadomein | Het domein van de pagina waarop de bezoeker landt, zoals `products.example.co.uk`. |
| Paginadomein en pad | Het domein en pad, zoals `products.example.co.uk/mens/pants/overview.html` . |
| Hoofddomein van pagina (TLD+1) | Het hoofddomein van de pagina waarop de bezoeker landt, zoals example.co.uk. |
| Pagina-URL | De URL van een webpagina op uw site. |
| Referentiedomein | Het domein waar uw bezoekers vandaan kwamen voordat ze uw site bezochten, bijvoorbeeld verwijzingen die afkomstig waren van `abcsite.com` versus `xyzsite.com`. |
| Parameter querytekenreeks | Als een pagina-URL op uw site er zo uitziet `https://example.com/?page=12345&cat=1`, zijn pagina en cat beide parameters voor de queryreeks. (Zie `https://en.wikipedia.org/wiki/Query_string`.)  U kunt slechts één parameter van het vraagkoord per regelreeks specificeren. Om extra parameters van het vraagkoord toe te voegen, gebruik `ANY` als uw exploitant, dan voeg nieuwe parameters van het vraagkoord aan de regel toe. |
| Referenter | De locatie van de webpagina (volledige URL) waar uw bezoekers zich bevonden voordat ze naar uw site kwamen. Er bestaat een verwijzing buiten het gedefinieerde domein. |
| Refererend Domein en Weg | Een aaneenschakeling van het Verwijzende Domein en weg URL. Voorbeelden zijn:    `www.example.com/products/id/12345` of `ad.example.com/foo` |
| Verwijzen naar parameter | Een parameter van het vraagkoord op referentie URL. Als uw bezoekers bijvoorbeeld van `example.com/?page=12345&cat=1`herkomst zijn, zijn pagina en kat de verwijzende parameters. |
| Refererend hoofddomein | Het hoofddomein van de referentie. Er bestaat een verwijzing buiten het gedefinieerde domein. |
| Zoekmachine | Een zoekmachine zoals Google of Yahoo! die bezoekers naar uw site bracht. |
| Trefwoorden zoeken | Een woord dat wordt gebruikt om een zoekopdracht uit te voeren met een zoekmachine. |
| Zoekmachine + trefwoorden | Een samenvoeging van het Sleutelwoord van het Onderzoek en de Motor van het Onderzoek om de onderzoeksmotor uniek te identificeren. Als u bijvoorbeeld naar de tekstcomputer zoekt, worden het zoekprogramma en het trefwoord als volgt geïdentificeerd: `Search Tracking Code = "<search_type>:<search engine>:<search keyword>" where    search_type = "n" or "p", search_engine = "Google", and search_keyword = "computer"`**Opmerking:**n = natuurlijk; p = betaald |
| De waarde van het kanaal instellen op | U weet niet alleen welk marketingkanaal een bezoeker naar uw site brengt, maar u kunt ook weten welke banneradvertentie, zoektrefwoord of e-mailcampagne binnen het kanaal krediet opvragen voor de siteactiviteit van een bezoeker. Deze id is een kanaalwaarde die samen met het kanaal wordt opgeslagen. Deze waarde is vaak een campagne-id die is ingesloten in de bestemmingspagina of de verwijzende URL. in andere gevallen is het de zoekengine en combinatie van trefwoorden zoeken, of de verwijzende URL die de bezoeker het meest correct identificeert vanuit een bepaald kanaal. |

## Intern kanaal (Sessie vernieuwen)

Het interne kanaal (dat vaak wordt hernoemd naar Sessievernieuwen) bestaat uit bezoeken aan de site waar de verwijzende URL overeenkomt met de instelling voor interne URL-filters in de beheerconsole. Dit houdt in dat de bezoeker van de site is gekomen om zijn bezoek te starten.

![](assets/int-channel1.png)

### Beste werkwijzen overschrijven

U kunt het beste de optie last-touch negeren uitschakelen voor Direct en Intern kanaal, zodat ze geen krediet kunnen opnemen van andere hardnekkige laatste aanraakkanalen (of van elkaar).

>[!NOTE]In dit document wordt ervan uitgegaan dat voor Direct vernieuwen en Sessie de optie Negeren is uitgeschakeld.

![](assets/int-channel2.png)

### Betrokkenheidsperiode

Zowel het eerste als het laatste aanraakkanaal voor een bezoeker worden opnieuw ingesteld na 30 dagen inactiviteit op die browser.

>[!NOTE] De standaardinstelling is 30 dagen en u kunt deze indien nodig wijzigen met de beheerinstellingen.

Als de bezoeker de site regelmatig gebruikt, wordt het betrokkenheidsvenster bij de bezoekers weergegeven. Zij moeten 30 dagen inactief zijn voor de periode om te verlopen en kanalen om worden teruggesteld.
Voorbeeld:

* Dag 1: Gebruiker komt naar de site op Weergave. Het eerste en laatste aanraakkanaal worden ingesteld op Weergave.

* Dag 2: Gebruiker komt naar de site voor natuurlijk zoeken. First-touch blijft Display en Last touch is ingesteld op Natuurlijk zoeken.

* Dag 35: De gebruiker is niet in 33 dagen naar de site geweest en komt terug met het tabblad dat hij of zij in de browser had geopend. Ervan uitgaande dat het venster 30 dagen lang geldig is, zou het venster gesloten zijn en zouden de marketingkanaalcookies verlopen zijn. Het eerste aanraak- en laatste aanraakkanaal wordt opnieuw ingesteld en wordt ingesteld op Sessie vernieuwen nadat de gebruiker van een interne URL is gekomen.

### Relatie tussen eerste en laatste aanraking

Als u de interactie tussen eerste en laatste aanraking wilt begrijpen en wilt bevestigen dat overschrijvingen naar behoren werken, kunt u een first-touch-kanaalrapport genereren dat is gekoppeld aan een last-touch-kanaalrapport en waarin uw belangrijkste succesmetrische parameter is toegevoegd (zie het onderstaande voorbeeld). Het voorbeeld demonstreert de interactie tussen eerste en laatste aanraakkanalen.

![](assets/int-channel3.png)

Het snijpunt waar het eerste staat gelijk aan het laatste aanraakpunt wordt oranje gemarkeerd. Zowel Direct als Sessie vernieuwen krijgen alleen &#39;last-touch&#39;-kredieten als dit ook het eerste aanraakkanaal is, omdat ze geen krediet kunnen halen van andere hardnekkige kanalen (gemarkeerde rijen in grijs).

### Waarom wordt de sessie vernieuwd?

Aangezien we weten dat verversen van sessie met laatste aanraking alleen kan plaatsvinden als dit ook de eerste aanraking was, wordt in de onderstaande scenario&#39;s uitgelegd hoe Vernieuwen van sessie een eersteklas kanaal kan zijn.

**Scenario 1: Time-out sessie**

Een bezoeker komt naar de website en laat het tabblad vervolgens open in zijn browser om op een latere datum te gebruiken. De periode van de betrokkenheid van de bezoeker verloopt (of ze verwijderen hun cookies vrijwillig) en ze gebruiken het tabblad Openen om de website opnieuw te bezoeken. Aangezien de verwijzende URL een intern domein is, wordt het bezoek geclassificeerd als Sessie vernieuwen.

**Scenario 2: Niet alle sitepagina&#39;s zijn gelabeld**

Een bezoeker landt op pagina A die niet is getagd en gaat vervolgens naar pagina B die is getagd. Pagina A wordt beschouwd als de interne referentie en het bezoek wordt geclassificeerd als Sessie vernieuwen.

**Scenario 3: Omleiding**

Als een omleiding niet is ingesteld om verwijzingsgegevens door te geven aan de nieuwe landingspagina, gaan de werkelijke gegevens van de invoerverwijzende verwijzing verloren en wordt nu de omleidingspagina (waarschijnlijk een interne pagina) weergegeven als verwijzend domein. Het bezoek wordt geclassificeerd als Sessie vernieuwen.

**Scenario 4: Domeinoverschrijdend verkeer**

Een bezoeker beweegt zich van één domein dat aan Reeks A, aan een tweede domein in brand steekt dat aan Reeks B. Als de interne URL-filters in Suite B het eerste domein bevatten, wordt het bezoek in Suite B geregistreerd als Intern, omdat Marketing Channels het als een nieuw bezoek in de tweede suite zien. Het bezoek wordt geclassificeerd als Sessie vernieuwen.

**Scenario 5: Lange laadtijden van invoerpagina**

Een bezoeker landt op Pagina A die zwaar is op inhoud, en de code van de Analyse van Adobe wordt gevestigd bij de bodem van de pagina. Voordat alle inhoud (inclusief de aanvraag voor een Adobe Analytics-afbeelding) kan worden geladen, klikt de bezoeker op Pagina B. Pagina B wordt geactiveerd wanneer Adobe Analytics een afbeeldingsaanvraag indient. Aangezien de afbeeldingsaanvraag van Pagina A nooit is geladen, wordt de tweede pagina weergegeven als de eerste hit van het bezoek in Adobe Analytics, waarbij Pagina A de verwijzende persoon is. Het bezoek wordt geclassificeerd als Sessie vernieuwen.

**Scenario 6: Cookies wissen halverwege de site**

Een bezoeker komt naar de site en halverwege de sessie worden de cookies gewist. Zowel eerste als laatste aanraakkanalen worden opnieuw ingesteld en het bezoek wordt geclassificeerd als Sessie vernieuwen (omdat de referentie intern zou zijn).
