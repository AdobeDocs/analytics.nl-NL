---
title: Gerichte revisie (na elke release van de website)
description: Voer de volgende stappen uit om ervoor te zorgen dat uw implementatie foutloos en in overeenstemming met uw KPI's blijft.
feature: Implementation Basics
exl-id: e38f92b6-bd6e-4835-a8e5-0f29ac962066
role: Admin, Leader
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Gerichte revisie (na elke release van de website)

Waarom zou u uw implementatie om de paar maanden moeten herzien? Dus u kunt elk probleem met de gegevenskwaliteit aanpakken terwijl het nog steeds klein is. Als u constant dit Gerichte Overzicht na elke websiteversie doet, zult u vinden dat uw tweejaarlijkse [ Volledige Revisies ](/help/implement/review/full-review.md) veel gemakkelijker zijn. U zult ook voorkomen dat kleine problemen groeien in grote gegevenskwesties die het vertrouwen van de belanghebbenden zouden kunnen ondermijnen.

## 1. Begin met uw top 5 KPIs

Als u de beste vijf prestatiekernindicatoren (KPI&#39;s) kent, kunt u de bijbehorende maatstaven en dimensies bepalen die u moet onderzoeken. Als u uw KPIs in de laatste 6 maanden niet hebt verfrist of als uw zaken nog geen KPIs hebben gecreeerd, volg [ deze instructies ](/help/implement/review/define-kpis.md).

## 2. Zorg ervoor dat de KPI-meetgegevens en -variabelen nog steeds goed functioneren

Vergeet niet dat code-updates na verloop van tijd onbedoelde gevolgen kunnen hebben. U wilt ervoor zorgen dat alle metriek en dimensies verbonden aan uw [ top 5 KPIs ](/help/implement/review/define-kpis.md) nog behoorlijk functioneren. Ideaal gezien, wordt dit gedaan direct na een websiteversie; als u het niet in de laatste paar maanden hebt gedaan, doe het *nu*. Dit doet u als volgt:

* Creeer dashboards om per uur trended meningen van deze kritieke metriek en variabelen (of opstelling [ alarm ](https://experienceleague.adobe.com/docs/analytics/components/alerts/intellligent-alerts.html?lang=nl-NL) voor elke metrisch) te zien. Dan controleer hen voor een dag of twee om te verzekeren u de gegevens krijgt u verwacht, en de gegevens zijn correct. Zoek buigpunten. Wees bereid om kritieke problemen onmiddellijk op te lossen. Als u om het even welke discrepanties vindt, kijk in uw gegevenslaag, de regels van de markeringsmanager, en verwerkingsregels om te weten te komen waarom.
* Herstel het [ Dashboard van de Gezondheid van de Analyse ](https://express.adobe.com/page/tnNQGNlfzta3b/) om brede tendensen van uw metriek en variabelen van KPI te controleren.

*voor meer details over hoe te ervoor te zorgen dat uw metriek en variabelen behoorlijk functioneren, [ leest deze uiteinden ](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/my-five-best-tips-for-keeping-adobe-analytics-humming/td-p/388608) van Adobe Analytics Champion Sarah Owen.*

## 3. Beoordeel grondig de gegevens uit het bijgewerkte gedeelte van uw site

Zorg ervoor dat de meest recente plaatsversie de gegevensinzameling voor die sectie van de plaats niet ongunstig beïnvloedde: herzie alle code en variabelen die aan die sectie beantwoorden om ervoor te zorgen dat nieuw het volgen zoals ontworpen werkt.

## 4. Werk uw documentatie bij

Als u onlangs metriek of variabelen hebt toegevoegd of veranderd, moet u uw Document van de Vereisten van het Bedrijfs (BRD) en de Verwijzing van het Ontwerp van de Oplossing (SDR) bijwerken.

Als u geen documentatie van uw implementatie hebt, voer een lijst van variabelen uit en creeer uw BRD of SDR gebruikend [ dit malplaatje ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=nl-NL#implementation).

## 5. Verbeter onmiddellijk eventuele leemten in de gegevenskwaliteit die u hebt gevonden

De situatie beoordelen en een plan opstellen om de gegevens te corrigeren. Breng vervolgens de gewenste wijzigingen aan, werk de documentatie bij en informeer uw belanghebbenden over de wijzigingen die u hebt aangebracht.

*bekijk deze 2 minieme video van Adobe Analytics Champion Sarah Owen over natuurlijke tijden wanneer u revisies van uw implementatie in uw bezige programma kunt passen:*


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ die uw implementatie ](https://video.tv.adobe.com/v/3440175?quality=12&learn=on&captions=dut){target="_blank"} voor een demo video herzien.

>[!ENDSHADEBOX]


