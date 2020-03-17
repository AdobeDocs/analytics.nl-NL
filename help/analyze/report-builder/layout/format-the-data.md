---
description: Naast de standaardopmaakopties voor cellen die beschikbaar zijn via de functie Opmaken > Cellen (Ctrl+1) van Excel, kunt u beperkte opmaak toepassen op celbereiken met behulp van de rapportbuilder. Deze opmaakkeuzes zijn afhankelijk van de gekozen metrische waarde.
title: De datum opmaken
topic: Report builder
uuid: 5211db30-07b3-4413-97c3-e40e6ff223cd
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# De datum opmaken

Naast de standaardopmaakopties voor cellen die beschikbaar zijn via de functie Opmaken > Cellen (Ctrl+1) van Excel, kunt u beperkte opmaak toepassen op celbereiken met behulp van de rapportbuilder. Deze opmaakkeuzes zijn afhankelijk van de gekozen metrische waarde.

Nadat u afmetingen [aan het raster Rijlabels hebt](/help/analyze/report-builder/layout/c-metrics-dimensions/t-add-metrics-and-dimensions.md) toegevoegd, klikt u op **[!UICONTROL Format]**.

Klik in het **[!UICONTROL Format]** menu **[!UICONTROL Custom Format]** om aangepaste notaties toe te passen voor datums die lijken op de functie voor voorvoegen en uitstellen. U kunt bijvoorbeeld tekst invoeren die altijd na de datum optreedt (bijvoorbeeld A.D. B.C.E. A.H. enz.). U kunt vóór de datum tekst toevoegen, zoals [!UICONTROL Start Date] en [!UICONTROL Start and End Date]. Daarnaast kunt u een aangepaste datumexpressie maken van dag-, maand- en jaarafkortingen en een aangepast scheidingsteken gebruiken tussen delen van de datum. Alle datumnotaties moeten bestaan uit drie afkortingen die alleen tussen haakjes staan.

In de volgende tabel wordt beschreven hoe u datumafkortingen in het [!UICONTROL Custom Format] veld kunt gebruiken:

| Afkorting | Betekenis | Voorbeeld met woensdag 14 maart 2012 |
|--- |--- |--- |
| dd-MM-yyy | Volledige numerieke datum | 03/14/2012 |
| M | Aantal maanden | 3 |
| MM | Aantal maanden met 0 opvulling voor maanden &lt; 10 | 03 |
| MMM | Korte naam van de maand | mrt |
| MMMM | Lange naam van de maand | maart |
| D | Lange naam van de datum | Woensdag 14 maart 2012 |
| d | Aantal dagen | 14 |
| dd | Aantal dagen met 0 opvulling voor dagen &lt; 10 | 01 - 09 |
| ddd | Korte naam van de dag | Wed |
| dddd | Lange naam van de dag | woensdag |
| jj | Jaar met twee cijfers | 10 |
| jjjj | Volledig jaar met 4 cijfers | 2012 |
