---
title: Veelgestelde vragen over marketingkanalen
description: Veelgestelde vragen over marketingkanalen.
translation-type: tm+mt
source-git-commit: 7c722e361978a3d7517e95c23442b703e7e25270
workflow-type: tm+mt
source-wordcount: '1310'
ht-degree: 0%

---


# Veelgestelde vragen over marketingkanalen

Veelgestelde vragen over marketingkanalen.

## Mijn volgcodes volgen geen patroon en ik heb duizenden die moeten worden gespecificeerd voor mijn kanaal van Verbonden.

* Gebruik het eliminatieproces. Als uw e-mail en gelieerde kanalen dezelfde parameter voor de queryreeks gebruiken, maar u hebt slechts een paar codes voor het bijhouden van e-mail, kunt u de codes voor het bijhouden van e-mail opgeven in een regelset die e-mail definieert. Vervolgens classificeert u alle andere volgcodes met *`affiliates.`*
* Voeg in uw e-mailsysteem een parameter voor de querytekenreeks toe aan alle bestemmingspagina-URL&#39;s, zoals *`&ch=eml`* de URL. Maak een regelset die detecteert of de parameter voor de query gelijk is *`eml`*. Als het niet bevat *`eml`*, is het een gelieerde.

## Verwijzende domeinen bevatten meer gegevens dan ik verwacht.

* Verwijzende domeinen zouden te hoog in de lijst van de verwerkingsregel kunnen zijn. Het zou één van de laatste (of laatste) regelreeksen moeten zijn, omdat de verwerkingsorde belangrijk is.

## Ik heb een regel gecreeerd die een parameter van het vraagkoord aanpast en het werkt niet.

* Controleer of de parameternaam is opgegeven in de parametervelden van de querytekenreeks (meestal een alfanumerieke waarde). Zorg er ook voor dat de parameterwaarde wordt opgegeven na de operator, zoals in het volgende voorbeeld van een e-mailregel wordt getoond.

   ![](assets/example_email.png)

## Waarom wordt al mijn laatste-aanrakingsverkeer toegeschreven aan een intern domein?

* U hebt een regel die intern verkeer aanpast. Houd er rekening mee dat deze regels gelden voor elke hit die een bezoeker op uw site maakt, en niet alleen voor het eerste bezoek. Als u een regel hebt zoals *`Page URL exists`* zonder andere criteria, komt dat kanaal overeen op elke volgende hit op uw site, omdat een pagina-URL altijd bestaat.

## Hoe zuivert ik verkeer dat in Geen Kanaal wordt getoond die op het rapport wordt geïdentificeerd?

* Regels worden op volgorde verwerkt. Als er geen specifieke criteria zijn gevonden, vallen treffers onder een van de drie categorieën:

1. Geen referentie (een rechtstreeks bezoek).

2. Interne referentie, op de eerste pagina van een bezoek.

3. Een verwerkingsglitch op de pagina.

Zorg ervoor dat u een kanaal voor deze drie mogelijkheden hebt. Maak bijvoorbeeld regels die het volgende aangeven:

1. **[!UICONTROL Referrer]** en **[!UICONTROL Does Not Exist]** en **[!UICONTROL Is First Page of Visit]**. (Zie [Direct.](/help/components/c-marketing-channels/c-faq.md))

2. **[!UICONTROL Referrer Matches Internal URL Filters]** en **[!UICONTROL Is First page of Visit]**. (Zie [Intern](/help/components/c-marketing-channels/c-faq.md).)

3. **[!UICONTROL Referrer]** en **[!UICONTROL Exists]** en **[!UICONTROL Referrer Does Not Match Internal URL Filters]**.

Ten slotte maakt u een *ander* kanaal waarmee de resterende resultaten worden vastgelegd, zoals wordt beschreven in [Geen kanaal geïdentificeerd](/help/components/c-marketing-channels/c-faq.md#no-channel-identified).

## Relatie tussen eerste en laatste aanraking

Als u de interactie tussen oudere eerste en laatste aanraakafmetingen wilt begrijpen en wilt bevestigen dat overschrijvingen naar behoren werken, kunt u een first-touch-kanaalrapport genereren dat is gekoppeld aan een last-touch-kanaalrapport en waarin de maatstaf voor het succes van uw sleutel is toegevoegd (zie het onderstaande voorbeeld). Het voorbeeld demonstreert de interactie tussen eerste en laatste aanraakkanalen.

![](assets/int-channel3.png)

De doorsnede waar de eerste staat gelijk aan de laatste aanraking is de diagonaal van de tabel. Zowel Direct als Sessie vernieuwen krijgen alleen &#39;last-touch&#39;-kredieten als dit ook het eerste aanraakkanaal is, omdat ze geen krediet kunnen halen van andere persisterende kanalen (gemarkeerde rijen).

## Redenen voor Geen kanaal geïdentificeerd {#no-channel-identified}

Wanneer uw regels geen gegevens vangen, of als de regels niet correct worden gevormd, toont het rapport de gegevens in de [!UICONTROL No Channel Identified] rij op het rapport. U kunt een regelreeks tot stand brengen genoemd *Andere*, bijvoorbeeld, aan het eind van uw verwerkingsorde, die ook intern verkeer identificeert.

![](assets/example_other.png)

Dit soort regel dient als catch-all om ervoor te zorgen dat het kanaalverkeer altijd extern verkeer aanpast, en typisch niet omhoog in **[!UICONTROL No Channel Identified]**. Wees voorzichtig om geen regel te creëren die ook intern verkeer identificeert. Het plaatsen van de waarde van het kanaal aan **[!UICONTROL Referring Domain]** of aan **[!UICONTROL Page URL]** zijn de gemeenschappelijkste, nuttigste manieren om een efficiënte Andere regel tot stand te brengen.

>[!NOTE]
>
>Er zou nog wat kanaalverkeer kunnen zijn dat in de Geen Geïdentificeerde categorie van het Kanaal kan vallen. Bijvoorbeeld: Een bezoeker komt naar de site en bladwijzers op een pagina en tijdens hetzelfde bezoek komt de pagina via de bladwijzer terug. Aangezien dit niet de eerste pagina van het bezoek is, zal het noch in het directe kanaal noch in het andere kanaal gaan omdat er geen verwijzend domein is.

## Redenen voor intern (Sessie vernieuwen) {#internal}

Vernieuwen van laatste aanraaksessie kan alleen plaatsvinden als dit ook de eerste aanraking was. Zie &quot;Verhouding tussen eerste en laatste aanraking&quot; hierboven. In de onderstaande scenario&#39;s wordt uitgelegd hoe Zitting vernieuwen een eersteklas kanaal kan zijn.

* **Time-out** sessie: Een bezoeker komt naar de website en laat het tabblad vervolgens open in zijn browser om op een latere datum te gebruiken. De periode van de betrokkenheid van de bezoeker verloopt (of ze verwijderen hun cookies vrijwillig) en ze gebruiken het tabblad Openen om de website opnieuw te bezoeken. Aangezien de verwijzende URL een intern domein is, wordt het bezoek geclassificeerd als Sessie vernieuwen.

* **Niet alle sitepagina&#39;s zijn gecodeerd**: Een bezoeker landt op pagina A die niet is getagd en gaat vervolgens naar pagina B die is getagd. Pagina A wordt beschouwd als de interne referentie en het bezoek wordt geclassificeerd als Sessie vernieuwen.

* **Omleiding**: Als een omleiding niet is ingesteld om verwijzingsgegevens door te geven aan de nieuwe landingspagina, gaan de werkelijke gegevens van de invoerverwijzende verwijzing verloren en wordt nu de omleidingspagina (waarschijnlijk een interne pagina) weergegeven als verwijzend domein. Het bezoek wordt geclassificeerd als Sessie vernieuwen.

* **Domeinoverschrijdend verkeer**: Een bezoeker beweegt zich van één domein dat aan Reeks A, aan een tweede domein in brand steekt dat aan Reeks B. Als de interne URL-filters in Suite B het eerste domein bevatten, wordt het bezoek in Suite B geregistreerd als Intern, omdat Marketing Channels het als een nieuw bezoek in de tweede suite zien. Het bezoek wordt geclassificeerd als Sessie vernieuwen.

( **Lange laadtijden** van invoerpagina: Een bezoeker landt op pagina A die zwaar is op inhoud, en de code van Adobe Analytics wordt gevestigd bij de bodem van de pagina. Voordat alle inhoud (inclusief Adobe Analytics-afbeeldingsaanvraag) kan worden geladen, klikt de bezoeker op Pagina B. Pagina B activeert de Adobe Analytics-afbeeldingsaanvraag. Aangezien de afbeeldingsaanvraag van Pagina A nooit is geladen, wordt de tweede pagina weergegeven als de eerste hit van het bezoek in Adobe Analytics, met Pagina A als de referentie. Het bezoek wordt geclassificeerd als Sessie vernieuwen.

* **Cookies wissen halverwege de site**: Een bezoeker komt naar de site en halverwege de sessie worden de cookies gewist. Zowel eerste als laatste aanraakkanalen worden opnieuw ingesteld en het bezoek wordt geclassificeerd als Sessie vernieuwen (omdat de referentie intern zou zijn).

## Waarom zijn sommige kanalen onveranderd na het veranderen van de regels van de kanaalverwerking van de Marketing?

Soms worden de de verwerkingsregels van het Kanaal van de Marketing verkeerd opstelling, die het noodzakelijk maken om verwerkingsregels te veranderen. Nadat u de wijzigingen hebt toegepast, kunt u bepaalde metrische gegevens van kenmerken weergeven op een onjuist kanaal. Er zijn verschillende zaken die in overweging moeten worden genomen:

* **De gegevens van het Kanaal van de marketing worden verzameld in echt - tijd**: De het kanaalgegevens van de marketing worden verwerkt bij gegevensinzameling, en is 100% permanent. Het wijzigen van de verwerkingsregels heeft geen invloed op gegevens met terugwerkende kracht.
* **Het wijzigen van de verwerkingsregels heeft niet onmiddellijk invloed op First Touch-gegevens**: Bijvoorbeeld:
   1. Een gebruiker komt binnen door uw e-mailkanaal omdat het verkeerd opstelling was, dan verlaat uw plaats.
   2. De volgende dag wijzigt u de verwerkingsregel voor e-mail om deze te corrigeren.
   3. Die gebruiker komt een paar dagen later terug door middel van natuurlijke zoekopdracht en koopt een aankoop.
   4. Het e-mailkanaal krijgt First Touch-krediet en natuurlijke zoekopdrachten krijgt Last Touch-creditering.

   Zelfs enkele dagen nadat u de verwerkingsregels hebt gewijzigd, kunnen gegevens nog steeds worden verzameld in het verkeerde First Touch-kanaal. De eerste aanraakgegevens worden voortdurend in het onjuiste kanaal verzameld totdat de betrokkenheid van alle gebruikers verloopt.

De beste manier om deze discrepanties te corrigeren is het doen van een of beide van de volgende maatregelen:

* **Handmatig verlopen alle perioden** voor betrokkenheid van bezoekers: Deze instelling vervalt ogenblikkelijk alle eerste en laatste aanraakkanalen voor alle bezoekers:
   1. Ga naar Admin Tools > Report Suites.
   2. Houd de muisaanwijzer boven Beeldbewerkingsinstellingen > Marketingkanalen > Vervaldatum betrokkenheid bezoeker
   3. Klik op Alles vervallen.
   4. Klik op OK in het pop-upvenster met waarschuwingen om te bevestigen dat u begrijpt wat het gaat doen.

* **Alleen de maatstaven voor laatste aanraking weergeven vanaf het moment dat u de regels hebt gecorrigeerd**: Metrische gegevens voor laatste aanraking volgen altijd de huidige regels. Wanneer u de tijd vanaf het moment waarop u de verwerkingsregels hebt gewijzigd, bekijkt, worden de meest actuele verwerkingsregels correct weergegeven.
