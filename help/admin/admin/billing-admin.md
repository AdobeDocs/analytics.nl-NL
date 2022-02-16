---
description: De het Factureren pagina laat u tot factureringsinformatie, met inbegrip van verkeersdetails voor elke rapportreeks toegang hebben. Alleen een geautoriseerde beheerder heeft toegang tot deze pagina.
title: Facturering
feature: Admin Tools
exl-id: cea802e4-99c4-491e-99c2-8476870001f7
source-git-commit: 2c0aef13bdb88b0a7aa9f100c72c21f66a14c8dd
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 1%

---

# Facturering

De het Factureren pagina laat u tot factureringsinformatie, met inbegrip van verkeersdetails voor elke rapportreeks toegang hebben. Alleen een geautoriseerde beheerder heeft toegang tot deze pagina.

>[!NOTE]
>
>Neem contact op met uw accountmanager als de toegang tot het tabblad Facturering voor uw bedrijf is uitgeschakeld.

De gegevens van het verkeersoverzicht van de factureringspagina laten u paginameningsgegevens in rapporten met factureerbare servervraag op uw factuur correleren. De [!UICONTROL Billing] kunt u het volgende doen:

* Controleer uw factuur.
* Verdeling van de kosten per rapportenpakket voor interne boekhoudingen.
* Bekijk de distributie van primaire en secundaire servervraag.

De [!UICONTROL Billing] de pagina organiseert informatie door maand.

Om maandelijkse gegevens van het verkeersoverzicht te bekijken, bepaal de plaats van de maand waar u verkeersgegevens wilt bekijken, dan klik **[!UICONTROL View]**.

Het resultaat [!UICONTROL Monthly Invoice] het rapport bevat de volgende informatie :

| Kolom | Beschrijving |
|--- |--- |
| Rapportsuite | De rapportsuite die is betrokken bij de gegevensverzamelingsactiviteit. |
| Locatie | Het gegevenscentrum dat de gegevens van de rapportreeks opslaat: San Jose (Californië), Dallas (Texas), Pacific Northwest (VS), Londen (VK), of Singapore. In de meeste gevallen, worden alle reeksen van het bedrijfrapport gevestigd in het zelfde gegevenscentrum. |
| Primaire serveraanroepen | Aanvragen die rechtstreeks zijn ontvangen van de browsers van de websitebezoeker of de API voor het invoegen van gegevens. Deze groep bevat primaire Hits (paginaweergaven), primaire aangepaste gebeurtenissen, primaire downloadgebeurtenissen en primaire afsluitgebeurtenissen. |
| Secundaire serveraanroepen | Kopieën van primaire servervraag die door multi-suite markeringen wordt gecreeerd of door een VISTA regel wordt gekopieerd/wordt bewogen.  Als een secundaire servervraag (niet gekopieerd) aan een verschillende rapportreeks door een regel VISTA is verplaatst, identificeert de Factureringspagina deze overdracht met een negatief aantal. In dit geval, worden de geaccumuleerde secundaire vraag afgetrokken van de primaire servervraag. |
| Totaal aantal serveraanroepen | Het gecombineerde totaal van primaire en secundaire server roept voor deze rapportreeks bij de bepaalde plaats. |
| Paginaweergaven | De totalen van de paginaweergave voor elke rapportsuite. U kunt de waarden van de paginaweergave bevestigen in Site Metrics > Paginaweergaven. |
| Downloads | De totalen van de download voor elke rapportreeks. U kunt de downloadwaarden bevestigen in Site Content > Links > Bestandsdownloads. |
| Aangepaste koppelingen | De verbindingstotalen van de douane voor elke rapportreeks. U kunt de waarden voor aangepaste koppelingen bevestigen in Site-inhoud > Koppelingen > Aangepaste koppelingen. |
| Koppelingen afsluiten | De verbindingstotalen van de uitgang voor elke rapportreeks. U kunt de waarden voor de afsluitkoppelingen bevestigen in Site Content > Links > Koppelingen afsluiten. |

>[!NOTE]
>
>Om een werkexemplaar van te verkrijgen [!UICONTROL Monthly Invoice] rapport, kopieer het naar het klembord en plak het in een spreadsheetprogramma zoals Microsoft Excel*.

## Datum van rapportage versus datum van verwerking {#section_51A48C2F223F4904BE1407C13333C457}

In de rapportgebruikersinterface worden de gepresenteerde gegevens altijd gekoppeld aan de **Datum van rapportage**, dit is de tijdstempel die aan de gebeurtenis is gekoppeld.

Bij gebruik/facturering daarentegen wordt altijd het volgende gebruikt: **Verwerkingsdatum** of wanneer de gegevens daadwerkelijk in het systeem zijn verwerkt. Vanwege standaardwachttijden, gegevensinvoer of verschillen in tijdzone van gebeurtenissen (alles wordt verwerkt in Pacific Time) komen de Datum en de datum van verwerking van de rapportage gewoonlijk niet volledig overeen.
