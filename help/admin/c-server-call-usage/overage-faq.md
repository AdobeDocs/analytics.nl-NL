---
description: Veelgestelde vragen over Adobe Analytics-serveroproepgebruik
title: Veelgestelde vragen over serveroproepgebruik
uuid: 43340481-2e49-446b-bec7-86fcadeb4233
exl-id: a660542c-9389-4608-bc25-49831c21ceb7
source-git-commit: 9186c8d61368074cbf1df6e63bd8d3136adf0f57
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Veelgestelde vragen over serveroproepgebruik

| Vraag | Antwoord |
|--- |--- |
| V: Ik ben een analytische beheerder. Waarom zie ik geen [!UICONTROL Server Call Usage] verbinding onder de Admin sectie voor mijn login bedrijf? | A: U kunt kiezen welke van uw login bedrijven de verbinding voor [!UICONTROL Server Call Usage] onder de Admin sectie tonen. Als u het niet ziet, gelieve de Zorg van de Cliënt te contacteren om het toe te laten. |
| V: Is [!UICONTROL Server Call Usage] een alleen-beheerfunctie? | A: Nee. Enkel zoals de [!UICONTROL Billing] eigenschap die [!UICONTROL Server Call Usage] vervangt, kunt u niet-admin de toestemming toewijzen om tot deze verbinding toegang te hebben. |
| V: Zijn de [!UICONTROL Server Call Usage] en verbintenisdetails specifiek voor één login bedrijf? | A: Nee. Gebruiks- en verplichtingsgegevens die worden weergegeven, gelden voor al uw aanmeldingsbedrijven die onder uw Adobe Analytics-contract vallen. |
| V: Onder het [!UICONTROL Report Suite Usage] lusje, kan ik consumptie over rapportseries zien die niet beschikbaar voor rapportering onder het huidige login bedrijf zijn. Is dat een probleem? | A: Nee. Net als uw [!UICONTROL Server Call Usage]- en verplichtingsgegevens omvat de lijst met rapportsuites alle aanmeldingsbedrijven die u in het kader van uw Analytics-contract hebt geïmplementeerd. |
| V: Is de gebruiksperiode altijd gelijk aan de duur van mijn Analytics-contract of factureringscyclus? | A: Nee. De periode van het gebruik is de duur waarvoor uw server-vraag verplichting van toepassing is en kan van uw contracttijdlijn of factureringscyclus verschillend zijn. Uw jaarlijkse contract zou u bijvoorbeeld kunnen toestaan aan één miljard servervraag per maand, in welk geval uw verplichting één miljard servervraag zou zijn en uw gebruiksperiode één maand zou zijn. |
| V: Mijn contract bevat een verplichting voor Video Heart Beats, maar ik zie ze niet onder [!UICONTROL Server Call Usage]. Moet ik contact opnemen met de klantenservice? | A: Consumptie- en verplichtingsdetails voor hartslagen van video maken geen deel uit van [!UICONTROL Server Call Usage]. |
| V: Mijn contract omvat geen voorziening voor secundaire servervraag maar ik zie hen nog onder [!UICONTROL Current Usage] en [!UICONTROL Report Suite Usage] lusjes. Is dit een bug? | A: Nee. Hoewel uw contract niet uitdrukkelijk secundaire servervraag voorziet, kunt u hen nog veroorzaken als u in de gegevens van Analytics naar meer dan één van uw rapportreeksen verzendt. U kunt of uw implementatie herzien om ervoor te zorgen u niet in dergelijke vraag verzendt of uw Manager van de Rekening contacteren om uw contract bij te werken zodat omvat het een voorziening voor dergelijke vraag. |
| V: Mijn contract omvat geen voorziening voor secundaire servervraag maar ik zie hen nog onder [!UICONTROL Current Usage] en [!UICONTROL Report Suite Usage] lusjes. Betekent dit dat ik zal beginnen met overuren? | A: Of u zou beginnen overages te veroorzaken wanneer u in secundaire servervraag verzendt zonder voor hen wordt provisioned hangt van uw contract af. In sommige gevallen, secundair-server-vraag consumptie zou tegen uw verplichting voor primaire servervraag kunnen tellen, die hen aan een tarief sneller dan u zou voorzien vernietigen. In andere gevallen, kon u voor secundaire servervraag worden in rekening gebracht zelfs als u niet al uw primaire servervraag hebt verbruikt. Raadpleeg uw contract of neem contact op met uw accountmanager om te bevestigen. |
| V: Mijn contract/gebruiksperiode begon net, en ik ontvang reeds alarm over het overschrijden van mijn secundaire verplichting van de servervraag. Is dit een insect en zal ik overuren gaan factureren? | A: Nee. Dit zou kunnen betekenen u secundaire servervraag verbruikt zonder hen uitdrukkelijk provisioned als deel van uw contract van Adobe Analytics worden. De waarschuwing is enkel om ervoor te zorgen dat u zich hiervan bewust bent en u toe te laten om correctieve actie te nemen, indien nodig. Zie ook Veelgestelde vragen 8 hierboven. |
| V: Ik heb geen [!UICONTROL Server Call Usage] alarm gecreeerd, maar ik ontvang veelvoudige dergelijke alarm, allen met de zelfde inhoud. Is dit een bug? | A: Nee. De standaardalarm wordt teweeggebracht voor alle login bedrijven die [!UICONTROL Server Call Usage] toegelaten verbinding onder de [!UICONTROL Admin] sectie hebben. Het alarm omvat de naam van het bedrijf dat de alarm teweegbracht. Als beheerder kunt u deze waarschuwingen uitschakelen en/of verwijderen om dubbele meldingen te voorkomen, uzelf uit de lijst met ontvangers te verwijderen of de koppeling [!UICONTROL Server Call Usage] voor specifieke bedrijven uit te schakelen. |
