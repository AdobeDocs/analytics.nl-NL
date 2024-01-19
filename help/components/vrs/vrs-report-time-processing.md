---
description: De tijdverwerking van het rapport is een virtuele het rapportreeks plaatsen die gegevens om op een niet-destructieve, retroactieve manier toelaat worden verwerkt.
title: Tijdverwerking rapporteren
role: Admin
solution: Analytics
feature: VRS
exl-id: 3742b9d1-f1fb-4690-bd44-b4719ff9d9bc
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '1276'
ht-degree: 0%

---

# Tijdverwerking rapporteren

[!UICONTROL Report time processing] is een instelling voor een virtuele rapportsuite waarmee gegevens in Analysis Workspace op niet-destructieve, retroactieve wijze kunnen worden verwerkt.

[!UICONTROL Report Time Processing] beïnvloedt slechts de gegevens in de virtuele rapportreeks en beïnvloedt geen gegevens of gegevensinzameling in de reeks van het basisrapport. Het verschil tussen [!UICONTROL Report Time Processing] en traditionele analytische verwerking het best wordt begrepen gebruikend het volgende diagram:

![Traditionele verwerkingsleiding](assets/google1.jpg)

Tijdens de gegevensverwerking van Analytics, stromen de gegevens door de pijpleiding van de gegevensinzameling en in een preprocessing stap, die gegevens voor rapportering voorbereidt. Bij deze voorbewerkingsstap worden de logica voor het verlopen van het bezoek en de persistentielogica voor eVar (onder andere) toegepast op de gegevens terwijl deze worden verzameld. Het primaire nadeel van dit voorbewerkingsmodel is dat elke configuratie vooraf moet worden uitgevoerd voordat gegevens worden verzameld. Dit betekent dat wijzigingen in de instellingen voor voorbewerking alleen van toepassing zijn op nieuwe gegevens vanaf dat moment. Dit is problematisch als de gegevens uit orde aankomen of als de montages verkeerd werden gevormd.

[!UICONTROL Report Time Processing] Dit is een fundamenteel andere manier om analysegegevens voor rapportage te verwerken. In plaats van de verwerkingslogica vooraf te bepalen alvorens de gegevens worden verzameld, negeert de Analytics de gegevensreeks tijdens de preprocessing stap en past deze logica toe telkens als een rapport wordt in werking gesteld:

![Tijdverwerkingspijplijn rapporteren](assets/google2.jpg)

Deze verwerkingsarchitectuur maakt veel flexibelere rapportageopties mogelijk. Bijvoorbeeld, kunt u de periode van de bezoekonderbreking in om het even welke tijdsduur veranderen u op een niet destructieve manier wilt en die veranderingen worden weerspiegeld in uw persistentie van eVar en segmentcontainers voor de volledige rapporteringsperiode. Bovendien, kunt u om het even welk aantal virtuele rapportreeksen tot stand brengen, elk met de verschillende opties van de Verwerking van de Tijd van het Rapport die op de zelfde reeks van het basisrapport worden gebaseerd, zonder om het even welke gegevens in de reeks van het basisrapport te veranderen.

[!UICONTROL Report Time Processing] biedt Analytics ook de mogelijkheid om te voorkomen dat er nieuwe bezoeken op de achtergrond worden gestart en biedt de [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/mobile.html) om een nieuw bezoek te beginnen wanneer een gebeurtenis van de Lancering van de App wordt teweeggebracht.

## Configuratieopties

De volgende configuratieopties zijn momenteel beschikbaar aan virtuele rapportreeksen met toegelaten de Verwerking van de Tijd van het Rapport:

* **[!UICONTROL Visit Timeout]:** De time-outinstelling voor een bezoek definieert de hoeveelheid inactiviteit die een unieke bezoeker moet hebben voordat een nieuw bezoek automatisch wordt gestart. De standaardwaarde is 30 minuten. Als u de time-out van het bezoek bijvoorbeeld instelt op 15 minuten, wordt een nieuwe bezoekgroep gemaakt voor elke reeks verzamelde hits, gescheiden door 15 minuten inactiviteit. Deze instelling is niet alleen van invloed op uw aantal bezoeken, maar ook op de manier waarop de containers van het bezoekensegment worden geëvalueerd en op de logica voor het verlopen van bezoeken voor alle eVars die tijdens het bezoek verlopen. Als u de time-out van het bezoek verlaagt, neemt het totale aantal bezoeken in uw rapportage waarschijnlijk toe, terwijl een langere time-out van het bezoek het totale aantal bezoeken in uw rapportage waarschijnlijk zal verminderen.
* **[!UICONTROL Mobile App Visit Settings]:** Voor rapportsuites met gegevens die zijn gegenereerd door mobiele apps via de [Adobe mobiele SDK&#39;s](https://experienceleague.adobe.com/docs/mobile.html), zijn er aanvullende bezoekinstellingen beschikbaar. Deze instellingen zijn niet-destructief en hebben alleen invloed op treffers die zijn verzameld via de mobiele SDK&#39;s. Deze instellingen zijn niet van invloed op gegevens die buiten de SDK voor mobiele apparaten worden verzameld.
* **[!UICONTROL Prevent Background Hits from starting a new Visit]:** Achtergrondhits worden verzameld door de SDK&#39;s van mobiele apparaten wanneer de toepassing zich in de achtergrondstatus bevindt.
* **[!UICONTROL Start a New Visit upon each App Launch]:** Naast de time-out bij een bezoek kunt u een bezoek forceren om te beginnen wanneer een gebeurtenis App Launch is opgenomen vanuit de SDK&#39;s voor mobiele apparaten, ongeacht het inactiviteitsvenster. Dit het plaatsen beïnvloedt metrisch bezoek en de container van het bezoekensegment, evenals de logica van de bezoekafloop op eVars.
* **[!UICONTROL Start New Visit with Event]:** Een nieuwe sessie wordt gestart wanneer een gebeurtenis wordt geactiveerd, ongeacht of er een time-out voor een sessie is opgetreden. De nieuwe sessie bevat de gebeurtenis die deze heeft gestart. Bovendien kunt u meerdere gebeurtenissen gebruiken om een sessie te starten en een nieuwe sessie wordt geactiveerd als een van deze gebeurtenissen in de gegevens wordt waargenomen. Dit het plaatsen zal uw bezoektelling, de container van de de segmentatie van het bezoek, en de logica van de bezoekafloop op eVars beïnvloeden.

Hier is een video over het starten van een nieuw bezoek met de gebeurtenis:

>[!VIDEO](https://video.tv.adobe.com/v/23129/?quality=12)

## Beperkingen van tijdverwerking rapporteren

De Verwerking van de Tijd van het rapport steunt niet alle metriek en dimensies beschikbaar in traditionele Analytics rapportering. Virtuele rapportsuites die de Verwerking van de Tijd van het Rapport gebruiken zijn slechts toegankelijk in Analysis Workspace en is niet toegankelijk in Data Warehouse, Report Builder, Gegevensvoer, of rapporteringsAPI.

Bovendien verwerkt de Tijd van het Rapport slechts gegevens die uit binnen de rapporteringsdatumwaaier (die als &quot;datumvenster&quot;hieronder wordt bedoeld) komen. Dit betekent dat de waarden van eVar die voor een bezoeker vóór de rapporteringsdatumwaaier worden geplaatst &quot;nooit verlopen&quot;niet in de rapporteringsvensters blijven en niet in rapporten verschijnen. Dit betekent ook dat de metingen van de klantenloyaliteit uitsluitend gebaseerd zijn op de gegevens in de rapporteringsdatumwaaier en niet op de volledige geschiedenis voorafgaand aan de rapporteringsdatumwaaier.

De volgende afmetingen en metriek worden niet gesteund met de Verwerking van de Tijd van het Rapport:

* **Analyses voor doel**
* **Analyses voor Advertising Cloud-afmetingen/metriek**
* **Counter Vars**
* [**Dagen voor eerste aankoop**](/help/components/dimensions/days-before-first-purchase.md)
* [**Dagen sinds laatste aankoop**](/help/components/dimensions/days-since-last-purchase.md)
* [**Dagen sinds laatste bezoek**](/help/components/dimensions/days-since-last-visit.md)
* **Origineel van invoerpagina**
* **Lineaire toewijzing Vars**
* **Lijstvars**
* [**Afmetingen marketingkanalen**](/help/components/dimensions/marketing-channel.md)
* [**Oorspronkelijk referentiedomein**](/help/components/dimensions/original-referring-domain.md)
* [**Retourfrequentie**](/help/components/dimensions/return-frequency.md)
* [**Eenvoudige toegang*](/help/components/metrics/single-access.md)
* **Gegevensbronnen van transactie-id**
* [**Bezoek nummer**](/help/components/dimensions/visit-number.md)

## Betrokken afmetingen en metriek

Hieronder volgt een lijst van afmetingen en metriek die afhankelijk van de geselecteerde montages van de Verwerking van de Tijd van het Rapport worden beïnvloed:

* Als &quot;Voorkomen dat de Hits van de Achtergrond van een Nieuw Bezoek&quot;wordt toegelaten, komen de volgende veranderingen voor. Zie [Contextbewuste sessionisatie](vrs-mobile-visit-processing.md) voor meer informatie .
   * [**Bounces**](/help/components/metrics/bounces.md) / [**Stuitsnelheid:**](/help/components/metrics/bounce-rate.md) Achtergrondresultaten die niet worden gevolgd door een treffer op de voorgrond, worden niet beschouwd als een stuit en dragen niet bij aan de stuiterende waarde.
   * [**Tijd in seconden per bezoek:**](/help/components/metrics/time-spent-per-visit.md) Alleen bezoeken die voorgrondhits bevatten, dragen bij aan deze meting.
   * **Tijd besteed per bezoek:** Alleen bezoeken die voorgrondhits bevatten, dragen bij aan deze meting.
   * [**Invoer metrisch**](/help/components/metrics/entries.md) / [**Metrisch afsluiten:**](/help/components/metrics/exits.md) In deze dimensie worden alleen items en uitgangen van bezoeken met voorgrondhits weergegeven.
   * [**Dimensie item**](/help/components/dimensions/entry-dimensions.md) / [**Afmetingen afsluiten:**](/help/components/dimensions/exit-dimensions.md) In deze dimensie worden alleen items en uitgangen van bezoeken met voorgrondhits weergegeven.
   * [**Unieke metrische bezoekers:**](/help/components/metrics/unique-visitors.md) Unieke bezoekers nemen geen bezoekers op die alleen achtergrondtreffers hadden in het bereik van de rapportdatum.
* [**Bezoeken:**](/help/components/metrics/visits.md) De bezoeken weerspiegelen welke montages de virtuele rapportreeks heeft gevormd, die van de reeks van het basisrapport kan verschillend zijn.
* **Geserialiseerde gebeurtenissen met gebeurtenis-id&#39;s:** Gebeurtenissen die gebruikmaken van serienummering van gebeurtenissen met een gebeurtenis-id, worden alleen gededupliceerd voor gebeurtenissen die binnen het bereik van de rapportdatum voor een bezoeker plaatsvinden. Deze gebeurtenissen worden niet over alle datums of bezoekers globaal als gevolg van het venster Datum van de Verwerking van de Tijd van het Rapport gededupliceerd.
* **Aankopen** / [**Ontvangsten**](/help/components/metrics/revenue.md) / [**Orders**](/help/components/metrics/orders.md) / [**Eenheden:**](/help/components/metrics/units.md) Wanneer de aankoop-id wordt gebruikt, worden deze metriek alleen gededupliceerd voor dubbele aankoop-id&#39;s die binnen het bereik van de rapportdatum voor een bezoeker voorkomen in plaats van voor alle datums of bezoekers over de hele wereld vanwege het venster Datum van rapporttijdverwerking.
* [**Niet-verkoopbare variabelen**](/help/components/dimensions/evar.md) / **gereserveerde eVars:** Waarden die in een eVar zijn ingesteld, blijven alleen behouden als de waarde binnen het bereik van de rapportdatum is ingesteld vanwege het venster Tijdverwerkingsdatum rapporteren. Bovendien kunnen op tijd gebaseerde vervaldatums een uur vroeg of een uur laat verlopen als de persistentie een zomertijdwijziging omvat.
* [**Merchandising Vars**](/help/components/dimensions/evar-merchandising.md) / **gereserveerde eVars:** Zie hierboven. Daarnaast wordt voor de conversiesyntaxis, waarbij de binding is ingesteld op &quot;een gebeurtenis&quot;, in plaats daarvan &quot;een hit&quot; gebruikt.
* [**Type hit:**](/help/components/dimensions/hit-type.md) Deze dimensie geeft aan of een hit op de voor- of achtergrond staat.
* **Dimensionen met (laag verkeer) of &quot;Uniques Exceeded&quot;:** Het (Laag-verkeer) lijnpunt wordt bepaald lichtjes verschillend wanneer het gebruiken van de Verwerking van de Tijd van het Rapport, en is gewaarborgd niet om te passen wat wanneer het melden op de Reeks van het basisrapport wordt waargenomen. De lijnpunten van het Dimension die geen deel van Laag-verkeer uitmaken worden gegarandeerd niet 100% van de gegevens voor dat lijnpunt vertegenwoordigen. Deze verschillen kunnen groter worden naarmate het aantal unieke waarden in een dimensie groter wordt.
