---
title: Beheerdersrollen in Adobe Analytics
description: Begrijp hoe te beginnen met Adobe Analytics, algemene roltypes, en het programma openen aan UI.
feature: Admin Tools
exl-id: 9d10716f-5b66-42dc-b288-af34da203c35
source-git-commit: 9057cc83881a72fa039e9398ed3daaf4259ef2bf
workflow-type: tm+mt
source-wordcount: '1090'
ht-degree: 0%

---

# Beheerdersrollen in Adobe Analytics

Adobe Analytics ondersteunt verschillende typen beheerders. Volledige Adobe Analytics-beheerders hebben toegang tot alles in Adobe Analytics, terwijl andere beheerders en gebruikers gespecialiseerde taken kunnen uitvoeren.

>[!NOTE]
>
>Voordat aan gebruikers rollen kunnen worden toegewezen in Adobe Analytics, moet een gebruiker worden toegewezen als eerste beheerder in Experience Cloud. De eerste beheerder kan gebruikers in de organisatie dan voorzien van andere zeer belangrijke rollen, zoals die in dit artikel worden beschreven. Voor meer informatie over eerste admin, zie [Adobe Analytics First Admin Guide](/help/admin/admin-console/first-admin-guide.md).


## Belangrijkste rollen in Experience Cloud en Adobe Analytics

Houd rekening met de volgende sleutelrollen bij het gebruik van Adobe Analytics:

* **Volledige Adobe Analytics-beheerders:** Deze gebruikers hebben volledige toegang tot alles in Adobe Analytics, inclusief instellingen voor rapportsuite en gebruikersmachtigingen. Afhankelijk van de structuur van uw organisatie kunnen verschillende personen of teams verantwoordelijk zijn voor verschillende facetten van het analysebeheer. Eén persoon is bijvoorbeeld verantwoordelijk voor de aanwijzing van de variabelen die in een implementatie moeten worden gebruikt. Een andere persoon kan voor het toelaten van gebruikers verantwoordelijk zijn om rapporten correct te trekken door iedereen te verzekeren heeft de correcte toestemmingen. Identificeer minstens één gebruiker die voor de montages en gebruikerstoestemmingen van het het rapportpakket van de Analyse kan verantwoordelijk zijn, en zij kunnen andere beheerders van Analytics van daar uitnodigen.
* **Beheerders van gegevensverzameling:** Deze gebruikers hebben volledige toegang tot alles in de Gegevensverzameling van Adobe Experience Platform, met inbegrip van het publiceren toestemmingen, het creëren van containers, en gebruikerstoestemmingen. Deze gebruikers zijn niet noodzakelijkerwijs programmeurs, maar het is nuttig om ten minste een beginner op de hoogte te hebben van HTML, CSS en JavaScript. Ze zijn verantwoordelijk voor het werken met de eigenaars van uw website om tags op uw site te laten implementeren. Identificeer minstens één gebruiker die voor de implementatie van uw organisatie verantwoordelijk is, en zij kunnen andere beheerders van de gegevensinzameling van daar uitnodigen.
* **Beheerders van productprofiel:** Deze gebruikers kunnen gebruikers toevoegen aan of verwijderen uit een productprofiel, machtigingsitems in hun productprofiel aanpassen en productprofielen toewijzen aan of verwijderen uit gebruikersgroepen. Beheerders van productprofielen hebben geen volledige toegang tot Adobe Analytics. Zij zijn echter ideaal voor teamleiders of managers die toegang tot Adobe Analytics voor hun team moeten verlenen en beheren. Voor meer informatie over productprofielen raadpleegt u [Productprofielen voor Adobe Analytics](/help/admin/admin-console/permissions/product-profile.md).
* **Ondersteuningsafgevaardigden**: Deze gebruikers, ook wel ondersteunde gebruikers genoemd, hebben geen extra bevoegdheden in de interface Analytics. In plaats daarvan krijgen ze extra privileges wanneer ze communiceren met de klantenservice van Adobe. Deze gebruikers zijn bijna altijd ook Analytics-beheerders, omdat dit de klantenservice helpt problemen met hen op te lossen. Identificeer ten minste één Analytics-beheerder die verantwoordelijk is voor het faciliteren van de interactie tussen eindgebruikers en de klantenservice van Adobe.
* **Eigenaars van websites:** Deze personen of teams zijn verantwoordelijk voor de codering en ontwikkeling van uw website. Ze hebben geen accounts nodig, maar ze willen samenwerken met beheerders voor gegevensverzameling om de tagcode op uw website te plaatsen en te implementeren.
* **Eindgebruikers:** deze gebruikers bekijken typisch rapporten en zoeken antwoorden op bedrijfsvragen. Analysebeheerders verlenen deze gebruikers machtigingen om in het product te werken.

## Volledige toegang voor productbeheer verlenen aan Analytics

Systeembeheerders hebben geen directe toegang tot producten; zij kunnen zich echter toegang verschaffen door zichzelf toe te voegen als beheerder op productniveau.

Adobe Analytics toegang geven tot uzelf of anderen:

1. Aanmelden bij de [Admin Console](https://adminconsole.adobe.com/) met uw Adobe ID-gebruikersgegevens.
1. Klik op de knop **[!UICONTROL Products]** aan de bovenkant. Alle producten die door uw organisatie worden aangeschaft, staan links. Klikken **[!UICONTROL Adobe Analytics]** klikt u op de knop **[!UICONTROL New Profile]** knop.
1. Geef dit profiel de naam &#39;toegang voor volledige beheer van analysemogelijkheden&#39; en klik op **[!UICONTROL Next]** > **[!UICONTROL Save]**.
1. Klik op de pagina Productprofielen op het nieuwe profiel en klik vervolgens op de knop **[!UICONTROL Permissions]** tab.
1. Klik op een van de machtigingsregelitems. Indien **[!UICONTROL Auto-include]** is beschikbaar, schakelt u deze in. Indien **[!UICONTROL Auto-include]** is niet beschikbaar, klikt u op **[!UICONTROL Add all]**. Met beide opties worden alle machtigingsitems naar de rechterkolom verplaatst.
1. Klik op **[!UICONTROL Save]**.
Herhaal bovenstaande stap voor alle machtigingscategorieën.
1. Nadat alle toestemmingscategorieën aan het profiel worden verleend, ga terug naar de pagina van Producten door te klikken **[!UICONTROL Product]** bovenaan.
1. Klik onder de tegel Adobe Analytics op **[!UICONTROL Assign Users]**.
1. Voer het e-mailadres in waar u volledige toegang tot Analytics wilt geven en wijs hieraan het nieuwe volledige toegangsprofiel voor beheerders toe. Klik op **[!UICONTROL Save]**.

De gebruiker heeft nu volledige toegang tot Adobe Analytics.

## Toegang voor productbeheerder verlenen voor gegevensverzameling in Experience Platform

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

## Toegang voor productbeheer verlenen voor productprofielen

Zie de sectie &quot;Beheer van productprofielbeheerders&quot; in het artikel voor informatie over het toewijzen van gebruikers als productprofielbeheerders. [Productprofielen beheren voor zakelijke gebruikers](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) in de gebruikershandleiding voor de onderneming.

## Volgende stappen

[Een rapportsuite maken](/help/admin/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md): Laat uw Analytics-beheerder zich aanmelden bij het hulpprogramma en maak een rapportsuite voor gegevensverzameling

[Een eigenschap voor de tag Analytics maken](/help/implement/launch/create-analytics-property.md): Laat uw beheerder van gegevensverzameling zich aanmelden bij het gereedschap en maak een eigenschap die u op uw site wilt implementeren

Voordat aan gebruikers rollen kunnen worden toegewezen in Adobe Analytics, moet een gebruiker worden toegewezen als eerste beheerder in Experience Cloud. De eerste beheerder kan gebruikers in de organisatie dan voorzien van andere zeer belangrijke rollen, zoals die in dit artikel worden beschreven.

Een eerste beheerder is het uitgangspunt om de rest van de organisatie toe te laten om elke oplossing van de Experience Cloud te gebruiken.

Nadat een contract is ondertekend

1. Het inrichtingsteam bij Adobe bereidt de account voor die moet worden gemaakt.

1. De eerste beheerder ontvangt een e-mail met aanmeldingsgegevens vóór de begindatum van het contract.

>[!IMPORTANT]
>
>   Het wordt ten zeerste aanbevolen ervoor te zorgen dat de contactgegevens van de eerste beheerder aan de Adobe worden verstrekt en nauwkeurig zijn voordat het contract wordt ondertekend.
