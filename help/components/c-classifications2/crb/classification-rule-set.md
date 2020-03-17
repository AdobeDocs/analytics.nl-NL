---
description: Een regelset is een groep classificatieregels voor een specifieke variabele. U past een variabele op de regelreeks toe. Als u veelvoudige regelreeksen voor één variabele wilt tot stand brengen, moet u elke regel toepassen die op veelvoudige rapportreeksen wordt geplaatst.
subtopic: Classifications
title: Classificatiereeksen
topic: Admin tools
uuid: c4d7b77c-fa98-44be-955f-9aee7f73480b
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Classificatiereeksen

Een regelset is een groep classificatieregels voor een specifieke variabele. U past een variabele op de regelreeks toe. Als u veelvoudige regelreeksen voor één variabele wilt tot stand brengen, moet u elke regel toepassen die op veelvoudige rapportreeksen wordt geplaatst.

## Classificatiereeksen

Een regelset is een groep classificatieregels voor een specifieke variabele. U past een variabele op de regelreeks toe. Als u veelvoudige regelreeksen voor één variabele wilt tot stand brengen, moet u elke regel toepassen die op veelvoudige rapportreeksen wordt geplaatst.

## Pagina met indelingsregels {#section_C60B0888C76D49C596EF19F11808B718}

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

De volgende velden en opties zijn beschikbaar op de [!UICONTROL Classifications Rule Builder]website.

<table id="table_A5D92409969747E39E041216A5AA32CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="/help/components/c-classifications2/crb/classification-rule-set.md"  > Regelset toevoegen</a> </p> </td> 
   <td colname="col2"> <p>Maakt een regelset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Regels </p> </td> 
   <td colname="col2"> Geeft het aantal regels in de set weer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> Toont de activiteitenstatus van de regelreeks, zoals Ontwerp of Actief. De actieve regels verwerken dagelijks, onderzoek classificatiegegevens die typisch één maand teruggaan. De regels controleren automatisch op nieuwe waarden en uploaden de classificaties. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Laatst gewijzigd </p> </td> 
   <td colname="col2"> Geeft aan wanneer de regelset is bewerkt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dupliceren </p> </td> 
   <td colname="col2"> Dupliceert (kopieert) een regelreeks, zodat u de regel kunt toepassen die aan een andere variabele, of aan de zelfde variabele in een verschillende rapportreeks wordt geplaatst. </td> 
  </tr> 
 </tbody> 
</table>

## Een set classificatieregel maken {#create-classification-rule-set}

<!-- 

t_classification_rule_set.xml

 -->

Geef de classificatieregel een naam, pas de variabele toe en geef instellingen voor overschrijven op.

1. (Vereiste) Definieer de classificatiestructuur in **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

   (Zie [Classificaties](https://marketing.adobe.com/resources/help/en_US/reference/classifications.html) in Admin Tools voor hulp bij het toevoegen van classificaties.)

   Variabelen worden pas in het [!UICONTROL New Rule Set] deelvenster weergegeven nadat voor die variabele ten minste één classificatie is gedefinieerd.

   U kunt classificaties maken voor een variabele in **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Traffic]** > **[!UICONTROL Traffic Classifications]** (of **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Classifications]**). Selecteer vervolgens de variabele en klik op **[!UICONTROL Add Classification]**.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]** > **[!UICONTROL Add Rule Set]**.

   ![](assets/new_rule_set.png)

1. Geef de regelset een naam en klik op **[!UICONTROL Create Rule Set]**.
1. Selecteer de regelset die u wilt bewerken.

   ![](assets/classification_rules_page.png)

1. Klik op **[!UICONTROL Select Report Suites and Variables]**.

   De rapportreeks en de veranderlijke lijst zijn bevolkt met alle gerubriceerde variabelen beschikbaar in alle rapportreeksen in uw login bedrijf. Één enkele variabele in een rapportreeks kan tot slechts één regelreeks behoren.

   Zie *`Variable`* in de definities voor de pagina van de Bouwer [van de Regel van de](/help/components/c-classifications2/crb/classification-rule-definitions.md) Classificatie voor meer informatie.
1. Geef de te gebruiken rapportsuites en -variabelen op en klik op **[!UICONTROL Save]**.
1. Ga door classificatieregels [aan de regelreeks](/help/components/c-classifications2/crb/classification-rule-set.md) toe te voegen.
