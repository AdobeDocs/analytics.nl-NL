---
description: Laat u toe om toegang tot het melden van gegevens te controleren. De opties omvatten sterke wachtwoorden, wachtwoordafloop, IP login beperkingen, en e-maildomeinbeperkingen.
title: Beveiligingsbeheer
topic: Admin tools
uuid: b3fbdba0-e2bf-4d67-92e3-ef05711141d4
translation-type: tm+mt
source-git-commit: ''

---


# Beveiligingsbeheer

Met Beveiligingsbeheer kunt u de toegang tot rapportgegevens beheren. De opties omvatten sterke wachtwoorden, wachtwoordafloop, IP login beperkingen, en e-maildomeinbeperkingen.

## Instellingen

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Company Settings]** > **[!UICONTROL Security]**

| Instelling | Beschrijving |
|--- |--- |
| Sterke wachtwoorden vereisen | Dwingt gebruikers om veiligere wachtwoorden tot stand te brengen die aan de volgende regels houden: <ul><li>Moet ten minste acht tekens lang zijn.</li><li>Tussen het eerste en laatste teken moet ten minste één symbool/cijfer staan.</li><li>Moet ten minste één alpha-teken hebben.</li><li>Kan niet vinden in een woordenboek of bevatten woorden uit een woordenboek (Engels).</li><li>Mag geen drie (3) opeenvolgende karakters van login gebruikersbenaming omvatten.</li><li>Moet anders zijn dan de vorige 10 wachtwoorden.</li></ul>**Opmerking**: Deze eigenschap wordt afgedwongen op nieuwe wachtwoorden die door:gaan. Het controleert geen bestaande wachtwoorden, of dwingt gebruikers om bestaande wachtwoorden te veranderen. Om deze reden, denk na toelatend wachtwoordafloop om gebruikers te dwingen om hun wachtwoorden te veranderen en aan de sterke wachtwoordregels te houden. |
| Wachtwoordvervaldatum | Hiermee worden gebruikers gedwongen hun wachtwoord voor gebruikersaccounts regelmatig te wijzigen. U kunt het interval specificeren waarmee u wachtwoorden wilt verlopen, en wachtwoorden dwingen om onmiddellijk te verlopen. |
| IP-aanmeldbeperkingen afdwingen | (Deze functionaliteit kan niet worden gebruikt in combinatie met de aanmeldingsgegevens voor Experience Cloud. Deze functionaliteit is niet meer beschikbaar vanaf oktober 2020. [Meer...](/help/admin/company/login-restrictions-eol.md))<br> beperkt rapporttoegang tot specifieke IP adressen of IP adreswaaiers. U kunt tot 100 ingangen in de IP lijst van de Filter van het Adres toevoegen, en elke ingang kan een specifiek adres of een waaier van adressen zijn. De Beperkingen van de Aanmelding van de afdwingen IP worden niet afgedwongen tot er minstens één ingang in de IP lijst van de Filter van het Adres is. Geaccepteerd IP-adres: Als u een IP-adresbereik wilt opgeven, plaatst u het bereik tussen haakjes (bijvoorbeeld `192.168.10.[20-240]`). U kunt vervangingen ook gebruiken om om het even welk aantal van 0 tot 255 (bijvoorbeeld, ` 192.168.[10-14]te specificeren.*8) Mislukte logins zijn geregistreerd en kunnen worden weergegeven vanuit het [Gebruikslogbestand en het Toegangslogbestand](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/logs.html#section_6FBAF92D9EA244809C45A78A2F0A7232). |
| E-maildomeinbeperkingen afdwingen | Hiermee filtert u de e-mailadressen en domeinen waarnaar Analytics bladwijzers, downloadbare rapporten en waarschuwingen verzendt. De lijst met e-mailfilters ondersteunt maximaal 100 berichten en elk item kan een e-mailadres of een volledig e-maildomein zijn. Als een gepland rapport een niet-goedgekeurd e-maildoel heeft, stuurt Analytics een e-mailmelding van het probleem en een koppeling om het rapport ongedaan te maken. **[!UICONTROL Enforce Email Domain Restrictions]** wordt pas afgedwongen als er ten minste één item voorkomt in de lijst voor het toegestane e-maildomein. **[!UICONTROL Accepted Email Address and Domains]**: Om een IP adreswaaier te specificeren, sluit de waaier in haakjes (bijvoorbeeld, 192.168.10.[20-240]). U kunt ook jokertekens gebruiken om een willekeurig getal tussen 0 en 255 op te geven (bijvoorbeeld 192.168.[10-14].*) |
| Herstelmelding wachtwoord | Hiermee worden de opgegeven beheerders op de hoogte gesteld wanneer een gebruiker een wachtwoord voor een gebruikersaccount opnieuw probeert in te stellen. **[!UICONTROL Available Admins]**: Hiermee geeft u alle beheerders weer. U kunt meerdere beheerders selecteren door Ctrl+klikken en Shift+klikken. **[!UICONTROL Email Members]**: Hiermee geeft u de momenteel gedefinieerde e-mailgroep weer. |
