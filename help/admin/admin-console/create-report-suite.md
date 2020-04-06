---
title: Een rapportsuite maken
description: Maak een basiscontainer voor gegevensverzameling in Adobe Analytics.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Een rapportsuite maken

Een rapportsuite is een silo met gegevens die door Adobe Analytics wordt gebruikt om rapporten op te halen. Een organisatie kan vele rapportreeksen hebben, elk die verschillende gegevensreeksen bevatten. Afzonderlijke rapportsuites waren in het verleden belangrijk, maar het hebben van één enkele rapportsuite is voordeliger geworden. De inleiding aan virtuele rapportreeksen en de verwerking van de rapporttijd staat een gebruiker toe om hun eigen ondergroepen van gegevens tot stand te brengen, die de flexibiliteit toestaan om zowel globale als plaats-specifieke gegevens te verkrijgen.

Dit artikel is ontworpen voor systeembeheerders of analytische beheerders ter voorbereiding op gegevensverzameling.

## Vereisten

[Adobe Analytics First Admin Guide](first-admin-guide.md): Zorg ervoor dat een systeembeheerder u toegang tot Adobe Analytics heeft verleend via de Experience Cloud Admin Console

## Een rapportsuite maken

>[!NOTE] Er is ook een manier om een rapportsuite te maken in Adobe Analytics met behulp van de verouderde beheerder. Adobe raadt u aan de instellingwizard van de rapportsuite te gebruiken die hier wordt beschreven.

1. Meld u met uw Adobe-id aan bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com) .
1. Klik op het pictogram van 9 vierkante pixels rechtsboven en klik vervolgens op het gekleurde Analytics-logo.
1. Het modale venster Welkom bij Adobe Analytics verschijnt automatisch. Als u dat niet doet, klikt u rechtsboven op het Help-pictogram en selecteert u Welkom bij Adobe Analytics.
1. Klik in het modale venster op Setup starten.
1. Volg elke herinnering die de grondbeginselen als bezitstype, industrieën, en tijdzone schetst. Klik op Volgende.
1. De rapportsuite is nu gemaakt. Adobe raadt u ook aan een suite met ontwikkelingsrapporten te hebben, zodat tests geen invloed hebben op de gegevens van de klant. Klik op het Help-pictogram rechtsboven en selecteer vervolgens nogmaals Welkom bij Adobe Analytics.
1. Klik in het modale venster op Instellen starten.
Noem dit rapportreeks het zelfde, behalve voeg &quot;- DEV&quot;aan het eind toe. Aangezien dit rapportpakket alleen intern verkeer zal ontvangen, kan de geschatte grootte het kleinst zijn.
1. Klik op Volgende om het maken van uw dev-rapportsuite te voltooien.

Voor meer informatie over de stappen in dit modale venster, zie de modaal [van de](/help/implement/prepare/implementation-modal.md) Implementatie in de de gebruikershandleiding van de Implementatie.

## Problemen oplossen

**Nadat u zich hebt aangemeld bij de Experience Cloud, wordt het pictogram Analytics grijs weergegeven.**

Dit betekent dat aan uw account niet de juiste machtigingen voor Analytics zijn verleend. Werk met een systeembeheerder in uw organisatie om ervoor te zorgen dat u tot een profiel behoort met de juiste machtigingen voor toegang tot Adobe Analytics.

**Nadat u zich hebt aangemeld bij Adobe Analytics, ontbreken de pop-up en het vervolgkeuzemenu Welkom bij Adobe Analytics.**

Zorg ervoor dat u zich hebt aangemeld via de Experience Cloud en niet via my.omniture.com. Gebruiker die zich via my.omniture.com aanmeldt, beschikt niet over de wizard om de rapportsuite in te stellen.

## Volgende stappen

[Maak en configureer een eigenschap voor Adobe Analytics in Launch](/help/implement/launch/create-analytics-property.md): Een gebied maken om uw analytische implementatie te beheren
