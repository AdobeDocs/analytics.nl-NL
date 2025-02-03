---
title: Gebruikersvoorkeuren en bedrijfsvoorkeuren instellen in Analysis Workspace
description: U kunt algemene voorkeuren en projectvoorkeuren instellen voor gebruikers en een voorkeur voor donkere thema's.
feature: Workspace Basics
role: User, Admin
exl-id: f32e3061-f396-4730-96e1-d251b00e32f0
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '3108'
ht-degree: 0%

---

# Voorkeuren

U kunt instellingen voor Analysis Workspace en de bijbehorende componenten voor alle nieuwe projecten of deelvensters beheren die u maakt. Bestaande projecten en deelvensters worden niet beïnvloed.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ voorkeur ](https://video.tv.adobe.com/v/332600/?quality=12&learn=on){target="_blank"} voor een demo video beheren.

>[!ENDSHADEBOX]


## Voorkeuren bijwerken

1. In Adobe Analytics, ga naar [!UICONTROL **Project**] landende pagina, dan selecteren [!UICONTROL **Voorkeur**].

   ![ voorkeur van de Gebruiker ](assets/user-preferences.png)

1. Voor informatie over de beschikbare voorkeuren op elk tabblad gaat u verder met een van de volgende secties in dit artikel:

   * [Algemene voorkeuren](#general-preferences)

   * [Bedrijf](#company-preferences)

   * [Projectvoorkeuren](#project-preferences)

   * [Voorkeuren voor de tabel Vrije vorm](#freeform-table-preferences)

   * [Voorkeuren voor visualisatie](#visualizations-preferences)

## Algemene voorkeuren

U kunt algemene voorkeuren aanpassen voor alle nieuwe projecten die u in Analysis Workspace maakt. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [ voorkeur van de Update ](#update-preferences).

| Voorkeur | Opties |
| --- | --- |
| Openingspagina | Kies welke pagina als de standaardpagina wordt weergegeven wanneer u Adobe Analytics opent: <ul><li>Projectlijst (standaard)</li><li>Leeg project</li><li>Specifiek project geselecteerd uit een lijst</li></ul> |
| Tips weergeven | Hiermee geeft u tips weer in een blauw vak rechtsonder in Analysis Workspace. <p>Deze optie is standaard ingeschakeld.</p> |
| Onderdelen die worden weergegeven in linkerspoorweggroepen | Kies hoeveel van elke component in het menu Componenten in de linkerspoorstaaf moet worden weergegeven. <p>Als u 0 kiest, is de component niet meer toegankelijk vanaf de linkerspoorstaaf van uw werkruimten.</p><p>Standaard worden vijf componenten weergegeven voor elk van de volgende opties:</p> <ul><li>Dimensies</li><li>Metrics</li><li>Filters</li><li>Datumbereiken</li></ul> <p>Voor meer informatie over Componenten in Analysis Workspace, zie [ Overzicht van Componenten ](/help/analyze/analysis-workspace/components/analysis-workspace-components.md).</p> |

## Bedrijfsvoorkeuren

U kunt bedrijfvoorkeur bijwerken die op alle gebruikers en projecten binnen uw organisatie van toepassing is. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [ voorkeur van de Update ](#update-preferences).

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **het lusje van Rapporten** | | |
|  | Tabblad Rapporten verbergen | Hiermee verbergt u het tabblad Rapporten voor alle gebruikers in uw organisatie. |
| **het delen van het Project** | | |
| | Alleen delen met Workspace-gebruikers toestaan | <p>Wanneer deze optie is ingeschakeld, kunnen gebruikers in uw organisatie de optie &quot;Delen met iedereen&quot; niet zien in het menu Delen. Dit betekent dat de gebruikers geen projecten met mensen kunnen delen die geen rekening van Analysis Workspace in uw organisatie hebben zoals die in [ wordt beschreven een project met iedereen (geen vereiste login) ](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link) in [ projecten van het Aandeel ](/help/analyze/analysis-workspace/curate-share/share-projects.md).</p><p>Houd rekening met het volgende wanneer u deze optie in- of uitschakelt:</p> <ul><li><p>Wanneer u deze optie inschakelt, hebben mensen die eerder via de optie &quot;Delen met iedereen&quot; toegang tot een project hebben gekregen, geen toegang meer tot het project.</p></li><li><p>Als deze optie is ingeschakeld (om alleen delen met Workspace-gebruikers toe te staan) en later is uitgeschakeld (om delen met iedereen toe te staan), krijgen mensen die eerder toegang tot een project hebben gekregen via de optie Delen met iedereen) niet automatisch weer toegang tot het project. In dit geval, moet de gebruiker die het project deelde de [!UICONTROL **Verbinding toelaten is actieve**] optie die beschikbaar is wanneer het delen van een project met iedereen ([!UICONTROL **Aandeel**] > [!UICONTROL **Aandeel met iedereen**]), zoals die in [ wordt beschreven een project met iedereen (geen vereiste login) ](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link) in [ projecten van het Aandeel ](/help/analyze/analysis-workspace/curate-share/share-projects.md).</p></li> |
| | Verificatie van Experience Cloud vereisen | <p>Wanneer toegelaten, moeten de mensen die toegang tot een project van &quot;Aandeel met iedereen&quot;optie in Analysis Workspace worden verleend voor authentiek verklaren gebruikend hun geloofsbrieven van het Experience Cloud.</p> <p>Nadat deze optie is ingeschakeld, wordt de optie &quot;Verificatie van Experience Cloud vereisen&quot; ingeschakeld in het dialoogvenster Delen wanneer een gebruiker een project deelt met de optie &quot;Delen met iedereen&quot;. De gebruiker die het project deelt, kan dit niet uitschakelen. (Voor informatie over hoe de gebruikers projecten met iedereen kunnen delen, zie [ een project met iedereen (geen vereiste login) delen ](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link) in [ projecten van het Aandeel ](/help/analyze/analysis-workspace/curate-share/share-projects.md).)</p> <p>Houd rekening met het volgende wanneer u deze optie inschakelt:</p><ul><li><p>Wanneer u deze optie inschakelt, worden alle projecten die eerder met de optie &quot;Delen met iedereen&quot; zijn gedeeld en waarvoor de optie &quot;Verificatie van Experience Cloud vereisen&quot; niet is ingeschakeld, gedeactiveerd.</p></li> <li><p>Als deze optie wordt toegelaten (om Experience Cloud authentificatie te vereisen) en dan later onbruikbaar gemaakt (om iedereen met de verbinding toe te staan om tot het project toegang te hebben), krijgen de mensen die eerder toegang tot een project door &quot;Aandeel met iedereen&quot;aandeeloptie ontvingen niet automatisch hun toegang tot het project terug. In dit geval, moet de gebruiker die het project deelde de &quot;Verbinding actief&quot;optie toelaten die beschikbaar is wanneer het delen van een project met iedereen ([!UICONTROL **Aandeel**] > [!UICONTROL **Aandeel met iedereen**] > [!UICONTROL **Verbinding is actief**]), zoals die in [ wordt beschreven een project met iedereen (geen vereiste login) ](/help/analyze/analysis-workspace/curate-share/share-projects.md#share-public-link) in [ projecten van het Aandeel ](/help/analyze/analysis-workspace/curate-share/share-projects.md).</p></li> <li><p>Deze optie is alleen beschikbaar als SSO in uw organisatie is geïmplementeerd. Voor informatie over hoe de systeembeheerders SSO voor uw organisatie kunnen toelaten, zie [ Identiteit van de Opstelling en Enige Sign-On ](https://helpx.adobe.com/enterprise/using/set-up-identity.html) {target=_blank}.</p><p>Als SSO voor uw organisatie wordt gevormd, controleer om te zien of wordt om het even welk soort auto-rekening verwezenlijking uitgevoerd in de console. Typisch, zou een systeembeheerder deze opstelling, zoals die in [ wordt beschreven automatische rekeningsverwezenlijking ](https://helpx.adobe.com/enterprise/using/automatic-account-creation.html) {target=_blank} toelaten.</p></li><li><p>Als uw organisatie in een industrie is die naleving HIPAA vereist, wordt deze optie automatisch toegelaten en kan niet worden onbruikbaar gemaakt.</p></li></ul> |

{style="table-layout:auto"}

## Voorkeuren voor projecten en analyses

U kunt projectvoorkeuren aanpassen voor alle nieuwe projecten die u in Analysis Workspace maakt. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [ voorkeur van de Update ](#update-preferences).

Sommige van deze zelfde voorkeur kunnen ook voor individuele projecten worden aangepast, zoals die in [ het overzicht van het Project ](/help/analyze/analysis-workspace/build-workspace-project/freeform-overview.md) worden beschreven.

Klik op de gekoppelde voorkeurstitels voor meer informatie en context over elke voorkeur.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Vertoning** | | |
|  | [ dichtheid van de Mening ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/view-density.html) | Kies hoeveel inhoud u op het scherm wilt weergeven door de verticale opvulling van de linkerrails, vrije-vormtabellen en cohortabellen te verminderen. <ul><li>Compact</li><li>Comfortabel</li><li>Uitgebreid (standaard)</li></ul> |
| | [ palet van de Kleur ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/color-palettes.html) | Kies de visualisatiekleurenpaletten die in Analysis Workspace worden gebruikt.<ul><li>**Categorisch palet**: Toegepast op vele visualisaties in Analysis Workspace. Elke kleur vertegenwoordigt een duidelijke categoriale waarde. Kies een optie voor door de Adobe opgegeven opties of voer een aangepast palet in dat met komma&#39;s gescheiden hexwaarden wordt gedefinieerd.</li><li>**Afwisselend palet**: Toegepast op de lijst van de Cohort in Analysis Workspace. Dit palet heeft een numerieke betekenis met twee uiteinden en een basislijn in het midden.</li><li>**Opeenvolgend palet**: Toegepast op de tendensen van de Frequentie (gestapelde bar) geleide analyse. Dit palet heeft een numerieke betekenis, van licht tot donker.</li></ul> |
| **Gegevens** | | |
|  | [ Reeks van het Rapport ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?#report-suite) | Kies uit waar tabellen en visualisaties de gegevens afleiden. <ul><li>Recentste (standaard)</li><li>Specifieke rapportsuite geselecteerd uit een lijst</li></ul> |
|  | [ Kalender ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html?#calendar) | Selecteer uit een lijst van: <ul><li>Door Adobe opgegeven bereiken (standaard is deze maand)</li><li>Aangepast gedefinieerde bereiken</li></ul> |
|  | [ Type van Comité ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/panels.html) | <ul><li>Vrije vorm (standaard)</li><li>Leeg</li><li>Snelle inzichten</li></ul> |
|  | Herhalingsinstanties tellen | Geeft aan of herhalingsinstanties worden geteld in rapporten. Met deze instelling (indien geactiveerd) worden bijvoorbeeld meerdere weergaven van opeenvolgende pagina&#39;s op dezelfde pagina behandeld als weergaven van meerdere pagina&#39;s. Als deze optie is uitgeschakeld, tellen ze als een weergave van één pagina. <p>**Nota:** Dit het plaatsen beïnvloedt slechts bepaalde metriek (zoals Enige Bezoekingen van de Pagina) en het is niet op Stroom of Vallout visualisaties van toepassing.</p> |
|  | Getalnotatie | <ul><li>1.000.00 (standaard)</li><li>1.000,00</li><li>1 000 00</li></ul> |
|  | CSV-scheidingsteken | <ul><li>Komma (standaard)</li><li>Puntkomma</li><li>Colon</li><li>Pijp</li><li>Periode</li><li>Spatie</li><li>Tab</li></ul> |
|  | Annotaties tonen | Kies of annotaties zichtbaar zijn in uw projecten. Voor meer informatie over annotaties, zie [ Overzicht van Annotaties ](/help/analyze/analysis-workspace/components/annotations/overview.md). |

## Voorkeuren voor de tabel Vrije vorm

U kunt de voorkeuren voor vrije-vormtabellen aanpassen voor alle nieuwe projecten die u in Analysis Workspace maakt. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [ voorkeur van de Update ](#update-preferences).

Sommige van deze voorkeuren kunnen ook worden aangepast voor afzonderlijke tabellen.

Klik op de titels van de gekoppelde sectie voor meer informatie en context over de beschikbare voorkeuren.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Lijst** | | |
| | Tabeltype | <ul><li>Vrije vorm</li><li>Tabelbuilder</li></ul> |
| | Standaardtabelmetrisch | <ul><li>Voorvallen</li><li>Unieke bezoekers</li><li>Bezoeken</li></ul> |
| | Standaardtabelafmetingen | Kies uit Minuut, Uur, Dag, Week, Maand, Kwart of Jaar. |
| | Datums uitlijnen | Selecteer deze optie als u datums uit elke kolom wilt uitlijnen met alle datums die op dezelfde rij beginnen. |
| **[Kolom](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)** | | |
| | Koptekst van tekstomloop | Hiermee kunt u de koptekst laten omlopen in Freeform-tabellen om kopteksten leesbaarder te maken en tabellen beter deelbaar te maken. Dit is handig voor .pdf-rendering en voor metriek met lange namen. Standaard ingeschakeld. |
| | Totalen tonen | Dit totaal is doorgaans gelijk aan of een subset van de [!UICONTROL Grand Total] . Dit weerspiegelt alle tabelfilters die binnen de vrije-vormtabel worden toegepast, inclusief de optie [!UICONTROL Include None] . |
| | Totaal tonen | Dit totaal vertegenwoordigt alle treffers die zijn verzameld, soms genoemd &quot;rapportsuite total&quot;. Wanneer een segment wordt toegepast op deelvensterniveau of binnen de vrije-vormtabel, wordt dit totaal aangepast aan alle resultaten die overeenkomen met de segmentcriteria. Het grote totaal wordt niet gesteund voor lijsten of onderverdelingen met [ statische rijen ](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md). |
| | Menggrijswaarden tonen | Lijngrafieken onder aan het diagram weergeven of verbergen. Als de legenda is verborgen, wordt deze niet langer visueel doorverwezen naar de regels. |
| | Getal | Hiermee wordt bepaald of in een cel de numerieke waarde voor de metrische waarde wordt weergegeven of verborgen. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de numerieke waarde het aantal paginaweergaven voor het rij-item. |
| | Percentage | Bepaalt of een cel de percentagewaarde voor metrisch toont/verbergt. Als de metrische waarde bijvoorbeeld Paginaweergaven is, is de percentagewaarde het aantal paginaweergaven voor het rijitem gedeeld door de totale paginaweergaven voor de kolom.  Opmerking: we kunnen percentages van meer dan 100% weergeven, om nauwkeuriger te zijn. We verplaatsen het bovenste gebonden plafond ook naar 1000% om ervoor te zorgen dat kolommen te groot kunnen worden. |
| | anomalieën tonen <!-- This setting was moved from the "Project" tab. this is already in the tool/docs under "Freeform table, But the doc doesn't give a definition. --> | Hiermee wordt bepaald of de waarden in deze kolom een anomaliedetectie uitvoeren. |
| | nul interpreteren als geen waarde | Voor cellen met een waarde 0 bepaalt u of een cel van 0 of een lege cel moet worden weergegeven. Dit is handig wanneer u gegevens bekijkt voor elke dag van een maand, en sommige dagen zijn nog niet gebeurd.  In plaats van &#39;0&#39; voor toekomstige datums weer te geven, kunnen lege cellen worden weergegeven. Grafieken voldoen ook aan deze instelling (ze geven dus geen lijn of balk weer met 0 waarden als deze instelling is ingeschakeld). |
| | Achtergrond | Hiermee wordt bepaald of alle celopmaak, inclusief de staafgrafiek en voorwaardelijke opmaak, in een cel wordt weergegeven of verborgen <ul><li>Staafgrafiek</li> Hiermee wordt een horizontale staafgrafiek weergegeven die de waarde van de cel ten opzichte van het totaal voor de kolom vertegenwoordigt. <li>Voorwaardelijke opmaak</li>Voor meer informatie over voorwaardelijk formatteren, zie &quot;Voorwaardelijke het formatteren&quot;in [ Montages van de Kolom ](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/column-settings.md)</ul> |
| | Celvoorvertoning | Toont een voorproef van hoe elke cel met de momenteel geselecteerde opmaakopties wordt getoond. |
| **[Rij](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/table-settings.md)** | | |
| | Uitsplitsing naar positie | Selecteer deze optie als u wilt dat de uitsplitsing bij de positie van het item blijft en niet bij het item zelf. Voor meer informatie over onderverdelingen, zie [ onderverdelingen dimensies ](/help/analyze/analysis-workspace/components/dimensions/t-breakdown-fa.md). |
| | Percentage berekening | <ul><li>Kolom</li><li>Rij</li></ul> |
| | Kolomtotalen (alleen statische rijen) | <ul><li>De som van rijen weergeven: geeft de som van de afzonderlijke regelitems weer </li><li>Totaal-generaal weergeven: geeft de gedupliceerde som van rijen weer.</li></ul> |

## Voorkeuren voor visualisatie

U kunt de visualisatievoorkeuren bijwerken voor alle nieuwe projecten die u in Analysis Workspace maakt. Voor informatie over hoe te om tot deze voorkeur toegang te hebben, zie [ voorkeur van de Update ](#update-preferences).

Sommige van deze voorkeuren kunnen ook worden aangepast voor afzonderlijke visualisaties.

Klik op de titels van de gekoppelde sectie voor meer informatie en context over de beschikbare voorkeuren.

| Sectie | Voorkeur | Opties |
| --- | --- | --- |
| **Algemene Gebreken** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor alle visualisaties. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legendetekst voor alle visualisaties verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as voor alle visualisaties. Dit kan handig zijn als u een grote gegevensset hebt. |
| | Dubbele as weergeven (indien van toepassing) | Is slechts van toepassing als u twee metriek hebt - u kunt een y-as op de linkerzijde (voor één metrisch) en op het recht (voor andere metrisch) hebben. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Normalisatie (indien van toepassing) | Dwingt metriek tot gelijke verhoudingen. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Y-as anker bij nul | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO ingesteld als de standaardinstelling van het diagram. Als u dit vakje inschakelt, wordt de y-as gedwongen tot nul (en wordt het diagram opnieuw getekend). |
| | Afwijkingen van schaal Y-as toestaan | Als u veelvoudige metriek in een grafiek hebt, moet u over elke anomalie bewegen om de betrouwbaarheidsband voor die metrisch te zien. De y-as wordt niet automatisch geschaald om de visualisatie beter leesbaar te maken met het betrouwbaarheidsinterval Anomaly-detectie. Met deze optie kan het betrouwbaarheidsinterval de visualisatie schalen. <p>Voor meer informatie, zie [ anomalieën van de Mening in Analysis Workspace ](/help/analyze/analysis-workspace/c-anomaly-detection/view-anomalies.md).</p> |
| **[Lijn](/help/analyze/analysis-workspace/visualizations/line.md)** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor de lijnvisualisatie. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor lijnvisualisatie verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as in de lijnvisualisatie. Dit kan handig zijn als u een grote gegevensset hebt. |
| | Dubbele as weergeven (indien van toepassing) | Is slechts van toepassing als u twee metriek hebt - u kunt een y-as op de linkerzijde (voor één metrisch) en op het recht (voor andere metrisch) hebben. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | Normalisatie (indien van toepassing) | Dwingt metriek tot gelijke verhoudingen. Dit is handig wanneer uitgezette metriek van zeer verschillende grootten zijn. |
| | x-as tonen | Hiermee geeft u de x-as weer op het lijndiagram. |
| | Y-as tonen | Hiermee geeft u de y-as op het lijndiagram weer. |
| | Y-as van anker | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO ingesteld als de standaardinstelling van het diagram. Als u dit vakje inschakelt, wordt de y-as gedwongen tot nul (en wordt het diagram opnieuw getekend). |
| | min. tonen | Bedek een label voor een minimumwaarde om de dalen snel in metrische vorm te markeren. Opmerking: de hoofdwaarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie. |
| | max. tonen | bedek een label voor de maximumwaarde om de pieken snel in metrisch formaat te markeren. Opmerking: de maximale waarden worden afgeleid van de zichtbare gegevenspunten in de visualisatie, niet van de volledige reeks waarden binnen een dimensie. |
| | Trendline tonen | Toon een regressie of bewegende gemiddelde trendline aan uw lijnreeks. Met behulp van trendlines wordt een duidelijker patroon in de gegevens weergegeven. |
| **[Cohort](/help/analyze/analysis-workspace/visualizations/cohort-table/t-cohort.md)** | | |
| | Granulariteit | Voor getreneerde visualisaties kunt u de tijdsgranulariteit (Dag, Week, Maand, Kwart, of Jaar) veranderen. Deze wijziging geldt ook voor de gegevensbrontabel. |
| | Alleen percentages weergeven | Hiermee verwijdert u de getalwaarde en geeft u alleen het percentage weer. |
| | Percentages afronden naar dichtstbijzijnde gehele getal | Rondt de percentagewaarde aan het meest dichtbijgelegen geheel in plaats van het tonen van de decimale waarde. |
| | Gemiddelde percentagerij weergeven | Hiermee voegt u een nieuwe rij boven aan de tabel in en voegt u vervolgens het gemiddelde voor de waarden binnen elke kolom toe. |
| | Voorvertoning van cohort | Een voorvertoning van de manier waarop het kleurenpalet in de cohortvisualisatie wordt weergegeven. |
| | Kleurenpalet Cohort | Het kleurenpalet dat wordt gebruikt in de cohortvisualisatie. |
| **[Combo grafieken](/help/analyze/analysis-workspace/visualizations/combo-charts.md)** | | |
| | X-as tonen | Hiermee geeft u de x-as weer op de Combo-grafiek. |
| | Y-as tonen | Hiermee geeft u de y-as weer op de keuzelijst met invoervak. |
| | Scheepjes weergeven op lijnen | Ballonnen tonen op lijnen in Combo-grafieken. |
| **[Zeer belangrijke Metrische Samenvatting](/help/analyze/analysis-workspace/visualizations/key-metric.md)** | | |
| | Weergavetype Samenvatting | <ul><li>Percentage wijziging benadrukken</li><li>Nummerwaarde benadrukken</li></ul> |
| | Meerdere regels tonen | hoe of verberg lijngrafieken bij de bodem van de grafiek. Als de legenda is verborgen, wordt deze niet langer visueel doorverwezen naar de regels. |
| | max. en min. tonen op vonklines | Minimum- en maximumwaarden tonen op primaire diagrammen en vergelijkingslijngrafieken. |
| | Vergelijking tonen | Vergelijkingsgegevens tonen. Wanneer deze optie is verborgen, worden zowel het vergelijkingsregeldiagram als de summiere wijzigingsobjecten verborgen. |
| | Nummerwaardeopties | In de [!UICONTROL **Zeer belangrijke Metrische Summiere**] sectie <ul><li>Percentage wijziging tonen</li><li>Raw-verschil tonen</li>Onbewerkt verschil tussen de totale waarde van de meting in het primaire datumbereik en het secundaire datumbereik</ul> |
| **[Uitval](/help/analyze/analysis-workspace/visualizations/fallout/configuring-fallout.md)** | | |
| | Container | Hiermee kunt u schakelen tussen Bezoek en Bezoeker om het plakken van bezoekers te analyseren. De standaardinstelling is Bezoeker. Met deze instellingen kunt u de betrokkenheid van bezoekers op bezoekersniveau (verschillende bezoeken) begrijpen of de analyse beperken tot één bezoek. <p>De volgende opties zijn beschikbaar:</p> <ul><li>Bezoek</li><li>Bezoeker</li></ul> |
| **[Stroom](/help/analyze/analysis-workspace/visualizations/c-flow/create-flow.md)** | | |
| | Container | In de [!UICONTROL **Stroom**] sectie <ul><li>Bezoek</li><li>Bezoeker</li></ul> |
| | Labels voor tekstomloop | Normaal gesproken worden de labels op de Flow-elementen ingekort om de schermruimte op te slaan, maar u kunt het volledige label zichtbaar maken door dit selectievakje in te schakelen. Standaard = uitgeschakeld. |
| | Herhalingsinstanties opnemen | Stroomvisualisaties zijn gebaseerd op instanties van een dimensie. Met deze instelling kunt u herhaalde exemplaren, zoals opnieuw laden van pagina&#39;s, opnemen of uitsluiten. Herhalingen kunnen echter niet worden verwijderd uit Flow-visualisaties met multigetaxeerde afmetingen, zoals listVars, listProps, s.product, merchandising Vars, enz. Standaard = uitgeschakeld. |
| | Knopinfo weergeven | Bepaalt of tooltips die knoopgegevens bevatten wanneer het hangen over individuele knopen binnen een stroomvisualisatie worden getoond. |
| | Aantal kolommen | Hiermee bepaalt u hoeveel kolommen u in het stroomdiagram wilt opnemen. |
| | Items uitgevouwen per kolom | Hoeveel punten u in elke kolom wilt. |
| **Gestapelde Grafieken** | | |
| | 100% gestapeld | Met deze instelling op een gestapeld gebied, gestapelde staaf of horizontale staaf verandert u het diagram in een &#39;100% gestapelde&#39; visualisatie. <p>Voor meer informatie, zie [ gestapelde Bar en bar ](/help/analyze/analysis-workspace/visualizations/bar.md).</p> |
| **[Histogram](/help/analyze/analysis-workspace/visualizations/histogram.md)** | | |
| | Aantal emmers | Kies het aantal gegevensbereiken (emmers) in de visualisatie. Het maximumaantal emmers is 50. <p>Voor meer informatie, zie [ Histogram ](/help/analyze/analysis-workspace/visualizations/histogram.md).</p> |
| | Telmethode | Kies een van de volgende opties: <ul><li>Actief</li><li>Bezoek</li><li>Bezoeker</li></ul> <p>Als u dit bijvoorbeeld gebruikt in combinatie met paginaweergaven, kunt u per bezoeker paginaweergaven, paginaweergaven voor een bezoek of paginaweergaven per hit kiezen. Bij Actief wordt &quot;Voorvallen&quot; gebruikt als de metrische y-as in een vrije-vormtabel.</p> |
| **[Kaart](/help/analyze/analysis-workspace/visualizations/map-visualization.md)** | | |
| | Dimensie vastzetten | <ul><li>Mobiele breedte/lengte</li><li>Geografische dimensie</li></ul> |
| | Type kaart | <ul><li>Luchtbellen</li><li>Warmtekaart</li></ul> |
| | Kleurthema | Kies uit Koraal, Rode tinten, Groenen, Vervagen, Heatmap en Positief/Negatief. |
| | Toewijzingsstijl | Kies uit Standaard, Streets, Helder, Licht, Donker en Satelliet. |
| **[Summiere Verandering](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Waarde | <!-- Seem to be basically the same options as in "Number value options" --> <ul><li>Percentage wijziging</li><li>Onbewerkt verschil</li></ul> |
| | Percentage | De waarden van vertoningen in percentages voor de Summiere visualisaties van de Verandering. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de visualisatie Samenvattingswijziging verbergen. |
| **[Summiere Aantal](/help/analyze/analysis-workspace/visualizations/summary-number-change.md)** | | |
| | Percentage | De waarden van vertoningen in percentages voor de Summiere visualisaties van het Aantal. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de visualisatie Samenvattingsnummer verbergen. |
| | Samenvattingswaarde met | Kies uit Max, Min, Gemiddeld, Mediaan en Sum. |
| | Afkorting | In de [!UICONTROL **Summiere sectie van het Aantal**] |
| **[Boomstructuur](/help/analyze/analysis-workspace/visualizations/treemap.md)** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor de Treemap-visualisaties. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as in de Treemap-visualisatie. Dit kan handig zijn als u een grote gegevensset hebt. |
| **[Venn](/help/analyze/analysis-workspace/visualizations/venn.md)** | | |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legendetekst voor de Venn-visualisatie verbergen. |
| **[Spreiding](/help/analyze/analysis-workspace/visualizations/scatterplot.md)** | | |
| | Percentage | Hiermee geeft u waarden weer in percentages voor de verstrooiingsvisualisaties. |
| | Legenda zichtbaar | Hiermee kunt u de gedetailleerde legenda-tekst voor de verstrooiing verbergen. |
| | Maximale aantal items | Hiermee verkleint u het aantal items op de X-as in de verstrooiingsvisualisatie. Dit kan handig zijn als u een grote gegevensset hebt. |
| | Anker y-as bij nul | Als alle waarden die in het diagram worden uitgezet aanzienlijk boven nul liggen, wordt de onderkant van de y-as NON-ZERO ingesteld als de standaardinstelling van het diagram. Als u dit vakje inschakelt, wordt de y-as gedwongen tot nul (en wordt het diagram opnieuw getekend). |

## Standaardvoorkeuren herstellen

U kunt al uw gebruikersvoorkeuren herstellen naar de standaardwaarden van het systeem. Dit beïnvloedt beheerdervoorkeur onder het Bedrijf tabel niet.

Deze handeling kan niet ongedaan worden gemaakt.

1. In Adobe Analytics, uitgezochte [!UICONTROL **Componenten**] **>** [!UICONTROL **Voorkeur**].

   ![ voorkeur van de Gebruiker ](assets/user-preferences.png)

1. Selecteer **[!UICONTROL Restore defaults]** in de rechterbovenhoek.

1. Selecteer **[!UICONTROL Restore defaults]** wanneer hierom wordt gevraagd.

## [!UICONTROL Dark theme]

Als u liever een donkere achtergrond voor uw Adobe Analytics-gebruikersinterface hebt, kunt u schakelen naar [!UICONTROL Dark theme] .

1. Klik op het gebruikerspictogram van het Experience Cloud rechtsboven.

   ![ donker-thema ](assets/dark-theme.png)

1. Verplaats de **[!UICONTROL Dark theme]** -schakeloptie naar rechts.

