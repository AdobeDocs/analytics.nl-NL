---
description: Veelgestelde vragen over Adobe Analytics-serveroproepgebruik
title: Veelgestelde vragen over serveroproepgebruik
feature: Server Call Usage
exl-id: a660542c-9389-4608-bc25-49831c21ceb7
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 0%

---

# Veelgestelde vragen over serveroproepgebruik

| Vraag | Antwoord |
|--- |--- |
| V: Ik ben een analytische beheerder. Waarom zie ik geen [!UICONTROL Server Call Usage] koppeling onder de sectie Admin voor mijn aanmeldingsbedrijf? | A: U kunt kiezen voor welke aanmeldbedrijven de koppeling wordt weergegeven voor [!UICONTROL Server Call Usage] onder de sectie Beheer. Als u het niet ziet, gelieve de Zorg van de Cliënt te contacteren om het toe te laten. |
| V: Is [!UICONTROL Server Call Usage] een alleen-beheerfunctie? | A: Nee. Net als de [!UICONTROL Billing] functie die [!UICONTROL Server Call Usage] vervangt, kunt u een niet-beheerder de toestemming toewijzen om tot deze verbinding toegang te hebben. |
| V: zijn [!UICONTROL Server Call Usage] en de verbintenisdetails specifiek voor één login bedrijf? | A: Nee. Gebruiks- en verplichtingsgegevens die worden weergegeven, gelden voor al uw aanmeldingsbedrijven die onder uw Adobe Analytics-contract vallen. |
| V: Onder de [!UICONTROL Report Suite Usage] tab, kan ik consumptie over rapportreeksen zien die niet voor rapportering onder het huidige login bedrijf beschikbaar zijn. Is dat een probleem? | A: Nee. Net als uw [!UICONTROL Server Call Usage] en de verbintenisdetails, omvat de lijst van rapportreeksen alle login bedrijven u in het kader van uw contract van de Analyse hebt uitgevoerd. |
| V: Is de gebruiksperiode altijd gelijk aan de duur van mijn Analytics-contract of factureringscyclus? | A: Nee. De periode van het gebruik is de duur waarvoor uw server-vraag verplichting van toepassing is en kan van uw contracttijdlijn of factureringscyclus verschillend zijn. Uw jaarlijkse contract zou u bijvoorbeeld kunnen toestaan aan één miljard servervraag per maand, in welk geval uw verplichting één miljard servervraag zou zijn en uw gebruiksperiode één maand zou zijn. |
| V: Mijn contract bevat een verplichting voor Video Heart Beats, maar ik zie ze niet onder [!UICONTROL Server Call Usage]. Moet ik contact opnemen met de klantenservice? | A: Consumptie- en verplichtingsdetails voor Video Heart Mats maken geen deel uit van [!UICONTROL Server Call Usage]. |
| V: Mijn contract omvat geen voorziening voor secundaire servervraag maar ik zie hen nog onder [!UICONTROL Current Usage] en [!UICONTROL Report Suite Usage] tabs. Is dit een bug? | A: Nee. Hoewel uw contract niet uitdrukkelijk secundaire servervraag voorziet, kunt u hen nog veroorzaken als u in de gegevens van Analytics naar meer dan één van uw rapportreeksen verzendt. U kunt of uw implementatie herzien om ervoor te zorgen u niet in dergelijke vraag verzendt of uw Team van de Rekening van de Adobe contacteert om uw contract bij te werken zodat omvat het een voorziening voor dergelijke vraag. |
| V: Mijn contract omvat geen voorziening voor secundaire servervraag maar ik zie hen nog onder [!UICONTROL Current Usage] en [!UICONTROL Report Suite Usage] tabs. Betekent dit dat ik zal beginnen met overuren? | A: Of u zou beginnen overages te veroorzaken wanneer u in secundaire servervraag verzendt zonder voor hen wordt provisioned hangt van uw contract af. In sommige gevallen, secundair-server-vraag consumptie zou tegen uw verplichting voor primaire servervraag kunnen tellen, die hen aan een tarief sneller dan u zou voorzien vernietigen. In andere gevallen, kon u voor secundaire servervraag worden in rekening gebracht zelfs als u niet al uw primaire servervraag hebt verbruikt. Raadpleeg uw contract of neem contact op met uw Adobe-accountteam om te bevestigen. |
| V: Mijn contract/gebruiksperiode begon net, en ik ontvang reeds alarm over het overschrijden van mijn secundaire verplichting van de servervraag. Is dit een insect en zal ik overuren gaan factureren? | A: Nee. Dit zou kunnen betekenen u secundaire servervraag verbruikt zonder hen uitdrukkelijk provisioned als deel van uw contract van Adobe Analytics worden. De waarschuwing is enkel om ervoor te zorgen dat u zich hiervan bewust bent en u toe te laten om correctieve actie te nemen, indien nodig. Zie ook Veelgestelde vragen 8 hierboven. |
| V: Ik heb geen [!UICONTROL Server Call Usage] signaleringen, maar ik ontvang meerdere dergelijke waarschuwingen, allemaal met dezelfde inhoud. Is dit een bug? | A: Nee. De standaardalarm wordt teweeggebracht voor alle login bedrijven die hebben [!UICONTROL Server Call Usage] koppeling ingeschakeld onder [!UICONTROL Admin] sectie. Het alarm omvat de naam van het bedrijf dat de alarm teweegbracht. Als beheerder kunt u deze waarschuwingen uitschakelen en/of verwijderen om dubbele meldingen te voorkomen, uzelf uit de lijst met ontvangers te verwijderen of de klantenservice de optie [!UICONTROL Server Call Usage] koppeling voor specifieke ondernemingen. |
