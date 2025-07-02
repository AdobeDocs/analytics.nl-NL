---
description: Veelgestelde vragen over Workspace
title: Veelgestelde vragen
feature: Workspace Basics
role: User, Admin
exl-id: cf7a9a73-bcbe-4bf5-b5dc-913199ab229c
source-git-commit: d37fa0aff0b1bbe196b943bc26e86b1e79936184
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 25%

---

# Veelgestelde vragen

+++Wat zijn de eerste vereisten voor het gebruik van Analysis Workspace?
[ verzendt gegevens naar Adobe Analytics gebruikend de uitbreiding van Adobe Analytics ](/help/implement/launch/validate-publish-prod.md): Het gebruiken van Analysis Workspace vereist een werkende implementatie. Zorg ervoor dat uw organisatie gegevens naar Adobe verzendt voordat u het hulpprogramma gebruikt. Andere implementaties, zoals oudere handmatige implementaties, kunnen ook werken.
+++

+++Wat zijn het Beleid en de toegangseisen voor Analysis Workspace?
Zie [ Vereisten van het Beleid ](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md).
+++

+++Zal Analysis Workspace invloed hebben op gegevensverzameling?
Aangezien Analysis Workspace een rapportagetool is, heeft de tool geen invloed op de dataverzameling. U kunt componenten lukraak naar een project slepen om te zien wat er gebeurt, zonder negatieve gevolgen. Sleep verschillende combinaties van dimensies en metriek in uw werkruimteproject om te zien wat beschikbaar aan u is. Als u per ongeluk een ongeldige component naar uw Workspace-project sleept of een stap terug wilt gaan, drukt u op Ctrl + Z (Windows) of Cmd + Z (Mac) om de laatste uitgevoerde actie ongedaan te maken. U kunt ook met een schone lei beginnen door in het menu linksboven te klikken op **[!UICONTROL Project]** > **[!UICONTROL New]**.
+++

+++Hoeveel rapportsuites kunnen in een project van Analysis Workspace worden getoond?
U kunt projecten in Analysis Workspace met gegevens van meer [ veelvoudige rapportsuites ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/build-workspace-project/multiple-report-suites.html) nu tot stand brengen.
+++

+++Hoe implementeert u Analysis Workspace?
Er is geen speciale implementatie vereist. Analysis Workspace is beschikbaar voor alle bedrijven met Analytics Standard of Premium. Nochtans, zijn de standaardtoestemmingen op inhoud (zoals rapportsuites en projectcomponenten) van toepassing, en voor het leiden en het delen van projecten. Zie [ Vereisten van het Beleid en van de Toegang ](/help/analyze/analysis-workspace/workspace-faq/frequently-asked-questions-analysis-workspace.md).
+++

+++Kan ik Analysis Workspace voor Data Warehouse gebruiken?
Analysis Workspace wordt niet aanbevolen voor het exporteren van bulkgegevens. Het is een visualisatiewerkruimte die dashboardachtige analyseprojecten maakt.
+++

+++Hoe kan ik de prestaties van Analysis Workspace optimaliseren?

Zie [ Optimizing Prestaties ](/help/analyze/analysis-workspace/workspace-faq/optimizing-performance.md).

+++

+++Hoe worden gegevens opgenomen in uw Analysis Workspace-project?

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Gegevens in Analysis Workspace ](https://video.tv.adobe.com/v/31072?quality=12&learn=on){target="_blank"} voor een demo video.

+++

+++Hoe kan ik het gebruik van Workspace volgen?

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Logboek dat ](https://video.tv.adobe.com/v/29768?quality=12&learn=on){target="_blank"} voor een demo video volgt.

+++

+++Wanneer ik metrisch over sleep, zegt het &quot;Ongeldige gegevens&quot;. Hoe los ik dit probleem op?

De melding &quot;Ongeldige data&quot; betekent dat Adobe geen data kan retourneren met de combinatie van dimensies en metrics die in het rapport wordt gebruikt. Zo kunnen twee metrics die boven op elkaar zijn gestapeld, niet als data worden geretourneerd, omdat er geen manier is om twee metrics op die manier weer te geven. Plaats de metriek in plaats daarvan naast elkaar.

+++

+++Wanneer ik metrisch over sleep, zie ik geen daadwerkelijke gegevens - enkel nul. Hoe kan ik dit probleem oplossen?

Als u een werkruimterapport hebt gemaakt maar er geen gegevens zijn, kunt u een aantal dingen controleren:

* Controleer de rapportreeks tweemaal en zorg ervoor het met gegevens wordt bevolkt.
* Als u een segment in uw rapport toepaste, zouden de segmentcriteria geen gegevens kunnen aanpassen. Verwijder het segment of pas de segmentdefinitie aan.
* Controleer de datumwaaier in de hogere juiste hoek en zorg ervoor het aan een waarde wordt geplaatst die u zou verwachten.
* Navigeer aan uw website en gebruik [ Debugger ](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) om te bevestigen dat het gegeven wordt verzameld.


+++

+++Als alleen-lezen gebruiker, welke acties kan ik in Analysis Workspace uitvoeren?
Wanneer een project alleen-lezen wordt gedeeld, zijn alle bewerkingsfuncties en -functies volledig uitgeschakeld en kunnen ontvangers het vervolgkeuzemenu alleen wijzigen om een filter op een vooraf gedefinieerde manier op het deelvenster toe te passen.
+++
