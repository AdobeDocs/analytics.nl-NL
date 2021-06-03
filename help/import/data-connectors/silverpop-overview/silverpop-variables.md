---
description: De integratie van de Verbindingen van Gegevens voor Silverpop gebruikt variabelen van de Analyse om diverse Silverpop metriek te volgen.
title: Variabelen voor analytische integratie
uuid: 3aef3caf-e24e-4fe7-b4d7-50ca0f6703b5
exl-id: 0b8b31f5-65a8-41e0-97d1-d75fb1b91f62
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 4%

---

# Variabelen voor analytische integratie{#analytics-integration-variables}

De integratie van de Verbindingen van Gegevens voor Silverpop gebruikt variabelen van de Analyse om diverse Silverpop metriek te volgen.

Na het identificeren van de Gebeurtenis en eVars om met de Silverpop integratie te gebruiken, gebruik de Admin Console van Adobe Analytics om hen (zie [Suites van het Rapport](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html)) toe te laten.

In de volgende tabel worden de variabelen voor Analytics beschreven die nodig zijn voor de Silverpop-integratie.

## Vereiste variabelen {#section-3ca8dc46bab0436cba0c9ef827c8356a}

| Type variabele | Naam | Populatiemethode | Beschrijving |
|---|---|---|---|
| gebeurtenis (numeriek) | Bounces | Automatisch geïmporteerd uit Silverpop. | Met de gebeurtenis Bounces kunt u het aantal e-mailberichten zien dat niet aan ontvangers is bezorgd vanwege een leveringsprobleem. |
| gebeurtenis (numeriek) | Klikken | Automatisch geïmporteerd uit Silverpop. | Met de gebeurtenis Klikken kunt u het aantal bezoekers zien dat op het e-mailbericht heeft geklikt. |
| gebeurtenis (numeriek) | Openen | Automatisch geïmporteerd uit Silverpop. | Met de gebeurtenis Geopend kunt u het aantal bezoekers zien dat het e-mailbericht heeft geopend. |
| gebeurtenis (numeriek) | Verzenden | Automatisch geïmporteerd uit Silverpop. | Met de gebeurtenis Verzenden kunt u het aantal e-mailberichten zien dat is verzonden. |
| gebeurtenis (numeriek) | Abonnementen opzeggen | Automatisch geïmporteerd uit Silverpop. | Met de gebeurtenis Unsubscribed kunt u het aantal bezoekers zien dat het e-mailbericht heeft geopend, maar vervolgens op de koppeling Unsubscribe klikken om toekomstige e-mailberichten van uw organisatie af te melden. |
| eVar | Silverpop-id/Bezoeker-id | Verzameld van vraagparameters in e-mailverbindingen door de geautomatiseerde inzamelingsmethode of een elektrisch toestel JavaScript. | Unieke bezoeker-id |
| eVar of s.campagne | Verzendings-id | Verzameld van vraagparameters in e-mailverbindingen door de geautomatiseerde inzamelingsmethode of een elektrisch toestel JavaScript. | Dit wordt vaak opgeslagen in de campagnevariabele. |

## Optionele variabelen {#section-5f0a32b0a2084c87a64b5f90c0d0fb53}

| Type variabele | Naam | Populatiemethode | Beschrijving |
|---|---|---|---|
| event (teller) | Bestand gedownload | Handmatig verzameld via Analytics-tags. | Deze gebeurtenis wordt gebruikt om gebruikers te identificeren die een bestand op de site hebben gedownload. |
| event (teller) | Formulier gestart | Handmatig verzameld via Analytics-tags. | Formulier gestart wordt gebruikt om gebruikers te identificeren die een formulier beginnen, maar het niet invullen. |
| event (teller) | Formulier voltooid | Handmatig verzameld via Analytics-tags. | Het ingevulde formulier wordt gebruikt om bezoekers te identificeren die een formulier beginnen en het niet invullen. |
| eVar | E-mailadres | Handmatig verzameld via Analytics-tags. | Het e-mailadres is bedoeld voor het handmatig verzamelen van het e-mailadres op aanmeldingspagina&#39;s, aanmeldingspagina&#39;s of andere pagina&#39;s waarop het e-mailadres wordt verzameld. Deze variabele wordt gebruikt om opnieuw op de markt te brengen aan gebruikers die ervoor gekozen hebben binnen om e-mail te ontvangen, maar kan niet reeds door een e-mail in het verleden hebben geklikt. |
| eVar | Gedownload bestand | Handmatig verzameld via Analytics-tags. | Gedownload bestand geeft aan welk bestand een bezoeker heeft gedownload. |
| eVar | Formuliernaam | Handmatig verzameld via Analytics-tags. | De Naam van het formulier geeft aan welke vorm een verlaten bezoeker heeft. |
