---
title: Veelgestelde vragen over marketingkanalen
description: Veelgestelde vragen over marketingkanalen.
feature: Marketing Channels
exl-id: 6698ef7e-bdac-4b1a-a723-4984e12ce70a
source-git-commit: 2eff7656741bdba3d5d7d1f33e9261b59f8e6083
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# Veelgestelde vragen over marketingkanalen

>[!NOTE]
>
>Om de doeltreffendheid van de Kanalen van de Marketing voor Attributie en Customer Journey Analytics te maximaliseren, hebben wij sommige gepubliceerd [herziene beste praktijken](/help/components/c-marketing-channels/mchannel-best-practices.md).
>
>Analysebeheerders kunnen marketingkanalen voor hun organisaties beheren, zoals beschreven in [Marketingkanalen beheren](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md).

Veelgestelde vragen over marketingkanalen.

## Mijn volgcodes volgen geen patroon en ik heb duizenden die moeten worden gespecificeerd voor mijn kanaal van Verbonden.

* Gebruik het eliminatieproces. Als uw e-mail en gelieerde kanalen dezelfde parameter voor de queryreeks gebruiken, maar u hebt slechts een paar codes voor het bijhouden van e-mail, kunt u de codes voor het bijhouden van e-mail opgeven in een regelset die e-mail definieert. Vervolgens classificeert u alle andere volgcodes met *`affiliates.`*
* Voeg in uw e-mailsysteem een parameter voor de queryreeks toe aan alle bestemmingspagina-URL&#39;s, zoals *`&ch=eml`*. Creeer een regelreeks ontdekt of de parameter van de ch vraag evenaart *`eml`*. Als het geen *`eml`*, dan is het een partner.

## Verwijzende domeinen bevatten meer gegevens dan ik verwacht.

Verwijzende domeinen zouden te hoog in de lijst van de verwerkingsregel kunnen zijn. Het zou één van de laatste (of laatste) regelreeksen moeten zijn, omdat de verwerkingsorde belangrijk is.

## Ik heb een regel gecreeerd die een parameter van het vraagkoord aanpast en het werkt niet.

Controleer of de parameternaam is opgegeven in de parametervelden van de querytekenreeks (meestal een alfanumerieke waarde). Zorg er ook voor dat de parameterwaarde wordt opgegeven na de operator, zoals in het volgende voorbeeld van een e-mailregel wordt getoond.

![](assets/example_email.png)

## Waarom wordt al mijn laatste-aanrakingsverkeer toegeschreven aan een intern domein?

U hebt een regel die intern verkeer aanpast. Houd er rekening mee dat deze regels gelden voor elke hit die een bezoeker op uw site maakt, en niet alleen voor het eerste bezoek. Als je een regel hebt zoals *`Page URL exists`* zonder andere criteria, wordt dat kanaal aangepast op elke volgende hit op uw site, omdat een pagina-URL altijd bestaat.

## Hoe zuivert ik verkeer dat in Geen Kanaal wordt getoond die op het rapport wordt geïdentificeerd?

Regels worden op volgorde verwerkt. Als er geen specifieke criteria zijn gevonden, vallen treffers onder een van de drie categorieën:

1. Geen referentie (een rechtstreeks bezoek).

2. Interne referentie, op de eerste pagina van een bezoek.

3. Een verwerkingsglitch op de pagina.

Zorg ervoor dat u een kanaal voor deze drie mogelijkheden hebt. Maak bijvoorbeeld regels die het volgende aangeven:

1. **[!UICONTROL Referrer]** en **[!UICONTROL Does Not Exist]** en **[!UICONTROL Is First Page of Visit]**. (Zie [Direct.](/help/components/c-marketing-channels/c-faq.md))

2. **[!UICONTROL Referrer Matches Internal URL Filters]** en **[!UICONTROL Is First page of Visit]**. (Zie [Intern](/help/components/c-marketing-channels/c-faq.md).)

3. **[!UICONTROL Referrer]** en **[!UICONTROL Exists]** en **[!UICONTROL Referrer Does Not Match Internal URL Filters]**.

Ten slotte kunt u een *Overige* kanaal dat de resterende klappen, zoals die in wordt beschreven [Geen kanaal geïdentificeerd](/help/components/c-marketing-channels/c-faq.md#no-channel-identified).

## Relatie tussen eerste en laatste aanraking

Als u de interactie tussen oudere eerste en laatste aanraakafmetingen wilt begrijpen en wilt bevestigen dat overschrijvingen naar behoren werken, kunt u een first-touch-kanaalrapport genereren dat is gekoppeld aan een last-touch-kanaalrapport en waarin de maatstaf voor het succes van uw sleutel is toegevoegd (zie het onderstaande voorbeeld). Het voorbeeld demonstreert de interactie tussen eerste en laatste aanraakkanalen.

![](assets/int-channel3.png)

De doorsnede waar de eerste staat gelijk aan de laatste aanraking is de diagonaal van de tabel. Zowel Direct als Sessie vernieuwen krijgen alleen &#39;last-touch&#39;-kredieten als dit ook het eerste aanraakkanaal is, omdat ze geen krediet kunnen halen van andere persisterende kanalen (gemarkeerde rijen).

## Redenen voor Geen kanaal geïdentificeerd {#no-channel-identified}

Wanneer uw regels geen gegevens vangen, of als de regels niet correct worden gevormd, toont het rapport de gegevens in [!UICONTROL No Channel Identified] rij over het rapport. U kunt een regelset maken die *Overige* Aan het einde van uw verwerkingsbestelling bijvoorbeeld geeft dit ook het interne verkeer aan.

![](assets/example_other.png)

Dit soort regel dient als catch-all om ervoor te zorgen dat het kanaalverkeer altijd extern verkeer aanpast, en typisch niet in eindigt **[!UICONTROL No Channel Identified]**. Wees voorzichtig om geen regel te creëren die ook intern verkeer identificeert. De waarde van het kanaal instellen op **[!UICONTROL Referring Domain]** of aan **[!UICONTROL Page URL]** zijn de gemeenschappelijkste, nuttigste manieren om een efficiënte Andere regel tot stand te brengen.

>[!NOTE]
>
>Er zou nog één of ander kanaalverkeer kunnen zijn dat in de Geen Geïdentificeerde categorie van het Kanaal kan vallen. Bijvoorbeeld: een bezoeker komt naar de site en bladwijzers op een pagina en tijdens hetzelfde bezoek komt de pagina via de bladwijzer terug. Aangezien dit niet de eerste pagina van het bezoek is, zal het noch in het Directe kanaal noch in het Andere kanaal gaan omdat er geen verwijzend domein is.

## Redenen voor intern (Sessie vernieuwen) {#internal}

Interne laatste aanraking (Sessie vernieuwen) kan alleen optreden als dit ook de eerste aanraking was. Zie &quot;Relatie tussen eerste en laatste aanraking&quot; hierboven. In de onderstaande scenario&#39;s wordt uitgelegd hoe Zitting vernieuwen een eersteklas kanaal kan zijn.

* **Time-out sessie**: Een bezoeker komt naar de website en laat het tabblad vervolgens open in zijn browser om op een latere datum te gebruiken. De periode van de betrokkenheid van de bezoeker verloopt (of ze verwijderen hun cookies vrijwillig) en ze gebruiken het tabblad Openen om de website opnieuw te bezoeken. Aangezien de verwijzende URL een intern domein is, wordt het bezoek geclassificeerd als Sessie vernieuwen.

* **Niet alle sitepagina&#39;s zijn gelabeld**: Een bezoeker landt op pagina A die niet is gecodeerd en gaat vervolgens naar pagina B die is gecodeerd. Pagina A wordt beschouwd als de interne referentie en het bezoek wordt geclassificeerd als Sessie vernieuwen.

* **Omleiding**: Als een omleiding niet is ingesteld om verwijzingsgegevens door te geven aan de nieuwe landingspagina, gaan de werkelijke gegevens van de invoerverwijzende verwijzing verloren en wordt nu de omleidingspagina (waarschijnlijk een interne pagina) weergegeven als het verwijzende domein. Het bezoek wordt geclassificeerd als Sessie vernieuwen.

* **Domeinoverschrijdend verkeer**: Een bezoeker gaat van het ene domein dat wordt geactiveerd naar Suite A, naar het andere domein dat wordt geactiveerd naar Suite B. Als de interne URL-filters in Suite B het eerste domein bevatten, wordt het bezoek in Suite B geregistreerd als Intern, omdat Marketing Channels het als een nieuw bezoek in de tweede suite zien. Het bezoek wordt geclassificeerd als Sessie vernieuwen.

* **Lange laadtijden van invoerpagina&#39;s**: Een bezoeker landt op pagina A met veel inhoud en de Adobe Analytics-code bevindt zich onder aan de pagina. Voordat alle inhoud (inclusief Adobe Analytics-verzoek om afbeelding) kan worden geladen, klikt de bezoeker op Pagina B. Pagina B wordt de Adobe Analytics-aanvraag voor een afbeelding geactiveerd. Aangezien de afbeeldingsaanvraag van Pagina A nooit is geladen, wordt de tweede pagina weergegeven als de eerste hit van het bezoek in Adobe Analytics, met Pagina A als de referentie. Het bezoek wordt geclassificeerd als Sessie vernieuwen.

* **Cookies wissen halverwege de site**: Een bezoeker komt naar de site en halverwege de sessie worden de cookies gewist. Zowel eerste als laatste-aanraakkanalen worden opnieuw ingesteld en het bezoek wordt geclassificeerd als Sessie vernieuwen (omdat de referentie intern zou zijn).

Hieronder ziet u een voorbeeld van de instelling Interne (verfrissen van sessie) voor zowel eerste als laatste aanraakkanalen:

* Dag 1: de gebruiker komt naar de site op het scherm. Het eerste en laatste aanraakkanaal worden ingesteld op Weergave.
* Dag 2: De gebruiker komt naar de site voor natuurlijk zoeken. First-touch blijft Display en Last touch is ingesteld op Natuurlijk zoeken.
* Dag 35: De gebruiker is niet in 33 dagen naar de site geweest en komt terug gebruikend het lusje dat zij in hun browser open hadden. Ervan uitgaande dat het venster 30 dagen lang geldig is, zou het venster gesloten zijn en zouden de marketingkanaalcookies verlopen zijn. Het eerste aanraak- en laatste aanraakkanaal wordt opnieuw ingesteld en wordt ingesteld op Sessie vernieuwen nadat de gebruiker van een interne URL is gekomen.

## Waarom zijn sommige kanalen onveranderd na het veranderen van de regels van de kanaalverwerking van de Marketing?

Soms worden de de verwerkingsregels van het Kanaal van de Marketing verkeerd opstelling, die het noodzakelijk maken om verwerkingsregels te veranderen. Nadat u de wijzigingen hebt toegepast, kunt u bepaalde metrische gegevens van kenmerken weergeven op een onjuist kanaal. Er zijn verschillende zaken die in overweging moeten worden genomen:

* **Marketing Channel-gegevens worden verzameld in realtime**: Gegevens van marketingkanalen worden verwerkt na gegevensverzameling en zijn 100% permanent. Het wijzigen van de verwerkingsregels heeft geen invloed op gegevens met terugwerkende kracht.
* **Wijzigingen in verwerkingsregels hebben niet onmiddellijk invloed op First Touch-gegevens**: Bijvoorbeeld:
   1. Een gebruiker komt binnen door uw e-mailkanaal omdat het verkeerd opstelling was, dan verlaat uw plaats.
   2. De volgende dag wijzigt u de verwerkingsregel voor e-mail om deze te corrigeren.
   3. Die gebruiker komt een paar dagen later terug door middel van natuurlijke zoekopdracht en koopt een aankoop.
   4. Het e-mailkanaal krijgt First Touch-krediet en natuurlijke zoekopdrachten krijgt Last Touch-creditering.

  Zelfs enkele dagen nadat u de verwerkingsregels hebt gewijzigd, kunnen gegevens nog steeds worden verzameld in het verkeerde First Touch-kanaal. De eerste aanraakgegevens worden voortdurend in het onjuiste kanaal verzameld totdat de betrokkenheid van alle gebruikers verloopt.

De beste manier om deze discrepanties te corrigeren is het doen van een of beide van de volgende maatregelen:

* **Handmatig alle werkingsperioden voor bezoekers verlopen**: Met deze instelling verloopt direct alle eerste en laatste aanraakkanalen door alle bezoekers:
   1. Ga naar Admin Tools > Report Suites.
   2. Houd de muisaanwijzer boven Beeldbewerkingsinstellingen > Marketingkanalen > Vervaldatum betrokkenheid bezoeker
   3. Klik op Alles vervallen.
   4. Klik op OK in het pop-upvenster met waarschuwingen om te bevestigen dat u begrijpt wat het gaat doen.

* **Alleen de metriek Last Touch weergeven vanaf het moment dat u de regels hebt gecorrigeerd**: De maateenheden voor laatste aanraking volgen altijd de huidige regelset. Wanneer u de tijd vanaf het moment waarop u de verwerkingsregels hebt gewijzigd, bekijkt, worden de meest actuele verwerkingsregels correct weergegeven.
