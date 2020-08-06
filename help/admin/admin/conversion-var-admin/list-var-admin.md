---
title: Lijstvariabelen
description: Creeer en vorm lijstvariabelen voor gebruik in het melden.
translation-type: tm+mt
source-git-commit: 763c1b7405c1a1b3d6dbd685ce796911dd4ce78b
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 1%

---


# Lijstvariabelen

Creeer en vorm lijstvariabelen voor gebruik in het melden. Stel hier hun waarden voor scheidingstekens, verlopen, toewijzing en maximum in.

U kunt tot de configuratie in de Admin Console toegang hebben:

1. Ga naar **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**
2. Selecteer de rapportsuite.
3. Klik op  **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL List Variables]** .

* **Naam**: Elke gescheiden waarde kan maximaal 255 tekens bevatten (of minder als multi-byte tekens worden gebruikt). Dit is de maximumlengte van elk element.
* **Scheidingsteken** waarde: Het teken dat wordt gebruikt om waarden in de keuzelijst van elkaar te scheiden. Meestal gaat het om tekens zoals komma&#39;s, dubbele punten, pijpen of iets dergelijks.

   >[!NOTE]
   >
   >Multi-bytetekens worden niet ondersteund als scheidingstekens in List Vars. Het scheidingsteken moet één byte zijn.

* **Vervaldatum**: Net als bij het verlopen van de eVar, bepaalt dit de hoeveelheid tijd die tussen de Lijst Var en de omzettingsgebeurtenis kan voorkomen voor hen om worden verwant.
   * **In een paginaweergave of op bezoekniveau**: Gebeurtenissen na afloop van de paginaweergave of het bezoek zijn niet weer gekoppeld aan waarden in de lijst Var.
   * **Gebaseerd op een tijdsperiode, zoals dag, week, maand, enz**.: Gebeurtenissen met succes na de opgegeven tijdsperiode worden niet gekoppeld aan waarden binnen de List Var. Ook kan een aangepast aantal dagen worden gedefinieerd.
   * **Specifieke conversiegebeurtenissen**: Eventuele andere succesgebeurtenissen die na de opgegeven specifieke gebeurtenis plaatsvinden, worden niet gekoppeld aan waarden in de lijst Var.
   * **Nooit**: Elke hoeveelheid tijd kan tussen de gebeurtenis List Var en success worden doorgegeven.

* **Toewijzing**: Deze instelling bepaalt hoe succesgebeurtenissen de creditering verdelen over waarden:
   * **Volledig**: Alle variabelewaarden die vóór het verlopen van de variabele zijn gedefinieerd, krijgen volledige creditering voor succesgebeurtenissen.
   * **Lineair**: Alle variabele waarden die vóór de vervaldatum van de variabele zijn gedefinieerd, krijgen krediet verdeeld over conversiegebeurtenissen.
   * Variabele waarden worden nooit overschreven, maar worden toegevoegd aan de waarden die waardering krijgen voor succesgebeurtenissen.

* **Max. waarden**: Hiermee geeft u het aantal toegestane actieve waarden voor deze lijstvariabele aan. Als u bijvoorbeeld instelt op 3, worden alleen de laatste drie vastgelegde waarden opgeslagen en alle vorige vastgelegde waarden verwijderd. Merk op dat als er meerdere waarden voor dezelfde lijstvariabele worden verzonden in dezelfde hit en u het gebruik van maximale waarden hebt beperkt, elke waarde dezelfde tijdstempel heeft en er geen garantie is dat de waarde wordt opgeslagen.

Een maximum van 250 waarden wordt opgeslagen in één keer per bezoeker. Als 250 waarden per bezoeker worden overschreden, worden de recentste 250 waarden gebruikt. De vervaldatum voor deze waarden is gebaseerd op de geconfigureerde vervaldatum voor de variabele.

Met de instelling Max. waarden kunt u de toewijzing beperken tot een bepaald aantal waarden. Als een list var bijvoorbeeld op de eerste pagina van een bezoek is ingesteld op &quot;A,B,C&quot; en op de volgende pagina op &quot;X,Y,Z&quot; wordt de toewijzing verdeeld over deze zes waarden op basis van de toewijzing. Als u de toewijzing wilt beperken tot alleen &quot;X,Y,Z&quot;, kunt u maximale waarden instellen op drie.
