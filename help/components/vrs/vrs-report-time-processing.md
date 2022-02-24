---
description: De tijdverwerking van het rapport is een virtuele het rapportreeks plaatsen die gegevens om op een niet destructieve, retroactieve manier toelaat worden verwerkt.
title: Verwerking rapportduur
feature: VRS
exl-id: 3742b9d1-f1fb-4690-bd44-b4719ff9d9bc
source-git-commit: df16d37de742d96f66fd74d7a7b47729f0454fd5
workflow-type: tm+mt
source-wordcount: '1396'
ht-degree: 0%

---

# Verwerking rapportduur

[!UICONTROL Report time processing] is een instelling voor een virtuele rapportsuite waarmee gegevens op niet-destructieve, retroactieve wijze kunnen worden verwerkt.

>[!NOTE]
>
>[!UICONTROL Report Time Processing] is alleen beschikbaar voor Analysis Workspace.

[!UICONTROL Report Time Processing] beïnvloedt slechts de gegevens in de virtuele rapportreeks en beïnvloedt geen gegevens of gegevensinzameling in de reeks van het basisrapport. Het verschil tussen [!UICONTROL Report Time Processing] en traditionele analytische verwerking het best wordt begrepen gebruikend het volgende diagram:

![Google1](assets/google1.jpg)

Tijdens de gegevensverwerking van Analytics, stromen de gegevens door de pijpleiding van de gegevensinzameling en in een preprocessing stap, die gegevens voor rapportering voorbereidt. Bij deze voorbewerkingsstap worden de logica voor het verlopen van het bezoek en de persistentielogica van de eVar toegepast (onder andere) op de gegevens terwijl deze worden verzameld. Het primaire nadeel van dit voorbewerkingsmodel is dat elke configuratie vooraf moet worden uitgevoerd voordat gegevens worden verzameld. Dit betekent dat wijzigingen in de instellingen voor voorbewerking alleen van toepassing zijn op nieuwe gegevens vanaf dat moment. Dit is problematisch als de gegevens uit orde aankomen of als de montages verkeerd werden gevormd.

[!UICONTROL Report Time Processing] Dit is een fundamenteel andere manier om analysegegevens voor rapportage te verwerken. In plaats van de verwerkingslogica vooraf te bepalen alvorens de gegevens worden verzameld, negeert de Analytics de gegevensreeks tijdens de preprocessing stap en past deze logica toe telkens als een rapport wordt in werking gesteld:

![Google2](assets/google2.jpg)

Deze verwerkingsarchitectuur maakt veel flexibelere rapportageopties mogelijk. Bijvoorbeeld, kunt u de periode van de bezoekonderbreking in om het even welke tijdsduur veranderen u op een niet destructieve manier wilt en die veranderingen worden weerspiegeld in uw persistentie en segmentcontainers retroactief alsof u die montages had toegepast alvorens de gegevens werden verzameld. Bovendien, kunt u om het even welk aantal virtuele rapportreeksen tot stand brengen, elk met de verschillende opties van de Verwerking van de Tijd van het Rapport die op de zelfde reeks van het basisrapport worden gebaseerd, zonder om het even welke gegevens in de reeks van het basisrapport te veranderen.

[!UICONTROL Report Time Processing] biedt Analytics ook de mogelijkheid om te voorkomen dat achtergrondhits nieuwe bezoeken beginnen en biedt de [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/mobile.html) om te melden dat de rapportage een nieuw bezoek moet starten wanneer een gebeurtenis App Launch wordt gestart.

## Configuratieopties

De volgende configuratieopties zijn momenteel beschikbaar aan virtuele rapportreeksen met toegelaten de Verwerking van de Tijd van het Rapport:

* **[!UICONTROL Visit Timeout]:** De time-outinstelling voor een bezoek definieert de hoeveelheid inactiviteit die een unieke bezoeker moet hebben voordat een nieuw bezoek automatisch wordt gestart. De standaardwaarde is 30 minuten. Als u de time-out van het bezoek bijvoorbeeld instelt op 15 minuten, wordt een nieuwe bezoekgroep gemaakt voor elke reeks verzamelde hits, gescheiden door 15 minuten inactiviteit. Deze instelling is niet alleen van invloed op uw aantal bezoeken, maar ook op de manier waarop de containers van het bezoekensegment worden geëvalueerd en op de logica voor het verlopen van bezoeken voor alle eVars die tijdens het bezoek verlopen. Als u de time-out van het bezoek verlaagt, neemt het totale aantal bezoeken in uw rapportage waarschijnlijk toe, terwijl een langere time-out van het bezoek het totale aantal bezoeken in uw rapportage waarschijnlijk zal verminderen.
* **[!UICONTROL Mobile App Visit Settings]:** Voor rapportsuites met gegevens die zijn gegenereerd door mobiele apps via de [Adobe Mobile SDK&#39;s](https://experienceleague.adobe.com/docs/mobile.html), zijn er aanvullende bezoekinstellingen beschikbaar. Deze instellingen zijn niet-destructief en hebben alleen invloed op treffers die zijn verzameld via de mobiele SDK&#39;s. Deze instellingen zijn niet van invloed op gegevens die buiten de SDK voor mobiele apparaten worden verzameld.
* **[!UICONTROL Prevent Background Hits from starting a new Visit]:** Achtergrondhits worden verzameld door de SDK&#39;s van mobiele apparaten wanneer de toepassing zich in de achtergrondstatus bevindt.
* **[!UICONTROL Start a New Visit upon each App Launch]:** Naast de time-out bij een bezoek kunt u een bezoek forceren om te beginnen wanneer een gebeurtenis App Launch is opgenomen vanuit de SDK&#39;s voor mobiele apparaten, ongeacht het inactiviteitsvenster. Dit het plaatsen beïnvloedt metrisch bezoek en de container van het bezoekensegment, evenals de logica van de bezoekafloop op eVars.
* **[!UICONTROL Start New Visit with Event]:** Een nieuwe sessie wordt gestart wanneer een gebeurtenis wordt geactiveerd, ongeacht of er een time-out voor een sessie is opgetreden. De nieuwe sessie bevat de gebeurtenis die deze heeft gestart. Bovendien kunt u meerdere gebeurtenissen gebruiken om een sessie te starten en een nieuwe sessie wordt geactiveerd als een van deze gebeurtenissen in de gegevens wordt waargenomen. Dit het plaatsen zal uw bezoektelling, de container van de de segmentatie van het bezoek, en de logica van de bezoekafloop op eVars beïnvloeden.

Hier is een video over het starten van een nieuw bezoek met de gebeurtenis:

>[!VIDEO](https://video.tv.adobe.com/v/23129/?quality=12)

## Beperkingen van tijdverwerking rapporteren

De Verwerking van de Tijd van het rapport steunt niet alle metriek en dimensies beschikbaar in traditionele Analytics rapportering. Virtuele rapportsuites die de Verwerking van de Tijd van het Rapport gebruiken zijn slechts toegankelijk in Analysis Workspace en is niet toegankelijk in [!UICONTROL Reports & Analytics], Data Warehouse, Report Builder, Gegevensfeeds of de API voor rapportage.

Bovendien verwerkt de Tijd van het Rapport slechts gegevens die uit binnen de rapporteringsdatumwaaier (die als &quot;datumvenster&quot;hieronder wordt bedoeld) komen. Dit betekent dat de waarden van de eVar die aan &quot;nooit verlopen&quot;voor een bezoeker vóór de rapporteringsdatumwaaier worden geplaatst niet in de rapporteringsvensters blijven en niet in rapporten verschijnen. Dit betekent ook dat de metingen van de klantenloyaliteit uitsluitend gebaseerd zijn op de gegevens in de rapporteringsdatumwaaier en niet op de volledige geschiedenis voorafgaand aan de rapporteringsdatumwaaier.

Hieronder volgt een lijst met metriek en afmetingen die momenteel niet worden ondersteund bij het gebruik van de Verwerking van de Tijd van het Rapport:

* **Analyses voor doel:** Momenteel niet ondersteund. Toekomstige steun is gepland.
* **Analyses voor voor voor Advertising Cloud gereserveerde metriek/afmetingen:** Momenteel niet ondersteund. Toekomstige steun is gepland.
* **Single Access Metric:** Permanent niet ondersteund.
* **Lijstvariabelen:** Momenteel niet ondersteund. Toekomstige steun is gepland.
* **Counter Vars:** Permanent niet ondersteund.
* **Variabelen marketingkanalen:** Momenteel niet ondersteund. Toekomstige steun is gepland.
* **Dagen sinds laatste aankoop Dimension:** Vanwege de aard van het venster Verwerkingsdatum van de Tijd van het Rapport, wordt deze dimensie niet gesteund.
* **Dagen vóór eerste aankoop Dimension:** Vanwege de aard van het venster Verwerkingsdatum van de Tijd van het Rapport, wordt deze dimensie niet gesteund.
* **Dimension van retourfrequentie:** Vanwege de aard van het venster Verwerkingsdatum van de Tijd van het Rapport, wordt deze dimensie niet gesteund. Een alternatieve benadering die metrische meting van de bezoektelling in een segment gebruikt is mogelijk, of gebruikend bezoek metrisch in een histogramrapport.
* **Dagen sinds laatste bezoek Dimension:** Vanwege de aard van het venster Verwerkingsdatum van de Tijd van het Rapport, wordt deze dimensie niet gesteund.
* **Oorspronkelijke Dimension van invoerpagina:** Vanwege de aard van het venster Verwerkingsdatum van de Tijd van het Rapport, wordt deze dimensie niet gesteund.
* **Lineaire toewijzingsvariabelen:** Momenteel niet ondersteund. Toekomstige steun is gepland.
* **Oorspronkelijke Dimension van verwijzend domein:** Momenteel niet ondersteund. Toekomstige steun is gepland.
* **Bezoek nummer:** Vanwege de aard van het venster Verwerkingsdatum van de Tijd van het Rapport, wordt deze metrische waarde niet gesteund. Als alternatief voor mobiele apps kunt u een berekende maatstaf gebruiken, inclusief bezoekers/bezoeken met de installatiemethode van de app om nieuwe bezoekers of bezoeken te identificeren.
* **Gegevensbronnen van transactie-id:** Momenteel niet ondersteund. Toekomstige steun is gepland.

## Betrokken afmetingen en metriek

Hieronder volgt een lijst van afmetingen en metriek die afhankelijk van de geselecteerde montages van de Verwerking van de Tijd van het Rapport worden beïnvloed:

* Als &quot;Voorkomen dat de Hits van de Achtergrond van een Nieuw Bezoek&quot;wordt toegelaten, komen de volgende veranderingen voor. Zie [Contextbewuste sessionisatie](vrs-mobile-visit-processing.md) voor meer informatie .
   * **Bounces/Bounce rate:** Achtergrondresultaten die niet worden gevolgd door een treffer op de voorgrond, worden niet beschouwd als een stuit en dragen niet bij aan de stuiterende waarde.
   * **Tijd in seconden per bezoek:** Alleen bezoeken die voorgrondhits bevatten, dragen bij aan deze meting.
   * **Tijd besteed per bezoek:** Alleen bezoeken die voorgrondhits bevatten, dragen bij aan deze meting.
   * **Dimension en statistieken voor in- en uitstappen:** In deze dimensie worden alleen items en uitgangen van bezoeken met voorgrondhits weergegeven.
   * **Unieke metrische bezoekers:** Unieke bezoekers nemen geen bezoekers op die alleen achtergrondtreffers hadden in het bereik van de rapportdatum.
* **Bezoeken:** De bezoeken weerspiegelen welke montages de virtuele rapportreeks heeft gevormd, die van de reeks van het basisrapport kan verschillend zijn.
* **Geserialiseerde gebeurtenissen met gebeurtenis-id&#39;s:** Gebeurtenissen die gebruikmaken van serienummering van gebeurtenissen met een gebeurtenis-id, worden alleen gededupliceerd voor gebeurtenissen die binnen het bereik van de rapportdatum voor een bezoeker plaatsvinden. Deze gebeurtenissen worden niet over alle datums of bezoekers globaal als gevolg van het venster Datum van de Verwerking van de Tijd van het Rapport gededupliceerd.
* **Aankopen/inkomsten/orders/eenheden:** Wanneer de aankoop-id wordt gebruikt, worden deze metriek alleen gededupliceerd voor dubbele aankoop-id&#39;s die binnen het bereik van de rapportdatum voor een bezoeker voorkomen in plaats van voor alle datums of bezoekers over de hele wereld vanwege het venster Datum van rapporttijdverwerking.
* **Niet-commerciële eVars/gereserveerde eVars:** Waarden die in een eVar zijn ingesteld, blijven alleen behouden als de waarde binnen het bereik van de rapportdatum is ingesteld vanwege het venster Tijdverwerkingsdatum rapporteren. Bovendien kunnen op tijd gebaseerde vervaldatums een uur vroeg of een uur laat verlopen als de persistentie een zomertijdwijziging omvat.
* **Merchandising Vars/reserved Vars:** Zie hierboven. Daarnaast wordt voor de conversiesyntaxis, waarbij de binding is ingesteld op &quot;een gebeurtenis&quot;, in plaats daarvan &quot;een hit&quot; gebruikt.
* **Type hit:** Deze dimensie geeft aan of een hit op de voor- of achtergrond staat.
