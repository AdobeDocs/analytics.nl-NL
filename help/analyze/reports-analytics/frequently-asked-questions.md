---
description: Verstrekt antwoorden en het oplossen van problemensuggesties aan enkele van de vaakst gestelde vragen van Analytics.
keywords: Analyses voor probleemoplossing
title: Veelgestelde vragen voor rapporten en analyses
feature: Reports & Analytics Basics
role: User, Admin
exl-id: 99702728-971f-484a-91f5-f3210b89485c
source-git-commit: 4ddc2640aa8b3a22411c86ff8bfe0ecf345a3d63
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Veelgestelde vragen

{{ra-eol}}

Verstrekt antwoorden en het oplossen van problemensuggesties aan enkele van de vaakst gestelde vragen van Analytics voor Rapporten &amp; Analytics. Raadpleeg voor veelgestelde implementatievragen het dialoogvenster [Veelgestelde vragen](/help/implement/faq.md) in de gebruikershandleiding Implementeren.

>[!IMPORTANT]
>Effectief **31 december 2023**, is Adobe voornemens de rapporten en analyses en de bijbehorende rapporten en functies te beëindigen. Op dat moment werken de rapporten en analyses en alle bijbehorende rapporten en programma&#39;s niet meer. De rapporten, visualisaties en de onderliggende technologie die de rapporten &amp; Analytics van de macht niet meer aan de technologienormen van Adobe voldoen. De meeste functies voor rapporten en analyses zijn beschikbaar in Analysis Workspace. Sinds de release van Analysis Workspace in 2015 zijn de functionaliteit en mogelijkheden van Rapporten en Analytics verplaatst naar Analysis Workspace en is een drempel voor pariteit van de workflow bereikt. Deze kennisgeving legt het einde van de levensduur uit.

**Mijn account is vergrendeld. hoe ontgrendel ik het?**

Neem contact op met een beheerder binnen uw organisatie om een account opnieuw te activeren. Zie ook [Aanmeldingsproblemen met Adobe Analytics oplossen](/help/technotes/troubleshoot-login.md) in de gebruikershandleiding voor technische notities.

**Waarom zie ik een leeg rapport, ook al weet ik dat er gegevens verzameld zijn?**

Er zijn verscheidene dingen om rapportgegevens problemen op te lossen te controleren:

* Controleer de gebruikte cijfers: In sommige rapporten wordt standaard de waarde Opbrengst in Rapporten en Analyse gebruikt. Zorg metrisch u bekijkt voor het rapport relevant is.
* Controleer het datumbereik: Datumbereiken, met name die buiten het beleid van uw organisatie voor gegevensbehoud, kunnen geen gegevens retourneren. Controleer of het datumbereik juist is ingesteld.
* Interne URL-filters controleren: Sommige rapporten van verkeersbronnen werken pas nadat u de interne filters URL correct hebt gedefinieerd.

**Waarom ontbreken sommige rapporten in het navigatiemenu?**

Rapporten die ontbreken in een menu komen meestal voort uit beperkte machtigingen of menuaanpassingen. Neem contact op met een productbeheerder binnen uw organisatie om ervoor te zorgen dat u toegang hebt tot alle benodigde afmetingen en metriek en dat de menustructuur van een rapportsuite niet is aangepast.

**Waarom worden sommige lange waarden afgesneden?**

Bijna alle variabelen in Adobe Analytics hebben een tekenlimiet. Paginanaam heeft een limiet van 100 tekens, terwijl aangepaste conversievariabelen (eVars) een limiet van 255 tekens hebben. Adobe raadt u aan ervoor te zorgen dat de waarden die u naar Adobe verzendt, beknopt zijn om afkapping te voorkomen.

**Waarom zie ik een grote vertraging in de rapportage?**

Real-time rapportage maakt het mogelijk dat bepaalde verkeersmetriek binnen minuten beschikbaar is, terwijl conversie en andere verwerkingsintensieve gegevens meestal binnen 30-90 minuten beschikbaar zijn. Hoewel het Experience Cloud platform robuust is, zijn er een paar situaties die tot vertragingen in rapportering kunnen leiden. Deze vertraging wordt bedoeld als latentie. Zie [Latentie](/help/technotes/latency.md) in de gebruikershandleiding voor technische notities voor meer informatie.

**Waarom kan ik de apparaatversie niet zien op iPhones?**

Apple-apparaten rapporteren hun firmware-versie in de userAgent-tekenreeks, niet in de apparaatversie. Het is moeilijk om de iPhone-apparaatversie te bepalen aan de hand van informatie die beschikbaar is voor Adobe Analytics. Zie [iPhone-apparaatversies vergelijken](https://helpx.adobe.com/analytics/kb/comparing-iphone-device-versions.html) in de KB Analytics voor meer informatie.

**Waarom komen de totalen onder aan mijn verslag niet overeen wanneer ik de waarden opsommen?**

Dimension-items kunnen vaak op meerdere plaatsen worden toegepast. bijvoorbeeld bezoeken die middernacht omspannen of meerdere producten die tot één bestelling behoren. De dimensie-item wordt gerapporteerd in alle toepasselijke posten, maar wordt gededupliceerd in het totaal van het rapport. Zie [De som van de lijnitems vergelijken om het totaal te rapporteren](https://helpx.adobe.com/analytics/kb/sum-line-items-different-from-total.html) in de KB Analytics voor meer informatie.

**Hoe sluit ik gegevens van een bepaalde IP adressen in mijn rapportreeks uit?**

U kunt gegevens uit interne websiteactiviteiten, zoals site-tests en werknemersgebruik, uit uw rapporten verwijderen. Met deze functie kunnen u en uw collega&#39;s uw site bezoeken zonder uw verkeersgegevens te scheeftrekken. Zie [Exclusief door IP Adres](/help/admin/admin/exclude-ip.md) in de gebruikershandleiding voor Admin voor meer informatie.

**Kan ik een rapportsuite verwijderen?**

Het verwijderen van een rapportsuite is niet mogelijk. Een rapportsuite kan echter voor alle weergaven in Adobe Analytics worden verborgen. Merk op dat de servervraag die naar een verborgen rapportreeks wordt verzonden nog aan uw maandelijkse contractgrens telt. Zie [Rapportagesuites verbergen](/help/admin/company/c-hide-report-suites.md) in de gebruikershandleiding voor Admin voor meer informatie.

**Wanneer het gebruiken van segmentatie, welke container zou ik moeten gebruiken? Paginaweergave, bezoek of bezoeker?**

De segmentcontainer die u gebruikt, is afhankelijk van de breedte waarmee u gegevens wilt vastleggen. De containers van de paginamening brengen slechts in klappen die segmentcriteria aanpassen, nuttig om irrelevante delen van bezoeken uit te filteren. Met Bezoek-containers haalt u alle resultaten van een bezoek bij een of meer treffers die voldoen aan de criteria van een bepaald segment. Dit is handig als u sessies in het algemeen wilt bekijken. Bezoekerscontainers brengen alle bezoeken waar een hit aan segmentcriteria voldeed, nuttig om mensen te bekijken. Het is uw keus als analist om te bepalen welke segmentcontainer best is te gebruiken. Zie [Overzicht van segmentatie](/help/components/segmentation/seg-overview.md) in de gebruikershandleiding van Componenten voor meer informatie.

**Waarom wordt mijn segment niet in de Data Warehouse weergegeven?**

Vanwege de unieke verwerkingsarchitectuur van de Data Warehouse is het platform niet geoptimaliseerd voor het verwerken van bepaalde soorten gegevens, zoals plakken. Zie [Data Warehouse segmentcompatibiliteit](/help/components/segmentation/seg-reference/seg-compatibility.md) in de gebruikershandleiding van Componenten voor meer informatie.
