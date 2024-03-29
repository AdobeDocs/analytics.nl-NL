---
title: Laatste aanraakkanaaldetail
description: Details voor het meest recente marketingkanaal binnen de afloop van de betrokkenheid van de bezoeker.
feature: Dimensions
exl-id: def03267-f3e5-4772-a707-5678c45eba6d
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Laatste aanraakkanaaldetail

De details van het laatste aanraakkanaal [dimensie](overview.md) rapporteert details over het meest recente marketingkanaal waarmee een bezoeker tijdens de aanstellingsperiode van die bezoeker (standaard 30 dagen) een overeenkomst heeft. Deze dimensie is nuttig om te begrijpen wat heeft bijgedragen tot de treffer die een marketingkanaal afstemt. Als een bezoeker bijvoorbeeld naar uw site is gekomen en het marketingkanaal &#39;Betaalde zoekopdracht&#39; heeft gevonden, kunt u met de kanaalgegevens zien welk zoekprogramma is gebruikt of naar welk trefwoord zij hebben gezocht.

## Deze dimensie vullen met gegevens

Deze dimensie kopieert waarden van andere variabelen. De gebruikte variabele verwijst naar de kanaalwaarde binnen elke [Verwerkingsregel voor marketingkanalen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md). Wanneer een hit overeenkomt met een verwerkingsregel voor een marketingkanaal, wordt de instelling [Laatste aanraakkanaal](last-touch-channel.md) De dimensie wordt geplaatst aan de kanaalnaam, en deze afmeting wordt geplaatst aan de kanaalwaarde die in de regel wordt geplaatst.

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Zorg ervoor dat het gewenste afmetingsitem zich in een aanraakkenmerk of aangepaste variabele bevindt.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* Selecteer de gewenste vervolgkeuzelijst onder [!UICONTROL Set the channel's value] binnen de de verwerkingsregel van het Kanaal van de Marketing.
* Het resultaat van de bezoeker op uw site moet overeenkomen met de criteria die worden beschreven in de verwerkingsregel voor marketingkanalen.

## Dimension-items

De items van het Dimension zijn afhankelijk van de kanaalwaarde die in de vervolgkeuzelijst voor de toepasselijke verwerkingsregel voor marketingkanalen wordt vermeld. Als u bijvoorbeeld de waarde van het kanaal instelt op &#39;Pagina-URL&#39;, bevatten dimensie-items pagina-URL&#39;s op uw site. Als u de waarde van het kanaal instelt op Verwijzen van domein, omvatten de afmetingspunten domeinen die bezoekers door klikten om aan uw plaats te krijgen. Deze dimensie voegt alle detaildimensie-items samen, ongeacht in welk kanaal ze zich bevinden.

Adobe raadt aan kanaalwaarden voor het marketingkanaal in te stellen voor informatie over kanalen.
