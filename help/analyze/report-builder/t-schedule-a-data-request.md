---
description: Leer hoe u rapporten kunt plannen.
title: Hoe te om een gegevensverzoek te plannen
uuid: f6d8c90f-e185-4d60-8035-f20f74bfcd89
feature: Report Builder
role: User, Admin
exl-id: 6aaadaa8-d68f-4a03-8838-53a61b152e31
source-git-commit: ed753ab23e65f845f472dd1df3b144284e4e94a6
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 0%

---

# Workbooks plannen

U kunt werkboeken plannen, geavanceerde leveringsopties specificeren, ontvangers specificeren, en de planningsgeschiedenis bekijken. Met de geavanceerde leveringsopties kunt u werkboeken configureren die u op een bepaald tijdstip of met intervallen wilt verzenden. U kunt het dossierformaat ook specificeren waarin om het werkboek te verzenden.

U kunt bijvoorbeeld plannen dat werkboeken direct of volgens een terugkerend schema worden geleverd en de bestandsindeling opgeven in [!DNL Advanced Delivery Options]. De grens van de dossiergrootte is 5 MB voor een werkboek uploadt.

Bovendien, nadat u een werkboekprogramma in Report Builder creeert, kunt u het programma in bekijken en uitgeven **[!UICONTROL Analytics]** > **[!UICONTROL Reports]**. (Zie [Rapportschema en distributie](/help/analyze/reports-analytics/scheduling.md) in de Help bij Rapporten en Analytics.)

>[!NOTE]
>
>U moet Excel 2007 of het verenigbaarheidspak hebben geïnstalleerd om een werkboek te plannen. U kunt maximaal 10 geplande werkboeken per licentie voor Reporten Builder hebben. U kunt dit aantal echter verhogen door andere licenties af te trekken. Ga hiertoe naar **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Company settings]** > **[!UICONTROL Report Builder Reports]**. Een werkboek dat is gepland (of geupload aan de Bibliotheek van het Werkboek) en niet (bijgewerkt, vervangen) in meer dan 28 maanden is aangeraakt zal worden geschrapt.

>[!NOTE]
>
>De &quot;Tijd van de Levering&quot;/&quot;Tijd van Dag&quot;ingegaan door de gebruiker specificeert de tijd dat het werkboek met verwerking zou moeten beginnen, niet de tijd dat het eigenlijk zal worden geleverd. De daadwerkelijke tijd dat het werkboek zal worden geleverd is hoofdzakelijk gebaseerd op hoe lang het aan proces (de complexe en grote werkboeken nemen langer aan proces dan de eenvoudigere werkboeken) vergt. Bijvoorbeeld, als een werkboek 15 minuten aan proces vergt, dan zal de daadwerkelijke leveringstijd minstens 15 minuten voorbij de oorspronkelijk gespecificeerde &quot;Tijd van de Levering&quot;/&quot;Tijd van Dag zijn.
>Bovendien zijn er een aantal andere factoren die de vertraging kunnen verder verhogen alvorens het werkboek eigenlijk wordt geleverd:
>
> * **Vele verschillende programma&#39;s van hetzelfde type tegelijk uitvoeren** kan het systeem overladen. Het plannende systeem staat slechts een paar (5-10) werkboeken van één type toe om gelijktijdig te lopen, zodat wanneer meer dan 5-10 allen in één keer gepland zijn, zullen sommigen in lijn op andere werkboeken moeten wachten alvorens zij met verwerking kunnen beginnen. Dit probleem kan worden verholpen door de werkboeken van een bedrijf op gestaffelde tijden door de dag of het uur te plannen, eerder dan gelijktijdig.
> * Naast het specifieke werkboektype, zullen de werkboeken ook in lijn wachten als het bedrijf heeft **meer dan 15-20 van om het even welk die type van werkboek tegelijkertijd (over alle verschillende werkboektypes) wordt gepland**. Dit kan worden verlicht door onthutsende planningstijden in plaats van vele tezelfdertijd te hebben lopen.
> * **Problemen bij downstreamdiensten** dat de Planner zich op baseert ook levering van werkboeken kan beïnvloeden. Bijvoorbeeld, als u onafhankelijk APIs gebruikt om werkboeken in werking te stellen en de API verzoekrij te vullen, dan kunnen uw geplande werkboeken langzaam leveren terwijl u voor die bron concurreert.
> * **Vertraging rapportsuite** (een vertraging in gegevensinzameling) kan sommige geplande werkboeken ook vertragen.

## Een werkmap plannen

1. Genereer en sla een werkboek op.
1. Klik op de werkbalk Report Builder op **[!UICONTROL Schedule]**.

   De [!UICONTROL Scheduled Reports] bevat een overzicht van alle taken die u hebt gemaakt en van het aantal resterende taken.
1. Op de **[!UICONTROL Scheduled Reports]** tabblad, klikt u op **[!UICONTROL New]**. De Basis plannende Tovenaar toont de opties worden gebruikt om het geplande rapport te bepalen die.

   ![Screenshot die de Basic Scheduling Wizard weergeeft.](assets/simple-schedule-wizard.png)

1. In de [!UICONTROL Basic Scheduling Wizard], configureert u de volgende opties:

| Veld | Beschrijving |
|--- |--- |
| Rapport selecteren | De naam van het werkboek. Voor nieuwe geplande rapporten, is dit gebied bevolkt met de actieve werkboeknaam. |
| Selecteren | Hiermee geeft u de pagina Rapport selecteren weer. U kunt een rapport van de server (waar al uw eerder geplande werkboeken worden opgeslagen), of van uw lokale machine selecteren. Als u een werkboek van de lokale aandrijving in .xls formaat selecteert, zet het systeem het dossier in .xlsx om. Als onderdeel van die conversie wordt het bestand geopend in Excel en geactiveerd. Als het geselecteerde werkboek voor het geplande rapport zelfde filename zoals het werkboek momenteel open in Excel heeft, selecteert het systeem het lokale dossier in plaats van het eerder geupload dossier. Als u een rapport van de het plannen bewaarplaats selecteert, wordt een exemplaar van het werkboek gecreeerd op de server, met zijn filename die met 1 wordt bijgewerkt. Het onlangs gecreeerde geplande rapport gebruikt het gekopieerde werkboek. |
| Aanpassen | Hiermee kunt u de datumnotatie aanpassen. |
| Naar | Toont uw Boek van het Adres van Vooruitzichten, als toepasselijk. |
| Verzenden naar: E-mail | De e-mailontvanger van het werkboek. |
| Power BI | Zie [Werkboek publiceren naar Microsoft-Power BI](/help/analyze/report-builder/c-publish-power-bi/integration-power-bi.md) voor meer informatie . |
| Onderwerp | Een door de gebruiker gedefinieerde beschrijving. |
| Planning | Hier kunt u opgeven wanneer het werkboek moet worden verzonden. (Direct, uur, dag, week, maand, en jaarlijks.) |

## Geavanceerde leveringsopties

1. Klikken **[!UICONTROL Advanced Delivery Options]** om bestands- en publicatieopties te configureren:

| Veld | Beschrijving |
|--- |--- |
| **Tabblad Planning** |  |
| Leveringstijd | Laat u het werkboek onmiddellijk of voor een recentere tijd plannen. De tijd van de dag is relatief ten opzichte van de tijdzone die op uw computer is opgegeven. |
| Herhalingspatroon | Verzendt het werkboek dat op uw selecties wordt gebaseerd. |
| Bereik van herhaling | Laat u specificeren wanneer te beginnen en ophouden ontvangend het werkboek.   Nota: Het plannen van een werkboek op de eerste dag van om het even welke huidige periode (week, maand, kwartaal, of jaar) keert gegevens slechts voor de eerste dag terug. |
| **Tabblad Bestandsopties** |  |
| Bestandsindeling | Hiermee kunt u een leveringsindeling selecteren voor Excel 2007 (.xlsx) of 2003 (.xls), .pdf, .csv, .mht, .txt en .xml. |
| Bestandsbestemming | Hier geeft u E-mail of FTP op. De opties op de pagina veranderen afhankelijk van uw selectie. Voor FTP moet u ervoor zorgen dat de host extern beschikbaar is. |
| Taal voor bestandsinhoud | Hiermee geeft u de taal op die u voor de begeleidende letter wilt gebruiken. U kunt Chinees (Vereenvoudigd of Traditioneel), Duits, Frans, Japans, Koreaans, Braziliaans Portugees, of Spaans selecteren. |
| **Tabblad Publicatieopties** |  |
| Publiceren naar Power BI | <ul><li>Werkboek publiceren naar Power BI</li><li>Alle verzoeken om Report Builder publiceren als Power BI Datasets</li><li>Alle opgemaakte tabellen publiceren als gegevenssets voor Power BI</li></ul> |
| Dit Power BI-rapport labelen als | Etiketteringsdetails |

1. Klikken **[!UICONTROL OK]** en klik vervolgens op **[!UICONTROL Exit]**.

   De Report Builder toont het geplande werkboek in [Geplande Taakmanager](/help/analyze/report-builder/r-arb-scheduled-reports.md).
