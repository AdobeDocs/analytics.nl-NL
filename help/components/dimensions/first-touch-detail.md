---
title: Eerste aanraakkanaaldetail
description: Details voor het eerste marketingkanaal binnen de afloop van de betrokkenheid van de bezoeker.
feature: Dimensions
exl-id: a155182d-7bc0-4c7d-9de7-680bfe2d6432
source-git-commit: e934de3938f013067d6bbd6b516b0444b0c9f782
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Eerste aanraakkanaaldetail

De &quot;Eerste detail van het aanrakingskanaal&quot;[&#x200B; dimensie &#x200B;](overview.md) meldt details rond het eerste marketing kanaal een bezoekersgelijken met tijdens de de betrokkenheidsperiode van die bezoeker (30 dagen door gebrek). Deze dimensie is nuttig om te begrijpen wat heeft bijgedragen tot de treffer die een marketingkanaal afstemt. Als een bezoeker bijvoorbeeld naar uw site is gekomen en het marketingkanaal &#39;Betaalde zoekopdracht&#39; heeft gevonden, kunt u met de kanaalgegevens zien welk zoekprogramma is gebruikt of naar welk trefwoord zij hebben gezocht.

## Deze dimensie vullen met gegevens

Deze dimensie kopieert waarden van andere variabelen. De variabele gebruikte verwijzingen de kanaalwaarde binnen elke [&#x200B; de verwerkingsregel van het Kanaal van de Marketing &#x200B;](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md). Wanneer een klap een de verwerkingsregel van het marketingkanaal aanpast, wordt de [&#x200B; Laatste dimensie van het aanrakingskanaal &#x200B;](last-touch-channel.md) geplaatst aan de kanaalnaam, en deze dimensie wordt geplaatst aan de kanaalwaarde die in de regel wordt geplaatst.

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Zorg ervoor dat het gewenste afmetingsitem zich in een aanraakkenmerk of aangepaste variabele bevindt.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* Selecteer de gewenste vervolgkeuzelijst onder [!UICONTROL Set the channel's value] in de verwerkingsregel voor marketingkanalen.
* De klap van de bezoeker aan uw plaats moet de criteria aanpassen die in de de verwerkingsregel van het Kanaal van de Marketing _worden geschetst en_ moet de eerste marketing kanaalwaarde zijn om dit in de de betrokkenheidsperiode van de bezoeker te doen.

Als een volgende hit voldoet aan de criteria onder een ander marketingkanaal, wordt deze dimensie niet overschreven met het nieuwe marketingkanaal.

## Dimension-objecten

Dimension-items zijn afhankelijk van de kanaalwaarde die in de vervolgkeuzelijst voor de toepasselijke verwerkingsregel voor marketingkanalen wordt vermeld. Als u bijvoorbeeld de waarde van het kanaal instelt op &#39;Pagina-URL&#39;, bevatten dimensie-items pagina-URL&#39;s op uw site. Als u de waarde van het kanaal instelt op Verwijzen van domein, omvatten de afmetingspunten domeinen die bezoekers door klikten om aan uw plaats te krijgen. Deze dimensie voegt alle detaildimensie-items samen, ongeacht in welk kanaal ze zich bevinden.

Adobe raadt aan kanaalwaarden voor insight rondom kanaaldetails in te stellen voor het marketingkanaal.
