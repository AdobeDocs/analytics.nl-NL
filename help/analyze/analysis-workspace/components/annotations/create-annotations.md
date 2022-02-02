---
title: Annotaties maken
description: Hoe te om annotaties in Werkruimte tot stand te brengen.
role: User, Admin
source-git-commit: f8a928782b4c4916f5ff2042cb72941d76f57d7d
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---


# Annotaties maken

>[!NOTE]
>
>Deze functie is momenteel in beperkte tests.

1. U kunt op vier manieren annotaties maken:

   * Ga naar [!UICONTROL Analytics] > [!UICONTROL Components] > [!UICONTROL Annotation]. De pagina Annotatiebeheer wordt geopend. Klikken [!UICONTROL Create New Annotation] en de aantekenaar Annotation opent, of

   * Klik met de rechtermuisknop op een punt in een tabel- of lijngrafiek. De aantekenaar voor annotaties wordt geopend, of

   * Ga in Workspace naar [!UICONTROL Components] > [!UICONTROL Create annotation].

   * Gebruik deze sneltoets om de aannemer van de Annotatie te openen:
      * (PC) `ctrl` `shift` + o
      * (Mac) `shift` + `command` + o

1. Vul de elementen van de Bouwer in.

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
   | [!UICONTROL Apply to all projects] | Standaard wordt de annotatie toegepast op het huidige project. Als u dit selectievakje inschakelt, kunt u de annotatie toepassen op alle projecten die u bezit. |

1. Klik op [!UICONTROL Save].