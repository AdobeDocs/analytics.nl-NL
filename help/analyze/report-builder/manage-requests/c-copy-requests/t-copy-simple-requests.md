---
description: Leer hoe u een eenvoudige aanvraag kopieert.
title: Hoe te om eenvoudige verzoeken te kopiëren
uuid: ff20560a-01ee-47e7-8bd1-b73edb010456
feature: Report Builder
role: User, Admin
exl-id: ceed28d5-cb7f-4343-96fd-2ce09f5a3515
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Eenvoudige aanvragen kopiëren

Kopieer een eenvoudig verzoek in plaats van een referentieverzoek. Een eenvoudig verzoek is een verzoek dat geen verwijzingen naar een ander verzoek of de inhoud van een cel bevat.

A [referentieverzoek](/help/analyze/report-builder/manage-requests/c-copy-requests/t-copy-referential-requests.md) gebruikt waarden uit cellen als invoer voor parameters, zoals een gegevensfilter of relationeel filter. Deze filters gebruiken of aanpassing of trending en zijn gebaseerd op resultaten van een voorafgaand verzoek of op de user-entered inhoud van een cel, genoemd een inputcel.

Een eenvoudige aanvraag kopiëren

1. Maak een geldige aanvraag.
1. Klik met de rechtermuisknop op een van de cellen waar de aanvraag is toegewezen of selecteer een gebied met cellen met aanvragen.

   Wees consistent wanneer u een cel kiest waaruit u wilt kopiëren in de groep cellen die onder het verzoek valt. De voorkeurskeuze is de bovenste en meest linkse cel van de set cellen waarop de aanvraag betrekking heeft en die van links naar rechts werkt. Dit komt omdat het spreadsheet van Excel honderden kolommen en duizenden rijen beschikbaar voor juiste en neerwaartse uitbreiding heeft. Als u toch besluit een aanvraagkopie te starten van de cel uiterst rechts of onderaan in een set cellen die aan een aanvraag zijn gekoppeld, staat het systeem u niet toe om de aanvraag te plakken als de cellen die moeten worden geplakt zich voorbij de linker- of bovenrand van de spreadsheet bevinden.
1. Selecteren **[!UICONTROL Copy Request]**.
1. Klik in een ander gedeelte van het spreadsheet met de rechtermuisknop op een lege cel (een cel die geen verzoek bevat).

   U kunt voorkomen dat al gemaakte aanvragen verloren gaan of worden beschadigd, door cellen met aanvragen te plakken naar cellen die momenteel zijn toegewezen aan een aanvraag. Als u cellen met verzoeken kopieert of knipt, wordt met het snelmenu het volgende gedaan: [!UICONTROL Paste Requests] Deze optie is beschikbaar wanneer u met de rechtermuisknop klikt op cellen (of de set cellen) die verzoeken bevatten. U moet een andere cel selecteren als het doel van de plakbewerking, zodat aanvragen elkaar niet overlappen. Dit geldt ongeacht of u één cel selecteert met een verzoek om te plakken of een gebied cellen met verzoeken.
1. Klik op **[!UICONTROL Paste Request]**.

   Een kopie van de oorspronkelijke aanvraag wordt in de cel(len) geplaatst, op een positie of op posities ten opzichte van de oorspronkelijke aanvraag.

   >[!NOTE]
   >
   >Alleen aanvragen worden gekopieerd, niet de inhoud van de cellen. Als u andere informatie hebt die niet op verzoeken wordt gebaseerd, maar relevant voor het begrijpen van de gegevens die in de cellen (zoals de kopballen van de lijstkolom of rijherkenningstekens) worden getoond, gebruik de standaardopdrachten van Excel Exemplaar en Deeg.

   Omdat Excel verschillende klemborden voor het kopiëren van celinhoud en het kopiëren van verzoeken gebruikt, kunt u zowel niet-verzoekcelinhoud als verzoeken kopiëren door een Exemplaar/Deeg en de Verzoeken van het Exemplaar/van het Deeg in reeks uit te voeren. Als u echter opmaak toepast op aanvragen in het werkblad en vervolgens kopieert en plakt, wordt de oorspronkelijke opmaak (zoals randen, lettertypen, enz.) door Report Builder gereproduceerd. in het plakgebied.

   Als u een aanvraag wijzigt die u naar het klembord hebt gekopieerd of geknipt voordat u de aanvraag plakt, wordt de aanvraag van het klembord verwijderd. Om het verzoek in zijn originele staat te houden, wijzig geen verzoek tussen de tijd u het kopieert en de tijd u het kleeft.
