---
title: Consolidatieproces voor een classificatieset
description: Het volledige proces van consolidering van classificatiesets.
source-git-commit: 496b4891d447ed9dd091a6498a792146a2d5aceb
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Consolidatieproces voor een classificatieset

Gebruik deze interface om een consolidatie van classificatiesets te maken van begin tot eind.

## Maken

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Consolidations]** > **[!UICONTROL Add]**

De volgende velden zijn beschikbaar wanneer u een consolidatie maakt:

* **[!UICONTROL Name]**: De naam van de consolidatie.
* **[!UICONTROL Notify of issues]**: Een door komma&#39;s gescheiden lijst met e-mailadressen die op de hoogte worden gesteld van problemen met deze consolidatie.
* **[!UICONTROL Dataset to match]**: Een vervolgkeuzelijst met alle classificatiesets.

Nadat u een classificatieset hebt geselecteerd, wordt een tabel met twee kolommen weergegeven:

* De rechterkolom bevat alle classificatiesets die u wilt verenigen. Deze begint met de geselecteerde classificatieset in de bovenstaande vervolgkeuzelijst.
* De linkerkolom bevat alle classificatiesets die in aanmerking komen om te worden samengevoegd met de oorspronkelijk geselecteerde gegevensset. **Schema&#39;s moeten exact overeenkomen om in aanmerking te komen voor consolidatie**. Als schema&#39;s niet overeenkomen met de geselecteerde classificatieset, worden ze niet weergegeven in deze linkerkolom.

Sleep de gewenste classificatiesets van de beschikbare kolom aan de linkerkant naar de consolidatiekolom aan de rechterkant. Als de consolidatie een naam heeft en twee of meer classificatiesets in de rechterkolom staan, klikt u op **[!UICONTROL Save & Continue]**.

## Validatie

Zodra u een consolidatie hebt gecreeerd, verschijnt een lijst van brondatasets op het recht. De **[!UICONTROL Validate]** zorgt u ervoor dat elke afzonderlijke classificatieset geldig is voor deze consolidatie. U kunt de classificatiestappen hier opnieuw rangschikken om prioriteit te bepalen in gevallen van mismatch classificatiewaarden. **De hoogste classificatieset in de lijst overschrijft alle niet-overeenkomende waarden in andere classificatiesets.**

## Uitvoeren

Nadat een consolidatie is gevalideerd, kunt u deze uitvoeren. Als u een consolidatie uitvoert, wordt een gelijksoortigheidsrapport met de volgende tabelkolommen weergegeven:

* **[!UICONTROL Dataset name]**: De naam van de classificatieset.
* **[!UICONTROL Mismatch]**: Het percentage van rijen waarin de sleutelwaarden niet de bronclassificatieset overeenkwamen. Als het percentage niet-overeenkomende items hoog is, is het mogelijk dat de classificatiegegevens te verschillend zijn. Controleer of de geselecteerde classificatiesets vergelijkbare classificatiegegevens hebben.
* **[!UICONTROL Absent]**: Het percentage rijen waarin de hoofdwaarden zich in die classificatieset bevonden, maar niet in de bronclassificatieset. Alle afwezige rijen worden toegevoegd aan de geconsolideerde classificatieset.

## Goedkeuren

Handelt als laatste aanroep voordat de afzonderlijke classificatiesets worden verwijderd en een geconsolideerde classificatieset wordt gemaakt. Controleer of alles juist is en klik vervolgens op **[!UICONTROL Approve]**.

Na goedkeuring wordt het geconsolideerde classificatieset gemaakt. De status is ingesteld op [!UICONTROL Complete], en voor de consolidatie is geen verdere actie vereist.
