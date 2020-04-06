---
description: 'null'
title: Toegang verzenden en verzoeken verwijderen
uuid: d006cd5c-e3cd-4385-8683-acaf73cb681b
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Toegang verzenden en verzoeken verwijderen


## Overzicht {#section_BD70882995894C1CA19C205C49FEC23C}

Als uw klanten (consumenten/betrokkenen) willen weten welke gegevens u over hen handhaaft of beslissen zij van uw eigenschappen van Analytics willen worden geschrapt, bent u als gegevenscontrolemechanisme verantwoordelijk voor het antwoorden op die verzoeken. De gegevenscontroller bepaalt hoe uw organisatie zal communiceren met de betrokkenen (bijvoorbeeld via een gebruikersportaal voor de betrokkene) en de interactie met de betrokkene beheert. Het is ook de verantwoordelijkheid van de verwerkingsverantwoordelijke om de lus met de betrokkene te sluiten wanneer het verzoek is uitgevoerd. Met andere woorden, Adobe Experience Cloud, als de gegevensverwerker, accepteert geen aanvragen rechtstreeks van betrokkenen en retourneert geen gegevens rechtstreeks naar hen. In plaats daarvan ontvangt Adobe aanvragen van en retourneert het alleen gegevens aan u als gegevenscontroller.

Mogelijk wilt u er ook voor zorgen dat uw mobiele apps en websites relevante pop-upberichten en ondersteunend materiaal hebben over de rechten van betrokkenen met betrekking tot hun direct identificeerbare of indirect identificeerbare gegevens en andere gegevens die u verzamelt.

## Consumentengoedkeuring beheren {#section_3012015E7E8942519FB9279CF7057EAB}

U bent als gegevenscontroller verantwoordelijk voor het verkrijgen van uitdrukkelijke toestemming van de betrokkenen voordat u gegevens over de betrokkenen verzamelt (mogelijk met inbegrip van gegevens van Adobe Analytics) en voor het [implementeren van een opt-outmechanisme](https://marketing.adobe.com/resources/help/en_US/dtm/opt-in.html) op uw website. Hierdoor kunnen betrokkenen zich afmelden voor toekomstige gegevensverzameling in Adobe Experience Cloud.

## Gebruikers en hun gegevens valideren {#section_AFB2CC225AA94AF6A3CE9F24EF788358}

Als verantwoordelijke voor de verwerking bent u verantwoordelijk voor het controleren van de identiteit van de betrokkene en het recht op de gegevens die hij aanvraagt. Verder is het uw verantwoordelijkheid ervoor te zorgen dat de juiste gegevens worden teruggestuurd naar de betrokkene en dat deze niet per ongeluk gegevens over andere betrokkenen ontvangt.

Hieronder valt het controleren van de gegevens die door Adobe Analytics zijn geretourneerd als onderdeel van een aanvraag voor toegang tot Data Privacy voordat deze naar de betrokkene worden verzonden. Wees extra voorzichtig als u persoonlijke id&#39;s gebruikt en niet alleen gegevens retourneert waar die id aanwezig is, maar ook gegevens voor andere treffers op een gedeeld apparaat waar die id soms aanwezig was. Zie [Id-uitbreiding.](/help/admin/c-data-governance/gdpr-id-expansion.md)

Elk bestand combineert gegevens uit al uw rapportsuites en verwijdert automatisch extra kopieën van gerepliceerde treffers. U kunt bepalen welke van deze bestanden naar de betrokkene moeten worden geretourneerd. Of u kunt enkele van deze gegevens extraheren en combineren met gegevens van andere systemen voordat u deze terugstuurt naar de betrokkene.

## Verzoeken verzenden {#submit-requests}

U kunt toegang tot gegevensprivacy verzenden en aanvragen verwijderen via onze interface-portal [voor](https://www.adobe.io/apis/experienceplatform/gdpr/docs/alldocs.html#!api-specification/markdown/narrative/tutorials/privacy_service_tutorial/privacy_service_ui_tutorial.md) gegevensprivacy of via onze API voor [gegevensprivacy.](https://www.adobe.io/apis/experienceplatform/gdpr.html)

>[!NOTE] De Data Privacy API ondersteunt batchverzendingen voor meerdere gebruikers in één aanvraag. De momenteel ondersteunde limiet is 1000 aparte gebruikers (kan meerdere id&#39;s per gebruiker hebben) in één JSON-aanvraagbestand.

## Voorbeeld-JSON-aanvraag {#sample-json-request}

Hier is JSON die door de API of UI van de Privacy van Gegevens zou kunnen worden voorgelegd, verzoekend de verwerking van de Privacy van Gegevens voor drie gebruikers.

```
{ 
    "companyContexts": [ 
        { 
            "namespace": "imsOrgID", 
            "value": "5D7236525AA6D9580A495C6C@AdobeOrg" 
        } 
    ], 
    "users": [ 
        { 
            "key": "Data Privacy-1234", 
            "action": ["access"], 
            "userIDs": [ 
                { 
                    "namespace": "AAID", 
                    "namespaceId", 10, 
                    "type": "standard", 
                    "description": "Legacy Visitor ID", 
                    "value": "2D783E5885312539-4000010360000181", 
                } 
            ] 
        }, 
        { 
            "key": "Data Privacy-1235", 
            "action": ["access"], 
            "userIDs": [ 
                { 
                    "namespace": "ECID", 
                    "namespaceId": 4, 
                    "type": "standard", 
                    "description": "This is the ID generated by the Adobe ID service.", 
                    "value": "22470866493385587460528148368265592748", 
                } 
            ] 
        }, 
        { 
            "key": "Data Privacy-1236", 
            "action": ["access","delete"], 
            "userIDs": [ 
                { 
                    "namespace": "CRM-ID", 
                    "type": "analytics", 
                    "description": "namespace defined on eVar17 in some report suites", 
                    "value": "ACME-12345678"
                }, 
                { 
                    "namespace": "email address", 
                    "type": "analytics", 
                    "description": "namespace defined on eVar23 in some report suites", 
                    "value": "john@mail.com" 
                } 
            ] 
        } 
    ], 
    "expandIds": true 
} 
```

Er zijn drie blokken in de sectie van de gebruiker, die drie afzonderlijke verzoeken vertegenwoordigen, waarschijnlijk voor drie afzonderlijke betrokkenen.

* De eerste aanvraag is een toegangsaanvraag met een traditionele Adobe Analytics cookie ID (AID).
* Het tweede verzoek is ook een toegangsverzoek maar gebruikt een CID/ECID cookie.
* Het derde verzoek vraagt zowel toegang als schrapping voor gespecificeerde IDs. Hoewel ID-uitbreiding is opgegeven voor alle aanvragen, heeft dit de grootste invloed op dit derde verzoek, aangezien alleen niet-cookie-id&#39;s worden gebruikt. Dientengevolge, zal dit verzoek koekjesidentiteitskaarts ook ontdekken verbonden aan om het even welke apparaten met gespecificeerde CRM-identiteitskaart of e-mailadres, en zal het verzoek uitbreiden om die IDs eveneens te omvatten.

Houd er rekening mee dat

* De waarde &quot;5D7236525AA6D9580A495C6C@AdobeOrg&quot; in de sectie &quot;companyContext&quot; moet worden bijgewerkt met de waarde van uw eigen Experience Cloud-organisatie.
* De velden &quot;type&quot; en &quot;namespace&quot; worden meer gedetailleerd beschreven in de sectie [Namespaces](/help/admin/c-data-governance/gdpr-namespaces.md) .
* De velden &quot;description&quot; worden genegeerd.
* De &quot;sleutel&quot;gebieden kunnen om het even welke waarde bevatten die u wilt. Als u een interne id hebt die u gebruikt voor het bijhouden van aanvragen voor gegevensprivacy, kunt u die waarde hier plaatsen om het gemakkelijker te maken aanvragen in het systeem van Adobe aan te passen aan aanvragen in uw eigen systemen.

## Details antwoord {#section_93F554F65DBB48A18B75EB5784056C96}

Deze secties bevatten details over toegang en schrappingsreacties.

**Toegang tot reactiegegevens**

De gegevens die worden geretourneerd voor een toegangsverzoek, verschaffen u, de gegevenscontroller, een URL waarmee u een ZIP-bestand kunt downloaden dat een map bevat voor elk Adobe-product dat u bezit. In de map Analytics zijn er mogelijk:

* Personbestanden - Voortgekomen uit treffers met een overeenkomend ID-PERSON-label

   * Een CSV-bestand met één rij voor elke overeenkomende hit en één kolom voor elk veld met een ACC-ALL- of ACC-PERSON-label, gesorteerd op tijdstempel.
   * Een HTML-samenvattingsbestand met één item voor elk ACC-ALL- of ACC-PERSON-label. Bij elk item worden alle unieke waarden voor dat veld weergegeven, evenals het aantal keren dat elke waarde is opgetreden. Velden met tijdstempels worden afgerond om alleen unieke dagen op te geven.

* Apparaatbestanden - Voortgekomen uit resultaten waarbij een van de velden een bepaald ID-APPARAAT had, maar geen van deze velden een overeenkomende ID-PERSON had

   * Een CSV-bestand met één rij voor elke overeenkomende hit en één kolom voor elk veld met een ACC-ALL-label, gesorteerd op tijdstempel.
   * HTML-overzichtsbestand met één item voor elk ACC-ALL-label. Bij elk item worden alle unieke waarden voor dat veld vermeld, evenals het aantal keren dat elke waarde is opgetreden. Velden met tijdstempels worden afgerond om alleen unieke dagen op te geven.

Elk bestand combineert gegevens uit al uw rapportsuites en verwijdert automatisch extra kopieën van gerepliceerde treffers.

U kunt bepalen welke van deze om aan de betrokkene terug te komen. Of u kunt enkele van deze gegevens extraheren en combineren met gegevens van andere systemen voordat u deze terugstuurt naar de betrokkene.

**Details van reactie verwijderen**

Er worden geen gegevens geretourneerd voor verwijderingsaanvragen - alleen een status voor de Data Privacy API die aan de aanvraag is toegewezen.

## Gegevensprivacyverwerking testen op uw gegevens {#section_FBA843DBFAE64D979D8DB8A3C56784D7}

Klanten van Analytics zullen doorgaans een aantal testrapporten instellen om de functionaliteit te controleren voordat deze aan het grote publiek wordt uitgebracht. Websites of toepassingen die aan de productie voorafgaan, verzenden gegevens naar deze evaluatiereeksen voor test/dev/QA-rapporten om te beoordelen hoe de zaken werken wanneer de code wordt uitgebracht voordat echt verkeer naar de reeksen van het productierapport wordt verzonden.

Bij een normale configuratie kan de verwerking van een GPDR-aanvraag echter niet eerst op deze testreeksen worden getest voordat aanvragen op de reeksen van het productieverslag worden ingediend. De reden hiervoor is dat een verzoek van de Privacy van Gegevens automatisch wordt toegepast op alle rapportreeksen in de organisatie van de Wolk van de Ervaring, die vaak alle rapportreeksen voor uw bedrijf is.

Er zijn een paar manieren dat u nog steeds uw verwerking van de Privacy van Gegevens kunt testen alvorens het op al uw rapportseries toe te passen:

* U kunt onder andere een aparte Experience Cloud-organisatie instellen die alleen testrapporten bevat. Gebruik vervolgens deze Experience Cloud-organisatie voor het testen van uw gegevensprivacy en uw normale Experience Cloud-organisatie voor de daadwerkelijke verwerking van gegevensprivacy.
* Een andere optie is verschillende naamruimten toe te wijzen aan de id&#39;s in uw testreeks van het testrapport, in tegenstelling tot de naamruimten in uw productierapporten.

   U kunt bijvoorbeeld voor elke naamruimte een &quot;qa-&quot; opgeven in de reeks testrapporten. Wanneer u de verzoeken van de Privacy van Gegevens met slechts namespaces met het qa prefix voorlegt, zullen deze verzoeken slechts tegen uw reeksen van het testrapport lopen. Later, wanneer u verzoeken indient zonder het qa prefix, zullen zij op uw reeksen van het productierapport van toepassing zijn. **Dit is de geadviseerde benadering, tenzij u bezoekerId, AID, ECID of customVisitorId namespaces gebruikt, omdat deze hardcoded zijn en u kunt geen afwisselende namen voor hen in uw reeksen** van het testrapport specificeren.
