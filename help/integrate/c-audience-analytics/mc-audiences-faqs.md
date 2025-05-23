---
description: Antwoorden op vragen die u zou kunnen hebben wanneer het uitvoeren van Audience Analytics.
solution: Experience Cloud
title: Veelgestelde vragen voor Audience Analytics
feature: Audience Analytics
exl-id: 86e7967c-030c-44d6-8294-e7e6d41f6fc3
source-git-commit: 750c4b0ffb52c3f2cf25abcd76ef149a4521109e
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 0%

---

# Veelgestelde vragen

Antwoorden op vragen die u zou kunnen hebben wanneer het uitvoeren van Audience Analytics.

## Veelgestelde vragen over wetgeving {#legal}

+++ Hoe weet ik of ik persoonlijk Identificeerbare Informatie (PII) in mijn Analytische gegevens heb? Zo ja, wat doe ik eraan?

Als u e-mails/adressen/etc. in een hulpmiddel of eVar hebt, denk na hashing de gegevens tijdens inzameling. Als uw land IP adres als PII beschouwt, [IP-verduistering inschakelen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/exclude-ip.html?lang=nl-NL). Bespreek met uw Analysebeheerder wat u verzamelt. Bespreek met uw Juridische Dienst wat zij als PII beschouwen.

+++

+++ Hoe weet ik of mijn rapportsuites onsite personalisatie, of offsite/onsite het richten doen?

Dit geldt niet voor het verzenden van Adobe Analytics-gegevens naar Adobe Audience Manager. Vraag het uzelf:

* Wilt u een Analytics-gedeeld segment met een dimensie MCA terug naar het Experience Cloud delen?

* Exporteert u (bijvoorbeeld via gegevensfeeds) naar een Business Intelligence (BI)-systeem dat voor deze doeleinden wordt gebruikt?

+++

## Adobe Audience Manager-specifieke veelgestelde vragen {#aam-specific}

+++ Hoe creeer ik een bestemming van Analytics in Audience Manager?

Zie [Een analysedoel configureren in Adobe Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html?lang=nl-NL)&quot;.

+++

+++ Hoe lang duurt het nadat u een analysedoel hebt gemaakt en opgeslagen, totdat er gegevens in mijn geselecteerde rapportsuite worden weergegeven?

Het kan enkele uren duren om nieuwe gegevens in uw rapportensuites te plaatsen.

+++

+++ Ik heb een nieuwe bestemming van Analytics gecreeerd, maar ik zie het niet in de sectie van Toewijzingen van de Bestemming van mijn beschikbare segmenten. Waar ging die bestemming heen of hoe vind ik het?

Een bestemming Analytics verdwijnt uit de sectie van de Toewijzingen van de Bestemming van een segment wanneer u selecteert **[!UICONTROL Automatically map all current and future segments]** optie in **[!UICONTROL Segment Mappings]**. Selecteer **[!UICONTROL Manually map segments]** in plaats van de automatische optie.

+++

Zal ik hier alle informatie van Adobe Audience Manager, in Analytics krijgen?

Nr, slechts gegevens met betrekking tot mensen die aan uw plaats tijdens of na het inschakelen van het Publiek van de Audience Manager en tijdens/na segmentkwalificatie komen.

+++

+++ Zal dit me een per-segment totaal adresseerbaar publiek geven?

Niet echt. Het zal u het aantal bezoekers in dat segment vertellen die aan uw plaats tijdens of na segmentkwalificatie kwamen.

+++

+++ Hoe verschilt dit van de oude cookie bestemming tot Analytics?

Segmenten worden gekwalificeerd voor en geretourneerd in real-time - op dezelfde hit. Vriendelijke namen worden automatisch weergegeven.

+++

+++ Wat als sommige van mijn verslagen persoonlijke gegevens hebben en sommigen niet?&lt;

Tip: Maak twee bestemmingen - voeg de reeksen van het persoonlijke gegevensrapport aan één bestemming toe en de reeksen van het niet-persoonlijke gegevensrapport aan andere.

+++

## Analytische specifieke veelgestelde vragen {#aa-specific}

+++ Zal dit integratieoppervlak een dimensie of segment zijn in Analytics?

Als afmetingen: publiek-id en naam publiek.

+++

+++Waar kan ik deze afmetingen in Analytics gebruiken?

Overal; ze worden behandeld net als elke andere dimensie die in Analytics wordt verzameld.

+++

+++ Waarom zie ik geen gegevens die in Analytics komen?

U hebt waarschijnlijk conflicterende Adobe Audience Manager-privacybesturingselementen tussen gegevensbron en doel.

+++

+++ Waarom ontbreken sommige van mijn segmenten in Analytics, hoewel ik verkoos om alle segmenten te verzenden?&lt;

* Uw Adobe Audience Manager-besturingselementen voor gegevensuitvoer op de bestemming en in de gegevensbronnen van de segmenten zijn mogelijk tegenstrijdig, waardoor bepaalde segmenten niet kunnen worden verzonden.

* Als u de eigenschappen van derdegegevens in uw segmenten gebruikt, kunnen die segmenten niet aan bestemmingen (een reeks rapportreeksen) worden gedeeld die persoonlijke gegevens bevatten.

+++

+++ Waarom zie ik &quot;Audience limit Rebage&quot; in mijn Analytics-rapport? (Opmerking: dit wordt ook weergegeven als Audience ID = -1 en `::max_audiences_exceeded::` in Data Warehouse)

Door gebrek, verzendt de Audience Analytics integratie voor Adobe Audience Manager alle segmenten die een bezoeker voor, op een per-raakbasis, aan Analytics kwalificeert. Als een bezoeker tot meer dan 150 segmenten van Adobe Audience Manager op één hit behoort, **150 meest recente gekwalificeerde segmenten** worden verzonden naar Analytics, terwijl de resterende lijst wordt afgekapt. Een extra vlag wordt verzonden naar Analytics die erop wijst dat de segmentlijst werd beknot, en vertoningen zoals &quot;de grens van het publiek bereikte&quot;in de dimensie van de Naam van het Publiek en &quot;-1&quot;in de dimensie van identiteitskaart van het Publiek.

Hoewel het onwaarschijnlijk is dat een bezoeker bij een bepaald resultaat voor meer dan 150 segmenten in aanmerking komt, kan dit een klein percentage van de tijd zijn. Als de limiet van het publiek is bereikt in de rapportage, hebt u twee opties:

* Optie 1: Blijf de integratie laten werken in zijn uit-van-de-doos staat, die de 150 onlangs gekwalificeerde segmenten voor een bepaalde bezoeker verzendt.

* Optie 2: In Adobe Audience Manager kiest u de 150 segmenten die voor uw bedrijf het belangrijkst zijn voor de integratie. Adobe Audience Manager controleert vervolgens alleen bezoekers op die 150 segmenten. Het nadeel van deze benadering is dat u slechts die 150 segmenten over alle bezoekers ontvangt. Anderzijds kan de Optie 1-benadering onbeperkte segmenten bieden vanwege het per-raaktype van de integratie.

+++

+++ Zullen extra servervraag aan Analytics voor deze integratie in rekening worden gebracht?

Nee. Adobe Audience Manager-soorten publiek worden opgenomen in de detectieserver van Analytics. Dit veroorzaakt geen extra servervraag aan (primaire of secundaire) Analytics.

+++

## Veelgestelde vragen over doorsturen op de server (SSF) {#SSF}

+++ Als ik oudere SSF heb uitgevoerd, moet ik ook naar Analytics Admin gaan en rapportsuite SSF inschakelen?

Ja. In de de bestemmingsopstelling van Adobe Audience Manager, zult u slechts rapportsuites zien die SSF hebben aangezet.

+++

+++ Waarom kan ik niet bepaalde rapportsuites voor SSF in Analytics Admin aanzetten?

Alleen suites die zijn toegewezen aan uw Experience Cloud Org kunnen worden ingeschakeld.

Zie voor meer veelgestelde vragen over dit onderwerp [Veelgestelde vragen over doorsturen op de server](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-faq.md).

+++

## Algemene veelgestelde vragen {#section_E55410BBFB624AAFB87ADCF7F036DDA3}

+++ Waarom telt de segmentbezoeker verschillend tussen Audience Manager en Analytics?

Zie [Verschillen in aantal bezoekers](/help/integrate/c-audience-analytics/visitor-count-reconciliation.md).

+++

+++ Wat is het verschil tussen &quot;publiek&quot; in Adobe Audience Manager en &quot;segmenten&quot; in Analytics?

Zie [Segmenten begrijpen in Analytics en Audience Manager](/help/integrate/c-audience-analytics/aam-analytics-segments.md). Het Adobe Audience Manager-publiek wordt verzonden en gedeeld als &#39;dimensie&#39;-componenten die in Analytics moeten worden gebruikt. Zij verschijnen niet als segmenten in de Bouwer van het Segment, bijvoorbeeld, maar als afmetingen die u segmenten kunt bouwen met.

+++

+++ Wat is het verschil tussen klantkenmerken en klantgegevens die vanuit Adobe Audience Manager zijn geïntegreerd?

Kenmerken van de klant zijn niet op tijd gebaseerd; ze zijn retroactief van toepassing en gaan door. Geïntegreerde Adobe Audience Manager-gegevens zijn alleen op tijd gebaseerd en gaan door. Bovendien, zijn de klantenattributen een raadplegingstabel voor Experience Cloud bezoeker IDs, terwijl de integratie van Adobe Audience Manager gegevens is die in elke slag voor een bezoeker worden vastgemaakt.

+++

+++ Hoe zit het met de oude aanpak van dit probleem, bijvoorbeeld de oude bèta- of Consulting-plug-in cookie-bestemmingen?

Wij adviseren dat u de nieuwe integratie uitvoert en oude bestemmingen verwijdert.

+++
