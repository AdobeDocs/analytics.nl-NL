---
description: Opzoektabel om het type hit te bepalen op basis van de waarde page_event.
keywords: Gegevensfeed;pagina;gebeurtenis;pagina_gebeurtenis;post_page_event
title: Pagina-gebeurtenis opzoeken
feature: Reports & Analytics Basics
uuid: 73af597c-5560-466e-94b2-ddd1d64797c8
exl-id: ef0467df-b94b-4cec-b312-96d8f42c23b0
source-git-commit: 027435640c9092808f3adb1244228267c03b593c
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Pagina-gebeurtenis opzoeken

Opzoektabel om het type hit te bepalen op basis van de waarde page_event.

| Type hit | `page_event` value | `post_page_event` value |
| --- | --- | --- |
| Paginaweergaven | 0: Alle oproepen van de paginaweergave en `trackState` oproepen van mobiele SDK&#39;s | Dezelfde waarde als `page_event` |
| Link tracking | 10: Aangepaste koppelingen en `trackAction` oproepen in mobiele SDK&#39;s<br>11: Koppelingen downloaden<br>12: Koppelingen afsluiten | 100: Aangepaste koppelingen en `trackAction` oproepen in mobiele SDK&#39;s<br>101: Koppelingen downloaden<br>102: Koppelingen afsluiten |
| Milestone-video | 31: Start media<br>32: Media-updates (geen andere variabele-verwerking)<br>33: Media-updates (met andere variabelen) | 76: Start media<br>77: Media-updates (geen andere variabele-verwerking)<br>78: Media-updates (met andere variabelen) |
| Hartslagvideo | 50: Start van mediastream (niet-Primetime)<br>51: Mediastroom sluiten (niet-Primetime)<br>52: Scrubbing van mediastream (niet-Primetime)<br>53: Mediastream blijft in leven (niet-Primetime)<br>54: Mediastream en start (niet-Primetime)<br>55: Mediastroom en close (niet-Primetime)<br>56: Mediastroom en scrubben (niet-Primetime)<br>60: Start van primaire mediastream<br>61: Primetime-mediastream sluiten<br>62: Primetime-mediastream scrubben<br>63: Primetime-mediastream in leven houden<br>64: Primetime-mediastream en begin<br>65: Primetime-mediastream en sluiten<br>66: Primetime-mediastream en scrubben | Dezelfde waarde als `page_event` |
| Enquête | 40: Om het even welke vraag die van Onderzoek wordt geproduceerd | 80: Om het even welke vraag die van Onderzoek wordt geproduceerd |
| Analyses voor doel | 70: Actief bevat gegevens over doelactiviteit | Dezelfde waarde als `page_event` |
