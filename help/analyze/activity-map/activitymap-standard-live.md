---
description: Activity Map biedt twee basismodi voor aanvullende rapportage van paginaactiviteiten.
title: Standaardmodus versus Live-modus
uuid: 8b97b56e-ff20-4a8b-8c37-7f7b45c9a86b
feature: Activity Map
role: User, Admin
exl-id: 2364e7b0-443a-49a8-b084-403501f52360
source-git-commit: 266cf18050d60f08f7e170c56453d1e1d805cb7b
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 2%

---

# Standaardmodus versus Live-modus

Activity Map biedt twee basismodi voor aanvullende rapportage van paginaactiviteiten.

* Standaardmodus, waarin de [Koppelingen in paginarapport](/help/analyze/activity-map/activitymap-links-report.md)Hiermee worden koppelingsgegevens weergegeven, variërend van één dag tot meerdere dagen, geaggregeerd over het volledige datumbereik.
* In de modus Live wordt de activiteitstrends in real-time weergegeven.

U kunt schakelen tussen de twee modi door op de knop Modus op de werkbalk te klikken.

## Standaardmodus {#section_0C755F30B7EC4A13A62AB9A391AF51E6}

In **Standaardmodus** kunt u het datumbereik op de werkbalk selecteren, zoals hieronder wordt weergegeven.

![](assets/standard_mode.png)

Op deze wijze, worden de metriek van de Handel die geen toegelaten &quot;Deelname&quot;hebben lineair toegewezen. Bijvoorbeeld, laten wij zeggen een gebruiker op een verbinding &quot;IPod mini&quot;op de homepage klikt, dan door 3 meer pagina&#39;s navigeert. Op de vierde pagina, koopt de gebruiker een mini IPod voor $200. De link &#39;IPod mini&#39; ontvangt $200 aan participatieopbrengsten en $50 ($200/4) aan inkomsten (lineair toegewezen inkomsten).

V: Wat gebeurt er als een pagina koppelingen met dezelfde naam in afzonderlijke gebieden bevat? Ontvangen de twee verbindingen afzonderlijk krediet aangezien zij verschillende gebieden maar de zelfde verbindingsnaam op een pagina hebben?

A: Het hangt af van hoe u de koppelingsgegevens samenvoegt. In Activity Map, bekijken wij identiteitskaart|Gebied voor een bepaalde pagina, zodat zouden de toegewezen gegevens voor de &quot;Verbinding ID|Gebied&quot;combinatie zijn. In dit geval, omdat de regio verschilt, zou de link|regio verschillend zijn, en daarom zullen alle toegewezen inkomsten voor de eerste verbinding|regio verschillen van alle toegewezen inkomsten voor de tweede verbinding. Maar in Adobe Analytics UI, kunt u enkel het rapport van identiteitskaart van de verbinding (in plaats van het rapport van de Verbinding|van het Gebied) voor een bepaalde pagina (pagina bekijken die door Verbinding wordt opgesplitst). In dat geval zouden de opbrengsten over beide regio&#39;s worden geaggregeerd.

## Live-modus {#section_D619B77D89A840F0B1C2DEA2715A516A}

In **Live-modus** Analytische gegevens worden in stappen van 1 minuut tot 15 minuten weergegeven. In deze modus gaat het om het analyseren en volgen van trends op de webpagina voor de korte termijn.

De live modus reageert op de behoeften van publicatieorganisaties. Deze organisaties moeten microtrends op koppelingspopulariteit binnen een paar belangrijke pagina&#39;s volgen. De mogelijkheid om snel te zien welke koppelingen ondermaats of heet worden, is van essentieel belang voor uw publicatiebedrijf.

>[!IMPORTANT]
>
>Virtuele rapportsuites zijn niet compatibel met Live-modus, alleen met de standaardmodus.

![](assets/live_mode.png)
