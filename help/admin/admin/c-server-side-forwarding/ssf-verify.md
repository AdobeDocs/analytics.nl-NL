---
description: Om te verifiëren dat Server-kant het door:sturen behoorlijk wordt toegelaten, zult u de reactie van HTTP van het Analytics volgende verzoek moeten inspecteren. Dit kan worden gedaan gebruikend de de ontwikkelaarshulpmiddelen van browser of door een het proxying hulpmiddel zoals Debugger van het Web te gebruiken Charles. De volgende instructies illustreren welke indicatoren aanwezig moeten zijn om server-kant het door:sturen behoorlijk toegelaten te verzekeren.
solution: Audience Manager
title: Hoe te om uw server-kant te verifiëren die implementatie door:sturen
uuid: e37296cc-0120-486a-a4ca-78d648cf6a11
translation-type: tm+mt
source-git-commit: ''

---


# Hoe te om uw server-kant te verifiëren die implementatie door:sturen

Om te verifiëren dat Server-kant het door:sturen behoorlijk wordt toegelaten, zult u de reactie van HTTP van het Analytics volgende verzoek moeten inspecteren. Dit kan worden gedaan gebruikend de de ontwikkelaarshulpmiddelen van browser of door een het proxying hulpmiddel zoals Debugger van het Web te gebruiken Charles. De volgende instructies illustreren welke indicatoren aanwezig moeten zijn om server-kant het door:sturen behoorlijk toegelaten te verzekeren.

Om de status van server-zijhet door:sturen te controleren:

1. Laad een testpagina die bijgewerkte code AppMeasurement bevat.
1. Controleer in de foutopsporingsprogramma&#39;s van uw browser of met behulp van uw proxysoftware de HTTP-reactie van de traceringsaanvraag van Analytics (u kunt dit eenvoudig filteren door een pad met &quot;b/ss&quot; te selecteren).
1. Controleer de HTTP-respons. Als de reactie de gegevens van de Manager van de Publiek (zoals hieronder geïllustreerd) bevat, dan server-zijhet door:sturen werkt.

![](assets/ssf-succeed.png)

>[!CAUTION]
>
>Als de reactie het zeer belangrijke waardepaar `"status":"SUCCESS"` of een 2 x 2 beeld bevat, dan server-zijdoor:sturen * wordt niet* correct gevormd. Gelieve te zorgen ervoor dat de Dienst van de Identiteit behoorlijk wordt opgesteld, hebt u de module van de Meting van de App opgesteld, dat de toepasselijke rapportreeks aan correcte IMS Org in kaart is gebracht, en dat server-zijhet door:sturen in de Analytics admin console is toegelaten.

>[!MORELIKETHIS]
>
>* [Charles Web Debugger](https://www.charlesproxy.com/)

