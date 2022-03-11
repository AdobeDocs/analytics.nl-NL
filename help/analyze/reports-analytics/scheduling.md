---
description: Informatie over het plannen, downloaden en verspreiden van rapporten.
subtopic: Schedule
title: Rapport Planning en distributie
uuid: 1230b0f3-e026-4b83-b231-14d6f75a3836
feature: Reports & Analytics Basics
role: User, Admin
exl-id: ec59d365-f294-41da-ae36-3b4ebe64ab23
source-git-commit: 000d9aedbe8d3ac109be472d9e29f7798f86baa7
workflow-type: tm+mt
source-wordcount: '1674'
ht-degree: 1%

---

# Rapport Planning en distributie

Informatie over het plannen, downloaden en verspreiden van rapporten.

>[!IMPORTANT]
>Met ingang van 15 april 2022 is Adobe voornemens alle geplande rapporten met een aanmaakdatum van meer dan twee jaar te onderbreken (alle taken die vóór 31 januari 2020 zijn gemaakt). Er worden geen rapporten of gegevens verwijderd. Alleen rapporten die ouder zijn dan twee jaar worden gepauzeerd en er worden geen aanvullende geplande rapporten verzonden. [Meer informatie](/help/analyze/reports-analytics/scheduled-reports-eol.md)

Wanneer u een rapport voor levering in een toepassing van Adobe Analytics plant, kunt u de Plannende en hulpmiddelen van de Distributie gebruiken om te bekijken welke dossiers automatisch zijn verzonden en de leveringen te wijzigen of te eindigen.

Vanwege verschillen in verwerkingsmechanismen en platforms hebben de verschillende typen downloadbare en geplande rapporten die beschikbaar zijn in Adobe Analytics, verschillende beperkingen met betrekking tot het maximumaantal rijen dat ze in één aanvraag kunnen verwerken. Hier zijn de limieten van elk:

* Word, CSV, Excel, HTML en PDF: Het zelfde aantal rijen zichtbaar in het rapport. Deze limiet is standaard ingesteld op 50 rijen, maar kan worden verhoogd tot 200. Uitsplitsingsrapporten hebben een harde limiet van 50 rijen.
* Gegevens extraheren: 50.000 rijen
* Data Warehouse: Onbeperkt

Deze beperkingen gelden voor afzonderlijke geplande en gedownloade rapporten; dashboards zijn beperkt tot de hoeveelheid ruimte beschikbaar binnen een rapport.

## Leveringstijd versus verwerkingstijd

De &quot;Tijd van de Levering&quot;of &quot;Tijd van Dag&quot;ingegaan door de gebruiker specificeert de tijd dat het rapport met verwerking zou moeten beginnen, niet de tijd dat het daadwerkelijk zal worden geleverd. Wanneer het verslag wordt uitgebracht, is het in de eerste plaats gebaseerd op de tijd die het kost om te verwerken. Het verwerken van complexe en grote rapporten duurt langer dan het vereenvoudigen van rapporten. Bijvoorbeeld, als een rapport 15 minuten aan verwerking vergt, dan zal de daadwerkelijke leveringstijd minstens 15 minuten voorbij de oorspronkelijk gespecificeerde &quot;Tijd van de Levering&quot;of &quot;Tijd van Dag&quot;zijn.

Bovendien zijn er een aantal andere factoren die de vertraging nog kunnen vergroten voordat het verslag daadwerkelijk wordt uitgebracht:

* **Vele verschillende programma&#39;s van het zelfde type tezelfdertijd in werking stellen** (bijvoorbeeld veel dashboards enz.) kan het systeem overladen. Het planningssysteem staat slechts een paar (5-10) rapporten van om het even welk één type toe om gelijktijdig te lopen. Wanneer meer dan 5-10 allen in één keer gepland zijn, zullen sommigen in lijn op andere rapporten moeten wachten te beëindigen alvorens zij met verwerking kunnen beginnen. Deze kwestie kan worden verlicht door de rapporten van een bedrijf op gestaffelde tijden door dag of uur, eerder dan gelijktijdig te plannen.
* Naast het specifieke rapporttype (dashboards, enz.), zullen de rapporten ook in lijn wachten als het bedrijf heeft **meer dan 15-20 van om het even welk type van rapport dat tegelijkertijd (over alle verschillende rapporttypes) wordt gepland**. Dit kan worden verlicht door onthutsende planningstijden in plaats van vele tezelfdertijd te hebben lopen.
* **Problemen bij downstreamdiensten** dat de Planner zich op baseert ook levering van rapporten kan beïnvloeden. Bijvoorbeeld, als u onafhankelijk APIs gebruikt om rapporten in werking te stellen en de API verzoekrij te vullen, dan kunnen uw geplande rapporten langzaam leveren terwijl u voor die bron concurreert.
* **Vertraging rapportsuite** (een vertraging in het verzamelen van gegevens) kan sommige geplande rapporten ook vertragen.


## Een rapport verzenden {#task_27642CD33D484FD0BF59EBD159EEF52C}

Stappen die beschrijven om rapporten in een verscheidenheid van formaten te downloaden en te e-mailen, en een rapport voor levering te plannen.

1. Voer een rapport uit en klik op **[!UICONTROL More]** > **[!UICONTROL Send]**.
1. Geef leveringsopties op:

   | Optie | Beschrijving |
   |--- |--- |
   | Indeling | Selecteer PDF of HTML. |
   | Verzenden naar | Geef een e-mailadres op waarop u het rapport wilt ontvangen. |
   | Onderwerp | Onderwerp van de e-mail. |
   | Planning | Selecteer deze optie om het rapport direct of met een ander interval te verzenden. |

1. Klikken **[!UICONTROL Advanced Delivery Options]** om een leveringsschema op te geven.

| Optie | Beschrijving |
| --- |--- |
| Rapportbestandsnaam | Specificeert de naam van het rapport. De standaardindeling is `<report name> for <suite> - <report date range>`. Als u een aangepaste naam wilt opgeven, selecteert u [!UICONTROL Custom]. |
| Rapportindeling | Hier kunt u de indelingen PDF, CSV, Excel, HTML, Word of Mobiel opgeven voor levering. Als u CSV selecteert, kunt u ook de codering voor CSV opgeven:<ul><li>Shift-JIS: Japanse tekencodering.</li><li>EUC-JP: Uitgebreide Unix-code, voornamelijk voor Japans, Koreaans en Vereenvoudigd Chinees.</li></ul> |
| Rapportinhoud | <ul><li>Aantal rijen in de tabel: Hiermee geeft u het aantal rijen op dat zichtbaar moet zijn in de tabel van het rapport dat u verzendt.</li><li>Taal voor kop- en voettekst: Hier geeft u de taal van de kop- en voettekst op.</li><li>Opmerkingen: Geeft de tekst aan die aan het begin van het rapport wordt weergegeven.</li></ul> |
| Digitale handtekeningbestand verzenden | Wanneer u een rapport opvraagt, zoals een rapport met bladwijzer of verzoeken om een Data Warehouse, kunt u een gegevenshandtekening aanvragen. De Adobe beperkt de toegang tot de gegevens niet, maar het doel van het Digitale Dossier van de Handtekening (.sig) is de geldigheid van het geleverde rapportdossier te verifiëren. Met de digitale handtekening kunnen rapportontvangers controleren of het bestand afkomstig is van Adobe en niet is gewijzigd. |
| Doel rapporteren | <ul><li>E-mail: Hiermee kunt u instellingen voor e-mailadressen, de onderwerpregel en notities configureren.</li><li>FTP: Hiermee kunt u FTP-instellingen configureren, waaronder de host, poort, map, gebruikersnaam en wachtwoord.</li></ul> |

1. Klik op **[!UICONTROL Scheduling Options]**.

| Optie | Beschrijving |
|--- |--- |
| Rapport nu verzenden | Verzendt het rapport onmiddellijk. |
| Plan voor later | Geeft opties weer om een tijdframe en leveringsopties op te geven. |
| Tijdschema rapport | **Vast**: Voorkomt dat de datum vooruit gaat naarmate de tijd verstrijkt. **Rollen**: Hiermee kan de datum worden vervroegd in de tijd. Enkele overwegingen:<ul><li>Als u Rolling voor zowel de begin als einddata selecteert, en u een dagrapport voor de vorige dag selecteert, ontvangt u elke dag een e-mail met een rapport voor de vorige dag.</li><li>Als u Vast voor de beginnende dag selecteert, en het rollen voor de einddag, ontvangt u op de eerste dag een rapport voor de vorige dag. De tweede dag ontvangt u een rapport voor de vorige twee dagen, en op de derde dag ontvangt u een rapport voor de vorige drie dagen, etc.</li><li>Als u Vast hebt geselecteerd voor zowel de begin- als de einddatum, ontvangt u elke dag een identiek rapport voor de opgegeven dagen.</li><li>U kunt geen schuivende begindatum en een vaste einddatum selecteren.</li></ul> |
| Leveringsfrequentie | <ul><li>**Uur**: Levert e-mail elk uur, om het even welk ander uur, of een ander interval van uren.</li><li>**Dagelijks**: Verzendt de e-mail elke dag, elke andere dag, elke derde dag, of om het even welk ander interval van dagen. U kunt het ook elke weekdag laten verzenden.</li><li>**Wekelijks**: Verzendt het e-mailbericht elke week, andere week, elke derde week of elk ander interval van weken. U kunt ook opgeven welke dag van de week het wordt verzonden.</li><li>**Maandelijks**: Hiermee geeft u het interval op in een aantal maanden en u kunt ook de dag van de maand selecteren waarop de gegevens worden verzonden, of de dag van de week in een bepaalde week van de maand.</li><li>**Jaarlijks**: Hier geeft u de dag op van het jaar waarin het rapport wordt verzonden. U kunt dit ook doen op een bepaalde dag van de week in een willekeurige week van het jaar.</li><li>**Dag**: Is op de tijdzone van toepassing verbonden aan de geselecteerde rapportreeks.</li></ul> |
| Opties voor eindaflevering | <ul><li>**Nooit einde**: Geeft geen einde aan.</li><li>**Einde na `value` voorkomen**: Hier geeft u het aantal exemplaren op voordat de levering wordt beëindigd.</li><li>**Eindigen op**: Hier kunt u een specifieke datum opgeven. Als u de gegevens op de zelfde datum wilt verwerken zoals de rapportgegevens, bevat het rapport slechts gegevens die in het gegevensbestand op het tijdstip zijn gezet het rapport wordt verzonden. Omdat de volledige verwerking voor een dag tot 24 uren kan vergen, zouden de volledige gegevens niet op het tijdstip kunnen beschikbaar zijn het rapport wordt verzonden. Voor volledige gegevens stelt u altijd de verwerkingstijd in gedurende 24 uur na het einde van de verslagperiode.</li></ul> |

## Een rapport afdrukken {#task_0F7CF6D6ED54462CAE4A793E271AF7E5}

Stappen die beschrijven hoe te om een rapport te drukken.

1. Voer een rapport uit.
1. Klik op **[!UICONTROL More]** > **[!UICONTROL Print]**.  ![](assets/print.png)

## Een rapport downloaden met gebruik van basisopties {#task_43660107A1C9485D92981CD75B562577}

Download gedetailleerde informatie over een specifiek rapport in de indelingen PDF, CSV, Excel of Raw Data Export.

1. In  **[!UICONTROL Analytics]** > **[!UICONTROL Reports]** selecteert u een rapport dat u wilt weergeven.
1. Klik op **[!UICONTROL Download]**.

   ![](assets/download_basic.png)

1. Selecteer het gewenste formaat voor het rapport:

   * **[!UICONTROL PDF]**: Specificeert dat het rapport in Adobe PDF zal worden gedownload, wat u het rapport met anderen laat delen, ongeacht welk computersysteem de ontvanger loopt.
   * **[!UICONTROL CSV]**: Geeft aan dat het rapport wordt gedownload in [!DNL .csv] (indeling met door komma&#39;s gescheiden waarden).
   * **[!UICONTROL Excel]**: Specificeert dat het rapport in het formaat van Microsoft Excel zal worden gedownload, dat u het rapport met anderen laat delen die het in een spreadsheetprogramma kunnen openen.
   * **[!UICONTROL Word]**: Geeft op dat het rapport wordt gedownload in de Microsoft Word-indeling.

   >[!NOTE]
   >
   >Als u een rapport downloadt met een van de onbewerkte exportindelingen en de paginanaam leeg is, heeft Adobe Analytics waarschijnlijk niet genoeg tijd om de gegevens te verwerken. Download het rapport op een later tijdstip.

## Geplande rapporten beheren {#task_C17677C543454FF2B06D10EA5652DFBC}

Informatie over het beheren van geplande rapporten.

In de [!UICONTROL Schedule Reports Manager], kunt u terugkerende rapportleveringen uitgeven en schrappen. U kunt leveringsschema&#39;s maken die uw rapporten via e-mail of FTP naar een opgegeven adres verzenden. U kunt deze programma&#39;s vormen om de rapporten met gespecificeerde intervallen voor een tijdsduur of voor onbepaalde tijd automatisch te verzenden, of de levering van een terugkerend rapport tegen te houden.

De [!UICONTROL Schedule Report Manager] toont de punten die een specifieke gebruiker heeft gecreeerd. Als de gebruikersaccount in de toepassing is uitgeschakeld, worden alle geplande leveringen gestopt.

1. Als u de manager wilt openen, klikt u op **[!UICONTROL Analytics]** > **[!UICONTROL Components]** > **[!UICONTROL All components]** > **[!UICONTROL Scheduled reports]**.

## Een rapportkoppeling delen {#task_9711DDE9E140451B8C914EC5513E21EC}

Stappen die beschrijven hoe te om een rapport te delen door een rapportverbinding (URL) te produceren om naar een andere gebruiker te verzenden.

Wanneer de ontvanger op de koppeling klikt, vraagt het systeem aanmeldingsgegevens aan (bedrijfsnaam, gebruikersnaam en wachtwoord). Na het programma openen, wordt de ontvanger getoond het rapport dat door de originele gebruiker wordt geproduceerd. Standaardmachtigingsbeperkingen zijn van toepassing.

Een rapportkoppeling delen

1. Voer een rapport uit.
1. Klik op **[!UICONTROL More]** > **[!UICONTROL Link to This Report]**.

## Abonnement op geplande rapporten opzeggen {#concept_6B48360F935740B6851BA85D32DEF637}

U kunt uw abonnement op geplande rapporten opzeggen. U zult niet meer het rapport ontvangen zelfs als uw gebruikersnaam aan het geplande rapport opnieuw wordt toegevoegd.

>[!IMPORTANT]
>
>Om u het rapport opnieuw te ontvangen, moet een nieuw programma worden gecreeerd.

Abonnement op een gepland rapport opzeggen:

1. Breng het e-mailbericht naar de koppeling naar het rapport waarvan u het abonnement wilt opzeggen.

   ![](assets/unsubscribe-email.png)

1. Klik op de knop **[!UICONTROL click here]** koppeling naast **[!UICONTROL To cancel automatic delivery of this report]**.

1. Bevestig dat u de levering van het rapport wilt annuleren.

   >[!NOTE]
   >
   >Dit werkschema is het zelfde of u de rapportplanner of de rapportontvanger bent.

Als u het abonnement op een rapport opzegt, wordt het geplande rapport niet geannuleerd.

Om een gepland rapport te annuleren, navigeer aan de Manager van het Programma en klik op rode X naast de rapportnaam. [Meer...](/help/analyze/reports-analytics/scheduling.md#task_C17677C543454FF2B06D10EA5652DFBC)
