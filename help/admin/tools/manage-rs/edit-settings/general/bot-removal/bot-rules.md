---
description: Met beide regels kunt u verkeer verwijderen dat wordt gegenereerd door bekende spinnen en bots uit uw rapportsuite. Door beide verkeer te verwijderen, kunt u de gebruikersactiviteit op uw website nauwkeuriger meten.
title: Begrijp en vorm beide regels
feature: Bot Removal
role: Admin
exl-id: 1c0009f6-2746-4ef1-8dcb-e2693617e91e
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 0%

---

# Begrijp en vorm beide regels

Met beide regels kunt u verkeer verwijderen uit uw rapportsuite die wordt gegenereerd door bekende spinnen en bots. Door beide verkeer te verwijderen, kunt u de gebruikersactiviteit op uw website nauwkeuriger meten.

Nadat beide regels zijn gedefinieerd, wordt al het inkomende verkeer vergeleken met de gedefinieerde regels. Het verkeer dat om het even welk van deze regels aanpast wordt niet verzameld in de rapportreeks en is niet inbegrepen in verkeersmetriek.

Het verwijderen van beide verkeer vermindert typisch het volume van verkeer en omzettingsmetriek. Vele klanten vinden dat het verwijderen van beide verkeer in verhoogde omzettingspercentages en verhogingen van andere bruikbaarheidsmetriek resulteert.

Beide verkeersgegevens worden opgeslagen in een aparte gegevensopslagruimte die kan worden weergegeven in de rapporten Bots en Bot Pages.

>[!NOTE]
>
>Adobe Experience Platform Edge Network verleent de dienst van de a [ botopsporing ](https://experienceleague.adobe.com/docs/experience-platform/datastreams/bot-detection.html) die de etiketten raken die als zijn van bots worden geïdentificeerd. Het botdetectieproces dat in Adobe Analytics wordt gebruikt, is apart en verwijst niet naar de beide scores die zijn opgenomen bij gegevens die via de Edge Network aankomen. De twee systemen gebruiken echter dezelfde IAB-botlijst.

## Beide regels bijwerken of uploaden

>[!IMPORTANT]
>
>Alvorens beide verkeer te verwijderen, moet u met de belanghebbenden communiceren om ervoor te zorgen dat zij als gevolg van deze wijziging de noodzakelijke aanpassingen kunnen aanbrengen in de belangrijkste prestatie-indicatoren. Indien mogelijk, adviseren wij eerst verwijderend beide verkeer van een kleine rapportreeks om de potentiële impact te schatten.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ beide regels ](https://video.tv.adobe.com/v/335738/?quality=12){target="_blank"} voor een demo video vormen.

>[!ENDSHADEBOX]


Om beide regels bij te werken of te uploaden:

1. Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** .

1. Selecteer de rapportsuite waar u beide regels wilt bijwerken en selecteer vervolgens **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Bot Rules]** .

1. Gebruik een van de volgende opties om beide regels voor de rapportsuite bij te werken of te uploaden:

   * Selecteer [!UICONTROL **toelaten IAB Bot het Filtreren Regels**] om bots in Internationale Spinnen &amp; Bots van het Bureau van IAB (Internationale Advertising) te verwijderen om beide verkeer te verwijderen.

     We raden u aan deze optie minimaal te selecteren.

     Voor meer informatie, zie de sectie hieronder, [ StandaardIAB bot regels ](#standard-iab-bot-rules).

   * Selecteer [!UICONTROL **toevoegen Regel**] om de regels van de douanebot te bepalen en toe te voegen die op gebruikersagenten, IP adressen of IP waaiers worden gebaseerd.

     Voor meer informatie, zie de sectie hieronder, [ de botregels van de Douane ](#custom-bot-rules).

   * Naast het [!UICONTROL **Uitgezochte CSV Bot- dossier om**] gebied in te voeren, uitgezocht [!UICONTROL **Dossier**] kiezen, dan het CSV- dossier dat de beide regels bepaalt.

     Voor meer informatie, zie de sectie hieronder, [ uploadt beide regels ](#upload-bot-rules).

1. Selecteer [!UICONTROL **sparen**].

## Standaardregels voor IAB-bot

Standaard IAB-bot-regels kunnen worden ingeschakeld door het selectievakje [!UICONTROL Enable IAB Bot Filtering Rules] in te schakelen. Deze selectie verwijdert bots uit de International Spiders &amp; Bots List van IAB (International Advertising Bureau) om beide verkeer te verwijderen. Adobe werkt deze lijst van de IAB maandelijks bij.

![](/help/admin/tools/manage-rs/edit-settings/general/bot-removal/assets/bot-iab-checkbox.png)

Adobe kan de gedetailleerde IAB-bonenlijst niet aan klanten aanbieden, maar u kunt het Bots-rapport gebruiken om een lijst weer te geven met bots die uw site hebben geopend. Om zowel aan de IAB lijst voor te leggen, bezoek [ IAB ](https://www.iab.com).

Voor informatie over hoe te om standaardIAB bot regels in een rapportreeks toe te laten, zie [ Update of upload beide regels ](#update-or-upload-bot-rules).

## Aangepaste botregels

>[!NOTE]
>
>In de gebruikersinterface kunnen 500 regels handmatig worden gedefinieerd. Nadat deze limiet is bereikt, moeten de regels bulksgewijs worden beheerd via de opties voor het importeren van bestanden en het exporteren van regels.

Met aangepaste botregels kunt u op verkeer gebaseerde voorwaarden die u definieert, filteren. Om met het proces te beginnen om de regels van de douanebot in een rapportreeks toe te laten, zie [ Update of upload beide regels ](#update-or-upload-bot-rules).

De regels voor aangepaste bones worden gedefinieerd met behulp van de volgende voorwaardetypen:

* User Agent
* IP-adres
* IP-bereik

Meerdere voorwaarden kunnen voor één regel worden gedefinieerd. Meerdere voorwaarden komen overeen met &#39;of&#39;. Bijvoorbeeld, als u een waarde voor de Agent van de Gebruiker en IP Adres verstrekt, wordt het verkeer beschouwd als zowel verkeer als één van beide voorwaarde wordt voldaan aan.

### User Agent

Een voorwaarde van de Agent van de Gebruiker controleert de waarde van de gebruikersagent om te zien of controleert het **[!UICONTROL starts with]** of **[!UICONTROL contains]** het gespecificeerde koord. Als **[!UICONTROL contains]** is geselecteerd, komt de subtekenreeks overeen als deze ergens in de gebruikersagent voorkomt.

Optionele waarden kunnen in de lijst **[!UICONTROL does not contain]** worden opgenomen om waarden te definiëren die de gebruikersagent niet mag bevatten voor een geslaagde overeenkomst. U kunt meerdere waarden opgeven door één waarde per regel op te nemen. Als de gebruikersagent aan de criteria voldoet die in het gelijke koord worden gespecificeerd, maar ook een koord op bevat bevat geen lijst, wordt het beschouwd als geen gelijke.

Het veld **[!UICONTROL contains]** mag maximaal 100 tekens bevatten. De lijst bevat geen lijst bevat maximaal 255 tekens min een scheidingsteken voor elke nieuwe regel. (Dit is gelijk aan het aantal tekenreeksen - 1. Als u 4 *specificeert bevat* geen koorden, worden 3 separatorkarakters vereist.) Alle tekenreeksovereenkomsten zijn niet hoofdlettergevoelig.

### IP Adres (met inbegrip van vervangingsgelijken)

Komt een IP adres of veelvoudige adressen in het zelfde blok met vervangingen (&#42;) aan. Geef de numerieke waarden op van het IP-adres dat u wilt afstemmen. Vervang &#42; voor alle waarden die u wilt afstemmen met een jokerteken. De volgende lijst bevat voorbeelden van IP het koord van de adresgelijke:

```
10.10.10.1
10.10.10.*
```

### IP-adresbereik

Verstrek de begin en eindwaaiers van de IP adressen om aan te passen. Vervang &#42; voor alle waarden die u wilt afstemmen met een jokerteken.

### Een aangepaste botregel definiëren

1. Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** , selecteer een of meer rapportsuites en klik op **[!UICONTROL General]** > **[!UICONTROL Bot Rules]** .
1. Klik op **[!UICONTROL Add Rule]** en definieer een of meer overeenkomende voorwaarden.
1. Klik op **[!UICONTROL Save]**. De wijziging moet binnen 30 minuten van kracht worden.

## Boterregels uploaden

Als u beide regels voor bulkimport wilt opgeven, kunt u een CSV-bestand uploaden dat de regels definieert.

1. Om met het proces te beginnen om beide regels aan een rapportreeks te uploaden, zie [ Update of upload beide regels ](#update-or-upload-bot-rules).

1. Maak een CSV-bestand met de volgende kolommen in rij 1 van het werkblad en in de aangegeven volgorde:

   | Kolom 1, rij 1 | Kolom 2, rij 1 | Kolom 3, rij 1 | Kolom 4, rij 1 | Kolom 5, rij 1 | Kolom 6, rij 1 |
   |--- |--- |---|---|---|---|
   | Bot-naam | Beginnen met IP | IP-einde | Regel <br> (bevat of begint met) </br> | Gebruikersagent opnemen | De Uitsluiting van de Agent van de gebruiker <br> (255-karaktergrens) </br> |

   U kunt drie soorten beide regels definiëren:

   * Gebruikersagent bevat of begint met
   * Enkel IP-adres of jokerteken
   * IP-bereik

   Elke rij in het importbestand kan slechts een van de volgende twee definities bevatten:

   >[!NOTE]
   >
   >   Om een bot aan te passen die een combinatie regels gebruikt die met OF (bijvoorbeeld, gebruikersagent of IP adres) worden verbonden, verstrek een identieke naam voor alle regels die u op het gebied van de beide naam wilt combineren. EN overeenkomsten worden niet ondersteund.


   * **de agent van de Gebruiker bevat of begint met**: Verstrek één enkel koord van de gebruikersagent in de Agent omvatten kolom aan te passen. Specificeer het type van gelijke u wilt uitvoeren door *te plaatsen bevat* of *begint met* op het gebied van de Regel van de Overeenkomst van de Agent. Een facultatieve waarde kan in de kolom van de Uitsluiting van de Agent worden omvat die één of meerdere pijp-afgebakende ( `|`) koorden bepaalt die de Agent niet bevat. Tekenreeksovereenkomsten zijn niet hoofdlettergevoelig. Zowel moeten de IP kolommen van het Begin als IP van het Eind leeg zijn.

   * **Enige IP adres of vervangingsgelijke**: Om één enkel IP adres ( `10.10.10.1`) of vervangingsIP adres ( `10.10.*.*`) aan te passen, plaats de zelfde waarde in zowel de IP kolommen van het Begin als van het IP Eind. De Regel van de gelijke, Agent omvat, en de Uitsluiting van de Agent moet leeg zijn.

   * **IP waaiergelijke**: Bepaal een waaier van IP adressen gebruikend de IP kolommen van het Begin en IP van het Eind. Jokertekens kunnen worden gebruikt om IP-bereiken aan te passen, bijvoorbeeld `10.10.10.*` tot en met `10.10.20.*` . De Regel van de gelijke, Agent omvat, en de Uitsluiting van de Agent moet leeg zijn.

1. Op de pagina van de Regels van de Bot in de Manager van de Reeks van het Rapport, naast het [!UICONTROL **Uitgezochte Bot Csv- dossier om**] in te voeren, uitgezocht [!UICONTROL **Dossier**] kiest, dan het Csv- dossier dat de botregels bepaalt die u wilt invoeren.

1. (Optioneel) Schakel het selectievakje **[!UICONTROL Overwrite existing rules]** in om alle bestaande regels te verwijderen en deze te vervangen door de regels die zijn gedefinieerd in het uploadbestand.

1. Selecteer [!UICONTROL **Dossier van de Invoer**].

1. In het [!UICONTROL **gebied van de Reeksen van de Regel**], herzie de regels die werden ingevoerd.

1. Selecteer [!UICONTROL **sparen**].

## Boterbouwregels exporteren

Alle regels die in de gebruikersinterface zijn gedefinieerd, exporteren in een CSV-indeling:

1. Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** .

1. Selecteer de rapportsuite met de beide regels die u wilt exporteren en selecteer vervolgens **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Bot Rules]** .

1. Selecteer **[!UICONTROL Export Bot Rules]** en sla het CSV-bestand op in uw bestandssysteem.

## Gevolgen van beide regels voor gegevensverzameling {#section_F01A3130E7A04A9993371CF26F6586F2}

Beide regels worden toegepast op alle analysegegevens. Gegevens die door Bot Rules zijn verwijderd, zijn alleen zichtbaar in de Boot and Bot Pages Reports.

VISTA-regels worden toegepast na beide regels. Zie [ orde van de Verwerking ](/help/technotes/processing-order.md) in de de gebruikersgids van Technotes.

**de Verwerking van het Bezoek van het Hoog:** als meer dan 100 controles in een bezoek voorkomen, bepaalt het melden als de tijd van het bezoek in seconden minder dan of gelijk aan het aantal controles in het bezoek is. In deze situatie, die te wijten is aan de kosten van het verwerken van lange, intensieve bezoeken, begint de rapportage opnieuw met een nieuw bezoek. Hoog-raakbezoeken worden typisch veroorzaakt door beide aanvallen en worden niet beschouwd als normaal bezoekersbladeren.

>[!NOTE]
>
>Hits duidelijk als *`bots`* worden gefactureerd als [ servervraag.](/help/admin/tools/server-call-usage/overage-overview.md)

## Gevolgen van IP Obfuscatie op bot filtreren {#section_92E60B95BE8940D983F28C79E0CD6B12}

De IAB bot- lijst is uitsluitend gebaseerd op gebruikersagent, zodat wordt het filtreren gebaseerd op die lijst niet beïnvloed door IP verduisteringsmontages. Voor niet-IAB bot filtreren (douaneregels), kan IP deel van de het filtreren criteria uitmaken. Als het filtreren bots gebruikend IP, beide het filtreren gebeurt nadat het laatste octet is verwijderd als dat het plaatsen wordt toegelaten, maar vóór de andere IP verduisteringsopties, zoals het schrappen van volledige IP of het vervangen van het met één of andere unieke identiteitskaart.

Als IP de verwarring wordt toegelaten, gebeurt IP de uitsluiting alvorens het IP adres wordt verduisterd, zodat moeten de klanten om het even wat niet veranderen wanneer zij IP verduistering toelaten.

Als het laatste octet wordt verwijderd, wordt dat gedaan vóór IP het filtreren. Als dusdanig, wordt het laatste octet vervangen met 0, en IP de uitsluitingsregels zouden moeten worden bijgewerkt om IP adressen met nul op het eind aan te passen. Overeenkomende &#42; moet overeenkomen met 0.
