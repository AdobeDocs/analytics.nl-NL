---
description: Adobe Analytics Server Call Usage FAQ
title: Veelgestelde vragen over serveroproepgebruik
feature: Server Call Usage
exl-id: a660542c-9389-4608-bc25-49831c21ceb7
source-git-commit: 72bd67179e003b70233d863d34153fec77548256
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Server Call Usage FAQ

| Vraag | Antwoord |
|--- |--- |
| V: Ik ben een analytische beheerder. Waarom zie ik geen [!UICONTROL Server Call Usage] koppeling onder de sectie Admin voor mijn aanmeldingsbedrijf? | A: U kunt kiezen voor welke aanmeldbedrijven de koppeling wordt weergegeven voor [!UICONTROL Server Call Usage] onder de sectie Beheer. Als u het niet ziet, gelieve de Zorg van de Cliënt te contacteren om het toe te laten. |
| Q: Is [!UICONTROL Server Call Usage] an Admin-only feature? | A: No. Just like the [!UICONTROL Billing] feature that [!UICONTROL Server Call Usage] replaces, you can assign a non-admin the permission to access this link. |
| V: zijn [!UICONTROL Server Call Usage] en de verbintenisdetails specifiek voor één login bedrijf? | A: No. Usage and commitment details displayed span all your login companies governed by your Adobe Analytics contract. |
| V: Onder de [!UICONTROL Report Suite Usage] tab, kan ik consumptie over rapportreeksen zien die niet voor rapportering onder het huidige login bedrijf beschikbaar zijn. Is dat een probleem? | A: Nee. Net als uw [!UICONTROL Server Call Usage] en de verbintenisdetails, omvat de lijst van rapportreeksen alle login bedrijven u in het kader van uw contract van de Analyse hebt uitgevoerd. |
| Q: Is the usage period always the same as the duration of my Analytics contract or billing cycle? | A: No. Usage period is the duration for which your server-call commitment is applicable and may be different from your contract time line or billing cycle. Uw jaarlijkse contract zou u bijvoorbeeld kunnen toestaan aan één miljard servervraag per maand, in welk geval uw verplichting één miljard servervraag zou zijn en uw gebruiksperiode één maand zou zijn. |
| Q: My contract includes a commitment for Video Heart Beats but I do not see them under [!UICONTROL Server Call Usage]. Moet ik contact opnemen met de klantenservice? | A: Consumptie- en verplichtingsdetails voor Video Heart Mats maken geen deel uit van [!UICONTROL Server Call Usage]. |
| Q: My contract does not include a provision for secondary server calls but I still see them under the [!UICONTROL Current Usage] and [!UICONTROL Report Suite Usage] tabs. Is this a bug? | A: Nee. Hoewel uw contract niet uitdrukkelijk secundaire servervraag voorziet, kunt u hen nog veroorzaken als u in de gegevens van Analytics naar meer dan één van uw rapportreeksen verzendt. U kunt of uw implementatie herzien om ervoor te zorgen u niet in dergelijke vraag verzendt of uw Manager van de Rekening contacteren om uw contract bij te werken zodat omvat het een voorziening voor dergelijke vraag. |
| V: Mijn contract omvat geen voorziening voor secundaire servervraag maar ik zie hen nog onder [!UICONTROL Current Usage] en [!UICONTROL Report Suite Usage] tabs. Betekent dit dat ik zal beginnen met overuren? | A: Whether you would start incurring overages when you send in secondary server calls without being provisioned for them depends on your contract. In sommige gevallen, secundair-server-vraag consumptie zou tegen uw verplichting voor primaire servervraag kunnen tellen, die hen aan een tarief sneller dan u zou voorzien vernietigen. In andere gevallen, kon u voor secundaire servervraag worden in rekening gebracht zelfs als u niet al uw primaire servervraag hebt verbruikt. Raadpleeg uw contract of neem contact op met uw accountmanager om te bevestigen. |
| V: Mijn contract/gebruiksperiode begon net, en ik ontvang reeds alarm over het overschrijden van mijn secundaire verplichting van de servervraag. Is dit een insect en zal ik overuren gaan factureren? | A: Nee. This could mean you are consuming secondary server calls without them being explicitly provisioned as part of your Adobe Analytics contract. The alert is simply to ensure that you are aware of this and to enable you to take corrective action, if needed. Zie ook Veelgestelde vragen 8 hierboven. |
| Q: I did not create any [!UICONTROL Server Call Usage] alerts, but I am receiving multiple such alerts, all with the same content. Is dit een bug? | A: No. De standaardalarm wordt teweeggebracht voor alle login bedrijven die hebben [!UICONTROL Server Call Usage] koppeling ingeschakeld onder [!UICONTROL Admin] sectie. Het alarm omvat de naam van het bedrijf dat de alarm teweegbracht. As an Admin, you can disable and/or delete these alerts to avoid duplicates, remove yourself from the list of recipients, or have Customer Care disable the [!UICONTROL Server Call Usage] link for specific companies. |
