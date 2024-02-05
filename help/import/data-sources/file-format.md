---
title: Bestandsindeling gegevensbron
description: U moet een bestand op de juiste manier genereren voor gebruik in gegevensbronnen.
exl-id: 6632b970-e931-4272-a69b-c1130ad6475f
feature: Data Sources
role: Admin
source-git-commit: cc25fe304d9cab3db3fa2ddd306338ff3bb88a55
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 3%

---

# Bestandsindeling gegevensbron

Gegevensbronbestanden hebben de volgende eigenschappen:

* Het bestand staat in `.txt` gebruiken.
* Lijnen met opmerkingen beginnen met &#39;`#`en zijn optioneel.
* De eerste regel zonder opmerkingen bevat de koppen van het bestand.
* De eerste waarde van elke rij is de datum, die het formaat gebruikt `MM/DD/YYYY` of `MM/DD/YYYY/HH/mm/SS`.
* Waarden op elke rij, inclusief kopteksten, worden gescheiden door tabs.
* Elke rij moet minstens één afmeting en één metrisch hebben.

## Opmerkingen

Elke rij die begint met &#39;`#`&#39; is een opmerking. Bij het downloaden van een gegevensbronsjabloonbestand zijn de eerste twee regels opmerkingen.

* De eerste opmerking geeft het type sjabloon aan dat u hebt geconfigureerd voor de gegevensbron, de achterste gebruiker-id die de gegevensbron heeft gemaakt en de gegevensbron-id.
* De tweede opmerking bevat vriendelijke namen voor elk van de kopteksten die in het sjabloonbestand zijn opgenomen.

Alle rijen met opmerkingen worden door de Adobe genegeerd wanneer het bestand wordt verwerkt, zodat u de sjabloonopmerkingen kunt verwijderen of uw eigen opmerkingen in het hele bestand kunt toevoegen. U kunt alleen opmerkingen toevoegen aan volledige rijen. U kunt geen opmerkingen toevoegen aan afzonderlijke velden of gedeeltelijke rijen.

## Kopteksten

Bij het uploaden van gegevensbronbestanden zijn kolomkoppen vereist. Deze kolomkoppen zijn niet hoofdlettergevoelig, maar vereiste spaties zijn nodig (bijvoorbeeld `eVar1` is een ongeldige koptekst, terwijl `EVAR 1` is geldig). Kolomkoppen zijn van toepassing op alle rapportsuites. Gebruik de volgende tabellen om ervoor te zorgen dat elke header in het gegevensbronbestand correct is ingesteld.

>[!TIP]
>
>U kunt een bestand met gegevensbronnen helemaal opnieuw maken als u de juiste koppen in het gegevensbronbestand opneemt. Er is geen limiet aan het aantal kopteksten dat u in één bestand kunt opnemen. Elke rij kan echter maximaal 4096 bytes bevatten.

| Dimension | Koptekst gegevensbron |
| --- | --- |
| [Categorie](/help/components/dimensions/category.md) | `Category` |
| [eVar1 - eVar250](/help/components/dimensions/evar.md) | `Evar 1` - `Evar 250` |
| [Marketingkanaal](/help/components/dimensions/marketing-channel.md) | `Marketing Channel` |
| [Detail marketingkanaal](/help/components/dimensions/marketing-detail.md) | `Marketing Channel Detail` |
| [Product](/help/components/dimensions/product.md) | `Product` |
| [Trackingcode](/help/components/dimensions/tracking-code.md) | `Tracking Code` |
| [Transactie-id](/help/implement/vars/page-vars/transactionid.md) | `transactionID` |
| [Postcode](/help/components/dimensions/zip-code.md) | `Zip` |

{style="table-layout:auto"}

Dimensionen en metriek komen in dezelfde koptekstrij.

| Metrisch | Koptekst gegevensbron |
| --- | --- |
| [Toevoegingen aan winkelwagen](/help/components/metrics/cart-additions.md) | `Cart Adds` |
| [Verwijderingen uit winkelwagen](/help/components/metrics/cart-removals.md) | `Cart Removes` |
| [Weergaven winkelwagen](/help/components/metrics/cart-views.md) | `Cart Views` |
| [Houtskaarten](/help/components/metrics/carts.md) | `Cart Opens` |
| [Betalingen](/help/components/metrics/checkouts.md) | `Checkouts` |
| [Aangepaste gebeurtenissen](/help/components/metrics/custom-events.md) | `Event 1` - `Event 1000` |
| [Orders](/help/components/metrics/orders.md) | `Orders` |
| [Omzet](/help/components/metrics/revenue.md) | `Price` |
| [Eenheden](/help/components/metrics/units.md) | `Quantity` |

{style="table-layout:auto"}

Adobe ondersteunt geen gegevensbronnen voor andere dimensies of metriek. Als andere variabelen nodig zijn dan de variabelen in de bovenstaande tabellen, kunt u het volgende doen: [Opsommings-API voor gegevens](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/) in plaats daarvan.

## Datum

De eerste waarde in elke rij **moet** de datum zijn. De datumnotatie moet een van de volgende notaties hebben:

* **`MM/DD/YYYY/HH/mm/SS`**
* **`MM/DD/YYYY`**

Als u de uren/minuten/seconden weglaat, wordt de tijdstempel automatisch ingesteld op 12 uur voor die dag.

Eén gegevensbronbestand ondersteunt maximaal 90 unieke dagen. Als u meer dan 90 unieke dagen wilt opnemen in een upload, splitst u de gegevens in meerdere bestanden.

## Dimension- en metrische gegevens

De volgende waarden na de datum in elke rij bevatten de gegevens die u wilt uploaden. Elke rij komt overeen met die tijdstempel. Zorg ervoor dat op elke rij hetzelfde aantal tabbladen voorkomt. De kolommen kunnen in om het even welke orde zijn; zorg ervoor dat de gegevens in elke rij op de kopballen bij de bovenkant richten. De maximale hoeveelheid gegevens die één rij kan bevatten, is 4096 bytes.

Gegevens van Dimension mogen geen puntkomma&#39;s bevatten (`;`). Rijen met puntkomma&#39;s worden overgeslagen.

## Volgende stappen

[Bestand uploaden](file-upload.md): Leer het uploaden van een gegevensbronbestand voor inname door Adobe.
