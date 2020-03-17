---
description: Informatie over speciale tekens die worden gebruikt in de gegevensfeed.
keywords: Data Feed;job;special characters;hit_data;multi-valued variables;events_list;products_list;mvvars
subtopic: data feeds
title: Speciale tekens in gegevensfeeds
topic: Reports and analytics
uuid: 5efe019b-39e6-4226-a936-88202a02f5e6
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Speciale tekens in gegevensfeeds

Adobe gebruikt escape-logica om ervoor te zorgen dat waarden die naar gegevensverzamelingsservers worden verzonden, geen bestanden voor gegevensinvoer beschadigen of negatief beïnvloeden. De volgende tekens zijn door Adobe gereserveerd voor de volgende doeleinden in `hit_data.tsv`.

## Speciale tekens in een kolom

| Teken | Beschrijving |
|--- |--- |
| `\t` | Geeft een tab aan. Hiermee wordt het einde van een kolom of gegevensveld gemarkeerd. |
| `\n` | Vertegenwoordigt een nieuwe regel. Hiermee markeert u het einde van een rij of treffer. |
| `\` | Backslash. Hiermee worden tekens verwijderd als deze worden verzonden als onderdeel van gegevensverzameling. |

Wanneer deze gereserveerde waarden worden voorafgegaan door een backslash, zijn ze verzonden als onderdeel van gegevensverzameling.

| Teken | Beschrijving |
|--- |--- |
| `\\t` | De waarde &#39;`\t`&#39; is verzonden tijdens de gegevensverzameling en is door Adobe beschermd. |
| `\\n` | De waarde &#39;`\n`&#39; is verzonden tijdens de gegevensverzameling en is door Adobe beschermd. |
| `\\` | De waarde &#39;`\`&#39; is verzonden tijdens de gegevensverzameling en is door Adobe beschermd. |

Een bezoeker van uw site gebruikt bijvoorbeeld een interne zoekopdracht en zoekt naar &quot;zoeken\ntekenreeks&quot;. U vult eVar1 met &quot;search\nstring&quot; en verzendt die waarde naar Adobe. Adobe ontvangt deze hit en escapeert de nieuwe regel die in de tekenreeks is opgenomen. De werkelijke waarde die in onbewerkte gegevens wordt geplaatst, is &quot;search\\nstring&quot;.

## Speciale tekens in multigetaxeerde variabelen (events_list, products_list, mvars)

De volgende tekens hebben een speciale betekenis in kolommen die meerdere waarden kunnen bevatten.

| Teken | Beschrijving |
|--- |--- |
| `,` | Komma. Geeft het einde van een individuele waarde aan. Hiermee worden de tekenreeksen van producten, gebeurtenis-id&#39;s of andere waarden gescheiden. |
| `;` | Halfdubbele punt. Geeft het einde aan van een afzonderlijke waarde in `product_list`. Hiermee scheidt u velden binnen één productreeks. |
| `=` | Gelijk aan teken. Wijst een waarde toe aan een gebeurtenis in `product_list`. |
| `^` | Caret. Hiermee worden tekens verwijderd als deze worden verzonden als onderdeel van gegevensverzameling. |

Wanneer deze gereserveerde waarden worden voorafgegaan door een invoegpunt, zijn ze verzonden als onderdeel van de gegevensverzameling.

| Teken | Beschrijving |
|--- |--- |
| `^,` | De waarde &#39;`,`&#39; is verzonden tijdens de gegevensverzameling en is door Adobe beschermd. |
| `^;` | De waarde &#39;`;`&#39; is verzonden tijdens de gegevensverzameling en is door Adobe beschermd. |
| `^=` | De waarde &#39;`=`&#39; is verzonden tijdens de gegevensverzameling en is door Adobe beschermd. |
| `^^` | De waarde &#39;`^`&#39; is verzonden tijdens de gegevensverzameling en is door Adobe beschermd. |
