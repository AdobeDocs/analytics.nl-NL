---
title: eVar
description: Een aangepaste dimensie die u kunt gebruiken in rapporten.
translation-type: tm+mt
source-git-commit: f18fbd091333523cd9351bfa461a11f0c3f17bef

---


# eVar

*Deze Help-pagina beschrijft hoe eVars als een dimensie werken. Voor informatie over hoe te om eVars uit te voeren, zie[Vars](/help/implement/vars/page-vars/evar.md)in de de gebruikersgids van het Uitvoeren.*

Variabelen zijn aangepaste variabelen die u kunt gebruiken zoals u dat wilt. Als u een document [van het](/help/implement/prepare/solution-design.md)oplossingsontwerp hebt, komen de meeste dimensies specifiek voor uw organisatie tot eVars. Standaard blijven de eVars behouden na de hit waarop ze zijn ingesteld. U kunt hun vervaldatum en toewijzing onder de variabelen [van de](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) Omzetting in de montages van de rapportreeks aanpassen.

## Hoe werkt eVars

Wanneer u gegevens naar Adobe Analytics verzendt, vertalen de servers van de gegevensinzameling de slag in één enkele rij gegevens met honderden kolommen. Voor elke eVar worden twee kolommen toegewezen; één voor directe gegevensinzameling, en andere voor persisterende waarden.

* Een standaardkolom bevat gegevens die vanuit de afbeeldingsaanvraag naar Adobe worden verzonden.
* Een kolom &quot;post&quot; bevat permanente gegevens, die afhankelijk zijn van de vervaldatum en de toewijzing van de eVar.

Onder bijna alle omstandigheden wordt de `post_evar` kolom gebruikt in rapporten.

### Hoe koppelen we aan metriek

Gebeurtenissen met succes en eVars worden vaak gedefinieerd in verschillende verzoeken om afbeeldingen. In de `post_evar` kolom kunnen eVar-waarden zichzelf aan gebeurtenissen koppelen en gegevens in de rapportage weergeven. Ga bijvoorbeeld als volgt te werk:

1. Een bezoeker arriveert op uw homepage naar uw site.
2. Ze zoeken naar &#39;katten&#39; met behulp van de interne zoekactie van uw site. Met uw implementatie wordt eVar1 ingesteld op intern zoeken.
3. Ze bekijken een product en gaan door met het afrekenen.

Een vereenvoudigde versie van de onbewerkte gegevens ziet er ongeveer als volgt uit:

| `visitor_id` | `pagename` | `evar1` | `post_evar1` | `event_list` |
| --- | --- | --- | --- | --- |
| `examplevisitor_987` | `Home page` |  |  |  |
| `examplevisitor_987` | `Search results` | `cats` | `cats` | `event1` |
| `examplevisitor_987` | `Product page` |  | `cats` | `prodView` |
| `examplevisitor_987` | `Cart` |  | `cats` | `scAdd` |
| `examplevisitor_987` | `Checkout` |  | `cats` | `scCheckout` |
| `examplevisitor_987` | `Purchase confirmation` |  | `cats` | `purchase` |

* De `visitor_id` kolom verbindt hits met dezelfde bezoeker. In onbewerkte gegevens bepalen de samengevoegde waarden van de bezoeker-id `visid_high` en `visid_low` bepalen deze.
* De `pagename` kolom vult de afmetingen Pagina&#39;s in.
* De `evar` kolom bepaalt de klappen wanneer eVar1 uitdrukkelijk werd geplaatst.
* De vorige waarde `post_evar1` wordt meegenomen, afhankelijk van de toewijzing en vervaldatum van de variabele in de instellingen van de rapportsuite.
* De `event_list` kolom bevat alle metrische gegevens. In dit voorbeeld `event1` is &quot;Zoeken&quot; en de andere gebeurtenissen zijn standaardmetingen voor winkelwagentjes. In daadwerkelijke ruwe gegevens, `event_list` bevat een komma-afgebakende reeks aantallen met een raadplegingslijst die die aantallen bindt aan metrisch.

### Gegevensverzameling omzetten in rapportage

Gereedschappen in Adobe Analytics, zoals Analyse Workspace, werken uit deze verzamelde gegevens. Bijvoorbeeld, als u een rapport gebruikend eVar1 als afmeting en Orden als metrisch trok, zou u een rapport gelijkend op het volgende zien:

| `Internal search term (eVar1)` | `Orders` |
| --- | --- |
| `cats` | `1` |

De Werkruimte van de analyse trekt dit rapport gebruikend de volgende logica:

* Kijk door alle `event_list` waarden en kies alle treffers `purchase` erin.
* Geef de `post_evar1` waarde weer van de resultaten.

### Het belang van toewijzing en vervaldatum

Aangezien de toewijzing en de vervaldatum bepalen welke waarden blijven bestaan, zijn zij essentieel om de meeste waarde uit een analytische implementatie te krijgen. Adobe raadt u ten zeerste aan om binnen uw organisatie te bespreken hoe meerdere waarden voor elke eVar worden verwerkt (toewijzing) en wanneer eVars stoppen met het voortduren van gegevens (vervaldatum).

* Standaard gebruikt een eVar de laatste toewijzing. Nieuwe waarden overschrijven persistente waarden.
* Standaard gebruikt een eVar een einde aan een bezoek. Wanneer een bezoek eindigt, kopiëren de waarden niet meer van rij naar rij in de `post_evar` kolom.

U kunt de toewijzing en de vervaldatum van eVar onder de variabelen [van de](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) Omzetting in de montages van de rapportreeks veranderen.
