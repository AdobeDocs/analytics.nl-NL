---
title: Overzicht van classificatiesets
description: Leer hoe u classificatiesets kunt gebruiken om classificatiegegevens te beheren. Begrijp hoe classificatiesets verschillen van oudere classificaties.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
feature: Classifications
source-git-commit: 77599d015ba227be25b7ebff82ecd609fa45a756
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Overzicht van classificatiesets

Classificatiesets bieden één interface voor het beheer van classificaties en regels. Dit werkschema combineert de verwezenlijking van classificaties in de reeksinstellingen van het Rapport met [&#x200B; de invoerder van de Classificatie &#x200B;](/help/components/classifications/sets/manage/set-manager.md). Het resultaat is één intuïtieve interface voor het maken en beheren van classificatiegegevens.


## Classificatiesets versus oudere classificaties

Het belangrijkste verschil tussen classificatiesets en oudere classificaties is de relatie van de classificaties met een rapportenpakket.

In verouderde classificaties, is elke classificatie direct verbonden met een rapportreeks. Zeer gelijkaardige classificaties (bijvoorbeeld voor een productcatalogus) worden herhaald wanneer gebruikt over veelvoudige rapportreeksen.

![&#x200B; Verouderde classificatie &#x200B;](manage/assets/classifications-legacy.svg)

In classificatiesets definieert u abonnementen van rapportsuites en combinaties van belangrijke dimensies. Bijvoorbeeld, moet een classificatie van de productcatalogus die voor veelvoudige rapportreeks van toepassing is u slechts eenmaal als classificatieset bepalen. En binnen die classificatiereeks vormt u veelvoudige rapporten reeksen en zeer belangrijke afmetingscombinaties om aan die classificatiereeks in te tekenen.

![&#x200B; de reeksen van de Classificatie &#x200B;](manage/assets/classifications-sets.svg)


Als u **[!UICONTROL Classification sets]** wilt openen vanuit het menu **[!UICONTROL Components]** in de Adobe Analytics-interface, moet u een productbeheerder zijn of behoren tot een productprofiel dat het machtigingsitem [!UICONTROL Report Suite Tools] > [!UICONTROL Classifications] bevat. Let op: oudere interfaces voor classificatiebeheer zijn beschikbaar in het menu **[!UICONTROL Admin]** .

Indelingssets bestaan uit drie functionele gebieden:

* [**[!UICONTROL Classification Sets]**](manage/set-manager.md): classificatiesets maken, bewerken en verwijderen.
* [**[!UICONTROL Jobs]**](job-manager.md): bekijk de status van classificatiesets taken.
* [**[!UICONTROL Consolidations]**](consolidations/manage.md): combineer meerdere classificatiesets tot één classificatieset.


## Workflow

De workflow voor classificatiesets bestaat meestal uit de volgende stappen:

1. Overweeg voor welke rapportsuite en dimensiecombinaties u een classificatieset wilt maken. Een voorbeeld hiervan is het definiëren van een productclassificatieset dat u maakt voor elke rapportsuite waarvoor u producten met meer details wilt classificeren. Bijvoorbeeld details zoals categorie en kleur.
1. [&#x200B; creeer een classificatiereeks &#x200B;](/help/components/classifications/sets/manage/create.md) met abonnementen voor één of meerdere rapportreeks en afmetingscombinaties die producten identificeren. Bijvoorbeeld:

   | Rapportsuite | Key Dimension |
   |---|---|
   | Rapportsuite 1 | Product-id |
   | Rapportsuite 2 | Product-SKU |

1. [&#x200B; voeg de classificaties &#x200B;](/help/components/classifications/sets/manage/schema.md#add) toe die u aan het schema van de classificatieset hebt geïdentificeerd. Bijvoorbeeld:

   | Classificatienaam | Identiteitsnaam |
   |---|---|
   | Categorie | categorie |
   | Kleur | kleur |

1. Maak handmatig een bestand met classificatiegegevens. [&#x200B; Gebruik een malplaatje &#x200B;](/help/components/classifications/sets/manage/schema.md#template) om u te verzekeren gebruikt het [&#x200B; gesteunde dossierformaat &#x200B;](data-files.md#classification-set-file-formats) en kolommen voor het dossier. Voeg vervolgens de gegevens toe aan het sjabloonbestand.

   Alternatief kunt u gegevens van uw productcatalogus in de [&#x200B; gesteunde dossierformaten &#x200B;](data-files.md#classification-set-file-formats) met kolommen direct uitvoeren die aan het malplaatje aanhangen. Bijvoorbeeld een CSV-bestand, zoals:

   ```
   Key,Category,Color
   Adobe Nike Tech Fleece Full-Zip Hoodie - Men's,Men,Black
   Adobe Nike Tech Fleece Full-Zip Hoodie - Women's,Women,Black
   Men's North Face Adobe Jacket,Men,Black
   Nike Air Hybrid 2 Golf Bag,Equipment,Blue
   STITCH&reg; Ultimate Garment Bag,Equipment,Brown
   Adobe Analytics Training Tee - Navy,Men,Navy
   AirPods Pro 2,Electronics,White
   Adobe Analytics Training Tee - Green,Men,Green
   Women's North Face Adobe Jacket,Women,Blue
   Adobe Analytics Training Tee - Grey,Men,Gray
   Adobe Analytics One Million Views - Grey,Equipment,Grey
   Adobe and MGM Tee - White,Women,White
   Adobe and MGM Tee - Charcoal,Women,Charcoal
   ```

1. [&#x200B; uploadt &#x200B;](/help/components/classifications/sets/manage/schema.md#upload) het dossier dat de classificatiegegevens in het schema van de classificatieset bevat.

1. [&#x200B; Automate &#x200B;](/help/components/classifications/sets/manage/schema.md#automate) het proces van updates aan uw productcatalogus die u weerspiegeld in classificatiegegevens door het gebruik van een wolkenplaats wilt zien.

1. [&#x200B; Download &#x200B;](/help/components/classifications/sets/manage/schema.md#download) uw classificatiegegevens om de inhoud te bevestigen.

1. [&#x200B; inspecteer de baangeschiedenis &#x200B;](/help/components/classifications/sets/job-manager.md) om uw acties (de invoer, de uitvoer, en meer) op classificaties te zien.
1. Als u veelvoudige gelijkaardige classificatiereeksen als resultaat van een migratie van de functionaliteit van de erfenisclassificatie hebt, [&#x200B; consolideert &#x200B;](consolidations/manage.md) deze classificatiereeksen.



## Verbeteringen

De backend architectuur die met classificatiesets wordt vrijgegeven bevat verscheidene verbeteringen:

* Verminderde verwerkingstijd (van 72 uur tot 24 uur).
* Een vernieuwde gebruikersinterface voor het beheer van classificaties.
* De optie om classificatiegegevens in Adobe Experience Platform door de [&#x200B; bron van Adobe Analytics schakelaar voor classificatiegegevens &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/connectors/adobe-applications/classifications) te gebruiken.

De backend architectuur die met classificatiesets wordt vrijgegeven bevat ook verscheidene veranderingen:

* **[!UICONTROL Overwrite on conflict]** wordt altijd ingeschakeld wanneer u de browser of de automatische importbewerking gebruikt.
* Wanneer u de browser of de automatische importfunctie gebruikt, wordt de optie om direct na het importeren te exporteren niet meer ondersteund. De uitvoer moet afzonderlijk worden geïnitieerd.
* Het API-eindpunt Analytics 2.0 `GetDimensions` retourneert nu tekenreeks-id&#39;s voor classificaties in plaats van numerieke id&#39;s. Numerieke id&#39;s kunnen nog steeds worden gebruikt, maar het wordt aanbevolen om waar mogelijk de nieuwe tekenreeks-id&#39;s te gebruiken. Numerieke id&#39;s kunnen worden opgehaald met de parameter voor de querytekenreeks `?expansion=hidden` .

>[!IMPORTANT]
>
>De prestaties van classificatiesets zijn voornamelijk afhankelijk van het aantal unieke sleutelwaarden die gegevens bevatten. Wees voorzichtig wanneer u variabelen hebt die grote aantallen unieke waarden bevatten. Vooral wanneer u dergelijke variabelen van veelvoudige rapportreeksen en dimensies in één enkel classificatieset combineert.

## Beperkingen

* Classificatiesets ondersteunen nog geen regels. De functionaliteit van regels wordt toegevoegd aan de interface van classificatiesets alvorens de [&#x200B; functionaliteit van de bouwer van de erfenisregel &#x200B;](/help/components/classifications/crb/classification-rule-builder.md) niet beschikbaar wordt.
* Er is geen migratie van oude classificatieregels en configuraties naar classificatiesets. Een migratienut wordt toegevoegd aan de interface van classificatiesets alvorens de functionaliteit van de erfenisclassificatie niet beschikbaar wordt.
