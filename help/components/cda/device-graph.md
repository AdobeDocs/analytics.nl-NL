---
title: Apparaatgrafiek
description: Begrijp de eerste vereisten en de beperkingen van het stitching van gegevens gebruikend de apparatengrafiek.
translation-type: tm+mt
source-git-commit: eb2bee26dd58dcff13b4ddf41c6f6ab337d8d374
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 2%

---


# Apparaatgrafiek

Analytics voor verschillende apparaten biedt twee verschillende methoden om gegevens aan elkaar te koppelen. Deze methode gebruikt de de coopgrafiek van de Dienst van de Identiteit van het Adobe Experience Platform of PrivéGrafiek om gegevens samen te binden. CDA communiceert regelmatig met de apparatengrafiek om apparaten samen te verbinden.

## Verschillen tussen co-op grafiek en privé grafiek

Adobe biedt twee typen apparaatgrafieken als onderdeel van de id-service:

* **Grafiek** naast elkaar: Een opslagplaats van hashed apparaat ID&#39;s die om het even welke klant kan bijdragen tot en van verwijzingen voorzien. Aangezien dit type apparaatgrafiek een gezamenlijke grafiek is, komt deze meestal overeen met meer apparaten dan een persoonlijke grafiek.
* **Privégrafiek**: Een opslagplaats van hashed apparaat ID&#39;s die slechts uw organisatie van verwijzingen voorziet.

## Specifieke voorwaarden voor de apparaatgrafiek

Als u Analytics voor verschillende apparaten wilt implementeren met de grafiekmethode van het apparaat, is het volgende vereist. Werk met teams binnen uw organisatie en uw accountmanager van Adobe om ervoor te zorgen dat u aan alle volgende voorwaarden voldoet.

>[!IMPORTANT] Als niet aan alle voorwaarden wordt voldaan, kan het zijn dat Analytics voor verschillende apparaten niet kan worden ingeschakeld of dat de gegevens niet correct worden opgeslagen.

* Alle voorwaarden die op de [overzichtspagina](overview.md)worden vermeld.
* Uw organisatie moet de Coop Grafiek van de Dienst van de Identiteit van het Adobe Experience Platform of PrivéGrafiek gebruiken. Zie de [startpagina](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) in de gebruikershandleiding voor apparaatcoop.
* Voor uw implementatie moet de nieuwste versie van de Experience Cloud ID Service worden gebruikt. Zie de [startpagina](https://docs.adobe.com/content/help/nl-NL/id-service/using/home.html) in de gebruikershandleiding van de Experience Cloud Identity Service. De meeste implementaties die gebruikmaken van het Adobe Experience Platform Launch hebben waarschijnlijk al ECID geïmplementeerd.
* Uw implementatie moet de `setCustomerIDs` functie (of het equivalent van SDK) aanroepen wanneer een individu kan worden geïdentificeerd, zoals wanneer een gebruiker zich aanmeldt of een e-mail opent. Deze eis geldt voor alle platforms, inclusief mobiele apps indien gebruikt. Zie [`setCustomerIDs`](https://docs.adobe.com/content/help/en/id-service/using/id-service-api/methods/setcustomerids.html) de gebruikershandleiding van de Experience Cloud Identity Service.

## Specifieke beperkingen voor de apparaatgrafiek

* Verouderde Analytics-id&#39;s worden niet ondersteund. Alleen bezoekers met Experience Cloud-id&#39;s zijn gebonden.
* Als uw organisatie een Privé Grafiek gebruikt, nemen de nieuwe apparaten tot 24 uren om worden vastgemaakt.
* Als uw organisatie de Co-op grafiek gebruikt, kunnen nieuwe apparaten die uw plaats bezoeken tot twee weken duren om te stikken. De mate van stitching in CDA voor de meest recente twee weken is doorgaans lager dan voor datumbereiken die ouder zijn dan twee weken.
* Apparaatgrafieken van derden worden niet ondersteund.

## Volgende stappen

Als uw organisatie aan alle vereisten voldoet en de beperkingen begrijpt, kunt u Analytics [voor verschillende apparaten](setup.md)instellen.

