---
description: U kunt rapporten plannen om volgens de tijd en dossierformaat te verzenden dat u bepaalt.
title: Een gegevensaanvraag plannen
uuid: f6d8c90f-e185-4d60-8035-f20f74bfcd89
feature: Report Builder
role: Bedrijfs Praktijk, Beheerder
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 0%

---


# Workbooks plannen

U kunt werkboeken plannen, geavanceerde leveringsopties specificeren, ontvangers specificeren, en de planningsgeschiedenis bekijken. Met de geavanceerde leveringsopties kunt u werkboeken configureren die u op een bepaald tijdstip of met intervallen wilt verzenden. U kunt het dossierformaat ook specificeren waarin om het werkboek te verzenden.

U kunt bijvoorbeeld werkboeken plannen die direct of volgens een terugkerend schema worden geleverd en de bestandsindeling opgeven in [!DNL Advanced Delivery Options]. De grens van de dossiergrootte is 5 MB voor een werkboek uploadt.

Bovendien, nadat u een werkboekprogramma in Report Builder creeert, kunt u het programma in **[!UICONTROL Analytics]** > **[!UICONTROL Reports]** bekijken en uitgeven. (Zie [Plan en distributie rapporteren](/help/analyze/reports-analytics/scheduling.md) in de Help Rapporten &amp; Analytics.)

>[!NOTE]
>
>U moet Excel 2007 of het verenigbaarheidspak hebben geïnstalleerd om een werkboek te plannen. U kunt maximaal 10 geplande werkboeken per Report Builder licentie hebben. U kunt dit aantal echter verhogen door andere licenties af te trekken. Ga hiertoe naar **[!UICONTROL Admin]** > **[!UICONTROL Company Settings]** > **[!UICONTROL Report Builder Reports]**. Een werkboek dat is gepland (of geupload aan de Bibliotheek van het Werkboek) en niet (bijgewerkt, vervangen) in meer dan 28 maanden is aangeraakt zal worden geschrapt.

>[!NOTE]
>
>De &quot;Tijd van de Levering&quot;/&quot;Tijd van Dag&quot;ingegaan door de gebruiker specificeert de tijd dat het werkboek zou moeten beginnen verwerkend, niet de tijd dat het eigenlijk zal worden geleverd. De daadwerkelijke tijd dat het werkboek zal worden geleverd is hoofdzakelijk gebaseerd op hoe lang het aan proces (de complexe en grote werkboeken nemen langer aan proces dan de eenvoudigere werkboeken) vergt. Bijvoorbeeld, als een werkboek 15 minuten aan proces vergt, dan zal de daadwerkelijke leveringstijd minstens 15 minuten voorbij de oorspronkelijk gespecificeerde &quot;Tijd van de Levering&quot;/&quot;Tijd van Dag zijn.
>Bovendien zijn er een aantal andere factoren die de vertraging kunnen verder verhogen alvorens het werkboek eigenlijk wordt geleverd:
>
> * **Het runnen van vele verschillende programma&#39;s van het zelfde type bij zelfde** timecan overload het systeem. Het plannende systeem staat slechts een paar (5-10) werkboeken van één type toe om gelijktijdig te lopen, zodat wanneer meer dan 5-10 allen in één keer gepland zijn, zullen sommigen in lijn op andere werkboeken moeten wachten alvorens zij met verwerking kunnen beginnen. Dit probleem kan worden verholpen door de werkboeken van een bedrijf op gestaffelde tijden door de dag of het uur te plannen, eerder dan gelijktijdig.
> * Naast het specifieke werkboektype, zullen de werkboeken ook in lijn wachten als het bedrijf **meer dan 15-20 van om het even welk die type werkboek heeft tegelijkertijd wordt gepland (over alle verschillende werkboektypes)**. Dit kan worden verlicht door onthutsende planningstijden in plaats van vele tezelfdertijd te hebben lopen.
> * **De kwesties in stroomafwaartse** diensten die de Planner op baseert kunnen ook levering van werkboeken beïnvloeden. Bijvoorbeeld, als u onafhankelijk APIs gebruikt om werkboeken in werking te stellen en de API verzoekrij te vullen, dan kunnen uw geplande werkboeken langzaam leveren terwijl u voor die bron concurreert.
> * **De latentie**  van de Reeks van het rapport (een vertraging in gegevensinzameling) kan sommige geplande werkboeken ook vertragen.


## Een werkmap plannen

1. Genereer en sla een werkboek op.
1. Klik op **[!UICONTROL Schedule]** op de werkbalk Report Builder.

   Het tabblad [!UICONTROL Scheduled Reports] bevat een overzicht van alle taken die u hebt gemaakt en van het aantal resterende taken.
1. Klik op het tabblad **[!UICONTROL Scheduled Reports]** op **[!UICONTROL New]**.
1. De Basis plannende Tovenaar toont:

   ![](assets/simple-schedule-wizard.png)

1. In [!UICONTROL Basic Scheduling Wizard], vorm de volgende opties:

| Veld | Beschrijving |
|--- |--- |
| Rapport selecteren | De naam van het werkboek. Voor nieuwe geplande rapporten, is dit gebied bevolkt met de actieve werkboeknaam. |
| Selecteren | Hiermee geeft u de pagina Rapport selecteren weer. U kunt een rapport van de server (waar al uw eerder geplande werkboeken worden opgeslagen), of van uw lokale machine selecteren. Als u een werkboek van de lokale aandrijving in .xls formaat selecteert, zet het systeem het dossier in .xlsx om. Als onderdeel van die conversie wordt het bestand geopend in Excel en geactiveerd. Als het geselecteerde werkboek voor het geplande rapport zelfde filename zoals het werkboek momenteel open in Excel heeft, selecteert het systeem het lokale dossier in plaats van het eerder geupload dossier. Als u een rapport van de het plannen bewaarplaats selecteert, wordt een exemplaar van het werkboek gecreeerd op de server, met zijn filename die met 1 wordt bijgewerkt. Het onlangs gecreeerde geplande rapport gebruikt het gekopieerde werkboek. |
| Aanpassen | Hiermee kunt u de datumnotatie aanpassen. |
| Naar | Toont uw Boek van het Adres van Vooruitzichten, als toepasselijk. |
| Verzenden naar: E-mail | De e-mailontvanger van het werkboek. |
| Verzenden naar: Publicatielijst | Toont een lijst van beschikbare distributielijsten voor dit bedrijf. |
| Power BI | Zie [Werkboek publiceren naar Microsoft Power BI](/help/analyze/report-builder/c-publish-power-bi/integration-power-bi.md) voor meer informatie. |
| Onderwerp | Een door de gebruiker gedefinieerde beschrijving. |
| Planning | Hier kunt u opgeven wanneer het werkboek moet worden verzonden. (Direct, uur, dag, week, maand, en jaarlijks.) |

## Geavanceerde leveringsopties

1. Klik op **[!UICONTROL Advanced Delivery Options]** om bestands- en publicatieopties te configureren:

| Veld | Beschrijving |
|--- |--- |
| **Tabblad Planning** |  |
| Leveringstijd | Laat u het werkboek onmiddellijk of voor een recentere tijd plannen. De tijd van de dag is relatief ten opzichte van de tijdzone die op uw computer is opgegeven. |
| Herhalingspatroon | Verzendt het werkboek dat op uw selecties wordt gebaseerd. |
| Bereik van herhaling | Laat u specificeren wanneer te beginnen en ophouden ontvangend het werkboek.   Opmerking:  Het plannen van een werkboek op de eerste dag van om het even welke huidige periode (week, maand, kwartaal, of jaar) keert gegevens slechts voor de eerste dag terug. |
| **Tabblad Bestandsopties** |  |
| Bestandsindeling | Hiermee kunt u een leveringsindeling selecteren voor Excel 2007 (.xlsx) of 2003 (.xls), .pdf, .csv, .mht, .txt en .xml. |
| Bestandsbestemming | Hier geeft u E-mail of FTP op. De opties op de pagina veranderen afhankelijk van uw selectie. Voor FTP moet u ervoor zorgen dat de host extern beschikbaar is. |
| Publicatielijst | Als u het geplande werkboek naar veelvoudige het publiceren lijsten verzendt, loopt het werkboek eens voor elke lijst. De variabele rapportreeksen worden vervangen door de rapportreeks die aan de het publiceren lijst wordt toegewezen. |
| Taal bestandsinhoud | Hiermee geeft u de taal op die u voor de begeleidende letter wilt gebruiken. U kunt Chinees (Vereenvoudigd of Traditioneel), Duits, Frans, Japans, Koreaans, Braziliaans Portugees, of Spaans selecteren. |
| **Tabblad Publicatieopties** |  |
| Publiceren naar Power BI | <ul><li>Werkboek publiceren naar Power BI</li><li>Alle Report Builder-verzoeken publiceren als Power BI-gegevenssets</li><li>Alle opgemaakte tabellen publiceren als gegevenssets voor Power BI</li></ul> |
| Dit Power BI-rapport labelen als | Etiketteringsdetails |

1. Klik **[!UICONTROL OK]**, dan klik **[!UICONTROL Exit]**.

   Report Builder toont het geplande werkboek in [Geplande Manager van de Taak](/help/analyze/report-builder/r-arb-scheduled-reports.md).

