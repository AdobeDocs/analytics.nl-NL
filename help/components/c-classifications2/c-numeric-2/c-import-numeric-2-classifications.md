---
description: Het import- en exportbestand bevat zes kolommen voor elke numerieke 2-classificatie.
subtopic: Classifications
title: Numerieke 2 classificaties importeren
topic: Admin tools
uuid: 82a3034c-e002-4991-900f-22dd45d54910
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Numerieke 2 classificaties importeren

>[!IMPORTANT]
>
>De mogelijkheid om classificaties met numerieke waarden 2 en datum in te voeren is uit de codebase verwijderd. Deze wijziging wordt van kracht met ingang van het onderhoudscontract van juli 2019. Als u Numerieke of Datum-Toegelaten kolommen in uw de invoerdossier hebt, zullen die cellen stil worden genegeerd, en om het even welke andere gegevens binnen dat dossier zullen worden ingevoerd als normaal. Bestaande classificaties kunnen nog steeds worden geëxporteerd via de standaardclassificatieworkflow en blijven beschikbaar in de rapportage.

Het import- en exportbestand bevat zes kolommen voor elke numerieke 2-classificatie.

De volgende definities veronderstellen dat uw numerieke 2 classificatienaam MyCost is.

**~MijnKosten:** Een beschrijvende naam voor de rij.

**~MijnKosten^~id~:** De id voor het bewerken van een bestaande rij. Wanneer u een nieuwe rij toevoegt, moet deze leeg zijn. Er wordt automatisch een id toegewezen wanneer u exporteert vanuit classificatiebeheer.

**~MijnKosten^~waarde~:** De waarde voor de rij. Als de tariefkolom vast is, dan is dit een vlakke waarde die over de gehele periode wordt verdeeld. Als de tariefkolom een gebeurtenis is, dan is dit de vermenigvuldiger voor die gebeurtenis. Deze vermelding mag geen komma&#39;s bevatten.

**~MijnKosten^~punt~:** De tijdsperiode waarop deze rij betrekking heeft. Dit moet een begin- en einddatum bevatten, gescheiden door een streepje. Het streepje moet in ruimten zijn ingesloten. De definitie moet als volgt worden opgemaakt:

YYYY/MM/DD - YYYY/MM/DD

**~MijnKosten^~rate~:** De gebeurtenis die met de [!UICONTROL Value] kolom moet worden vermenigvuldigd. Geldige waarden zijn:

* vast - gebruikt om aan te geven dat de waarde een forfaitaire waarde is die over de periode moet worden gespreid.
* inkomsten
* bestellen
* eenheid
* scopen
* scviews
* instance
* klikken
* uitchecken
* scheuren
* scremove
* gebeurtenis 1
* gebeurtenis 2
* enz.

**~MyCost^~hinge~:** De gebeurtenis die moet worden gebruikt om de waarde te verdelen tijdens een uitsplitsing. Deze waarde is vaak gelijk aan de [!UICONTROL ~MyCost^~frequentie~], tenzij u [!UICONTROL fixed]. De geldige waarden voor deze kolom zijn gelijk aan die van [!UICONTROL ~MyCost^~tarief~], met toevoeging van [!UICONTROL none].
