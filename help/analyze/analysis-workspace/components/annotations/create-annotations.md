---
title: Annotaties maken
description: Hoe te om annotaties in Werkruimte tot stand te brengen.
role: User, Admin
source-git-commit: 6b5fd4e25056d7efbf3119a4d55d2e0a7897965f
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---


# Annotaties maken

>[!NOTE]
>
>Deze functie is momenteel in beperkte tests.

1. U kunt op vier manieren annotaties maken:

   * Ga naar [!UICONTROL Analytics] > [!UICONTROL Components] > [!UICONTROL Annotation]. De pagina Annotatiebeheer wordt geopend. Klikken [!UICONTROL Create New Annotation] en de aantekenaar Annotation wordt geopend.

   * Klik met de rechtermuisknop op een punt in een tabel- of lijngrafiek. De aannemer van de Annotatie opent. Merk op dat, door gebrek, de aantekeningen die op deze manier worden gecreeerd slechts in het project zichtbaar zijn waar zij werden gecreeerd. Maar u kunt ze beschikbaar maken voor alle projecten.

   * Ga in Workspace naar [!UICONTROL Components] > [!UICONTROL Create annotation]. De aannemer van de Annotatie opent.

   * Gebruik deze sneltoets om de aannemer van de Annotatie te openen:
      * (PC) `ctrl` `shift` + o
      * (Mac) `shift` + `command` + o

1. Vul de elementen van de Annotation builder in.

   ![](assets/ann-builder.png)

   | Element | Beschrijving |
   | --- | --- |
   | [!UICONTROL Title] | Geef de annotatie een naam, bijvoorbeeld &quot;Herdenkingsdag&quot; |
   | [!UICONTROL Description] | (Optioneel) Geef een beschrijving van de annotatie, bijvoorbeeld &quot;Publieke vakantie waargenomen in de VS&quot;. |
   | [!UICONTROL Tags] | (Optioneel) Organiseer annotaties door een tag te maken of toe te passen. |
   | [!UICONTROL Applied date] | Selecteer de datum of het datumbereik dat aanwezig moet zijn om de annotatie zichtbaar te maken. |
   | [!UICONTROL Color] | Pas een kleur toe op de annotatie. De annotatie wordt in het project weergegeven met de geselecteerde kleur. De kleur kan worden gebruikt om annotaties te categoriseren, zoals feestdagen, externe gebeurtenissen, problemen bij het bijhouden van wijzigingen, enzovoort. |
   | [!UICONTROL Scope] | (Optioneel) Sleep de metriek die de annotatie activeert en zet deze neer. Vervolgens sleept u alle afmetingen of segmenten die als filters fungeren (zodat de annotatie zichtbaar is). Als u geen bereik opgeeft, wordt de annotatie toegepast op al uw gegevens.<ul><li>**[!UICONTROL Any of these metrics are present]**: Sleep en zet tot 10 metriek neer die de annotatie zal teweegbrengen om te tonen.</li><li>**[!UICONTROL With all of these filters]**: Sleep tot 10 dimensies of segmenten die worden gefilterd wanneer de annotatie wordt weergegeven.</li></ul><p>Gebruik hoofdletters/kleine letters: Een eVar is gestopt met het verzamelen van gegevens voor een specifiek datumbereik. Sleep de eVar naar de **[!UICONTROL Any of these metrics are present]** . Of uw [!UICONTROL Visits] metrisch rapporteert geen gegevens - volg het zelfde proces. |
   | [!UICONTROL Apply to all report suites] | Standaard wordt de annotatie toegepast op de oorspronkelijke rapportsuite. Als u dit selectievakje inschakelt, kunt u de annotatie toepassen op alle rapportsuites in het bedrijf. |
   | [!UICONTROL Apply to all projects] | Standaard wordt de annotatie toegepast op het huidige project. Als u dit selectievakje inschakelt, kunt u de annotatie toepassen op alle projecten die u bezit. Dit selectievakje wordt alleen weergegeven wanneer u de Annotatiebuilder start vanuit de Annotatiebuilder? |

1. Klik op [!UICONTROL Save].

## Annotaties maken op basis van een [!UICONTROL Line] diagram

1. Van binnen een [!UICONTROL Line] een dip of een punt in het diagram selecteren [!UICONTROL Line] en klik er met de rechtermuisknop op. Een pop-up genaamd **[!UICONTROL Annotate selection]** wordt weergegeven.

   ![](assets/annotate-line.png)

1. Klik op **[!UICONTROL Annotate selection]**. De aannemer van de Annotatie opent.

>[!NOTE]
>
>Merk op de project-enige Annotatie. Schakel het selectievakje in om de annotatie beschikbaar te maken voor al uw projecten.

1. Vul de hierboven vermelde gegevens in. De datum/data en metrische gegevens, enz. zijn al ingevuld.

## Een annotatie maken vanuit een tabel voor vrije vorm

1. Ga zoals u voor een grafiek van de Lijn te werk, maar klik een rij in de lijst met de rechtermuisknop aan die moet worden geannoteerd.

1. Selecteren **[!UICONTROL Create annotation from selection]**.

   ![](assets/annotate-table.png)

1. Vul de hierboven vermelde gegevens in. De datum/data en metrische gegevens, enz. zijn al ingevuld.

