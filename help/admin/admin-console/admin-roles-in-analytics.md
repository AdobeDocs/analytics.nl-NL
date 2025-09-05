---
title: Beheerdersrollen in Adobe Analytics
description: Begrijp hoe te beginnen met Adobe Analytics, algemene roltypes, en het programma openen aan UI.
feature: Admin Tools
exl-id: 9d10716f-5b66-42dc-b288-af34da203c35
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 0%

---

# Beheerdersrollen in Adobe Analytics

Adobe Analytics ondersteunt verschillende typen beheerders. Volledige Adobe Analytics-beheerders hebben toegang tot alles in Adobe Analytics, terwijl andere beheerders en gebruikers gespecialiseerde taken kunnen uitvoeren.

>[!NOTE]
>
>Voordat aan gebruikers rollen kunnen worden toegewezen in Adobe Analytics, moet een gebruiker worden toegewezen als eerste beheerder in Experience Cloud. De eerste beheerder kan gebruikers in de organisatie dan voorzien van andere zeer belangrijke rollen, zoals die in dit artikel worden beschreven. Voor meer informatie over eerste admin, zie [ Adobe Analytics eerste admin gids ](/help/admin/admin-console/first-admin-guide.md).


## Belangrijkste rollen in Experience Cloud en Adobe Analytics

Houd rekening met de volgende sleutelrollen bij het gebruik van Adobe Analytics:

* **Volledige beheerders van Adobe Analytics:** Deze gebruikers hebben volledige toegang tot alles in Adobe Analytics, met inbegrip van de montages van de rapportreeks en gebruikerstoestemmingen. Afhankelijk van de structuur van uw organisatie kunnen verschillende personen of teams verantwoordelijk zijn voor verschillende facetten van het analysebeheer. Eén persoon is bijvoorbeeld verantwoordelijk voor de aanwijzing van de variabelen die in een implementatie moeten worden gebruikt. Een andere persoon kan voor het toelaten van gebruikers verantwoordelijk zijn om rapporten correct te trekken door iedereen te verzekeren heeft de correcte toestemmingen. Identificeer minstens één gebruiker die voor de montages en gebruikerstoestemmingen van het het rapportpakket van de Analyse kan verantwoordelijk zijn, en zij kunnen andere beheerders van Analytics van daar uitnodigen.
* {de beheerders van de Inzameling van 0} Gegevens:**Deze gebruikers hebben volledige toegang tot alles in de Inzameling van Gegevens van Adobe Experience Platform, met inbegrip van het publiceren toestemmingen, het creëren van containers, en gebruikerstoestemmingen.** Deze gebruikers zijn niet noodzakelijkerwijs programmeurs, maar het is nuttig om ten minste een beginner van HTML, CSS en JavaScript te kennen. Ze zijn verantwoordelijk voor het werken met de eigenaars van uw website om tags op uw site te laten implementeren. Identificeer minstens één gebruiker die voor de implementatie van uw organisatie verantwoordelijk is, en zij kunnen andere beheerders van de gegevensinzameling van daar uitnodigen.
* **Admin van het Product:** Een Beheerder van het Product beheert een product in Admin Console, evenals gebruikersrechten aan dat product.
* {de beheerders van het Profiel van 0} Product:**Deze gebruikers kunnen gebruikers aan een productprofiel toevoegen of verwijderen, toestemmingspunten in hun productprofiel aanpassen, en productprofielen toewijzen of verwijderen aan gebruikersgroepen.** Beheerders van productprofielen hebben geen volledige toegang tot Adobe Analytics. Zij zijn echter ideaal voor teamleiders of managers die toegang tot Adobe Analytics voor hun team moeten verlenen en beheren. Voor meer informatie over productprofielen, zie [ profielen van het Product voor Adobe Analytics ](/help/admin/admin-console/permissions/product-profile.md).
* **Beheerder van de Steun**: Ook gekend als gesteunde gebruikers, hebben zij geen extra voorrechten in de interface Analytics. In plaats daarvan krijgen ze extra privileges wanneer ze communiceren met de klantenservice van Adobe. Deze gebruikers zijn bijna altijd ook Analytics-beheerders, omdat dit de klantenservice helpt problemen met hen op te lossen. Identificeer minstens één Analytics-beheerder die verantwoordelijk is voor het faciliteren van de interactie tussen eindgebruikers en de Adobe-klantenservice.
* **de eigenaars van de Website:** Deze individuen of teams zijn verantwoordelijk voor de codering en de ontwikkeling van uw website. Ze hebben geen accounts nodig, maar ze willen samenwerken met beheerders voor gegevensverzameling om de tagcode op uw website te plaatsen en te implementeren.
* **Eind gebruikers:** deze gebruikers bekijken typisch rapporten en zoeken antwoorden aan bedrijfsvragen. Analysebeheerders verlenen deze gebruikers machtigingen om in het product te werken.

## Volledige toegang voor productbeheer verlenen aan Analytics

Systeembeheerders hebben geen directe toegang tot producten, maar kunnen zichzelf toegang geven door zichzelf toe te voegen als beheerder op productniveau.

Adobe Analytics toegang geven tot uzelf of anderen:

1. Login aan [ Admin Console ](https://adminconsole.adobe.com/) met uw geloofsbrieven van Adobe ID.
1. Klik op de tab **[!UICONTROL Products]** bovenaan. Alle producten die door uw organisatie worden aangeschaft, staan links. Klik op **[!UICONTROL Adobe Analytics]** en vervolgens op de knop **[!UICONTROL New Profile]** .
1. Geef dit profiel de naam &#39;Volledige beheertoegang voor analysemogelijkheden&#39; en klik vervolgens op **[!UICONTROL Next]** > **[!UICONTROL Save]** .
1. Klik op de pagina Productprofielen op het nieuwe profiel en klik vervolgens op het tabblad **[!UICONTROL Permissions]** .
1. Klik op een van de machtigingsregelitems. Als **[!UICONTROL Auto-include]** beschikbaar is, schakelt u deze in. Als **[!UICONTROL Auto-include]** niet beschikbaar is, klikt u op **[!UICONTROL Add all]** . Met beide opties worden alle machtigingsitems naar de rechterkolom verplaatst.
1. Klik op **[!UICONTROL Save]** .
Herhaal bovenstaande stap voor alle machtigingscategorieën.
1. Nadat alle machtigingscategorieën aan het profiel zijn toegekend, gaat u terug naar de pagina Producten door boven op **[!UICONTROL Product]** te klikken.
1. Klik onder de tegel Adobe Analytics op **[!UICONTROL Assign Users]** .
1. Voer het e-mailadres in waar u volledige toegang tot Analytics wilt geven en wijs hieraan het nieuwe volledige toegangsprofiel voor beheerders toe. Klik op **[!UICONTROL Save]**.

De gebruiker heeft nu volledige toegang tot Adobe Analytics.

## Toegang voor productbeheer verlenen voor gegevensverzameling in Experience Platform

Toegang tot productbeheer voor gegevensverzameling in Experience Platform is vrijwel gelijk aan het verlenen van toegang tot productbeheer voor Analytics.

1. Login aan [ Adobe Admin Console ](https://adminconsole.adobe.com) met uw geloofsbrieven van Adobe ID.
1. Klik op de tab **[!UICONTROL Products]** bovenaan. Alle producten die door uw organisatie worden aangeschaft, staan links. Klik op **[!UICONTROL Experience Platform Launch]** en vervolgens op **[!UICONTROL New Profile]** .
1. Geef dit profiel de naam &#39;Volledige beheertoegang voor gegevensverzameling&#39; en klik vervolgens op **[!UICONTROL Done]** .
1. Klik op de pagina **[!UICONTROL Product Profiles]** op het nieuwe profiel en klik vervolgens op de tab **[!UICONTROL Permissions]** .
1. Klik op een van de machtigingsregelitems. Als **[!UICONTROL Auto-include]** beschikbaar is, schakelt u deze in. Als automatisch opnemen niet beschikbaar is, klikt u op **[!UICONTROL Add all]** . Met beide opties worden alle machtigingsitems naar de rechterkolom verplaatst.
1. Klik op **[!UICONTROL Save]**. Herhaal bovenstaande stap voor alle machtigingscategorieën.
1. Wanneer alle machtigingscategorieën zijn toegewezen aan het profiel, gaat u terug naar de pagina Overzicht door boven op **[!UICONTROL Overview]** te klikken.
1. Klik onder de [!UICONTROL Experience Platform Launch] -tegel op **[!UICONTROL Assign Users]** .
1. Voer het e-mailadres in waar u volledige toegang tot Analytics wilt geven en wijs hieraan het nieuwe volledige toegangsprofiel voor beheerders toe. Klik op **[!UICONTROL Save]**.
1. De gebruiker heeft nu volledige toegang tot de Gegevensverzameling van Experience Platform.

## Toegang voor productbeheer verlenen voor productprofielen

Voor informatie over het toewijzen van gebruikers als beheerders van het productprofiel, zie de &quot;Manage de beheerders&quot;sectie van het productprofiel in het artikel, [ beheren productprofielen voor ondernemingsgebruikers ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) in de de gebruikersgids van de Onderneming.

## Volgende stappen

[ creeer een Reeks van het Rapport ](/help/admin/tools/manage-rs/new-rs/t-create-a-report-suite.md): Heb uw login van Analysebeheer aan het hulpmiddel en creeer een rapportreeks voor gegevensinzameling

[ creeer een de markeringsbezit van de Analyse ](/help/implement/launch/create-analytics-property.md): Heb uw het beheerderslogin van de Inzameling van Gegevens aan het hulpmiddel en creeer een bezit om op uw plaats uit te voeren

Voordat aan gebruikers rollen kunnen worden toegewezen in Adobe Analytics, moet een gebruiker worden toegewezen als eerste beheerder in Experience Cloud. De eerste beheerder kan gebruikers in de organisatie dan voorzien van andere zeer belangrijke rollen, zoals die in dit artikel worden beschreven.

Een eerste beheerder is het uitgangspunt om de rest van de organisatie in staat te stellen om elke oplossing van Experience Cloud te gebruiken.

Nadat een contract is ondertekend

1. Het inrichtingsteam bij Adobe bereidt het maken van de account voor.

1. De eerste beheerder ontvangt een e-mail met aanmeldingsgegevens vóór de begindatum van het contract.

>[!IMPORTANT]
>
>   Het verdient ten zeerste aanbeveling ervoor te zorgen dat de contactgegevens van de eerste beheerder aan Adobe worden verstrekt en correct zijn voordat het contract wordt ondertekend.
