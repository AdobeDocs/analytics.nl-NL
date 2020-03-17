---
title: SSL-certificaatlicentie
description: Certificaatprocedures voor door de klant beheerde certificaten
translation-type: tm+mt
source-git-commit: 290838566b86f71902abd303b5c43dd2661d3ce1

---


# SSL/TLS-certificaatlicentie

Adobe raadt u aan uw certificaat zonder extra kosten te beheren via het [Adobe Managed Certificate Program](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html).  Het door Adobe beheerde certificaatprogramma is volledig geautomatiseerd en zorgt ervoor dat certificaten tijdig worden vernieuwd zodat er geen gevolgen zijn vanwege verlopen certificaten.

Als u ervoor kiest om het [Adobe Managed Certificate Program](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html) niet te gebruiken, bent u verantwoordelijk voor het opgeven van een SSL/TLS-certificaat voor cookies van de eerste fabrikant.

Als u uw eigen certificaat opgeeft, is het uw verantwoordelijkheid om dit te kopen en te onderhouden.  Uw SSL/TLS-certificaat moet een onbeperkte serverlicentie bevatten.

Voor beveiliging van certificaten vraagt u bij Adobe een CSR [] -bestand voor certificaatondertekening aan en vraagt u bij de gewenste certificeringsinstantie om ondertekening van het certificaat.  Geef Adobe het ondertekende certificaat voor implementatie.  Door dit proces te volgen, blijft de veiligheid van de sleutel van het certificaat behouden.  De klantenservice van Adobe helpt u bij dit proces.

Als onderdeel van certificaatonderhoud, minstens één maand vóór het verlopen van uw certificaat, schik u bij de gewenste certificeringsinstantie in om een vernieuwd certificaat te verkrijgen en geef dit door aan Adobe.  Voor dit certificaat moet dezelfde CSR worden gebruikt als eerder.  Neem contact op met Adobe als u een kopie van de CSR nodig hebt of als u een nieuwe CSR wilt genereren met een nieuwe sleutel.

De Zorg van de klant kan op customercare@adobe.com of 1-800-497-0335 worden bereikt.

Veel gebruikte certificeringsinstanties zijn DigiCert, Comodo en GeoTrust.
