---
title: Adobe Analytics implementeren met de extensie Analytics
description: Leer hoe u Adobe Analytics implementeert met tags en de extensie Analytics
feature: Launch Implementation
source-git-commit: e6b40881a543b43c03b612c7e7b0d9bd09f44c0d
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Adobe Analytics implementeren met de extensie Analytics

Tijdens de levensduur van Adobe Analytics heeft Adobe verschillende methoden aangeboden om code op uw site te implementeren voor gegevensverzameling. Aanbevolen Adobe is door tags in Adobe Experience Platform.

Tags in Adobe Experience Platform zijn een oplossing voor tagbeheer waarmee u naast andere coderingsvereisten ook analytische code kunt implementeren. Adobe biedt integratie met andere oplossingen en producten aan, en laat u douanecode opstellen. Al deze taken kunnen worden uitgevoerd zonder dat ontwikkelingsteams in uw organisatie code op uw site hoeven bij te werken.

Alle klanten met een actief Adobe Experience Cloud-contract kunnen tags gebruiken. Als u niet zeker bent als u toegang hebt, contacteer één van de het systeembeheerders van Experience Cloud van uw organisatie.

Een overzicht op hoog niveau van de uitvoeringstaken:

![Adobe Analytics die de uitbreidingsworkflow voor Analytics gebruikt](../assets/analytics-extension-annotated.png)

|<div style="width:20px"></div>| Taak | Meer informatie | |-| —|| | 1 | Zorg ervoor dat u beschikt over **een rapportsuite gedefinieerd**. | [Report Suite Manager](../../admin/admin/c-manage-report-suites/report-suites-admin.md) | | 2 | **Een gegevenslaag maken** om het bijhouden van de gegevens op uw website te beheren. | [Een gegevenslaag maken](../prepare/data-layer.md) | | 3 | **Een tag-eigenschap maken**. Eigenschappen zijn overkoepelende containers die worden gebruikt om te verwijzen naar tagbeheergegevens.| [Een Adobe Analytics-tageigenschap maken](../launch/create-analytics-property.md) | | 4 | **De extensie Analytics installeren** in de eigenschap tag. Configureer de extensie Analytics om gegevens naar Adobe Analytics te verzenden. | [Overzicht Adobe Analytics-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/analytics/overview.html?lang=en) | | 5 | **Distribueren naar een ontwikkelomgeving**. Zorg voor een omgeving waarin u de ontwikkeling van tags kunt doorlopen. | [Implementeer een analytische implementatie in een ontwikkelomgeving](./deploy-dev.md) | | 6 | **Valideren en publiceren naar productie**. Voeg de eigenschap tag toe aan uw website. Dan gebruik gegevenselementen, regels, etc., om uw implementatie aan te passen.| [Een ontwikkelimplementatie valideren en publiceren naar productie](./validate-publish-prod.md) |

## Aanvullende bronnen

Tags kunnen in hoge mate worden aangepast. Meer informatie over hoe u optimaal kunt profiteren van Adobe Analytics door de juiste gegevens op te nemen in uw implementatie.

- [Documentatie over tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html#): Leer hoe de interface werkt en welke extensies beschikbaar zijn.

- [Implementatievariabelen](../vars/overview.md): Bepaal welke variabelen u naar de servers van de gegevensinzameling wilt verzenden.
