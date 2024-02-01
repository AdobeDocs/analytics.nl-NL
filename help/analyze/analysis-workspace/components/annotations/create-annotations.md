---
title: Annotaties maken
description: In Workspace kunt u notities maken.
role: Admin
feature: Annotations
exl-id: 3cf9a0fd-11c9-4375-8bbe-9551ba86f86d
source-git-commit: ee4772913c8b702658646755a2a11598c8530236
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Annotaties maken

Standaard kunnen alleen beheerders annotaties maken. Gebruikers hebben rechten om annotaties weer te geven zoals ze doen met andere onderdelen van Analytics (zoals segmenten, berekende metriek, enz.).

Beheerders kunnen echter de opdracht [!UICONTROL Annotation Creation] toestemming (Analytics Tools) aan gebruikers via [Adobe Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/analytics-tools.html).

1. U kunt op verschillende manieren annotaties maken:

| Aanmaakmethode | Details |
| --- | --- |
| **Ga naar [!UICONTROL Analytics] > [!UICONTROL Components] > [!UICONTROL Annotation].** | De pagina Annotatiebeheer wordt geopend. Klikken [!UICONTROL Create New Annotation] en de [!UICONTROL Annotation builder] wordt geopend. |
| **Klik met de rechtermuisknop op een punt in een tabel.** | [!UICONTROL The Annotation builder] wordt geopend. Merk op dat, door gebrek, de aantekeningen die op deze manier worden gecreeerd slechts in het project zichtbaar zijn waar zij werden gecreeerd. Maar u kunt ze beschikbaar maken voor alle projecten. U ziet ook dat de datum/data en metrische gegevens, enz. al zijn ingevuld.<p>![](assets/annotate-table.png) |
| **Klik met de rechtermuisknop op een punt in een [!UICONTROL Line] grafiek.** | De [!UICONTROL Annotation builder] wordt geopend. Merk op dat, door gebrek, de aantekeningen die op deze manier worden gecreeerd slechts in het project zichtbaar zijn waar zij werden gecreeerd. Maar u kunt ze beschikbaar maken voor alle projecten. U ziet ook dat de datum/data en metrische gegevens, enz. al zijn ingevuld.<p>![](assets/annotate-line.png) |
| **Ga in Workspace naar [!UICONTROL Components] > [!UICONTROL Create annotation].** | De [!UICONTROL Annotation builder] wordt geopend. |
| **Deze hotkey gebruiken** om de aannemer van de Annotatie te openen: (PC) `ctrl` `shift` + o, (Mac) `shift` + `command` + o | Houd er rekening mee dat u met de sneltoets een annotatie maakt voor de huidige datum zonder dat er een bereik (afmetingen of metriek) is geselecteerd. |

{style="table-layout:auto"}

1. Vul de [!UICONTROL Annotation builder] elementen.

   ![](assets/ann-builder.png)

   | Element | Beschrijving |
   | --- | --- |
   | [!UICONTROL Project-only Annotation] | Standaard wordt de annotatie toegepast op het huidige project. Als u dit selectievakje inschakelt, kunt u de annotatie beschikbaar stellen voor alle projecten die u bezit.<p> ![](assets/project-only.png) |
   | [!UICONTROL Title] | Geef de annotatie een naam, bijvoorbeeld &quot;Herdenkingsdag&quot; |
   | [!UICONTROL Description] | (Optioneel) Geef een beschrijving van de annotatie, bijvoorbeeld &quot;Publieke feestdag in de VS&quot;. |
   | [!UICONTROL Tags] | (Optioneel) Organiseer annotaties door een tag te maken of toe te passen. |
   | [!UICONTROL Applied date] | Selecteer de datum of het datumbereik dat aanwezig moet zijn om de annotatie zichtbaar te maken. |
   | [!UICONTROL Color] | Pas een kleur toe op de annotatie. De annotatie wordt in het project weergegeven met de geselecteerde kleur. De kleur kan worden gebruikt om annotaties te categoriseren, zoals feestdagen, externe gebeurtenissen, problemen bij het bijhouden van wijzigingen, enzovoort. |
   | [!UICONTROL Scope] | (Optioneel) Sleep de metriek die de annotatie activeert en zet deze neer. Vervolgens sleept u alle afmetingen of segmenten die als filters fungeren (zodat de annotatie zichtbaar is). Als u geen bereik opgeeft, wordt de annotatie toegepast op al uw gegevens.<ul><li>**[!UICONTROL Any of these metrics are present]**: Sleep en zet tot 10 metriek neer die de annotatie zal teweegbrengen om te tonen.</li><li>**[!UICONTROL With all of these filters]**: Sleep en zet tot 10 dimensies of segmenten neer die zullen filtreren wanneer de annotatie toont.</li></ul><p>Gebruiksscenario&#39;s: een eVar heeft gestopt met het verzamelen van gegevens voor een specifiek datumbereik. Sleep de eVar naar de **[!UICONTROL Any of these metrics are present]** in. Of uw [!UICONTROL Visits] metrisch rapporteert geen gegevens - volg het zelfde proces.<p>**Opmerking:** Elke annotatie die wordt toegepast op een component die vervolgens wordt gebruikt als onderdeel van een berekende definitie van metrisch object of segment, neemt de annotatie NIET automatisch over. De gewenste berekende metrisch moet ook aan de werkingsgebiedsectie worden toegevoegd om de aantekening te tonen. Er moet echter een nieuwe annotatie worden gemaakt voor elk segment dat u met dezelfde informatie wilt annoteren.<p>Voorbeeld: u past een annotatie toe op [!UICONTROL Orders] op een bepaalde dag. Vervolgens gebruikt u [!UICONTROL Orders] in een berekende metrische waarde voor hetzelfde datumbereik. De nieuwe berekende metrische waarde zal niet automatisch de aantekening voor orden tonen; berekende metrisch moet ook aan de werkingsgebiedsectie voor de te tonen aantekening worden toegevoegd. |
   | [!UICONTROL Apply to all report suites] | Standaard wordt de annotatie toegepast op de oorspronkelijke rapportsuite. Als u dit selectievakje inschakelt, kunt u de annotatie toepassen op alle rapportsuites in het bedrijf. |

   {style="table-layout:auto"}

1. Klik op **[!UICONTROL Save]**.
