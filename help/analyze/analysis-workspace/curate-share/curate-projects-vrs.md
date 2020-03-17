---
title: vrijwillige VUT- en projectcursus
description: Leer hoe u vrs-componenten en -projecten kunt beheren
translation-type: tm+mt
source-git-commit: db983980a6ec3db4d60bbc8fc3ba57a4e1219287

---


# vrijwillige VUT- en projectcursus

Wanneer u projecten of virtuele rapportsuites (VRSs) leidt, filtert u hoofdzakelijk componenten uit zodat uw publiek slechts die project/VRS componenten (afmetingen, metriek, segmenten, datumwaaiers) ziet die u hen wilt gebruiken.

>[!NOTE]
>
>Productprofielen zijn het belangrijkste mechanisme dat bepaalt welke componenten een gebruiker kan zien. Ze worden beheerd via de [beheerconsole](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html#createproductprofiles). Curatie is een secundair filter.

We hebben de laatste tijd de curatele ervaring verbeterd. Hier is een overzicht van wat de **[!UICONTROL Show All]** knoop, naast de gebogen reeds beschikbare componenten, in verschillende gebogen ervaringen en op toestemmingsniveau onthult:

| Curvetype | Admins | Niet-Admin-projecteigenaars | Niet-beheerders |
|---|---|---|---|
| Gekromde VRS | Alle niet-gebogen VRS-componenten | Niet-beheerde VRS-componenten waarvan deze rol eigenaar is of die met hen zijn gedeeld | Niet-beheerde VRS-componenten waarvan deze rol eigenaar is of die met hen zijn gedeeld |
| Samengevoegd project | Alle niet-gekrulde projectcomponenten | Alle niet-gekrulde projectcomponenten | Niet-gekrulde projectcomponenten die deze rol bezit of die met hen zijn gedeeld |
| Gekromd project in een gekromd VRS | Alle niet-gebogen componenten, vermeld onder **[!UICONTROL Non-Curated Project Components]** en **[!UICONTROL Non-Curated VRS Components]** | Alle niet-gebogen projectcomponenten EN niet-gekrulde componenten VRS die deze rol bezit of die met hen zijn gedeeld | Niet-gekromde VRS en projectcomponenten die deze rol bezit of die met hen zijn gedeeld |

>[!IMPORTANT]
>
>De kromming van VRS wordt altijd toegepast vóór projectkromming. Dit betekent dat zelfs als uw gebogen project bepaalde componenten omvat, zij uit zullen worden gefiltreerd als het gebogen VRS hen niet omvat.
