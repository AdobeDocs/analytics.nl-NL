---
title: Eerste Adobe Analytics-beheerdershandleiding
description: Begrijp hoe te beginnen met Adobe Analytics, algemene roltypes, en het programma openen aan UI.
exl-id: fbbbd335-0d22-473e-adef-f92f8eab7bf0
feature: Admin Tools
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 1%

---

# Eerste Adobe Analytics-beheerdershandleiding

Een eerste beheerder is het uitgangspunt om de rest van de organisatie toe te laten om elke oplossing van de Experience Cloud te gebruiken. Nadat een contract is ondertekend, bereidt een inrichtingsteam bij Adobe zich voor op het aanmaken van de account. De eerste beheerder ontvangt een e-mail met aanmeldingsgegevens vóór de begindatum van het contract. Het wordt ten zeerste aanbevolen ervoor te zorgen dat de contactgegevens van de eerste beheerder aan de Adobe worden verstrekt en nauwkeurig zijn voordat het contract wordt ondertekend.

## Belangrijke rollen bij het gebruik van de Experience Cloud

Als uw organisatie Adobe Analytics heeft aangeschaft, moet u rekening houden met een aantal belangrijke rollen:

* **Adobe Analytics-beheerders:** Deze gebruikers hebben volledige toegang tot alles in Adobe Analytics, inclusief instellingen voor rapportsuite en gebruikersmachtigingen. Afhankelijk van de structuur van uw organisatie kunnen verschillende personen of teams verantwoordelijk zijn voor verschillende facetten van het analysebeheer. Eén persoon is bijvoorbeeld verantwoordelijk voor de aanwijzing van de variabelen die in een implementatie moeten worden gebruikt. Een andere persoon kan voor het toelaten van gebruikers verantwoordelijk zijn om rapporten correct te trekken door iedereen te verzekeren heeft de correcte toestemmingen. Identificeer minstens één gebruiker die voor de montages en gebruikerstoestemmingen van het het rapportpakket van de Analyse kan verantwoordelijk zijn, en zij kunnen andere beheerders van Analytics van daar uitnodigen.
* **Beheerders van gegevensverzameling:** Deze gebruikers hebben volledige toegang tot alles in de Gegevensverzameling van Adobe Experience Platform, met inbegrip van het publiceren toestemmingen, het creëren van containers, en gebruikerstoestemmingen. Deze gebruikers zijn niet noodzakelijkerwijs programmeurs, maar het is nuttig om ten minste een beginner op de hoogte te hebben van HTML, CSS en JavaScript. Ze zijn verantwoordelijk voor het werken met de eigenaars van uw website om tags op uw site te laten implementeren. Identificeer minstens één gebruiker die voor de implementatie van uw organisatie verantwoordelijk is, en zij kunnen andere beheerders van de gegevensinzameling van daar uitnodigen.
* **Ondersteuningsafgevaardigden**: Deze gebruikers, ook wel ondersteunde gebruikers genoemd, hebben geen extra bevoegdheden in de interface Analytics. In plaats daarvan krijgen ze extra privileges wanneer ze communiceren met de klantenservice van Adobe. Deze gebruikers zijn bijna altijd ook Analytics-beheerders, omdat dit de klantenservice helpt problemen met hen op te lossen. Identificeer ten minste één Analytics-beheerder die verantwoordelijk is voor het faciliteren van de interactie tussen eindgebruikers en de klantenservice van Adobe.
* **Eigenaars van websites:** Deze personen of teams zijn verantwoordelijk voor de codering en ontwikkeling van uw website. Ze hebben geen accounts nodig, maar ze willen samenwerken met beheerders voor gegevensverzameling om de tagcode op uw website te plaatsen en te implementeren.
* **Eindgebruikers:** deze gebruikers bekijken typisch rapporten en zoeken antwoorden op bedrijfsvragen. Analysebeheerders verlenen deze gebruikers machtigingen om in het product te werken.

Als eerste beheerder, kan uw rol in één of meerdere van deze rollen overlappen. Zolang elk van deze basisverantwoordelijkheden wordt behandeld, kunt u toestemmingen verlenen om anderen in uw organisatie in werking te stellen.

## Beheerdersrechten voor producten verlenen voor Analytics

Systeembeheerders hebben geen directe toegang tot producten, maar ze kunnen zichzelf toegang geven door zichzelf toe te voegen als beheerder op productniveau. Als u uzelf of anderen toegang wilt geven tot Adobe Analytics, kunt u deze stappen volgen.

1. Aanmelden bij de [Admin Console](https://adminconsole.adobe.com/) met uw Adobe ID-gebruikersgegevens.
1. Klik bovenaan op het tabblad Producten. Alle producten die door uw organisatie worden aangeschaft, staan links. Klik op Adobe Analytics en vervolgens op de knop Nieuw profiel.
1. Geef dit profiel de naam &#39;Volledige beheerderstoegang van Analytics&#39; en klik vervolgens op Done.
1. Klik op de pagina Productprofielen op het nieuwe profiel en klik vervolgens op het tabblad Machtigingen.
1. Klik op een van de machtigingsregelitems. Als Auto-include beschikbaar is, laat het toe. Als automatisch opnemen niet beschikbaar is, klikt u op Alles toevoegen. Met beide opties worden alle machtigingsitems naar de rechterkolom verplaatst.
1. Klik op Opslaan. Herhaal bovenstaande stap voor alle machtigingscategorieën.
1. Zodra alle toestemmingscategorieën aan het profiel worden verleend, ga terug naar de pagina van het Overzicht door Overzicht bij de bovenkant te klikken.
1. Klik onder de tegel Adobe Analytics op Gebruikers toewijzen.
1. Voer het e-mailadres in waar u volledige toegang tot Analytics wilt geven en wijs hieraan het nieuwe volledige toegangsprofiel voor beheerders toe. Klik op Opslaan.
1. De gebruiker heeft nu volledige toegang tot Adobe Analytics.

## Het verlenen van product admin toegang voor de Inzameling van Gegevens in Experience Platform

Toegang tot productbeheer voor gegevensverzameling in Experience Platform is vrijwel gelijk aan het verlenen van toegang tot productbeheer voor Analytics.

1. Aanmelden bij de [Adobe Admin Console](https://adminconsole.adobe.com) met uw Adobe ID-gebruikersgegevens.
1. Klik op de knop **[!UICONTROL Products]** aan de bovenkant. Alle producten die door uw organisatie worden aangeschaft, staan links. Klikken **[!UICONTROL Experience Platform Launch]** en klik vervolgens op **[!UICONTROL New Profile]**.
1. Geef dit profiel de naam &#39;toegang tot volledige beheerder van gegevensverzameling&#39; en klik vervolgens op **[!UICONTROL Done]**.
1. Terug op de **[!UICONTROL Product Profiles]** pagina, klikt u op het nieuwe profiel en klikt u vervolgens op de knop **[!UICONTROL Permissions]** tab.
1. Klik op een van de machtigingsregelitems. Indien **[!UICONTROL Auto-include]** is beschikbaar, schakelt u deze in. Als automatisch opnemen niet beschikbaar is, klikt u op **[!UICONTROL Add all]**. Met beide opties worden alle machtigingsitems naar de rechterkolom verplaatst.
1. Klik op **[!UICONTROL Save]**. Herhaal bovenstaande stap voor alle machtigingscategorieën.
1. Als alle machtigingscategorieën zijn toegewezen aan het profiel, gaat u terug naar de pagina Overzicht door op **[!UICONTROL Overview]** bovenaan.
1. Onder de [!UICONTROL Experience Platform Launch] tegel, klikken **[!UICONTROL Assign Users]**.
1. Voer het e-mailadres in waar u volledige toegang tot Analytics wilt geven en wijs hieraan het nieuwe volledige toegangsprofiel voor beheerders toe. Klik op **[!UICONTROL Save]**.
1. De gebruiker heeft nu volledige toegang tot de Inzameling van de Gegevens van het Experience Platform.

## Volgende stappen

[Een rapportsuite maken](/help/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Laat uw Analytics-beheerder zich aanmelden bij het hulpprogramma en maak een rapportsuite voor gegevensverzameling

[Een eigenschap voor de tag Analytics maken](/help/implement/launch/create-analytics-property.md): Laat uw beheerder van gegevensverzameling zich aanmelden bij het gereedschap en maak een eigenschap die u op uw site wilt implementeren
