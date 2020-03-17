---
description: Maak een gegevenselement in Dynamisch tagbeheer.
keywords: Dynamic Tag Management;data element;create new data element;name;type;default value;force lowercase value;remember this value for
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: Een gegevenselement maken
uuid: eacd5c60-6197-4129-a9e1-a39e9a58b38a
translation-type: tm+mt
source-git-commit: dfe8409b13fcf67eae6a0c404f83c1209f89ae12

---


# Een gegevenselement maken

Maak een gegevenselement in Dynamisch tagbeheer.

1. [Creeer het Bezit](/help/implement/other/dtm/t-create-web-property.md)van het Web, als u dit nog niet hebt gedaan.
1. Klik in de webeigenschap op **[!UICONTROL Rules]** > **[!UICONTROL Data Elements]**.
1. Klik op **[!UICONTROL Create New Data Element]**.
1. Vul de volgende velden en opties in:

   <table id="choicetable_681F7D5B86534FF0B6DB67E117B8E381"> 
    <thead class="chhead sthead"> 
      <th class="choptionhd"> Option</th> 
      <th class="chdeschd"> Beschrijving</th> 
    </thead> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>Naam</strong></td> 
      <td class="chdesc stentry"> <p>De beschrijvende naam van het gegevenselement die een markeerteken kan herkennen. Bijvoorbeeld, 
        <code>
          Product ID
        </code>. </p> <p> <p>Opmerking:  De naam wordt van verwijzingen voorzien door de regelbouwer, niet een identiteitskaart Als u de naam van het Element van Gegevens verandert, moet u zijn verwijzing in elke regel veranderen die het gebruikt. </p> </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>Type</strong></td> 
      <td class="chdesc stentry"> <p> Hiermee geeft u aan waaruit de gegevens worden opgehaald, zoals JS-object, CSS-kiezer, Cookie, URL-parameter of Aangepast script. </p> <p>Afhankelijk van het type dat u selecteert, worden verschillende opties weergegeven. Zie <a href="https://marketing.adobe.com/resources/help/en_US/dtm/data_elements.html"> Typen gegevenselementen</a> in de productdocumentatie voor dynamisch tagbeheer voor meer informatie en voorbeelden. </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>Standaardwaarde</strong></td> 
      <td class="chdesc stentry"> <p>Een standaardelement. Deze waarde zorgt ervoor dat het gegevenselement altijd een waarde heeft, zelfs als een URL-parameter niet bestaat of niet kan worden gevonden door Dynamisch tagbeheer. </p> <p> <p>Opmerking:  Als er geen waarde en geen standaardwaarde is, wordt niets geretourneerd. Om het even welke variabele die dat gegevenselement van verwijzingen voorzien zal niet worden geplaatst. Het veld voor de standaardwaarde wordt genegeerd als het gegevenselement 'aangepaste code' is. </p> </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>Waarde in kleine letters forceren</strong></td> 
      <td class="chdesc stentry"> <p>Met Dynamisch tagbeheer wordt de waarde automatisch verlaagd. </p> </td> 
    </tr> 
    <tr class="chrow strow"> 
      <td class="choption"><strong>Deze waarde onthouden voor</strong></td> 
      <td class="chdesc stentry"> <p>Hoelang u Dynamisch Beheer van de Markering deze waarde wilt herinneren. </p> <p> Geldige waarden zijn: </p> 
      <ul id="ul_52F6CD8FC22942208F3F45492E914104"> 
        <li id="li_32E4366C5B2E46D788CD8478620FE3E0"> <p>Sessie: De op zitting-gebaseerde timing kan afhankelijk van de implementatie variëren. Sessiegegevenselementen worden ingesteld op het sessiecookie. Deze instelling kan echter op een webserver of browser worden gebaseerd. Het heeft geen betrekking op de sessie die wordt gebruikt in marketingrapporten en -analyses. </p> </li> 
        <li id="li_8A944564BF7643E4B21F0EF2394B3FE8"> <p>Voorvertoning </p> </li> 
        <li id="li_5C8A2F2392FD475AA89DDA7D5B5CF88B"> <p>Bezoeker </p> </li> 
      </ul> </td> 
    </tr> 
   </table>

   Zie [Gegevenselementen](https://marketing.adobe.com/resources/help/en_US/dtm/data_elements.html) in de productdocumentatie van het Beheer van de Markering van Adobe voor meer informatie over hoe te om gegevenselementen te gebruiken.
1. Klik op **[!UICONTROL Save Data Element]**.
