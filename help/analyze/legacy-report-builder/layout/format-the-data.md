---
description: Leer hoe u standaard en beperkte opmaak toepast op celbereiken.
title: De datum in Report Builder opmaken
uuid: 5211db30-07b3-4413-97c3-e40e6ff223cd
feature: Report Builder
role: User, Admin
exl-id: 9b251b09-9156-40b5-8e1f-fb6594a25c26
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 3%

---

# De datum opmaken

{{legacy-arb}}

Naast de standaardopmaakopties voor cellen die beschikbaar zijn via de functie Opmaken > Cellen (Ctrl+1) van Excel, kunt u beperkte opmaak toepassen op celbereiken met Report Builder. Deze opmaakkeuzes zijn afhankelijk van de gekozen metrische waarde.

Nadat u [ afmetingen ](/help/analyze/legacy-report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) aan het net van de Etiketten van de Rij toevoegt, klik **[!UICONTROL Format]**.

Klik in het menu **[!UICONTROL Format]** op **[!UICONTROL Custom Format]** om aangepaste notaties toe te passen voor datums die lijken op de functie voor voorvoegen en uitstellen. U kunt bijvoorbeeld tekst invoeren die altijd na de datum optreedt (bijvoorbeeld A.D. B.C.E. A.H. enz.). U kunt vóór de datum tekst toevoegen, zoals [!UICONTROL Start Date] en [!UICONTROL Start and End Date] . Daarnaast kunt u een aangepaste datumexpressie maken van dag-, maand- en jaarafkortingen en een aangepast scheidingsteken gebruiken tussen delen van de datum. Alle datumnotaties moeten bestaan uit drie afkortingen die alleen tussen haakjes staan.

In de volgende tabel wordt beschreven hoe u datumafkortingen in het veld [!UICONTROL Custom Format] kunt gebruiken:

| Afkorting | Betekenis | Voorbeeld   tot en met woensdag 14 maart 2012 |
|--- |--- |--- |
| dd-MM-yyy | Volledige numerieke datum | 14-03-2012 |
| M | Aantal maanden | 3 |
| MM | Aantal maanden met 0 opvulling voor maanden &lt; 10 | 03 |
| MMM | Korte naam van maand | mrt |
| MMMM | Lange naam van de maand | maart |
| D | Lange naam van de datum | donderdag 14 maart 2012 |
| d | Aantal dagen | 14 |
| dd | Aantal dagen met 0 opvulling voor dagen &lt; 10 | 01 - 09 |
| ddd | Korte naam van de dag | Wed |
| dddd | Lange naam van de dag | woensdag |
| jj | Jaar met twee cijfers | 10 |
| jjjj | Volledig jaar met 4 cijfers | 2012 |
