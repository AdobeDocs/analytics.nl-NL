---
description: Logbestanden waarmee u kunt zien wanneer gebruikers zich aanmelden, hoe ze deze gebruiken, gebruiken, gebruiken, gebruiken, rapporten met suites en Admin wijzigen.
title: Logboeken
feature: Admin Tools
exl-id: 43f79e2a-2cb9-47eb-982a-54714c9cbafc
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 2%

---

# Logboeken

Logbestanden waarmee u kunt zien wanneer gebruikers zich aanmelden, hoe ze deze gebruiken, gebruiken, gebruiken, gebruiken, rapporten met suites en Admin wijzigen.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Logs]**

## Beheerderslogboek {#section_8ADE8A7204A8401C968ABC20AECA381D}

Het beheerderlogboek rapporteert alle veranderingen die door beheerders in admin hulpmiddelen worden aangebracht. Het logboek verstrekt een gateway aan user-defined rapporten van om het even welke drie logboeken. U kunt zoeken naar gebeurtenissen die binnen een bepaald datumbereik overeenkomen met de geselecteerde criteria.

## Gebruik en toegangslogboek {#section_6FBAF92D9EA244809C45A78A2F0A7232}

Met [!UICONTROL Usage and Access Log] kunt u het rapportgebruik op gebruikersaccountniveau evalueren. Zo worden bijvoorbeeld acties voor openen, maken, bijwerken, delen en verwijderen in Analysis Workspace bijgehouden. Hierdoor kunt u beter zien wie de werkruimte gebruikt en hoe vaak.

| Element | Beschrijving |
|---|---|
| Datumbereik | Geef een filter voor het datumbereik op. U kunt een datum handmatig invoeren in de notatie JJJJ-MM-DD of op het kalenderpictogram klikken om een datum te selecteren. |
| Aanmelden | Filter het logbestand op gebruikersnaam. |
| IP | Filter het logboek door een IP adres. |
| Rapportsuite | Filter het logboek door een specifieke identiteitskaart van de rapportreeks. |
| Type gebeurtenis | Filter het logbestand op een gebeurtenistype. Selecteer een gebeurtenistype in de vervolgkeuzelijst. Zie de volledige lijst met gebeurtenistypen hieronder. |
| Gebeurtenis | Filter het logbestand op een woord of woordgroep in de gebeurtenisbeschrijving. |
| Rapport downloaden | Exporteert de inhoud van het [!UICONTROL Usage & Access Log] naar een bestand met tabs als scheidingsteken. |

### Gebeurtenistypen

| Het type Event | Beschrijving |
| --- | --- |
| Geen categorie | Kan elk gebeurtenistype zijn. |
| Aanmelden mislukt | Aanmeldingsproces gebruiker is mislukt. |
| Aanmelden gelukt | Gebruiker is aangemeld. |
| Handeling Admin | Er is een beheeractie opgetreden, zoals het bewerken van een rapportsuite, het wijzigen van de bedrijfsinstellingen, het maken van een gebruiker, enzovoort. |
| Wijziging van beveiligingsinstelling | Er is een beveiligingsinstelling gewijzigd. |
| Bekeken rapport | Er is een rapport met rapporten en analyses weergegeven. |
| Gedownload rapport | Er is een rapport met rapporten en analyses gedownload. |
| Waarschuwing verzonden | Er is een waarschuwing verzonden. |
| Handeling van gebruiker | Gebruikersgegevens zijn bewerkt. |
| Gereedschap weergegeven | Er is een gereedschap weergegeven. |
| Omniture-actie | Adobe heeft een handeling uitgevoerd. |
| Herstel van wachtwoord | Er is een wachtwoord hersteld. |
| BookMarks | Er is een bladwijzer beheerd. |
| Dashboards | Er is een dashboard beheerd. |
| Waarschuwingen | Er is een waarschuwing beheerd. |
| Kalendergebeurtenissen | Er is een kalendergebeurtenis beheerd. |
| Targets | Er is een doel beheerd. |
| Rapportinstellingen | Er is een rapportinstelling beheerd. |
| Geplande rapporten | Een gepland rapport is beheerd. |
| Uitsluiten door IP | IP-instelling gewijzigd. |
| Pagina&#39;s een naam geven | Vervangen. |
| Classificaties | Er is een classificatie beheerd. |
| Databronnen | Er is een gegevensbron beheerd. |
| Werkruimteproject | Een Workspace-project is weergegeven of bewerkt. |
| Segment | Er is een segment gemaakt/bewerkt. |
| Berekend metrisch | Er is een berekende metrische waarde gemaakt/bewerkt. |
| Datumbereik | Er is een datumbereik gemaakt/bewerkt. |
| Virtuele rapportsuite | Er is een virtuele rapportsuite gemaakt/bewerkt. |
| Contributieanalyse | Er is een bijdrageanalysetaak uitgevoerd. |
| API-methode | Er is een API-aanroep gemaakt. |


## Logboek voor wijzigen van suite rapporteren {#section_3864966639414BBEA871F4D0352F56B6}

In het logbestand Wijziging van rapportsuite worden de wijzigingen weergegeven die u buiten Admin hebt aangebracht in uw rapportsuites.

De hulpmiddelen die een rapportreeks van buiten [!UICONTROL Admin Tools] kunnen wijzigen omvatten:

* Bijwerkingen die zijn ge??pload in een webbrowser (classificaties die zijn ge??pload via FTP worden niet opgenomen in het wijzigingslogboek)
* Wijzigingen die in eerdere versies zijn aangebracht.
* Wijzigingen aangebracht door een accountvertegenwoordiger of door de klantenservice met interne tools

| Element | Beschrijving |
|---|---|
| Datumbereik | Geef een filter voor het datumbereik op. U kunt een datum handmatig invoeren in de notatie JJJJ-MM-DD of op het kalenderpictogram klikken om een datum te selecteren. |
| Bedrijf | Filter het logboek door bedrijfsnaam. |
| Aanmelden | Filter het logbestand op gebruikersnaam. |
| IP | Filter het logboek door een IP adres. |
| Gebeurtenis | Filter het logbestand op een woord of woordgroep in de gebeurtenisbeschrijving. |
| Rapport downloaden | Exporteert de inhoud van het [!UICONTROL Usage & Access Log] naar een bestand met tabs als scheidingsteken. |
