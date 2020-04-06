---
description: Server-kant het door:sturen wordt ontworpen voor klanten die gegevens van Analytics aan andere Oplossingen van de Wolk van de Ervaring in echt - tijd willen delen. Wanneer toegelaten, server-zijhet door:sturen staat ook Analytics toe om gegevens aan andere oplossingen van de Wolk van de Ervaring te duwen en voor die oplossingen om gegevens aan Analytics tijdens het proces van de gegevensinzameling te duwen.
solution: Audience Manager
title: Server-kant door:sturen overzicht
uuid: 22ddbde5-6805-4eba-8f82-62772644dcaa
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Server-kant door:sturen overzicht

Server-kant het door:sturen wordt ontworpen voor klanten die gegevens van Analytics aan andere Oplossingen van de Wolk van de Ervaring in echt - tijd willen delen. Wanneer toegelaten, server-zijhet door:sturen staat ook Analytics toe om gegevens aan andere oplossingen van de Wolk van de Ervaring te duwen en voor die oplossingen om gegevens aan Analytics tijdens het proces van de gegevensinzameling te duwen.

Server-kant het door:sturen verbetert op gegevensinzameling omdat het:

* Vermindert vraag van de pagina. Met server-kant door:sturen, hoeven de [!DNL Audience Manager] klanten niet meer DIL voor gegevensinzameling te gebruiken omdat het van Analytics door:sturen. Het verwijderen van DIL betekent het elimineren van een `"/event"` vraag. Minder vraag helpt paginaoplaadtijden te verbeteren, wat voor een betere klantenervaring op uw plaats maakt.
* Hiermee kunt u gebruikmaken van gegevensuitwisseling tussen Experience Cloud-oplossingen.
* Conformeert met onze beste praktijken voor de implementatie en implementatie van code in Audience Manager.

>[!TIP]
>
>De huidige klanten van de Manager van de Publiek die Analytics gebruiken zouden aan server-zijhet door:sturen moeten migreren. De nieuwe klanten van de Analytics van Adobe en van de Manager van de Publiek zouden server-zijdoor:sturen (in plaats van DIL) als standaardgegevensinzameling en overdrachtmethode moeten uitvoeren.

>[!IMPORTANT]
>Op verzoek van de EU-regelgeving inzake naleving van cookies hebben gegevenscontrollers (klanten van Analytics) nu de mogelijkheid om gegevens vóór toestemming te beperken tot Adobe Analytics en te voorkomen dat deze gegevens op de server worden doorgestuurd naar Adobe Audience Manager (AAM). Een nieuwe variabele van de implementatiecontext laat u treffers markeren waar de toestemming niet is ontvangen. De variabele, wanneer ingesteld, voorkomt dat deze treffers naar AAM worden verzonden totdat toestemming is ontvangen. Voor meer informatie, zie naleving [GDPR_ePrivacy en server-zijhet door:sturen](/help/admin/admin/c-server-side-forwarding/ssf-gdpr.md).

Om te begrijpen waar uw organisatie in termen van het uitvoeren van server-kant het door:sturen is, ga door deze bevestigingsstappen:

## ![step1_icon.png image](assets/step1_icon.png) Verify ECID service implementation

Controleer of de service Experience Cloud ID (ECID) is geïmplementeerd door de aanvraag voor het bijhouden van [analysemogelijkheden](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-test-verify.html)te inspecteren.

Controleer op het tabblad Verzoek of er een ECID-waarde wordt ingesteld. Dit vertelt u dat de Dienst van de Identiteit correct wordt uitgevoerd, wat een noodzakelijke voorwaarde voor server-zijhet door:sturen is.

* Ga door met stap 2 als u een ECID-waarde ziet.
* Als u geen ECID-waarde ziet, [implementeert u Identiteitsservice](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-implementation-guides.html) voordat u verdergaat met stap 2.

## ![step2_icon.png image](assets/step2_icon.png) Verifieer server-side het door:sturen implementatieversie

Verifieer of u reeds een versie van server-zij het door:sturen uitgevoerd hebt, door het Analytics volgende verzoek [te](/help/admin/admin/c-server-side-forwarding/ssf-verify.md)inspecteren.

Controleer op het tabblad &quot;Reactie&quot; of de reactie gegevens van Audience Manager bevat. Indien u ziet:

* Een **JSON-reactie van Audience Manager die items bevat zoals &quot;postbacks&quot; of &quot;dcs_region&quot;**: u hebt één of andere vorm van server-kant reeds toegelaten door:sturen. Ga door met stap 3.
* De **&quot;status&quot;:&quot;SUCCESS&quot;**: u hebt de uitgevoerde Module van het Beheer van de Publiek, maar heeft server niet behoorlijk gevormd door:sturen. Ga door met stap 3.
* Een afbeelding **van** 2 x 2: u hebt server-kant het door:sturen niet of de uitgevoerde Module van het Beheer van de Publiek. U kunt dit als volgt corrigeren:

   * **AAM-klanten met DIL**: De volgende twee items coördineren in nauwe samenhang:

      1. Verwijder de DIL-code en installeer de paginacode [Audience Management Module](https://marketing.adobe.com/resources/help/en_US/aam/c_profiles_audiences.html) .
      1. Schakel het doorsturen aan de serverzijde in de UI Analytics Admin in zoals beschreven in stap 3. Als u deze instelling inschakelt voordat u DIL-code verwijdert, worden gegevens gedupliceerd en worden aanvullende serveraanroepen in rekening gebracht voor Audience Manager.
   * **Nieuwe klanten** AAM - installeer de de paginacode van de Module [van het Beheer van de](https://marketing.adobe.com/resources/help/en_US/aam/c_profiles_audiences.html) Publiek en ga aan stap 3 verder. De gegevens zullen niet naar de Manager van het Publiek worden verzonden tot server-kant het door:sturen in stap 3 wordt aangezet.


## ![step3_icon.png image](assets/step3_icon.png) Verifieer server-side het door:sturen implementatie van rapportreeks

Verifieer of u server-kant door:sturen op het rapport-reeks niveau, eerder dan de erfenis het volgen serverbenadering hebt uitgevoerd.

Server-kant door:sturen op het rapport-reeks niveau wordt geadviseerd over de erfenis volgende serverbenadering omdat u op een fijner niveau kunt controleren welke gegevens van Analytics worden gedeeld. Het is ook een noodzakelijke voorwaarde voor deze integratie van Analytics van het Publiek.

Ga naar **Analytics** > **Admin** > **Report Suites** > (selecteer **report suites**) > **Edit Settings** **** ****>General > Server Side Forwarding. Als dit selectievakje is:

* **Inactief** (U kunt geen selectie maken of het menu bestaat niet): u hebt de geselecteerde rapportsuites niet aan uw IMS Org in kaart gebracht. Zorg ervoor dat uw toepasselijke rapportensuites aan de juiste Ervaring Cloud Organisatie gebruikend de [Hulp van de Afbeelding van de Reeks van het Rapport worden in kaart gebracht UI](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/report-suite-mapping.html).
* **Uitgeschakeld**: U hebt niet de nieuwe server-kant het door:sturen aangezet. Lees de inhoud op de pagina en ga verder met het inschakelen van de functie.
* **Ingeschakeld**: U wordt provisioned voor nieuwe server-kant door:sturen. U kunt ook deze integratie voor Audience Analytics instellen.

>[!NOTE] Gegevens worden pas weergegeven in andere Experience Cloud-oplossingen, zoals [Audience Manager](https://marketing.adobe.com/resources/help/en_US/aam/c_aam_home.html) of [Publiek](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html) , als alle drie de stappen zijn voltooid. Nadat deze instellingen zijn ingeschakeld, duurt het enkele uren voordat deze instellingen van kracht worden.

