---
title: Ondersteunde HTTPS-versleutelingsalgoritmen
description: Beveiligingsinstellingen en certificaattypen voor TLS-scripts.
feature: Regional Data Collection
exl-id: f1cbb0cb-fd65-4f22-8594-0d97b6906698
source-git-commit: 299de03c05f6a8af4f6c5d98c76bae54eec4c088
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Ondersteunde HTTPS-versleutelingsalgoritmen

## Beveiligingsniveaus verbeteren

Adobe biedt twee cipher veiligheidsniveaus aan om aan verschillende klantenbehoeften voor veiligheid op de inzameling van gegevens van eerste partij te voldoen. Deze niveaus bepalen welke encryptiealgoritmen voor verbindingen HTTPS met onze servers worden gesteund. Adobe controleert en werkt regelmatig de reeks gesteunde algoritmen bij die op huidige veiligheidspraktijken worden gebaseerd. Neem contact op met de klantenservice als u de beveiligingsinstellingen van de ontvanger wilt wijzigen.

&#39;Standaard&#39; vereist TLS 1.2 of hoger en minimaal 128-bits codering. Het is ontworpen om de breedste apparaatcompatibiliteit te bieden en tegelijk een veilige codering te behouden.

Bij &#39;hoog&#39; coderingsbeveiligingsniveau is TLS 1.2 of hoger vereist en wordt ondersteuning voor zwakkere ciphers verwijderd. Het is ontworpen voor klanten die de sterkste encryptie willen en zich niet zorgen maken over steun voor oudere apparaten.

Van de volgende clients is bekend dat ze geen verbinding kunnen maken met de beveiliging van het script ingesteld op &quot;Hoog&quot;.

* Windows 8.1 en eerder (laatst bijgewerkt in 2018)
* Windows Phone 8.1 en eerder (laatst bijgewerkt in 2016)
* OS X 10.10 en eerder (laatst bijgewerkt in 2017)
* iOS 8.4 en eerder (laatstelijk bijgewerkt in 2015)

## Ondersteunde HTTPS-certificaattypen

Adobe steunt zowel RSA als ECC certificaattypes om aan verschillende klantenbehoeften te voldoen. RSA-certificaten worden meer ondersteund voor clients, maar ECC-certificaten gebruiken minder verwerking aan zowel de server- als de clientzijde. Voor Adobe Beheerde certificaten, zowel worden RSA als ECC verstrekt. Voor klant beheerde certificaten, zowel worden RSA als ECC geadviseerd. Moderne clients ondersteunen zowel RSA als ECC. De volgende cliënten zijn gekend om certificaten RSA slechts te steunen:

* Windows Vista en eerder (laatst bijgewerkt in 2012)
* Windows Phone 8.0 en eerder (laatst bijgewerkt in 2014)
* OS X 10.8 en eerder (laatst bijgewerkt in 2013)
* iOS 5.1 en eerder (laatstelijk bijgewerkt in 2012)
* Android 4.3 en eerder (laatstelijk bijgewerkt in 2013)
