---
title: Type referentie
description: Het type referentie, afhankelijk van waar de bezoeker vandaan komt.
feature: Dimensions
exl-id: a6cfcbf4-cd08-4e7f-8e86-47488ceb0ea3
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Type referentie

De dimensie &#39;Type referentie&#39; rapporteert welke generieke kanalen bezoekers hebben aangeklikt om op uw site te komen. Adobe handhaaft de regels voor elk afmetingspunt, in tegenstelling tot [Marketingkanalen](marketing-channel.md), waar uw organisatie regels voor elk kanaal handhaaft.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar veelvoudige raadplegingslijsten intern aan Adobe. Elke waarde is gebaseerd op de [referentie](referrer.md) van de hit, die afhankelijk is van [Interne URL-filters](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md). Zorg ervoor dat de verwijzingsafmeting en interne filters URL correct worden gevormd.

## Dimension-items

Dimension-items bevatten het type referentie van de hit. Specifieke waarden zijn onder meer:

* **Getypte/bladwijzer**: Er bestaan geen verwijzingsgegevens voor de hit.
* **Zoekprogramma&#39;s**: De referentie is afkomstig van een herkend zoekprogramma dat een trefwoordqueryreeks bevat.
* **Sociale netwerken:**: Referergegevens behoorden tot een door Adobe erkend sociaal netwerk.
* **Andere websites**: Referergegevens behoorden niet tot een zoekmachine of sociaal netwerk dat door Adobe wordt herkend.
* **Vaste schijf**: Referrer is afkomstig van een lokale kopie van een webpagina op de vaste schijf van de bezoeker.
* **E-mail**: Referrer is afkomstig van een URL met een protocol van `imap://` of `mail://`. Omvat geen online e-maildiensten, aangezien deze typisch gebruiken `https://` protocol.

### Sociale netwerken

De volgende lijst verwijst naar de &quot;Sociale netwerken&quot;raadplegingslijst die Adobe gebruikt. Adobe geeft deze lijst als een belediging aan klanten van Adobe Analytics. Als u zou willen adviseren dat Adobe een domein aan deze lijst toevoegt, een steunafgevaardigde in uw organisatie hebben contacteer de Zorg van de Klant.

>[!NOTE]
>
>Deze lijst is anders dan de standaardlijst met sociale netwerken in [Verwerkingsregels voor distributiekanalen](../c-marketing-channels/c-rules.md).

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
* `boards.qwant.com`
* `bolt.com`
* `brightkite.com`
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
* `linkedin.com`
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
* `pinterest.ca`
* `pinterest.fr`
* `pinterest.es`
* `pinterest.de`
* `pinterest.se`
* `pinterest.pt`
* `pinterest.dk`
* `pinterest.ie`
* `pinterest.co.kr`
* `pinterest.ch`
* `pinterest.at`
* `pinterest.`
* `pinterest.nz`
* `pinterest.ph`
* `pinterest.cl`
* `pinterest.hu`
* `pinterest.be`
* `pinterest.in`
* `pinterest.co`
* `plaxo.com`
* `plurk.com`
* `plus.url.google.com`
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
* `t.ifeng.com`
* `t.people.com.cn`
* `t.qq.com`
* `t.sina.com.cn`
* `t.sohu.com`
* `tabelog.com`
* `tagged.com`
* `taringa.net`
* `thefancy.com`
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
* `weibo.com`
* `weourfamily.com`
* `wer-kennt-wen.de`
* `wordpress.com`
* `xanga.com`
* `xing.com`
* `answers.yahoo.com`
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

Wanneer u specifieke domeinen in de dimensie van het type van &quot;Referrer&quot;bekijkt, kunnen er domeinen zijn die u onder &quot;de motoren van het Onderzoek&quot;zou verwachten die in plaats daarvan onder &quot;Andere websites&quot;worden vermeld. U ziet bijvoorbeeld `'google.com'` onder &quot;Andere websites&quot;.

* **Zoekmachinedomeinen in het dimensiemenu &#39;Zoekprogramma&#39;s&#39;**: De referentie voldoet aan alle criteria om te classificeren als een zoekmachine op Adobe. Het verwijzende domein is een geldige onderzoeksmotor, *en* De verwijzende URL bevat een parameter van het sleutelwoordvraagkoord.
* **Zoekmachinedomeinen in het item Andere websites**: De verwijzende URL voldeed niet aan alle criteria om te classificeren als zoekmachine. Algemene voorbeelden zijn subdomeinen die zijn toegewezen aan andere functies dan zoekopdrachten. Bijvoorbeeld: `mail.google.com` of `autos.yahoo.com` zijn geen zoekmachines, maar bevinden zich op een topdomein dat vaak aan zoekopdrachten is gekoppeld. Deze subdomeinen bevatten geen queryreeks voor trefwoorden, daarom worden deze opgenomen onder &#39;Andere websites&#39; in plaats van &#39;Zoekprogramma&#39;s&#39;.
