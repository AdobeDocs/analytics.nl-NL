---
description: Manieren om Report Builder-resultaten te optimaliseren en een lijst met foutberichten die af en toe kunnen optreden.
title: Problemen oplossen en best practices voor Report Builder
uuid: 36a08143-dc78-40f5-9ce9-7d16980aa27b
feature: Report Builder
role: User, Admin
exl-id: 41a640ce-2316-439b-b3ba-f0bace9af268
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '1378'
ht-degree: 80%

---

# Problemen oplossen en best practices voor Report Builder

Manieren om Report Builder-resultaten te optimaliseren en een lijst met foutberichten die af en toe kunnen optreden.

## Report Builder 5.0-gebruikers en 5.1-werkmappen openen {#section_C29898775999453FABB5FB0E098415C8}

Adobe heeft het scheidingsteken tussen dimensies en classificaties gewijzigd van een onderstrepingsteken (_) in ||. Deze wijziging heeft compatibiliteitsimplicaties voor een gebruiker van Report Builder 5.0 die een werkmap van Report Builder v5.1 met classificatieaanvragen opent. Telkens wanneer een werkmap van een oudere versie dan v5.1 wordt geopend, worden alle geserialiseerde classificatieaanvragen geconverteerd naar deze indeling.

Hierdoor ontstaat een probleem met voorwaartse compatibiliteit: als een werkmap na conversie naar v5.1 wordt gedeeld met een gebruiker van Report Builder v5.0, kan deze gebruiker de classificatieaanvraag niet herkennen (er wordt gezocht naar “_”, maar v5.1 heeft “||” geserialiseerd).

Bij het openen van een ARB v5.1-werkmap met classificatieaanvraag ervaart u het volgende neveneffect:

* Bij het openen van de werkmap krijgt u de volgende waarschuwing: “Deze werkmap is het laatst opgeslagen met Report Builder v5.1. Deze versie heeft bepaalde eigenschappen geïntroduceerd die incompatibel zijn met de Report Builder-versie die op deze computer is geïnstalleerd. U wordt dringend geadviseerd een upgrade naar de recentste versie van Report Builder uit te voeren voordat u deze werkmap bijwerkt.”
* Als met de rechtermuisknop klikt op een ARB-aanvraag met classificatie, worden de contextmenu’s van Report Builder (aanvraag bewerken, afhankelijke aanvraag toevoegen...) niet worden weergegeven.
* Als u Alle vernieuwen uitvoert door op de derde knop te klikken, of door een reeks aanvragen vanuit het formulier van Aanvraagbeheer te vernieuwen, wordt de classificatieaanvraag zonder fouten uitgevoerd. De classificatiewaarden worden echter niet uitgeschreven.
* U kunt de aanvraag nog steeds bewerken door Aanvraagbeheer te openen en vervolgens de rijen te doorlopen totdat u bij de betreffende aanvraag komt.
* Als u de aanvraag bewerkt, alle parameters ongewijzigd laat en vervolgens op Voltooien klikt, wordt de reactie op de juiste wijze uitgeschreven. Het bewerken van de aanvraag lost het probleem op aangezien de parameters voor de reactielay-out opnieuw worden geserialiseerd. Er is dus een tijdelijke oplossing, hoewel dit tijdrovend is.

## Verificatiekwesties in Report Builder {#section_FD79104DF1414FE2B36591606C963DE6}

In Report Builder is verificatie vereist om data-aanvragen te maken op basis van uw rapportsuites. Soms zijn er problemen met de aanmelding bij Report Builder, afhankelijk van uw instellingen binnen [!DNL Analytics] of uw netwerk.

* **Ongeldig aanmeldingsbedrijf**: Deze fout treedt het vaakst op wanneer het aanmeldingsbedrijf onjuist is ingevoerd, of wanneer er problemen zijn met de netwerkactiviteit. Ga als volgt te werk:
   * Controleer de spelling van het aanmeldingsbedrijf om te controleren of er geen typefout of verkeerde spatie in staat.
   * Meld u bij Analytics aan via hetzelfde aanmeldingsbedrijf om te controleren of de data juist zijn. Als u zich niet met deze aanmeldingsgegevens kunt aanmelden, informeer dan bij een van de beheerders van uw organisatie naar het juiste aanmeldingsbedrijf.
* **Firewall**: Report Builder gebruikt poort 80 en 443. Zorg ervoor dat deze poorten zijn toegestaan door de firewall van uw organisatie. Zie ook de interne IP-adressen van Adobe voor meer firewalluitsluitingen.

## Aanbevelingen voor het optimaliseren van aanvragen {#section_33EF919255BF46CD97105D8ACB43573F}

De volgende factoren kunnen de complexiteit van aanvragen verhogen en tot een langzamere verwerking leiden.

* **Factoren die leveringen kunnen vertragen**: Er waren te veel bladwijzers, dashboards en Report Builder-werkboeken gepland binnen een paar uur. Overweeg ook te veel werkboeken van Report Builder die rond de zelfde tijd werden gepland. Wanneer dit gebeurt, gaat de rapport-API-wachtrij achterlopen.
* **Factoren die de werkmapruntime kunnen vertragen**: Aanzienlijke toename van classificaties of het vergroten van de datumbereik van de aanvraag in de loop van de tijd.
* **Veroorzaakt dat in de mislukking van de werkboeklevering resulteert**: De complexe formules van Excel in een werkboek, in het bijzonder degenen die datum en tijd impliceren.
* **Cellen die 0s (geen waarden) terugkeren**: Een apostrof of één enkel citaat in de het bladnaam van Excel zal rapportaannemer veroorzaken om geen waarden terug te keren. (Dit is een beperking van Microsoft Excel.)
* **Prestaties van afzonderlijke aanvragen**: De verwerkingssnelheid kan worden beïnvloed door de volgende instellingen:

   | Instelling | Snellere prestaties | Tragere prestaties |
   |--- |--- |--- |
   | Uitsplitsingen en uitsplitsingsvolgorde | Weinig | Veel |
   |  | Voorbeeld: Als u A uitsplitst op Z, moet het aantal items voor A altijd kleiner zijn dan het aantal items voor Z. Als dit andersom is, kan de aanvraagtijd aanzienlijk toenemen. |
   | Datumbereik | Klein bereik | Breed bereik |
   | Filteren | Specifieke filtering | Populairste filtering |
   | Granulariteit | Samengevoegd | Uurlijks<ul><li>Dagelijks</li><li>Wekelijks</li><li>Maandelijks</li><li>Driemaandelijks</li><li>Jaarlijks</li></ul> |
   | Aantal vermeldingen | Kleine dataset | Grote dataset |

* **Planningstijd**: Verdeel de planning over een periode van 24 uur (zie onderstaande tabel). Als bestaande bladwijzers, dashboards, en Report Builder-werkmappen vlak na elkaar worden gepland, kan dat vertragingen veroorzaken. Plan grotere, complexere aanvragen in de vroege ochtend, zodat handmatige pulls en vernieuwing mogelijk is in de loop van de werkdag.

   | Planningstijd | 01:00 - 2:00 uur | 02:00 - 07:00 uur | 07:00 - 18:00 | 18:00 - Middernacht |
   |--- |--- |--- |--- |--- |
   | Gebruik van Report Builder | Rustig | Heel druk | Clientgebruik.<br>Hogere aantallen gebruikers die lokaal vernieuwen en vragen om “direct verzenden”.<br>Controleer bovendien of de API-wachtrij wordt gewist wanneer bij geplande werkmappen een time-out optreedt. | Niet bezet |

* **Time-outs**: Bij alle geplande rapportagetijden treedt na vier uur een time-out op. Het systeem probeert nog drie keer te plannen, wat mogelijk resulteert in een fout. (Het uitvoeren van de dataset duurt gewoonlijk langer naarmate deze groter is.) Deze zijn te zien in [!DNL Analytics]-rapportage en Report Builder:

## Beschrijvingen van foutberichten {#section_3DF3A1EEDAD149CB941BEABEF948A4A5}

Een lijst met foutberichten die soms kunnen optreden wanneer u Report Builder gebruikt.

>[!NOTE]
>
>Dit is slechts een selectie van foutberichten, geen volledige lijst. Neem contact op met de beheerder voor meer informatie over het oplossen van fouten.

* **Deze eigenschap kan alleen op een geopende werkmap worden toegepast.**: Als er geen werkmappen (spreadsheetdocumenten) in Excel zijn geopend, en u op een van de pictogrammen in de Report Builder-werkbalk klikt, wordt dit bericht weergegeven. Daarnaast wordt de werkbalk uitgeschakeld totdat u een spreadsheet opent. U kunt echter op het online Help-pictogram klikken terwijl de werkbalk nog is ingeschakeld zonder dat deze fout optreedt.
* **U moet eerst de [!UICONTROL Request Wizard] afsluiten voordat u [!UICONTROL Request Manager] activeert.**: Terwijl de [!UICONTROL Request Manager] en de [!UICONTROL Request Wizard] zijn functioneel gekoppeld, is het niet mogelijk om met de [!UICONTROL Request Manager] voordat de in de [!UICONTROL Request Wizard].
* **Er is geen aanvraag aan dit bereik gekoppeld.**: Dit foutbericht treedt op als u op de knop [!UICONTROL From Sheet] in [!UICONTROL Request Manager] klikt wanneer een cel van de spreadsheet geen aanvragen bevat. Als u wilt identificeren welke cellen in de spreadsheet aanvragen bevatten, klikt u op individuele aanvragen die worden vermeld in de tabel in [!UICONTROL Request Manager]. Als een aanvraag is gekoppeld aan cellen, worden de cellen gemarkeerd getoond wanneer de aanvraag in de tabel wordt geselecteerd.
* **Het geselecteerde bereik is ongeldig. Selecteer een ander bereik.**: Als een cel in de spreadsheet wordt geselecteerd terwijl er al een aanvraag aan is toegewezen, treedt deze fout op. Verwijder de aanvraag die aan de cellen is toegewezen of kies een andere reeks cellen voor toewijzing. Wanneer u cellen wilt verwijderen, is het belangrijk dat u cellen met aanvragen zoekt en de aanvragen verwijdert voordat u de cellen verwijdert (rijen of kolommen verwijdert).
* **Sluit de gemarkeerde Excel-cel af voordat u deze functie gebruikt.**: Als u in een Excel-cel staat in *bewerkingsmodus* en op een van de pictogrammen van Report Builder klikt, verschijnt dit foutbericht. De bewerkingsmodus in een Excel-cel betekent dat de cel is geselecteerd en de cursor in de cel wordt weergegeven. U bent ook in bewerkingsmodus in een Excel-cel wanneer u direct in de [!UICONTROL Formula]-balk of in de [!UICONTROL Name Box] boven in Excel typt.
* **Het geselecteerde bereik doorsnijdt het bereik van een andere aanvraag. Wijzig de selectie.**: Als u al een set cellen aan de spreadsheet hebt toegewezen, wordt deze fout weergegeven.
* **Herstelt aan werkboek (Verwijderde Verslagen: Formule van /xl/calcChain.xml**: Soms worden de formules van een werkboek bedorven wanneer het bewaren of het overbrengen. Wanneer het dossier wordt geopend, probeert Excel om deze formules in werking te stellen en ontbreekt. U kunt dit probleem oplossen door `calcChain.xml` van het spreadsheet, dwingend Excel om zijn formuleringsberekeningen te verfrissen.
   1. De naam van de bestandsextensie van het werkboek wijzigen van `.xlsx` tot `.zip`.
   2. Pak de inhoud uit en open de `/xl/` map.
   3. Verwijderen `calcChain.xml`.
   4. Comprimeer de inhoud en wijzig de bestandsextensie weer in `.xlsx`.
   5. Open het werkboek in Excel en vernieuw alle verzoeken van Report Builder.
* **Excel-cellen die zijn gekoppeld aan de invoerfilters of het uitvoerbereik kunnen zijn verwijderd**: Report Builder gebruikt de Namen van Excel om gegevensverzoeken aan cellen vast te maken. Als u de Namen van Excel van het Manager van Namen schrapt, kunt u deze fout zien. Aanvragen kunnen niet worden hersteld als Excel-namen worden verwijderd. Als het werkboek gepland was, kunt u of een exemplaar van de Plannende Manager downloaden, of eerder geleverde exemplaren van het werkboek openen.
