---
title: Annotaties maken
description: Annotaties maken in Workspace.
role: Admin
feature: Annotations
exl-id: 3cf9a0fd-11c9-4375-8bbe-9551ba86f86d
source-git-commit: 75d8705170169a0ef9f1ee59b12e4bb2c3afac7a
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Annotaties maken {#create-annotations}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_annotations_details"
>title="Details van aantekening"
>abstract="Met annotaties kunt u op effectieve wijze contextuele gegevensnuances en inzichten aan uw organisatie meedelen. Met deze sjablonen kunt u kalendergebeurtenissen koppelen aan specifieke afmetingen/metriek."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_annotations_scope"
>title="Toepassingsgebied"
>abstract="Met het bereik kunt u aanpassen welke gegevens worden geannoteerd. Berekende metriek en segmenten zullen automatisch geen annotaties erven die worden toegepast op componenten die in hun definities worden gebruikt. U kunt nieuwe berekende metriek aan de werkingsgebiedsectie van een bestaande aantekening toevoegen. Voor nieuwe segmenten is een nieuwe annotatie vereist."

<!-- markdownlint-enable MD034 -->

Standaard kunnen alleen beheerders annotaties maken. Gebruikers hebben rechten om annotaties weer te geven zoals ze doen met andere onderdelen van Analytics (zoals segmenten, berekende metriek, enz.).

Nochtans, kunnen Admins de [!UICONTROL Annotation Creation] toestemming (Hulpmiddelen van Analytics) aan gebruikers via [ Adobe Admin Console ](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/analytics-tools.html) geven.

1. U kunt op verschillende manieren annotaties maken:

| Aanmaakmethode | Details |
| --- | --- |
| **ga naar [!UICONTROL Analytics] > [!UICONTROL Components] > [!UICONTROL Annotation].** | De pagina Annotatiebeheer wordt geopend. Klik op [!UICONTROL Create New Annotation] en [!UICONTROL Annotation builder] wordt geopend. |
| **klik een punt op een lijst met de rechtermuisknop aan.** | [!UICONTROL The Annotation builder] wordt geopend. Merk op dat, door gebrek, de aantekeningen die op deze manier worden gecreeerd slechts in het project zichtbaar zijn waar zij werden gecreeerd. Maar u kunt ze beschikbaar maken voor alle projecten. U ziet ook dat de datum/data en metrische gegevens, enz. al zijn ingevuld.<p>![](assets/annotate-table.png) |
| **klik een punt in a [!UICONTROL Line] grafiek met de rechtermuisknop aan.** | De lus [!UICONTROL Annotation builder] wordt geopend. Merk op dat, door gebrek, de aantekeningen die op deze manier worden gecreeerd slechts in het project zichtbaar zijn waar zij werden gecreeerd. Maar u kunt ze beschikbaar maken voor alle projecten. U ziet ook dat de datum/data en metrische gegevens, enz. al zijn ingevuld.<p>![](assets/annotate-line.png) |
| **in Workspace, ga [!UICONTROL Components] > [!UICONTROL Create annotation].** | De lus [!UICONTROL Annotation builder] wordt geopend. |
| **gebruik dit hotkey** om de aannemer van de Annotatie te openen: (PC) `ctrl` `shift` + o, (Mac) `shift` + `command` + o | Houd er rekening mee dat u met de sneltoets een annotatie maakt voor de huidige datum zonder dat er een bereik (afmetingen of metriek) is geselecteerd. |

{style="table-layout:auto"}

1. Vul de [!UICONTROL Annotation builder] -elementen in.

   ![](assets/ann-builder.png)

   | Element | Beschrijving |
   | --- | --- |
   | [!UICONTROL Project-only Annotation] | Standaard wordt de annotatie toegepast op het huidige project. Als u dit selectievakje inschakelt, kunt u de annotatie beschikbaar stellen voor alle projecten die u bezit.<p> ![](assets/project-only.png) |
   | [!UICONTROL Title] | Geef de annotatie een naam, bijvoorbeeld &quot;Herdenkingsdag&quot; |
   | [!UICONTROL Description] | (Optioneel) Geef een beschrijving van de annotatie, bijvoorbeeld &quot;Publieke feestdag in de VS&quot;. |
   | [!UICONTROL Tags] | (Optioneel) Organiseer annotaties door een tag te maken of toe te passen. |
   | [!UICONTROL Applied date] | Selecteer de datum of het datumbereik dat aanwezig moet zijn om de annotatie zichtbaar te maken. |
   | [!UICONTROL Color] | Pas een kleur toe op de annotatie. De annotatie wordt in het project weergegeven met de geselecteerde kleur. De kleur kan worden gebruikt om annotaties te categoriseren, zoals feestdagen, externe gebeurtenissen, problemen bij het bijhouden van wijzigingen, enzovoort. |
   | [!UICONTROL Scope] | (Optioneel) Sleep de metriek die de annotatie activeert en zet deze neer. Vervolgens sleept u alle afmetingen of segmenten die als filters fungeren (zodat de annotatie zichtbaar is). Als u geen bereik opgeeft, wordt de annotatie toegepast op al uw gegevens.<ul><li>**[!UICONTROL Any of these metrics are present]**: sleep en zet tot 10 metriek neer die de annotatie zal teweegbrengen om te tonen.</li><li>**[!UICONTROL With all of these filters]**: Sleep en zet tot 10 dimensies of segmenten neer die zullen filtreren wanneer de annotatie toont.</li></ul><p>Gebruiksscenario&#39;s: een eVar heeft gestopt met het verzamelen van gegevens voor een specifiek datumbereik. Sleep de eVar naar het dialoogvenster **[!UICONTROL Any of these metrics are present]** . Of uw [!UICONTROL Visits] metrische code rapporteert geen gegevens - volg hetzelfde proces.<p>**Nota:** Om het even welke die annotatie op een component wordt toegepast die dan als deel van een berekende metrische of segmentdefinitie wordt gebruikt erft automatisch niet de annotatie. De gewenste berekende metrisch moet ook aan de werkingsgebiedsectie worden toegevoegd om de aantekening te tonen. Er moet echter een nieuwe annotatie worden gemaakt voor elk segment dat u met dezelfde informatie wilt annoteren.<p>Voorbeeld: u past een annotatie toe op [!UICONTROL Orders] op een bepaalde dag. Vervolgens gebruikt u [!UICONTROL Orders] in een berekende metrische waarde voor hetzelfde datumbereik. De nieuwe berekende metrische waarde zal niet automatisch de aantekening voor orden tonen; berekende metrisch moet ook aan de werkingsgebiedsectie voor de te tonen aantekening worden toegevoegd. |
   | [!UICONTROL Apply to all report suites] | Standaard wordt de annotatie toegepast op de oorspronkelijke rapportsuite. Als u dit selectievakje inschakelt, kunt u de annotatie toepassen op alle rapportsuites in het bedrijf. |

   {style="table-layout:auto"}

1. Klik op **[!UICONTROL Save]**.
