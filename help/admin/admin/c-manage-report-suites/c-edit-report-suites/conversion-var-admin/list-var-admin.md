---
title: Lijstvariabelen
description: Creeer en vorm lijstvariabelen voor gebruik in het melden.
feature: Admin Tools
role: Admin
exl-id: 6d9a52d4-e7f3-4bbc-bad4-55c79f30b9f7
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Lijstvariabelen

Creeer en vorm lijstvariabelen voor gebruik in het melden. Stel de waarden voor scheidingstekens, verlopen, toewijzing en maximum in.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Finding Methods]**

* **Naam**: Elke gescheiden waarde kan maximaal 255 tekens bevatten (of minder als multi-byte tekens worden gebruikt). Dit is de maximumlengte van elk element.
* **Scheidingsteken waarde**: Het teken dat wordt gebruikt om waarden in de keuzelijst van elkaar te scheiden. Meestal gaat het om tekens zoals komma&#39;s, dubbele punten, pijpen of iets dergelijks.

  >[!NOTE]
  >
  >Multi-bytetekens worden niet ondersteund als scheidingstekens in List Vars. Het scheidingsteken moet één byte zijn.

* **Verlopen**: Net als bij het verlopen van eVar bepaalt dit veld hoeveel tijd er kan optreden tussen de List Var en de conversiegebeurtenis voor de koppeling.
   * **Op paginaweergave of bezoekniveau**: Gebeurtenissen met succes na de paginaweergave of het bezoek zijn niet weer gekoppeld aan waarden in de lijst Var.
   * **Gebaseerd op een tijdsperiode, zoals dag, week, maand enz.**: Gebeurtenissen met succes na de opgegeven tijdsperiode worden niet gekoppeld aan waarden binnen de List Var. Ook kan een aangepast aantal dagen worden gedefinieerd.
   * **Specifieke conversiegebeurtenissen**: Eventuele andere succesgebeurtenissen die na de opgegeven specifieke gebeurtenis worden uitgevoerd, worden niet gekoppeld aan waarden in de lijst Var.
   * **Nooit**: U kunt elke hoeveelheid tijd tussen de gebeurtenis List Var en success doorgeven.

* **Toewijzing**: Deze instelling bepaalt hoe succesgebeurtenissen de creditering verdelen over waarden:
   * **Volledig**: Alle variabelewaarden die vóór het verlopen van de variabele zijn gedefinieerd, krijgen volledige creditering voor succesgebeurtenissen.
   * **Lineair**: Alle variabelewaarden die vóór het verstrijken van de variabele zijn gedefinieerd, krijgen krediet gedeeld krediet voor conversiegebeurtenissen.
   * Variabele waarden worden nooit overschreven, maar worden toegevoegd aan de waarden die waardering krijgen voor succesgebeurtenissen.

* **Max. waarden**: Hiermee geeft u aan hoeveel actieve waarden zijn toegestaan voor deze lijstvariabele. Als u bijvoorbeeld instelt op 3, worden alleen de laatste drie vastgelegde waarden opgeslagen en alle vorige vastgelegde waarden verwijderd. Merk op dat als er meerdere waarden voor dezelfde lijstvariabele worden verzonden in dezelfde hit en u het gebruik van maximale waarden hebt beperkt, elke waarde dezelfde tijdstempel heeft en er geen garantie is dat de waarde wordt opgeslagen.

Een maximum van 250 waarden wordt opgeslagen in één keer per bezoeker. Als 250 waarden per bezoeker worden overschreden, worden de recentste 250 waarden gebruikt. De vervaldatum voor deze waarden is gebaseerd op de geconfigureerde vervaldatum voor de variabele.

Met de instelling Max. waarden kunt u de toewijzing beperken tot een bepaald aantal waarden. Als een list var bijvoorbeeld op de eerste pagina van een bezoek is ingesteld op &quot;A,B,C&quot; en op de volgende pagina op &quot;X,Y,Z&quot; wordt de toewijzing verdeeld over deze zes waarden op basis van de toewijzing. Als u de toewijzing wilt beperken tot alleen &quot;X,Y,Z&quot;, kunt u maximale waarden instellen op drie.
