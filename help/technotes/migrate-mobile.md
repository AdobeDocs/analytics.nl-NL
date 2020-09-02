---
description: Meer informatie over het migreren van verwerkingsregels voor mobiele services naar Adobe Analytics
title: De verwerkingsregels voor mobiele services migreren naar Adobe Analytics
translation-type: tm+mt
source-git-commit: bdb6f9ba435513cd1dc3febf35eae0e821c756ca
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---


# De verwerkingsregels voor mobiele services migreren naar Adobe Analytics

Met de komende (nog onaangekondigde) onderbreking van de functionaliteit van de Mobiele Diensten van Adobe, voorziet dit document u van instructies over hoe te om het even welke extra verwerkingsregels - voorbij Metriek van de Levenscyclus - te migreren die u in Mobiele Diensten UI aan Adobe Analytics creeerde.

De verwerkingsregels worden gebruikt om waarden van de variabelen van contextgegevens naar steunen en eVars te bewegen. U kunt bijvoorbeeld de waarde van een contextgegevensvariabele voor de zoekterm in de waarde van een eVar Handelsvariabele plaatsen en die waarde bij elke hit overschrijven. Zonder verwerkingsregels hebben contextgegevensvariabelen geen betekenis en vullen ze geen rapporten in Analytics.

## Verwerkingsregels migreren

Als u mobiele services gebruikt voor aanvullende functionaliteit, zoals verwerkingsregels en rapportfuncties voor gebruik, kunt u naadloos overschakelen naar de interface Analytics (verwerkingsregels UI of Analysis Workspace) om deze functies uit te voeren. Voor Metriek van de Levenscyclus, of regels die opstelling in de UI van de verwerkingsregels van aa waren, moet u geen migratie doen. Levenscyclusstatistieken zijn &#39;out-of-box&#39;-meetgegevens die automatisch worden verzameld wanneer de Mobile SDK voor het eerst wordt geïmplementeerd in uw app.

Nochtans, als u om het even welke extra verwerkingsregels in Mobiele Diensten UI (voorbij de Metriek van de Levenscyclus) plaatst, zou u die over moeten migreren zodat u hen in Analytics kunt uitgeven/schrappen nadat u toegang tot de Mobiele Diensten verliest.

1. Meld u aan bij Experience.adobe.com en ga naar Mobiele services.
1. Klik op het tandwielpictogram van een mobiele app waarvan u contextvariabele toewijzingen naar Adobe Analytics wilt migreren.
1. Klik op het **[!UICONTROL Manage Variables and Metrics]** menu-item en vervolgens op het **[!UICONTROL Custom Variables]** tabblad. Hier, kunt u zien welke de veranderlijke afbeeldingen van de Context (contextgegevens) aan de configuratie zijn toegevoegd. Noteer deze configuraties (of neem een schermafbeelding). Voorbeeld:

   ![Contextvariabele](assets/context-var.png)

1. Schakel in Experience Cloud over naar Adobe Analytics en zorg ervoor dat u zich in dezelfde mobiele rapportsuite bevindt die u in Mobile Services hebt bekeken.
1. Ga naar Beheer > Rapportageopties > Instellingen bewerken > Algemeen > Verwerkingsregels.
1. Klik op Regel toevoegen.
1. Negeer de voorwaarden en ga verder om dezelfde contextvariabele(s) toe te voegen die/s in Mobiele diensten bestaan.

   ![Verwerkingsregel](assets/proc-rule.png)

## Melding van mobiel gebruik in Analysis Workspace

Naast mobiele metriek en dimensies (als de rapportsuite is ingeschakeld voor Mobiele services), bevat Analysis Workspace verschillende sjablonen voor mobiele projecten die de analyse kunnen vergemakkelijken:

* Berichten: Richt zich op in-app en duw overseinenprestaties.
* Locatie: Bevat een Kaart met locatiegegevens.
* Belangrijkste cijfers: Houd een impuls op de belangrijkste metriek van uw app.
* Toepassingsgebruik: Hoeveel gebruikers van apps, lanceert, en lanceert eerst app had, en wat was de gemiddelde zittingslengte?
* Overname: Hoe kunnen koppelingen voor mobiele aankopen worden uitgevoerd?
* Prestaties: Hoe presteert de app en waar hebben gebruikers problemen?
* Behoud: Wie zijn mijn loyale gebruikers en wat doen ze?
* Reizen: Wat zijn de opvallende gebruikspatronen voor mijn app?

Hier volgt een fragment van de Mobile App Usage-sjabloon:

![Gebruik van mobiele toepassingen](assets/mobile-app-usage.png)

De sjablonen openen:

1. Meld u aan bij experience.adobe.com en selecteer Analytics.
1. Zorg ervoor u in een rapportreeks bent die voor de Mobiele Diensten wordt toegelaten.
1. Klik op het tabblad Werkruimte.
1. Klik op Nieuw project maken.
1. Selecteer een van de mobiele sjablonen en klik op Maken.

## Andere functionaliteit voor mobiele services migreren

De volgende functionaliteit voor mobiele services heeft ook banden met Adobe Analytics, maar vereist een aangeschafte Adobe Analytics SKU:

* Verwervingskoppelingen
* Push Messaging
* In-app-berichten
* Beheer van locatiepunten

Als u mobiele services gebruikt voor betaalde functionaliteit, hebt u geen levensvatbaar migratiepad naar andere interne of externe tools:

* Voor de Verbindingen van de Aankoop, kunnen wij u aan de Partners van Adobe richten om aan uw behoefte te voldoen.
* Hoewel in Adobe Campaign Standard en Adobe Campaign Classic (alleen push) lettertypen voor pushberichten en in-app-berichten worden gevonden, is de onderliggende gegevensset die voor het activeren wordt gebruikt, anders en is migratie van gegevens- of berichtenactiviteit niet mogelijk.
* Voor de functionaliteit van de Plaats, wordt u aangemoedigd om de nieuwe Dienst [van de Plaats van](https://www.adobe.com/experience-platform/location-service.html)Adobe Experience Platform over te nemen, die voor alle klanten van AEP vrij is.
