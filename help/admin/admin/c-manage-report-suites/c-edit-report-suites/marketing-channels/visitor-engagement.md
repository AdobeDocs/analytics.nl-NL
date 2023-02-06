---
description: Leer hoe u verloopt over betrokkenheid van bezoekers in marketingkanalen.
subtopic: Marketing channels
title: Vervaldatum marketingkanaal
feature: Marketing Channels
exl-id: a9df659b-3b6a-4bdb-bd77-f4490d2b7c79
source-git-commit: 6b216a9af4b5614203b0f34fa754985b12ff59ea
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Vervaldatum marketingkanaal

>[!NOTE]
>
> Voor algemene informatie over de Kanalen van de Marketing, zie [Aan de slag met marketingkanalen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
>
> Om de doeltreffendheid van de Marketing Kanalen voor Attribution IQ en Customer Journey Analytics te maximaliseren, hebben wij sommige gepubliceerd [herziene beste praktijken](/help/components/c-marketing-channels/mchannel-best-practices.md).

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Expiration]**.

Leer hoe u de verloopperiode of de periode voor de betrokkenheid van bezoekers opgeeft voor marketingkanalen.

De betrokkenheid van bezoekers is hoeveel tijd u wilt toestaan dat de vorige activiteit van de bezoeker op uw site wordt toegewezen aan het eerste aanraakkanaal. De standaardvervalinstelling is 30 dagen.

Als de bezoeker de site regelmatig gebruikt, wordt het betrokkenheidsvenster bij de bezoekers weergegeven. Zij moeten 30 dagen inactief zijn voor de periode om te verlopen en kanalen om worden teruggesteld. Zowel het eerste als het laatste aanraakkanaal voor een bezoeker worden opnieuw ingesteld na 30 dagen inactiviteit op die browser.

Voorbeeld:

* Dag 1: Gebruiker komt naar de site op Weergave. Het eerste en laatste aanraakkanaal worden ingesteld op Weergave.
* Dag 2: Gebruiker komt naar de site voor natuurlijk zoeken. First-touch blijft Display en Last touch is ingesteld op Natuurlijk zoeken.
* Dag 35: De gebruiker is niet in 33 dagen naar de site geweest en komt terug met het tabblad dat hij of zij in de browser had geopend. Ervan uitgaande dat het venster 30 dagen lang geldig is, zou het venster gesloten zijn en zouden de marketingkanaalcookies verlopen zijn. Het eerste aanraak- en laatste aanraakkanaal wordt opnieuw ingesteld en wordt ingesteld op Sessie vernieuwen nadat de gebruiker van een interne URL is gekomen.

## Vervalinstellingen voor marketingkanalen

Expiratie-instellingen bestaan uit de volgende instellingen:

| Veld | Definitie |
|--- |--- |
| Dagen van inactiviteit | Het aantal dagen dat moet verstrijken voordat de eerste aanraakactie van een bezoeker verloopt. De standaardwaarde is 30. |
| Nooit | De periode van de betrokkenheid van de bezoeker loopt niet af. |
| Kanaal opnieuw instellen | Verloopt alle perioden voor betrokkenheid van bezoekers.  Als u alle gegevens van het marketingkanaal opnieuw moet instellen, kunt u alle perioden van de betrokkenheid van bezoekers verlopen. Mogelijk moet u gegevens opnieuw instellen als uw verwerkingsregels eerder onjuist zijn geconfigureerd. Alle waarden voor het eerste en laatste aanraakkanaal verlopen onmiddellijk en worden opnieuw ingesteld wanneer bezoekers terugkeren. |

## Vervaldatum van marketingkanalen definiëren {#define-expiration}

Geef de periode voor de betrokkenheid van de bezoeker op.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
2. In de [!UICONTROL Report Suite Manager], klikt u op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Expiration]**.

   ![](assets/mchannel_expiration.png)

3. Configureer de velden voor de periode van de betrokkenheid van bezoekers.
4. Klik op **[!UICONTROL Save.]**
