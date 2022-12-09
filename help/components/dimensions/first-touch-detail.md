---
title: Eerste aanraakkanaaldetail
description: Details voor het eerste marketingkanaal binnen de afloop van de betrokkenheid van de bezoeker.
feature: Dimensions
exl-id: a155182d-7bc0-4c7d-9de7-680bfe2d6432
source-git-commit: 6f7f46b0fee46e572a65f639ea511478c0118f4e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Eerste aanraakkanaaldetail

De dimensie &#39;First touch channel detail&#39; rapporteert details rond het eerste marketingkanaal waarmee een bezoeker tijdens de betrokkenheidsperiode van die bezoeker overeenkomt (standaard 30 dagen). Deze dimensie is nuttig om te begrijpen wat heeft bijgedragen tot de treffer die een marketingkanaal afstemt. Als een bezoeker bijvoorbeeld naar uw site is gekomen en het marketingkanaal &#39;Betaalde zoekopdracht&#39; heeft gevonden, kunt u met de kanaalgegevens zien welk zoekprogramma is gebruikt of naar welk trefwoord zij hebben gezocht.

## Deze dimensie vullen met gegevens

Deze dimensie kopieert waarden van andere variabelen. De gebruikte variabele verwijst naar de kanaalwaarde binnen elke [Verwerkingsregel voor marketingkanalen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels-admin.md). Wanneer een hit overeenkomt met een verwerkingsregel voor een marketingkanaal, wordt de instelling [Laatste aanraakkanaal](last-touch-channel.md) De dimensie wordt geplaatst aan de kanaalnaam, en deze afmeting wordt geplaatst aan de kanaalwaarde die in de regel wordt geplaatst.

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Zorg ervoor dat het gewenste afmetingsitem zich in een aanraakkenmerk of aangepaste variabele bevindt.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* Selecteer de gewenste vervolgkeuzelijst onder [!UICONTROL Set the channel's value] binnen de de verwerkingsregel van het Kanaal van de Marketing.
* Het resultaat van de bezoeker op uw site moet overeenkomen met de criteria die worden beschreven in de verwerkingsregel voor marketingkanalen _en_ moet de eerste waarde van het marketingkanaal zijn om dit te doen in de aanstellingsperiode van de bezoeker.

Als een volgende hit voldoet aan de criteria onder een ander marketingkanaal, wordt deze dimensie niet overschreven met het nieuwe marketingkanaal.

## Dimension-items

Dimension-items zijn afhankelijk van het vervolgkeuzemenu met kanaalwaarden. Als u bijvoorbeeld de waarde van het kanaal instelt op &#39;Pagina-URL&#39;, bevatten dimensie-items pagina-URL&#39;s op uw site. Als u de waarde van het kanaal instelt op Verwijzen van domein, omvatten de afmetingspunten domeinen die bezoekers door klikten om aan uw plaats te krijgen. Deze dimensie voegt alle detaildimensie-items samen, ongeacht in welk kanaal ze zich bevinden.

Adobe raadt u aan kanaalwaarden voor het marketingkanaal in te stellen voor meer informatie over kanalen.
