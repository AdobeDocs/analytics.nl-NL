---
description: Om te verifiëren dat Server-kant het door:sturen behoorlijk wordt toegelaten, zult u de reactie van HTTP van het Analytics volgende verzoek moeten inspecteren. Deze instructies illustreren welke indicatoren aanwezig moeten zijn om server-kant het door:sturen behoorlijk toegelaten te verzekeren.
solution: Analytics
title: Hoe te om uw server-kant te verifiëren die implementatie door:sturen
feature: Server-Side Forwarding
exl-id: 21db4572-da3c-43aa-a774-86a089656695
role: Admin
source-git-commit: def7d071de1765acf524a638a8f8d13ae69e1a1f
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Hoe te om uw server-kant te verifiëren die implementatie door:sturen

Om te verifiëren dat Server-kant het door:sturen behoorlijk wordt toegelaten, zult u de reactie van HTTP van het Analytics volgende verzoek moeten inspecteren. Dit kan worden gedaan gebruikend de de ontwikkelaarshulpmiddelen van browser of door een het proxying hulpmiddel zoals Debugger van het Web te gebruiken Charles. De volgende instructies illustreren welke indicatoren aanwezig moeten zijn om server-kant het door:sturen behoorlijk toegelaten te verzekeren.

Om de status van server-zijhet door:sturen te controleren:

1. Laad een testpagina die bijgewerkte code van het AppMeasurement bevat.
1. Controleer in de foutopsporingsprogramma&#39;s van uw browser of met behulp van uw proxysoftware de HTTP-reactie van de traceringsaanvraag van Analytics (u kunt dit eenvoudig filteren door een pad met &quot;b/ss&quot; te selecteren).
1. Inspect the HTTP response. Als de reactie Audience Manager gegevens (zoals hieronder geïllustreerd) bevat, dan server-zijhet door:sturen werkt.

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/assets/ssf-succeed.png)

>[!CAUTION]
>
>Als de reactie het sleutelwaardepaar bevat `"status":"SUCCESS"` of een 2 x 2 beeld, dan server-zijdoor:sturen * wordt niet* correct gevormd. Gelieve te zorgen ervoor dat de Dienst van de Identiteit behoorlijk wordt opgesteld, hebt u de module van de Meting van de App opgesteld, dat de toepasselijke rapportreeks aan correcte organisatie ID in kaart is gebracht, en dat server-side het door:sturen in de Hulpmiddelen van Analytics Admin is toegelaten.

>[!MORELIKETHIS]
>
>* [Charles Web Debugger](https://www.charlesproxy.com/)
