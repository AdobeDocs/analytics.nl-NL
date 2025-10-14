---
title: eVar (dimensie)
description: Een aangepaste dimensie die u kunt gebruiken in rapporten.
feature: Dimensions
exl-id: ce7cc999-281d-4c52-b64d-d44cc320ab2d
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# eVar

*Deze hulppagina beschrijft hoe eVars als a [&#x200B; dimensie &#x200B;](overview.md) werken. Voor informatie over hoe te om eVars uit te voeren, zie [&#x200B; eVars &#x200B;](/help/implement/vars/page-vars/evar.md) in de de gebruikersgids van het Uitvoeren.*

Vars zijn douane [&#x200B; afmetingen &#x200B;](overview.md) die u kunt gebruiken nochtans u houdt van. Als u het document van het oplossingsontwerp van a [&#128279;](/help/implement/prepare/solution-design.md) hebt, beëindigen de meeste dimensies specifiek voor uw organisatie omhoog als [!UICONTROL eVars].

Standaard blijven de eVars behouden na de hit waarop ze zijn ingesteld. Zie de secties [&#x200B; hoe eVars &#x200B;](#how-evars-work) en [&#x200B; werken hoe eVars aan metriek &#x200B;](#how-evars-tie-to-metrics) hieronder voor details op hoe de persistentie van eVar op de architectuur van Adobe werkt. U kunt, hun afloop en toewijzing toelaten onbruikbaar maken of aanpassen onder [&#x200B; variabelen van de Omzetting &#x200B;](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md) in [!UICONTROL Report suite settings]. In de volgende afbeelding ziet u een voorbeeld van eVar-definities in de interface Conversievariabelen:

![&#x200B; Evar voorbeelden &#x200B;](assets/evars-sample.png)

Het aantal beschikbare eVars is afhankelijk van uw contract met Adobe. Er zijn maximaal 250 eVars beschikbaar als uw contract met Adobe dit ondersteunt.

Het hoofdlettergebruik (hoger of lager) in rapporten is gebaseerd op de eerste waarde die u in een bepaalde kalendermaand verzendt. Het hoofdlettergebruik kan afhankelijk van het rapportagevenster worden gewijzigd en het geval van een eVar-waarde die het eerst in die periode wordt verzameld.

## Vars vullen met gegevens

Elke eVar verzamelt gegevens van [`v1` - `v250` vraagkoord &#x200B;](/help/implement/validate/query-parameters.md) in beeldverzoeken. De parameter van de `v1` querytekenreeks verzamelt bijvoorbeeld gegevens voor eVar1, terwijl de parameter van de `v222` querytekenreeks gegevens voor eVar222 verzamelt.

AppMeasurement, dat JavaScript-variabelen compileert in een verzoek om gegevensverzameling, gebruikt de variabelen `eVar1` - `eVar250` . Zie [&#x200B; eVar &#x200B;](/help/implement/vars/page-vars/evar.md) in de de gebruikersgids van het Uitvoeren voor implementatierichtlijnen.

## Dimension-objecten

Aangezien eVars aangepaste tekenreeksen in uw implementatie bevatten, bepaalt uw organisatie wat de dimensie-items voor elke eVar zijn. Zorg ervoor dat u het doel van elke eVar en typische afmetingspunten in het document van het a [&#x200B; oplossingsontwerp &#x200B;](/help/implement/prepare/solution-design.md) registreert.

## Hoe werkt eVars

Wanneer u gegevens naar Adobe Analytics verzendt, vertalen de servers van de gegevensinzameling de slag in één enkele rij gegevens met honderden kolommen. Twee kolommen worden gewijd aan elke eVar; één voor directe gegevensinzameling, en andere voor persisterende waarden.

* Een standaardkolom bevat gegevens die vanuit de afbeeldingsaanvraag naar Adobe worden verzonden.
* Een kolom &quot;post&quot; bevat permanente gegevens, die afhankelijk zijn van de vervaldatum en de allocatie van de eVar.

Onder bijna alle omstandigheden wordt de kolom `post_evar` gebruikt in rapporten.

### Hoe koppelen we aan metriek

Gebeurtenissen met succes en eVars worden vaak op verschillende momenten gedefinieerd. In de kolom `post_evar` kunnen eVar-waarden zichzelf aan gebeurtenissen koppelen en gegevens in de rapportage weergeven. Ga bijvoorbeeld als volgt te werk:

1. Een bezoeker arriveert op uw homepage naar uw site.
2. Ze zoeken naar &#39;katten&#39; met behulp van de interne zoekactie van uw site. In uw implementatie wordt eVar1 gebruikt voor intern zoeken.
3. Ze bekijken een product en gaan door met het afrekenen.

Een vereenvoudigde versie van de onbewerkte gegevens ziet er ongeveer als volgt uit:

| `visitor_id` | `pagename` | `evar1` | `post_evar1` | `event_list` |
| --- | --- | --- | --- | --- |
| `examplevisitor_987` | `Home page` | | | |
| `examplevisitor_987` | `Search results` | `cats` | `cats` | `event1` |
| `examplevisitor_987` | `Product page` | | `cats` | `prodView` |
| `examplevisitor_987` | `Cart` | | `cats` | `scAdd` |
| `examplevisitor_987` | `Checkout` | | `cats` | `scCheckout` |
| `examplevisitor_987` | `Purchase confirmation` | | `cats` | `purchase` |

* De kolom `visitor_id` koppelt items aan dezelfde bezoeker. In onbewerkte gegevens bepalen de samengevoegde waarden van `visid_high` en `visid_low` de bezoeker-id.
* De kolom `pagename` vult de afmetingen Pagina&#39;s in.
* De kolom `evar` bepaalt de hits wanneer eVar1 expliciet werd ingesteld.
* `post_evar1` draagt de vorige waarde, afhankelijk van de toewijzing en de vervaldatum van de variabele die onder de montages van de rapportreeks wordt geplaatst.
* De kolom `event_list` bevat alle metrische gegevens. In dit voorbeeld is `event1` &#39;&#39;Zoeken&#39;&#39; en zijn de andere gebeurtenissen standaardwaarden voor winkelwagentjes. In onbewerkte gegevens bevat `event_list` een door komma&#39;s gescheiden reeks getallen met een opzoektabel die deze getallen koppelt aan een metrische waarde.

### Gegevensverzameling omzetten in rapportage

Gereedschappen in Adobe Analytics, zoals Analysis Workspace, werken uit deze verzamelde gegevens. Bijvoorbeeld, als u een rapport trok gebruikend eVar1 als afmeting en Orders als metrisch, zou u een rapport gelijkend op het volgende zien:

| `Internal search term (eVar1)` | `Orders` |
| --- | --- |
| `cats` | `1` |

Analysis Workspace haalt dit rapport op aan de hand van de volgende logica:

* Bekijk alle `event_list` -waarden en kies alle rijen met `purchase` in de waarden.
* Geef de waarde `post_evar1` weer van deze rijen.

Het resulterende rapport geeft elke andere waarde in `post_evar1` aan de linkerkant weer en hoeveel orders aan die waarde aan de rechterkant zijn toegewezen.

### Het belang van toewijzing en vervaldatum

Aangezien de toewijzing en de vervaldatum bepalen welke waarden blijven bestaan, zijn zij essentieel om de meeste waarde uit een analytische implementatie te krijgen. Adobe raadt u ten zeerste aan om binnen uw organisatie te bespreken hoe meerdere waarden voor elke eVar worden verwerkt (toewijzing) en wanneer eVars stoppen met het aanhouden van gegevens (vervaldatum).

* Een eVar gebruikt standaard de laatste toewijzing. Nieuwe waarden overschrijven persistente waarden.
* Een eVar gebruikt standaard een verloop van een bezoek. Wanneer een bezoek eindigt, kopiëren de waarden niet meer van rij naar rij in de kolom `post_evar` .

U kunt de toewijzing en de vervaldatum van eVar onder [&#x200B; variabelen van de Omzetting &#x200B;](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md) in de reeksinstellingen van het Rapport veranderen.

## Waarde van eVars over props

Adobe raadt in de meeste gevallen eVars aan, ondersteund door het volgende:

* Voor eVars geldt een limiet van 255 bytes in rapporten. Props hebben een limiet van 100 bytes.
* Props blijven standaard behouden na de hit die ze hebben ingesteld. Vars hebben een aangepaste vervaldatum, zodat u kunt bepalen wanneer een eVar geen krediet meer krijgt voor een volgende gebeurtenis. Nochtans, als u [&#x200B; verwerking van de rapporttijd &#x200B;](/help/components/vrs/vrs-report-time-processing.md) gebruikt, zowel kunnen de steunen als eVars een model van de douaneattributie gebruiken.
* Adobe ondersteunt maximaal 250 eVars en slechts 75 props.

Zie [&#x200B; prop &#x200B;](prop.md) voor meer vergelijkingen tussen steunen en eVars.
