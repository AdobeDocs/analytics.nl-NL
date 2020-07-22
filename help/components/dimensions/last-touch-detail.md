---
title: Laatste aanraakkanaaldetail
description: Details voor het meest recente marketingkanaal binnen de afloop van de betrokkenheid van de bezoeker.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# Laatste aanraakkanaaldetail

De dimensie &#39;Laatste aanraakkanaaldetails&#39; rapporteert gegevens over het meest recente marketingkanaal waarmee een bezoeker tijdens de aanspreekperiode van die bezoeker (standaard 30 dagen) een overeenkomst heeft. Deze dimensie is nuttig om te begrijpen wat heeft bijgedragen tot de treffer die een marketingkanaal afstemt. Als een bezoeker bijvoorbeeld naar uw site is gekomen en het marketingkanaal &#39;Betaalde zoekopdracht&#39; heeft gevonden, kunt u met de kanaalgegevens zien welk zoekprogramma is gebruikt of naar welk trefwoord zij hebben gezocht.

## Deze dimensie vullen met gegevens

Deze dimensie kopieert waarden van andere variabelen. De gebruikte variabele verwijst naar de kanaalwaarde binnen elke de verwerkingsregel [van het](/help/admin/admin/marketing-channels-admin.md)Kanaal van de Marketing. Wanneer een hit overeenkomt met een verwerkingsregel voor een marketingkanaal, wordt de dimensie van het [laatste aanraakkanaal](last-touch-channel.md) ingesteld op de kanaalnaam en wordt deze dimensie ingesteld op de kanaalwaarde die in de regel is ingesteld.

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Zorg ervoor dat het gewenste afmetingsitem zich in een aanraakkenmerk of aangepaste variabele bevindt.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* Selecteer de gewenste dropdown waarde onder [!UICONTROL Set the channel's value] de de verwerkingsregel van het Kanaal van de Marketing.
* Het resultaat van de bezoeker op uw site moet overeenkomen met de criteria die worden beschreven in de verwerkingsregel voor marketingkanalen.

## Dimensie-items

Dimensie-items zijn afhankelijk van het vervolgkeuzemenu met kanaalwaarden. Als u bijvoorbeeld de waarde van het kanaal instelt op &#39;Pagina-URL&#39;, bevatten dimensie-items pagina-URL&#39;s op uw site. Als u de waarde van het kanaal instelt op Verwijzen van domein, omvatten de afmetingspunten domeinen die bezoekers door klikten om aan uw plaats te krijgen. Deze dimensie voegt alle detaildimensie-items samen, ongeacht in welk kanaal ze zich bevinden.

Adobe raadt u aan kanaalwaarden voor het marketingkanaal in te stellen voor meer informatie over kanalen.
