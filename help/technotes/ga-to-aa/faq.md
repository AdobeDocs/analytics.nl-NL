---
title: Veelgestelde vragen over migratie naar Adobe Analytics
description: Krijg antwoorden op veelgestelde vragen wanneer u overschakelt van een extern platform naar Adobe.
feature: Third-party Integration
exl-id: 1201909e-b20c-48c5-b287-393da8e22d78
source-git-commit: 58d53d6013abcd7d99f2c3cb640d6a648a4ef360
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 35%

---

# Veelgestelde vragen over migratie naar Adobe Analytics

**Hoe kan ik mijn historische gegevens van mijn derdeplatform aan Adobe Analytics migreren?**

Elk Analytics-platform heeft verschillende manieren om data te verzamelen, te behandelen en op te slaan. In plaats van historische data te migreren raadt Adobe aan een duidelijke grensdatum vast te stellen om te beginnen met het verzamelen en gebruiken van data in Adobe Analytics. Vaak gebruikte grensdata zijn het begin van een boekjaar, het begin van een kalenderjaar of het begin van een kalendermaand. Als gebruikers historische data willen bekijken, kunnen ze zich aanmelden bij het externe platform om een bepaalde historische rapportage te verkrijgen.

Neem contact op met uw Adobe-accountteam als uw organisatie er zeker van is dat historische gegevens naar Adobe worden verzonden. Een implementatieconsultant kan met uw organisatie samenwerken om een Google Analytics-data-export te vertalen naar een databron die kan worden opgenomen door Adobe-servers voor dataverzameling.

Voor het bewegen over historische gegevens moet de aanbeveling [&#x200B; Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-overview) gebruiken die in om het even welke bron van omni-kanaalgegevens kan brengen.

**ik wordt gebruikt aan een segmentatie drop-down lijst in veel van mijn rapporten. Hoe kan ik dat opnieuw maken in [!UICONTROL Analysis Workspace]?**

Drop-down filters zijn een flexibele en robuuste eigenschap in [!UICONTROL Analysis Workspace] die een segmentatie drop-down lijst toestaat. Vanuit een werkruimteproject:

1. Het gebruik ***ctrl*** klikt ***(Vensters) of*** cmd ***+*** klikt ***(Mac) op de componenten die u in de drop-down filter zou willen omvatten.*** U bent niet beperkt tot alleen segmenten. Elke component kan in een vervolgkeuzemenu worden opgenomen.
2. Sleep de groep componenten in het geëtiketteerde werkruimtegebied *Daling een Segment hier*. Houd **[!UICONTROL shift]** ingedrukt voordat u verlaat.

Gebruikers die dit [!UICONTROL Workspace] -project openen, kunnen dit vervolgkeuzefilter gebruiken om segmenten of andere componenten toe te passen op het project. Zie [&#x200B; Overzicht van Panelen &#x200B;](/help/analyze/analysis-workspace/c-panels/panels.md) in de gids van Hulpmiddelen van Adobe Analytics voor meer informatie.

**ik wordt gebruikt om op een afmetingspunt te klikken om een boor te zien. Hoe kan ik die eenvoudige workflow repliceren in de Analysis Workspace?**

Dimension-items in [!UICONTROL Analysis Workspace] beschikken ook over een eenvoudige workflow voor uitsplitsingen. Open de uitsplitsing met behulp van het contextmenu op een dimensie-item. Selecteer vervolgens **[!UICONTROL Breakdown]** en de gewenste component. U kunt de zelfde uitsplitsing op veelvoudige afmetingspunten toepassen door ***ctrl*** + ***te gebruiken uitgezocht*** (Vensters) of ***cmd*** + ***uitgezocht*** (Mac) op elke waarde.
