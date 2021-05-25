---
title: eVar
description: Een aangepaste dimensie die u kunt gebruiken in rapporten.
exl-id: ce7cc999-281d-4c52-b64d-d44cc320ab2d
source-git-commit: f811651dd86786a081bef25942dbb4bece54befa
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---

# eVar

*Deze Help-pagina beschrijft hoe eVars als een dimensie werken. Zie [eVars](/help/implement/vars/page-vars/evar.md) in de gebruikershandleiding Implementeren voor informatie over het implementeren van eVars.*

Variabelen zijn aangepaste variabelen die u kunt gebruiken zoals u dat wilt. Als u een [document van het oplossingsontwerp](/help/implement/prepare/solution-design.md) hebt, komen de meeste dimensies specifiek voor uw organisatie tot eVars. Standaard blijven de eVars behouden na de hit waarop ze zijn ingesteld. U kunt hun vervaldatum en toewijzing aanpassen onder [Conversievariabelen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in de montages van de Reeks van het Rapport.

Het aantal beschikbare eVars is afhankelijk van uw contract met Adobe. Er zijn maximaal 250 eVars beschikbaar als uw contract met Adobe dit ondersteunt.

Het (bovenste of onderste) geval dat bij de rapportage wordt gebruikt, is gebaseerd op de eerste waarde van de back-endsysteemregisters. Deze waarde kan de eerste instantie zijn die ooit wordt gezien of kan variëren met een bepaalde tijdsperiode (bijvoorbeeld maandelijks), afhankelijk van de verscheidenheid en hoeveelheid gegevens die aan de rapportsuite zijn gekoppeld.

## Vars vullen met gegevens

Elke eVar verzamelt gegevens van [`v1` - `v250` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken. Bijvoorbeeld, verzamelt de `v1` parameter van het vraagkoord gegevens voor eVar1, terwijl de `v222` parameter van het vraagkoord gegevens voor eVar222 verzamelt.

AppMeasurement, die JavaScript-variabelen in een afbeeldingsaanvraag voor gegevensverzameling compileert, gebruikt de variabelen `eVar1` - `eVar250`. Zie [eVar](/help/implement/vars/page-vars/evar.md) in de gebruikershandleiding Implementeren voor implementatierichtlijnen.

## Dimension-items

Aangezien eVars aangepaste tekenreeksen in uw implementatie bevatten, bepaalt uw organisatie wat de dimensie-items voor elke eVar zijn. Zorg ervoor u het doel van elke eVar en typische afmetingspunten in een [document van het oplossingsontwerp](/help/implement/prepare/solution-design.md) registreert.

## Hoe werkt eVars

Wanneer u gegevens naar Adobe Analytics verzendt, vertalen de servers van de gegevensinzameling de slag in één enkele rij gegevens met honderden kolommen. Er worden twee kolommen gewijd aan elke eVar; één voor directe gegevensinzameling, en andere voor persisterende waarden.

* Een standaardkolom bevat gegevens die vanuit de afbeeldingsaanvraag naar Adobe worden verzonden.
* Een kolom &quot;post&quot; bevat permanente gegevens, die afhankelijk zijn van de vervaldatum en de toewijzing van de eVar.

Onder bijna alle omstandigheden, wordt de `post_evar` kolom gebruikt in rapporten.

### Hoe koppelen we aan metriek

Gebeurtenissen met succes en eVars worden vaak gedefinieerd in verschillende verzoeken om afbeeldingen. In de kolom `post_evar` kunnen eVar-waarden zichzelf aan gebeurtenissen koppelen en gegevens in rapportage weergeven. Ga bijvoorbeeld als volgt te werk:

1. Een bezoeker arriveert op uw homepage naar uw site.
2. Ze zoeken naar &#39;katten&#39; met behulp van de interne zoekactie van uw site. Uw implementatie gebruikt eVar1 voor intern onderzoek.
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

* De kolom `visitor_id` koppelt items aan dezelfde bezoeker. In daadwerkelijke ruwe gegevens, bepalen de samengevoegde waarden van `visid_high` en `visid_low` bezoekersidentiteitskaart
* In de kolom `pagename` wordt de dimensie Pagina&#39;s gevuld.
* De kolom `evar` bepaalt de klappen wanneer eVar1 uitdrukkelijk werd geplaatst.
* `post_evar1` draagt de vorige waarde, afhankelijk van de toewijzing en de vervaldatum van de variabele die onder de montages van de rapportreeks wordt geplaatst.
* De kolom `event_list` bevat alle metrische gegevens. In dit voorbeeld is `event1` &#39;Searches&#39; en zijn de andere gebeurtenissen standaard winkelwagenmaateenheden. In daadwerkelijke ruwe gegevens, `event_list` bevat een komma-afgebakende reeks aantallen met een raadplegingstabel die die aantallen bindt aan metrisch.

### Gegevensverzameling omzetten in rapportage

Gereedschappen in Adobe Analytics, zoals Analysis Workspace, werken uit deze verzamelde gegevens. Bijvoorbeeld, als u een rapport gebruikend eVar1 als afmeting en Orden als metrisch trok, zou u een rapport gelijkend op het volgende zien:

| `Internal search term (eVar1)` | `Orders` |
| --- | --- |
| `cats` | `1` |

Analysis Workspace haalt dit rapport op met de volgende logica:

* Bekijk alle `event_list` waarden en kies alle treffers met `purchase` erin.
* Uit deze resultaten geeft u de waarde `post_evar1` weer.

### Het belang van toewijzing en vervaldatum

Aangezien de toewijzing en de vervaldatum bepalen welke waarden blijven bestaan, zijn zij essentieel om de meeste waarde uit een analytische implementatie te krijgen. Adobe adviseert hoogst dat u binnen uw organisatie bespreekt hoe de veelvoudige waarden voor elke eVar worden behandeld (toewijzing) en wanneer eVars het persisteren gegevens (afloop) ophouden.

* Standaard gebruikt een eVar de laatste toewijzing. Nieuwe waarden overschrijven persistente waarden.
* Standaard gebruikt een eVar een verloop van een bezoek. Wanneer een bezoek eindigt, kopiëren de waarden niet meer van rij naar rij in de `post_evar` kolom.

U kunt de toewijzing en vervaldatum van eVar wijzigen onder [Conversievariabelen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in de instellingen van de rapportsuite.

## Waarde van eVars over props

Adobe raadt in de meeste gevallen eVars aan, ondersteund door het volgende:

* Voor eVars geldt een limiet van 255 bytes in rapporten. Props hebben een limiet van 100 bytes.
* Props blijven standaard behouden na de hit die ze hebben ingesteld. Vars hebben een aangepaste vervaldatum, zodat u kunt bepalen wanneer een eVar geen krediet meer krijgt voor een volgende gebeurtenis. Nochtans, als u [rapporttijdverwerking](/help/components/vrs/vrs-report-time-processing.md) gebruikt, zowel kunnen de steunen als eVars een model van de douaneattributie gebruiken.
* Adobe ondersteunt maximaal 250 eVars en slechts 75 props.

Zie [prop](prop.md) voor meer vergelijkingen tussen eigenschappen en eVars.
