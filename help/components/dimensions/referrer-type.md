---
title: Type referentie
description: Het type referentie, afhankelijk van waar de bezoeker vandaan komt.
feature: Dimensions
exl-id: a6cfcbf4-cd08-4e7f-8e86-47488ceb0ea3
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Type referentie

Het &quot;Type van Referateur&quot;[ afmeting ](overview.md) meldt welke generische kanaalbezoekers door klikten om bij uw plaats aan te komen. Adobe handhaaft de regels voor elk afmetingspunt, in tegenstelling tot [ de kanalen van de Marketing ](marketing-channel.md), waar uw organisatie regels voor elk kanaal handhaaft.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar meerdere opzoektabellen die intern zijn voor Adobe. Elke waarde is gebaseerd op [ verwijzer ](referrer.md) van de klap, die van [ Interne filters URL ](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) afhangt. Zorg ervoor dat de verwijzingsafmeting en interne filters URL correct worden gevormd.

## Dimension-objecten

Dimension-objecten bevatten het type referentie van de hit. Specifieke waarden zijn onder meer:

* **Typed/Bookmarked**: Geen verwijzersgegevens bestaan voor de hit.
* **de motoren van het Onderzoek**: De verwijzer kwam uit een erkende onderzoeksmotor die een koord van de sleutelwoordvraag omvat.
* **Sociale netwerken:**: De gegevens van de verwijzer behoorden tot een Adobe-erkend sociaal netwerk.
* **Andere websites**: De gegevens van de verwijzer behoorden niet tot een onderzoeksmotor of sociaal netwerk dat Adobe erkent.
* **Vaste aandrijving**: De verwijzing kwam van een lokaal exemplaar van een Web-pagina op de harde aandrijving van de bezoeker voort.
* **E-mail**: De verwijzing kwam van een URL met een protocol van `imap://` of `mail://` voort. Omvat geen online e-mailservices, aangezien deze doorgaans het `https://` -protocol gebruiken.

### Sociale netwerken

De volgende lijst verwijst naar de opzoektabel &#39;Sociale netwerken&#39; die Adobe gebruikt. Adobe biedt deze lijst als een belediging aan klanten van Adobe Analytics. Als u wilt aanbevelen dat Adobe een domein aan deze lijst toevoegt, moet u een medewerker van de support in uw organisatie contact opnemen met de klantenservice.

>[!NOTE]
>
>Deze lijst is verschillend dan de standaardlijst van sociale netwerken in [ de verwerkingsregels van het Kanaal van de Marketing ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-rules.md).

* `12seconds.tv`
* `4travel.jp`
* `advogato.org`
* `ameba.jp`
* `anobii.com`
* `answers.yahoo.com`
* `asmallworld.net`
* `avforums.com`
* `backtype.com`
* `badoo.com`
* `bebo.com`
* `bigadda.com`
* `bigtent.com`
* `biip.no`
* `blackplanet.com`
* `blog.seesaa.jp`
* `blogspot.com`
* `blogster.com`
* `blomotion.jp`
* `bolt.com`
* `brightkite.com`
* `bsky.app`
* `buzznet.com`
* `cafemom.com`
* `care2.com`
* `classmates.com`
* `cloob.com`
* `collegeblender.com`
* `cyworld.co.kr`
* `cyworld.com.cn`
* `dailymotion.com`
* `delicious.com`
* `deviantart.com`
* `digg.com`
* `diigo.com`
* `disqus.com`
* `draugiem.lv`
* `facebook.com`
* `faceparty.com`
* `fc2.com`
* `flickr.com`
* `flixster.com`
* `fotolog.com`
* `foursquare.com`
* `friendfeed.com`
* `friendsreunited.com`
* `friendsreunited.co.uk`
* `friendster.com`
* `fubar.com`
* `gaiaonline.com`
* `geni.com`
* `go.bsky.app`
* `goodreads.com`
* `plus.google.com`
* `plus.url.google.com`
* `grono.net`
* `habbo.com`
* `hatena.ne.jp`
* `hi5.com`
* `hotnews.infoseek.co.jp`
* `hyves.nl`
* `ibibo.com`
* `identi.ca`
* `t.ifeng.com`
* `imeem.com`
* `instagram.com`
* `intensedebate.com`
* `irc-galleria.net`
* `iwiw.hu`
* `jaiku.com`
* `jp.myspace.com`
* `kaixin001.com`
* `kakaku.com`
* `kanshin.com`
* `kozocom.com`
* `last.fm`
* `likeshop.me`
* `linkedin.com`
* `linkin.bio`
* `livejournal.com`
* `lnkd.in`
* `meetup.com`
* `me2day.net`
* `mister-wong.com`
* `mixi.jp`
* `mixx.com`
* `mouthshut.com`
* `mp.weixin.qq.com`
* `multiply.com`
* `mumsnet.com`
* `myheritage.com`
* `mylife.com`
* `myspace.com`
* `myyearbook.com`
* `nasza-klasa.pl`
* `matome.naver.jp`
* `netlog.com`
* `nettby.no`
* `netvibes.com`
* `nextdoor.com`
* `nicovideo.jp`
* `ning.com`
* `odnoklassniki.ru`
* `ok.ru`
* `orkut.com`
* `pakila.jp`
* `photobucket.com`
* `pinterest.com`
* `pinterest.co.uk`
* `plaxo.com`
* `plurk.com`
* `po.st`
* `reddit.com`
* `renren.com`
* `skyrock.com`
* `slideshare.net`
* `smcb.jp`
* `smugmug.com`
* `snapchat.com`
* `sonico.com`
* `studivz.net`
* `stumbleupon.com`
* `t.163.com`
* `t.co`
* `t.hexun.com`
* `t.people.com.cn`
* `t.qq.com`
* `t.sina.com.cn`
* `t.sohu.com`
* `tabelog.com`
* `tagged.com`
* `taringa.net`
* `thefancy.com`
* `threads.com`
* `threads.net`
* `tiktok.com`
* `toutiao.com`
* `tripit.com`
* `trombi.com`
* `trytrend.jp`
* `tuenti.com`
* `tumblr.com`
* `twine.com`
* `twitter.com`
* `uhuru.jp`
* `viadeo.com`
* `vimeo.com`
* `vk.com`
* `wayn.com`
* `web-cdn.bsky.app`
* `weibo.com`
* `weourfamily.com`
* `wer-kennt-wen.de`
* `wordpress.com`
* `x.com`
* `xanga.com`
* `xing.com`
* `yammer.com`
* `yaplog.jp`
* `yelp.com`
* `yelp.co.uk`
* `youku.com`
* `youtube.com`
* `yozm.daum.net`
* `yuku.com`
* `zooomr.com`
* `zhihu.com`

### Zoekprogramma&#39;s in het item Andere websites

Wanneer u specifieke domeinen in de dimensie van het type van &quot;Referrer&quot;bekijkt, kunnen er domeinen zijn die u onder &quot;de motoren van het Onderzoek&quot;zou verwachten die in plaats daarvan onder &quot;Andere websites&quot;worden vermeld. U ziet bijvoorbeeld `'google.com'` onder &#39;Andere websites&#39;.

* **de motordomeinen van het Onderzoek in het de afmetingspunt van de &quot;motoren van het Onderzoek&quot;**: De verwijzer voldeed aan alle criteria om als onderzoeksmotor door Adobe te classificeren. Het verwijzende domein is een geldige onderzoeksmotor, *en* verwijzende URL bevat een parameter van het sleutelwoordvraagkoord.
* **de motordomeinen van het Onderzoek in het &quot;Andere websites&quot;afmetingspunt**: Het verwijzen URL voldeed niet aan alle criteria om als onderzoeksmotor te classificeren. Algemene voorbeelden zijn subdomeinen die zijn toegewezen aan andere functies dan zoekopdrachten. `mail.google.com` of `autos.yahoo.com` zijn bijvoorbeeld geen zoekprogramma&#39;s, maar bevinden zich in een domein op hoofdniveau dat vaak wordt gekoppeld aan zoekopdrachten. Deze subdomeinen bevatten geen queryreeks voor trefwoorden, daarom worden deze opgenomen onder &#39;Andere websites&#39; in plaats van &#39;Zoekprogramma&#39;s&#39;.
