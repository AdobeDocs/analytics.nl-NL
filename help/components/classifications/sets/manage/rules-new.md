---
title: Regels voor classificatiesets
description: Leer hoe u classificatiesets gebruikt om regels voor classificatiegegevens te definiëren.
feature: Classifications
hide: true
hidefromtoc: true
source-git-commit: bccb3409875336a092ab641ad69b866b43621984
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---


# Classificatieregels

U gebruikt regels om automatische classificaties te steunen in scenario&#39;s waar uw belangrijkste dimensie constant verandert. Het bijwerken van classificaties door middel van uploaden of automatiseren wordt een omslachtig proces of vertraagt de juiste classificatie voor nieuwe dimensie-waarden. Bijvoorbeeld interne campagnes, volgcodes of product-SKU&#39;s. De dimensie moet waarden bevatten waarmee u een of meer regels kunt toepassen, zodat u classificatiegegevens kunt afleiden van de waarden.

U bepaalt regels binnen de context van een classificatieset, wat impliceert dat de regels (wanneer geactiveerd) op alle rapportreeks en zeer belangrijke afmetingscombinaties worden toegepast die aan de classificatiereeks worden geabonneerd. Deze implementatie wijkt enigszins af van de manier waarop de bouwer van de oude classificatieregel werkt. In de classificatieregel definieert u een of meer regels als onderdeel van een afzonderlijk ingestelde regel en koppelt u de regel die is ingesteld aan een of meer rapportsuites. In de nieuwe interface, worden de regels binnen de classificatieset ook bedoeld als regelreeks maar binnen de zelfde interface bepaald waar u andere eigenschappen van classificatiesets vormt.


Een regelset definiëren voor een classificatieset:

1. Selecteer **[!UICONTROL Components]** in de bovenste menubalk van Adobe Analytics en selecteer vervolgens **[!UICONTROL Classification sets]** .
1. Selecteer in **[!UICONTROL Classification Sets]** de tab **[!UICONTROL Classification Sets]** .
1. Selecteer in **[!UICONTROL Classifications Sets]** Manager de classificatieset waarvoor u de regels wilt definiëren.
1. In de **[!UICONTROL Classification Set: _dialoog van de classificatiereeks naam_]**, selecteer het **[!UICONTROL Rules]** lusje.

   * Als u de interface van **[!UICONTROL Rules]** voor het eerst voor een classificatiereeks toegang hebt, of u tot nu toe hebt besloten om de interface van de bouwer van erfenisregels te blijven gebruiken, wordt u voorgesteld van een dialoog die u toestaat om te selecteren hoe te beginnen. De opties zijn:

      * **migreer bestaande regels**. Importeer uw huidige classificatieregels en blijf met deze regels werken in de nieuwe interface. De bestaande regels blijven behouden en worden omgezet in de nieuwe indeling.
         * Selecteer **[!UICONTROL Migrate rules]** om door te gaan.
         * Lees in het dialoogvenster **[!UICONTROL Confirm migration]** de implicaties van de migratie.
            * Selecteer **[!UICONTROL Migrate rules]** om de migratie te bevestigen. Nadat de migratie wordt voltooid, gebruik de [ Vastgestelde interface van de Regel ](#rule-set-interface) om nieuwe regels tot stand te brengen en uw bestaande gemigreerde regels uit te geven.
            * Selecteer **[!UICONTROL Cancel]** om de migratie te annuleren

      * **Begin vers**. Creeer nieuwe classificatieregels van kras gebruikend de nieuwe regelbouwer. Selecteer deze optie als u de classificatielogica opnieuw wilt ontwerpen of vers wilt beginnen met nieuwe classificatieregels.
         * Selecteer **[!UICONTROL Create new rules]** om door te gaan.
         * Lees in het dialoogvenster **[!UICONTROL Confirm start fresh]** de implicaties van een nieuwe start.
            * Selecteer **[!UICONTROL Start fresh]** om een nieuw begin te bevestigen en om het even welke bestaande regels te verwerpen. Gebruik de [ Vastgestelde interface van de Regel ](#rule-set-interface) om nieuwe regels tot stand te brengen.
            * Selecteer **[!UICONTROL Cancel]** om te annuleren.


      * **de erfenisinterface van het Gebruik**. Ga door met het gebruik van de vorige regelbuilderinterface. U kunt op elk gewenst moment naar de nieuwe ervaring migreren als u klaar bent.
         * Selecteer **[!UICONTROL Go to legacy interface]** om door te gaan. U wordt naar de oudere **[!UICONTROL Classification Rule Builder]** -interface geleid.

   * Als u reeds gemigreerde regels hebt of nieuwe regels voor een classificatieset gecreeerd, komt u rechtstreeks in de Vastgestelde interface van de Regel.



## Interface voor regelsets

Wanneer u regels maakt of bewerkt, gebruikt u de regelsetinterface.

![ de vastgestelde interface van de Regel ](assets/rulesets-ui.png)

| | Naam | Beschrijving |
|---|---|---|
| 1 | **[!UICONTROL Functions]** | U gebruikt het **[!UICONTROL Functions]** gebied om uw functies te selecteren en te slepen en neer te zetten aan de bouwer van de regelreeks. |
| 2 | **de vastgestelde bouwer van de Regel** | U bouwt uw regelreeks gebruikend één of meerdere regels. Een regel is de implementatie van een functie en wordt altijd gekoppeld aan slechts één functie. Een functie kan meerdere operatoren hebben. U maakt een regel door een functie naar de constructor voor regelsets te slepen. Het type function definieert de interface van de regel. <br/> zie de [ interface van de Regel ](#rule-interface) voor meer informatie.<br/> u kunt functies op om het even welke plaats opnemen, en de functies worden uitgevoerd in opeenvolging om de definitieve waarden voor de classificaties te bepalen.<br/> Gebruik **[!UICONTROL Collapse all]** om alle regels samen te vouwen en gebruik **[!UICONTROL Expand all]** om alle regels uit te vouwen. |
| 3 | **[!UICONTROL Status]** | De status en de datum van laatste wijziging van de regelset weergeven. <br/> Uitgezocht **[!UICONTROL Activate]** om de regelreeks te activeren. <br/> Uitgezocht **[!UICONTROL Deactivate]** om de regelreeks te deactiveren. |
| 4 | **[!UICONTROL Lookback]** | Geef het terugzoekvenster voor de regelset op.<br/> selecteer een optie (van 1 maand tot 6 maanden) van het drop-down menu.<br/> Uitgezocht **[!UICONTROL Perform lookback]** om een raadpleging uit te voeren gebruikend de geselecteerde raadplegingsperiode. |
| 5 | **[!UICONTROL Test options]** | Gebruik waarden voor de monstersleutel om de classificaties te testen: <ul><li>Voeg waarden toe of plak waarden in het tekstgebied **[!UICONTROL Sample keys]** .<br/> Controle **[!UICONTROL Remember sample keys]** om steekproefsleutels te verzekeren blijft over verschillend gebruik van de regelvastgestelde interface.</li><li>Selecteer **[!UICONTROL Test rule set]** om uw regelset te testen.</li></ul> |


## Regelinterface

U bepaalt elke individuele regel binnen de regel die in de interface van de Regel wordt geplaatst. De interface bestaat uit de volgende elementen:

![ interface van de Regel ](assets/rule-ui.png)

| | Beschrijving |
|---|---|
| 1 | De naam van de geselecteerde functie en de invoer die voor de functie is ingevoerd. |
| 2 | De invoer voor de geselecteerde functie. De invoer is afhankelijk van de geselecteerde functie. Voor de functie Reguliere expressie is de invoer bijvoorbeeld een reguliere expressie en voor de functie Splitsen is de invoer een token. Voer de juiste invoer voor de specifieke functie in. `^(.+)\:(.+)\:(.+)$` bijvoorbeeld voor een reguliere expressie die drie classificaties in een interne campagnecode identificeert. |
| 3 | Elke bewerking stelt een specifieke classificatie in op een waarde. <br/> selecteer een classificatie van **[!UICONTROL Set Classification]** drop-down menu en ga een waarde voor **[!UICONTROL to]** in. <br/> Gebruik ![ CrossSize400 ](/help/assets/icons/CrossSize400.svg) om een verrichting van de lijst te schrappen. |
| 4 | Selecteer ![ toevoegen ](/help/assets/icons/Add.svg) **[!UICONTROL Add operation]** om een extra verrichting aan de functie toe te voegen. |
| 5 | Selecteer ![ ChevronDown ](/help/assets/icons2/ChevronDown.svg) om de regel samen te vouwen. Selecteer ![ ChevronLeft ](/help/assets/icons/ChevronLeft.svg) om de regel uit te breiden.<br/> Uitgezochte ![ CrossSize400 ](/help/assets/icons/CrossSize400.svg) om de regel te schrappen. |

## Functieverwijzing

Voor elke ondersteunde functie vindt u hieronder meer informatie over de vereiste invoer- en voorbeeldgebruiksgevallen.


### Begint met...

Stelt een classificatie in op basis van een specifieke waarde waarmee de sleuteldimensie begint.

+++ Details 

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Starts With]** . Bijvoorbeeld: `em` .

#### Hoofdletters gebruiken

U wilt een regel definiëren die automatisch `Email` als een waarde aan de **[!UICONTROL Channel]** -classificatie toewijst wanneer de waarde voor de belangrijkste dimensie van de interne campagne met `em` begint (bijvoorbeeld: `em:FY2025:Summer Sale`).

![ regel - begint met ](assets/rule-startswith.png)

+++



### Eindigt met...

Stelt een classificatie in op basis van een specifieke waarde waarmee de belangrijkste dimensie eindigt.

+++ Details 

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Ends With]** . Bijvoorbeeld: `Sale` .

#### Hoofdletters gebruiken

U wilt een regel definiëren die automatisch `Sale` als een waarde aan de **[!UICONTROL Type]** -classificatie toewijst wanneer de waarde voor de belangrijkste dimensie in de interne campagne `Sale` bevat (bijvoorbeeld: `em:FY2025:Summer Sale`)..

![ regel - beëindigt met ](assets/rule-endswith.png)

+++


### Bevat...

Stelt een classificatie in op basis van een specifieke waarde die de sleuteldimensie bevat.

+++ Details 

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Contains]** . Bijvoorbeeld: `2025` .

#### Hoofdletters gebruiken

U wilt een regel definiëren die automatisch `2025` als een waarde aan de **[!UICONTROL Year]** -classificatie toewijst wanneer de waarde voor de belangrijkste dimensie van de interne campagne eindigt met `2025` (bijvoorbeeld: `em:FY2025:Summer Sale`).

![ Regel - bevat ](assets/rule-contains.png)

+++


### Overeenkomst

Stelt een classificatie in op basis van een specifieke waarde die overeenkomt met de belangrijkste dimensie.

+++ Details 

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Match]** . Bijvoorbeeld: `em:FY2025:Summer` .

#### Hoofdletters gebruiken

U wilt een regel definiëren waarmee `2025 Summer Email` automatisch als een waarde wordt toegewezen aan de **[!UICONTROL Type]** -classificatie wanneer de waarde voor de interne campagne voor de belangrijkste dimensie overeenkomt met `em:FY2025:Summer` .

![ Regel - Gelijken ](assets/rule-match.png)

+++


### Gewone uitdrukking

Stelt een of meer classificaties in op basis van een reguliere expressie die wordt toegepast op de waarde van de hoofddimensie.

+++ Details 

#### Vereiste invoer

Voer een waarde in voor **[!UICONTROL Regular Expression]** . Bijvoorbeeld: `^(.+)\:(.+)\:(.+)$` .

#### Hoofdletters gebruiken

U wilt een regel definiëren om automatisch waarden toe te wijzen aan de classificaties **[!UICONTROL Channel]** , **[!UICONTROL Type]** en **[!UICONTROL Year]** door de reguliere expressie `^(.+)\:(.+)\:(.+)$` toe te passen en match groups ( `$1` , `$2` en `$3` ) te gebruiken op de waarden voor belangrijke dimensie Interne campagne.

![ Regel - Regelmatige uitdrukking ](assets/rule-regex.png)


#### Referentietabel {#section_0211DCB1760042099CCD3ED7A665D716}

| Gewone uitdrukking | Beschrijving |
|---|---|
| `(?ms)` | Hiermee zorgt u dat de volledige reguliere expressie overeenkomt met een invoer van meerdere regels, zodat de eigenschap . jokerteken voor nieuwe-regeltekens |
| `(?i)` | Maakt het gehele reguliere-expressiefase ongevoelig |
| `[abc]` | Eén teken van: a, b of c |
| `[^abc]` | Elk enkel teken behalve: a, b of c |
| `[a-z]` | Eén teken in het bereik a-z |
| `[a-zA-Z]` | Eén teken in het bereik a-z of A-Z |
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

+++


## Prioriteit regel

Als een waarde van de belangrijkste dimensie aan veelvoudige regels wordt aangepast, en de regelreeksen regels met de zelfde Vastgestelde verrichting van de Indeling bevat, bepaalt de laatste regel de waarde voor de classificatie. Dus, zou u de belangrijkste Vastgestelde verrichting van de Classificatie als deel van de laatste regel in uw regelreeks moeten rangschikken.

Als u veelvoudige regels creeert die niet de zelfde Vastgestelde verrichting van de Indeling delen, is de verwerkingsorde niet van belang.


### Voorbeeld

U wilt met de classificatie **[!UICONTROL Type]** classificeren hoe gebruikers naar een atleet zoeken door de zoekreeks als sleuteldimensie te gebruiken. Als u bijvoorbeeld deze regelset gebruikt:

![ Prioriteit van Regels ](assets/rule-priority.png)

* Wanneer een gebruiker naar `Cowboys Fantasy Tony Romo` zoekt, wordt `Romo` geclassificeerd als **[!UICONTROL Type]** .
* Wanneer een gebruiker naar `Cowboys Fantasy Tony Romeo` zoekt, wordt `Fantasy` geclassificeerd als **[!UICONTROL Type]**.
* Wanneer een gebruiker naar `Cowboys vs. Broncos` zoekt, wordt `Team` geclassificeerd als **[!UICONTROL Type]**.

