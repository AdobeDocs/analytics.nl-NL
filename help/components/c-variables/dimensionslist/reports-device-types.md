---
description: Hiermee groepeert u mobiele apparaten in mobiele telefoons, tablets, e-readers, gameconsoles, televisies, set-top boxes, mediaspelers en andere categorieën op hoog niveau, zodat u de distributie tussen de typen mobiele apparaten kunt zien.
title: Apparaattypen
topic: Reports
uuid: e1224769-9a94-4cad-a1ed-e285d60d23f3
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# Apparaattypen

Hiermee groepeert u mobiele apparaten in mobiele telefoons, tablets, e-readers, gameconsoles, televisies, set-top boxes, mediaspelers en andere categorieën op hoog niveau, zodat u de distributie tussen de typen mobiele apparaten kunt zien.

Deze dimensie is ook handig voor het definiëren van segmenten voor gebruikers van telefoons en tablets door te segmenteren waar het type mobiel apparaat gelijk is aan &quot;apparaattype&quot;.

**Dynamische apparaatgegevens**

Deze dimensie gebruikt dynamische apparatengegevens die voortdurend worden bijgewerkt aangezien de nieuwe apparaten worden vrijgegeven en geïdentificeerd. Bijvoorbeeld, zou een nieuwe tablet die tijdens de huidige maand wordt vrijgegeven verkeerd kunnen worden geïdentificeerd aangezien het nog niet in het apparatengegevensbestand bestaat. Wanneer het apparatengegevensbestand met het nieuwe apparaat wordt bijgewerkt, worden om het even welke veranderingen als gevolg toegepast op alle toekomstige rapporteringsdata (niet aan historische gegevens). Daarom zou u kleine verschillen op dit verslag voor historische data in tijd kunnen zien. In het algemeen zal het meest actuele verslag over elke verslagperiode beschikken over de meest nauwkeurige gegevens.

De gegevens voor dit rapport worden gevuld met de userAgent-tekenreeks van de bezoeker.

>[!NOTE]
>Alleen wijzigingen die zijn aangebracht in een bestaande mobiele id, worden met terugwerkende kracht doorgevoerd. Als het apparaat nieuw is en nog geen mobiele id heeft, beginnen de enige gegevens die aan dit apparaat worden gekoppeld op de datum waarop een id aan de apparaatdatabase wordt toegevoegd.
