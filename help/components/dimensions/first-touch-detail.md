---
title: Eerste aanraakkanaaldetail
description: Details voor het eerste marketingkanaal binnen de afloop van de betrokkenheid van de bezoeker.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Eerste aanraakkanaaldetail

De dimensie &#39;First touch channel detail&#39; rapporteert details rond het eerste marketingkanaal waarmee een bezoeker tijdens de betrokkenheidsperiode van die bezoeker overeenkomt (standaard 30 dagen). Deze dimensie is nuttig om te begrijpen wat heeft bijgedragen tot de treffer die een marketingkanaal afstemt. Als een bezoeker bijvoorbeeld naar uw site is gekomen en het marketingkanaal &#39;Betaalde zoekopdracht&#39; heeft gevonden, kunt u met de kanaalgegevens zien welk zoekprogramma is gebruikt of naar welk trefwoord zij hebben gezocht.

## Deze dimensie vullen met gegevens

Deze dimensie kopieert waarden van andere variabelen. De gebruikte variabele verwijst naar de kanaalwaarde binnen elke de verwerkingsregel [van het](/help/admin/admin/marketing-channels-admin.md)Kanaal van de Marketing. Wanneer een hit overeenkomt met een verwerkingsregel voor een marketingkanaal, wordt de dimensie van het [laatste aanraakkanaal](last-touch-channel.md) ingesteld op de kanaalnaam en wordt deze dimensie ingesteld op de kanaalwaarde die in de regel is ingesteld.

Als u deze dimensie op een specifieke waarde wilt plaatsen, zijn de volgende stappen vereist:

* Controleer of de gewenste waarde voor de afmeting voorkomt in een aanraakkenmerk of aangepaste variabele.
* Plaats een de verwerkingsregel van het Kanaal van de Marketing die de gewenste criteria voor de slag bevat.
* Selecteer de gewenste dropdown waarde onder [!UICONTROL Set the channel's value] de de verwerkingsregel van het Kanaal van de Marketing.
* De bezoeker die op uw site is aangekomen, moet voldoen aan de criteria die worden beschreven in de regel voor verwerking van marketingkanalen __ en dit moet de eerste marketingkanaalwaarde zijn die wordt gebruikt in de aanspreekperiode van de bezoeker.

Als een volgende hit voldoet aan de criteria onder een ander marketingkanaal, wordt deze dimensie niet overschreven met het nieuwe marketingkanaal.

## Dimensiewaarden

Dimensiewaarden zijn afhankelijk van het vervolgkeuzemenu voor kanaalwaarden. Als u bijvoorbeeld de waarde van het kanaal instelt op &#39;Pagina-URL&#39;, bevatten waarden voor de afmetingen pagina-URL&#39;s op uw site. Als u de waarde van het kanaal instelt op Verwijzen naar domein, omvatten de waarden van de afmeting domeinen die bezoekers door klikten om aan uw plaats te krijgen. Deze dimensie voegt alle waarden van de detaildimensie samen, ongeacht in welk kanaal zij zich bevinden.

Adobe raadt u aan kanaalwaarden voor het marketingkanaal in te stellen voor meer informatie over kanalen.
