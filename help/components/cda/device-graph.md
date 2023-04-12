---
title: Apparaatgrafiek
description: Begrijp de eerste vereisten en de beperkingen van het stitching van gegevens gebruikend de apparatengrafiek.
exl-id: b8408a7d-6aff-4fff-b535-f10d422bcf0d
source-git-commit: 34ba0e09cd909951a777b0ad3da080958633f97e
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 2%

---

# Apparaatgrafiek

Analytics voor verschillende apparaten kan de persoonlijke grafiek gebruiken om gegevens aan elkaar te koppelen. De privégrafiek is een opslagplaats van hashed apparaat-id&#39;s die specifiek is voor uw organisatie. CDA communiceert regelmatig met de apparatengrafiek om apparaten samen te verbinden.

## Specifieke voorwaarden voor de apparaatgrafiek

Als u Apparaatanalyse wilt implementeren met de grafiekmethode van het apparaat, is het volgende vereist. Werk met teams binnen uw organisatie en uw Adobe Account Team om ervoor te zorgen dat u aan alle volgende voorwaarden voldoet.

>[!WARNING]
>
>Als niet aan alle voorwaarden wordt voldaan, kan het zijn dat u Cross-Device Analytics of slechte resultaten niet kunt inschakelen bij het koppelen van gegevens.

* Alle voorwaarden die op de [overzichtspagina](overview.md).
* Uw organisatie moet de [Adobe Experience Platform Identity Service Private Graph](https://business.adobe.com/products/experience-platform/identity-service.html). Zie ook de [Startpagina](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=nl) in de gebruikershandleiding voor Identiteitsservice.
* Voor uw implementatie moet de nieuwste versie van de Experience Cloud-id-service (ECID) worden gebruikt. Zie de [Startpagina](https://experienceleague.adobe.com/docs/id-service/using/home.html) in de gebruikershandleiding voor de id-service. De meeste implementaties gebruiken [Tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html) in Adobe Experience Platform is ID Service waarschijnlijk al geïmplementeerd.
* Uw implementatie moet de `setCustomerIDs` functie (of SDK-equivalent) wanneer een individu kan worden geïdentificeerd, bijvoorbeeld wanneer een gebruiker zich aanmeldt of een e-mail opent. Deze eis geldt voor alle platforms, inclusief mobiele apps indien gebruikt. Zie [`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html) in de gebruikershandleiding voor de id-service.

## Specifieke beperkingen voor de apparaatgrafiek

* Verouderde analyse-id&#39;s worden niet ondersteund. Alleen bezoekers met Experience Cloud-id&#39;s zijn aangesloten.
* Als uw organisatie een Privé Grafiek gebruikt, nemen de nieuwe apparaten tot 24 uren om worden vastgemaakt.
* Apparaatgrafieken van derden worden niet ondersteund.

## Volgende stappen

Zodra uw organisatie aan alle vereisten voldoet en de beperkingen begrijpt, kunt u beginnen [Apparaatanalyse instellen](setup.md).
