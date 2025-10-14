---
title: Rapporten exporteren uit Report Builder
description: Beschrijft hoe te om gegevens van Report Builder naar veilige bestemmingen uit te voeren
role: User, Admin
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 5829482b-3a5e-416b-9c82-404face30b29
source-git-commit: ecb08c3d9dfe7394ecff5415c08be7a38b0cba6a
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 0%

---

# Workbooks plannen door naar cloudinstellingen te exporteren

U kunt Adobe Analytics-werkboeken exporteren van Report Builder naar cloudproviders zoals Google, Azure en Amazon.

Alternatief, kunt u werkboeken met anderen delen gebruikend e-mail, zoals die in [&#x200B; werkboeken van het Programma voor het delen door e-mail &#x200B;](/help/analyze/report-builder/schedule-reportbuilder.md) wordt beschreven.

[&#x200B; Voordelen om rapporten van rapportaannemer naar de wolk &#x200B;](#advantages-of-exporting-to-the-cloud) uit te voeren omvatten de capaciteit om rapporten in derdehulpmiddelen te gebruiken of hen te combineren met buitengegevens.

Alvorens u werkboeken van Report Builder naar een wolkenbestemming uitvoert, zorg ervoor dat uw gegevensblokken, uw milieu, en uw toestemmingen aan de [&#x200B; uitvoervereisten &#x200B;](#export-requirements) voldoen.

## Het exportproces begrijpen

Gebruik het volgende proces bij het exporteren van werkboeken van Report Builder naar de cloud:

1. [Een cloudaccount configureren](/help/components/locations/configure-import-accounts.md)

1. [Een locatie op de account configureren](/help/components/locations/configure-import-locations.md)

1. [Een rapport exporteren vanuit Report Builder](#export-a-report-from-report-builder)

## Een rapport exporteren vanuit Report Builder

>[!NOTE]
>
>Alvorens u gegevens uitvoert zoals die in deze sectie worden beschreven, leer meer over [&#x200B; het de uitvoerproces &#x200B;](#understand-the-export-process) in de sectie hierboven.

Rapporten exporteren uit Report Builder:

1. Als u niet reeds hebt, vorm een de uitvoerrekening en plaats, zoals die in [&#x200B; wordt beschreven vormt de rekeningen van de wolkenuitvoer &#x200B;](/help/components/locations/configure-import-accounts.md).

1. Open het rechterdeelvenster van **[!UICONTROL Adobe Report Builder]** in het Excel-werkblad dat de gegevens bevat die u wilt exporteren.

1. Selecteer [!UICONTROL **Programma**].

<!-- add screenshot -->

1. Selecteer op het tabblad **[!UICONTROL Workbooks]** het plusteken om een nieuw schema te maken

   ![&#x200B; de bouwerprogramma&#39;s tabel van het Rapport &#x200B;](assets/report-builder-schedule-cloud.png)

   of

   Om het werkboek op een programma uit te voeren dat u reeds creeerde, selecteer het programma van de lijst van programma&#39;s, dan uitgezocht **[!UICONTROL Send on schedule]**.

1. In het **juiste paneel van Adobe Report Builder** &lbrace;, specificeer de volgende informatie verder creërend een nieuw programma:

   | Veldnaam | Functie |
   |---------|----------|
   | **[!UICONTROL File]** | Toont het werkboekdossier dat momenteel voor de uitvoer wordt geselecteerd. Selecteer het werkboekpictogram ![&#x200B; TableSelect &#x200B;](/help/assets/icons/TableSelect.svg) naast de dossiernaam om het huidige werkboek te kiezen als het niet reeds wordt geselecteerd. |
   | **[!UICONTROL Filename]** <!--should be File name --> | Staat u toe om filename te veranderen alvorens het werkboek uit te voeren.<p>De naam van het werkboekdossier blijft aan de naam van het werkboek in gebreke</p> |
   | **[!UICONTROL File type]** | Kies het bestandstype voor het geëxporteerde bestand. U kunt Excel, PDF of CSV kiezen.<p>Wanneer u **[!UICONTROL CSV]** selecteert, houd er rekening mee dat het geplande werkboek als gehechtheid van het PIT wordt verzonden. Sommige e-mailbeheerders van bedrijven kunnen e-mailberichten blokkeren met ZIP-bijlagen. U ziet een waarschuwing op basis hiervan.</p> |
   | **[!UICONTROL Append time stamp to file name]** | Selecteer deze optie als u een tijdstempel van de exportbewerking wilt opnemen in de naam van het geëxporteerde bestand. |
   | **[!UICONTROL Filename preview]** <!--should be File name preview --> | Hiermee geeft u een voorbeeld weer van de manier waarop de bestandsnaam na het exporteren wordt weergegeven. |
   | **[!UICONTROL Password protect the workbook]** | Geef een wachtwoord op om het geëxporteerde bestand te beveiligen, zodat alleen mensen met het wachtwoord toegang hebben tot het bestand. <p>Wachtwoorden moeten ten minste 8 tekens hebben en ten minste 1 cijfer en 1 speciaal teken (zoals `!` , `@` , `#` en `$` ) bevatten.</p> |
   | **[!UICONTROL Email]** | Selecteer deze optie als u het bestand naar een specifiek e-mailadres wilt verzenden. Voor meer informatie over deze optie, zie [&#x200B; werkboeken van het Programma door e-mail &#x200B;](/help/analyze/report-builder/schedule-reportbuilder.md) te delen. |
   | **[!UICONTROL Other deliveries]** | Selecteer deze optie als u het bestand naar een cloudaccount wilt verzenden en selecteer de account en locatie in de vervolgkeuzemenu&#39;s **[!UICONTROL Account]** en **[!UICONTROL Location]** die hieronder worden beschreven. |
   | **[!UICONTROL Account]** | Selecteer de exportaccount voor de cloud waarin u de gegevens wilt verzenden. <p>Of als u nog geen cloudaccount hebt geconfigureerd die u wilt gebruiken, kunt u een nieuwe account configureren:<ol><li>Selecteer [!UICONTROL **toevoegen rekening**], dan specificeer de volgende informatie:<ul><li>[!UICONTROL **de rekeningsnaam van de Plaats**]: Specificeer een naam voor de plaatsrekening. Deze naam wordt weergegeven wanneer u een locatie maakt </li><li>[!UICONTROL **de rekeningsbeschrijving van de Plaats**]: Verstrek een korte beschrijving van de rekening helpen het van andere rekeningen van het zelfde rekeningtype onderscheiden.</li><li>**[!UICONTROL Make account available to all users in your organization]**: Selecteer deze optie als u wilt dat andere gebruikers in uw organisatie de account kunnen gebruiken. Houd rekening met het volgende wanneer u accounts deelt:<ul><li>Accounts die u deelt, kunnen niet worden verwijderd.</li><li>Gedeelde accounts kunnen alleen door de eigenaar van de account worden bewerkt.</li><li>Iedereen kan een locatie voor de gedeelde account maken.</li></ul></li><li>[!UICONTROL **het type van Rekening**]: Selecteer het type van wolkenrekening die u naar uitvoert. Beschikbare accounttypen zijn Amazon S3 Role ARN, Google Cloud Platform, Azure SAS en Azure RBAC.</li></ul><li>Om uw rekening te voltooien vormen, ga met Stap 6 in [&#x200B; verder de invoer en de uitvoerrekeningen van de wolk &#x200B;](/help/components/locations/configure-import-accounts.md) vormen, dan breid de sectie uit die aan het [!UICONTROL **type van Rekening**] beantwoordt u selecteerde. <p>De volgende accounttypen zijn beschikbaar:</p><ul><li>Amazon S3 Role ARN</li><li>Google Cloud Platform</li><li>Azure SAS</li><li>Azure RBAC</li></ul></ol> |
   | **[!UICONTROL Location]** | Selecteer de locatie op de account waarnaar u de exportgegevens wilt verzenden.<p>Of, als u niet reeds de plaats hebt gevormd die u op de rekening wilt gebruiken die u selecteerde, kunt u een nieuwe plaats vormen:<ol><li>Selecteer [!UICONTROL **plaats**] toevoegen, dan specificeer de volgende informatie: <ul><li>[!UICONTROL **Naam**]: De naam van de plaats.</li><li>[!UICONTROL **Beschrijving**]: Verstrek een korte beschrijving van de plaats helpen het van andere plaatsen op de rekening onderscheiden.</li><li>**[!UICONTROL Make location available to all users in your organization]**: Selecteer deze optie als u wilt dat andere gebruikers in uw organisatie de locatie kunnen gebruiken. Houd rekening met het volgende wanneer u accounts deelt:<ul><li>Locaties die u deelt, kunnen niet worden verwijderd.</li><li>Gedeelde locaties kunnen alleen door de eigenaar van de account worden bewerkt.</li><li>Locaties kunnen alleen worden gedeeld als de account waaraan de locatie is gekoppeld, ook wordt gedeeld.</li></ul></li><li>[!UICONTROL **rekening van de Plaats**]: Selecteer de rekening waar u de plaats wilt tot stand brengen.</li></ul><li>Om uw plaats te beëindigen vormen, ga met de verbinding hieronder voort die aan het accounttype beantwoordt dat u op het [!UICONTROL **de rekening van de Plaats**] gebied selecteerde:<ul><li>[&#x200B; Amazon S3 Rol ARN &#x200B;](/help/components/locations/configure-import-locations.md#amazon-s3-role-arn)</li><li>[&#x200B; Google Cloud Platform &#x200B;](/help/components/locations/configure-import-locations.md#google-cloud-platform)</li><li>[&#x200B; Azure SAS &#x200B;](/help/components/locations/configure-import-locations.md#azure-sas)</li><li>[&#x200B; Azure RBAC &#x200B;](/help/components/locations/configure-import-locations.md#azure-rbac)</li></ul> |
   | **[!UICONTROL Show scheduling options]** | Selecteer deze optie om extra opties voor het plannen van de uitvoer te bekijken. Laat deze optie uitgeschakeld als u de exportbewerking maar één keer wilt verzenden. Wanneer deze optie is uitgeschakeld, wordt het exporteren onmiddellijk gestart. |
   | **[!UICONTROL Starting on]** | De dag en tijd waarop de geplande export moet beginnen. <p>Deze optie is alleen beschikbaar wanneer u een geplande exportfrequentie kiest.</p> |
   | **[!UICONTROL Ending on]** | De dag en tijd waarop de geplande export verloopt. De geplande export wordt niet meer uitgevoerd na de datum en tijd die u instelt. <p>Deze optie is alleen beschikbaar wanneer u een geplande exportfrequentie kiest.</p> |
   | **[!UICONTROL Frequency]** | U kunt de frequentie instellen op uurbasis, dagelijks, wekelijks, maandelijks of jaarlijks op een bepaalde dag. Bijvoorbeeld, kunt u opstelling een programma om het werkboek op de eerste Zondagnacht van de maand te verzenden zodat uw ontvangers de e-mail in hun inbox eerste ding op Maandmorgen hebben. |

   {style="table-layout:auto"}

1. Selecteer [!UICONTROL **verzenden op programma**] om het werkboek uit te voeren.

   Gegevens worden verzonden naar de cloudaccount die u hebt opgegeven met de opgegeven frequentie.

   U ziet een bevestigingstoets bij de bodem van de hub van Report Builder en het geplande werkboek is vermeld onder het lusje van Werkboeken.

## Voordelen van exporteren naar de cloud

Door Adobe Analytics-gegevens naar de cloud te exporteren, kunt u:

* Exporteer naar een gedeelde locatie, zoals Google Cloud Platform, Microsoft Azure en Amazon S3.

* Sla grote hoeveelheden historische gegevens op.

  Dit type van gegevens kan worden gebruikt om tendensen op lange termijn te ontdekken om bedrijfsintelligentie te bereiken, en uiteindelijk tot betere bedrijfsbesluitvorming te leiden.

* Berekende metriek opnemen in de geëxporteerde Adobe Analytics-gegevens.

* De gegevensoutput van de structuur als samengevoegde waarden.

* Eén keer of volgens een schema exporteren.

* Exporteer bestanden in Excel-, PDF- of CSV-indeling.

* Exporteer gegevensblokken met meerdere afmetingen.

## Exportvereisten {#export-requirements}

### Minimumvereisten

Zorg ervoor dat uw gegevensblokken, uw omgeving, en uw toestemmingen aan de volgende vereisten voldoen:

* **blokken van Gegevens:** Alle gegevensblokken moeten minstens één component aan een kolom, een rij, of een waarde omvatten.

* **Milieu:** zorg ervoor dat de [&#x200B; IP adressen &#x200B;](/help/technotes/ip-addresses.md) en [&#x200B; Domeinen &#x200B;](/help/technotes/domains.md) die door Adobe Analytics worden gebruikt door de firewall van hun organisatie worden toegestaan.


<!--
## Manage exports

After data is exported from Analysis Workspace, you can edit, re-export, duplicate, tag, or delete existing exports, as described in [Manage exports](/help/components/exports/manage-exports.md). 

-->

## Geplande werkboeken beheren

Voor informatie over het beheren van werkboeken die reeds gepland zijn, zie [&#x200B; geplande werkboeken beheren &#x200B;](/help/analyze/report-builder/manage-schedules-reportbuilder.md).
