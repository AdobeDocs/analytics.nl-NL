---
description: De berekende metrierechten verschillen tussen gebruikers op beheerdersniveau en gebruikers zonder beheerdersrechten.
title: Berekende metrieke op rol-gebaseerde rechten
feature: Calculated Metrics
exl-id: 018d9ef5-5a6f-4ebc-a241-c1291ba6b561
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Berekende waarden: op rollen gebaseerde rechten

De berekende metrierechten verschillen tussen gebruikers op beheerdersniveau en gebruikers zonder beheerdersrechten.

|  | Maken | Delen | Weergeven/beheren | Goedkeuren | Toepassen |
|--- |--- |--- |--- |--- |--- |
| Gebruikers op beheerniveau | Beheerders kunnen berekende metriek maken en in de Admin Console productprofielen maken om de rechten van gebruikers om berekende metriek te maken te beperken. | Kan met volledig bedrijf, met gebruikersgroepen, en met individuele gebruikers delen. | Report Builder: kan bekijken/bewerken/verwijderen/enzovoort. haar eigen berekende maatstaven en de maatstaven die ermee worden gedeeld. | Kan berekende metriek goedkeuren als canonicaal. | Kan berekende waarden toepassen in de hele organisatie. |
| Gebruikers op niet-beheerniveau | Standaard kunnen gebruikers berekende metriek maken. Deze rechten kunnen echter door beheerders worden beperkt. | Kan alleen met individuele gebruikers delen | Kan weergeven/bewerken/verwijderen/enzovoort. alleen hun eigen berekende maatstaven. De gebruikers niet-admin moeten toegang tot alle componentengebeurtenissen hebben om gedeelde metriek (de toestemmingen in de console Admin worden nog afgedwongen) te kunnen zien.  Als een dashboard of een gepland rapport met een niet-admin gebruiker wordt gedeeld en zij metrisch niet hebben die met hen wordt gedeeld, zal het rapport met metrisch lopen toegepast (veronderstellend zij toestemmingen hebben om de gebeurtenissen te bekijken). Nochtans, zullen zij niet de definitie kunnen zien of metrisch uitgeven. | Kan alleen goedgekeurde berekende metriek gebruiken; kan niet markeren als goedgekeurd. | Kan hun eigen berekende metriek en segmenten toepassen die met hen zijn gedeeld. |