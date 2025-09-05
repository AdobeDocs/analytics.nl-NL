---
description: Laat u toe om toegang tot het melden van gegevens te controleren. De opties omvatten sterke wachtwoorden, wachtwoordafloop, IP login beperkingen, en e-maildomeinbeperkingen.
title: Beveiligingsbeheer
feature: Company Settings
exl-id: 6dcf0354-4b4a-4bd5-ba6c-ae42c7b9e4df
role: Admin
source-git-commit: e09234ca27fbf923e026aa1f2ed0ebfed636bf7c
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Beveiligingsbeheer

Met Beveiligingsbeheer kunt u de toegang tot rapportgegevens beheren. De opties omvatten sterke wachtwoorden, wachtwoordafloop, IP login beperkingen, en e-maildomeinbeperkingen.

## Instellingen

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Company settings]** > **[!UICONTROL Security]**

| Instelling | Beschrijving |
| --- | --- |
| Sterke wachtwoorden vereisen | Dwingt gebruikers om veiligere wachtwoorden tot stand te brengen die aan de volgende regels houden: <ul><li>Moet ten minste acht tekens lang zijn.</li><li>Tussen het eerste en laatste teken moet ten minste één symbool/cijfer staan.</li><li>Moet ten minste één alpha-teken hebben.</li><li>Kan niet vinden in een woordenboek of bevatten woorden uit een woordenboek (Engels).</li><li>Mag geen drie (3) opeenvolgende karakters van login gebruikersbenaming omvatten.</li><li>Moet anders zijn dan de vorige 10 wachtwoorden.</li></ul>**Nota**: Deze eigenschap wordt afgedwongen op nieuwe wachtwoorden die door:gaan. Het controleert geen bestaande wachtwoorden, of dwingt gebruikers om bestaande wachtwoorden te veranderen. Om deze reden, denk na toelatend wachtwoordafloop om gebruikers te dwingen om hun wachtwoorden te veranderen en aan de sterke wachtwoordregels te houden. |
| Wachtwoordvervaldatum | Hiermee worden gebruikers gedwongen hun wachtwoord voor gebruikersaccounts regelmatig te wijzigen. U kunt het interval specificeren waarmee u wachtwoorden wilt verlopen, en wachtwoorden dwingen om onmiddellijk te verlopen. |
| E-maildomeinbeperkingen afdwingen | Hiermee filtert u de e-mailadressen en domeinen waarnaar Analytics bladwijzers, downloadbare rapporten en waarschuwingen verzendt. De lijst met e-mailfilters ondersteunt maximaal 100 berichten en elk item kan een e-mailadres of een volledig e-maildomein zijn. Als een gepland rapport een niet-goedgekeurd e-maildoel heeft, stuurt Analytics een e-mailmelding van het probleem en een koppeling om het rapport ongedaan te maken. **[!UICONTROL Enforce Email Domain Restrictions]** wordt pas afgedwongen als er ten minste één item voorkomt in de lijst Filter voor geaccepteerde e-maildomeinen. **[!UICONTROL Accepted Email Address and Domains]**: Als u een IP-adresbereik wilt opgeven, plaatst u het bereik tussen haakjes (bijvoorbeeld `192.168.10.[20-240]` ). U kunt ook jokertekens gebruiken om een willekeurig getal tussen 0 en 255 op te geven (bijvoorbeeld `192.168.[10-14].*`) |
| Herstelmelding wachtwoord | Hiermee worden de opgegeven beheerders op de hoogte gesteld wanneer een gebruiker een wachtwoord voor een gebruikersaccount opnieuw probeert in te stellen. **[!UICONTROL Available Admins]**: geeft alle beheerders weer. U kunt meerdere beheerders selecteren door Ctrl+klikken en Shift+klikken. **[!UICONTROL Email Members]**: geeft de momenteel gedefinieerde e-mailgroep weer. |
