---
title: Apparaatgrafiek
description: Begrijp de eerste vereisten en de beperkingen van het stitching van gegevens gebruikend de apparatengrafiek.
exl-id: b8408a7d-6aff-4fff-b535-f10d422bcf0d
feature: CDA
role: Admin
source-git-commit: be5a73347d417c8dc6667d4059e7d46ef5f0f5cd
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---

# Apparaatgrafiek

Analytics voor verschillende apparaten kan de persoonlijke grafiek gebruiken om gegevens aan elkaar te koppelen. De privégrafiek is een opslagplaats van hashed apparaat-id&#39;s die specifiek is voor uw organisatie. CDA communiceert regelmatig met de apparatengrafiek om apparaten samen te verbinden.

## Specifieke voorwaarden voor de apparaatgrafiek

Als u Apparaatanalyse wilt implementeren met de grafiekmethode van het apparaat, is het volgende vereist. Werk met teams binnen uw organisatie en uw Team van de Rekening van de Adobe om ervoor te zorgen dat u aan elk van het volgende voldoet.

>[!WARNING]
>
>Als niet aan alle voorwaarden wordt voldaan, kan het zijn dat u Cross-Device Analytics of slechte resultaten niet kunt inschakelen bij het koppelen van gegevens.

* Alle voorwaarden die worden vermeld op de [overzichtspagina](overview.md).
* Uw organisatie moet de [Adobe Experience Platform Identity Service Private Graph](https://business.adobe.com/products/experience-platform/identity-service.html). Zie ook de [Startpagina](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=nl) in de gebruikershandleiding voor Identiteitsservice.
* Uw implementatie moet de nieuwste versie van de Experience Cloud-id-service (ECID) gebruiken. Zie de [Startpagina](https://experienceleague.adobe.com/docs/id-service/using/home.html) in de gebruikershandleiding voor de id-service. De meeste implementaties gebruiken [Tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html) in Adobe Experience Platform is ID Service waarschijnlijk al geïmplementeerd.
* Uw implementatie moet de `setCustomerIDs` functie (of SDK-equivalent) wanneer een individu kan worden geïdentificeerd, bijvoorbeeld wanneer een gebruiker zich aanmeldt of een e-mail opent. Deze eis geldt voor alle platforms, inclusief mobiele apps indien gebruikt. Zie [`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html) in de gebruikershandleiding voor de id-service.

## Specifieke beperkingen voor de apparaatgrafiek

* Verouderde analyse-id&#39;s worden niet ondersteund. Alleen bezoekers met Experience Cloud-id&#39;s worden vastgezet.
* Als uw organisatie een Privé Grafiek gebruikt, nemen de nieuwe apparaten tot 24 uren om worden vastgemaakt.
* Apparaatgrafieken van derden worden niet ondersteund.

## Volgende stappen

Zodra uw organisatie aan alle vereisten voldoet en de beperkingen begrijpt, kunt u beginnen [Apparaatanalyse instellen](setup.md).
