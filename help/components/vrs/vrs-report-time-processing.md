---
description: De tijdverwerking van het rapport is een virtuele het rapportreeks plaatsen die gegevens om op een niet destructieve, retroactieve manier toelaat worden verwerkt.
title: Verwerking rapportduur
uuid: 1a1d82ea-8c93-43cc-8689-cdcf59c309b1
exl-id: 3742b9d1-f1fb-4690-bd44-b4719ff9d9bc
source-git-commit: 3867573780a791ec4cf2b2ceda33707d972f3f5c
workflow-type: tm+mt
source-wordcount: '1419'
ht-degree: 0%

---

# Verwerking rapportduur

De tijdverwerking van het rapport is een virtuele het rapportreeks plaatsen die gegevens om op een niet destructieve, retroactieve manier toelaat worden verwerkt.

>[!NOTE]
>
>Verwerking van rapporttijd is alleen beschikbaar voor Analysis Workspace.

De Verwerking van de Tijd van het rapport beïnvloedt slechts de gegevens in de virtuele rapportreeks en beïnvloedt geen gegevens of gegevensinzameling in de reeks van het basisrapport. Het verschil tussen de Verwerking van de Tijd van het Rapport en de traditionele verwerking van Analytics wordt het best begrepen gebruikend het volgende diagram:

![Google1](assets/google1.jpg)

Tijdens de gegevensverwerking van Analytics, stromen de gegevens door de pijpleiding van de gegevensinzameling en in een preprocessing stap, die gegevens voor rapportering voorbereidt. Bij deze voorbewerkingsstap worden de logica voor het verlopen van het bezoek en de persistentielogica van de eVar toegepast (onder andere) op de gegevens terwijl deze worden verzameld. Het primaire nadeel van dit voorbewerkingsmodel is dat elke configuratie vooraf moet worden uitgevoerd voordat gegevens worden verzameld. Dit betekent dat wijzigingen in de instellingen voor voorbewerking alleen van toepassing zijn op nieuwe gegevens vanaf dat moment. Dit is problematisch als de gegevens uit orde aankomen of als de montages verkeerd werden gevormd.

De Verwerking van de Tijd van het rapport is een fundamenteel verschillende manier om de gegevens van Analytics voor rapportering te verwerken. In plaats van de verwerkingslogica vooraf te bepalen alvorens de gegevens worden verzameld, negeert de Analytics de gegevensreeks tijdens de preprocessing stap en past deze logica toe telkens als een rapport wordt in werking gesteld:

![Google2](assets/google2.jpg)

Deze verwerkingsarchitectuur maakt veel flexibelere rapportageopties mogelijk. Bijvoorbeeld, kunt u de periode van de bezoekonderbreking in om het even welke tijdsduur veranderen u op een niet destructieve manier wilt en die veranderingen worden weerspiegeld in uw persistentie en segmentcontainers retroactief alsof u die montages had toegepast alvorens de gegevens werden verzameld. Bovendien, kunt u om het even welk aantal virtuele rapportreeksen tot stand brengen, elk met de verschillende opties van de Verwerking van de Tijd van het Rapport die op de zelfde reeks van het basisrapport worden gebaseerd, zonder om het even welke gegevens in de reeks van het basisrapport te veranderen.

De Verwerking van de Tijd van het rapport staat ook Analytics toe om achtergrondklappen te verhinderen nieuwe bezoeken te beginnen en staat [mobiele SDK](https://www.adobe.io/apis/cloudplatform/mobile.html) toe om rapportering te vertellen om een nieuw bezoek te beginnen wanneer een gebeurtenis van de Lancering van de App wordt teweeggebracht.

De volgende configuratieopties zijn momenteel beschikbaar aan virtuele rapportreeksen met toegelaten de Verwerking van de Tijd van het Rapport:

* **Time-out bij bezoek:** de time-out bij bezoek bepaalt de hoeveelheid inactiviteit die een unieke bezoeker moet hebben voordat een nieuw bezoek automatisch wordt gestart. De standaardwaarde is 30 minuten. Als u de time-out van het bezoek bijvoorbeeld instelt op 15 minuten, wordt een nieuwe bezoekgroep gemaakt voor elke reeks verzamelde hits, gescheiden door 15 minuten inactiviteit. Deze instelling is niet alleen van invloed op uw aantal bezoeken, maar ook op de manier waarop de containers van het bezoekensegment worden geëvalueerd en op de logica voor het verlopen van bezoeken voor alle eVars die tijdens het bezoek verlopen. Als u de time-out van het bezoek verlaagt, neemt het totale aantal bezoeken in uw rapportage waarschijnlijk toe, terwijl een langere time-out van het bezoek het totale aantal bezoeken in uw rapportage waarschijnlijk zal verminderen.
* **Bezoek instellingen mobiele app:** voor rapportsuite met gegevens die zijn gegenereerd door mobiele apps via de SDK&#39;s van  [Adobe Mobile SDK](https://www.adobe.io/apis/cloudplatform/mobile.html), zijn extra bezoek-instellingen beschikbaar. Deze instellingen zijn niet-destructief en hebben alleen invloed op treffers die zijn verzameld via de mobiele SDK&#39;s. Deze instellingen zijn niet van invloed op gegevens die buiten de SDK voor mobiele apparaten worden verzameld.
* **Voorkomen dat op de achtergrond uitgevoerde Hits een nieuw bezoek begint:** achtergrondtreffers worden verzameld door de mobiele SDK&#39;s wanneer de toepassing zich in de achtergrondstatus bevindt.
* **Start een nieuw bezoek bij elke App Launch:** Naast de time-out van het bezoek kunt u een bezoek afdwingen om te beginnen wanneer een App Launch-gebeurtenis is opgenomen vanuit de mobiele SDK&#39;s, ongeacht het inactiviteitsvenster. Dit het plaatsen beïnvloedt metrisch bezoek en de container van het bezoekensegment, evenals de logica van de bezoekafloop op eVars.
* **Nieuwe bezoeker starten met gebeurtenis:** een nieuwe sessie start wanneer een gebeurtenis wordt geactiveerd, ongeacht of er een time-out voor een sessie is opgetreden. De nieuwe sessie bevat de gebeurtenis die deze heeft gestart. Bovendien kunt u meerdere gebeurtenissen gebruiken om een sessie te starten en een nieuwe sessie wordt geactiveerd als een van deze gebeurtenissen in de gegevens wordt waargenomen. Dit het plaatsen zal uw bezoektelling, de container van de de segmentatie van het bezoek, en de logica van de bezoekafloop op eVars beïnvloeden.

De Verwerking van de Tijd van het rapport steunt niet alle metriek en dimensies beschikbaar in traditionele Analytics rapportering. Virtuele rapportsuites die de Verwerking van de Tijd van het Rapport gebruiken zijn slechts toegankelijk in Analysis Workspace en is niet toegankelijk in [!UICONTROL Reports & Analytics], Data Warehouse, Report Builder, Gegevensvoer, of rapporteringsAPI.

Bovendien verwerkt de Tijd van het Rapport slechts gegevens die uit binnen de rapporteringsdatumwaaier (die als &quot;datumvenster&quot;hieronder wordt bedoeld) komen. Dit betekent dat de waarden van de eVar die aan &quot;nooit verlopen&quot;voor een bezoeker vóór de rapporteringsdatumwaaier worden geplaatst niet in de rapporteringsvensters blijven en niet in rapporten verschijnen. Dit betekent ook dat de metingen van de klantenloyaliteit uitsluitend gebaseerd zijn op de gegevens in de rapporteringsdatumwaaier en niet op de volledige geschiedenis voorafgaand aan de rapporteringsdatumwaaier.

Hieronder volgt een lijst met metriek en afmetingen die momenteel niet worden ondersteund bij het gebruik van de Verwerking van de Tijd van het Rapport:

* **Analytics for Target:** Momenteel niet ondersteund. Toekomstige steun is gepland.
* **Analyse voor voor Advertising Cloud gereserveerde metriek/afmetingen:** momenteel niet ondersteund. Toekomstige steun is gepland.
* **Single Access Metric:** Permanent niet ondersteund.
* **List Vars:** momenteel niet ondersteund. Toekomstige steun is gepland.
* **Counter eVars:** Permanent niet ondersteund.
* **Variabelen voor marketingkanalen:** momenteel niet ondersteund. Toekomstige steun is gepland.
* **Dagen sinds laatste aankoop Dimension:** vanwege de aard van het venster Verwerkingsdatum rapporttijd, wordt deze dimensie niet ondersteund.
* **Dagen voor eerste aankoop Dimension:** Vanwege de aard van het venster Verwerkingsdatum rapporttijd wordt deze dimensie niet ondersteund.
* **De Dimension van de Frequentie van de terugkeer:** wegens de aard van het venster van de Datum van de Verwerking van de Tijd van het Rapport, wordt deze afmeting niet gesteund. Een alternatieve benadering die metrische meting van de bezoektelling in een segment gebruikt is mogelijk, of gebruikend bezoek metrisch in een histogramrapport.
* **Dagen sinds laatste bezoek Dimension:** vanwege de aard van het venster Verwerkingsdatum rapporttijd wordt deze dimensie niet ondersteund.
* **Invoer pagina Originele Dimension:** vanwege de aard van het venster Verwerkingsdatum rapporttijd wordt deze dimensie niet ondersteund.
* **Lineaire toewijzingsvariabelen:** momenteel niet ondersteund. Toekomstige steun is gepland.
* **Oorspronkelijk verwijzend domein Dimension:** momenteel niet ondersteund. Toekomstige steun is gepland.
* **Bezoek Aantal:** wegens de aard van het venster van de Datum van de Verwerking van de Tijd van het Rapport, wordt deze metrisch niet gesteund. Als alternatief voor mobiele apps kunt u een berekende maatstaf gebruiken, inclusief bezoekers/bezoeken met de installatiemethode van de app om nieuwe bezoekers of bezoeken te identificeren.
* **Gegevensbronnen van transactie-id:** momenteel niet ondersteund. Toekomstige steun is gepland.

Hieronder volgt een lijst van afmetingen en metriek die afhankelijk van de geselecteerde montages van de Verwerking van de Tijd van het Rapport worden beïnvloed:

* Als &quot;Voorkomen dat de Hits van de Achtergrond van een Nieuw Bezoek&quot;wordt toegelaten, komen de volgende veranderingen voor. Zie [Contextbewuste sessionisatie](vrs-mobile-visit-processing.md) voor meer informatie.
   * **Stuiterwaarden/Stuitsnelheid:** Achtergrondresultaten die niet worden gevolgd door een voorgrondhit, worden niet als stuit beschouwd en dragen niet bij aan de stuitsnelheid.
   * **Tijd besteed seconden per bezoek:** Alleen bezoeken die voorgrondhits bevatten, dragen bij aan deze meting.
   * **Tijd besteed per bezoek:** Alleen bezoeken die voorgrondhits bevatten, dragen bij aan deze meting.
   * **Dimension en metriek voor in- en uitschakelen:** Alleen items en uitgangen van bezoeken met voorgrondhits worden in deze dimensie weergegeven.
   * **Unieke metagegevens van bezoekers:** Unieke bezoekers omvatten geen bezoekers die alleen achtergrondtreffers hadden in het bereik van de rapportdatum.
* **Bezoekingen:** Bezoeken weerspiegelt de instellingen die de virtuele rapportsuite heeft geconfigureerd, die kunnen verschillen van de set met basisrapporten.
* **Geserialiseerde gebeurtenissen met gebeurtenis-id&#39;s:** Gebeurtenissen die gebruikmaken van serialisatie van gebeurtenissen met een gebeurtenis-id, worden alleen gededupliceerd voor gebeurtenissen die binnen het bereik van de rapportdatum voor een bezoeker plaatsvinden. Deze gebeurtenissen worden niet over alle datums of bezoekers globaal als gevolg van het venster Datum van de Verwerking van de Tijd van het Rapport gededupliceerd.
* **Aankopen/Opbrengsten/Orders/Eenheden:** Wanneer de aankoop-id wordt gebruikt, worden deze cijfers alleen gededupliceerd voor dubbele aankoop-id&#39;s die binnen het bereik van de rapportdatum voor een bezoeker voorkomen, in plaats van voor alle datum of bezoekers, globaal vanwege het venster Datum van rapporttijdverwerking.
* **Niet-commerciële eVars/gereserveerde eVars:** Waarden die in een eVar zijn ingesteld, blijven alleen bestaan als de waarde binnen het bereik van de rapportdatum is ingesteld vanwege het venster Tijdverwerkingsdatum rapporteren. Bovendien kunnen op tijd gebaseerde vervaldatums een uur vroeg of een uur laat verlopen als de persistentie een zomertijdwijziging omvat.
* **Merchandising Vars/reserved Vars:** Zie hierboven. Daarnaast wordt voor de conversiesyntaxis, waarbij de binding is ingesteld op &quot;een gebeurtenis&quot;, in plaats daarvan &quot;een hit&quot; gebruikt.
* **Type hoogte:** deze dimensie geeft aan of een hit op de voor- of achtergrond staat.
