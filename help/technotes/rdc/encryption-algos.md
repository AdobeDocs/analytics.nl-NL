---
title: Ondersteunde HTTPS-versleutelingsalgoritmen
description: Op 23 juni 2022 verwijderen we ondersteuning voor TLS 1.2-ciphers die SHA1 of CBC gebruiken voor klanten met een coderingsbeveiligingsniveau dat is ingesteld op "Hoog".
feature: Regional Data Collection
exl-id: f1cbb0cb-fd65-4f22-8594-0d97b6906698
source-git-commit: 84a8dc9c6052d34e9dea370e444c83e84bf17852
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Ondersteunde HTTPS-versleutelingsalgoritmen

Adobe biedt twee cipher veiligheidsniveaus aan om aan verschillende klantenbehoeften voor veiligheid op de inzameling van gegevens van eerste partij te voldoen. Deze niveaus bepalen welke encryptiealgoritmen voor verbindingen HTTPS met onze servers worden gesteund. Klanten hebben de standaardinstelling &quot;Standaard&quot;, die alleen moderne versleutelingsalgoritmen ondersteunt. &quot;Hoog&quot;steunt een kleinere lijst van encryptiealgoritmen voor klanten die zich meer over deze verbindingen zorgen maken. Voor beide veiligheidsniveaus, werkt Adobe regelmatig de reeks gesteunde algoritmen bij die op huidige veiligheidspraktijken worden gebaseerd. Neem contact op met de klantenservice als u de beveiligingsinstellingen van de ontvanger wilt wijzigen.

Op 23 juni 2022 verwijderen we ondersteuning voor TLS 1.2-ciphers die SHA1 of CBC gebruiken voor klanten met een coderingsbeveiligingsniveau dat is ingesteld op &quot;Hoog&quot;.  Deze wijziging heeft gevolgen voor de veilige gegevensverzameling voor eindgebruikers op oudere besturingssystemen.

De volgende TLS 1.2-ciphers worden niet meer ondersteund:

* TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
* TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
* TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
* TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
* TLS_RSA_WITH_AES_128_CBC_SHA
* TLS_RSA_WITH_AES_256_CBC_SHA
* TLS_RSA_WITH_AES_128_GCM_SHA256
* TLS_RSA_WITH_AES_256_GCM_SHA384

Van de volgende clients is bekend dat ze door deze wijziging worden beïnvloed omdat ze geen ondersteuning bieden voor de huidige coderingsstandaarden:

* Windows 8.1 en eerder (laatst bijgewerkt in 2018)
* Windows Phone 8.1 en eerder (laatst bijgewerkt in 2016)
* OS X 10.10 en eerder (laatst bijgewerkt in 2017)
* iOS 8.4 en eerder (laatstelijk bijgewerkt in 2015)

Deze wijziging heeft geen invloed op Android-apparaten.

Klanten met het beveiligingsniveau van de afteller ingesteld op &quot;Standaard&quot; worden niet beïnvloed door deze wijziging.
