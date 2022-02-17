---
title: Gerichte revisie (na elke release van de website)
description: Voer de volgende stappen uit om ervoor te zorgen dat uw implementatie foutloos en in overeenstemming met uw KPI's blijft.
feature: Implementation Basics
exl-id: e38f92b6-bd6e-4835-a8e5-0f29ac962066
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Gerichte revisie (na elke release van de website)

Waarom zou u uw implementatie om de paar maanden moeten herzien? Dus u kunt elk probleem met de gegevenskwaliteit aanpakken terwijl het nog steeds klein is. Als u na elke release van de website deze Focus Review consistent uitvoert, zult u zien dat uw tweejaarlijkse [Volledige revisies](/help/implement/review/full-review.md) zijn veel gemakkelijker. U zult ook voorkomen dat kleine problemen groeien in grote gegevenskwesties die het vertrouwen van de belanghebbenden kunnen ondermijnen.

## 1. Begin met uw top 5 KPIs

Als u de beste vijf prestatiekernindicatoren (KPI&#39;s) kent, kunt u de bijbehorende maatstaven en dimensies bepalen die u moet onderzoeken. Als u de KPI&#39;s in de afgelopen zes maanden niet hebt vernieuwd of als uw bedrijf nog geen KPI&#39;s heeft gemaakt, volgt u [deze instructies](/help/implement/review/define-kpis.md).

## 2. Zorg ervoor uw metriek van KPI en variabelen nog goed functioneert

Vergeet niet dat code-updates na verloop van tijd onbedoelde gevolgen kunnen hebben. U wilt ervoor zorgen dat alle metriek en afmetingen verbonden aan uw [top 5 KPI&#39;s](/help/implement/review/define-kpis.md) functioneert nog steeds naar behoren. In het ideale geval moet dit onmiddellijk na een websiterelease gebeuren. als u dit de afgelopen maanden nog niet hebt gedaan, doet u het *now*. Dit doet u als volgt:

* Maak dashboards om per uur trended weergaven van deze kritieke meetgegevens en variabelen weer te geven (of stel ze in) [intelligente waarschuwingen](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/intelligent-alerts/intellligent-alerts.html#analysis-workspace) voor elke metrieke waarde). Controleer de gegevens vervolgens gedurende een of twee dagen om te controleren of u de gegevens ontvangt die u verwacht en of de gegevens juist zijn. Zoek buigpunten. Wees bereid om kritieke problemen onmiddellijk op te lossen. Als u om het even welke discrepanties vindt, kijk in uw gegevenslaag, de regels van de markeringsmanager, en verwerkingsregels om te weten te komen waarom.
* Voer de [Health Dashboard van Analytics](https://assets.adobe.com/public/9549dbe7-765a-4899-77b8-85cbba1a4252) om brede tendensen van uw KPI metriek en variabelen te controleren.

*Voor meer informatie over hoe te om ervoor te zorgen uw metriek en variabelen behoorlijk functioneren, [lees deze tips](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/my-five-best-tips-for-keeping-adobe-analytics-humming/td-p/388608) uit Adobe Analytics Champion Sarah Owen.*

## 3. Beoordeel grondig de gegevens uit het bijgewerkte gedeelte van uw site

Zorg ervoor dat de meest recente plaatsversie de gegevensinzameling voor die sectie van de plaats niet negatief beïnvloedde: bekijk alle code en variabelen die aan die sectie beantwoorden om ervoor te zorgen dat het nieuwe volgen zoals ontworpen werkt.

## 4. De documentatie bijwerken

Als u onlangs metriek of variabelen hebt toegevoegd of veranderd, moet u uw Document van de Vereisten van het Bedrijfs (BRD) en de Verwijzing van het Ontwerp van de Oplossing (SDR) bijwerken.

Als u geen documentatie over de implementatie hebt, exporteert u een lijst met variabelen en maakt u een OOBH of SDR met [deze sjabloon](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=en#implementation).

## 5. Verbeter onmiddellijk eventuele tussenruimten in de gegevenskwaliteit

Evalueer de situatie en stel een plan op om de gegevens te corrigeren. Breng vervolgens de gewenste wijzigingen aan, werk de documentatie bij en informeer uw belanghebbenden over de wijzigingen die u hebt aangebracht.

*Bekijk deze 2-minuten video van Adobe Analytics Champion Sarah Owen over natuurlijke tijden wanneer u revisies van uw implementatie in uw drukke planning kunt passen:*

>[!VIDEO](https://video.tv.adobe.com/v/328340/?quality=12&learn=on)
