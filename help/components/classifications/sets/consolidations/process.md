---
title: Consolidatieproces voor een classificatieset
description: Het volledige proces van consolidering van classificatiesets.
exl-id: f36bcbcb-0ed0-44a7-a6a9-b28fd244fb27
feature: Classifications
source-git-commit: 828f41bf45c1954c3b68ad71a7746e24626b9eed
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Consolidatieproces voor een classificatieset

Met classificatieconsolisies kunt u classificaties van meerdere gegevenssets opnemen en deze in één gegevensset combineren. Gebruik deze interface om een consolidatie van classificatiesets te maken van begin tot eind. Deze interface is zeer waardevol voor organisaties die van een erfenisclassificatiearchitectuur naar een classificatiesetarchitectuur overgaan. De meeste organisaties die reeds op de architectuur van de classificatieset zijn typisch te hoeven niet om deze consolidatiewerkstroom te gebruiken.

## Maken

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]** > **[!UICONTROL Consolidations]** > **[!UICONTROL Add]**

De volgende velden zijn beschikbaar wanneer u een consolidatie maakt:

* **[!UICONTROL Name]**: De naam van de consolidatie.
* **[!UICONTROL Notify of issues]**: Een door komma&#39;s gescheiden lijst met e-mailadressen die op de hoogte worden gesteld van problemen met deze consolidatie.
* **[!UICONTROL Dataset to match]**: een vervolgkeuzelijst met alle classificatiesets.

Nadat u een classificatieset hebt geselecteerd, wordt een tabel met twee kolommen weergegeven:

* De rechterkolom bevat alle classificatiesets die u wilt verenigen. Deze begint met de geselecteerde classificatieset in de bovenstaande vervolgkeuzelijst.
* De linkerkolom bevat alle classificatiesets die in aanmerking komen om te worden samengevoegd met de oorspronkelijk geselecteerde gegevensset. **Schema&#39;s moeten precies aanpassen om voor consolidatie** verkiesbaar te zijn. Als schema&#39;s niet overeenkomen met de geselecteerde classificatieset, worden ze niet weergegeven in deze linkerkolom.

Sleep de gewenste classificatiesets van de beschikbare kolom aan de linkerkant naar de consolidatiekolom aan de rechterkant. Als de consolidatie een naam heeft en twee of meer classificatiesets in de rechterkolom staan, klikt u op **[!UICONTROL Save & Continue]** .

## Validatie

Zodra u een consolidatie hebt gecreeerd, verschijnt een lijst van brondatasets op het recht. Met de knop **[!UICONTROL Validate]** zorgt u ervoor dat elke afzonderlijke classificatieset geldig is voor deze consolidatie. U kunt de classificatiestappen hier opnieuw rangschikken om prioriteit te bepalen in gevallen van mismatch classificatiewaarden. **de hoogste classificatie die in de lijst wordt geplaatst overschrijft om het even welke mismatch waarden in andere classificatiereeksen.**

## Uitvoeren

Nadat een consolidatie is gevalideerd, kunt u deze uitvoeren. Als u een consolidatie uitvoert, wordt een gelijksoortigheidsrapport met de volgende tabelkolommen weergegeven:

* **[!UICONTROL Dataset name]**: De naam van de classificatieset.
* **[!UICONTROL Mismatch]**: Het percentage rijen waarin de sleutelwaarden niet overeenkomen met de bronclassificatieset. Als het percentage niet-overeenkomende items hoog is, is het mogelijk dat de classificatiegegevens te verschillend zijn. Controleer en controleer of de geselecteerde classificatiesets vergelijkbare classificatiegegevens hebben.
* **[!UICONTROL Absent]**: Het percentage rijen waarin de hoofdwaarden zich in die classificatieset bevonden, maar niet in de bronclassificatieset. Alle afwezige rijen worden toegevoegd aan de geconsolideerde classificatieset.

## Goedkeuren

De laatste aanroep voordat afzonderlijke classificatiesets worden verwijderd en vervangen door een geconsolideerde classificatieset. Controleer of alles juist is en selecteer vervolgens **[!UICONTROL Approve]** .

Na goedkeuring wordt het geconsolideerde classificatieset gemaakt. De status is ingesteld op [!UICONTROL Complete] en er is geen verdere actie vereist voor de consolidatie.
