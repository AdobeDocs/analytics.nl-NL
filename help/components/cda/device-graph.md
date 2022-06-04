---
title: Apparaatgrafiek
description: Begrijp de eerste vereisten en de beperkingen van het stitching van gegevens gebruikend de apparatengrafiek.
exl-id: b8408a7d-6aff-4fff-b535-f10d422bcf0d
source-git-commit: 3f4d8df911c076a5ea41e7295038c0625a4d7c85
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Apparaatgrafiek

Cross-Device Analytics biedt twee verschillende methoden om gegevens aan elkaar te koppelen. Bij deze methode wordt de Adobe Experience Platform Identity Service Co-op grafiek of de Private Graph gebruikt om gegevens aan elkaar te koppelen. CDA communiceert regelmatig met de apparatengrafiek om apparaten samen te verbinden.

## Verschillen tussen co-op grafiek en privé grafiek

Adobe biedt twee typen apparaatgrafieken als onderdeel van de ID-service:

* **Grafiek met meerdere uiteinden**: Een opslagplaats van hashed apparaat ID&#39;s die om het even welke klant kan bijdragen tot en van verwijzingen voorzien. Aangezien dit type apparaatgrafiek een gezamenlijke grafiek is, komt deze meestal overeen met meer apparaten dan een persoonlijke grafiek.
* **Privégrafiek**: Een opslagplaats van hashed apparaat ID&#39;s die slechts uw organisatie van verwijzingen voorziet.

## Specifieke voorwaarden voor de apparaatgrafiek

Als u Apparaatanalyse wilt implementeren met de grafiekmethode van het apparaat, is het volgende vereist. Werk met teams binnen uw organisatie en uw Adobe-accountmanager om ervoor te zorgen dat u aan alle volgende voorwaarden voldoet.

>[!WARNING]
>
>Als niet aan alle voorwaarden wordt voldaan, kan het zijn dat u Cross-Device Analytics of slechte resultaten niet kunt inschakelen bij het koppelen van gegevens.

* Alle voorwaarden die op de [overzichtspagina](overview.md).
* Uw organisatie moet de Adobe Experience Platform Identity Service Co-op Graph of Private Graph gebruiken. Zie de [Startpagina](https://experienceleague.adobe.com/docs/device-co-op/using/home.html) in de gebruikershandleiding voor cogebruikers van apparaten.
* Uw implementatie moet de nieuwste versie van de Experience Cloud ID-service gebruiken. Zie de [Startpagina](https://experienceleague.adobe.com/docs/id-service/using/home.html) in de gebruikershandleiding van de Experience Cloud Identity Service. Bij de meeste implementaties met tags in Adobe Experience Platform is ECID waarschijnlijk al geïmplementeerd.
* Uw implementatie moet de `setCustomerIDs` functie (of SDK-equivalent) wanneer een individu kan worden geïdentificeerd, bijvoorbeeld wanneer een gebruiker zich aanmeldt of een e-mail opent. Deze eis geldt voor alle platforms, inclusief mobiele apps indien gebruikt. Zie [`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html) in de gebruikershandleiding van de Experience Cloud Identity Service.

## Specifieke beperkingen voor de apparaatgrafiek

* Verouderde analyse-id&#39;s worden niet ondersteund. Alleen bezoekers met Experience Cloud-id&#39;s zijn aangesloten.
* Als uw organisatie een Privé Grafiek gebruikt, nemen de nieuwe apparaten tot 24 uren om worden vastgemaakt.
* Als uw organisatie de Co-op grafiek gebruikt, kunnen nieuwe apparaten die uw plaats bezoeken tot twee weken duren om te stikken. De mate van stitching in CDA voor de meest recente twee weken is doorgaans lager dan voor datumbereiken die ouder zijn dan twee weken.
* Apparaatgrafieken van derden worden niet ondersteund.

## Volgende stappen

Zodra uw organisatie aan alle vereisten voldoet en de beperkingen begrijpt, kunt u beginnen [Apparaatanalyse instellen](setup.md).
