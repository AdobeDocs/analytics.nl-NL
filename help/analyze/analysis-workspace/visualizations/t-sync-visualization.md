---
description: Door visualisatie te synchroniseren kunt u bepalen welke datatabel of gegevensbron overeenkomt met een visualisatie.
keywords: Analysis Workspace;Visualisatie synchroniseren met gegevensbron
title: Visualisatiegegevensbronnen beheren
feature: Visualizations
role: User, Admin
exl-id: 0500b27a-032e-4dc8-98b7-58519ef59368
source-git-commit: 41ac4a97019e8192c96f3cdb141dad3d5db18d12
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# Visualisatiegegevensbronnen beheren {#manage-visualization-data-sources}

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_lockselection"
>title="Selectie vergrendelen"
>abstract="Schakel deze instelling in om de visualisatie te vergrendelen op de geselecteerde posities of op de geselecteerde items in de gegevensbron."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_lockselection_showtable"
>title="Tabel tonen"
>abstract="Als u **[!UICONTROL Show table]** selecteert, wordt een nieuwe gegevensbron voor uw huidige visualisatie gegenereerd, los van de oorspronkelijke gegevensbron."

<!-- markdownlint-enable MD034 -->

Door visualisatie te synchroniseren kunt u bepalen welke datatabel of gegevensbron overeenkomt met een visualisatie.

**Uiteinde:** u kunt zien welke visualisaties door de kleur van de punt naast de titel verwant zijn. Gelijktijdige kleuren betekenen dat visualisaties zijn gebaseerd op dezelfde gegevensbron.

Door een gegevensbron te beheren, kunt u de gegevensbron weergeven of de selectie vergrendelen. Deze instellingen bepalen hoe de visualisatie verandert (of niet verandert) wanneer er nieuwe gegevens binnenkomen.

1. [ creeer een project ](/help/analyze/analysis-workspace/home.md) met een gegevenslijst en a [ visualisatie ](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md).
1. Selecteer in de gegevenstabel de cellen (gegevensbron) die u aan de visualisatie wilt koppelen.
1. Klik in de visualisatie op de stip naast de titel om het dialoogvenster **[!UICONTROL Data Source]** weer te geven. Selecteer **[!UICONTROL Show Data Source]** of **[!UICONTROL Lock Selection]** .

   ![](assets/manage-data-source.png)

   Als u een visualisatie synchroniseert met een tabelcel, wordt een nieuwe (verborgen) tabel gemaakt en wordt de gesynchroniseerde visualisatie met die tabel gekleurd.

## Source-instellingen voor gegevens




>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ de bronmontages van Gegevens ](https://video.tv.adobe.com/v/23729?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


| Element | Beschrijving |
| --- | --- |
| Gekoppelde visualisaties | Als er visualisaties zijn die met een vrije vorm of cohortlijst worden verbonden, opent de top-linker punt om van de aangesloten visualisaties een lijst te maken en een &quot;show&quot;checkbox optie hebben om de lijst te tonen/te verbergen. Als u de muisaanwijzer boven de gekoppelde visualisatie houdt, gaat u naar de gekoppelde visualisatie. |
| Source van gegevens weergeven | Hiermee kunt u (door het selectievakje in te schakelen) of de datatabel die overeenkomt met de visualisatie verbergen (door deze uit te schakelen). |
| Selectie vergrendelen | Schakel deze instelling in om de visualisatie te vergrendelen op de gegevens die momenteel zijn geselecteerd in de corresponderende gegevenstabel. Als deze optie is ingeschakeld, kiest u tussen:<ul><li>**Geselecteerde Plaatsen**: Kies deze optie als u de visualisatie op de posities wilt blijven die in de overeenkomstige gegevenslijst worden geselecteerd. Deze posities blijven zichtbaar, zelfs als de specifieke posten in deze posities veranderen. Kies deze optie bijvoorbeeld als u de vijf belangrijkste campagnemenamen in deze visualisatie altijd wilt weergeven, ongeacht de naam van welke campagne in de bovenste vijf voorkomt.</li><li>**Geselecteerde Punten**: Kies deze optie als u de visualisatie op de specifieke punten wilt blijven die momenteel in de overeenkomstige gegevenslijst worden geselecteerd. Deze items blijven zichtbaar, zelfs als ze een andere positie innemen onder de items in de tabel. Kies deze optie bijvoorbeeld als u in deze visualisatie altijd dezelfde vijf specifieke campagnemenamen wilt weergeven, ongeacht de plaats waar die campagnemenamen staan.</li></ul> |

Deze architectuur verschilt van de vorige omdat Analysis Workspace niet langer een dubbele, verborgen tabel maakt waarin de vergrendelde selectie voor u wordt opgeslagen. De gegevensbron verwijst nu naar de tabel waaruit u de visualisatie hebt gemaakt.

## Voorbeelden van gebruiksgevallen

* U kunt een overzichtsvisualisatie tot stand brengen en het sluiten aan een cel in de lijst u het van creeerde. Wanneer u &quot;Gegevens Source tonen&quot; inschakelt, wordt precies aangegeven waar deze gegevens vandaan komen in de tabel. De brongegevens worden grijs weergegeven:

  ![](assets/data-source2.png)>
* U kunt veel visualisaties toevoegen en deze uit verschillende cellen in dezelfde tabel betrekken, zoals u hier ziet. De tabel is hetzelfde als in het bovenstaande voorbeeld, maar de broncel (en metrisch) zijn anders:

  ![](assets/data-source3.png)>
* U kunt zien of er visualisaties verbonden zijn met een vrije vorm of cohortlijst door de top-left punt (de Montages van Source van Gegevens) te klikken. Als u de muisaanwijzer boven de gekoppelde visualisatie houdt, gaat u naar de gekoppelde visualisatie.

  ![](assets/linked-visualizations.png)>
