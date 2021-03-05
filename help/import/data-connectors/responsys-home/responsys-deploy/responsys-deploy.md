---
description: Stel de Resys gegevensschakelaar voor gebruik in Adobe Analytics op.
title: De integratie implementeren
uuid: 5abf6d49-b05b-4e0f-8d9b-bb02d8f1c84a
translation-type: tm+mt
source-git-commit: 5d8032a9806836e7d0ecbd7fa3652ed1fd137e89
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 3%

---


# De integratie implementeren{#deploying-the-integration}

Deze integratie implementeren is een eenvoudig proces waarvoor de volgende acties nodig zijn:

## Voltooiing van de Tovenaar van de Integratie van Adobe{#completing-the-adobe-integration-wizard}

Stappen om de integratietovenaar in de interface van Verbindingen van Gegevens te voltooien.

1. Navigeer naar het gebied Data Connectors (voorheen Genesis) in de Adobe Experience Cloud.
1. Start de integratiewizard Resys.
1. Kies de gewenste rapportsuite en geef een naam op voor de integratie.
1. Configureer de volgende items:

   | Item | Beschrijving |
   |---|---|
   | E-mailadres | Het e-mailadres van de primaire contactpersoon |
   | Beschrijving | (Optioneel) Beschrijving voor deze integratie-instelling |
   | Account-id | Verkregen door het contacteren van het Team van de Steun Responsys in support@responsys.com |

1. Vorm de volgende **[!UICONTROL Variable Mappings]** punten:

   | Item | Beschrijving |
   |---|---|
   | Bericht-id | Selecteer een eVar voor het verzamelen van identiteitskaart van het Bericht in echt - tijd. |
   | Ontvangers-id | Selecteer een eVar voor het verzamelen van ontvangers-id&#39;s in real-time. |
   | Totaal Bounces | Selecteer een numerieke gebeurtenis om dagelijkse grenzen van Responsys te ontvangen. |
   | E-mail verzonden | Selecteer een numerieke gebeurtenis om dagelijks te ontvangen verzendt van Responsys. |
   | Geklikt | Selecteer een numerieke gebeurtenis om dagelijks totaal te ontvangen klikken van Responsys. |
   | Geopend | Selecteer een numerieke gebeurtenis om dagelijks totaal te ontvangen opent van Responsys. |
   | Abonnement opgezegd | Selecteer een numerieke gebeurtenis om dagelijks afmeldt van Responsys te ontvangen. |
   | Geleverd | Selecteer een numerieke gebeurtenis om dagelijks te ontvangen levert van Responsys. |

1. Schakel gegevenstoegang in en configureer gegevensverzameling.
   1. Wijzig zo nodig de namen van classificaties.
   1. **[!UICONTROL Partner segments]** zijn standaard remarketing segmenten die in uw integratie inbegrepen zijn.
   1. Schakel onder **[!UICONTROL Access Requests]** het selectievakje in om toe te staan dat productinformatie naar Responsys wordt geëxporteerd in dagelijkse hermarketingsegmenten.
   1. Vorm of u identiteitskaart door uw de inzamelingscode van Analytics manueel bij te werken of door de geautomatiseerde oplossing te gebruiken zult verzamelen. Als u **[!UICONTROL Automated Solution]** selecteert, moet u de parameters omvatten die in e-mailverbindingen worden gebruikt om identiteitskaart&#39;s over te gaan.
1. Herzie alle configuratiepunten en klik **[!UICONTROL Activate Now]**.

## Het vormen binnen het Systeem Responsys{#configuring-within-the-responsys-system}

Om de integratie te activeren, moet contact worden opgenomen met de ondersteuning van Responsys.

Na de voltooiing van de integratietovenaar, moet u de integratie binnen Responsys activeren.

Om dit te doen, gelieve het ondersteuningsteam te contacteren Responsys in support@responsys.com.
