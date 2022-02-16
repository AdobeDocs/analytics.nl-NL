---
description: Om te verifiëren dat Server-kant het door:sturen behoorlijk wordt toegelaten, zult u de reactie van HTTP van het Analytics volgende verzoek moeten inspecteren. Dit kan worden gedaan gebruikend de de ontwikkelaarshulpmiddelen van browser of door een het proxying hulpmiddel zoals Debugger van het Web te gebruiken Charles. De volgende instructies illustreren welke indicatoren aanwezig moeten zijn om server-kant het door:sturen behoorlijk toegelaten te verzekeren.
solution: Analytics
title: Implementatie van server-side doorsturen controleren
feature: Server-Side Forwarding
exl-id: 21db4572-da3c-43aa-a774-86a089656695
source-git-commit: ee56267979979f8e03b1c6a0d849ccf994599024
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 5%

---

# Implementatie van server-side doorsturen controleren

Om te verifiëren dat Server-kant het door:sturen behoorlijk wordt toegelaten, zult u de reactie van HTTP van het Analytics volgende verzoek moeten inspecteren. Dit kan worden gedaan gebruikend de de ontwikkelaarshulpmiddelen van browser of door een het proxying hulpmiddel zoals Debugger van het Web te gebruiken Charles. De volgende instructies illustreren welke indicatoren aanwezig moeten zijn om server-kant het door:sturen behoorlijk toegelaten te verzekeren.

Om de status van server-zijhet door:sturen te controleren:

1. Laad een testpagina die bijgewerkte code AppMeasurement bevat.
1. Controleer in de foutopsporingsprogramma&#39;s van uw browser of met behulp van uw proxysoftware de HTTP-reactie van de traceringsaanvraag van Analytics (u kunt dit eenvoudig filteren door een pad met &quot;b/ss&quot; te selecteren).
1. Inspect the HTTP response. Als de reactie Audience Manager gegevens (zoals hieronder geïllustreerd) bevat, dan server-zijhet door:sturen werkt.

![](assets/ssf-succeed.png)

>[!CAUTION]
>
>Als de reactie het sleutelwaardepaar bevat `"status":"SUCCESS"` of een 2 x 2 beeld, dan server-zijdoor:sturen * wordt niet* correct gevormd. Gelieve te zorgen ervoor dat de Dienst van de Identiteit behoorlijk wordt opgesteld, hebt u de module van de Meting van de App opgesteld, dat de toepasselijke rapportreeks aan correcte IMS Org in kaart is gebracht, en dat server-zijhet door:sturen in de Analytics admin console is toegelaten.

>[!MORELIKETHIS]
>
>* [Charles Web Debugger](https://www.charlesproxy.com/)

