---
title: websiteBot
description: Identificeer bots dynamisch met behulp van muisbeweging.
translation-type: tm+mt
source-git-commit: 7199a9fac01575bf446e69d24642752cd055e915
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---


# Adobe-plug-in: websiteBot

>[!IMPORTANT]
>
>Deze plug-in wordt geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-in, inclusief installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met deze plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Met de `websiteBot`-plug-in kunt u dynamisch bepalen of bezoekers van een desktopcomputer een knooppunt zijn. U kunt deze gegevens gebruiken om grotere nauwkeurigheid in alle types van rapportering te drijven, die u een betere manier geeft om wettig plaatsverkeer te meten.

Deze plug-in voert twee controles uit:

* Eerst wordt met de variabele `navigator.UserAgent` bepaald of het apparaat een desktopapparaat of een mobiel apparaat is. Mobiele apparaten worden genegeerd.
* Als het een desktopapparaat is, wordt er een gebeurtenislistener toegevoegd voor muisbewegingen.

Als de gebruikersagent zich op een bureaublad bevindt en er geen muisbeweging wordt gedetecteerd, stelt de insteekmodule de variabele `websiteBot` in op `true`. Als de gebruikersagent een mobiel apparaat is of als muisbeweging wordt gedetecteerd, stelt de insteekmodule de variabele `websiteBot` in op `false`.

## Vereisten

Adobe raadt het volgende aan voordat u deze plug-in gebruikt:

* **EVar-instellingen** configureren: Stel een eVar in onder  [Conversievariabelen in de instellingen van de rapportsuite ](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) . Stel de vervaldatum in op **&quot;Bezoeker&quot;** en de toewijzing op **&quot;Oorspronkelijke waarde (eerst)&quot;**.
* **Verzamel gebruikersagent in een afzonderlijke variabele**: Verzamel de userAgent-tekenreeks in een aparte variabele om de effectiviteit van deze insteekmodule te controleren. Stel een eVar in op `navigator.UserAgent` bij elke druk om deze gegevens te verzamelen.

## Plug-in installeren met de aangepaste code-editor van Launch

1. Meld u met uw Adobe-id aan bij [launch.adobe.com](https://launch.adobe.com).
1. Klik op de gewenste eigenschap.
1. Ga naar het [!UICONTROL Extensions] lusje, dan klik [!UICONTROL Configure] knoop onder de uitbreiding van Adobe Analytics.
1. Breid [!UICONTROL Configure tracking using custom code] accordeon uit, die [!UICONTROL Open Editor] knoop openbaart.
1. Open de aangepaste code-editor en plak de onderstaande plug-incode in het bewerkingsvenster.
1. Sla de wijzigingen in de extensie Analytics op en publiceer deze.

## Installeer de plug-in met AppMeasurement

Kopieer en plak de volgende code ergens in het AppMeasurement-bestand nadat het analytics tracking-object is geïnstantieerd (met [`s_gi`](../functions/s-gi.md)). Door opmerkingen en versienummers van de code in uw implementatie te behouden, kunt u Adobe doen met het oplossen van mogelijke problemen.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: websiteBot BETA v0.1 */
websiteBot = true;if(!/(android|bb\d+|meego).+mobile|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|ip(hone|od)|ipad|iris|kindle|Android|Silk|lge |maemo|midp|mmp|netfront|opera m(ob|in)i|palm( os)?|phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|windows (ce|phone)|xda|xiino/i.test(navigator.userAgent)||/1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|qtek|r380|r600|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|x700|yas\-|your|zeto|zte\-/i.test(navigator.userAgent.substr(0,4))){document.addEventListener('mousemove',function detectMouseMove(){document.removeEventListener('mousemove',detectMouseMove,false);websiteBot=false;})}else websiteBot=false;
/******************************************** END CODE TO DEPLOY ********************************************/
```

## De plug-in gebruiken

De variabele `websiteBot` is een booleaanse waarde. Als de insteekmodule een bot detecteert, wordt `true` geretourneerd. anders wordt `false` geretourneerd.

## Voorbeelden

```js
// Set eVar1 to detect bots. Dimension items in reporting are "true" or "false"
s.eVar1 = websiteBot;

// Use a ternary operator to set eVar values
s.eVar1 = websiteBot ? "Bot detected" : "Not a bot";
```

## Versiehistorie

### 0.1 (19 januari 2021)

* Bètaversie.
