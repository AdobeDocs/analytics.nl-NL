---
title: eVar (dimensie)
description: Een aangepaste dimensie die u kunt gebruiken in rapporten.
feature: Dimensions
exl-id: ce7cc999-281d-4c52-b64d-d44cc320ab2d
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 0%

---

# eVar

*In deze Help-pagina wordt beschreven hoe eVars werken als een [dimensie](overview.md). Voor informatie over het implementeren van eVars raadpleegt u [eVars](/help/implement/vars/page-vars/evar.md) in de gebruikershandleiding Implementeren.*

Variabelen zijn aangepaste variabelen die u kunt gebruiken. Als u een [document ontwerp oplossing](/help/implement/prepare/solution-design.md), komen de meeste dimensies die specifiek zijn voor uw organisatie neer op [!UICONTROL eVars], naast de standaardafmetingen die beschikbaar zijn in Adobe Analytics, zoals &#39;Paginanaam&#39;, &#39;Referring Domain&#39; en &#39;Channel&#39;. Zie [Overzicht van Dimension](overview.md) voor meer informatie .

Standaard blijven de eVars behouden na de hit waarop ze zijn ingesteld. U kunt de vervaldatum en de toewijzing aanpassen onder [Conversievariabelen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in [!UICONTROL Report suite settings]. Zie hieronder voor een voorbeeld van eVar-definities in de interface Conversievariabelen.

![Voorbeelden van gebeurtenissen](assets/evars-sample.png)

Het aantal beschikbare eVars is afhankelijk van uw contract met Adobe. Er zijn maximaal 250 eVars beschikbaar als uw contract met Adobe dit ondersteunt.

Het (bovenste of onderste) geval dat bij de rapportage wordt gebruikt, is gebaseerd op de eerste waarde van de back-endsysteemregisters. Deze waarde kan de eerste instantie zijn die ooit wordt gezien of kan variëren met een bepaalde tijdsperiode (bijvoorbeeld maandelijks), afhankelijk van de verscheidenheid en hoeveelheid gegevens die aan de rapportsuite zijn gekoppeld.

## Vars vullen met gegevens

Elke eVar verzamelt gegevens van de [`v1` - `v250` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. Bijvoorbeeld de `v1` de parameter van het vraagkoord verzamelt gegevens voor eVar1, terwijl `v222` de parameter van het vraagkoord verzamelt gegevens voor eVar222.

AppMeasurement, dat JavaScript-variabelen compileert in een afbeeldingsaanvraag voor gegevensverzameling, gebruikt de variabelen `eVar1` - `eVar250`. Zie [eVar](/help/implement/vars/page-vars/evar.md) in de gebruikershandleiding Implementeren voor implementatierichtlijnen.

## Dimension-items

Aangezien eVars aangepaste tekenreeksen in uw implementatie bevatten, bepaalt uw organisatie wat de dimensie-items zijn voor elke eVar. Zorg ervoor dat u het doel van elke eVar en typische afmetingspunten in een registreert [document ontwerp oplossing](/help/implement/prepare/solution-design.md).

## Hoe werkt eVars

Wanneer u gegevens naar Adobe Analytics verzendt, vertalen de servers van de gegevensinzameling de slag in één enkele rij gegevens met honderden kolommen. Twee kolommen worden gewijd aan elke eVar; één voor directe gegevensinzameling, en andere voor persisterende waarden.

* Een standaardkolom bevat gegevens die naar de Adobe worden verzonden vanuit de afbeeldingsaanvraag.
* Een kolom &quot;post&quot; bevat permanente gegevens, die afhankelijk zijn van de vervaldatum en de allocatie van de eVar.

Onder vrijwel alle omstandigheden `post_evar` wordt gebruikt in rapporten.

### Hoe koppelen we aan metriek

Gebeurtenissen met succes en eVars worden vaak gedefinieerd in verschillende verzoeken om afbeeldingen. De `post_evar` in de kolom kunnen eVar-waarden zichzelf aan gebeurtenissen koppelen en gegevens in de rapportage weergeven. Ga bijvoorbeeld als volgt te werk:

1. Een bezoeker arriveert op uw homepage naar uw site.
2. Ze zoeken naar &#39;katten&#39; met behulp van de interne zoekactie van uw site. Uw implementatie gebruikt eVar1 voor intern onderzoek.
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

* De `visitor_id` kolombindingen worden aan dezelfde bezoeker gekoppeld. In onbewerkte gegevens worden de samengevoegde waarden van `visid_high` en `visid_low` Bepaal bezoeker-id.
* De `pagename` wordt de pagina&#39;s gevuld.
* De `evar` de kolom bepaalt de klappen wanneer eVar1 uitdrukkelijk werd geplaatst.
* De `post_evar1` draagt de vorige waarde, afhankelijk van de toewijzing en de vervaldatum van de variabele die onder de montages van de rapportreeks wordt geplaatst.
* De `event_list` de kolom bevat alle metrische gegevens. In dit voorbeeld: `event1` is &#39;Zoekopdrachten&#39;, en de andere gebeurtenissen zijn standaardmetingen voor winkelwagentjes. In de feitelijke onbewerkte gegevens `event_list` bevat een kommagescheiden reeks getallen met een opzoektabel die deze getallen koppelt aan metrische getallen.

### Gegevensverzameling omzetten in rapportage

Gereedschappen in Adobe Analytics, zoals Analysis Workspace, werken uit deze verzamelde gegevens. Bijvoorbeeld, als u een rapport gebruikend eVar1 als afmeting en Orden als metrisch trok, zou u een rapport gelijkend op het volgende zien:

| `Internal search term (eVar1)` | `Orders` |
| --- | --- |
| `cats` | `1` |

Analysis Workspace haalt dit rapport op aan de hand van de volgende logica:

* Alles doorzoeken `event_list` waarden en kies alle resultaten met `purchase` in hen.
* Uit deze resultaten kunt u de opdracht `post_evar1` waarde.

### Het belang van toewijzing en vervaldatum

Aangezien de toewijzing en de vervaldatum bepalen welke waarden blijven bestaan, zijn zij essentieel om de meeste waarde uit een analytische implementatie te krijgen. De Adobe adviseert hoogst dat u binnen uw organisatie bespreekt hoe de veelvoudige waarden voor elke eVar worden behandeld (toewijzing) en wanneer eVars het persisteren gegevens (afloop) ophouden.

* Standaard gebruikt een eVar de laatste toewijzing. Nieuwe waarden overschrijven persistente waarden.
* Standaard gebruikt een eVar een verloop van een bezoek. Wanneer een bezoek eindigt, kopiëren de waarden niet meer van rij naar rij in `post_evar` kolom.

U kunt de toewijzing en vervaldatum van eVar wijzigen onder [Conversievariabelen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md) in de instellingen van de rapportsuite.

## Waarde van eVars over props

Adobe raadt in de meeste gevallen eVars aan, ondersteund door het volgende:

* Voor eVars geldt een limiet van 255 bytes in rapporten. Props hebben een limiet van 100 bytes.
* Props blijven standaard behouden na de hit die ze hebben ingesteld. Vars hebben een aangepaste vervaldatum, zodat u kunt bepalen wanneer een eVar geen krediet meer krijgt voor een volgende gebeurtenis. Als u echter [rapporttijdverwerking](/help/components/vrs/vrs-report-time-processing.md)kunnen zowel props als eVars een aangepast attributiemodel gebruiken.
* Adobe ondersteunt maximaal 250 eVars en slechts 75 props.

Zie [prop](prop.md) voor meer vergelijkingen tussen props en eVars.
