---
description: De classificatieregels kijken regelmatig naar niet-geclassificeerde termen. Als een regelovereenkomst wordt gevonden, voegen de regels automatisch de termijnen aan uw lijsten van classificatiegegevens toe. U kunt classificatieregels ook gebruiken om bestaande sleutels te overschrijven.
title: Classificatieregels
feature: Classifications
exl-id: 8fe5d838-fa89-4933-a0c0-498d4e59576d
source-git-commit: 750c4b0ffb52c3f2cf25abcd76ef149a4521109e
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 0%

---

# Classificatieregels

De classificatieregels kijken regelmatig naar niet-geclassificeerde termen. Als een regelovereenkomst wordt gevonden, voegen de regels automatisch de termijnen aan uw lijsten van classificatiegegevens toe. U kunt classificatieregels ook gebruiken om bestaande sleutels te overschrijven.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

De Bouwer van de Regel laat u tot een *classificatieregel*, dat een lijst is van *classificatieregels*. Een regel komt overeen met criteria die u opgeeft en voert vervolgens een handeling uit.

Classificatieregels zijn handig voor:

* **E-mail** en **Advertenties weergeven**: Maak classificatieregels voor het groeperen van afzonderlijke weergave- en advertentiecampagnes, zodat u kunt zien hoe de weergavecampagnes worden uitgevoerd op basis van e-mailcampagnes.

* **Trackingcodes**: Maak classificatieregels om toetswaarden te categoriseren die zijn afgeleid van tekenreeksen in volgcodes, en breng deze aan specifieke criteria aan die u definieert.
* **Zoektermen**: Gebruik [reguliere expressies](/help/components/classifications/crb/classification-quickstart-rules.md) en jokertekens om de classificatie van zoektermen te vereenvoudigen. Een zoekterm bevat bijvoorbeeld *`baseball`* kunt u een *`Sports League`* indeling naar *`MLB`*.

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

* [Belangrijke informatie over regels](/help/components/classifications/crb/classification-rule-builder.md)
* [Wanneer classificeren de regels sleutels niet?](/help/components/classifications/crb/classification-rule-builder.md)
* [Info over Prioriteit regel](/help/components/classifications/crb/classification-quickstart-rules.md)

>[!NOTE]
>
>De [!UICONTROL Rule Builder] biedt geen ondersteuning voor numerieke 2-classificaties.

## Belangrijke informatie over regels

* Opgeven [groepsmachtigingen](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-groups/groups.html?lang=nl-NL) voor classificaties in [!UICONTROL Admin Tools].

* **Reguliere expressies**: Help is beschikbaar onder [Regelmatige expressies in classificatieregels](/help/components/classifications/crb/classification-quickstart-rules.md).

* **Reeksen rapporteren**: U kunt pas een classificatie kiezen als ten minste één rapportsuite is geselecteerd. U kunt niet de rapportreeks toepassen tot u de regelreeks hebt gecreeerd en een variabele toegewezen.

  Wanneer u de regelreeks test, gebruik sleutels (de variabele die) van het rapport wordt geclassificeerd om te zien hoe zij door de regelreeks zullen worden beïnvloed. (De [key](/help/components/classifications/importer/c-saint-data-files.md) is de variabele die wordt geclassificeerd, of de eerste kolom in de tabel voor het uploaden naar classificatie.)

* **Prioriteit regel**: Als een sleutel overeenkomt met meerdere regels die dezelfde classificatie instellen (in het dialoogvenster [!UICONTROL Set Classification] kolom), wordt de laatste regel gebruikt die overeenkomt met de classificatie. Zie [Info over Prioriteit regel](/help/components/classifications/crb/classification-quickstart-rules.md).

* **Grenswaarden voor het aantal regels**: Er bestaat geen setlimiet voor het aantal regels dat u kunt maken. Een groot aantal regels kan echter van invloed zijn op de prestaties van de browser.
* **Verwerking**: Regels worden regelmatig verwerkt, afhankelijk van uw volume van aan classificatie gerelateerd verkeer.

  De actieve regelverwerking om de vier uur, die classificatiegegevens onderzoeken die typisch één maand teruggaan. De regels controleren automatisch op nieuwe waarden en uploaden de classificaties gebruikend de importeur.

* **Bestaande classificaties overschrijven**: Zie [Wanneer classificeren de regels sleutels niet?](/help/components/classifications/crb/classification-quickstart-rules.md) Indien nodig kunt u bestaande classificaties verwijderen of verwijderen met de importer.

## Wanneer classificeren de regels sleutels niet?

Wanneer u regels activeert, kunt u bestaande classificaties overschrijven. In de volgende situaties wordt met een classificatieregel een [key](/help/components/classifications/importer/c-saint-data-files.md)(variabele) indien:

* De sleutel is al geclassificeerd en u selecteert [Classificaties overschrijven](/help/components/classifications/crb/classification-rule-definitions.md).

  U kunt classificaties overschrijven wanneer [toevoegen en activeren](/help/components/classifications/crb/classification-quickstart-rules.md) een regel, en wanneer het activeren van een integratie van gegevensschakelaars. (Voor gegevensschakelaars, worden de regels gecreeerd door partners in het Dev Centrum en getoond in [!UICONTROL Classification Rule Builder].)

* Een geclassificeerde sleutel is niet meer in de gegevens weergegeven na een opgegeven tijdsperiode bij het overschrijven van een sleutel, zelfs nadat u [Classificaties overschrijven](/help/components/classifications/crb/classification-rule-definitions.md).
* De sleutel wordt niet geclassificeerd en de sleutel wordt nooit doorgegeven [!DNL Adobe Analytics] na het tijdsbestek dat ongeveer een maand geleden is begonnen.

  >[!NOTE]
  >
  >In rapporten zijn classificaties van toepassing op elk opgegeven tijdkader, telkens wanneer een sleutel bestaat. Het datumbereik van een rapport heeft geen invloed op de rapportage.

![](assets/overwrite_keys.png)

## Regelmatige expressies in classificatieregels {#regex-in-classification-rules}

Gebruik reguliere expressies om consistent opgemaakte tekenreekswaarden te laten overeenkomen met een classificatie. U kunt bijvoorbeeld een classificatie maken van specifieke tekens in een trackingcode. U kunt bepaalde tekens, woorden of tekenpatronen met elkaar in overeenstemming brengen.

<!-- 

regex_classification_rules.xml

 -->

* [Reguliere expressie - voorbeeld van code bijhouden](/help/components/classifications/crb/classification-quickstart-rules.md#section_2EF7951398EB4C2F8E52CEFAB4032669)
* [Reguliere expressie - een specifiek teken classificeren](/help/components/classifications/crb/classification-quickstart-rules.md#section_5D300C03FA484BADACBFCA983E738ACF)
* [Reguliere expressies - overeenstemmende volgcodes van variabele lengte](/help/components/classifications/crb/classification-quickstart-rules.md#section_E86F5BF5C2F44ABC8FFCE3EA67EE3BB2)
* [Reguliere expressies - voorbeeld &quot;Bevat niet&quot;](/help/components/classifications/crb/classification-quickstart-rules.md#section_FCA88A612A4E4B099458E3EF7B60B59C)
* [Reguliere expressies - referentietabel](/help/components/classifications/crb/classification-quickstart-rules.md#section_0211DCB1760042099CCD3ED7A665D716)

>[!NOTE]
>
>Reguliere expressies zijn het meest geschikt voor het bijhouden van codes die gebruikmaken van scheidingstekens.

## Reguliere expressie - voorbeeld van code bijhouden {#section_2EF7951398EB4C2F8E52CEFAB4032669}

>[!NOTE]
>
>Als de trackingcode URL-gecodeerd is, wordt **niet** door de Bouwer van Regels worden geclassificeerd.

In dit voorbeeld, veronderstel u volgende campagne-identiteitskaart wilt classificeren:

[!UICONTROL Sample Key]: `em:JuneSale:20130601`

De delen van de volgende code die u wilt classificeren zijn:

* `em` = e-mail
* `JuneSale` = naam campagne
* `20130601` = datum

[!UICONTROL Regular Expression]: `^(.+)\:(.+)\:(.+)$`

Hoe de reguliere expressie correleert met de campagne-id:

![](assets/regex.png)

[!UICONTROL Match Groups]: Hiermee wordt getoond hoe de reguliere expressie overeenkomt met de campagne-id-tekens, zodat u een positie in de campagne-id kunt classificeren.

![](assets/regex_tracking_code.png)

In dit voorbeeld wordt de regel getoond dat de datum van de campagne `20140601` bevindt zich bij de derde groep `(.+)`, geïdentificeerd door `$3`.

**[!UICONTROL Rule Builder]**

In de [!UICONTROL Rule Builder]Configureer de regel als volgt:

| Regeltype selecteren | Overeenkomstcriteria invoeren | Classificatie instellen | Naar |
|---|---|---|---|
| Gewone uitdrukking | &Hoed;(.+)\:(.+)\:(.+)$ | Campagnedatum | $ 3 |

**Syntaxis**

| Gewone uitdrukking | Tekenreeks of resultaat afstemmen | Overeenkomende overeenkomende groepen |
|--- |--- |--- |
| `^(.+)\:(.+)\:(.+)$` | `em:JuneSale:20130601` | `$0`: `em:JuneSale:20130601`  `$1`: em  `$2`: JuneSale  `$3`20130601 |
| De syntaxis maken | `^` = start de regel () = groepeert tekens en laat u overeenkomende tekens tussen haakjes extraheren.  `(.+)` = legt één vast ( . ) en ( + ) nog \ = begin van een tekenreeks.  `$` = geeft aan dat het voorgaande teken (of de vorige tekengroep) de laatste op de regel is. |

Zie [Reguliere expressies - referentietabel](/help/components/classifications/crb/classification-quickstart-rules.md#section_0211DCB1760042099CCD3ED7A665D716) voor informatie over wat de tekens in een reguliere expressie betekenen.

## Reguliere expressie - een specifiek teken classificeren {#section_5D300C03FA484BADACBFCA983E738ACF}

Een manier om een reguliere expressie te gebruiken, is het classificeren van een specifiek teken in een tekenreeks. Stel dat de volgende code twee belangrijke tekens bevat:

[!UICONTROL Sample Key]: `4s3234`

* `4` = merknaam
* `s` = identificeert een onderzoeksmotor zoals Google

![](assets/regex_char_position.png)

**[!UICONTROL Rule Builder]**

In de [!UICONTROL Rule Builder]Configureer de regel als volgt:

| Regeltype selecteren | Overeenkomstcriteria invoeren | Classificatie instellen | Naar |
|--- |--- |--- |--- |
| Gewone uitdrukking | `^.(s).*$` | Merk en motor | `$0` (De eerste twee tekens worden vastgelegd voor de merknaam en het zoekprogramma.) |
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

In de [!UICONTROL Rule Builder]Configureer de regel als volgt:

| Regeltype selecteren | Overeenkomstcriteria invoeren | Classificatie instellen | Naar |
|--- |--- |--- |--- |
| Gewone expressie voor overeenkomende tekenreeks `a:b` | `^([^\:]+)\:([^\:]+)$` | a | `$1` |
| Gewone expressie voor overeenkomende tekenreeks `a:b` | `^([^\:]+)\:([^\:]+)$` | b | `$2` |
| Gewone expressie voor overeenkomende tekenreeks `a:b:c` | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | a | `$1` |
| Gewone expressie voor overeenkomende tekenreeks `a:b:c` | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | b | `$2` |
| Gewone expressie voor overeenkomende tekenreeks `a:b:c` | `^([^\:]+)\:([^\:]+)\:([^\:]+)$` | c | `$3` |
| Gewone expressie voor overeenkomende tekenreeks `a:b:c:d` | `^([^\:]+)\:([^\:]+)\:([^\:]+)\:([^\:])$` | d | `$4` |

## Reguliere expressies - voorbeeld &quot;Bevat niet&quot; {#section_FCA88A612A4E4B099458E3EF7B60B59C}

In dit voorbeeld wordt een reguliere expressie geboden die overeenkomt met elke tekenreeks die geen specifieke tekens bevat, in dit geval `13`.

Reguliere expressie:

`^(?!.*13.*).*$`

Testen:

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

In dit resultaat `a:b:1313` geeft geen overeenkomst aan.

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
| `(a\b)` | a of b |
| `a?` | Nul of een van een |
| `a*` | Nul of meer van een |
| `a+` | Een of meer van een |
| `a{3}` | Precies 3 van a |
| `a{3,}` | 3 of meer van |
| `a{3,6}` | Tussen 3 en 6 van een |

Een goede bron voor het testen van de geldigheid van reguliere expressies is [https://rubular.com/](https://rubular.com/).

## Info over Prioriteit regel

Als een sleutel aan veelvoudige regels wordt aangepast en het de zelfde classificatiekolom plaatst die in [!UICONTROL Set Classification] kolom, wordt de laatste regel gebruikt. Als dusdanig, zou u het belangrijkste laatste in uw regelreeks kunnen willen rangschikken.

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

Als een gebruiker zoekt naar *`Cowboys fantasy Tony Romo`*, de term *`Player`* is geclassificeerd, omdat deze overeenkomt met de laatst opgegeven classificatie in de kolom Indeling instellen.

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

Voeg regels toe door een voorwaarde aan een classificatie aan te passen, en de actie te specificeren.

>[!NOTE]
>
>In deze procedure, moet u de regels op één of meerdere rapportsuites toepassen. Het aanbevolen aantal regels per regel ligt tussen 500 en 1000, hoewel er geen limieten zijn. Als u meer dan 100 regels hebt, kunt u de regel vereenvoudigen door [subclassificaties](/help/components/classifications/c-sub-classifications.md).

Een classificatieregel toevoegen of bewerken:

1. [Een set classificatieregel maken](/help/components/classifications/crb/classification-rule-set.md) .
1. Klik op de pagina met regelsets op **[!UICONTROL Add Rule]**.

   ![](assets/add_rule.png)

1. Volgende tot **[!UICONTROL Report Suites]**, klikt u op **[!UICONTROL Add Suites]** om één of meerdere rapportreeksen te specificeren om aan deze regelreeks toe te wijzen.

   De **[!UICONTROL Select Report Suites]** wordt weergegeven.

   >[!NOTE]
   >
   >De suites van het rapport tonen op deze pagina *alleen* wanneer aan de volgende voorwaarden is voldaan:
   >
   >* Voor de rapportsuite is ten minste één classificatie voor die variabele gedefinieerd in [!UICONTROL Admin Tools].
   >
   >   (Zie *Variabele* in [Classificatiereeksen](/help/components/classifications/crb/classification-rule-set.md) voor een toelichting op deze voorwaarde.)
   >
   >* U hebt de rapportsuite geselecteerd in het dialoogvenster **[!UICONTROL Available Report Suites]** pagina, die wordt weergegeven nadat u hebt geklikt [Regelset toevoegen](/help/components/classifications/crb/classification-rule-set.md) om de regelset te maken.

1. Geef op of bestaande waarden moeten worden overschreven:

   | **Regels overschrijven bestaande waarden** | (Standaardinstelling) Overschrijf altijd bestaande classificatietoetsen, inclusief classificaties die via de importer (SAINT) zijn geüpload. |
   |---|---|
   | **Regels overschrijven alleen ongestelde waarden** | Vul alleen lege (niet-ingestelde) cellen in. Bestaande classificaties worden niet gewijzigd. |

1. [De regel of regels definiëren](/help/components/classifications/crb/classification-rule-definitions.md#section_4A5BF384EEEE4994B6DC888339833529).

   ![Stap Resultaat](assets/classification_rules_page.png)

   Voor voorbeelden van bouwvoorschriften raadpleegt u [Classifications Rule Builder](/help/components/classifications/crb/classification-rule-builder.md) en [Regelmatige expressies in classificatieregels](/help/components/classifications/crb/classification-quickstart-rules.md).

   >[!NOTE]
   >
   >Als een sleutel overeenkomt met meerdere regels die dezelfde classificatie instellen (in de kolom Indeling instellen), wordt de laatste regel gebruikt die overeenkomt met de classificatie. Zie **Info over Prioriteit regel** voor meer informatie over sorteerregels.

1. [Uw regelset testen](/help/components/classifications/crb/classification-quickstart-rules.md).
1. Klik op **[!UICONTROL Active]** om de regel te valideren en te activeren.

   Als u een regel activeert, wordt het bestand automatisch samengesteld en voor u geüpload.

   Velddefinities: Zie [Classification Rule Builder](/help/components/classifications/crb/classification-rule-definitions.md) voor volledige definities van interfaceopties op deze pagina.

## Een set classificatieregel testen

<!-- 

t_classifications_test_rule.xml

 -->

U kunt een classificatieregel of een regelset testen. Als u een test uitvoert, worden alle regels in een set gecontroleerd.

Een set classificatieregel testen:

1. [Een set classificatieregel maken](/help/components/classifications/crb/classification-rule-set.md) .
1. Op de [!UICONTROL Classification Rule Builder]klikt u op de naam van de regelset.
1. Zorg ervoor dat de regelreeks met een rapportreeks wordt geassocieerd.
1. Klik in de regeleditor op **[!UICONTROL Test Rule Set]**.

   ![Stap Resultaat](assets/classification_test_rule_set.png)

1. Test-toetsen typen of plakken in het dialoogvenster [!UICONTROL Sample Keys] veld.

   Voorbeelden van voorbeeldtoetsen zijn:

   * Trackingcodes
   * Trefwoorden of woordgroepen zoeken

   Zie [Regelmatige expressies in classificatieregels](/help/components/classifications/crb/classification-quickstart-rules.md) voor informatie over het testen van reguliere expressies.
1. Klik op **[!UICONTROL Run Test]**.

   Regels die overeenkomen worden weergegeven in het dialoogvenster [!UICONTROL Results] tabel.
1. (Optioneel) Klik op **[!UICONTROL Activate]** om de regel te activeren en bestaande classificaties te overschrijven.

   Zie voor meer informatie over het gebruiken van regels om bestaande classificaties te beschrijven.

## Classificatieregels valideren en activeren

<!-- 

t_validate_rules.xml

 -->

Classificatieregels valideren en activeren:

1. [Een set classificatieregel maken](/help/components/classifications/crb/classification-rule-set.md) vervolgens [classificatieregels toevoegen](/help/components/classifications/crb/classification-quickstart-rules.md) naar de set.
1. Klik in de regeleditor op **[!UICONTROL Activate]**.

   ![](assets/overwrite_keys.png)

1. (Optioneel) Schakel **[!UICONTROL Overwrite classifications for]** &lt;*selectie*>.

   Met deze optie kunt u bestaande classificaties voor desbetreffende toetsen overschrijven.

   Zie [Regelpagina](/help/components/classifications/crb/classification-rule-definitions.md#section_4A5BF384EEEE4994B6DC888339833529) voor een definitie van deze optie.
