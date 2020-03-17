---
description: De classificatieregels kijken regelmatig naar niet-geclassificeerde termen. Als een regelovereenkomst wordt gevonden, voegen de regels automatisch de termijnen aan uw lijsten van classificatiegegevens toe. U kunt classificatieregels ook gebruiken om bestaande sleutels te overschrijven.
subtopic: Classifications
title: Classificatieregels
topic: Admin tools
uuid: 08685919-216d-448b-b886-3adf5ff5405e
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Classificatieregels

De classificatieregels kijken regelmatig naar niet-geclassificeerde termen. Als een regelovereenkomst wordt gevonden, voegen de regels automatisch de termijnen aan uw lijsten van classificatiegegevens toe. U kunt classificatieregels ook gebruiken om bestaande sleutels te overschrijven.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

De Bouwer van de Regel laat u tot stand brengen *`classification rule set`*, wat een lijst van is *`classification rules`*. Een regel komt overeen met criteria die u opgeeft en voert vervolgens een handeling uit.

Classificatieregels zijn handig voor:

* **E-mail** - en **weergaveadvertenties**: Maak classificatieregels voor het groeperen van afzonderlijke weergave- en advertentiecampagnes, zodat u kunt leren hoe de weergavecampagnes worden uitgevoerd op basis van e-mailcampagnes.

* **Trackingcodes**: Maak classificatieregels om toetswaarden die zijn afgeleid van tekenreeksen in volgcodes, te categoriseren en deze aan te passen aan specifieke criteria die u definieert.
* **Zoektermen**: Gebruik [reguliere expressies](/help/components/c-classifications2/crb/classification-quickstart-rules.md) en jokertekens om de classificatie van zoektermen te vereenvoudigen. Als een zoekterm bijvoorbeeld een zoekterm bevat *`baseball`*, kunt u een *`Sports League`* classificatie instellen op *`MLB`*.

Stel bijvoorbeeld dat een code voor bijhouden van een e-mailcampagne-id:

`em:Summer:2013:Sale`.

U kunt drie regels instellen in een regelset die de delen van de tekenreeks identificeren en vervolgens de waarden classificeren:

| Regeltype selecteren | Overeenkomstcriteria invoeren | Classificatie instellen | Naar |
|---|---|---|---|
| Begint met | em: | Kanaal | E-mail |
| Eindigt met | Verkoop | Type | Verkoop |
| Bevat | 2013 | Jaar | 2013 |

## Hoe regels worden verwerkt {#how-rules-are-processed}

Belangrijke informatie over de manier waarop classificatieregels worden verwerkt.

<!-- 

about_classification_rules.xml

 -->

* [Belangrijke informatie over regels](/help/components/c-classifications2/crb/classification-rule-builder.md)
* [Wanneer classificeren de regels sleutels niet?](/help/components/c-classifications2/crb/classification-rule-builder.md)
* [Info over Prioriteit regel](/help/components/c-classifications2/crb/classification-quickstart-rules.md)

> [!NOTE] Numerieke 2-classificaties worden [!UICONTROL Rule Builder] niet ondersteund.

## Belangrijke informatie over regels

* Geef [groepsmachtigingen](https://marketing.adobe.com/resources/help/en_US/reference/groups.html) op voor classificaties in [!UICONTROL Admin Tools].

* **Reguliere expressies**: De hulp is beschikbaar onder [Reguliere Uitdrukkingen in de Regels](/help/components/c-classifications2/crb/classification-quickstart-rules.md)van de Classificatie.

* **Reeksen** rapporteren: U kunt geen classificatie kiezen tot minstens één rapportreeks wordt geselecteerd. U kunt niet de rapportreeks toepassen tot u de regelreeks hebt gecreeerd en een variabele toegewezen.

   Wanneer u de regelreeks test, gebruik sleutels (de variabele die) van het rapport wordt geclassificeerd om te zien hoe zij door de regelreeks zullen worden beïnvloed. (De [sleutel](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md) is de variabele die wordt geclassificeerd, of de eerste kolom in de tabel voor het uploaden naar classificatie.)

* **Prioriteit** regel: Als een sleutel veelvoudige regels aanpast die de zelfde classificatie (in de [!UICONTROL Set Classification] kolom) plaatsen, wordt de laatste regel die de classificatie aanpast gebruikt. Zie [Prioriteit](/help/components/c-classifications2/crb/classification-quickstart-rules.md)regel.

* **Beperkingen op het aantal regels**: Er bestaat geen setlimiet voor het aantal regels dat u kunt maken. Een groot aantal regels kan echter van invloed zijn op de prestaties van de browser.
* **Verwerking**: Regels worden regelmatig verwerkt, afhankelijk van uw volume van aan classificatie gerelateerd verkeer.

   De actieve regelverwerking om de vier uur, die classificatiegegevens onderzoeken die typisch één maand teruggaan. De regels controleren automatisch op nieuwe waarden en uploaden de classificaties gebruikend de importeur.

* **Bestaande classificaties** overschrijven: Zie [Wanneer classificeren Regels sleutels niet?](/help/components/c-classifications2/crb/classification-quickstart-rules.md) Indien nodig kunt u bestaande classificaties verwijderen of verwijderen met de importer.

## Wanneer classificeren de regels sleutels niet?

Wanneer u regels activeert, kunt u bestaande classificaties overschrijven. In de volgende situaties classificeert een classificatieregel geen [sleutel](/help/components/c-classifications2/c-classifications-importer/c-saint-data-files.md)(variabele) als:

* De sleutel is al geclassificeerd en u selecteert geen Classificaties [](/help/components/c-classifications2/crb/classification-rule-definitions.md)overschrijven.

   U kunt classificaties beschrijven wanneer het [toevoegen van en het activeren](/help/components/c-classifications2/crb/classification-quickstart-rules.md) van een regel, en wanneer het activeren van een integratie van gegevensschakelaars. (Voor gegevensschakelaars, worden de regels gecreeerd door partners in het Dev Centrum en getoond in [!UICONTROL Classification Rule Builder].)

* Een geclassificeerde sleutel is niet meer in de gegevens weergegeven na een tijdsbestek dat is opgegeven bij het overschrijven van een sleutel, zelfs nadat u Classificaties [](/help/components/c-classifications2/crb/classification-rule-definitions.md)overschrijven hebt ingeschakeld.
* De sleutel wordt niet geclassificeerd en de sleutel wordt nooit overgegaan [!DNL Adobe Analytics] na het tijdkader dat ongeveer een maand geleden begint.

   >[!NOTE]
   >
   >In rapporten zijn classificaties van toepassing op elk opgegeven tijdkader, telkens wanneer een sleutel bestaat. Het datumbereik van een rapport heeft geen invloed op de rapportage.

![](assets/overwrite_keys.png)

## Regelmatige expressies in classificatieregels {#regex-in-classification-rules}

Gebruik reguliere expressies om consistent opgemaakte tekenreekswaarden te laten overeenkomen met een classificatie. U kunt bijvoorbeeld een classificatie maken van specifieke tekens in een trackingcode. U kunt bepaalde tekens, woorden of tekenpatronen met elkaar in overeenstemming brengen.

<!-- 

regex_classification_rules.xml

 -->

* [Reguliere expressie - voorbeeld van code bijhouden](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_2EF7951398EB4C2F8E52CEFAB4032669)
* [Reguliere expressie - een specifiek teken classificeren](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_5D300C03FA484BADACBFCA983E738ACF)
* [Reguliere expressies - overeenstemmende volgcodes van variabele lengte](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_E86F5BF5C2F44ABC8FFCE3EA67EE3BB2)
* [Reguliere expressies - voorbeeld &quot;Bevat niet&quot;](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_FCA88A612A4E4B099458E3EF7B60B59C)
* [Reguliere expressies - referentietabel](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_0211DCB1760042099CCD3ED7A665D716)

> [!NOTE] Reguliere expressies zijn het meest geschikt voor het bijhouden van codes die gebruikmaken van scheidingstekens.

## Reguliere expressie - voorbeeld van code bijhouden {#section_2EF7951398EB4C2F8E52CEFAB4032669}

> [!NOTE] Als het volgen code URL gecodeerd is, zal het **niet** door de Bouwer van Regels worden geclassificeerd.

In dit voorbeeld, veronderstel u volgende campagne-identiteitskaart wilt classificeren:

[!UICONTROL Sample Key]: `em:JuneSale:20130601`

De delen van de volgende code die u wilt classificeren zijn:

* `em` = e-mail
* `JuneSale` = naam campagne
* `20130601` = datum

[!UICONTROL Regular Expression]: `^(.+)\:(.+)\:(.+)$`

Hoe de reguliere expressie correleert met de campagne-id:

![](assets/regex.png)

[!UICONTROL Match Groups]: Toont hoe de reguliere expressie overeenkomt met de campagne-id-tekens, zodat u een positie in de campagne-id kunt classificeren.

![](assets/regex_tracking_code.png)

Dit voorbeeld vertelt de regel dat de campagnedatum bij de derde groep `20140601` is `(.+)`, geïdentificeerd door `$3`.

**[!UICONTROL Rule Builder]**

In [!UICONTROL Rule Builder], vorm de regel als volgt:

| Regeltype selecteren | Overeenkomstcriteria invoeren | Classificatie instellen | Naar |
|---|---|---|---|
| Gewone uitdrukking | &amp;Hoed;(.+)\:(.+)\:(.+)$ | Campagnedatum | $3 |

**Syntaxis**

| Gewone uitdrukking | Tekenreeks of resultaat afstemmen | Overeenkomende overeenkomende groepen |
|--- |--- |--- |
| `^(.+)\:(.+)\:(.+)$` | em:JuneSale:20130601 | `$0`: em:JuneSale:20130601 `$1`: em `$2`: Uitverkoop juni `$3`: 20130601 |
| De syntaxis maken | `^` = begint de lijn () = groepeert karakters en laat u passende karakters tussen de haakjes halen.  `(.+)` = legt één vast ( . ) en ( + ) nog \ = begin van een tekenreeks.  `$` = geeft aan dat het voorgaande teken (of de vorige tekengroep) de laatste op de regel is. |

Zie [Reguliere expressies - Referentietabel](/help/components/c-classifications2/crb/classification-quickstart-rules.md#section_0211DCB1760042099CCD3ED7A665D716) voor informatie over wat de tekens in een reguliere expressie betekenen.

## Reguliere expressie - een specifiek teken classificeren {#section_5D300C03FA484BADACBFCA983E738ACF}

Een manier om een reguliere expressie te gebruiken, is het classificeren van een specifiek teken in een tekenreeks. Stel dat de volgende code twee belangrijke tekens bevat:

[!UICONTROL Sample Key]: `4s3234`

* `4` = merknaam
* `s` = identificeert een zoekmachine, zoals Google

![](assets/regex_char_position.png)

**[!UICONTROL Rule Builder]**

In [!UICONTROL Rule Builder], vorm de regel als volgt:

| Regeltype selecteren | Overeenkomstcriteria invoeren | Classificatie instellen | Naar |
|--- |--- |--- |--- |
| Gewone uitdrukking | `^.(s).*$` | Merk en motor | `$0` (Hiermee legt u de eerste twee tekens vast voor de merknaam en het zoekprogramma.) |
| Gewone uitdrukking | `^.(s).*$` | Zoekmachine | `$1` (Hiermee legt u het tweede teken voor Google vast.) |

## Reguliere expressies - overeenstemmende volgcodes van variabele lengte {#section_E86F5BF5C2F44ABC8FFCE3EA67EE3BB2}

In dit voorbeeld wordt getoond hoe u specifieke tekens kunt identificeren tussen dubbele scheidingstekens wanneer u volgcodes van verschillende lengte hebt. Adobe raadt u aan één reguliere expressie te gebruiken voor elke trackingcode.

Voorbeeldtoetsen:

* `a:b`
* `a:b:c`
* `a:b:c:d`

**Syntaxis**

![](assets/regex_b.png)

![](assets/regex_varying_length.png)

**[!UICONTROL Rule Builder]**

In [!UICONTROL Rule Builder], vorm de regel als volgt:

| Regeltype selecteren | Overeenkomstcriteria invoeren | Classificatie instellen | Naar |
|--- |--- |--- |--- |
| Gewone expressie voor overeenkomende tekenreeks a:b | `^([^\:]+)\:([^\:]+)$` | a | `$1` |
| Gewone expressie voor overeenkomende tekenreeks a:b | `^([^\:]+)\:([^\:]+)$` | b | `$2` |
| Gewone expressie voor overeenkomende tekenreeks a:b:c | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | a | `$1` |
| Gewone expressie voor overeenkomende tekenreeks a:b:c | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | b | `$2` |
| Gewone expressie voor overeenkomende tekenreeks a:b:c | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | c | `$3` |
| Gewone expressie voor overeenkomende tekenreeks a:b:c:d | `^([^\:]+)\:([^\:]+)\:([^\:]+)\:([^\:])$` | d | `$4` |

## Reguliere expressies - voorbeeld &quot;Bevat niet&quot; {#section_FCA88A612A4E4B099458E3EF7B60B59C}

Dit voorbeeld biedt een reguliere expressie die overeenkomt met elke tekenreeks die geen specifieke tekens bevat, in dit geval `13`.

Reguliere expressie:

`^(?!.*13.*).*$`

Tekenreeksen testen:

```
a:b:
a:b:1313
c:d:xoxo
c:d:yoyo
```

Resultaten afstemmen:

```
a:b:
c:d:xoxo
c:d:yoyo
```

In dit resultaat wordt `a:b:1313` geen overeenkomst aangegeven.

## Reguliere expressies - referentietabel {#section_0211DCB1760042099CCD3ED7A665D716}

| Uitdrukking | Beschrijving |
|---|---|
| `(?ms)` | Hiermee zorgt u dat de volledige reguliere expressie overeenkomt met een invoer van meerdere regels, zodat de eigenschap . jokerteken voor nieuwe-regeltekens |
| (`?i`) | Maakt het gehele reguliere-expressiefase ongevoelig |
| [`abc`] | Eén teken van: a, b of c |
| [`^abc`] | Elk enkel teken behalve: a, b of c |
| [`a-z`] | Eén teken in het bereik a-z |
| [`a-zA-Z`] | Eén teken in het bereik a-z of A-Z |
| `^` | Begin van regel (komt overeen met het begin van de regel) |
| `$` | Komt overeen met het einde van de regel (of voor nieuwe regel aan het einde) |
| `\A` | Begin van tekenreeks |
| `\z` | Einde van tekenreeks |
| `.` | Willekeurig teken (behalve een nieuwe regel) |
| `\s` | Willekeurig spatieteken |
| `\S` | Willekeurig teken voor niet-witruimte |
| `\d` | Willekeurig cijfer |
| `\D` | Willekeurig niet-cijfer |
| `\w` | Willekeurig woordteken (letter, getal, onderstrepingsteken) |
| `\W` | Willekeurig niet-woordteken |
| `\b` | Willekeurige woordgrens |
| `(...)` | Alle ingesloten gegevens vastleggen |
| `(a|b)` | a of b |
| `a?` | Nul of een van een |
| `a*` | Nul of meer van een |
| `a+` | Een of meer van een |
| `a{3}` | Precies 3 van a |
| `a{3,}` | 3 of meer van een |
| `a{3,6}` | Tussen 3 en 6 van een |

Een goede bron voor het testen van de geldigheid van reguliere expressies is https://rubular.com/.

## Info over Prioriteit regel

Als een sleutel aan veelvoudige regels wordt aangepast, en het de zelfde classificatiekolom plaatst die in de [!UICONTROL Set Classification] kolom wordt getoond, wordt de laatste regel gebruikt. Als dusdanig, zou u het belangrijkste laatste in uw regelreeks kunnen willen rangschikken.

<!-- 

rule_priority.xml

 -->

Als u veelvoudige regels creeert die niet de zelfde classificatie delen, is de verwerkingsorde niet van belang.

Wat volgt een onderzoek-termijn regelvoorbeeld dat onderzoekstypes voor een atlete classificeert:

| Regelnummer | Type regel | Overeenkomst | Classificatie instellen | Naar |
|---|---|---|---|---|
| 1 | Bevat | Cowboy | Zoektype | Team |
| 2 | Bevat | Fantastische | Zoektype | Fantastische |
| 3 | Bevat | Romo | Zoektype | Speler |

Als een gebruiker naar *`Cowboys fantasy Tony Romo`* zoekt, *`Player`* wordt de term geclassificeerd, omdat deze overeenkomt met de laatst opgegeven classificatie in de kolom Classificatie instellen.

Stel dat u twee regels instelt in een set voor de volgende zoektermen:

| Regelnummer | Type regel | Overeenkomst | Classificatie instellen | Naar |
|---|---|---|---|---|
| 1 | Bevat | Cowboy | Plaats | Dallas |
| 2 | Bevat | Broncos | Plaats | Denver |

Een gebruiker zoekt naar *`Cowboys vs. Broncos`*. Als de regelbouwer een conflict in regel het aanpassen vindt, is de classificatie voor de tweede regel (Ontkent) op dit onderzoek van toepassing.

## Een classificatieregel toevoegen aan een regelset {#add-classification-to-rule-set}

<!-- 

t_classification_rule.xml

 -->

Stappen die beschrijven hoe te om een classificatieregel toe te voegen of uit te geven.

Voeg regels toe door een voorwaarde aan een classificatie aan te passen, en de actie te specificeren.

>[!NOTE]
>
>In deze procedure, moet u de regels op één of meerdere rapportsuites toepassen. Het aanbevolen aantal regels per regel ligt tussen 500 en 1000, hoewel er geen limieten zijn. Als u meer dan 100 regels hebt, kunt u uw regel vereenvoudigen door [subclassificaties](/help/components/c-classifications2/c-sub-classifications.md)te gebruiken.

1. [Maak een set](/help/components/c-classifications2/crb/classification-rule-set.md) classificatieregel.
1. Klik op de pagina met regelsets **[!UICONTROL Add Rule]**.

   ![](assets/add_rule.png)

1. Naast **[!UICONTROL Report Suites]**, klik **[!UICONTROL Add Suites]** om één of meerdere rapportreeksen te specificeren om aan deze regelreeks toe te wijzen.

   De **[!UICONTROL Select Report Suites]** pagina wordt weergegeven.

   >[!NOTE]
   Geef op deze pagina een overzicht van de suites *`only`* als aan de volgende voorwaarden is voldaan:        >

   * Voor de rapporteereeksen is ten minste één classificatie voor die variabele in gedefinieerd [!UICONTROL Admin Tools].
   (Zie *`Variable`* in [Classificatiereeksen](/help/components/c-classifications2/crb/classification-rule-set.md) voor een uitleg van deze voorwaarde.)

   * U hebt de rapportsuite op de **[!UICONTROL Available Report Suites]** pagina geselecteerd. Deze wordt weergegeven nadat u op Regelset [toevoegen hebt geklikt](/help/components/c-classifications2/crb/classification-rule-set.md) om de regelset te maken.


1. Geef op of bestaande waarden moeten worden overschreven:

   | **Regels overschrijven bestaande waarden** | (Standaardinstelling) Overschrijf altijd bestaande classificatietoetsen, inclusief classificaties die via de importer (SAINT) zijn geüpload. |
   |---|---|
   | **Regels overschrijven alleen ongestelde waarden** | Vul alleen lege (niet-ingestelde) cellen in. Bestaande classificaties worden niet gewijzigd. |

1. [Definieer de regel of regels](/help/components/c-classifications2/crb/classification-rule-definitions.md#section_4A5BF384EEEE4994B6DC888339833529).

   ![Stap resultaat](assets/classification_rules_page.png)

   Voor voorbeelden van bouwregels, zie de Bouwer [van de Regel van](/help/components/c-classifications2/crb/classification-rule-builder.md) Classificaties en de Reguliere Uitdrukkingen van de [Classificatieregels](/help/components/c-classifications2/crb/classification-quickstart-rules.md).

   >[!NOTE]
   >
   >Als een sleutel overeenkomt met meerdere regels die dezelfde classificatie instellen (in de kolom Indeling instellen), wordt de laatste regel gebruikt die overeenkomt met de classificatie. Zie **Over Prioriteit** regel hierboven voor meer informatie over sorteerregels.

1. [Test uw regelset](/help/components/c-classifications2/crb/classification-quickstart-rules.md).
1. Na het testen, klik **[!UICONTROL Active]** om de regel te bevestigen en te activeren.

   Als u een regel activeert, wordt het bestand automatisch samengesteld en voor u geüpload.

   Velddefinities: Zie de Bouwer [van de Regel van de](/help/components/c-classifications2/crb/classification-rule-definitions.md) Classificatie voor volledige definities van interfaceopties op deze pagina.

## Een set classificatieregel testen

<!-- 

t_classifications_test_rule.xml

 -->

Stappen die beschrijven hoe een classificatieregel of regelset moet worden getest. Als u een test uitvoert, worden alle regels in een set gecontroleerd.

1. [Maak een set](/help/components/c-classifications2/crb/classification-rule-set.md) classificatieregel.
1. Klik op de naam van de regelset [!UICONTROL Classification Rule Builder]in het deelvenster.
1. Zorg ervoor dat de regelreeks met een rapportreeks wordt geassocieerd.
1. Voor de regelredacteur, klik **[!UICONTROL Test Rule Set]**.

   ![Stap resultaat](assets/classification_test_rule_set.png)

1. Typ of plak testtoetsen in het [!UICONTROL Sample Keys] veld.

   Voorbeelden van voorbeeldtoetsen zijn:

   * Trackingcodes
   * Trefwoorden of woordgroepen zoeken
   Zie [Reguliere expressies in Classificatieregels](/help/components/c-classifications2/crb/classification-quickstart-rules.md) voor informatie over het testen van reguliere expressies.
1. Klik op **[!UICONTROL Run Test]**.

   Regels die overeenkomen, worden weergegeven in de [!UICONTROL Results] tabel.
1. (Optioneel) Klik **[!UICONTROL Activate]** om de regel te activeren en bestaande classificaties te overschrijven.

   Zie voor meer informatie over het gebruiken van regels om bestaande classificaties te beschrijven.

## Classificatieregels valideren en activeren

<!-- 

t_validate_rules.xml

 -->

Stappen die beschrijven hoe classificatieregels moeten worden gevalideerd en geactiveerd.

1. [Maak een set](/help/components/c-classifications2/crb/classification-rule-set.md) classificatieregel en [voeg classificatieregels](/help/components/c-classifications2/crb/classification-quickstart-rules.md) toe aan de set.
1. Voor de regelredacteur, klik **[!UICONTROL Activate]**.

   ![](assets/overwrite_keys.png)

1. (Optioneel) Schakel classificaties in als u deze wilt overschrijven **[!UICONTROL Overwrite classifications for]** *`<selection>`*.

   Met deze optie kunt u bestaande classificaties voor desbetreffende toetsen overschrijven.

   Zie [Regelpagina](/help/components/c-classifications2/crb/classification-rule-definitions.md#section_4A5BF384EEEE4994B6DC888339833529) voor een definitie van deze optie.
