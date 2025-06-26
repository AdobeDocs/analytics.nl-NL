---
description: Met de Segment Builder kunt u waarden vergelijken en beperken met behulp van geselecteerde operatoren.
title: Vergelijkingsoperatoren voor segmenten
feature: Segmentation
exl-id: 1ec1ff05-03a9-4151-8fcb-a72ebbce87dd
source-git-commit: 80e4a3ba4a5985563fcf02acf06997b4592261e4
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 0%

---

# Vergelijkingsoperatoren voor segmenten

Met de Segment Builder kunt u waarden vergelijken en beperken met behulp van geselecteerde operatoren. Er zijn drie categorieën operatoren: Standaard, Data Warehouse en Afzonderlijk aantal.

Afhankelijk van de operator die u selecteert:

* U kunt een waarde invoeren
* U kunt een deel van een waarde ingaan en van een drop-down menu (als beschikbaar) selecteren.
* Selecteer direct een waarde in de keuzelijst (indien beschikbaar).

Wanneer u een waarde voor een exploitant typt die beschikbare waarden, als **[!UICONTROL equals]** valideert, en de waarde niet de waarden beschikbaar voor de component aanpast, ziet u a ![ AlertRed ](/help/assets/icons/AlertRed.svg) pictogram. U kunt of een waarde van het drop-down menu selecteren of **[!UICONTROL _drukken gaat_]** binnen om de waarde in te gaan.

![ de gelijken van het Segment ](assets/segment-operator-equals.png)

## Jokertekens

Het enige ondersteunde jokerteken voor operatoren die jokertekens ondersteunen, is het sterretje: `*` . Als u naar het specifieke &#42; karakter moet zoeken, kunt u het met backslash, zoals `\*` ontsnappen.

Bijvoorbeeld, hebt u een paginanaam genoemd *Mijn koele product*.

* De segmentregel **[!UICONTROL Page name]** **[!UICONTROL matches]** `* product` komt overeen met de bovenstaande paginanaam.
* Nochtans, past de regel **[!UICONTROL Page name]** **[!UICONTROL matches]** `My \* product` slechts de paginanaam *Mijn * Product* aan.

## Standaardoperatoren

| Operator | De geselecteerde afmeting, segment of metrische gebeurtenis... |
|--- |--- |
| **[!UICONTROL equals]** | Retourneert items die exact overeenkomen voor een numerieke waarde of tekenreekswaarde. Opmerking: als u jokertekens gebruikt, gebruikt u de operator **[!UICONTROL matches]** . |
| **[!UICONTROL does not equal]** | Retourneert alle items die niet exact overeenkomen met de ingevoerde waarde.  Opmerking: als u jokertekens gebruikt, gebruikt u de operator **[!UICONTROL does not match]** . |
| **[!UICONTROL equals any of]** | Retourneert items die exact overeenkomen met een waarde in het invoerveld (maximaal 500 items). Bijvoorbeeld, zou het ingaan `Search Results, Homepage` voor de **[!UICONTROL Page Name]** dimensie met deze exploitant *Resultaten van het Onderzoek* en *Homepage* aanpassen, en tellen als 2 punten. Het invoerveld voor deze operator wordt door komma&#39;s gescheiden. |
| **[!UICONTROL does not equal any of]** | Hiermee worden items aangegeven die exact overeenkomen met een waarde in het invoerveld (maximaal 500 items) en worden vervolgens alleen items zonder deze waarden geretourneerd. Bijvoorbeeld, zou het ingaan `Search Results, Homepage` met deze exploitant voor de **[!UICONTROL Page Name]** dimensie *Resultaten van het Onderzoek* identificeren en *Homepage* en dan **hen uitsluiten** van de teruggekeerde punten. Dit voorbeeld telt 2 objecten. Het invoerveld voor deze operator wordt door komma&#39;s gescheiden. |
| **[!UICONTROL contains]** | Retourneert items die de subtekenreeksen van de ingevoerde waarden vergelijken. Bijvoorbeeld, als de regel **[!UICONTROL Page Name]** **[!UICONTROL contains]** `Search` is, dan zal deze regel om het even welke pagina aanpassen die substring `Search` in het heeft, met inbegrip van *Resultaten van het Onderzoek*, *Onderzoek*, en *het Zoeken*. De component &quot;contains&quot; is niet hoofdlettergevoelig in Adobe Analytics, maar is wel hoofdlettergevoelig in Customer Journey Analytics. |
| **[!UICONTROL does not contain]** | Retourneert het omgekeerde van de **[!UICONTROL contains]** -regel. Met name worden alle items die overeenkomen met de ingevoerde waarde niet opgenomen in de ingevoerde waarden. Bijvoorbeeld, als de regel **[!UICONTROL Page Name]** **[!UICONTROL does not contain]** `Search` is, dan zal het geen pagina aanpassen die het substring `Search` in het heeft, met inbegrip van *Resultaten van het Onderzoek*, *Onderzoek*, en *het Zoeken*. Deze waarden worden niet opgenomen in de resultaten. |
| **[!UICONTROL contains all of]** | Retourneert items die worden vergeleken met de subtekenreeksen, inclusief meerdere waarden die aan elkaar zijn gekoppeld. Bijvoorbeeld, zou het ingaan `Search Results` met deze exploitant voor de **[!UICONTROL Page Name]** dimensie *Resultaten van het Onderzoek* en *Resultaten van Onderzoek* aanpassen, maar *Onderzoek* of *Resultaten* individueel. De regel zou *Onderzoek* en *gevonden Resultaten* aanpassen samen. Het invoerveld voor deze operator wordt door spaties gescheiden (100 woorden). |
| **[!UICONTROL does not contain all of]** | Identificeert items in vergelijking met subtekenreeksen, inclusief meerdere waarden die aan elkaar zijn gekoppeld, en retourneert alleen items zonder deze waarden. Bijvoorbeeld, zou het ingaan `Search Results` met deze exploitant voor de **[!UICONTROL Page Name]** dimensie *Resultaten van het Onderzoek* identificeren en *Resultaten van Onderzoek* (maar niet *Onderzoek* of *Resultaten* individueel) en dan deze punten uitsluiten. Het invoerveld voor deze operator wordt door spaties gescheiden (100 woorden). |
| **[!UICONTROL contains any of]** | Retourneert items die worden vergeleken met de subtekenreeksen, inclusief meerdere waarden die zijn gekoppeld of onafhankelijk zijn geïdentificeerd. Bijvoorbeeld, zou het ingaan `Search Results` met deze exploitant *Resultaten van het Onderzoek* aanpassen, *Resultaten van Onderzoek*, *Onderzoek*, en *Resultaten*. Het zou één van beide *Onderzoek* OF *gevonden Resultaten* samen of onafhankelijk aanpassen. Het invoerveld voor deze operator wordt door spaties gescheiden (100 woorden). |
| **[!UICONTROL does not contain any of]** | Identificeert items op basis van subtekenreeksen en retourneert vervolgens waarden die deze subtekenreeksen niet bevatten. Er kunnen meerdere bij elkaar gevoegde waarden of waarden afzonderlijk worden geïdentificeerd. Bijvoorbeeld, zou het ingaan `Search Results` voor de **[!UICONTROL Page Name]** dimensie *Resultaat van het Onderzoek* s, *Resultaten van Onderzoek* h*, *Onderzoek* aanpassen, en *Resultaten* waar of *Onderzoek* of *Resultaat* samen of onafhankelijk worden gevonden. Items die deze subtekenreeksen bevatten, worden dan uitgesloten. Het invoerveld voor deze operator wordt door spaties gescheiden (100 woorden). |
| **[!UICONTROL starts with]** | Retourneert items die beginnen met de ingevoerde tekenreekswaarde. |
| **[!UICONTROL does not start with]** | Retourneert alle items die niet beginnen met de ingevoerde tekenreekswaarde. Dit is het omgekeerde van de operator **[!UICONTROL starts with]** . |
| **[!UICONTROL ends with]** | Retourneert items die eindigen met de ingevoerde tekenreekswaarde. |
| **[!UICONTROL does not end with]** | Retourneert alle items die niet eindigen met de ingevoerde tekenreekswaarde. Dit is het omgekeerde van de operator **[!UICONTROL ends with]** . |
| **[!UICONTROL matches]** | Retourneert items die exact overeenkomen op basis van een opgegeven numerieke waarde of tekenreekswaarde. De component **[!UICONTROL matches]** is hoofdlettergevoelig in Adobe Analytics en Customer Journey Analytics. **Nota**: Gebruik deze exploitant wanneer het gebruiken van [ vervanging ](#wildcards) (het globberen) eigenschappen. Voorbeelden van globbings:<ul><li>`a*e` komt overeen met `ae` , `abcde` , `adobe` en `a whole sentence`</li><li>`adob*` komt overeen met `adobe` , `adobe analytics` en `adobo recipe`</li><li>`*dobe` komt overeen met `dobe` , `adobe` en `cute little dobe`</li></ul> |
| **[!UICONTROL does not match]** | Retourneert alle items die niet exact overeenkomen met de ingevoerde waarde. Nota: Gebruik deze exploitant wanneer het gebruiken van [ vervanging ](#wildcards) (het globberen) eigenschappen. |
| **[!UICONTROL exists]** | Retourneert het aantal items dat bestaat. Als u bijvoorbeeld de **[!UICONTROL Pages Not Found]** -dimensie evalueert met de operator **[!UICONTROL exist]** , wordt het aantal bestaande foutpagina&#39;s geretourneerd. |
| **[!UICONTROL does not exist]** | Retourneert alle items die niet bestaan. Als u bijvoorbeeld de **[!UICONTROL Pages Not Found]** -dimensie evalueert met de operator **[!UICONTROL does not exist]** , wordt het aantal pagina&#39;s geretourneerd waarop deze foutpagina niet bestaat. |

## Data Warehouse-operatoren

| Operator | De geselecteerde afmeting, segment of metrische gebeurtenis... |
| --- | --- |
| **[!UICONTROL is less than]** | Retourneert items waarvan het numerieke aantal kleiner is dan de ingevoerde waarde. |
| **[!UICONTROL is less than or equal to]** | Retourneert items waarvan het numerieke getal kleiner dan of gelijk is aan de ingevoerde waarde. |
| **[!UICONTROL is greater than]** | Retourneert items waarvan het numerieke aantal groter is dan de ingevoerde waarde. |
| **[!UICONTROL is greater than or equal to]** | Retourneert items waarvan het numerieke getal groter dan of gelijk is aan de ingevoerde waarde. |

## Operatoren voor onderscheiden tellen

U kunt op een duidelijke telling van punten binnen een afmeting segmenteren. Voorbeelden: *Bezoekers die meer dan 5 verschillende producten* bekeken, of *Bezoeken waar meer dan 5 verschillende pagina&#39;s* werden gezien.

| Operator | De geselecteerde afmeting, segment of metrische gebeurtenis... |
| --- | --- |
| **[!UICONTROL equals]** | Retourneert dimensieitems waarvan het unieke aantal gelijk is aan de ingevoerde waarde. |
| **[!UICONTROL does not equal]** | Retourneert dimensieitems waarvan het unieke aantal niet gelijk is aan de ingevoerde waarde. |
| **[!UICONTROL is greater than]** | Retourneert dimensieitems waarvan het unieke aantal groter is dan de ingevoerde waarde. |
| **[!UICONTROL is less than]** | Retourneert dimensieitems waarvan het unieke aantal kleiner is dan de ingevoerde waarde. |
| **[!UICONTROL is greater than or equal to]** | Retourneert dimensieitems waarvan het unieke aantal groter dan of gelijk is aan de ingevoerde waarde. |
| **[!UICONTROL is less than or equal to]** | Retourneert dimensieitems waarvan het unieke aantal kleiner dan of gelijk is aan de ingevoerde waarde. |


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Afmetingen van de Afmeting ](https://video.tv.adobe.com/v/27257?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]
