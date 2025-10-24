---
title: Classificatieconsolidatie maken en bewerken
description: Verklaart om classificatieconsolisies tot stand te brengen, te bevestigen, in werking te stellen goed te keuren en te annuleren.
exl-id: f36bcbcb-0ed0-44a7-a6a9-b28fd244fb27
feature: Classifications
source-git-commit: 77599d015ba227be25b7ebff82ecd609fa45a756
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# Classificatieconsolisies maken en bewerken

Met classificatiesets kunt u classificatiesets samenvoegen tot één set. Gebruik deze interface om een consolidatie van classificatiesets te maken van begin tot eind. Deze interface is van het grootste belang voor organisaties die van oudere classificaties naar classificatiesets overgaan. De meeste organisaties die classificatiesets reeds het meest waarschijnlijk gebruiken te hoeven niet om deze consolidatiewerkstroom te gebruiken.

## Een consolidatie maken

Een classificatieconsolidatie maken in de Adobe Analytics-hoofdinterface:

1. Selecteer **[!UICONTROL Classification sets]** in het menu **[!UICONTROL Components]** .
1. Selecteer in **[!UICONTROL Classification Sets]** Manager de tab **[!UICONTROL Consolidations]** .
1. In de **[!UICONTROL Classification Sets - Consolidations]** manager, uitgezochte ![ AddCircle ](/help/assets/icons/AddCircle.svg) **[!UICONTROL New]**.
1. In het dialoogvenster **[!UICONTROL New Consolidation]**

   ![ de Reeksen van de Classificatie - Nieuwe Consolidatie ](assets/classifications-sets-consolidations-new.png)
   1. Voer een **[!UICONTROL Name]** in. Bijvoorbeeld: `Consolidation Example` .
   1. Voer een **[!UICONTROL Description (optional)]** in. Bijvoorbeeld `Example classification set` .
   1. Voer een of meer e-mailadressen (gescheiden door komma&#39;s) in **[!UICONTROL Notify of issues]** in. E-mailmeldingen worden naar deze gebruikers verzonden bij problemen.
   1. Selecteer een classificatieset in het vervolgkeuzemenu **[!UICONTROL Classification Set To Match]** .

      De lijst links van **[!UICONTROL Source Classification Set]** wordt gevuld met classificatiesets die vergelijkbaar zijn met de geselecteerde classificatielijst en die beschikbaar zijn voor consolidatie.

   1. Selecteer classificatiereeksen die u van de linkerlijst wilt consolideren en de geselecteerde reeksen op de juiste lijst onder de geselecteerde ![ Zeer belangrijke ](/help/assets/icons/Key.svg) **[!UICONTROL _classificatiereeks_]** laten vallen.

      U kunt afzonderlijke en geselecteerde classificatiesets in de lijst verplaatsen. U kunt de ![ Zeer belangrijke ](/help/assets/icons/Key.svg) **[!UICONTROL _classificatiereeks_]** met een geselecteerde classificatie ook vervangen die door belemmering en daling wordt geplaatst.

   1. Selecteer **[!UICONTROL Save]** om de classificatieconsolidatie op te slaan. Selecteer **[!UICONTROL Cancel]** om te annuleren.

Zodra het bewaard, wordt een classificatieconsolidatie bevestigd automatisch voor consolidatie. Deze validatie zorgt ervoor dat elk afzonderlijk classificatieset geldig is voor deze consolidatie. Wanneer dit is gelukt, wordt in het item in de consolidatielijst Indelingen de status **[!UICONTROL Validated]** weergegeven.

Nadat u een consolidatie hebt gemaakt, zijn de volgende stappen:

* [ re-Valideer ](#re-validate) de classificatieconsolidatie wanneer u veranderingen in de aanvankelijke configuratie hebt aangebracht.
* [ Looppas ](#run) de classificatieconsolidatie.
* [ keur ](#approve) de classificatieconsolidatie goed.



<!--
         
  

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Consolidations]** > **[!UICONTROL Add]**

The following fields are available when creating a consolidation:

* **[!UICONTROL Name]**: The name of the consolidation.
* **[!UICONTROL Notify of issues]**: A comma-delimited list of email addresses that are notified of issues with this consolidation.
* **[!UICONTROL Dataset to match]**: A drop-down list of all classification sets.

Once you select a classification set, a table with two columns appears:

* The right column contains all classification sets that you want to consolidate. It starts with the classification set selected using the above drop-down list.
* The left column contains all classification sets eligible to be merged with the originally selected dataset. **Schemas must exactly match to be eligible for consolidation**. If schemas do not match the selected classification set, they do not appear in this left column.

Drag the desired classification sets from the available column on the left to the consolidation column on the right. Once the consolidation is given a name and two or more classification sets are in the right column, click **[!UICONTROL Save & Continue]**.

-->

## Een consolidatie bewerken

Als u een classificatieconsolidatie wilt bewerken, gaat u naar de Adobe Analytics-hoofdinterface:

1. Selecteer **[!UICONTROL Classification sets]** in het menu **[!UICONTROL Components]** .
1. Selecteer in **[!UICONTROL Classification Sets]** Manager de tab **[!UICONTROL Consolidations]** .
1. In de manager **[!UICONTROL Classification Sets Consolidations]** :
   1. Selecteer de titel van uw rubriceringsconsolidatie. Het dialoogvenster Consolidatie: dialoogvenster voor de consolidatie van classificaties wordt weergegeven. De vormgeving en beschikbare acties zijn afhankelijk van de huidige status van de consolidatie en of u nog steeds de optie hebt om de classificatieconsolidatie te wijzigen.

      | Beschikbare acties | Beschrijving |
      |---|---|
      | ![ annuleert ](/help/assets/icons/Cancel.svg) **[!UICONTROL Cancel]** | [ annuleert de consolidatie ](#cancel). |
      | ![ Vinkje ](/help/assets/icons/Checkmark.svg) **[!UICONTROL Re-Validate]** | [ bevestigt opnieuw de consolidatie ](#re-validate). |
      | ![ Spel ](/help/assets/icons/Play.svg) **[!UICONTROL Run]** | [ stel de consolidatie ](#run) in werking. |
      | ![ ThumbUp ](/help/assets/icons/ThumbUp.svg) **[!UICONTROL Approve]** | [ keur de consolidatie ](#approve) goed. |



### Opnieuw valideren

U kunt een classificatieconsolidatie opnieuw valideren in het dialoogvenster Consolidatie: classificatieconsolidatie. Een ![ alarm ](/help/assets/icons/Alert.svg) zou extra informatie over kwesties met uw consolidatie kunnen verstrekken die vereisen om de consolidatie opnieuw te vormen.

![ de Reeksen van de Classificatie - consolidatie re-bevestigt ](assets/classifications-sets-consolidations-validated.png)

De classificatieconsolidatie opnieuw valideren:

1. Configureer de consolidatie opnieuw met dezelfde interface voor slepen en neerzetten als waarmee u de consolidatie hebt gemaakt.
1. Selecteer ![ Vinkje ](/help/assets/icons/Checkmark.svg) **[!UICONTROL Re-Validate]**. De validatie zorgt ervoor dat elk afzonderlijk classificatieset geldig is voor deze consolidatie. Wanneer succesvol, wordt een pop-upbericht getoond: ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL Successfully submitted consolidation for validation!]**
1. Selecteer ![ CrossSize400 ](/help/assets/icons/CrossSize400.svg) om de dialoog te sluiten. Of selecteer ![ Spel ](/help/assets/icons/Play.svg) Looppas om de consolidatie in werking te stellen of ![ annuleert ](/help/assets/icons/Cancel.svg) om de classificatie te annuleren.



<!--
Once you have created a consolidation, a list of source datasets appears on the right. The **[!UICONTROL Validate]** button makes sure that each individual classification set is valid for this consolidation. You can reorder the classification steps here to determine priority in cases of mismatched classification values. **The highest classification set in the list overwrites any mismatched values in other classification sets.**

-->

### Uitvoeren

Nadat een consolidatie van de classificatie is gevalideerd, kunt u de consolidatie uitvoeren.

Een classificatieconsolidatie uitvoeren:

1. Selecteer ![ Spel ](/help/assets/icons/Play.svg) **[!UICONTROL Run]**. Een pop-upbericht toont ![ CheckmarkCircle ](/help/assets/icons/CheckmarkCircle.svg) **[!UICONTROL Successfully submitted consolidation for processing!]**
1. Selecteer ![ CrossSize400 ](/help/assets/icons/CrossSize400.svg) om de dialoog te sluiten.


### Goedkeuren

Zodra een classificatieconsolidatie is uitgevoerd, is de consolidatiestatus **[!UICONTROL Waiting for Approval]** . De goedkeuring van een classificatieconsolidatie vervangt de afzonderlijke classificatiesets door het samenstel van geconsolideerde classificaties en de afzonderlijke classificatiesets worden geschrapt.

![ de reeksen van de Classificatie - Consolidatie die op Goedkeuring wachten ](assets/classifications-sets-consolidations-waitingforapproval.png)

Een consolidatie van een classificatieset goedkeuren:

1. Gebruik **[!UICONTROL Similarity Reports]** om de consolidatie te controleren. Dit rapport toont een lijst met de volgende kolommen:

   * **[!UICONTROL Classification Set Name]**: De naam van de classificatieset.
   * **[!UICONTROL Mismatch]**: Het percentage rijen waarin de sleutelwaarden niet overeenkomen met de bronclassificatieset. Als het percentage niet-overeenkomende items hoog is, kan dit een aanwijzing zijn dat de classificatiegegevens te verschillend zijn. Controleer en controleer of de geselecteerde classificatiesets vergelijkbare classificatiegegevens hebben.
   * **[!UICONTROL Absent]**: Het percentage rijen waar de zeer belangrijke waarden in de ![ Zeer belangrijke ](/help/assets/icons/Key.svg) classificatiereeks maar niet in de bronclassificatiereeks zijn. Alle afwezige rijen worden toegevoegd aan de geconsolideerde classificatieset.

1. Als de classificatieconsolidatie klaar voor goedkeuring is, uitgezochte ![ Vinkje ](/help/assets/icons/Checkmark.svg) **[!UICONTROL Approve]**. Een dialoogvenster van **[!UICONTROL Approve Consolidation?]** vraagt om bevestiging. Selecteer **[!UICONTROL Approve]** om de consolidatie goed te keuren. Selecteer **[!UICONTROL Cancel]** om te annuleren.

Na goedkeuring wordt het geconsolideerde classificatieset gemaakt. De status wordt ingesteld op **[!UICONTROL Complete]** .


### Annuleren

U kunt een classificatieconsolidatie vóór goedkeuring annuleren.

Een classificatieconsolidatie annuleren:

1. Selecteer **[!UICONTROL Cancel]**.

   U kunt een consolidatie niet hervatten wanneer de consolidatie is geannuleerd.
1. Selecteer **[!UICONTROL Cancel Consolidation]** om de consolidatie te annuleren. Selecteer **[!UICONTROL Go Back]** om de annulering te herstellen.
