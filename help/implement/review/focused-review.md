---
title: Gerichte revisie (na elke release van de website)
description: Voer de volgende stappen uit om ervoor te zorgen dat uw implementatie foutloos en in overeenstemming met uw KPI's blijft.
feature: Implementation Basics
exl-id: e38f92b6-bd6e-4835-a8e5-0f29ac962066
role: Admin, Leader
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Gerichte revisie (na elke release van de website)

Waarom zou u uw implementatie om de paar maanden moeten herzien? Dus u kunt elk probleem met de gegevenskwaliteit aanpakken terwijl het nog steeds klein is. Als u na elke release van de website deze Gericht revisie consistent uitvoert, zult u zien dat uw tweejaarlijkse [Volledige revisies](/help/implement/review/full-review.md) zijn veel gemakkelijker. U zult ook voorkomen dat kleine problemen groeien in grote gegevenskwesties die het vertrouwen van de belanghebbenden zouden kunnen ondermijnen.

## 1. Begin met uw top 5 KPIs

Als u de beste vijf prestatiekernindicatoren (KPI&#39;s) kent, kunt u de bijbehorende maatstaven en dimensies bepalen die u moet onderzoeken. Als u uw KPIs in de afgelopen 6 maanden niet hebt verfrist of als uw zaken nog geen KPIs hebben gecreeerd, volg [deze instructies](/help/implement/review/define-kpis.md).

## 2. Zorg ervoor dat de KPI-meetgegevens en -variabelen nog steeds goed functioneren

Vergeet niet dat code-updates na verloop van tijd onbedoelde gevolgen kunnen hebben. U wilt ervoor zorgen dat alle metriek en afmetingen verbonden aan uw [top 5 KPI&#39;s](/help/implement/review/define-kpis.md) werkt nog steeds correct. In het ideale geval gebeurt dit direct na een websiterelease. Als u dit de laatste maanden nog niet hebt gedaan, doet u het *now*. Dit doet u als volgt:

* Maak dashboards om per uur trended weergaven van deze kritieke meetgegevens en variabelen weer te geven (of stel ze in) [intelligente waarschuwingen](https://experienceleague.adobe.com/docs/analytics/components/alerts/intellligent-alerts.html) voor elke meeteenheid). Dan controleer hen voor een dag of twee om te verzekeren u de gegevens krijgt u verwacht, en de gegevens zijn correct. Zoek buigpunten. Wees bereid om kritieke problemen onmiddellijk op te lossen. Als u om het even welke discrepanties vindt, kijk in uw gegevenslaag, de regels van de markeringsmanager, en verwerkingsregels om te weten te komen waarom.
* Voer de [Health Dashboard van Analytics](https://express.adobe.com/page/tnNQGNlfzta3b/) om brede tendensen van uw KPI metriek en variabelen te controleren.

*Voor meer details over hoe te om ervoor te zorgen dat uw metriek en variabelen behoorlijk functioneren, [lees deze tips](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/my-five-best-tips-for-keeping-adobe-analytics-humming/td-p/388608) uit Adobe Analytics Champion Sarah Owen.*

## 3. Beoordeel grondig de gegevens uit het bijgewerkte gedeelte van uw site

Zorg ervoor dat de meest recente plaatsversie de gegevensinzameling voor die sectie van de plaats niet ongunstig beïnvloedde: herzie alle code en variabelen die aan die sectie beantwoorden om ervoor te zorgen dat nieuw het volgen zoals ontworpen werkt.

## 4. Werk uw documentatie bij

Als u onlangs metriek of variabelen hebt toegevoegd of veranderd, moet u uw Document van de Vereisten van het Bedrijfs (BRD) en de Verwijzing van het Ontwerp van de Oplossing (SDR) bijwerken.

Als u geen documentatie van uw implementatie hebt, voer een lijst van variabelen uit en creeer uw BRD of SDR gebruikend [deze sjabloon](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html#implementation).

## 5. Verbeter onmiddellijk eventuele leemten in de gegevenskwaliteit die u hebt gevonden

De situatie beoordelen en een plan opstellen om de gegevens te corrigeren. Breng vervolgens de gewenste wijzigingen aan, werk de documentatie bij en informeer uw belanghebbenden over de wijzigingen die u hebt aangebracht.

*Bekijk deze 2-minuten video van Adobe Analytics Champion Sarah Owen over natuurlijke tijden wanneer u revisies van uw implementatie in uw drukke planning kunt passen:*

>[!VIDEO](https://video.tv.adobe.com/v/328340/?quality=12&learn=on)
