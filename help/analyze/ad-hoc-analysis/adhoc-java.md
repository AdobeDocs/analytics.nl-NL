---
description: Instructies voor het uitvoeren van Ad Hoc Analysis met Java 11.
title: Ad Hoc Analysis uitvoeren met Java 11
translation-type: tm+mt
source-git-commit: d4cb2acb4ecaecce3644a2f3cf29913440e5cd6a
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 4%

---


# Ad Hoc Analysis uitvoeren met Java 11

>[!IMPORTANT]
>
>Adobe beweegt Ad Hoc Analysis op 1 maart 2021 naar de status &quot;end-of-life&quot;. [Meer informatie...](https://adobe.ly/discoverworkspace).

Als u Ad Hoc Analysis met Java 11 uitvoert, moet u aanvullende stappen volgen in vergelijking met Java 8.

## Vereisten

Werk samen met uw IT-team om ervoor te zorgen dat het volgende is ingesteld:

* Java 11 moet worden geïnstalleerd, met *JAVA_HOME* -omgevingsvariabele ingesteld
* JavaFX moet worden geïnstalleerd, waarbij de omgevingsvariabele *PATH_TO_FX_SDK* naar de directory van de JavaFX SDK verwijst. Bijvoorbeeld: *PATH_TO_FX_SDK=/homedir/javafx-sdk-11.0.2* op een Mac, of *PATH_TO_FX_SDK=C:\Users\username\javafx-sdk-11.0.2* op een pc.

## Ad Hoc Analysis installeren voor Java 11

1. Ga naar **[!UICONTROL Analytics > Tools > Ad Hoc Analysis]**.
1. Klik op **[!UICONTROL Ad Hoc Analysis (Java 11)]**. Hiermee wordt een ZIP-bestand gedownload.
1. Pak het gedownloade bestand uit.
1. **Selecteer het .bat-bestand (PC) of het .sh-bestand**(Mac). Selecteer het juiste datacenterbestand door het nummer na &quot;sc&quot; in de Adobe Analytics-URL te bekijken. (3 = LON, 4 = SIN, 5 = PNW) als u PC gebruikt, verifieer of u een werkend systeem met 32 bits of met 64 bits van Vensters door &quot;over uw PC&quot;te gaan in werking stelt. Selecteer vervolgens het juiste .bat-bestand.
1. **Voer het geselecteerde bestand** uit. Voor pc: Dubbelklik op het .bat-bestand. Voor Mac: Klik met de rechtermuisknop op het .sh-bestand en selecteer **[!UICONTROL Open With > Other... > Utilities > (Enable all applications) > select Terminal > Open]**.
1. Meld u aan bij Ad Hoc Analysis.

>[!NOTE]
>
>Federatieve en Enterprise ID-verificatiemethoden zijn niet compatibel met de Java 11-versie van Ad Hoc Analysis.

## Niet-ondersteunde functies in Ad Hoc Analysis (Java 11)

De Java 11-versie kent een aantal beperkingen die compatibel zijn met Ad Hoc Analysis:

* Federatieve en Enterprise ID-verificatiemethoden worden niet ondersteund.
* Linux-besturingssystemen worden niet ondersteund.
* Gebruik bij gebruik van een Mac niet het Mac-toepassingsmenu (inclusief *cmd + Q*). Dit kan ertoe leiden dat Ad Hoc Analysis zonder waarschuwing wordt gesloten. Gebruik in plaats daarvan het menu in Ad Hoc Analysis.
* De visualisatie van de Analyse van de Plaats wordt niet gesteund wanneer het runnen van Ad Hoc Analysis op MACOS.

## Veelgestelde vragen

**V: Ik krijg een fout &quot;Kan \bin\javaw niet vinden&quot; (voorbeeld hieronder) - wat moet ik doen?**

![](/help/analyze/ad-hoc-analysis/assets/error-java.png)

A: Als deze fout optreedt, werkt u samen met uw IT-team de omgevingsvariabele *JAVA_HOME* in die nodig is om Ad Hoc Analysis in Java 11 uit te voeren.
