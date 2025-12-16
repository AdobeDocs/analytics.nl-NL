---
title: Regels voor classificatiesets
description: Leer hoe u classificatiesets gebruikt om regels voor classificatiegegevens te definiëren.
feature: Classifications
hide: true
hidefromtoc: true
source-git-commit: 0f80bb314c8e041a98af26734d56ab364c23a49b
workflow-type: tm+mt
source-wordcount: '1565'
ht-degree: 0%

---


# Classificatieregels

U gebruikt regels om automatische classificaties te steunen in scenario&#39;s waar uw belangrijkste dimensie constant verandert. Het bijwerken van classificaties door middel van uploaden of automatiseren wordt een omslachtig proces of vertraagt de juiste classificatie voor nieuwe dimensie-waarden. Bijvoorbeeld interne campagnes, volgcodes of product-SKU&#39;s. De dimensie moet waarden bevatten waarmee u een of meer regels kunt toepassen, zodat u classificatiegegevens kunt afleiden van de waarden.

U definieert regels binnen de context van een classificatieset. Deze context impliceert dat de regels worden toegepast (wanneer geactiveerd) op alle rapportreeks en zeer belangrijke afmetingscombinaties die aan de classificatiereeks worden geabonneerd. Deze implementatie wijkt enigszins af van de manier waarop de bouwer van de oude classificatieregel werkt. In de de regelbouwer van de Classificatie, bepaal één of meerdere regels als deel van een afzonderlijk vastgestelde regel en associeer dan de regel die met één of meerdere rapportreeksen wordt geplaatst. In de nieuwe interface, worden de regels binnen de classificatiereeks ook bedoeld als regelreeks. Nochtans, worden de regelreeksen bepaald binnen de zelfde interface waar u andere eigenschappen van classificatiesets vormt.


Een regelset definiëren voor een classificatieset:

1. Selecteer **[!UICONTROL Components]** in de bovenste menubalk van Adobe Analytics en selecteer vervolgens **[!UICONTROL Classification sets]** .
1. Selecteer in **[!UICONTROL Classification Sets]** de tab **[!UICONTROL Classification Sets]** .
1. Selecteer in **[!UICONTROL Classifications Sets]** Manager de classificatieset waarvoor u de regels wilt definiëren.
1. In de **[!UICONTROL Classification Set: _dialoog van de classificatiereeks naam_]**, selecteer het **[!UICONTROL Rules]** lusje.

   * Als u voor het eerst tot de **[!UICONTROL Rules]** interface voor een classificatiereeks toegang hebt, of tot dusverre beslist om de interface van de bouwer van erfenisregels te blijven gebruiken, wordt u voorgesteld van een dialoog die u toestaat om te selecteren hoe te begonnen worden.

     ![&#x200B; migratie van Regels &#x200B;](assets/rules-migration.png)

     De opties zijn:

      * **migreer bestaande regels**. Importeer uw huidige classificatieregels en blijf met deze regels werken in de nieuwe interface. Uw bestaande regels blijven behouden en worden geconverteerd naar de nieuwe indeling.
         * Selecteer **[!UICONTROL Migrate rules]** om door te gaan.
         * Lees in het dialoogvenster **[!UICONTROL Confirm migration]** de implicaties van de migratie.
            * Selecteer **[!UICONTROL Migrate rules]** om de migratie te bevestigen. Nadat de migratie wordt voltooid, gebruik de [&#x200B; Vastgestelde interface van de Regel &#x200B;](#rule-set-interface) om nieuwe regels tot stand te brengen en uw bestaande gemigreerde regels uit te geven.
            * Selecteer **[!UICONTROL Cancel]** om de migratie te annuleren

      * **Begin vers**. Creeer nieuwe classificatieregels van kras gebruikend de nieuwe regelbouwer. Selecteer deze optie als u de classificatielogica opnieuw wilt ontwerpen of vers wilt beginnen met nieuwe classificatieregels.
         * Selecteer **[!UICONTROL Create new rules]** om door te gaan.
         * Lees in het dialoogvenster **[!UICONTROL Confirm start fresh]** de implicaties van een nieuwe start.
            * Selecteer **[!UICONTROL Start fresh]** om een nieuwe start te bevestigen en bestaande regels te negeren. Gebruik de [&#x200B; Vastgestelde interface van de Regel &#x200B;](#rule-set-interface) om nieuwe regels tot stand te brengen.
            * Selecteer **[!UICONTROL Cancel]** om te annuleren.


      * **de erfenisinterface van het Gebruik**. Ga door met het gebruik van de vorige regelbuilderinterface. U kunt op elk gewenst moment naar de nieuwe ervaring migreren als u klaar bent.
         * Selecteer **[!UICONTROL Go to legacy interface]** om door te gaan. U wordt naar de oudere **[!UICONTROL Classification Rule Builder]** -interface geleid.

   * Als u reeds gemigreerde regels hebt of nieuwe regels voor een classificatieset gecreeerd, komt u rechtstreeks in de Vastgestelde interface van de Regel.



## Interface voor regelsets {#rule-set-interface}

>[!CONTEXTUALHELP]
>id="classificationsets_rules_samplekeys"
>title="Voorbeeldtoetsen"
>abstract="Typ of plak testtoetsen om de linialen te testen. Elke regel is een aparte sleutelwaarde. Selecteer **[!UICONTROL Test Ruleset]** om een dialoogvenster met de resultaten weer te geven."


Om regels tot stand te brengen of uit te geven, gebruik de Vastgestelde interface van de Regel.

![&#x200B; de vastgestelde interface van de Regel &#x200B;](assets/rulesets-ui.png)

| | Naam | Beschrijving |
|---|---|---|
| 1 | **[!UICONTROL Functions]** | U gebruikt het **[!UICONTROL Functions]** gebied om uw functies te selecteren en te slepen en neer te zetten aan de bouwer van de regelreeks. |
| 2 | **de vastgestelde bouwer van de Regel** | U bouwt uw regelreeks gebruikend één of meerdere regels. Een regel is de implementatie van een functie en wordt altijd gekoppeld aan slechts één functie. Een functie kan meerdere operatoren hebben. U maakt een regel door een functie naar de constructor voor regelsets te slepen. Het type function definieert de interface van de regel. <br/> zie de [&#x200B; interface van de Regel &#x200B;](#rule-interface) voor meer informatie.<br/> u kunt functies op om het even welke plaats opnemen, en de functies worden uitgevoerd in opeenvolging om de definitieve waarden voor de classificaties te bepalen.<br/> Gebruik **[!UICONTROL Collapse all]** om alle regels samen te vouwen en gebruik **[!UICONTROL Expand all]** om alle regels uit te vouwen. |
| 3 | **[!UICONTROL Status]** | De status en de datum van laatste wijziging van de regelset weergeven. <br/> Uitgezocht **[!UICONTROL Activate]** om de regelreeks te activeren. <br/> Uitgezocht **[!UICONTROL Deactivate]** om de regelreeks te deactiveren. |
| 4 | **[!UICONTROL Lookback]** | Geef het terugzoekvenster voor de regelset op.<br/> selecteer een optie (van 1 maand tot 6 maanden) van het drop-down menu.<br/> Uitgezocht **[!UICONTROL Perform lookback]** om een raadpleging uit te voeren gebruikend de geselecteerde raadplegingsperiode. |
| 5 | **[!UICONTROL Test options]** | Gebruik waarden voor de monstersleutel om de classificaties te testen: <ul><li>Voeg waarden toe of plak waarden in het tekstgebied **[!UICONTROL Sample keys]** .<br/> Controle **[!UICONTROL Remember sample keys]** om ervoor te zorgen dat de steekproefsleutels over verschillend gebruik van de regelvastgestelde interface blijven.</li><li>Selecteer **[!UICONTROL Test rule set]** om uw regelset te testen.</li></ul> |


## Regelinterface

U bepaalt elke individuele regel binnen de regel die in de interface van de Regel wordt geplaatst. De interface bestaat uit de volgende elementen:

![&#x200B; interface van de Regel &#x200B;](assets/rule-ui.png)

| | Beschrijving |
|---|---|
| 1 | De naam van de geselecteerde functie en de invoer die voor de functie is ingevoerd. |
| 2 | De invoer voor de geselecteerde functie. De invoer is afhankelijk van de geselecteerde functie. Voor de functie **[!UICONTROL Regular expression]** is de invoer bijvoorbeeld een reguliere expressie. Voor de functie **[!UICONTROL Split]** is de invoer een token. Voer de juiste invoer voor de specifieke functie in. `^(.+)\:(.+)\:(.+)$` bijvoorbeeld voor een reguliere expressie die drie classificaties in een interne campagnecode identificeert. |
| 3 | Elke bewerking stelt een specifieke classificatie in op een waarde. <br/> selecteer een classificatie van **[!UICONTROL Set Classification]** drop-down menu en ga een waarde voor **[!UICONTROL to]** in. <br/> Gebruik ![&#x200B; CrossSize400 &#x200B;](/help/assets/icons/CrossSize400.svg) om een verrichting van de lijst te schrappen. |
| 4 | Selecteer ![&#x200B; toevoegen &#x200B;](/help/assets/icons/Add.svg) **[!UICONTROL Add operation]** om een extra verrichting aan de functie toe te voegen. |
| 5 | Selecteer ![&#x200B; ChevronDown &#x200B;](/help/assets/icons2/ChevronDown.svg) om de regel samen te vouwen. Selecteer ![&#x200B; ChevronLeft &#x200B;](/help/assets/icons/ChevronLeft.svg) om de regel uit te breiden.<br/> Uitgezochte ![&#x200B; CrossSize400 &#x200B;](/help/assets/icons/CrossSize400.svg) om de regel te schrappen. |

## Functieverwijzing

Voor elke ondersteunde functie vindt u hieronder meer informatie over de vereiste invoer- en voorbeeldgebruiksgevallen.


### Begint met...

Stelt een classificatie in op basis van een specifieke waarde waarmee de sleuteldimensie begint.

+++ Details 

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Starts With]** . Bijvoorbeeld: `em` .

#### Hoofdletters gebruiken

U wilt een regel definiëren die `Email` toewijst als de waarde voor de **[!UICONTROL Channel]** -classificatie wanneer de waarde voor de belangrijke dimensie Interne campagne begint met `em` (bijvoorbeeld: `em:FY2025:Summer Sale`).

>[!BEGINTABS]

>[!TAB  Regel ]

![&#x200B; regel - begint met &#x200B;](assets/rule-startswith.png)

>[!TAB  de resultaten van de Test ]

![&#x200B; Regel - begint met de Resultaten van de Test &#x200B;](assets/rule-startswith-test.png)

>[!ENDTABS]

+++



### Eindigt met...

Stelt een classificatie in op basis van een specifieke waarde waarmee de sleuteldimensie eindigt.

+++ Details 

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Ends With]** . Bijvoorbeeld: `2025` .

#### Hoofdletters gebruiken

U wilt een regel definiëren die `2025` als de waarde aan de **[!UICONTROL Year]** -classificatie toewijst wanneer de waarde voor de belangrijkste dimensie in de interne campagne `2025` bevat (bijvoorbeeld: `em:Summer Sale:FY2025`).

>[!BEGINTABS]

>[!TAB  Regel ]

![&#x200B; regel - beëindigt met &#x200B;](assets/rule-endswith.png)

>[!TAB  de resultaten van de Test ]

![&#x200B; regel - eindigt met de Resultaten van de Test &#x200B;](assets/rule-endswith-test.png)

>[!ENDTABS]

+++


### Bevat...

Stelt een classificatie in op basis van een specifieke waarde die de sleuteldimensie bevat.

+++ Details 

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Contains]** . Bijvoorbeeld: `Winter` .

#### Hoofdletters gebruiken

U wilt een regel definiëren om `Winter Sale` als een waarde toe te wijzen aan de **[!UICONTROL Type]** -classificatie wanneer de waarde voor de belangrijkste dimensie in de interne campagne met `Winter` bevat (bijvoorbeeld: `fb:Winter:FY2024`).


>[!BEGINTABS]

>[!TAB  Regel ]

![&#x200B; Regel - bevat &#x200B;](assets/rule-contains.png)

>[!TAB  de resultaten van de Test ]

![&#x200B; Regel - bevat Resultaten &#x200B;](assets/rule-contains-test.png)

>[!ENDTABS]

+++


### Overeenkomsten

Stelt een classificatie in op basis van een specifieke waarde die overeenkomt met de waarde van de belangrijkste dimensie.

+++ Details 

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Matches]** . Bijvoorbeeld: `em:Summer:2025` .

#### Hoofdletters gebruiken

U wilt een regel definiëren om `Email` als een waarde toe te wijzen aan de **[!UICONTROL Channel]** classificatie `Summer Sale` als een waarde aan de **[!UICONTROL Type]** classificatie en `2025` aan de **[!UICONTROL Year]** classificatie. Maar alleen wanneer de waarde voor de belangrijkste dimensie Interne campagne overeenkomt met `em:Summer:2025` .


>[!BEGINTABS]

>[!TAB  Regel ]

![&#x200B; Regel - Gelijken &#x200B;](assets/rule-matches.png)

>[!TAB  de resultaten van de Test ]

![&#x200B; Regel - Gelijken &#x200B;](assets/rule-matches-test.png)

>[!ENDTABS]

+++


### Gewone uitdrukking

Stelt een of meer classificaties in op basis van een reguliere expressie die wordt toegepast op de waarde van de hoofddimensie.

+++ Details 

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Regular Expression]** . Bijvoorbeeld: `^(.+)\:(.+)\:FY(.+)$` .

#### Hoofdletters gebruiken

U wilt een regel definiëren om waarden toe te wijzen aan de classificaties **[!UICONTROL Channel]** , **[!UICONTROL Type]** en **[!UICONTROL Year]** door de reguliere expressie `^(.+)\:(.+)\:FY(.+)$` toe te passen en match groups ( `$1` , `$2` en `$3` ) te gebruiken op de waarden voor de belangrijkste dimensie Interne campagne.

>[!BEGINTABS]

>[!TAB  Regel ]

![&#x200B; Regel - Regelmatige uitdrukking &#x200B;](assets/rule-regex.png)

>[!TAB  de resultaten van de Test ]

![&#x200B; Regel - de Regelmatige resultaten van de uitdrukkingstest &#x200B;](assets/rule-regex-test.png)

>[!ENDTABS]

+++


### Splitsen

Splitst de waarde van de belangrijkste dimensie, die op een teken wordt gebaseerd, op één of meerdere classificaties.

+++ Details

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Split]** . Bijvoorbeeld: `:` .

#### Hoofdletters gebruiken

U wilt een regel definiëren die de waarden voor de belangrijkste dimensie van de interne campagne splitst in de classificaties **[!UICONTROL Channel]** , **[!UICONTROL Type]** en **[!UICONTROL Year]** op basis van `:` **[!UICONTROL Token]** .

>[!BEGINTABS]

>[!TAB  Regel ]

![&#x200B; Regel - Gesplitst &#x200B;](assets/rule-split.png)

>[!TAB  de resultaten van de Test ]

![&#x200B; Regel - de resultaten van de Test van de Splitsing &#x200B;](assets/rule-split-test.png)

>[!ENDTABS]

+++


#### Referentietabel {#section_0211DCB1760042099CCD3ED7A665D716}

| Gewone uitdrukking | Beschrijving |
|---|---|
| `(?ms)` | De volledige reguliere expressie afstemmen op een invoer met meerdere regels, zodat de joker `.` overeenkomt met alle nieuwe-regeltekens |
| `(?i)` | De volledige reguliere expressie aanpassen zodat deze niet hoofdlettergevoelig is |
| `[abc]` | Eén teken van: a, b of c |
| `[^abc]` | Elk enkel teken behalve: a, b of c |
| `[a-z]` | Eén teken in het bereik a-z |
| `[a-zA-Z]` | Eén teken in het bereik a-z of A-Z |
| `^` | Begin van regel (komt overeen met het begin van de regel) |
| `$` | Komt overeen met het einde van de regel (of vóór de nieuwe regel aan het einde) |
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



## Prioriteit regel

De laatste regel bepaalt de waarde voor de classificatie als:

* Een waarde van de belangrijkste dimensie wordt aangepast aan veelvoudige regels.
* De regelset bevat regels met dezelfde **[!UICONTROL Set Classification]** -bewerking.

U moet dus de belangrijkste bewerking **[!UICONTROL Set Classification]** plaatsen als onderdeel van de laatste regel in de regelset.

Als u meerdere regels maakt die niet dezelfde **[!UICONTROL Set Classification]** -bewerking delen, is de verwerkingsvolgorde niet van belang.


### Voorbeeld

U wilt met de classificatie **[!UICONTROL Type]** classificeren hoe de gebruikers naar een team, een generiek type, of een speler zoeken gebruikend het onderzoekskoord als belangrijkste afmeting. Bijvoorbeeld door het gebruik van deze regelreeks:

+++ Details


>[!BEGINTABS]

>[!TAB  Regel ]

![&#x200B; Regel - Prioriteit &#x200B;](assets/rule-priority.png)

>[!TAB  de resultaten van de Test ]

![&#x200B; Regel - de Prioritaire resultaten van de Test &#x200B;](assets/rule-priority-test.png)

>[!ENDTABS]

+++ 

