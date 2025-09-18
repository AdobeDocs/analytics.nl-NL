---
description: Combineer zowel tijdstempelgegevens als gegevens zonder tijdstempel in één rapportsuite.
title: Configuratie tijdstempels
feature: Admin Tools
uuid: 0fa63658-1cc2-4adc-8d51-a0662d0aa941
exl-id: 4d64225a-5eb8-4b7b-ba13-3cdc12dd6651
role: Admin
source-git-commit: 2d5348a4a6377313f5aab229214d97a02c826939
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Configuratie tijdstempels

Met de beheerpagina &#39;[!UICONTROL Timestamps configuration]&#39; kunt u **[!UICONTROL Timestamps optional]** inschakelen voor een of meer rapportsuites. Met deze instelling kunt u zowel tijdstempelgegevens als gegevens zonder tijdstempel combineren in één rapportsuite.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Timestamps optional]**

## Huidige tijdstempelinstelling

Deze sectie toont uw huidige timestamp configuratie voor de geselecteerde rapportreeks. Het kan één van drie mogelijke waarden zijn:

* **Tijdstempels niet toegestaan (het plaatsen `visitorID` gesteund)**
* **vereiste tijdstempels (het plaatsen `visitorID` niet gesteund)**
* **facultatieve tijdstempels (het plaatsen van `visitorID` gesteund maar niet op timestamped hits)**

Onder deze tekst bevindt zich een selectievakje met het label **[!UICONTROL Convert selected report suites to Timestamps optional]** . Selecteer dit selectievakje en selecteer vervolgens **[!UICONTROL Save]** Schakelt [!UICONTROL Timestamps optional] in voor de geselecteerde rapportsuites.

## Tijdstempels niet toegestaan

Wanneer u gegevens naar een rapportsuite verzendt met deze tijdstempelconfiguratie, wordt de hit verzonden door Adobe-verwerkingsservers. Wanneer u probeert de variabele [`timestamp`](/help/implement/vars/page-vars/timestamp.md) in te stellen, wordt de hit permanent verwijderd.

## Vereiste tijdstempels

Wanneer u gegevens naar een rapportsuite verzendt met deze tijdstempelconfiguratie, moet elke hit de variabele [`timestamp`](/help/implement/vars/page-vars/timestamp.md) bevatten. Als bij een hit een implementatievariabele `timestamp` ontbreekt, wordt de hit permanent verwijderd.

Sessiegegevens waarvoor tijdstempels zijn ingeschakeld, worden maximaal 92 dagen bewaard. Met andere woorden, een bezoek wordt 92 dagen &quot;open gehouden&quot;, zodat eventuele extra treffers kunnen worden opgenomen in hetzelfde bezoek/dezelfde sessie. Hoewel u gegevens kunt toevoegen aan bestaande sessies, raadt Adobe aan om treffers in volgorde per bezoeker toe te voegen. De beetjes die uit orde per bezoeker worden ontvangen kunnen onverwachte rapporteringsresultaten veroorzaken, hoewel veel van deze beperkingen met rapport-tijd verwerking worden verlicht.

## Tijdstempels optioneel

Het plaatsen &quot;[!UICONTROL Timestamps optional]&quot;staat u toe om over veelvoudige rapportreeksen met of zonder de [`timestamp`](/help/implement/vars/page-vars/timestamp.md) variabele te integreren en te melden. De ideale gebruiksgevallen voor [!UICONTROL Timestamps optional] zijn:

* Gegevens met tijdstempel en gegevens zonder tijdstempel mixen in dezelfde algemene rapportsuite
* Tijdstempelgegevens verzenden van een mobiele app naar een algemene rapportsuite
* Voer een upgrade uit voor apps die offline tracering gebruiken zonder dat u een nieuwe rapportsuite hoeft te maken

Deze instelling wordt standaard ingeschakeld voor alle nieuwe rapportsuites, tenzij de nieuwe rapportsuite is gekopieerd uit een rapportsuite met een andere tijdstempelconfiguratie-instelling.

>[!WARNING]
>
>Als u [!UICONTROL Timestamps optional] gebruikt, moet u [`visitorID`](/help/implement/vars/config-vars/visitorid.md) niet instellen voor gegevens met een tijdstempel. Deze actie kan tot buiten-van-ordegegevens leiden en negatief tijdberekeningen (zoals bestede tijd), attributie, bezoekaantal/bezoek tellingen, en het schilderen rapporten beïnvloeden.

Als u [!UICONTROL Timestamps optional] eenmaal hebt ingeschakeld, kunt u het niet uitschakelen in deze interface. Neem contact op met de klantenservice van Adobe in het onwaarschijnlijke scenario dat u wilt terugschakelen naar een andere configuratie-instelling voor tijdstempels.
