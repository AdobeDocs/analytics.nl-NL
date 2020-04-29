---
description: Hiermee wordt de hoeveelheid inkomsten gemeten die door al uw producten gedurende een specifieke periode wordt gegenereerd.
title: Ontvangsten
topic: Reports
uuid: e5b72798-f5c7-440d-a62d-376bfd115ac8
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Ontvangsten

Hiermee wordt de hoeveelheid inkomsten gemeten die door al uw producten gedurende een specifieke periode wordt gegenereerd.

Met Revenue kunt u het algemene succes en de trend van uw site bekijken. U kunt het ook gebruiken om periodes te verdelen waar uw plaats bijzonder succesvol was, om de bron te vinden, en dat voor toekomstige campagnes te gebruiken.

## Algemene eigenschappen van rapport {#section_97FC92DFB07D45A79F40B452F9AEE57B}

* Er zijn vereisten waaraan moet worden voldaan voordat dit rapport gegevens kan verzamelen. Binnen dezelfde aanvraag voor een afbeelding moet het volgende plaatsvinden:

   * Een [!UICONTROL purchase] gebeurtenis moet in de `s.events` variabele worden gestart.

   * De `products` variabele moet worden gedefinieerd met een getal in het veld Prijs.
   * Dit zou bijvoorbeeld $35,99 in het opbrengstrapport doorgeven:

      ```js
       s.products="Mens;Shoes;1;35.99"
      ```

      ```js
       s.events="purchase"
      ```

* Wanneer de [!UICONTROL s.products] variabele meer dan één product bevat, telt dit allemaal mee voor het inkomstenverslag. Bijvoorbeeld, zou $9 in opbrengst aan rapportering [!DNL s.products="Mens;Socks;1;4.50,Womens;Socks;1;4.50"] overgaan.

   >[!NOTE]
   >
   >Ontvangsten worden niet vermenigvuldigd wanneer de hoeveelheid in één enkel product wordt verhoogd. Het geeft bijvoorbeeld [!DNL s.products="Womens;Socks;5;4.50"] niet $22,50 door aan rapportage, maar $4,50. Zorg ervoor dat uw implementatie de totale opbrengsten voor het vermelde aantal ( [!DNL s.products="Womens;Socks;5;22.50"]) doorgeeft.

* [!UICONTROL Revenue] het totale bedrag voor een tijdsperiode wordt afgerond op de dichtstbijzijnde valutawaarde. Het rondt niet elk afzonderlijk product of hit.
* Omdat Analytics elke dag naar de dichtstbijzijnde hele valuta afrondt, is het vergelijken van de som van elke dag met het maandelijkse totaal met een zeer klein bedrag. Dit is omdat het maandtotaal niet de som is van elke afgeronde dag, het is de absolute som afgerond op de dichtstbijzijnde hele valuta.
* U kunt een rapport maken dat geen inkomsten naar de dichtstbijzijnde gehele valuta afrondt met een [berekende maatstaf](https://docs.adobe.com/content/help/en/analytics/components/calculated-metrics/cm-overview.html).
* Tenzij de `purchaseID` variabele wordt gebruikt, kunnen gebruikers die de pagina vernieuwen inkomsten verhogen wanneer deze gegevens meerdere keren naar Adobe worden verzonden.
* Uuruitsplitsingen zijn gebaseerd op de tijdzone van de rapportsuite.
* Dit rapport bevat geen regelitems. Deze kan alleen in trended-indeling worden weergegeven.
* De korreligheid van uur, dag, week, maand, kwartaal, en jaar kan worden toegepast. Deze granulariteiten zijn beschikbaar afhankelijk van het bereik van de rapportdatum.
* Dit rapport kan worden uitgesplitst in de volgende rapporten (afhankelijk van de organisatie en de montages van de rapportreeks):

   * [!UICONTROL Time Spent per Visit] verslag.
   * [!UICONTROL Pages and Site Sections] verslag.
   * [!UICONTROL Videos] verslag.
   * [!UICONTROL Page Depth and Entry Pages] verslag.
   * De meeste [!UICONTROL Traffic Sources]rapporten, inclusief [!UICONTROL Search Keywords], [!UICONTROL Search Engines]en [!UICONTROL Referring Domains] rapporten.

   * [!UICONTROL Tracking Code] verslag en alle bijbehorende classificatierapporten.
   * [!UICONTROL Products variable] verslag en alle bijbehorende classificatierapporten. Ook [!UICONTROL Categories] rapporten.

   * Bijna alle [!UICONTROL Visitor Profile] rapporten, exclusief [!UICONTROL GeoSegmentation] rapporten.

   * Alle [!UICONTROL Custom Conversion] variabelen rapporteren met elementaire subrelaties.

* Uitsplitsingen zijn niet per uur beschikbaar.

## Productspecifieke eigenschappen {#section_ED87FFD020634453AABE86B0248BE69B}

* U kunt dit rapport openen door naar **[!UICONTROL Conversion]** > **[!UICONTROL Purchases]** > **[!UICONTROL Revenue]**.

* [!UICONTROL Traffic Sources] de uitsplitsingen zijn te vinden onder [!UICONTROL Finding Methods].

* U kunt dit rapport openen door naar **[!UICONTROL Site Metrics]** > **[!UICONTROL Purchases]** > **[!UICONTROL Revenue]**.

* Naast alle eerder vermelde uitsplitsingen zijn er [!UICONTROL First and Last Touch Marketing Channel] uitsplitsingen beschikbaar.

* U kunt dit rapport ook openen door naar **[!UICONTROL Site Metrics]** > **[!UICONTROL Purchases]** > **[!UICONTROL Revenue]**.

* Naast de eerder genoemde uitsplitsingen kunnen ook [!UICONTROL List]variabelen en de huidige [!UICONTROL Video] variabelen worden gebruikt.

* Dit rapport kan segmenten gebruiken.

* U kunt elk punt in dit rapport door alle andere rapporten en variabelen verdelen, toestaand u om onderverdelingen door om het even welke granulariteit te zien die u zou willen.
* U kunt alle [!UICONTROL conversion] en [!UICONTROL traffic] metriek naast elkaar gebruiken [!UICONTROL Revenue]. U kunt verschillende toewijzingen gebruiken voor alle [!UICONTROL conversion] metriek.

* Dit rapport kan veelvoudige hoogst gevorderde segmenten gebruiken.

Als dit rapport niet beschikbaar is op de opgegeven locatie, neemt u contact op met de beheerder. Ze hebben mogelijk de standaardnaam of menustructuur gewijzigd om beter aan de unieke behoeften van uw organisatie te voldoen.
