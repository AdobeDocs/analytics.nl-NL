---
title: Een document voor het ontwerp van een oplossing maken
description: Leer wat een document van het oplossingsontwerp is, en hoe u het in uw organisatie kunt gebruiken.
translation-type: tm+mt
source-git-commit: 283fcd5832abe4c09caa332c2ebc3a22029e6707

---


# Een document voor het ontwerp van een oplossing maken

Een document van het oplossingsontwerp (dat ook als een verwijzing van het oplossingsontwerp of bedrijfsvereisten document wordt bekend) is in wezen de blauwdruk van uw analytische implementatie. De code definieert criteria die door belanghebbenden in uw hele organisatie worden geïdentificeerd en zet deze om in variabelen in Adobe Analytics. Zonder één ding hebben organisaties een moeilijke tijd om de rapportagebehoeften te coördineren en hebben ze de neiging om belangrijke gegevens te verzamelen.

## Vereisten

[Valideer uw analytische implementatie en publiceer deze naar de productie](../launch/validate-publish-prod.md) - Hoewel dit niet rechtstreeks vereist is, raadt Adobe aan een basisimplementatie op te zetten, zodat kritieke gegevens worden verzameld terwijl aanvullende bedrijfsvereisten worden vastgesteld en geïmplementeerd.

## Eigendom en locatie van het ontwerpdocument

* **Bepaal wie in uw organisatie verantwoordelijk zal zijn voor het onderhoud van het document van het oplossingsontwerp.** Deze rol kan een individu of een team zijn. Zorg ervoor dat het onderhoud van het oplossingsontwerp wordt bewaard zelfs door rolveranderingen of organisatieherstructureringen. Het is een levend document en moet goed worden onderhouden.
* **Bepaal waar uw oplossingsdocument zal verblijven.** Er is geen enkele beste plaats voor documenten van het oplossingsontwerp om te verblijven, maar zij wonen typisch in een wijd toegankelijke interne plaats. Voorbeelden zijn een gedeeld spreadsheet of een samenwerkingswerkruimte zoals SharePoint of een interne wiki. Het hoeft niet voor iedereen bewerkbaar te zijn, maar het is goed voor degenen die toegang hebben tot de verslaggeving om deze tenminste te kunnen bekijken.

## Bedrijfsvereisten definiëren

Bij het bepalen van welke gegevens moeten worden verzameld, is het gemakkelijk om &quot;alles&quot;te zeggen, nochtans dat snel lastig kan worden te beheren, en zelfs minder waarde kan verstrekken dan het verzamelen van beknoptere hoeveelheden gegevens.

1. **Bepaal uw belangrijkste prestatie-indicatoren.** Wat wil je uiteindelijk dat bezoekers doen? Het antwoord op deze vraag varieert per industrie en verticaal en kan meerdere dingen zijn. Voorbeelden zijn aankopen, registraties of het klikken op advertentie.
1. **Cijfer uit de belangrijkste te verzamelen gegevens.** Stel bedrijfsvragen waarop u specifieke antwoorden wilt. De antwoorden op deze vragen zouden inzicht over hoe te om uw KPI&#39;s te verbeteren verstrekken.
1. **Neem deze vragen en bepaal wat u nodig hebt om te volgen.** Groepeer ze in afmetingen en metriek.
   * Dimensies zijn variabelen die tekst bevatten. Voorbeelden zijn interne zoekterm, productcategorie of de naam van een gebied waarop een bezoeker heeft geklikt.
   * Metrische gegevens zijn specifieke gebeurtenissen die een bezoeker moet uitvoeren. Wanneer een bezoeker een actie uitvoert die u wilt, wordt het aantal met één verhoogd. Voorbeelden zijn het verzenden van een bestelling, het abonneren op een nieuwsbrief of het indienen van een enquêtereactie.
1. **Wijs afmetingen en metriek in een pagina of een spreadsheet toe.** Deze pagina of tabel wordt uiteindelijk het document van het oplossingsontwerp. Enkele nuttige kolommen of opsommingstekens die moeten worden opgenomen:
   * Implementatiestatus: Gepland, actief, inactief, problemen enzovoort. Dit zou de kijkers van het document de status van de variabele informeren, als het is uitgevoerd, of als er kwesties met gegevensinzameling zijn.
   * Naam variabele: Bijvoorbeeld &#39;Interne zoektermen&#39;. Deze waarde zou zijn wat analisten zien wanneer het werken binnen Analytics.
   * Variabele Analytics toegewezen aan: Aan welke standaard- of aangepaste analytische variabele u waarden wilt toewijzen. Dimensies vallen doorgaans onder eVars, terwijl metrische gegevens onder gebeurtenissen vallen.
   * Logica: Een beschrijving van hoe de variabele wordt geplaatst, en wat zijn waarde bepaalt. Bijvoorbeeld &quot;Alleen instellen op interne zoekpagina&#39;s. Neemt de waarde van de parameter van het q vraagkoord.&quot;
   * Eventuele andere notities die u wilt opnemen met betrekking tot de variabele

## Aanvullende bronnen

Het definiëren van een document voor het ontwerp van een oplossing is een vrij complex project, vooral voor organisaties die er nog geen hebben gemaakt. Als u meer hulp nodig hebt, biedt Adobe u gespecialiseerd advies om uw organisatie aan de slag te krijgen met Adobe Analytics. Neem contact op met uw accountmanager als u de professionele services van Adobe wilt inschrijven. Er kan een vragenlijst [voor de](assets/technical-pre-implementation-questionnaire.pdf) technische pre-implementatie worden ingevuld, zodat Adobe precies weet hoe u hulp kunt bieden op basis van de behoeften van uw organisatie.

Er zijn ook verschillende Adobe-partners die gespecialiseerd zijn in het maken van een document voor het ontwerpen van oplossingen en het implementeren van Adobe Analytics op uw site.

## Volgende stappen

Voer de variabelen in uw document van het oplossingsontwerp uit.

[Een gegevenslaag](data-layer.md)maken: Vertaal variabelen in uw ontwerpdocument naar JavaScript-variabelen op uw site.
