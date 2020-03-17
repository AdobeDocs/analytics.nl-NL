---
description: 'null'
title: Beperkingen en specificaties
uuid: 6717b6ea-7e01-49b8-8f6e-fb733a03b687
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Beperkingen en specificaties

## Publicatiebeperkingen voor Power BI {#section_D4BDD70B20F94A0FAE53531CA528AE42}

> [!NOTE] Deze beperkingen zijn alleen van toepassing op de optie &quot;Publish Report Builder Requests as Power BI Dataset Tables&quot;.

* Een maximum van 100 verzoeken van de Bouwer van het Rapport kan naar Power BI per werkboek worden uitgevoerd.
* Het planningsproces zal ophouden exporterende verzoeken wanneer het 101e verzoek wordt bereikt.
* Alleen de eerste 10.000 rijen met analysegegevens worden naar Power BI verzonden volgens de aanvraag van Report Builder. De overige rijen worden genegeerd.

## Een aanvraag voor een Report Builder bewerken na publicatie naar Power BI {#section_6989E74F68DD43F08D37C36B6777DB50}

> [!NOTE] Deze specificatie is van toepassing op de opties &quot;Alle verzoeken van de Bouwer van het Rapport als de Lijsten van de Dataset van de Macht BI&quot;en &quot;publiceren Alle Formatted Lijsten in het Werkboek als de Lijsten van de Dataset van de Macht BI&quot;publiceren.

Het uitgeven van een verzoek van de Bouwer van het Rapport na het publiceren van het aan Power BI kan problemen veroorzaken.

* **Zaak 1**: U publiceert een werkboek aan Macht BI en creeert een visualisatie die op zijn gegevens wordt gebaseerd. Daarna, brengt u veranderingen in het werkboek aan, veroorzakend één van de kolommen van de gegevensreeks die het om verwijst te verdwijnen. Vervolgens publiceert u het bestand opnieuw. Hierdoor wordt de visualisatie in Power BI verbroken.

   **Hier is een voorbeeld van hoe de visualisatie zal breken:**

   1. In de Bouwer van het Rapport, creeer een werkboek met één verzoek, gebruikend de afmeting van de Pagina en metrische de Meningen van de Pagina.
   1. [Plan dit verzoek](/help/analyze/report-builder/whats-new-arb.md#rb-5-5-section) dat u wilt publiceren naar Power BI.
   1. Maak in Power BI een visualisatie voor pagina- en paginaweergaven.
   1. Bewerk nu het werkboek door Paginaweergaven uit de aanvraag te verwijderen.
   1. Bewerk het programma met het bijgewerkte werkboek en publiceer het verzoek opnieuw aan Power BI.
   1. Zodra het nieuwe werkboek naar de BI van de Macht wordt verzonden

      1. Verifieer dat het de bestaande dataset overlapt die werd gecreeerd toen u eerst publiceerde.
      1. Controleer of de tabel page_1 correct is bijgewerkt met de kolommen Pagina en Bezoek.
      1. Verifieer dat uw visualisatie gebroken is, aangezien het verwijst naar de kolom van de Mening van de Pagina die niet meer in page_1 lijst aanwezig is.
   **Hier is een voorbeeld van hoe de visualisatie NIET zal breken:**

   1. In de Bouwer van het Rapport, creeer een werkboek met één verzoek, gebruikend de afmeting van de Pagina en metrische de Meningen van de Pagina.
   1. [Plan dit verzoek](/help/analyze/report-builder/whats-new-arb.md#rb-5-5-section) dat u wilt publiceren naar Power BI.
   1. Maak in Power BI een visualisatie voor pagina- en paginaweergaven.
   1. Bewerk nu het werkboek in de Bouwer van het Rapport, het metrische Bezoek terwijl het houden van de Mening van de Pagina en van de Pagina.
   1. Bewerk het programma met het bijgewerkte werkboek en publiceer het verzoek opnieuw aan Power BI.
   1. Zodra het nieuwe werkboek naar de BI van de Macht wordt verzonden

      1. Verifieer dat het de bestaande dataset overlapt die werd gecreeerd toen u eerst publiceerde.
      1. Controleer of de tabel page_1 correct is bijgewerkt met de kolommen Pagina, Paginaweergaven en Bezoeken.
      1. Verifieer dat uw visualisatie behoorlijk blijft werken, aangezien het twee kolommen verwijzingen die nog in page_1 lijst aanwezig zijn.


* **Zaak 2**: U zet een sectie van uw werkboek aan een dashboard in Macht BI vast en u verwijdert later die vastgezette sectie (zoals een grafiek of een lijst) uit het werkboek. Hierdoor wordt de visualisatie verbroken.

## De naam van een Power BI-rapport wijzigen {#section_2E7893A78B914EBFACB2B08CBD9E472E}

Door gebrek, zal de naam van werkboekfilename (zonder de uitbreiding .xlsx) worden bevolkt, behalve dat worden de ruimten vervangen met onderstrepingstekens.

Houd er rekening mee dat

* Het label mag geen combinatie zijn van letters en cijfers die kunnen worden verward met een rij- en kolomadres. A100 kan bijvoorbeeld geen label zijn, omdat dit het adres van een cel in een werkblad is.
* De volgende tekens zijn geen geldige labeltekens: &#39;#&#39;, &#39;@&#39;, &#39;!&#39;, &#39;$&#39;, &#39;^&#39;, &#39;&amp;&#39;, &#39;*&#39;, &#39;`&#39;, &#39;~&#39;, &#39;. Deze worden vervangen door een onderstrepingsteken.
* Wanneer u een ongeldige naam ingaat, zal een waarschuwingsbericht worden getoond dat een auto-geproduceerde naam zal voorstellen. Als u klikt **[!UICONTROL Yes]**, wordt deze naam gebruikt. Als u klikt **[!UICONTROL No]**, zal de Geavanceerde UI van de Tovenaar u de nieuwe naam laten ingaan.

