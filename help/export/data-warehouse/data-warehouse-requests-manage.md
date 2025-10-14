---
description: Leer om, verzoeken van de Data Warehouse te bekijken te dupliceren en opnieuw voorrang te geven.
title: Aanvragen voor Data Warehouse beheren
feature: Data Warehouse
uuid: cdeb764f-56f9-43ec-9228-8ed5a2b58909
exl-id: a399d366-8402-4f4f-9b9f-14b218cd074a
source-git-commit: d929e97a9d9623a8255f16729177d812d59cec05
workflow-type: tm+mt
source-wordcount: '1148'
ht-degree: 0%

---

# Aanvragen voor Data Warehouse beheren

U kunt de verzoeken van de Data Warehouse bekijken en beheren die u hebt gemaakt. Alleen beheerders kunnen aanvragen van andere gebruikers in hun organisatie weergeven en beheren.

De volgende secties beschrijven activiteiten die u kunt uitvoeren wanneer het beheren van verzoeken.

## Verzoeken weergeven

Door gebrek, kunt u slechts de verzoeken bekijken die u creeert, tenzij de gebruikers hebben gekozen om hun verzoeken zichtbaar aan anderen in de organisatie (zoals die in [&#x200B; worden beschreven verzoek algemene montages van de Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/dw-general-settings.md)) te maken. Systeembeheerders kunnen alle aanvragen weergeven.

Om de verzoeken van de Data Warehouse te bekijken:

1. In Adobe Analytics, uitgezochte [!UICONTROL **Hulpmiddelen**] > [!UICONTROL **Data Warehouse**].

   Op de pagina Data Warehouse worden alle aanvragen weergegeven die u hebt gemaakt. Gegevens worden in elke kolom weergegeven. U kunt [&#x200B; vormen welke kolommen &#x200B;](#configure-columns) zichtbaar zijn.

   <!-- add screenshot of main page -->

<!-- describe columns? -->

1. (Optioneel) Klik op de naam van het verzoek om een dialoogvenster weer te geven met de volgende informatie: <!-- Check this -->

   * Wanneer een verzoek is begonnen met de verwerking

   * Beperkt tarief: Uw organisatie heeft teveel Data Warehouse verzoeken lopend. Het verzoek wordt gepauzeerd tot andere gegevensverzoeken volledig zijn.

## Verzoeken bewerken

Houd rekening met het volgende wanneer u verzoeken bewerkt:

* Slechts kunnen de verzoeken die worden gevormd om op een programma in werking te stellen worden uitgegeven.

* Niet alle velden die aan de aanvraag zijn gekoppeld, kunnen worden bewerkt. Velden die niet kunnen worden bewerkt, worden grijs weergegeven.

* Beheerders die de aanvraag van een andere gebruiker bewerken, moeten een nieuw account en een nieuwe locatie kiezen waartoe ze toegang hebben.

Een geplande aanvraag bewerken:

1. In Adobe Analytics, uitgezochte [!UICONTROL **Hulpmiddelen**] > [!UICONTROL **Data Warehouse**].

1. Selecteer op de pagina Data Warehouse de aanvraag die u wilt bewerken.

   ![&#x200B; beheer een verzoek &#x200B;](assets/dw-manage-request.png)

1. Selecteer [!UICONTROL **uitgeven**].

1. Bewerk de aanvraag naar wens. De opties voor grijze configuratie kunnen niet worden bewerkt.

   Voor informatie over elke configuratieoptie, zie [&#x200B; een verzoek van de Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

1. Selecteer [!UICONTROL **sparen veranderingen**].

## De geschiedenis van een verzoek weergeven

U kunt de geschiedenis van om het even welke verzoeken van de Data Warehouse bekijken u hebt gemaakt.

1. In Adobe Analytics, uitgezochte [!UICONTROL **Hulpmiddelen**] > [!UICONTROL **Data Warehouse**].

1. Selecteer op de pagina Data Warehouse de aanvraag waarvan u de geschiedenis wilt weergeven.

   ![&#x200B; beheer een verzoek &#x200B;](assets/dw-manage-request.png)

1. Selecteer [!UICONTROL **de geschiedenis van de Mening**].

   De **pagina van het verzoek van de Data Warehouse van 0&rbrace; Mening &lbrace;toont een lijst van individuele rapportleveringen die met het verzoek worden geassocieerd.**

   Selecteer **kolom** pictogram ![&#x200B; vormen kolompictogram &#x200B;](assets/configure-column-icon.png) om kolommen te verbergen of kolommen te tonen die niet door gebrek worden getoond.

   ![&#x200B; de geschiedenispagina van het Verzoek &#x200B;](assets/dw-request-history.png)

   De volgende kolommen zijn beschikbaar:

   | Kolom | Beschrijving |
   |---------|----------|
   | [!UICONTROL **gecreeerd Datum**] | De datum en tijd waarop het rapport is gemaakt.<p>Dit wordt getoond in de tijdzone van de gebruiker die het verzoek in werking stelde.</p> |
   | [!UICONTROL **begonnen Datum**] | De datum en het tijdstip waarop het rapport is gestart.<p>Dit wordt getoond in de tijdzone van de gebruiker die het verzoek in werking stelde.</p> |
   | [!UICONTROL **voltooide Datum**] | De datum en het tijdstip waarop het rapport is voltooid.<p>Dit wordt getoond in de tijdzone van de gebruiker die het verzoek in werking stelde.</p> |
   | [!UICONTROL **Datum bijgewerkt**] | De datum en tijd waarop het rapport voor het laatst is bijgewerkt.<p>Dit wordt getoond in de tijdzone van de gebruiker die het verzoek in werking stelde.</p> |
   | [!UICONTROL **Status**] | De status van de rapportlevering. Mogelijke statussen zijn:<ul><li>[!UICONTROL **Gemaakt**]: Het rapport werd gecreeerd maar is nog niet verwerkt.</li><li>[!UICONTROL **Hangende**]: Het rapport wacht om te worden verwerkt.</li><li>[!UICONTROL **Verwerking**]: Het rapport wordt momenteel verwerkt.</li><li>[!UICONTROL **Voltooid**]: Het voltooide rapport en is nu beschikbaar.</li><li>[!UICONTROL **Gepland**]: Het rapport is gepland maar is nog niet begonnen.</li><li>[!UICONTROL **Geannuleerd**]: Het rapport werd geannuleerd door de gebruiker.</li><li>[!UICONTROL **Fout - Verwerking**:] het rapport ontmoette een fout en kon niet worden verwerkt.</li><li>[!UICONTROL **Fout - het Niet verzenden**]: Het met succes geproduceerde rapport maar kon niet worden geleverd. Controleer de [&#x200B; configuratie van uw bestemming &#x200B;](/help/export/data-warehouse/create-request/dw-request-report-destinations.md), dan verzend het rapport opnieuw.</li></ul>. |
   | [!UICONTROL **van**] | De begindatum van het algemene tijdkader inbegrepen in het rapport.<p>Dit wordt getoond in de tijdzone van de rapportreeks.</p> |
   | [!UICONTROL **aan**] | De einddatum van het algemene tijdkader inbegrepen in het rapport. <p>Dit wordt getoond in de tijdzone van de rapportreeks.</p> |
   | [!UICONTROL **Verouderde verzoek identiteitskaart**] | Identiteitskaart die wordt gebruikt om een rapport in de interface van de erfenisData Warehouse te identificeren. Deze id kan nodig zijn wanneer u contact opneemt met de klantenservice van de Adobe. |
   | [!UICONTROL **identiteitskaart van het Rapport**] | Identiteitskaart die wordt gebruikt om een rapport in de huidige interface van de Data Warehouse te identificeren. Deze id kan nodig zijn wanneer u contact opneemt met de klantenservice van de Adobe. |


1. Selecteer een rapportlevering en selecteer vervolgens een van de volgende opties:

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **de details van de Bestemming**] | Hiermee geeft u de account- en locatiegegevens weer die aan de aanvraag zijn gekoppeld. Dit is de rekening en de plaats die vroeger werd gevormd, zoals die in [&#x200B; wordt beschreven vormen een rapportbestemming voor een verzoek van de Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/dw-request-report-destinations.md). |
   | [!UICONTROL **annuleert rapport**] | Hiermee annuleert u het rapport. U kunt geen rapporten annuleren die een status van [!UICONTROL **Voltooid**] hebben of [!UICONTROL **Geannuleerd**]. |
   | [!UICONTROL **Rerun rapport**] | Voert het rapport opnieuw met de gegevens in werking zoals het was toen het oorspronkelijk werd verzonden. U kunt een rapport opnieuw uitvoeren dat om het even welke volgende statussen heeft: [!UICONTROL **Geannuleerd**], [!UICONTROL **Voltooid**], [!UICONTROL **Fout - Verwerking**], of [!UICONTROL **Fout - Verzenden**]. |
   | [!UICONTROL **het rapport van het Terugsturen**] | Hiermee stuurt u het eerder gegenereerde rapportbestand opnieuw. U kunt een rapport opnieuw verzenden dat om het even welke volgende statussen heeft: [!UICONTROL **Voltooid**] of [!UICONTROL **Fout - Verlies om**] te verzenden. |

## Verzoeken kopiëren

Wanneer u een verzoek kopieert, worden alle configuratieopties gekopieerd van het originele verzoek.

1. In Adobe Analytics, uitgezochte [!UICONTROL **Hulpmiddelen**] > [!UICONTROL **Data Warehouse**].

1. Selecteer op de pagina Data Warehouse de aanvraag die u wilt kopiëren.

   ![&#x200B; beheer een verzoek &#x200B;](assets/dw-manage-request.png)

1. Selecteer [!UICONTROL **Exemplaar**].

   De pagina van het de verzoekverzoek van de Data Warehouse van het Exemplaar toont. Alle configuratieopties worden gekopieerd uit het oorspronkelijke verzoek.

1. Werk om het even welke configuratieopties verbonden aan het verzoek bij.

   Voor informatie over elke configuratieoptie, zie [&#x200B; een verzoek van de Data Warehouse &#x200B;](/help/export/data-warehouse/create-request/t-dw-create-request.md) creëren.

1. Selecteer [!UICONTROL **sparen veranderingen**].

## Aanvragen annuleren

Slechts kunnen de verzoeken die worden gevormd om op een programma in werking te stellen worden geannuleerd.

Een geplande aanvraag annuleren:

1. In Adobe Analytics, uitgezochte [!UICONTROL **Hulpmiddelen**] > [!UICONTROL **Data Warehouse**].

1. Selecteer op de pagina Data Warehouse de aanvraag die u wilt bewerken.

   ![&#x200B; beheer een verzoek &#x200B;](assets/dw-manage-request.png)

1. Selecteer [!UICONTROL **annuleren**].

   De aanvraag wordt niet meer uitgevoerd op het geplande tijdstip.

## Kolommen configureren

U kunt vormen welke informatie voor elk verzoek wordt getoond door kolommen toe te voegen of te verwijderen.

1. Selecteer **kolommen** pictogram in het hoger-recht van de pagina van de Data Warehouse vormen.

   ![&#x200B; vorm kolommen &#x200B;](assets/dw-configure-columns.png)

   De volgende kolommen zijn beschikbaar:

   | Beschikbare kolom | Beschrijving |
   |---------|----------|
   | Naam aanvraag | De naam van de persoon die de aanvraag heeft gemaakt. |
   | Rapportsuite | De rapportsuite die aan de aanvraag is gekoppeld. |
   | Gevraagd door | De gebruiker die de aanvraag heeft gemaakt. |
   | Aanvraagdatum | De datum waarop het verzoek is ingediend. |
   | Status | De volgende statussen zijn beschikbaar:<ul><li><p>**Voltooid**: Het verzoek liep met succes.</p></li><li><p>**Geannuleerd**: Het verzoek werd geannuleerd door de gebruiker.</p></li><li><p>**Gepland**: Het verzoek wordt gevormd om op een programma in werking te stellen.</p></li><li><p>**Ontbroken**: Het verzoek kon niet voltooien. Neem contact op met de Klantenondersteuning als het verzoek blijft mislukken.</p></li></ul> |

   {style="table-layout:auto"}

1. Zorg ervoor dat alle kolommen die u wilt weergeven, zijn geselecteerd. Geselecteerde kolommen worden weergegeven op de pagina Data Warehouse en geven de relevante informatie weer.

## Filteren en sorteren

1. Selecteer het **pictogram van de Filter** in het linkerspoor van de pagina van de Data Warehouse.

   ![&#x200B; verzoeken van de Filter &#x200B;](assets/dw-filter.png)

1. Breid de [!UICONTROL **Reeksen van het Rapport**], [!UICONTROL **Eigenaar**], of [!UICONTROL **Status**] secties uit, dan selecteer hoe u de verzoeken wilt filtreren.

## Zoeken naar aanvragen

1. Geef in het zoekveld boven aan de pagina Data Warehouse de aanvraagnaam op die u wilt weergeven.

   Verzoeken worden tijdens het typen gefilterd.