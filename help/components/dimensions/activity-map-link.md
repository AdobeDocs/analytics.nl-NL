---
description: De naam van de koppeling waarop is geklikt.
title: Koppeling Activity Mappen
uuid: 67864bf9-33cd-46fa-89a8-4d83d3b81152
feature: Dimensions
role: User, Admin
exl-id: 6aef3a0f-d0dd-4c84-ad44-07b286edbe18
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# Koppeling Activity Mappen

De &quot;Verbinding van de Activity Map&quot;[ dimensie ](overview.md) toont de populairste verbindingen die werden geklikt. U kunt deze dimensie gebruiken om te vergelijken welke verbindingen op uw plaats het meest worden gebruikt, ongeacht waar de verbindingen werden geklikt.

## Deze dimensie vullen met gegevens

Deze afmeting wint gegevens van de [ variabele van contextgegevens ](/help/implement/vars/page-vars/contextdata.md) terug `c.a.activitymap.link`. Als uw implementatie [ Activity Map ](/help/analyze/activity-map/overview.md) gebruikt, verzamelt deze variabele van contextgegevens automatisch gegevens wanneer de verbindingen worden geklikt.

Voor een bepaalde verbinding die werd geklikt, zoekt de Activity Map naar het volgende (in orde):

1. De variabele `s_objectID`
1. De binnentekst van de koppeling
1. Het kenmerk `alt` voor afbeeldingen
1. Het attribuut `title`
1. Het kenmerk `src` voor afbeeldingen
1. Het kenmerk `action` voor formulieren

Als het aangeklikte element geen van bovenstaande criteria bevat, verzamelt de Activity Map geen gegevens voor die klik.

## Dimension-items

Items van een Dimension bevatten de koppelingstekst of andere koppelingskenmerken waarop bezoekers klikken. De sitestructuur en -implementatie van uw organisatie bepalen de exacte verzamelde waarden.
