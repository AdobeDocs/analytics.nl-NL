---
title: Kleine Implementatiecontrole (na elke release van de website)
description: Voer de volgende stappen uit om ervoor te zorgen dat uw implementatie foutloos en in overeenstemming met uw KPI's blijft.
translation-type: tm+mt
source-git-commit: 82064e267729b6995402bd122c6f71b3d38967a3
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# Kleine Implementatiecontrole (na elke release van de website)

Waarom zou u uw implementatie na elke websiteversie moeten herzien? Omdat u er zeker van moet zijn dat de code-updates geen onbedoelde gevolgen hebben en u problemen met de gegevenskwaliteit moet oplossen terwijl deze nog klein zijn. Als u deze kleine revisie altijd uitvoert na elke websiterelease, zult u merken dat uw [grote revisies](/help/implement/review/major-review.md) (elke zes maanden) veel gemakkelijker zijn. U zult ook voorkomen dat kleine problemen groeien in grote gegevenskwesties die het vertrouwen van de belanghebbenden kunnen ondermijnen.

## 1. Hoe beïnvloedde de versie de gegevens voor dat gedeelte van de plaats?

Voer grondige eenheidstests uit: Controleer alle code en variabelen die overeenkomen met de sectie van de site die u net hebt bijgewerkt om te controleren of de nieuwe &#39;tracking&#39; werkt zoals deze is ontworpen.

## 2. De documentatie bijwerken

Werk uw Document van de Vereisten van het Bedrijfs (BRD) en de Verwijzing van het Ontwerp van de Oplossing (SDR) met om het even welke variabelen bij u toevoegde/veranderde om lancering aan te passen.

Beschikt u niet over documentatie over uw implementatie? Exporteer een lijst met variabelen en maak uw OOBH of SDR met [deze sjabloon](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=en#implementation).

## 3. Begin met uw top 5 KPIs

Als u de beste vijf prestatiekernindicatoren (KPI&#39;s) kent, kunt u de bijbehorende maatstaven en dimensies bepalen die u moet onderzoeken. Als u de KPI&#39;s in de afgelopen zes maanden niet hebt vernieuwd of als uw bedrijf nog geen KPI&#39;s heeft gemaakt, volgt u [deze instructies](/help/implement/review/define-kpis.md).

## 4. Werken alle KPI metriek en variabelen nog goed na de versie?

Onthoud dat code-updates onbedoelde gevolgen kunnen hebben. U wilt ervoor zorgen dat alle metriek en afmetingen verbonden aan [uw top 5 KPIs](/help/implement/review/define-kpis.md) nog behoorlijk functioneren. Dit doet u als volgt:

* **Maak dashboards** om de per uur georiënteerde weergaven van deze kritieke metriek en variabelen te zien (u kunt ook intelligente waarschuwingen voor elke metrische waarde instellen) en deze gedurende een dag of twee na de release controleren, om te controleren of u de gegevens die u verwacht krijgt en of de gegevens juist zijn. Zoek buigpunten. Wees bereid om kritieke problemen onmiddellijk op te lossen. Als er discrepanties optreden die er niet goed uitzien, raadpleegt u de gegevenslaag, de regels voor het beheer van tags en de verwerkingsregels om uit te zoeken waarom.
* **Voer het dashboard** Analytics Health opnieuw uit om brede tendensen van uw metriek en variabelen van KPI te controleren.
Lees deze tips van Adobe Analytics Champion Sarah Owen voor meer informatie over hoe u ervoor kunt zorgen dat de statistieken en variabelen goed werken.

## 5. Zijn er hiaten in uw gegevenskwaliteit?

Evalueer de situatie en stel een plan op om de gegevens te corrigeren. Breng vervolgens de gewenste wijzigingen aan, werk de documentatie bij en informeer uw belanghebbenden over de wijzigingen die u hebt aangebracht.

Bekijk deze video van Adobe Analytics Champion Sarah Owen over natuurlijke tijden wanneer u revisies van uw implementatie kunt opnemen in uw drukke planning:

>[!VIDEO](https://video.tv.adobe.com/v/328340/?quality=12&learn=on)
