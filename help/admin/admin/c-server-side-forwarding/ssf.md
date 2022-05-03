---
description: Server-kant het door:sturen wordt ontworpen voor klanten die gegevens van Analytics aan andere Oplossingen van Experience Cloud in real time willen delen. Wanneer toegelaten, server-zijhet door:sturen staat ook Analytics toe om gegevens aan andere oplossingen van Experience Cloud te duwen en voor die oplossingen om gegevens aan Analytics tijdens het proces van de gegevensinzameling te duwen.
solution: Analytics
title: Overzicht van server-side doorsturen
feature: Server-Side Forwarding
exl-id: e3cd72d2-9588-4770-a7c2-64b13a1e9519
source-git-commit: aa4550d7012f76571f7623428d3d4ee08f728f64
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Overzicht van server-side doorsturen

Server-kant het door:sturen wordt ontworpen voor klanten die gegevens van Analytics aan andere Oplossingen van Experience Cloud in real time willen delen. Wanneer toegelaten, server-zijhet door:sturen staat ook Analytics toe om gegevens aan andere oplossingen van Experience Cloud te duwen en voor die oplossingen om gegevens aan Analytics tijdens het proces van de gegevensinzameling te duwen.

Server-kant het door:sturen verbetert op gegevensinzameling omdat het:

* Vermindert vraag van de pagina. Met server-kant door:sturen, [!DNL Audience Manager] klanten hoeven niet meer DIL voor gegevensinzameling te gebruiken omdat het van Analytics door:sturen. DIL verwijderen betekent een `"/event"` vraag. Minder vraag helpt paginaoplaadtijden te verbeteren, wat voor een betere klantenervaring op uw plaats maakt.
* Laat u uit gegevens voordeel halen delend onder Experience Cloud oplossingen.
* Conform onze beste praktijken voor de implementatie en implementatie van code van de Audience Manager.

>[!TIP]
>
>De huidige klanten van de Audience Manager die Analytics gebruiken zouden aan server-zijhet door:sturen moeten migreren. De nieuwe klanten van Adobe Analytics en van de Audience Manager zouden server-zijdoor:sturen (in plaats van DIL) als standaardgegevensinzameling en overdrachtmethode moeten uitvoeren.

>[!IMPORTANT]
>Op verzoek van de EU-regelgeving inzake naleving van cookies hebben de voor de verwerking verantwoordelijken (klanten van Analytics) nu de mogelijkheid om gegevens vóór de toestemming te beperken tot Adobe Analytics en te voorkomen dat deze gegevens aan de serverzijde worden doorgestuurd naar Adobe Audience Manager (AAM). Een nieuwe variabele van de implementatiecontext laat u treffers markeren waar de toestemming niet is ontvangen. Als de variabele is ingesteld, worden deze treffers niet naar AAM verzonden totdat de toestemming is ontvangen. Zie voor meer informatie [GDPR_ePrivacy-naleving en server-side doorsturen](/help/admin/admin/c-server-side-forwarding/ssf-gdpr.md).

Om te begrijpen waar uw organisatie in termen van het uitvoeren van server-kant het door:sturen is, ga door deze bevestigingsstappen:

## ![step1_icon.png, afbeelding](assets/step1_icon.png) Implementatie van ECID-service controleren

Controleer of de Experience Cloud ID-service (ECID) is geïmplementeerd door de [Verzoek voor het bijhouden van analyses](https://experienceleague.adobe.com/docs/id-service/using/implementation/test-verify.html).

Controleer op het tabblad Verzoek of er een ECID-waarde wordt ingesteld. Dit vertelt u dat de Dienst van de Identiteit correct wordt uitgevoerd, wat een noodzakelijke voorwaarde voor server-zijhet door:sturen is.

* Ga door met stap 2 als u een ECID-waarde ziet.
* Als u geen ECID-waarde ziet, [Identiteitsservice implementeren](https://experienceleague.adobe.com/docs/id-service/using/implementation/implementation-guides.html) voordat u verdergaat met stap 2.

## ![step2_icon.png, afbeelding](assets/step2_icon.png) Verifieer server-kant het door:sturen implementatieversie

Verifieer of u reeds een versie van server-zij door:sturen uitgevoerd hebt, door [het verzoek voor het bijhouden van analyses inspecteren](/help/admin/admin/c-server-side-forwarding/ssf-verify.md).

Controleer op het tabblad &quot;Reactie&quot; of de reactie gegevens van de Audience Manager bevat. Indien u ziet:

* A **JSON-reactie van Audience Manager die items bevat zoals &quot;postbacks&quot; of &quot;dcs_region&quot;**: u hebt één of andere vorm van server-kant reeds toegelaten door:sturen. Ga door met stap 3.
* De **&quot;status&quot;:&quot;SUCCESS&quot;**: u hebt de uitgevoerde Module van het Beheer van de Publiek, maar heeft server niet behoorlijk gevormd door:sturen. Ga door met stap 3.
* A **2 x 2 afbeelding**: u hebt server-kant het door:sturen niet of de uitgevoerde Module van het Beheer van de Publiek. U kunt dit als volgt corrigeren:

   * **AAM klanten met DIL**: De volgende twee items coördineren in nauwe samenhang:

      1. Verwijder de DIL-code en installeer de [Module voor publieksbeheer](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html) paginacode.
      1. Schakel het doorsturen aan de serverzijde in de UI Analytics Admin in zoals beschreven in stap 3. Als u deze instelling inschakelt voordat u de DIL-code verwijdert, worden gegevens gedupliceerd en worden aanvullende serveraanroepen met facturering naar de Audience Manager gemaakt.
   * **Nieuwe AAM** - installeer de [Module voor publieksbeheer](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html) paginacode en ga verder met stap 3. De gegevens zullen niet naar Audience Manager worden verzonden tot server-kant het door:sturen in stap 3 wordt aangezet.


## ![step3_icon.png, afbeelding](assets/step3_icon.png) Verifieer server-kant het door:sturen implementatie van rapportreeks

Verifieer of u server-kant door:sturen op het rapport-reeks niveau, eerder dan de erfenis het volgen serverbenadering hebt uitgevoerd.

Server-kant door:sturen op het rapport-reeks niveau wordt geadviseerd over de erfenis volgende serverbenadering omdat u op een fijner niveau kunt controleren welke gegevens van Analytics worden gedeeld. Het is ook een noodzakelijke voorwaarde voor deze Audience Analytics-integratie.

Ga naar **Analyse** > **Beheer** > **Rapportageopties** > (selecteer **rapportsuites**) > **Instellingen bewerken** > **Algemeen** > **Server Side Forwarding**. Als dit selectievakje is:

* **Inactief** (U kunt geen selectie maken of het menu bestaat niet): u hebt niet de geselecteerde rapportsuites in kaart gebracht aan een organisatieidentiteitskaart Neem contact op met de klantenservice om ervoor te zorgen dat de rapportsuite correct is toegewezen.
* **Uitgeschakeld**: U hebt niet de nieuwe server-kant het door:sturen aangezet. Lees de inhoud op de pagina en ga verder met het inschakelen van de functie.
* **Ingeschakeld**: U wordt provisioned voor nieuwe server-kant door:sturen. U kunt deze Audience Analytics-integratie ook instellen.

>[!NOTE]
>
>Gegevens worden niet weergegeven in andere Experience Cloud-oplossingen, zoals [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html) of [Soorten publiek](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) totdat alle drie de stappen zijn voltooid. Nadat deze instellingen zijn ingeschakeld, duurt het enkele uren voordat deze instellingen van kracht worden.
