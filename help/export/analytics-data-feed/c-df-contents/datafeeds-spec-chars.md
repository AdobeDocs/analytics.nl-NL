---
description: Informatie over speciale tekens die worden gebruikt in de gegevensfeed.
keywords: Gegevensfeed;taak;speciale tekens;hit_data;multi-getaxeerde variabelen;events_list;products_list;mvars
subtopic: data feeds
title: Speciale tekens in gegevensfeeds
feature: Data Feeds
exl-id: b816ebc5-0b23-4420-aa8c-b88953d031e6
source-git-commit: 6e59ee3cb3eb59b025053603cd1357c5a2709d00
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 1%

---

# Speciale tekens in gegevensfeeds

Adobe gebruikt escape-logica om ervoor te zorgen dat waarden die naar gegevensverzamelingsservers worden verzonden, geen bestanden voor gegevensinvoer beschadigen of negatief beïnvloeden. De volgende tekens worden door Adobe gereserveerd voor de volgende doeleinden in `hit_data.tsv`.

## Speciale tekens in een kolom

| Teken | Beschrijving |
|--- |--- |
| `\t` | Geeft een tab aan. Hiermee wordt het einde van een kolom of gegevensveld gemarkeerd. |
| `\n` | Vertegenwoordigt een nieuwe regel. Hiermee markeert u het einde van een rij of treffer. |
| `\` | Backslash. Hiermee worden tekens verwijderd als deze worden verzonden als onderdeel van gegevensverzameling. |

Wanneer deze gereserveerde waarden worden voorafgegaan door een backslash, zijn ze verzonden als onderdeel van gegevensverzameling.

| Teken | Beschrijving |
|--- |--- |
| `\\t` | De waarde &#39;`\t`&#39; is verzonden tijdens gegevensverzameling, beschermd door Adobe. |
| `\\n` | De waarde &#39;`\n`&#39; is verzonden tijdens gegevensverzameling, beschermd door Adobe. |
| `\\` | De waarde &#39;`\`&#39; is verzonden tijdens gegevensverzameling, beschermd door Adobe. |

Een bezoeker van uw site gebruikt bijvoorbeeld interne zoekopdrachten en zoekt naar `"search\nstring"`. U vult eVar1 met `"search\nstring"`en deze waarde naar Adobe verzenden. Adobe ontvangt deze hit en escapeert de nieuwe regel die in de tekenreeks is opgenomen. De werkelijke waarde die in onbewerkte gegevens is geplaatst, is `"search\\nstring"`.

## Speciale tekens in multigetaxeerde variabelen (events_list, products_list, mvars)

De volgende tekens hebben een speciale betekenis in kolommen die meerdere waarden kunnen bevatten.

| Teken | Beschrijving |
|--- |--- |
| `,` | Komma. Geeft het einde van een individuele waarde aan. Hiermee worden de tekenreeksen van producten, gebeurtenis-id&#39;s of andere waarden gescheiden. |
| `;` | Halfdubbele punt. Vertegenwoordigt het einde van een afzonderlijke waarde in `product_list`. Hiermee scheidt u velden binnen één productreeks. |
| `=` | Gelijk aan teken. Hiermee wordt een waarde toegewezen aan een gebeurtenis in `product_list`. |
| `^` | Caret. Hiermee worden tekens verwijderd als deze worden verzonden als onderdeel van gegevensverzameling. |

Wanneer deze gereserveerde waarden worden voorafgegaan door een invoegpunt, zijn ze verzonden als onderdeel van de gegevensverzameling.

| Teken | Beschrijving |
|--- |--- |
| `^,` | De waarde &#39;`,`&#39; is verzonden tijdens gegevensverzameling, beschermd door Adobe. |
| `^;` | De waarde &#39;`;`&#39; is verzonden tijdens gegevensverzameling, beschermd door Adobe. |
| `^=` | De waarde &#39;`=`&#39; is verzonden tijdens gegevensverzameling, beschermd door Adobe. |
| `^^` | De waarde &#39;`^`&#39; is verzonden tijdens gegevensverzameling, beschermd door Adobe. |
