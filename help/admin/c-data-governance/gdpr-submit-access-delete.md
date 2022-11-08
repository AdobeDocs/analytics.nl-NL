---
description: Hoe te om gegevenstoegang en schrappingsverzoeken in Adobe Analytics voor te leggen.
title: Aanvragen voor toegang en verwijdering verzenden
feature: Data Governance
exl-id: bb94cedf-ac9b-4d38-9136-bd3da2acf018
source-git-commit: ac9e4934cee0178fb00e4201cc3444d333a74052
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 93%

---

# Aanvragen voor toegang en verwijdering verzenden

Als uw klanten (consumenten/geregistreerde personen) willen weten welke data u van hen onderhoudt, of als ze besluiten dat ze uit uw Analytics-eigenschappen willen worden verwijderd, bent u als datacontroller verantwoordelijk voor het reageren op deze aanvragen. De datacontroller bepaalt hoe uw organisatie communiceert met geregistreerde personen (bijvoorbeeld via een gebruikersportal voor de geregistreerde persoon), en beheert de interactie met de geregistreerde persoon. Het is ook de verantwoordelijkheid van de datacontroller om de lus met de geregistreerde persoon te sluiten wanneer de aanvraag is uitgevoerd. Met andere woorden: Adobe Experience Cloud zal, als dataverwerker, geen aanvragen rechtstreeks van geregistreerde personen accepteren of data direct naar hen retourneren. In plaats daarvan ontvangt Adobe alleen aanvragen van u als datacontroller ontvangen en data naar u retourneren.

Misschien wilt ook zeker weten dat uw mobiele apps en websites relevante pop-upberichten en ondersteunend materiaal hebben over de rechten van geregistreerde personen in verband met hun direct of indirect identificeerbare data en andere data die u verzamelt.

## Toestemming van consumenten beheren {#section_3012015E7E8942519FB9279CF7057EAB}

U, als de gegevensbeheerder, bent verantwoordelijk voor het verkrijgen van uitdrukkelijke toestemming van de betrokkenen voordat u gegevens over hen verzamelt (mogelijk met inbegrip van Adobe Analytics-gegevens) en voor het implementeren van een [opt-out-mechanisme](https://www.adobe.com/privacy/opt-out.html#customeruse) op uw website. Hierdoor kunnen geregistreerde personen zich afmelden voor toekomstige dataverzameling in Adobe Experience Cloud.

## Gebruikers en hun data valideren {#section_AFB2CC225AA94AF6A3CE9F24EF788358}

Als datacontroller is het uw verantwoordelijkheid om te controleren of geregistreerde personen inderdaad zijn wie ze zeggen te zijn, en of ze recht hebben op de data waar ze om vragen. Verder is het uw verantwoordelijkheid om ervoor te zorgen dat de juiste data worden geretourneerd naar geregistreerde personen, en dat deze niet per ongeluk data over andere geregistreerde personen ontvangen.

Hieronder valt de controle van de data die door Adobe Analytics worden geretourneerd als onderdeel van een Data Privacy-toegangsaanvraag voordat deze naar de geregistreerde persoon wordt verzonden. Wees extra voorzichtig als u persoons-id&#39;s gebruikt, en niet alleen data retourneert waar deze id in zit, maar ook data voor andere treffers op een gedeeld apparaat waar deze id soms aanwezig is geweest. Zie [Id-uitbreiding](/help/admin/c-data-governance/gdpr-id-expansion.md).

Elk bestand combineert data uit al uw rapportsuites en verwijdert automatisch extra kopieën van gerepliceerde treffers. U kunt bepalen welke van deze bestanden naar de geregistreerde persoon moeten worden geretourneerd. Of u kunt enkele van deze data extraheren en combineren met data van andere systemen voordat u deze terugstuurt naar de geregistreerde persoon.

## Aanvragen verzenden {#submit-requests}

U kunt toegang tot gegevensprivacy verzenden en aanvragen verwijderen via onze [UI Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/overview.html) of via onze [Privacy Service-API.](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html)

>[!NOTE]
>
>De Data Privacy-API ondersteunt batchverzendingen voor meerdere gebruikers in één aanvraag. De momenteel ondersteunde limiet is 1000 afzonderlijke gebruikers (er kunnen meerdere id&#39;s per gebruiker zijn) in één JSON-aanvraagbestand.

## Voorbeeld van JSON-aanvraag {#sample-json-request}

Dit is de JSON die kan worden verzonden via de API of gebruikersinterface van Data Privacy, waarin Data Privacy-verwerking voor drie gebruikers wordt aangevraagd.

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

Er zijn in de gebruikerssectie drie blokken, die drie afzonderlijke aanvragen vertegenwoordigen, waarschijnlijk voor drie afzonderlijke geregistreerde personen.

* De eerste aanvraag is een toegangsaanvraag met een traditionele Adobe Analytics-cookie-id (AAID).
* De tweede aanvraag is ook een toegangsaanvraag, maar maakt gebruik van een MCID/ECID-cookie.
* De derde aanvraag verzoekt om zowel toegang als verwijdering voor de opgegeven id&#39;s. Hoewel id-uitbreiding is opgegeven voor alle aanvragen, heeft die de grootste invloed op deze derde aanvraag, aangezien die als enige niet-cookie-id&#39;s gebruikt. Daardoor worden in deze aanvraag ook cookie-id&#39;s ontdekt die zijn gekoppeld aan apparaten met de opgegeven CRM-id of e-mailadres, en zal de aanvraag worden uitgebreid naar deze id&#39;s.

Houd rekening met het volgende:

* De waarde “5D7236525AA6D9580A495C6C@AdobeOrg” in de sectie “companyContexts” moet worden bijgewerkt met de waarde van uw eigen Experience Cloud-organisatie.
* De velden “type” en “namespace” worden meer gedetailleerd beschreven in de sectie [Naamruimten](/help/admin/c-data-governance/gdpr-namespaces.md).
* De “description”-velden worden genegeerd.
* De “key”-velden kunnen elke door u gewenste waarde bevatten. Als u een interne id hebt die u gebruikt voor het bijhouden van Data Privacy-aanvragen, kunt u deze waarde hier plaatsen om aanvragen in het Adobe-systeem gemakkelijker te kunnen aanpassen aan aanvragen in uw eigen systemen.

## Details van reacties {#section_93F554F65DBB48A18B75EB5784056C96}

Deze secties bevatten details over reacties op toegangs- en verwijderingsaanvragen.

**Details van toegangsreacties**

De data die worden voor een toegangsaanvraag worden geretourneerd, verschaffen u als datacontroller een URL waarmee u een ZIP-bestand kunt downloaden met een map voor elk Adobe-product dat u bezit. In de map Analytics kan het volgende staan:

* Persoonsbestanden - afgeleid van treffers met een overeenkomend ID-PERSON-label

   * Een CSV-bestand met één rij voor elke overeenkomende treffer en één kolom voor elk veld met een ACC-ALL- of ACC-PERSON-label, gesorteerd op tijdstempel.
   * Een HTML-overzichtsbestand met één vermelding voor elk ACC-ALL- of ACC-PERSON-label. Bij elke vermelding worden alle unieke waarden voor dat veld vermeld, en het aantal keren dat elke waarde is voorgekomen. Velden met tijdstempels worden afgerond zodat ze alleen unieke dagen aangeven.

* Apparaatbestanden - afgeleid uit treffers waarbij een van de velden overeenkwam met een opgegeven ID-DEVICE, maar geen van deze velden overeenkwam met een opgegeven ID-PERSON

   * Een CSV-bestand met één rij voor elke overeenkomende treffer en één kolom voor elk veld met een ACC-ALL-label, gesorteerd op tijdstempel.
   * Een HTML-overzichtsbestand met één vermelding voor elk ACC-ALL-label. Bij elke vermelding worden alle unieke waarden voor dat veld vermeld, en het aantal keren dat elke waarde is voorgekomen. Velden met tijdstempels worden afgerond zodat ze alleen unieke dagen aangeven.

Elk bestand combineert data uit al uw rapportsuites en verwijdert automatisch extra kopieën van gerepliceerde treffers.

U kunt bepalen welke van deze naar de geregistreerde persoon moeten worden geretourneerd. Of u kunt enkele van deze data extraheren en combineren met data van andere systemen voordat u deze terugstuurt naar de geregistreerde persoon.

**Details van verwijderingsreacties**

Er worden data geretourneerd voor verwijderingsaanvragen, alleen een status naar de Data Privacy-API dat de aanvraag met succes is afgehandeld.

## Data Privacy-verwerking testen op uw data {#section_FBA843DBFAE64D979D8DB8A3C56784D7}

Analytics-klanten zullen doorgaans een aantal testrapportsuites instellen om de functionaliteit te controleren voordat deze voor het grote publiek wordt uitgebracht. Pre-productiewebsites of -apps verzenden data naar deze test/dev/QA-rapportsuites om te beoordelen hoe alles zal werken wanneer de code wordt uitgebracht, voordat er echte traffic naar de productierapportsuites wordt verzonden.

Bij een normale configuratie kan de verwerking van een GPDR-aanvraag echter niet eerst op deze testrapportsuites worden getest, voordat aanvragen op de productierapportsuites worden toegepast. De reden hiervoor is dat een Data Privacy-aanvraag automatisch wordt toegepast op alle rapportsuites in de Experience Cloud-organisatie, en dat zijn vaak alle rapportsuites voor uw bedrijf.

Er zijn een paar manieren waarop u toch Data Privacy-verwerking kunt testen voordat deze op alle rapportsuites wordt toegepast:

* Een optie is om een afzonderlijke Experience Cloud-organisatie in te stellen die alleen testrapportsuites bevat. Gebruik vervolgens deze Experience Cloud-organisatie voor uw Data Privacy-tests en uw normale Experience Cloud-organisatie voor daadwerkelijke Data Privacy-verwerking.
* Een andere optie is om andere naamruimten toe te wijzen aan de id&#39;s in uw testrapportsuites, in tegenstelling tot de naamruimten in uw productierapportsuites.

   U kunt bijvoorbeeld voor elke naamruimte een voorvoegsel “qa-” opgeven in uw testrapportsuites. Wanneer u Data Privacy-aanvragen verzendt met uitsluitend naamruimten met het qa-voorvoegsel, worden deze aanvragen alleen uitgevoerd op uw testrapportsuites. Later, wanneer u aanvragen verzendt zonder het qa-voorvoegsel, worden ze toegepast op uw productierapportsuites. **Dit is de aanbevolen aanpak, tenzij u de naamruimten visitorId, AAID, ECID of customVisitorId gebruikt, omdat deze in de hardware zijn gecodeerd en u er geen andere namen voor kunt opgeven in uw testrapportsuites**.
