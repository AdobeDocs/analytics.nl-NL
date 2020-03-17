---
description: Opzoektabel om het type hit te bepalen op basis van de waarde page_event.
keywords: Data Feed;page;event;page_event;post_page_event
title: Pagina-gebeurtenis opzoeken
topic: Reports and analytics
uuid: 73af597c-5560-466e-94b2-ddd1d64797c8
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Pagina-gebeurtenis opzoeken

Opzoektabel om het type hit te bepalen op basis van de waarde page_event.

| Type hit | `page_event` value | `post_page_event` value |
| --- | --- | --- |
| Paginaweergaven | 0: Alle oproepen van de paginaweergave en `trackState` oproepen van mobiele SDK&#39;s | Dezelfde waarde als `post_page_event` |
| Koppeling bijhouden | 10: Aangepaste koppelingen en `trackAction` oproepen in mobiele SDK&#39;s<br>11: Koppelingen<br>12 downloaden: Koppelingen afsluiten | 100: Aangepaste koppelingen en `trackAction` oproepen in mobiele SDK&#39;s<br>101: Koppelingen<br>102 downloaden: Koppelingen afsluiten |
| Milestone-video | 31: Mediastart<br>32: Media-updates (geen andere variabele-verwerking)<br>33: Media-updates (met andere variabelen) | 76: Mediastart<br>77: Media-updates (geen andere variabele-verwerking)<br>78: Media-updates (met andere variabelen) |
| Hartslagvideo | 50: Start van mediastream (niet-Primetime)<br>51: Mediastroom close (non-Primetime)<br>52: Scrubbing van de mediastream (niet-Primetime)<br>53: Mediastream blijft in leven (niet-Primetime)<br>54: Mediastroom en start (niet-Primetime)<br>55: Mediastroom en close (niet-Primetime)<br>56: Mediastroom en scrubben (niet-Primetime)<br>60: Start<br>61 van primaire mediastream: Primetime mediastream close<br>62: Primetime-mediastream scrubben<br>63: Primetime-mediastream blijft in leven<br>64: Primetime-mediastream en start<br>65: Primetime mediastream en close<br>66: Primetime-mediastream en scrubben | Dezelfde waarde als `post_page_event` |
| Enquête | 40: Om het even welke vraag die van Onderzoek wordt geproduceerd | 80: Om het even welke vraag die van Onderzoek wordt geproduceerd |
| Analyses voor doel | 70: Actief bevat gegevens over doelactiviteit | Dezelfde waarde als `post_page_event` |
