---
description: Als u de methode voor het verzamelen van gegevens in de insteekmodule JavaScript hebt geselecteerd, kopieert u de volgende coderegels en voegt u deze toe aan de Adobe Analytics-code op uw pagina's.
title: Adobe Analytics-plug-incode
uuid: b10345ba-1e80-4e5c-af87-6e6a9dc87c00
translation-type: tm+mt
source-git-commit: a02fb674ea71a05e085c8e9b2dc4460f62f2cd51

---


# Adobe Analytics-plug-incode{#adobe-analytics-plug-in-code}

Als u de methode voor het verzamelen van gegevens in de insteekmodule JavaScript hebt geselecteerd, kopieert u de volgende coderegels en voegt u deze toe aan de Adobe Analytics-code op uw pagina&#39;s.

`/*`

`* Plugin: getQueryParam 2.3`

`*/ s.getQueryParam=new Function("p","d","u","" +"var s=this,v='',i,t;d=d?d:'';u=u?u:(s.pageURL?s.pageURL:s.wd.locati" +"on);if(u=='f')u=s.gtfs().location;while(p){i=p.indexOf(',');i=i<0?p" +".length:i;t=s.p_gpv(p.substring(0,i),u+'');if(t){t=t.indexOf('#')>-" +"1?t.substring(0,t.indexOf('#')):t;}if(t)v+=v?d+t:t;p=p.substring(i=" +"=p.length?i:i+1)}return v"); s.p_gpv=new Function("k","u","" +"var s=this,v='',i=u.indexOf('?'),q;if(k&&i>-1){q=u.substring(i+1);v" +"=s.pt(q,'&','p_gvf',k)}return v"); s.p_gvf=new Function("t","k","" +"if(t){var s=this,i=t.indexOf('='),p=i<0?t:t.substring(0,i),v=i<0?'T" +"rue':t.substring(i+1);if(p.toLowerCase()==k. oLowerCase())return s." +"epa(v)}return ''");`

`/*in the s_doPlugins function`

`s.campaign=s.getQueryParam("ET_CID"); //places query param value from cid in campaign variable s.eVar2=s.getQueryParam("ET_RID"); //places query param value from rid in eVar2 variable`

> [!NOTE] De bovenstaande plug-in gaat ervan uit dat bepaalde aangepaste handelvariabelen (eVars) beschikbaar zijn. Als de variabelen die in de bovenstaande plug-in zijn opgegeven, niet beschikbaar zijn in de implementatie van Adobe Analytics, vervangt u deze door de variabelen die beschikbaar zijn.

