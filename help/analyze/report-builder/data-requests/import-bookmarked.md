---
description: Alle bookmarked rapporten en dashboardrapporten zijn nu vermeld als dimensies in Stap 1 van de Tovenaar van het Verzoek en kunnen als verzoeken van de rapportaannemer worden ingevoerd.
title: Gekoppelde rapporten en dashboardrapporten importeren
topic: Report builder
uuid: 0fdbdb2e-5db7-4f64-b571-23482ba3606d
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Gekoppelde rapporten en dashboardrapporten importeren

Alle bookmarked rapporten en dashboardrapporten zijn nu vermeld als dimensies in Stap 1 van de Tovenaar van het Verzoek en kunnen als verzoeken van de rapportaannemer worden ingevoerd.

Wanneer u een bookmarked rapport selecteert, bevolkt de Tovenaar van het Verzoek alle afmetingen en metriek die dit bookmarked rapport bepalen. Het datumbereik, de granulariteit en het geselecteerde segment worden ook bijgewerkt op basis van de geselecteerde bladwijzer.

Dit is hoe Stap 1 van de Tovenaar van het Verzoek een dashboard en zijn rapporten toont:

![](assets/import_dashboard_reportlet.png)

Wanneer u klikt **[!UICONTROL Retrieve your Dashboards]** of **[!UICONTROL Retrieve your Bookmarks]**, worden uw bestaande dashboard- en/of bladwijzergegevens opgehaald en in het werkblad geplakt.

> [!NOTE] In de Bouwer van het Rapport, is de lijst van beschikbare dashboards en referenties beperkt tot de gebruiker maar ook tot degenen die op de rapportreeks van toepassing zijn u in Stap 1 van de tovenaar selecteerde. In marketingrapporten en -analyses hebt u daarentegen toegang tot alle bladwijzers en dashboards die voor u toegankelijk zijn, ongeacht de rapportsuites die deze dashboard en bladwijzers gebruiken.

> [!NOTE] Alleen gegevens worden geïmporteerd, dus als de bladwijzer een grafiek bevat of als het dashboardrapport alleen uit een grafiek bestaat, worden alleen de gegevens geïmporteerd die worden gebruikt om de grafiek te vullen.

Zodra u een verzoek door een dashboardrapport (of een referentie) in te voeren hebt gecreeerd, zal het verzoek dan aan de primaire dimensie van het rapport (of van de referentie) worden geassocieerd. Als u de aanvraag bewerkt, wordt in de structuurweergave het knooppunt voor de weergave van de rapportboomstructuur van het dashboard (of het knooppunt bladwijzer) niet meer geselecteerd: in plaats daarvan wordt de primaire dimensie geselecteerd .

De geïmporteerde bladwijzerplaat zal de rapportsuite, het geselecteerde segment, de dimensie en de geselecteerde metriek op de juiste wijze instellen voor dezelfde parameters die in de bladwijzer Rapporten &amp; analyse worden weergegeven.

>[!IMPORTANT]
>
>Het datumbereik wordt ingesteld op hetzelfde datumbereik, maar als een statisch datumbereik, zelfs als dit datumbereik een verschuivingsdatumbereik is in de bladwijzer Rapporten en analyse.

