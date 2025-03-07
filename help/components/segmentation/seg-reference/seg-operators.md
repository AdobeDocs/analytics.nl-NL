---
description: Met de Segment Builder kunt u waarden vergelijken en beperken met behulp van geselecteerde operatoren.
title: Vergelijkingsoperatoren voor segmenten
feature: Segmentation
exl-id: 1ec1ff05-03a9-4151-8fcb-a72ebbce87dd
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---

# Vergelijkingsoperatoren voor segmenten

Met de Segment Builder kunt u waarden vergelijken en beperken met behulp van geselecteerde operatoren. Er zijn drie categorieën operatoren: Standaard, Data Warehouse en Afzonderlijk aantal.

Het enige ondersteunde jokerteken is de asterisk: &#42; . Als u naar &#42; moet zoeken, kunt u het met backslash ontsnappen.

**Voorbeeld**: Veronderstel u een paginanaam genoemd &quot;Mijn koele product&quot; hebt. De segmentregel &quot;de naam van de Pagina past Mijn &#42; product&quot;aan zal de bovengenoemde paginanaam aanpassen. Nochtans, past de regel &quot;de naam van de Pagina Mijn \ \ &#42; product&quot;slechts de paginanaam &quot;Mijn &#42; Product&quot;aan.

## Standaardoperatoren

| Operator | De geselecteerde afmeting, segment of metrische gebeurtenis... |
|--- |--- |
| equals | Retourneert items die exact overeenkomen voor een numerieke waarde of tekenreekswaarde. Opmerking: als u jokertekens gebruikt, gebruikt u de operator &quot;overeenkomend&quot;. |
| is niet gelijk aan | Retourneert alle items die niet exact overeenkomen met de ingevoerde waarde.  Opmerking: als u jokertekens gebruikt, gebruikt u de operator &quot;komt niet overeen&quot;. |
| is gelijk aan een van de | Retourneert items die exact overeenkomen met een waarde in het invoerveld (maximaal 500 items). Als u bijvoorbeeld &quot;Zoekresultaten, homepage&quot; invoert met deze operator, komt dit overeen met &quot;Zoekresultaten&quot; en &quot;Homepage&quot; en telt u als 2 items. Het invoerveld voor deze operator wordt door komma&#39;s gescheiden. |
| is niet gelijk aan | Hiermee worden items aangegeven die exact overeenkomen met een waarde in het invoerveld (maximaal 500 items) en worden vervolgens alleen items zonder deze waarden geretourneerd. Als u bijvoorbeeld &quot;Zoekresultaten, homepage&quot; invoert met deze operator, worden &quot;Zoekresultaten&quot; en &quot;Homepage&quot; geïdentificeerd en worden deze vervolgens uitgesloten van de geretourneerde items. Dit voorbeeld telt 2 objecten. Het invoerveld voor deze operator wordt door komma&#39;s gescheiden. |
| contains | Retourneert items die de subtekenreeksen van de ingevoerde waarden vergelijken. Als de regel voor &quot;Pagina&quot; bijvoorbeeld &quot;Zoeken&quot; bevat, komt deze overeen met elke pagina waarop de subtekenreeks &quot;Zoeken&quot; staat, inclusief &quot;Zoekresultaten&quot;, &quot;Zoeken&quot; en &quot;Zoeken&quot;. De component &quot;contains&quot; is niet hoofdlettergevoelig in Adobe Analytics, maar is wel hoofdlettergevoelig in de Customer Journey Analytics. |
| bevat niet | Retourneert het omgekeerde van de regel &quot;contains&quot;. Met name worden alle items die overeenkomen met de ingevoerde waarde niet opgenomen in de ingevoerde waarden. Als de regel voor &quot;Pagina&quot; bijvoorbeeld geen &quot;Zoeken&quot; bevat, komt deze niet overeen met een pagina waarop de subtekenreeks &quot;Zoeken&quot; staat, inclusief &quot;Zoekresultaten&quot;, &quot;Zoeken&quot; en &quot;Zoeken&quot;. Deze waarden worden niet opgenomen in de resultaten. |
| bevat alle | Retourneert items die worden vergeleken met de subtekenreeksen, inclusief meerdere waarden die aan elkaar zijn gekoppeld. Als u bijvoorbeeld &quot;Zoekresultaten&quot; invoert met deze operator, komen de resultaten van de zoekopdracht overeen met die van de zoekresultaten, maar niet met de resultaten van de zoekopdracht afzonderlijk. Deze komt overeen met de zoekresultaten en de gevonden resultaten samen. Het invoerveld voor deze operator wordt door spaties gescheiden (100 woorden). |
| bevat niet alle | Identificeert items die worden vergeleken met subtekenreeksen, inclusief meerdere waarden die aan elkaar zijn gekoppeld, en retourneert alleen items zonder deze waarden. Als u bijvoorbeeld &quot;Zoekresultaten&quot; invoert met deze operator, worden &quot;Zoekresultaten&quot; en &quot;Zoekresultaten&quot; (maar niet &quot;Zoeken&quot; of &quot;Resultaten&quot; afzonderlijk) geïdentificeerd en worden deze items uitgesloten. Het invoerveld voor deze operator wordt door spaties gescheiden (100 woorden). |
| bevat een van de | Retourneert items die worden vergeleken met de subtekenreeksen, inclusief meerdere waarden die zijn gekoppeld of onafhankelijk zijn geïdentificeerd. Als u bijvoorbeeld &quot;Zoekresultaten&quot; invoert met deze operator, komt dit overeen met &quot;Zoekresultaten&quot;, &quot;Zoekresultaten&quot;, &quot;Zoeken&quot; en &quot;Resultaten&quot;. Deze komt ofwel overeen met &quot;Zoeken&quot; OF &quot;Resultaten&quot; gevonden samen of onafhankelijk. Het invoerveld voor deze operator wordt door spaties gescheiden (100 woorden). |
| bevat geen van de | Identificeert items op basis van subtekenreeksen en retourneert vervolgens waarden die deze subtekenreeksen niet bevatten. Er kunnen meerdere bij elkaar gevoegde waarden of waarden afzonderlijk worden geïdentificeerd. Als u bijvoorbeeld &quot;Zoekresultaten&quot; invoert, komt dit overeen met &quot;Zoekresultaten&quot;, &quot;Zoekresultaten&quot;, &quot;Zoeken&quot; en &quot;Resultaten&quot;, waarbij &quot;Zoeken&quot; of &quot;Resultaten&quot; samen of onafhankelijk worden gevonden. Items die deze subtekenreeksen bevatten, worden dan uitgesloten. Het invoerveld voor deze operator wordt door spaties gescheiden (100 woorden). |
| begint met | Retourneert items die beginnen met het teken of de tekenreeksen van de ingevoerde waarde. |
| start niet met | Retourneert alle items die niet beginnen met de tekens of tekenreeksen van de ingevoerde waarden. Dit is het omgekeerde van de operator &quot;start with&quot;. |
| eindigt met | Retourneert items die eindigen met het teken of de tekenreeksen van de ingevoerde waarde. |
| eindigt niet met | Retourneert alle items die niet eindigen met de tekens of tekenreeksen van de ingevoerde waarde. Dit is het omgekeerde van de operator &quot;ends with&quot;. |
| overeenkomsten | Retourneert items die exact overeenkomen op basis van een opgegeven numerieke waarde of tekenreekswaarde. De clausule &quot;overeenkomsten&quot;is case sensitive in Adobe Analytics en in Customer Journey Analytics. **Nota**: Gebruik deze exploitant wanneer het gebruiken van vervangingseigenschappen (het globberen). Voorbeelden van globbings:<ul><li>`a*e` komt overeen met `ae` , `abcde` , `adobe` en `a whole sentence`</li><li>`adob*` komt overeen met `adobe` , `adobe analytics` en `adobo recipe`</li><li>`*dobe` komt overeen met `dobe` , `adobe` en `cute little dobe`</li></ul> |
| komt niet overeen | Retourneert alle items die niet exact overeenkomen met de ingevoerde waarde. Opmerking: gebruik deze operator bij het gebruik van jokertekens (globbing). |
| exists | Retourneert het aantal items dat bestaat. Als u bijvoorbeeld de dimensie Pagina&#39;s niet gevonden evalueert met de operator &quot;exist&quot;, wordt het aantal bestaande foutpagina&#39;s geretourneerd. |
| bestaat niet | Retourneert alle items die niet bestaan. Als u bijvoorbeeld de afmetingen Pagina&#39;s niet gevonden hebt geëvalueerd met de operator &#39;&#39;bestaat niet&#39;&#39;, wordt het aantal pagina&#39;s geretourneerd waarop deze foutpagina niet bestaat. |

## Data Warehouse-operatoren

| Operator | De geselecteerde afmeting, segment of metrische gebeurtenis... |
| --- | --- |
| is kleiner dan | Retourneert items waarvan het numerieke aantal kleiner is dan de ingevoerde waarde. |
| is kleiner dan of gelijk aan | Retourneert items waarvan het numerieke getal kleiner dan of gelijk is aan de ingevoerde waarde. |
| is groter dan | Retourneert items waarvan het numerieke aantal groter is dan de ingevoerde waarde. |
| is groter dan of gelijk aan | Retourneert items waarvan het numerieke getal groter dan of gelijk is aan de ingevoerde waarde. |

## Operatoren voor onderscheiden tellen

U kunt op een duidelijke telling van punten binnen een afmeting segmenteren. Voorbeelden: &quot;Bezoekers die meer dan vijf verschillende producten hebben bekeken&quot; of &quot;Bezoek waarbij meer dan vijf verschillende pagina&#39;s werden bekeken&quot;.

| Operator | De geselecteerde afmeting, segment of metrische gebeurtenis... |
| --- | --- |
| equals | Retourneert dimensieitems waarvan het unieke aantal gelijk is aan de ingevoerde waarde. |
| is niet gelijk aan | Retourneert dimensieitems waarvan het unieke aantal niet gelijk is aan de ingevoerde waarde. |
| is groter dan | Retourneert dimensieitems waarvan het unieke aantal groter is dan de ingevoerde waarde. |
| is kleiner dan | Retourneert dimensieitems waarvan het unieke aantal kleiner is dan de ingevoerde waarde. |
| is groter dan of gelijk aan | Retourneert dimensieitems waarvan het unieke aantal groter dan of gelijk is aan de ingevoerde waarde. |
| is kleiner dan of gelijk aan | Retourneert dimensieitems waarvan het unieke aantal kleiner dan of gelijk is aan de ingevoerde waarde. |


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Afmetingen van de Afmeting ](https://video.tv.adobe.com/v/27257?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]
