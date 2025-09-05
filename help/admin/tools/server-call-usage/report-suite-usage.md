---
description: Het lusje van het Gebruik van de Reeks van het Rapport verstrekt de gegevens van het servergebruik voor elke rapportreeks in alle Login bedrijven verbonden aan uw Facturerend bedrijf, voor de huidige gebruiksperiode.
title: Gebruik van rapportsuite weergeven
feature: Server Call Usage
exl-id: bedd4ed8-1c8b-45fd-a059-fed88e9fbe73
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Gebruik van rapportsuite weergeven

Het lusje van het Gebruik van de Reeks van het Rapport verstrekt de gegevens van het servergebruik voor elke rapportreeks in alle Login bedrijven verbonden aan uw Facturerend bedrijf, voor de huidige gebruiksperiode.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Server Call Usage]** > **[!UICONTROL Report Suite Usage]**

>[!IMPORTANT]
>
>Als een rapportsuite niet is gekoppeld aan een Experience Cloud-organisatie, worden de gebruiksgegevens niet weergegeven in dit dashboard. Ook, zou een het facturerings identiteitskaart aan veelvoudige Org van Experience Cloud kunnen worden gebonden; er is niet altijd een 1 :1 verhouding tussen een org en een het facturerings identiteitskaart

Het dashboard Gebruik rapportsuite

* Toont het servervraaggebruik van de huidige gebruiksperiode van de gebruiksperiode (Alle Vraag, Primair, Secundair, Mobiel Primair, Secundair Mobiel) voor elke rapportreeks in uw organisatie van Experience Cloud.
* Toont percentage van algemeen gebruik per categorie van de servervraag.
* Wordt dagelijks bijgewerkt.
* Kan worden gedownload.
* Hiermee hebt u toegang tot de gebruikersinterface van **[!UICONTROL Manage Alerts]** .

![](/help/admin/tools/server-call-usage/assets/report-suite-usage.png)

## Dashboardinstellingen {#settings}

| Kolom | Definitie |
|--- |--- |
| Naam rapportsuite | Vriendelijke naam van de rapportsuite |
| Alle Vraag (% van Totaal) | Alle servervraag in de huidige gebruiksperiode wordt gemaakt die. |
| Primaire Vraag (%) | Alle primaire servervraag (en hun percentage van totaal) in de huidige gebruiksperiode die wordt gemaakt. |
| Secundaire Vraag (%) | Alle secundaire servervraag (en hun percentage van totaal) die in de huidige gebruiksperiode wordt gemaakt. |
| Primaire mobiele telefoon (%) | Alle mobiele primaire serveraanroepen (en hun percentage van het totaal) die in de huidige gebruiksperiode zijn gedaan. |
| Secundair mobiel (%) | Alle mobiele secundaire serveraanroepen (en hun percentage van het totaal) die in de huidige gebruiksperiode zijn gemaakt. |

{style="table-layout:auto"}

## Gebruiksrapport downloaden {#download}

Met deze optie kunt u huidige gebruiksgegevens en gegevens downloaden uit tijdsperioden voorafgaand aan de huidige gebruiksperiode (van januari 2015). Het rapport wordt gedownload als een CSV-bestand.

1. Selecteer minstens één rapportsuite.
1. Klik op **[!UICONTROL Download Report]**.

   ![](/help/admin/tools/server-call-usage/assets/download_report.png)

| Rapportelement | Beschrijving |
|--- |--- |
| Bestandsnaam | Hardcoded name: Gebruiksrapport `day and time of report creation.csv` |
| Opgenomen rapportageopties | Om het even welke rapportreeksen u op de pagina van het Gebruik van de Server van het Rapport selecteerde zijn inbegrepen in deze lijst. |
| Inclusief vraagtypes | Specificeer om het even welke combinatie van deze: Alle Vraag (Gebrek), Primair, Secundair, Mobiel Primair, Secundair Mobiel. |
| Tijdbereik | U kunt de huidige gebruiksperiode kiezen of een aangepast bereik opgeven.  Voor een douanewaaier, specificeer het Begin van de Waaier en het Eind van de Waaier. <br>**Nota:** u kunt gebruiksgegevens niet vóór Januari 2015 downloaden </br>. |

{style="table-layout:auto"}

1. Klik op **[!UICONTROL Download]**.

Hier is een schermafbeelding van hoe het gedownloade .csv-bestand eruitziet. Het omvat een kolom voor identiteitskaart van de rapportreeks. De rapportsuite-id geeft een unieke id op die alleen alfanumerieke tekens mag bevatten. Deze id kan niet worden gewijzigd nadat een rapportsuite is gemaakt.

![](/help/admin/tools/server-call-usage/assets/download-usage.png)
