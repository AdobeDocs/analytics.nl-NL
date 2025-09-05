---
description: Om te verifiëren dat Server-kant het door:sturen behoorlijk wordt toegelaten, zult u de reactie van HTTP van het Analytics volgende verzoek moeten inspecteren. Deze instructies illustreren welke indicatoren aanwezig moeten zijn om server-kant het door:sturen behoorlijk toegelaten te verzekeren.
solution: Analytics
title: Hoe te om uw server-kant te verifiëren die implementatie door:sturen
feature: Report Suite Settings
exl-id: 21db4572-da3c-43aa-a774-86a089656695
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Hoe te om uw server-kant te verifiëren die implementatie door:sturen

Om te verifiëren dat Server-kant het door:sturen behoorlijk wordt toegelaten, zult u de reactie van HTTP van het Analytics volgende verzoek moeten inspecteren. Dit kan worden gedaan gebruikend de de ontwikkelaarshulpmiddelen van browser of door een het proxying hulpmiddel zoals Debugger van het Web te gebruiken Charles. De volgende instructies illustreren welke indicatoren aanwezig moeten zijn om server-kant het door:sturen behoorlijk toegelaten te verzekeren.

Om de status van server-zijhet door:sturen te controleren:

1. Laad een testpagina die bijgewerkte AppMeasurement-code bevat.
1. Controleer in de foutopsporingsprogramma&#39;s van uw browser of met behulp van uw proxysoftware de HTTP-reactie van de traceringsaanvraag van Analytics (u kunt dit eenvoudig filteren door een pad met &quot;b/ss&quot; te selecteren).
1. Controleer de HTTP-respons. Als de reactie Audience Manager-gegevens bevat (zoals hieronder wordt geïllustreerd), werkt het doorsturen aan de serverzijde.

![](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/assets/ssf-succeed.png)

>[!CAUTION]
>
>Als de reactie het zeer belangrijke waardepaar `"status":"SUCCESS"` of een 2 x 2 beeld bevat, dan server-zijdoor:sturen * wordt niet correct gevormd. Gelieve te zorgen ervoor dat de Dienst van de Identiteit behoorlijk wordt opgesteld, hebt u de module van de Meting van de App opgesteld, dat de toepasselijke rapportreeks aan correcte organisatie ID in kaart is gebracht, en dat server-side het door:sturen in de Hulpmiddelen van Analytics Admin is toegelaten.

>[!MORELIKETHIS]
>
>* [ Charles Web Debugger ](https://www.charlesproxy.com/)
