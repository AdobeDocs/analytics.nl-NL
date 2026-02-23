---
description: Leer hoe time-parting dimensies het tijdstempel van verzamelde gebeurtenissen opstrijken en deze gebeurtenissen opsplitsen in meer betekenisvolle dimensies, zoals Uur van Dag of Dag van Week.
title: Afmetingen van tijd-scheiding
feature: Dimensions
role: User, Admin
exl-id: 92fbcc1e-1f7f-405a-8ad1-199fb7ba505e
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Afmetingen van tijd tot tijd

Het ontleden van de tijd neemt timestamp van verzamelde klappen en breekt het in zinvollere dimensies, zoals **Uur van Dag** of **Dag van Week**.


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; tijd-ontledende dimensies &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-learn/tutorials/analysis-workspace/building-freeform-tables/time-parting-dimensions-in-analysis-workspace){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


De tijd-ontledende dimensies zijn gebaseerd op de tijdzone van de rapportreeks of virtuele rapportreeks. Deze afmetingen zijn beschikbaar in Analysis Workspace en kunnen helpen om de volgende vragen te beantwoorden:

* Wat is, over een groot datumbereik, de populairste tijd van dag voor bezoekers om tot mijn plaats of app toegang te hebben?
* Zijn er dagen van de week of uren van de dag waarop de conversie hoger is op mijn site of app?
* Hoe vergelijk mijn weekendverkopen met mijn weekdagverkopen?
* Produceert een bepaalde marketing campagne hogere omzettingen in de ochtend, of in de namiddag?

>[!NOTE]
>
>De afmetingen voor tijdpartering zijn alleen beschikbaar in Analysis Workspace. Om tijd-ontledende dimensies in andere oplossingen van Analytics te gebruiken, kunt u het [&#x200B; getTimeParting elektrisch toestel &#x200B;](/help/implement/vars/plugins/gettimeparting.md) uitvoeren.

Afmetingen van tijdpartering in Analysis Workspace zijn onder andere:

| Dimension | Voorbeeldwaarden |
| --- | --- |
| Uur van de dag | 0-23 |
| AM/PM | AM, PM |
| Weekdag | Maandag, dinsdag, woensdag, donderdag, vrijdag, zaterdag, zondag |
| Weekend/Weekdag | Weekend, weekdag |
| Dag van Maand | 1-31 |
| Maand van jaar | Januari-december |
| Dag van het Jaar | 1-366 |
| Kwartaal van jaar | Q1, Q2, Q3, Q4 |
