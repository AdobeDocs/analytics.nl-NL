---
description: Server-kant het door:sturen wordt ontworpen voor klanten die gegevens van Analytics aan andere Oplossingen van Experience Cloud in real time willen delen. Wanneer toegelaten, server-zijhet door:sturen staat ook Analytics toe om gegevens aan andere oplossingen van Experience Cloud te duwen en voor die oplossingen om gegevens aan Analytics tijdens het proces van de gegevensinzameling te duwen.
solution: Analytics
title: Server-kant door:sturen overzicht
feature: Report Suite Settings
exl-id: e3cd72d2-9588-4770-a7c2-64b13a1e9519
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Server-kant door:sturen overzicht

Server-kant het door:sturen wordt ontworpen voor klanten die gegevens van Analytics aan andere Oplossingen van Experience Cloud in real time willen delen. Wanneer toegelaten, server-zijhet door:sturen staat ook Analytics toe om gegevens aan andere oplossingen van Experience Cloud te duwen en voor die oplossingen om gegevens aan Analytics tijdens het proces van de gegevensinzameling te duwen.

Server-kant het door:sturen verbetert op gegevensinzameling omdat het:

* Vermindert vraag van de pagina. Met server-kant door:sturen, hoeven de klanten van [!DNL Audience Manager] niet meer DIL voor gegevensinzameling te gebruiken omdat het van Analytics door:sturen. Als u DIL verwijdert, verwijdert u een `"/event"` -aanroep. Minder vraag helpt paginaoplaadtijden te verbeteren, wat voor een betere klantenervaring op uw plaats maakt.
* Hiermee kunt u gebruikmaken van gegevensuitwisseling tussen Experience Cloud-oplossingen.
* Conform onze best practices voor Audience Manager-code-implementatie en -implementatie.

>[!TIP]
>
>De huidige klanten van Audience Manager die Analytics gebruiken zouden aan server-zijhet door:sturen moeten migreren. De nieuwe klanten van Adobe Analytics en van Audience Manager zouden server-zijdoor:sturen (in plaats van DIL) als standaardgegevensinzameling en overdrachtmethode moeten uitvoeren.

>[!IMPORTANT]
>Op verzoek van de EU-regelgeving inzake naleving van cookies hebben de voor de verwerking verantwoordelijken (klanten van Analytics) nu de mogelijkheid om gegevens vóór de toestemming te beperken tot Adobe Analytics en te voorkomen dat deze gegevens aan de serverzijde naar Adobe Audience Manager worden doorgestuurd. Met een nieuwe variabele voor de implementatiecontext kunt u treffers markeren op plaatsen waar geen toestemming is ontvangen. Als de variabele is ingesteld, worden deze treffers niet naar Adobe Audience Manager verzonden totdat de toestemming is ontvangen. Voor meer informatie, zie [ naleving GDPR_ePrivacy en server-zij het door:sturen ](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-gdpr.md).

Om te begrijpen waar uw organisatie in termen van het uitvoeren van server-kant het door:sturen is, ga door deze bevestigingsstappen:

## ![ step1_icon.png beeld ](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/assets/step1_icon.png) verifieert ECID de dienstimplementatie

Verifieer of de dienst van identiteitskaart van Experience Cloud (ECID) wordt uitgevoerd, door het [ Analytics volgende verzoek ](https://experienceleague.adobe.com/docs/id-service/using/implementation/test-verify.html) te inspecteren.

Controleer op het tabblad Verzoek of er een ECID-waarde wordt ingesteld. Dit vertelt u dat de Dienst van de Identiteit correct wordt uitgevoerd, wat een noodzakelijke voorwaarde voor server-zijhet door:sturen is.

* Ga door met stap 2 als u een ECID-waarde ziet.
* Als u geen ECID waarde ziet, [ voert de Dienst van de Identiteit uit ](https://experienceleague.adobe.com/docs/id-service/using/implementation/implementation-guides.html) alvorens aan stap 2 te werk te gaan.

## ![ step2_icon.png beeld ](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/assets/step2_icon.png) verifieer server-kant het door:sturen implementatieversie

Verifieer of u reeds een versie van server-zij door:sturen uitgevoerd hebt, door [ het Analytics volgende verzoek ](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-verify.md) te inspecteren.

Controleer op het tabblad &quot;Reactie&quot; of de reactie Audience Manager-gegevens bevat. Indien u ziet:

* A **JSON reactie van Audience Manager die punten zoals &quot;postbacks&quot;of &quot;dcs_region&quot;omvat**: u hebt één of andere vorm van server-zij reeds toegelaten door:sturen. Ga door met stap 3.
* De **&quot;status&quot;:&quot;SUCCESS&quot;**: u hebt de Gedragsbeheermodule van het Publiek uitgevoerd, maar heeft server niet behoorlijk gevormd door:sturen. Ga door met stap 3.
* A **2 x 2 beeld**: u hebt niet server-kant het door:sturen of de uitgevoerde Module van het Beheer van de Publiek. U kunt dit als volgt corrigeren:

   * **de Klanten van Adobe Audience Manager met DIL**: coördineer de volgende twee punten in nauw verband:

      1. Verwijder de code van DIL en installeer de [ paginacode van de Module van het Beheer van het publiek 0&rbrace;.](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html)
      1. Schakel het doorsturen aan de serverzijde in de UI Analytics Admin in zoals beschreven in stap 3. Als u deze instelling inschakelt voordat u DIL-code verwijdert, worden gegevens gedupliceerd en worden aanvullende serveraanroepen in rekening gebracht naar Audience Manager.

   * **Nieuwe klanten van Adobe Audience Manager** - installeer de [ 3&rbrace; paginacode van de Module van het Beheer van de Publiek &lbrace;en ga verder met stap 3. ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/audience-management-module.html) De gegevens worden pas naar Audience Manager verzonden wanneer in stap 3 het doorsturen van de server is ingeschakeld.

## ![ step3_icon.png beeld ](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/assets/step3_icon.png) verifieer server-kant het door:sturen implementatie van rapportreeks

Verifieer of u server-kant door:sturen op het rapport-reeks niveau, eerder dan de erfenis het volgen serverbenadering hebt uitgevoerd.

Server-kant door:sturen op het rapport-reeks niveau wordt geadviseerd over de erfenis volgende serverbenadering omdat u op een fijner niveau kunt controleren welke gegevens van Analytics worden gedeeld. Het is ook een noodzakelijke voorwaarde voor deze Audience Analytics-integratie.

Ga naar **Analytics** > **Admin** > **de Reeksen van het Rapport** > (selecteren **rapportreeksen**) > **geeft Montages** > **Algemene** > **de Kant van de Server door:sturen** uit. Als dit selectievakje is:

* **Inactief** (U kunt geen selectie maken of het menu bestaat niet): u hebt niet de geselecteerde rapportsuites in kaart gebracht aan een organisatieidentiteitskaart. Neem contact op met de klantenservice om ervoor te zorgen dat de rapportsuite correct is toegewezen.
* **Gehandicapten**: U hebt niet de nieuwe server-kant het door:sturen aangezet. Lees de inhoud op de pagina en ga verder met het inschakelen van de functie.
* **Toegelaten**: U wordt provisioned voor het nieuwe server-zij door:sturen. U kunt deze Audience Analytics-integratie ook instellen.

>[!NOTE]
>
>De gegevens zullen niet in andere oplossingen van Experience Cloud, zoals [ Audience Manager ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html) of [ Soorten van publiek ](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) verschijnen tot alle 3 stappen volledig zijn. Nadat deze instellingen zijn ingeschakeld, duurt het enkele uren voordat deze instellingen van kracht worden.
