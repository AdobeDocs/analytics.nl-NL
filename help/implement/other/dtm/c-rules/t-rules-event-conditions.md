---
description: De voorwaarden bepalen wanneer een op gebeurtenis-gebaseerde regel wordt teweeggebracht.
keywords: Dynamic Tag Management;rule;create rule;new rule;event-based rule;delay link activation;apply event handler directly to element;bubbling;event bubbling
solution: Experience Cloud,Analytics,Target,Dynamic Tag Management
title: Voorwaarden maken voor op gebeurtenissen gebaseerde regels
uuid: a847391c-5aec-4d64-8a35-388587731598
translation-type: tm+mt
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# Voorwaarden maken voor op gebeurtenissen gebaseerde regels

De voorwaarden bepalen wanneer een op gebeurtenis-gebaseerde regel wordt teweeggebracht.

1. Selecteer het type interactie dat u wilt bijhouden, zoals muisklikken of het verzenden van een formulier.

   ![](assets/condition-event-based.png)

   Zie [Gebeurtenistypen](https://marketing.adobe.com/resources/help/en_US/dtm/event_types.html) in de productdocumentatie van Adobe Tagbeheer voor meer informatie.

1. Schakel indien nodig de volgende opties in:

   | Element | Beschrijving |
   |--- |--- |
   | Vertraging bij activeren van koppeling | Schakel deze optie in als de gebeurtenis een koppeling activeert en u wilt dat de koppeling wordt uitgesteld totdat de gebeurtenis tijd heeft om te worden gestart. |
   | Gebeurtenishandler rechtstreeks toepassen op element | Past de gebeurtenismanager op het specifieke element toe dat wordt gericht. Deze instelling is gekoppeld aan het concept voor terugkoppelen en laagplaatsen in een browser. |

   Als u bijvoorbeeld op een afbeelding klikt binnen een ankertag, bijvoorbeeld `<a href="abc.html"><img src="xyz.png"/></a>`, kunt u de klik verwachten dat deze aan de ankertag wordt gekoppeld, omdat de tag zich in de terugkoppelstroom bevindt. Wanneer u de klik echter inspecteert in de ontwikkelaars, heeft de klik mogelijk alleen invloed op de `<img>` tag. Om ervoor te zorgen dat de gebeurtenis correct wordt afgehandeld, associeert de klik met de `<img>` markering en hangt niet van browser af om omhoog de klik aan een ouderelement te beluisteren. Een gebeurtenis als een klik kan potentieel omhoog belopen aan `<body>`. Het is belangrijk om te begrijpen waar de gebeurtenis eigenlijk gebonden is, en het te richten specifiek om ervoor te zorgen dat de regel correct in brand steekt.

   *Bubbling* betekent dat de gebeurtenis eerst door het binnenste meeste element wordt vastgelegd en behandeld en vervolgens aan buitenste elementen wordt doorgegeven.

1. Geef de naam op van de tag die u wilt bijhouden en geef aanvullende eigenschappen op waaraan de tag moet voldoen.

   ![](assets/condition-event-based2.png)

   Zie [De CSS-kiezer](https://marketing.adobe.com/resources/help/en_US/dtm/css-selector.html) gebruiken in de productdocumentatie voor dynamisch tagbeheer voor informatie over het zoeken naar de juiste elementtag.

1. Selecteer en stel extra criteria of voorwaardetypes in u aan de regel wilt binden.

   ![](assets/condition-event-based3.png)

1. Geef uw voorkeur voor terugkoppelen van gebeurtenissen.

   Gebeurtenisterugkoppeling is een manier om gebeurtenissen door te geven in HTML DOM.

   | Als u... | Deze optie inschakelen |
   |--- |--- |
   | Verwante interactie over kindelementen van de regelselecteur u identificeerde om de regel in werking te stellen. | Toestaan dat gebeurtenissen op onderliggende elementen worden teruggekoppeld. |
   | Wilt u terugkoppelen voorkomen wanneer het onderliggende element al een eigen gebeurtenis activeert. | Niet toestaan als het onderliggende element al de gebeurtenis activeert. |
   | De gebeurtenissen van de regelkiezer die u hebt opgegeven, mogen niet verder gaan dan het element zelf in de gebeurtenishiërarchie. | Laat niet toe dat gebeurtenissen omhoog naar de ouders gaan. |
