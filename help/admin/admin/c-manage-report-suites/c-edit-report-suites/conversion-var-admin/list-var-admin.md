---
title: Lijstvariabelen
description: Creeer en vorm lijstvariabelen voor gebruik in het melden.
feature: Admin Tools
role: Admin
exl-id: 6d9a52d4-e7f3-4bbc-bad4-55c79f30b9f7
source-git-commit: cf924b337772764b33d750787a0d09b3f11203be
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Lijstvariabelen

Creeer en vorm lijstvariabelen voor gebruik in het melden. Stel de waarden voor scheidingstekens, verlopen, toewijzing en maximum in. Gegevens verzamelen voor lijstvariabelen met [`list1` - `list3`](/help/implement/vars/page-vars/list.md).

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL List Variables]**

* **[!UICONTROL Name]**: De naam van de lijstvariabele. Deze naam is het afmetingslabel in Analysis Workspace.

* **[!UICONTROL Status]**: Schakel het verzamelen van gegevens voor deze variabele in of uit. Als een variabele is uitgeschakeld, worden geen gegevens verzameld, zelfs niet als uw implementatie gegevens naar die variabele verzendt.

* **[!UICONTROL Value Delimiter]**: Het teken dat wordt gebruikt om waarden in de lijstvariabele van elkaar te scheiden. Meestal gaat het om tekens zoals komma&#39;s, dubbele punten, pijpen of iets dergelijks. Multi-bytetekens worden niet ondersteund als scheidingstekens in lijstvariabelen.

* **[!UICONTROL Expire After]**: Net als bij het verlopen van eVar bepaalt dit veld hoeveel tijd er kan optreden tussen de lijstvariabele en de conversiegebeurtenis voor de variabele.
   * **Op paginaweergave of bezoekniveau**: Gebeurtenissen met succes na de paginaweergave of het bezoek zijn niet weer gekoppeld aan waarden in de lijstvariabele.
   * **Gebaseerd op een tijdsperiode, zoals dag, week, maand enz.**: Gebeurtenissen met succes na de opgegeven tijdsperiode worden niet gekoppeld aan waarden binnen de lijstvariabele. Ook kan een aangepast aantal dagen worden gedefinieerd.
   * **Specifieke conversiegebeurtenissen**: Eventuele andere succesgebeurtenissen die na de opgegeven specifieke gebeurtenis plaatsvinden, worden niet gekoppeld aan waarden in de lijstvariabele.
   * **Nooit**: Elke hoeveelheid tijd kan tussen de lijstvariabele en succesgebeurtenis worden doorgegeven.

* **[!UICONTROL Allocation]**: Deze instelling bepaalt hoe succesgebeurtenissen de creditering verdelen over waarden:
   * **Volledig**: Alle variabelewaarden die vóór het verlopen van de variabele zijn gedefinieerd, krijgen volledige creditering voor succesgebeurtenissen.
   * **Lineair**: Alle variabelewaarden die vóór het verstrijken van de variabele zijn gedefinieerd, krijgen krediet gedeeld krediet voor conversiegebeurtenissen.
   * Variabele waarden worden nooit overschreven, maar worden toegevoegd aan de waarden die waardering krijgen voor succesgebeurtenissen.

* **[!UICONTROL Description]**: Een beschrijving van hoe uw organisatie de lijstvariabele gebruikt.

* **[!UICONTROL Max Values]**: Hiermee geeft u aan hoeveel actieve waarden zijn toegestaan voor deze lijstvariabele. Als u bijvoorbeeld instelt op 3, worden alleen de laatste drie vastgelegde waarden opgeslagen en alle vorige vastgelegde waarden verwijderd. Merk op dat als meerdere waarden voor dezelfde lijstvariabele worden verzonden in dezelfde hit en u het gebruik van maximale waarden hebt beperkt, elke waarde dezelfde tijdstempel heeft en er geen garantie is dat de waarde wordt opgeslagen. Als een bezoeker meer waarden dan maximaal toegestaan blijft, worden de meest recente waarden gebruikt. Maximaal 250 waarden zijn toegestaan.

  Deze instelling is handig om de toewijzing te beperken tot een specifiek aantal waarden. Als een lijstvariabele bijvoorbeeld is ingesteld op `"A,B,C"` op de eerste pagina van een bezoek, dan reeks aan `"X,Y,Z"` op de volgende pagina wordt de verdeling over deze zes waarden gebaseerd op de toewijzing ervan . Als u de toewijzing wilt beperken tot alleen `"X,Y,Z"`kunt u maximale waarden instellen op drie.
