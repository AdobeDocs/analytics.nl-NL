---
description: Beperkingen bij het gebruik van Report Builder en Microsoft-Power BI.
title: Beperkingen en specificaties
feature: Report Builder
role: User, Admin
exl-id: 4bbeec5b-64bc-4285-9f13-33b223b88834
source-git-commit: ae6ffed05f5a33f032d0c7471ccdb1029154ddbd
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# Beperkingen en specificaties

{{legacy-arb}}

## Power BI publicatiebeperkingen {#section_D4BDD70B20F94A0FAE53531CA528AE42}

>[!NOTE]
>
>Deze beperkingen zijn alleen van toepassing op de optie &quot;Publish Report Builder Requests as Power BI Dataset Tables&quot; (Verzoeken om ).

* Een maximum van 100 verzoeken van de Report Builder kan naar Power BI per werkboek worden uitgevoerd.
* Het planningsproces zal ophouden exporterende verzoeken wanneer het 101e verzoek wordt bereikt.
* Alleen de eerste 10.000 rijen met analysegegevens worden per aanvraag naar de Power BI verzonden. De overige rijen worden genegeerd.

## Een verzoek om Report Builder bewerken na publicatie naar Power BI {#section_6989E74F68DD43F08D37C36B6777DB50}

>[!NOTE]
>
>Deze specificatie is van toepassing op de opties &quot;Publish All Report Builder Requests as Power BI Dataset Tables&quot; en &quot;Publish All Formatted Tables in the Workbook as Power BI Dataset Tables&quot;.

Het bewerken van een Report Builder-aanvraag nadat deze naar Power BI is gepubliceerd, kan problemen veroorzaken.

* **Geval 1**: U publiceert een werkboek aan Power BI en creeert een visualisatie die op zijn gegevens wordt gebaseerd. Daarna, brengt u veranderingen in het werkboek aan, veroorzakend één van de kolommen van de gegevensreeks die het om verwijst te verdwijnen. Vervolgens publiceert u het bestand opnieuw. Hierdoor wordt de visualisatie in Power BI verbroken.

  **hier is een voorbeeld van hoe de visualisatie zal breken:**

   1. In Report Builder, creeer een werkboek met één verzoek, gebruikend de afmeting van de Pagina en metrische de Mening van de Pagina.
   2. Plan dit verzoek om te worden gepubliceerd naar Power BI.
   3. Maak in Power BI een visualisatie voor de weergave van pagina&#39;s en pagina&#39;s.
   4. Bewerk nu het werkboek door Paginaweergaven uit de aanvraag te verwijderen.
   5. Bewerk het programma met het bijgewerkte werkboek en publiceer het verzoek opnieuw aan Power BI.
   6. Zodra het nieuwe werkboek naar Power BI wordt verzonden

      1. Verifieer dat het de bestaande dataset overlapt die werd gecreeerd toen u eerst publiceerde.
      2. Controleer of de tabel page_1 correct is bijgewerkt met de kolommen Pagina en Bezoek.
      3. Verifieer dat uw visualisatie gebroken is, aangezien het verwijst naar de kolom van de Mening van de Pagina die niet meer in page_1 lijst aanwezig is.

  **hier is een voorbeeld van hoe de visualisatie NIET zal breken:**

   1. In Report Builder, creeer een werkboek met één verzoek, gebruikend de afmeting van de Pagina en metrische de Mening van de Pagina.
   2. Plan dit verzoek dat aan Power BI moet worden gepubliceerd.
   3. Maak in Power BI een visualisatie voor de weergave van pagina&#39;s en pagina&#39;s.
   4. Bewerk nu het werkboek in Report Builder en voeg metrisch Bezoek toe terwijl de Pagina- en Paginaweergaven behouden blijven.
   5. Bewerk het programma met het bijgewerkte werkboek en publiceer het verzoek opnieuw aan Power BI.
   6. Zodra het nieuwe werkboek naar Power BI wordt verzonden

      1. Verifieer dat het de bestaande dataset overlapt die werd gecreeerd toen u eerst publiceerde.
      2. Controleer of de tabel page_1 correct is bijgewerkt met de kolommen Pagina, Paginaweergaven en Bezoeken.
      3. Verifieer dat uw visualisatie behoorlijk blijft werken, aangezien het twee kolommen verwijzingen die nog in page_1 lijst aanwezig zijn.

* **Geval 2**: U zet een sectie van uw werkboek aan een dashboard in Power BI vast en u verwijdert later die vastgezette sectie (zoals een grafiek of een lijst) uit het werkboek. Hierdoor wordt de visualisatie verbroken.

## De naam van een Power BI-rapport wijzigen {#section_2E7893A78B914EBFACB2B08CBD9E472E}

Door gebrek, zal de naam van werkboekfilename (zonder de uitbreiding .xlsx) worden bevolkt, behalve dat worden de ruimten vervangen met onderstrepingstekens.

Houd rekening met het volgende:

* Het label mag geen combinatie zijn van letters en cijfers die kunnen worden verward met een rij- en kolomadres. A100 kan bijvoorbeeld geen label zijn, omdat dit het adres van een cel in een werkblad is.
* De volgende tekens zijn geen geldige labeltekens: `'#', '@', '!', '$', '^', '&', '&#42;', '`&#39; en `'~', ' '` . Ze worden vervangen door een onderstrepingsteken.
* Wanneer u een ongeldige naam ingaat, zal een waarschuwingsbericht worden getoond dat een auto-geproduceerde naam zal voorstellen. Als u op **[!UICONTROL Yes]** klikt, wordt deze naam gebruikt. Als u op **[!UICONTROL No]** klikt, kunt u de nieuwe naam invoeren in de interface van de geavanceerde wizard.
