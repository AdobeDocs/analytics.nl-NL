---
title: Lijstvariabelen
description: Creeer en vorm lijstvariabelen voor gebruik in het melden.
feature: Admin Tools
role: Admin
exl-id: 6d9a52d4-e7f3-4bbc-bad4-55c79f30b9f7
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Lijstvariabelen

Creeer en vorm lijstvariabelen voor gebruik in het melden. Stel de waarden voor scheidingstekens, verlopen, toewijzing en maximum in. Verzamel gegevens voor lijstvariabelen met behulp van [`list1` - `list3`](/help/implement/vars/page-vars/list.md) .

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL List Variables]**

* **[!UICONTROL Name]**: De naam van de lijstvariabele. Deze naam is het afmetingslabel in Analysis Workspace.

* **[!UICONTROL Status]**: het verzamelen van gegevens voor deze variabele in- of uitschakelen. Als een variabele is uitgeschakeld, worden geen gegevens verzameld, zelfs niet als uw implementatie gegevens naar die variabele verzendt.

* **[!UICONTROL Value Delimiter]**: Het teken dat wordt gebruikt om waarden in de lijstvariabele van elkaar te scheiden. Meestal gaat het om tekens zoals komma&#39;s, dubbele punten, pijpen of iets dergelijks. Multi-bytetekens worden niet ondersteund als scheidingstekens in lijstvariabelen.

* **[!UICONTROL Expire After]**: Net als bij eVar-vervaldatum bepaalt dit veld hoeveel tijd er kan optreden tussen de lijstvariabele en de conversiegebeurtenis voordat deze kan worden gekoppeld.
   * **bij een paginamening of bezoek niveau**: De gebeurtenissen van het succes voorbij de paginamening of het bezoek zouden niet terug met om het even welke waarden binnen de lijstvariabele verbinden.
   * **Gebaseerd op een tijdspanne, zoals dag, week, maand, enz.**: De gebeurtenissen van het succes voorbij de gespecificeerde tijdspanne zouden niet terug naar om het even welke waarden binnen de lijstvariabele verbinden. Ook kan een aangepast aantal dagen worden gedefinieerd.
   * **Specifieke omzettingsgebeurtenissen**: Om het even welke andere succesgebeurtenissen die na de specifieke aangewezen gebeurtenis in brand steken zouden niet terug naar om het even welke waarden binnen de lijstvariabele verbinden.
   * **nooit**: Om het even welke hoeveelheid tijd kan tussen de lijstvariabele en succesgebeurtenis overgaan.

* **[!UICONTROL Allocation]**: deze instelling bepaalt hoe succesgebeurtenissen de creditering tussen waarden verdelen:
   * **Volledig**: Alle veranderlijke die waarden vóór de vervaldatum van de variabele worden bepaald krijgen volledige krediet voor succesgebeurtenissen.
   * **Lineair**: Alle veranderlijke waarden die vóór de vervaldatum van de variabele worden bepaald krijgen krediet verdeelde kredieten voor omzettingsgebeurtenissen.
   * Variabele waarden worden nooit overschreven, maar worden toegevoegd aan de waarden die waardering krijgen voor succesgebeurtenissen.

* **[!UICONTROL Description]**: Een beschrijving van hoe uw organisatie de lijstvariabele gebruikt.

* **[!UICONTROL Max Values]**: geeft het aantal toegestane actieve waarden voor deze lijstvariabele aan. Als u bijvoorbeeld instelt op 3, worden alleen de laatste drie vastgelegde waarden opgeslagen en alle vorige vastgelegde waarden verwijderd. Merk op dat als meerdere waarden voor dezelfde lijstvariabele worden verzonden in dezelfde hit en u het gebruik van maximale waarden hebt beperkt, elke waarde dezelfde tijdstempel heeft en er geen garantie is dat de waarde wordt opgeslagen. Als een bezoeker meer waarden dan maximaal toegestaan blijft, worden de meest recente waarden gebruikt. Maximaal 250 waarden zijn toegestaan.

  Deze instelling is handig om de toewijzing te beperken tot een specifiek aantal waarden. Als een lijstvariabele bijvoorbeeld op de eerste pagina van een bezoek is ingesteld op `"A,B,C"` en op de volgende pagina op `"X,Y,Z"` is ingesteld, wordt de toewijzing verdeeld over deze zes waarden op basis van de toewijzing. Als u de toewijzing wilt beperken tot alleen `"X,Y,Z"` , kunt u maximale waarden instellen op drie.
