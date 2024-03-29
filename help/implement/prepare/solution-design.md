---
title: Een document voor het ontwerp van een oplossing maken
description: Leer wat een document van het oplossingsontwerp is, en hoe u het in uw organisatie kunt gebruiken.
feature: Implementation Basics
exl-id: 0b5c5ddd-5f53-4790-a649-1381135dacda
role: Admin, Developer, Leader
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Een document voor het ontwerp van een oplossing maken

Een document van het oplossingsontwerp (dat ook als een verwijzing van het oplossingsontwerp of bedrijfsvereisten document wordt bekend) is in wezen de blauwdruk van uw analytische implementatie. Het bepaalt criteria die door belanghebbenden door uw organisatie worden geïdentificeerd, en vertaalt hen aan variabelen binnen Adobe Analytics. Zonder één ding hebben organisaties een moeilijke tijd om de rapportagebehoeften te coördineren en hebben ze de neiging om belangrijke gegevens te verzamelen.

## Vereisten

[Uw analytische implementatie valideren en publiceren naar productie](../launch/validate-publish-prod.md) - Hoewel dit niet rechtstreeks vereist is, beveelt de Adobe aan om een basisimplementatie in te voeren, zodat kritische gegevens worden verzameld terwijl aanvullende bedrijfsvereisten worden vastgesteld en geïmplementeerd.

## Eigendom en locatie van het ontwerpdocument

* **Bepaal wie in uw organisatie verantwoordelijk zal zijn voor het onderhoud van het document van het oplossingsontwerp.** Deze rol kan een individu of een team zijn. Zorg ervoor dat het onderhoud van het oplossingsontwerp wordt bewaard zelfs door rolveranderingen of organisatieherstructureringen. Het is een levend document en moet goed worden onderhouden.
* **Bepaal waar uw oplossingsdocument zal verblijven.** Er is geen enkele beste plaats voor documenten van het oplossingsontwerp om te verblijven, maar zij wonen typisch in een wijd toegankelijke interne plaats. Voorbeelden zijn een gedeeld werkblad of een samenwerkingswerkruimte, zoals SharePoint, of een interne wiki. Het hoeft niet voor iedereen bewerkbaar te zijn, maar het is goed voor degenen die toegang hebben tot de verslaggeving om deze tenminste te kunnen bekijken.

## Bedrijfsvereisten definiëren

Bij het bepalen van welke gegevens moeten worden verzameld, is het gemakkelijk om &quot;alles&quot;te zeggen, nochtans dat snel lastig kan worden te beheren, en zelfs minder waarde kan verstrekken dan het verzamelen van beknoptere hoeveelheden gegevens.

1. **Bepaal uw belangrijkste prestatie-indicatoren.** Wat wil je uiteindelijk dat bezoekers doen? Het antwoord op deze vraag varieert per industrie en verticaal en kan meerdere dingen zijn. Voorbeelden zijn aankopen, registraties of het klikken op advertentie.
1. **Cijfer uit de belangrijkste te verzamelen gegevens.** Stel bedrijfsvragen waarop u specifieke antwoorden wilt. De antwoorden op deze vragen zouden inzicht over hoe te om uw KPI&#39;s te verbeteren verstrekken.
1. **Neem deze vragen en bepaal wat u nodig hebt om te volgen.** Groepeer ze in afmetingen en metriek.
   * Dimensionen zijn variabelen die tekst bevatten. Voorbeelden zijn interne zoekterm, productcategorie of de naam van een gebied waarop een bezoeker heeft geklikt.
   * Metrische gegevens zijn specifieke gebeurtenissen die een bezoeker moet uitvoeren. Wanneer een bezoeker een actie uitvoert die u wilt, wordt het aantal met één verhoogd. Voorbeelden zijn het verzenden van een bestelling, het abonneren op een nieuwsbrief of het indienen van een enquêtereactie.
1. **Wijs afmetingen en metriek in een pagina of een spreadsheet toe.** Deze pagina of tabel wordt uiteindelijk het document van het oplossingsontwerp. Enkele nuttige kolommen of opsommingstekens die moeten worden opgenomen:
   * Implementatiestatus: gepland, actief, inactief, problemen, enzovoort. Dit zou de kijkers van het document op de hoogte brengen van de status van de variabele, als het is uitgevoerd, of als er kwesties met gegevensinzameling zijn.
   * Naam variabele: bijvoorbeeld &quot;Interne zoektermen&quot;. Deze waarde zou zijn wat analisten zien wanneer het werken binnen Analytics.
   * Variabele Analytics toegewezen aan: aan welke standaard- of aangepaste analytische variabele u waarden toewijst. Dimensionen vallen doorgaans onder eVars, terwijl metrische gegevens onder gebeurtenissen vallen.
   * Logic: een beschrijving van hoe de variabele wordt ingesteld en wat de waarde ervan bepaalt. Bijvoorbeeld &quot;Alleen instellen op interne zoekpagina&#39;s. Neemt de waarde van de parameter van het q vraagkoord.&quot;
   * Andere notities die u wilt opnemen met betrekking tot de variabele

## Aanvullende bronnen

Het definiëren van een document voor het ontwerp van een oplossing is een vrij complex project, vooral voor organisaties die er nog geen hebben gemaakt. Als extra hulp gewenst is, verstrekt de Adobe gespecialiseerde advisering om uw organisatie te helpen aan de slag gaan met Adobe Analytics. Neem contact op met het accountteam van de Adobe als u de professionele services van de Adobe wilt inschrijven. A [Technische vragenlijst voorafgaand aan de uitvoering](assets/technical-pre-implementation-questionnaire.pdf) kan worden ingevuld, zodat de Adobe precies weet hoe u kunt helpen op basis van de behoeften van uw organisatie.

Er zijn ook verscheidene partners van de Adobe die zich in het helpen bij de verwezenlijking van een document van het oplossingsontwerp, evenals het uitvoeren van Adobe Analytics op uw plaats specialiseren.

## Volgende stappen

Voer de variabelen in uw document van het oplossingsontwerp uit.

[Een gegevenslaag maken](data-layer.md): Vertaal variabelen in uw ontwerpdocument naar JavaScript-variabelen op uw site.
