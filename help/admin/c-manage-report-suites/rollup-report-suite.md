---
description: Beschrijvingen van de types van rapportsuite en vergelijking van globale rapportsuites en rollup rapportsuites.
title: Methoden van rapportsuite
feature: Report Suite Settings
exl-id: 97bdc9bd-2212-436b-b3b4-ec518624f9e6
source-git-commit: 72bd67179e003b70233d863d34153fec77548256
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Methoden van rapportsuite

<!-- change filename since page name changed? -->

U kunt uw rapportreeksen als één van beide vormen *globale rapportsuites* of *rollup-rapportsuites*.

## Globale rapportsuites

Een algemene rapportsuite verzamelt gegevens van alle domeinen en apps die eigendom zijn van uw organisatie. De implementatie vereist om alle verzoeken om images naar één rapportsuite te verzenden.

Adobe beveelt in de meeste gevallen aan een algemene rapportsuite te implementeren. Zie &quot;[Overwegingen voor algemene rapporten](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/global-rs.html)&quot; voor de voordelen van de implementatie van een algemene rapportenreeks.

Met de *taggen met meerdere suite* en *virtuele rapportsuite* benaderingen:

* **Tags toevoegen met meerdere suite**: Met tagging met meerdere suite kunt u verzoeken om images niet alleen naar een algemene rapportsuite verzenden, maar ook naar afzonderlijke groepen met onderliggende rapporten. De globale rapportgegevens worden gededupliceerd over alle rapportsuites.

   Bijvoorbeeld, zou u alle gegevens in één globaal rapportreeks kunnen verzamelen en ook secundaire rapportsuites opzetten die op merk, regio, of een andere differentiator worden gebaseerd. De verschillende teams in uw bedrijf konden zich dan op gegevens in de rapportreeksen concentreren die voor hen relevant zijn.

   Om multi-suite het etiketteren te gebruiken, voer de reeksen van het kindrapport en een globale rapportreeks uit die alle gegevens van de kinderen omvat. De volgende code voor uw webpagina&#39;s en apps zal identiteitskaart van de Reeks van het Rapport (RSID) voor de globale rapportreeks en ook RSIDs voor de toepasselijke reeksen van het kindrapport omvatten.<!-- Wording/be more specific? And include any links? -->

   Er wordt een aparte serveraanroep naar elke rapportsuite in de afbeeldingsaanvraag uitgevoerd. De vraag aan de reeksen van het kindrapport is secundaire vraag.

* **Virtuele rapportsuite**: A [virtuele rapportsuite](/help/components/vrs/vrs-about.md) is een vraag op gespecificeerde segmenten die in een globale rapportreeks worden verzameld, en beschikbaar aan gespecificeerde groepen gebruikers. De virtuele rapportsuites staan u toe om rapportelementen voor verschillende eindgebruikers te leiden zonder multi-suite het etiketteren te gebruiken, waarbij secundaire servervraag wordt vermeden.

   Om virtuele rapportreeksen te gebruiken, voer een globale rapportreeks uit en ontleed dan de gegevens om virtuele rapportreeksen met specifieke toegepaste segmenten en met specifieke groepstoestemmingen tot stand te brengen. U kunt virtuele-rapportsuites maken in Virtual Report Suite Manager ([!UICONTROL Components] > [!UICONTROL Virtual Report Suites]). Zie &quot;[Workflow voor virtuele rapportsuite](/help/components/vrs/c-workflow-vrs/vrs-workflow.md)&quot; voor meer informatie .

Het gebruik van virtuele-rapportsuites in plaats van taggen met meerdere suite is vaak de beste manier, maar virtuele-rapportsuites hebben een aantal beperkingen. Zie &quot;[Virtuele rapportreeksen en tagging met meerdere suite-overwegingen](/help/components/vrs/vrs-considerations.md)&quot; om te bepalen welke rapportsuite-benadering de beste keuze is voor uw bedrijfsbehoeften. Voor een diepgaande vergelijking van virtuele rapportsuites en multi-suite het etiketteren functionaliteit, zie &quot;[Virtuele rapportsuite versus meerdere suite-tags](/help/components/vrs/vrs-about.md#section_317E4D21CCD74BC38166D2F57D214F78).&quot;

## Rolluprapporten

>[!NOTE]
>
>[!DNL Reports & Analytics] is het enige hulpmiddel dat rolluprapporten steunt, en Adobe adviseert niet meer het gebruiken van rollups. Overweeg in plaats daarvan een algemene rapportsuite met tags voor meerdere suite of virtuele rapportensuites.

Een rolluprapport is een eenvoudige samenvoeging van gegevens uit meerdere rapportageopes, zonder deduplicatie of een segment of gegevensuitsplitsingen. Rollups vereisen geen code-implementatie. Rolluprapporten gebruiken [gebruik maken van een kinderrapport](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md) en vervolgens [combineren in een rolluprapport](/help/admin/c-manage-report-suites/t-rollups.md) gebruiken [!UICONTROL Admin Tools].

Rolluprapporten zijn gratis: de reeksen van het kindrapport veroorzaken hun eigen servervraag, maar rollup leidt geen extra vraag. Rollups zijn een oudere functie en hebben vele beperkingen.

### Beperkingen van rolluprapporten {#limitations-rollups}

* Rollups verschaffen totale gegevens, maar rapporteren geen afzonderlijke waarden in rapporten. eVar1-waarden worden bijvoorbeeld niet opgenomen, maar het totale totaal kan wel.
* De gegevens worden niet gededupliceerd wanneer de rollup gegevens over rapportreeksen combineert.
* Rollups worden elke avond om middernacht uitgevoerd.
* Wanneer u een rapportsuite toevoegt aan een bestaande rollup, worden historische gegevens niet opgenomen in de rollup.
* Alle reeksen van het kindrapport moeten gegevens in hen hebben om een rollup te functioneren. Als nieuwe rapportsuites in een rollup worden omvat, zorg ervoor om minstens één paginamening naar elk van die rapportsuites te verzenden.
* Rollup-rapportreeksen kunnen maximaal 40 kindrapportsuites bevatten.
* Rollup-rapportsuites kunnen maximaal 100 gebeurtenissen bevatten.
* Gegevens in de reeksen van het rolluprapport ondersteunen geen onderverdelingen of segmenten.
* Het rapport Pagina&#39;s wordt vervangen door het rapport Popular Sites, dat metriek op het kind-suite niveau rapporteert.

## Vergelijking van de rapportfuncties Global Report Suite en Rollup

**Secundaire serveraanroepen**: Rollups doen geen extra serveraanroepen meer dan een enkele rapportsuite verzamelt. Als uw organisatie multi-suite markering gebruikt, worden secundaire serveraanroepen gedaan voor elke extra rapportsuite die in een beeldverzoek is opgenomen.

>[!TIP]
>
>Als u alleen een algemene rapportsuite gebruikt met [virtuele rapportsuites](/help/components/vrs/vrs-considerations.md), zijn geen secundaire servervraag nodig.

**Wijzigingen in implementatie**: Rollups vereisen geen implementatiewijzigingen, terwijl voor algemene rapportsuites de id van de algemene rapportsuite in uw implementatie moet worden opgenomen.

**Duplicatie**: Globale rapportsuites dedupliceren unieke bezoekers, terwijl rollups niet. Als een gebruiker bijvoorbeeld drie van uw domeinen op dezelfde dag bezoekt, tellen de rollups drie dagelijkse unieke bezoekers. Globale rapportsuites zouden één unieke bezoeker registreren.

**Tijdskader**: Rollups worden alleen elke nacht om middernacht verwerkt, terwijl algemene rapportsuites gegevens met standaardlatentie rapporteren.

**Breedte**: Rollups hebben geen manier om te communiceren tussen rapportsuites. Globale rapportsuites kunnen krediet aan omzettingsvariabelen tussen rapportsuites en verstrekken het schilderen over rapportsuites.

**Historische gegevens**: Rollups kunnen historische gegevens verzamelen, terwijl globale rapportsuites alleen gegevens rapporteren vanaf het punt waarop ze zijn geïmplementeerd.

**Rapporten**: Global report suites verschaffen gegevens over alle dimensies; rollups verschaffen alleen geaggregeerde gegevens over rapporten op hoog niveau.

**Ondersteunde producten**: Rollups kunnen alleen worden gebruikt in Rapporten en Analytics. Ze worden niet ondersteund in Analysis Workspace of Data Warehouse. Globale rapportsuites kunnen over alle producten worden gebruikt.

**Aantal samengevoegde rapportreeksen**: Rollups bieden alleen ondersteuning voor maximaal 40 kindrapportsuites. Algemene rapportsuites kunnen worden geïmplementeerd op elk aantal domeinen of apps die u hebt.
