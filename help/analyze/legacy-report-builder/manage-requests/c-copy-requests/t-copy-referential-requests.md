---
description: Leer hoe u referentiële verzoeken kopieert.
title: Hoe te om verwijzingsverzoeken te kopiëren
feature: Report Builder
role: User, Admin
exl-id: 3cd77325-7461-4345-a672-64c03ea1ae5b
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Referentieverzoeken kopiëren

{{legacy-arb}}

Een referentiële aanvraag gebruikt waarden uit cellen als invoer voor parameters, zoals een gegevensfilter of relationeel filter.

Om verwijzingsverzoeken in spreadsheet te verspreiden of te kopiëren en te kleven:

* U moet minstens één geldig verzoek in spreadsheet tot stand brengen.

* De gegevens die door het verzoek worden geproduceerd, moeten een cel bevatten waarvan de waarde afhankelijk is van een verzoek in een andere cel (met behulp van een afbraak- of bijpassende filter) of van een filter dat input krijgt van gegevens die in een cel zijn ingevoerd.

U kunt ook aanvragen maken die verwijzen naar invoerfilters van aanvragen in verschillende werkbladen, maar niet naar andere werkboeken. Bijvoorbeeld, kan een verzoek in Blad 2 een rapportreeks van een bepaalde cel in Blad 1 en een datumwaaier van een cel in een verzoek in Blad 2 gebruiken. De nieuwe output kan in één van beide blad of een nieuw blad binnen het zelfde werkboek worden geplaatst. Wanneer u een relatieve aanvraag plakt en een invoerfilter zich op een werkblad bevindt dat afwijkt van het werkblad waarop de gekopieerde aanvraaguitvoer zich bevindt, wordt het filter als een absoluut filter geplakt.

>[!NOTE]
>
>U kunt geen enkele aanvraag uitvoeren in meerdere werkbladen. Bovendien kan het systeem sommige gekopieerde aanvragen niet in nieuwe werkboeken plakken omdat de aanvragen invoerfilters uit andere werkbladen bevatten. Invoerfilters omvatten rapportsuites uit cellen, datumbereiken uit cellen, filters uit cellen en andere gerelateerde parameters.

**om verwijzingsverzoeken te kopiëren**

1. Selecteer de cellen die de aanvragen bevatten die u wilt kopiëren, inclusief de invoercel of de cel waarnaar wordt verwezen.
1. Klik met de rechtermuisknop in de gemarkeerde cellen en selecteer **[!UICONTROL Copy Requests]** in het snelmenu.

   Nadat u het gebied hebt geselecteerd waar aanvragen en invoercellen zich bevinden, markeert het systeem de cellen met deze elementen.
1. Selecteer één cel of een reeks aangrenzende cellen die u wilt vullen met de geplakte aanvragen.

   Controleer of het cel- of celbereik dat u selecteert, geen andere gegevens of aanvragen bevat.
1. Klik met de rechtermuisknop op de enkele cel of op de bovenste cel linksboven in het celbereik en selecteer **[!UICONTROL Paste Requests]** .

   Bij het plakken van aanvragen die een invoercel bevatten, zijn de volgende opties beschikbaar onder [!UICONTROL Paste Requests] :

   **de Absolute Cel van de Input van het Gebruik:** kleeft een exemplaar van het verzoek of de verzoeken en het formatteren verbonden aan de geselecteerde cellen aan het deeggebied u benadrukt. De invoercel (de cel waarnaar in een van de oorspronkelijke aanvragen wordt verwezen) wordt niet geplakt. In plaats daarvan blijft de invoercel op dezelfde positie staan als voorheen.

   **de Relatieve Cel van de Input van het Gebruik:** kleeft een exemplaar van het verzoek of de verzoeken en het formatteren verbonden aan de geselecteerde cellen aan het deeggebied u, met inbegrip van een exemplaar van de inputcel benadrukte. De ruimtelijke relatie tussen de aanvraag(en) en de invoercel is dezelfde als in de oorspronkelijke aanvraag(en). De nieuwe geplakte cellen hebben nu echter een kopie van de aanvragen, maar hebben aanvankelijk geen inhoud. Dit komt doordat er geen gegevens zijn gekoppeld aan de invoercel wanneer de invoercel opnieuw wordt gemaakt tijdens de plakbewerking. Als u gegevens wilt weergeven voor de nieuwe geplakte aanvraag(s), moet u een waarde in de invoercel invoeren en vervolgens de aanvraag(en) vernieuwen.
