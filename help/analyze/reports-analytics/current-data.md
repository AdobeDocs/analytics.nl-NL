---
description: Met de optie Huidige gegevens opnemen in rapporten en analyses kunt u de meest recente analysegegevens weergeven, vaak voordat de gegevens volledig worden verwerkt en voltooid. Met de huidige gegevens worden de meeste meetgegevens binnen enkele minuten weergegeven, zodat u over actiemotionele gegevens beschikt voor snelle besluitvorming.
subtopic: Current Data
title: Huidige data
uuid: 601d3695-be13-4b7f-9df0-de01c8bd64ee
feature: Reports & Analytics Basics
role: User, Admin
exl-id: 4e90f5ad-ba12-4282-a0d9-55765d88104b
source-git-commit: 4ddc2640aa8b3a22411c86ff8bfe0ecf345a3d63
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 1%

---

# Huidige data

{{ra-eol}}

Met de optie Huidige gegevens opnemen in rapporten en analyses kunt u de meest recente analysegegevens weergeven, vaak voordat de gegevens volledig worden verwerkt en voltooid. Met de huidige gegevens worden de meeste meetgegevens binnen enkele minuten weergegeven, zodat u over actiemotionele gegevens beschikt voor snelle besluitvorming.

Het is zichtbaar als optie als deel van de montages van een rapport:

![Huidige gegevensschermafbeelding](assets/current_data.png)

Huidige gegevens worden standaard ingeschakeld in alle rapporten die deze ondersteunen. Als u liever alle metriek wilt weergeven nadat de gegevens volledig zijn verwerkt, hebt u verschillende opties:

* Gebruik Analysis Workspace, dat volledig verwerkte gegevens gebruikt.
* Klik op &#39;Nee&#39; in de huidige instelling voor gegevensrapporten als u alleen volledig verwerkte gegevens wilt gebruiken.
* Verwijder het machtigingsitem &#39;Huidige gegevens&#39; uit een productprofiel in de Admin Console om te voorkomen dat gebruikers die geen beheerder zijn deze optie zien. Zie [Machtigingen voor productprofielen voor Analytics Tools](/help/admin/admin-console/permissions/analytics-tools.md) in de gebruikershandleiding voor Admin voor meer informatie.

Vanwege de prioritering van de beschikbaarheid van gegevens kunnen huidige gegevens momenteel niet worden gebruikt met segmenten, classificaties, indelingen, verf en sommige metriek. Als één van deze eigenschappen wordt gebruikt, worden de huidige gegevens gedwongen aan &quot;Nr&quot;in het rapport en een gele mededeling getoond die verklaart waarom de huidige gegevens niet beschikbaar zijn.

![Huidige gegevensmelding](assets/current_data_notice.png)

## Typische huidige gegevenslatentie

Metrische gegevens worden in een van de volgende drie tijdframes weergegeven. Klik het klokpictogram naast de Include Huidige knevel van Gegevens om de daadwerkelijke latentiewaarde voor elke metrisch op een rapport te zien.

| Tijdschema | Metrics |
| --- | --- |
| Minder dan 10 minuten | Instanties en paginaweergaven van verkeersvariabelen |
| Tussen 10 en 35 minuten | Conversiegebeurtenissen, instanties en paginaweergaven van conversievariabelen |
| Tussen 45 en 120 minuten | Alle andere gegevens, zoals bezoeken, unieke bezoekers en deelname |

Omdat sommige gegevens die op de huidige gegevensmening worden getoond niet volledig zijn verwerkt, kunt u een verschil tussen waarden zien die op de huidige gegevensmening en de gefinaliseerde mening worden gemeld. Bij trended-rapporten ligt het gegevensverschil doorgaans binnen 1%.

## Berekende standaarden

Aangezien berekende metriek kunnen worden tot stand gebracht gebruikend metriek die verschillende latentie hebben, zouden sommige recente waarden kunnen worden berekend gebruikend onvolledige gegevens in de huidige gegevensmening.

U maakt bijvoorbeeld de berekende metrische &#39;paginaweergaven per bezoek&#39; met behulp van de formule `Page Views divided by Visits`. Paginaweergaven worden meestal binnen 10 minuten weergegeven en Bezoekingen worden meestal binnen 2 uur weergegeven. Berekende meetwaarden in dit latentievenster worden berekend aan de hand van onvolledige meetwaarden. Als u een nieuwe pagina plaatst die 4000 hits krijgt van 4000 verschillende bezoeken over een periode van 2 uur, kan het latentieverschil tussen deze metriek onvolledige berekeningen veroorzaken.

Dit gegevensverschil is het meest zichtbaar wanneer nieuwe waarden worden gerapporteerd of korte tijdframes worden gebruikt. Wanneer een rapport langere datumwaaiers gebruikt, zullen de latentieverschillen die in de laatste uren van het melden voorkomen waarschijnlijk geen merkbaar effect op berekende metriek hebben.

Als u metriek hebt berekend die door deze verschillen zouden kunnen worden beïnvloed, of draai huidige gegevens of gebruiksmetriek met het zelfde verwachte latentievenster.

## Gedownloade rapporten

Wanneer u een rapport downloadt met de huidige toegelaten gegevensmening, wordt het rapport een rij gevormd, geproduceerd, en dan teruggekeerd aan browser. Als de gegevens worden verzameld terwijl het rapport produceert, verschijnen die gegevens in het rapport. Dit tijdvenster kan ertoe leiden dat het gedownloade rapport iets meer gegevens heeft.
