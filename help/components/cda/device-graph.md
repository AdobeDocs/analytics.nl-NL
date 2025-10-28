---
title: Apparaatgrafiek
description: Begrijp de eerste vereisten en de beperkingen van het stitching van gegevens gebruikend de apparatengrafiek.
exl-id: b8408a7d-6aff-4fff-b535-f10d422bcf0d
feature: CDA
role: Admin
source-git-commit: 6c74f4d4c14765742a2aafdfff2a083c6b0a7183
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---


# Apparaatgrafiek

{{available-existing-customers}}

>[!WARNING]
>
>De Grafiek van het apparaat binnen Analytics van het Apparaat zal niet meer op **31 December, 2025** beschikbaar zijn. Gelieve te schakelen om het even welke huidige apparatengrafiek toegelaten virtuele rapportreeks aan de [&#x200B; op gebied-gebaseerde methode &#x200B;](/help/components/cda/field-based-stitching.md).
>

Analytics voor verschillende apparaten kan de persoonlijke grafiek gebruiken om gegevens aan elkaar te koppelen. De privégrafiek is een opslagplaats van hashed apparaat-id&#39;s die specifiek is voor uw organisatie. CDA communiceert regelmatig met de apparatengrafiek om apparaten samen te verbinden.

## Specifieke voorwaarden voor de apparaatgrafiek

Als u Apparaatanalyse wilt implementeren met de grafiekmethode van het apparaat, is het volgende vereist. Werk met teams binnen uw organisatie en uw Adobe-accountteam om ervoor te zorgen dat u aan alle volgende voorwaarden voldoet.

>[!WARNING]
>
>Als niet aan alle voorwaarden wordt voldaan, kan het zijn dat u Cross-Device Analytics of slechte resultaten niet kunt inschakelen bij het koppelen van gegevens.
>

* Alle eerste vereisten die op de [&#x200B; overzichtspagina &#x200B;](overview.md) worden vermeld.
* Uw organisatie moet de [&#x200B; Persoonlijke Grafiek van de Dienst van de Identiteit van Adobe Experience Platform gebruiken &#x200B;](https://business.adobe.com/products/experience-platform/identity-service.html). Zie ook de [&#x200B; Pagina van het Huis &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=nl) in de de gebruikersgids van de Dienst van de Identiteit.
* Voor uw implementatie moet de nieuwste versie van de Experience Cloud ID Service (ECID) worden gebruikt. Zie de [&#x200B; Pagina van het Huis &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/home.html) in de de gebruikersgids van de Dienst van identiteitskaart De meeste implementaties die [&#x200B; Markeringen &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html) gebruiken in Adobe Experience Platform hebben waarschijnlijk reeds de Dienst van identiteitskaart opgesteld.
* Uw implementatie moet de functie `setCustomerIDs` (of het equivalent van SDK) aanroepen wanneer een individu kan worden geïdentificeerd, zoals wanneer een gebruiker zich aanmeldt of een e-mail opent. Deze eis geldt voor alle platforms, inclusief mobiele apps indien gebruikt. Zie [`setCustomerIDs` &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html) in de de gebruikersgids van de Dienst van identiteitskaart

## Specifieke beperkingen voor de apparaatgrafiek

* Verouderde analyse-id&#39;s worden niet ondersteund. Alleen bezoekers met Experience Cloud-id&#39;s zijn gebonden.
* Als uw organisatie een Privé Grafiek gebruikt, nemen de nieuwe apparaten tot 24 uren om worden vastgemaakt.
* Apparaatgrafieken van derden worden niet ondersteund.

## Volgende stappen

Zodra uw organisatie aan alle vereisten voldoet en de beperkingen begrijpt, kunt u [&#x200B; Opstelling Analytics van het Apparaat &#x200B;](setup.md) beginnen.
