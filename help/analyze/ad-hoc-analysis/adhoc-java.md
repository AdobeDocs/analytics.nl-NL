---
description: Instructies voor het uitvoeren van ad-hocanalyse met Java 11.
title: Ad hoc-analyse uitvoeren met Java 11
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Ad hoc-analyse uitvoeren met Java 11

Als u Ad hoc Analyse uitvoert met Java 11, moet u aanvullende stappen uitvoeren in vergelijking met Java 8.

## Vereisten

Werk samen met uw IT-team om ervoor te zorgen dat het volgende is ingesteld:

* Java 11 moet worden geïnstalleerd, met *JAVA_HOME* -omgevingsvariabele ingesteld
* JavaFX moet worden geïnstalleerd, waarbij de omgevingsvariabele *PATH_TO_FX_SDK* naar de directory van de JavaFX SDK verwijst. Bijvoorbeeld: *PATH_TO_FX_SDK=/homedir/javafx-sdk-11.0.2* op een Mac, of *PATH_TO_FX_SDK=C:\Users\username\javafx-sdk-11.0.2* op een pc.

## Ad hoc-analyse installeren voor Java 11

1. Ga naar **[!UICONTROL Analytics > Tools > Ad Hoc Analysis]**.
1. Klik op **[!UICONTROL Ad Hoc Analysis (Java 11)]**. Hiermee wordt een ZIP-bestand gedownload.
1. Pak het gedownloade bestand uit.
1. **Selecteer het .bat-bestand (PC) of het .sh-bestand**(Mac). Selecteer het juiste datacenterbestand door het nummer na &quot;sc&quot; in de URL voor Adobe Analytics te bekijken. (3 = LON, 4 = SIN, 5 = PNW) als u PC gebruikt, verifieer of u een werkend systeem met 32 bits of met 64 bits van Vensters door &quot;over uw PC&quot;te gaan in werking stelt. Selecteer vervolgens het juiste .bat-bestand.
1. **Voer het geselecteerde bestand** uit. Voor pc: Dubbelklik op het .bat-bestand. Voor Mac: Klik met de rechtermuisknop op het .sh-bestand en selecteer **[!UICONTROL Open With > Other... > Utilities > (Enable all applications) > select Terminal > Open]**.
1. Meld u aan bij ad-hocanalyse.

> [!NOTE] De verificatiemethoden van de federatieve en Enterprise-id zijn niet compatibel met de Java 11-versie van Ad Hoc Analysis.

## Niet-ondersteunde functies in ad-hocanalyse (Java 11)

Er zijn een paar bekende beperkingen in de Java 11-versie die compatibel zijn met Ad hoc-analyse:

* Fond- en Enterprise-id-verificatiemethoden worden niet ondersteund.
* Linux-besturingssystemen worden niet ondersteund.
* Gebruik bij gebruik van een Mac niet het Mac-toepassingsmenu (inclusief *cmd + Q*). Dit kan ertoe leiden dat de ad-hocanalyse zonder waarschuwing wordt afgesloten. Gebruik in plaats daarvan het menu in Ad hoc-analyse.
* De visualisatie van de Analyse van de Plaats wordt niet gesteund wanneer het runnen van Ad hoc Analyse op MACOS.

## Veelgestelde vragen

**V: Ik krijg een fout &quot;Kan \bin\javaw niet vinden&quot; (voorbeeld hieronder) - wat moet ik doen?**

![](/help/analyze/ad-hoc-analysis/assets/error-java.png)

A: Als u deze fout krijgt, werkt u samen met uw IT-team om de omgevingsvariabele *JAVA_HOME* in te stellen die vereist is om ad-hocanalyse uit te voeren in Java 11.
