## amass



### 最強コマンド
```
 amass_old enum -d amiya.co.jp -active -brute -src -ip -json aeiueoao.json -include arin, abuseipdb, alientvault, alterations, anubisdb, archiveit, arquivo, ask, askdns, bgptools, bgpview, baidu, bing, brute forcing, bufferover, censys, certspotter, cloudflare, commoncrawl, crtsh, dnsdumpster, digitorus, duckduckgo, fullhunt, gists, googlect, greynoise, haw, hackerone, hackertarget, hyperstat, ipv4info, maltiverse, mnemonic, n45ht, networksdb, pkey, radb, rapiddns, riddler, robtex, searchcode, searx, shadowserver, sitedossier, sonarsearch, spyonweb, sublist3rapi, teamcymru, threatcrowd, threatminer, ukwebarchive, urlscan, wayback, yahoo
```
コマンドの部分amass_oldはamassに変える。ただし、古いバージョンを使うこと。これは3.19.2


### brute force
```
amass enum -brute -d amiya.co.jp
```
bruteつけたほうが早かった

### multiple domains
```
amass enum -df domains.txt
```
-df	:Path to a file providing root domain names	amass enum -df domains.txt

or
```
amass enum -d example1.com -d example2.com
```
と思ったけど、-d重ねるのは無理かもしれない
内部ではどう動いているかわからないが、なんとなく並列でやってそう
アウトプットの仕分けはドメイン名を見て勝手にやれ。

### -list option
```
amass_old enum -list
```
利用可能なデータソースを表示

### -src option
どこからとってきたのかを表示する
ブルートフォースの時は\[Brute Forcing\]と表示される。たぶん
```
amass_old enum -d yahoo.co.jp -brute -src -json yahoo_src_brute.json
[Digitorus]       yahoo.co.jp
[Crtsh]           stgproxy.shub.yahoo.co.jp
[Crtsh]           eisen-prueba-c.yahoo.co.jp
[Crtsh]           settle.shub.yahoo.co.jp
[DNS]             ns01.yahoo.co.jp
[Crtsh]           sandbox.ca.wallet.yahoo.co.jp
[Crtsh]           beta.api.sbm.edit.yahoo.co.jp
[Digitorus]       mail.yahoo.co.jp
[Crtsh]           signup.im.yahoo.co.jp
[Crtsh]           eisen-core.yahoo.co.jp
[DNS]             ns12.yahoo.co.jp
[Crtsh]           raccoon2.ci.kks.yahoo.co.jp
[Crtsh]           stg-yjapp.yahoo.co.jp
[Crtsh]           detailsbeta.payment.yahoo.co.jp
[Crtsh]           b95.stage.yahoo.co.jp
[Crtsh]           shirosuke.yahoo.co.jp
[Digitorus]       ssl-tools.kainavi.search.yahoo.co.jp
[Crtsh]           id.yahoo.co.jp
[Crtsh]           gamma-mobilepf.yahoo.co.jp
[Crtsh]           oshigotoguide.froma.yahoo.co.jp
[Crtsh]           i.payment.mobile.yahoo.co.jp
[Crtsh]           notice.yahoo.co.jp
[Crtsh]           chakumero.yahoo.co.jp
[Crtsh]           cert.webhosting.yahoo.co.jp
[Crtsh]           achart.yahoo.co.jp
[DNS]             mx1.mail.yahoo.co.jp
[Crtsh]           security.yahoo.co.jp
[Crtsh]           gamma-m.yahoo.co.jp
[Crtsh]           openlog.yahoo.co.jp
[Crtsh]           snltool.store.yahoo.co.jp
[Crtsh]           lifemagazine.yahoo.co.jp
[RapidDNS]        auctions.search.yahoo.co.jp
[RapidDNS]        storeuser2.auctions.yahoo.co.jp
[Brute Forcing]   app.mail.yahoo.co.jp
[RapidDNS]        img47.auctions.yahoo.co.jp
[AlienVault]      fan.yahoo.co.jp
[Crtsh]           learning.yahoo.co.jp
[AlienVault]      fusion.insurance.yahoo.co.jp
[Crtsh]           bs.shopping.yahoo.co.jp
[Crtsh]           page23.auctions.yahoo.co.jp
[RapidDNS]        mg2.mail.yahoo.co.jp
[Crtsh]           bank.yahoo.co.jp
[RapidDNS]        keep.loco.yahoo.co.jp
[RapidDNS]        anime.geocities.yahoo.co.jp
[RapidDNS]        info.games.yahoo.co.jp
[RapidDNS]        froma.mobile.yahoo.co.jp
[AlienVault]      sidejob.yahoo.co.jp
[Crtsh]           b97.yahoo.co.jp
[RapidDNS]        img327.auctions.yahoo.co.jp
[RapidDNS]        bridge.yahoo.co.jp
[RapidDNS]        timer.ypc.yahoo.co.jp
[RapidDNS]        img335.auctions.yahoo.co.jp
[RapidDNS]        img167.auctions.yahoo.co.jp
[RapidDNS]        myname.mail.yahoo.co.jp
[RapidDNS]        docs.donation.yahoo.co.jp
[RapidDNS]        provider.bb.yahoo.co.jp
[RapidDNS]        fantasy.sports.yahoo.co.jp
[RapidDNS]        license.autos.yahoo.co.jp
[Crtsh]           order.shopping.yahoo.co.jp
[RapidDNS]        info.box.yahoo.co.jp
[RapidDNS]        owarai.variety.yahoo.co.jp
[RapidDNS]        openwatchlist6.auctions.yahoo.co.jp
[RapidDNS]        img45.auctions.yahoo.co.jp
[Brute Forcing]   rd.store.yahoo.co.jp
[RapidDNS]        soniccony5001-vm12.mail.kks.yahoo.co.jp
[RapidDNS]        nfs-f10medi001.auc.kks.yahoo.co.jp
^C
OWASP Amass v3.19.2                               https://github.com/OWASP/Amass
--------------------------------------------------------------------------------
1164 names discovered - brute: 23, cert: 507, dns: 23, scrape: 507, api: 104
--------------------------------------------------------------------------------
ASN: 2554 - IDC2554 Yahoo Japan Corporation
        202.218.78.0/23         1    Subdomain Name(s)
ASN: 24572 - YAHOO-JP-AS-AP Yahoo Japan
        114.110.48.0/20         10   Subdomain Name(s)
        183.79.0.0/16           283  Subdomain Name(s)
        124.83.128.0/17         304  Subdomain Name(s)
        114.111.64.0/18         27   Subdomain Name(s)
ASN: 23816 - YAHOO Yahoo Japan Corporation
        182.22.0.0/17           654  Subdomain Name(s)
        203.216.224.0/19        17   Subdomain Name(s)
        118.151.224.0/19        11   Subdomain Name(s)
        202.93.64.0/19          21   Subdomain Name(s)
        211.14.12.0/22          5    Subdomain Name(s)
        211.14.20.0/22          3    Subdomain Name(s)
        2404:a600::/32          1    Subdomain Name(s)
ASN: 9607 - BBTOWER BroadBand Tower, Inc.
        211.14.24.0/23          7    Subdomain Name(s)
ASN: 4694 - IDCF IDC Frontier Inc.
        164.46.0.0/16           1    Subdomain Name(s)
ASN: 7506 - INTERQ GMO Internet,Inc
        210.157.0.0/19          1    Subdomain Name(s)
        210.172.128.0/18        1    Subdomain Name(s)
ASN: 55898 - YAHOO-CORP Yahoo Japan Corporation
        211.14.26.0/23          19   Subdomain Name(s)
        2405:8500::/32          3    Subdomain Name(s)
        203.141.54.0/24         4    Subdomain Name(s)
        211.14.8.0/24           18   Subdomain Name(s)
        103.2.244.0/22          1    Subdomain Name(s)
ASN: 0 - Not routed
        202.239.0.0/20          28   Subdomain Name(s)
        124.147.32.0/19         1    Subdomain Name(s)
        100.64.0.0/10           1    Subdomain Name(s)
ASN: 2497 - IIJ Internet Initiative Japan Inc.
        160.17.0.0/16           2    Subdomain Name(s)
        202.221.0.0/16          2    Subdomain Name(s)
        210.148.0.0/15          2    Subdomain Name(s)

The enumeration has finished
Discoveries are being migrated into the local database
```


```
 amass_old enum -d yahoo.co.jp -active -src -json yahoo_src_active.json
[Active Crawl]    id.yahoo.co.jp
[Crtsh]           cn02.yahoo.co.jp
[RapidDNS]        academy2012.yahoo.co.jp
[AlienVault]      honyaku.yahoo.co.jp
[Crtsh]           biz.marketing.yahoo.co.jp
[AlienVault]      address.yahoo.co.jp
[Crtsh]           squirrels.ci.sec.ssk.yahoo.co.jp
[RapidDNS]        approach.yahoo.co.jp
[Digitorus]       ssl-tools.kainavi.search.yahoo.co.jp
[Active Crawl]    ybx-test.yahoo.co.jp
[AlienVault]      sdgs.yahoo.co.jp
[RapidDNS]        area-search.yahoo.co.jp
[Active Crawl]    payment.yahoo.co.jp
[AlienVault]      paypayfleamarket.yahoo.co.jp
[RapidDNS]        rd-ymobile.yahoo.co.jp
[Crtsh]           dir.yahoo.co.jp
[RapidDNS]        compass-ymobile.yahoo.co.jp
[AlienVault]      m-ym.yahoo.co.jp
[Active Crawl]    docs-donation.yahoo.co.jp
[AlienVault]      documentary.yahoo.co.jp
[RapidDNS]        qa-m-ym.yahoo.co.jp
[RapidDNS]        global-marketing.yahoo.co.jp
[RapidDNS]        info-search.yahoo.co.jp
[Crtsh]           squirrels.ci.sec.kks.yahoo.co.jp
[RapidDNS]        sc-shopping.yahoo.co.jp
[RapidDNS]        academy2013.yahoo.co.jp
[RapidDNS]        promo-smartapp.yahoo.co.jp
[Crtsh]           live-sports.yahoo.co.jp
[RapidDNS]        whatsnewmail.yahoo.co.jp
[RapidDNS]        labs.yahoo.co.jp
[Crtsh]           insp.auctions.yahoo.co.jp
[RapidDNS]        swr.yahoo.co.jp
[RapidDNS]        opc211014027074.yahoo.co.jp
[HyperStat]       m.yahoo.co.jp
[AlienVault]      shotworks.yahoo.co.jp
[RapidDNS]        google.yahoo.co.jp
[RapidDNS]        store-info.yahoo.co.jp
[RapidDNS]        alp.yahoo.co.jp
[Crtsh]           btcs.yahoo.co.jp
[RapidDNS]        chocotle.yahoo.co.jp
[RapidDNS]        t.yahoo.co.jp
[Active Crawl]    map.yahoo.co.jp
[Crtsh]           cert.webhosting.yahoo.co.jp
[Crtsh]           i.payment.mobile.yahoo.co.jp
[Crtsh]           girlsbaito.yahoo.co.jp
[Active Crawl]    toku.yahoo.co.jp
[Crtsh]           bizx.yahoo.co.jp
[RapidDNS]        affiliate.yahoo.co.jp
[Crtsh]           hacku.yahoo.co.jp
[Crtsh]           approduce.yahoo.co.jp
[RapidDNS]        yjapp.yahoo.co.jp
[Active Crawl]    promo-mobile.yahoo.co.jp
[Crtsh]           tools.mc.wallet.yahoo.co.jp
[Crtsh]           b95-stage.yahoo.co.jp
[Crtsh]           storeinfo-koubai.auctions.yahoo.co.jp
[Crtsh]           office.yahoo.co.jp
[Crtsh]           dis.yahoo.co.jp
^C
OWASP Amass v3.19.2                               https://github.com/OWASP/Amass
--------------------------------------------------------------------------------
263 names discovered - crawl: 26, dns: 10, cert: 84, scrape: 115, api: 28
--------------------------------------------------------------------------------
ASN: 23816 - YAHOO Yahoo Japan Corporation
        203.216.224.0/19        1    Subdomain Name(s)
        202.93.64.0/19          7    Subdomain Name(s)
        118.151.224.0/19        5    Subdomain Name(s)
        182.22.0.0/17           10   Subdomain Name(s)
        211.14.12.0/22          1    Subdomain Name(s)
        211.14.20.0/22          1    Subdomain Name(s)
ASN: 55898 - YAHOO-CORP Yahoo Japan Corporation, JP
        211.14.28.0/23          8    Subdomain Name(s)
        211.14.8.0/24           7    Subdomain Name(s)
        211.14.26.0/23          4    Subdomain Name(s)
        203.141.54.0/24         1    Subdomain Name(s)
        2405:8500::/32          1    Subdomain Name(s)
ASN: 0 - Not routed
        202.239.0.0/20          4    Subdomain Name(s)
ASN: 4694 - IDCF IDC Frontier Inc., JP
        210.152.128.0/19        1    Subdomain Name(s)
        164.46.0.0/16           1    Subdomain Name(s)
ASN: 2497 - IIJ Internet Initiative Japan Inc.
        202.221.0.0/16          1    Subdomain Name(s)
ASN: 9607 - BBTOWER BroadBand Tower, Inc.
        211.14.24.0/23          1    Subdomain Name(s)
ASN: 24572 - YAHOO-JP-AS-AP Yahoo Japan
        124.83.128.0/17         16   Subdomain Name(s)
        183.79.0.0/16           228  Subdomain Name(s)

The enumeration has finished
Discoveries are being migrated into the local database
```


### passive mode with passive option
```

 amass_old enum -d yahoo.co.jp -passive -src -json yahoo_src_passive.json
[AlienVault]      sb.yahoo.co.jp
[HackerTarget]    proxy-183.79.255.102.yahoo.co.jp
[AlienVault]      search.blogs.yahoo.co.jp
[HackerTarget]    omggw7006-vm11.mail.djm.yahoo.co.jp
[AlienVault]      sidejob.yahoo.co.jp
[Crtsh]           internal.api.ops.yahoo.co.jp
[Crtsh]           ev87.ciso.ssk.ynwm.yahoo.co.jp
[Crtsh]           ycm.yahoo.co.jp
[Crtsh]           e02.edit.tnz.yahoo.co.jp
[Crtsh]           testmob02.swks.bbt.yahoo.co.jp
[Crtsh]           ca.yca.platform.yahoo.co.jp
[Crtsh]           koubaibid.auctions.yahoo.co.jp
[Crtsh]           beacon.yahoo.co.jp
[Crtsh]           token.login.yahoo.co.jp
[Crtsh]           alpsmap.yahoo.co.jp
[Crtsh]           proxy.chef.sec.bbt.yahoo.co.jp
[Crtsh]           thumbp4.mail.kks.yahoo.co.jp
[Crtsh]           alation.corp.yahoo.co.jp
[Crtsh]           ev89.ciso.ssk.ynwm.yahoo.co.jp
[Crtsh]           closer19.auctions.yahoo.co.jp
[Crtsh]           d-marketing.yahoo.co.jp
[Crtsh]           ptnpop.mail.yahoo.co.jp
[Crtsh]           beta-workplace01.corp.yahoo.co.jp
[Crtsh]           pointtool.corp.yahoo.co.jp
[Crtsh]           special-bookstore.yahoo.co.jp
[Crtsh]           h.nextmanager.travel.yahoo.co.jp
[Reverse DNS]     mta501.stg.gm.kth.ynwl.yahoo.co.jp
[Crtsh]           order.mobile.yahoo.co.jp
[Crtsh]           trade.ec.yahoo.co.jp
[Crtsh]           submanager.realestate.yahoo.co.jp
[Crtsh]           p02.ad.research.tnz.yahoo.co.jp
[Crtsh]           bus1.webhosting.yahoo.co.jp
[Crtsh]           cuisine.yahoo.co.jp
[Crtsh]           ev62.ciso.ssk.ynwm.yahoo.co.jp
[Crtsh]           influenza.yahoo.co.jp
[Crtsh]           authori.tools.auctions.yahoo.co.jp
[Crtsh]           cstools.health.yahoo.co.jp
[Crtsh]           zms-proxy.athenz.corp.yahoo.co.jp
[Crtsh]           season.yahoo.co.jp
[Crtsh]           ev92.ciso.ssk.ynwm.yahoo.co.jp
[Crtsh]           api.ptnapi.mail.yahoo.co.jp
[Crtsh]           secure.beta.mobile.yahoo.co.jp
[Crtsh]           render.git.corp.yahoo.co.jp
[Crtsh]           feedback.listing.yahoo.co.jp
[Crtsh]           koukan.yahoo.co.jp
[Crtsh]           promo-batch.shop.yahoo.co.jp
[Crtsh]           fetch2.rts.yahoo.co.jp
[Crtsh]           ev45.ciso.ssk.ynwm.yahoo.co.jp
[Crtsh]           storeportal.yahoo.co.jp
[Crtsh]           ssltools.corp.yahoo.co.jp
[Crtsh]           faceapi-jlp-stg.yahoo.co.jp
[Crtsh]           ex-purchase.gyao.yahoo.co.jp
[Crtsh]           bizmt.corp.yahoo.co.jp
[Crtsh]           test-yjapp02.yahoo.co.jp
[Crtsh]           closer10.auctions.yahoo.co.jp
[Crtsh]           ax1.tera.kks.yahoo.co.jp
[Crtsh]           proxy.payment.yahoo.co.jp
[Crtsh]           rikunabi-cookie-check.yahoo.co.jp
[Crtsh]           ev55.ciso.ssk.ynwm.yahoo.co.jp
[Reverse DNS]     mta583.kth.gm.yahoo.co.jp
[Reverse DNS]     mta544.kth.gm.yahoo.co.jp
[Reverse DNS]     mta576.kth.gm.yahoo.co.jp
[Reverse DNS]     mta537.kth.gm.yahoo.co.jp
[Reverse DNS]     mta509.kth.gm.yahoo.co.jp
[Reverse DNS]     mta532.kth.gm.yahoo.co.jp
[Reverse DNS]     mta-f05.prod.goats.vip.kth.ynwl.yahoo.co.jp
[RapidDNS]        sonicconh6002-vm4.mail.ssk.yahoo.co.jp
[Reverse DNS]     mta523.kth.gm.yahoo.co.jp
[Reverse DNS]     mta522.kth.gm.yahoo.co.jp
[Reverse DNS]     mta513.kth.gm.yahoo.co.jp
[Reverse DNS]     mta521.kth.gm.yahoo.co.jp
[RapidDNS]        ymobnh603-vm12.mail.ssk.yahoo.co.jp
[Reverse DNS]     mta542.kth.gm.yahoo.co.jp
[Reverse DNS]     mta578.kth.gm.yahoo.co.jp
[Reverse DNS]     mta528.kth.gm.yahoo.co.jp
[Reverse DNS]     mta515.kth.gm.yahoo.co.jp
[Reverse DNS]     mta570.kth.gm.yahoo.co.jp
[DNS]             rest.cntr.oa.yahoo.co.jp
[RapidDNS]        info.shinsai.yahoo.co.jp
[Reverse DNS]     mta527.kth.gm.yahoo.co.jp
[Reverse DNS]     mta569.kth.gm.yahoo.co.jp
[Reverse DNS]     mta568.kth.gm.yahoo.co.jp
[Reverse DNS]     mta543.kth.gm.yahoo.co.jp


The enumeration has finished
Discoveries are being migrated into the local database
```


### ip option
```
amass_old enum -d yahoo.co.jp -ip -brute -src -json yahoo_src_brute_ip.json
[DNS]             ns12.yahoo.co.jp 124.83.159.228
[RapidDNS]        jvns11.yahoo.co.jp 124.83.159.219
[DNS]             mx3.mail.yahoo.co.jp 202.93.78.241,124.83.237.244,202.93.78.242,124.83.237.245
[RapidDNS]        ont211014008239.yahoo.co.jp 211.14.8.239
[RapidDNS]        ygn203141054163.yahoo.co.jp 203.141.54.163
[DNS]             mx5.mail.yahoo.co.jp 124.83.237.242,202.93.78.240,124.83.237.243,202.93.78.239
[RapidDNS]        gns06.yahoo.co.jp 118.151.254.152
[RapidDNS]        opc211014027081.yahoo.co.jp 211.14.27.81
[DNS]             ns02.yahoo.co.jp 118.151.254.149
[RapidDNS]        pinkribbon.yahoo.co.jp 182.22.64.64
[DNS]             mx1.mail.yahoo.co.jp 124.83.237.248,202.93.77.241,202.93.77.240,124.83.237.249
[RapidDNS]        opc211014027072.yahoo.co.jp 211.14.27.72
[DNS]             ns11.yahoo.co.jp 124.83.159.196
[DNS]             ns01.yahoo.co.jp 118.151.254.133
[RapidDNS]        monitor.yahoo.co.jp 210.81.152.121
[RapidDNS]        ont211014008238.yahoo.co.jp 211.14.8.238
[RapidDNS]        opc211014029234.yahoo.co.jp 211.14.29.234
[DNS]             mx2.mail.yahoo.co.jp 124.83.237.247,124.83.237.246,202.93.77.239,202.93.77.238
[AlienVault]      documentary.yahoo.co.jp 182.22.16.123
[RapidDNS]        jihanki.yahoo.co.jp 182.22.16.123
[RapidDNS]        iportal.yahoo.co.jp 182.22.16.123
[RapidDNS]        newsbiz.yahoo.co.jp 182.22.16.123
[AlienVault]      mycar.yahoo.co.jp 182.22.24.252
[RapidDNS]        ex.yahoo.co.jp 182.22.16.123
[RapidDNS]        coupons.yahoo.co.jp 182.22.16.123
[RapidDNS]        cast.yahoo.co.jp 182.22.16.123
[DNS]             carview.yahoo.co.jp 182.22.24.252
[RapidDNS]        dataforest.yahoo.co.jp 182.22.16.123
[AlienVault]      ipi.yahoo.co.jp 182.22.16.123
[Reverse DNS]     mta2006.mail.snz.ynwp.yahoo.co.jp 124.83.237.131
[Reverse DNS]     mta2084.mail.snz.ynwp.yahoo.co.jp 124.83.237.76
[RapidDNS]        compass-ymobile.yahoo.co.jp 182.22.16.123
[Reverse DNS]     ymobmtagw0008.mail.otm.ynwp.yahoo.co.jp 202.93.78.121
[RapidDNS]        quoterank.yahoo.co.jp 182.22.16.123
[Reverse DNS]     mta2123.mail.snz.ynwp.yahoo.co.jp 124.83.237.161
[Reverse DNS]     ybbmtaat2003.mail.snz.ynwp.yahoo.co.jp 124.83.237.37
[Reverse DNS]     mta0097.mail.otm.ynwp.yahoo.co.jp 202.93.78.20
[RapidDNS]        vegeta.yahoo.co.jp 182.22.16.123
[Reverse DNS]     mtagw2005.mail.vip.snz.ynwp.yahoo.co.jp 124.83.237.245
[Reverse DNS]     ymobmta0018.mail.otm.ynwp.yahoo.co.jp 202.93.78.127
[Reverse DNS]     ymobmtagw2008.mail.snz.ynwp.yahoo.co.jp 124.83.237.21
[Reverse DNS]     mtagw2007.mail.vip.snz.ynwp.yahoo.co.jp 124.83.237.243
[Reverse DNS]     ybbmta2009.mail.snz.ynwp.yahoo.co.jp 124.83.237.148
[Reverse DNS]     mta0107.mail.otm.ynwp.yahoo.co.jp 202.93.78.9
[RapidDNS]        ybbmx1.mail.yahoo.co.jp 124.83.237.241,124.83.237.240,202.93.78.238,202.93.77.237
[Reverse DNS]     zmtagw0002.mail.otm.ynwp.yahoo.co.jp 202.93.78.135
[Reverse DNS]     ont211014008250.yahoo.co.jp 211.14.8.250
[Reverse DNS]     mta2081.mail.snz.ynwp.yahoo.co.jp 124.83.237.49
[RapidDNS]        table.yahoo.co.jp 182.22.16.123
[Reverse DNS]     mta2002.mail.vip.snz.ynwp.yahoo.co.jp 124.83.237.235
[Reverse DNS]     mta0132.mail.otm.ynwp.yahoo.co.jp 202.93.78.68
[Reverse DNS]     mtagw0040.mail.otm.ynwp.yahoo.co.jp 202.93.78.124
[Reverse DNS]     mta0145.mail.otm.ynwp.yahoo.co.jp 202.93.78.64
[Reverse DNS]     mta0149.mail.otm.ynwp.yahoo.co.jp 202.93.78.80
[Brute Forcing]   video.yahoo.co.jp 202.239.2.248
[HackerTarget]    img247.auctions.yahoo.co.jp 183.79.210.121
^C
OWASP Amass v3.19.2                               https://github.com/OWASP/Amass
--------------------------------------------------------------------------------
419 names discovered - scrape: 51, api: 10, brute: 5, cert: 1, dns: 352
--------------------------------------------------------------------------------
ASN: 24572 - YAHOO-JP-AS-AP Yahoo Japan
        114.111.64.0/18         4    Subdomain Name(s)
        124.83.128.0/17         151  Subdomain Name(s)
        183.79.0.0/16           14   Subdomain Name(s)
ASN: 23816 - YAHOO Yahoo Japan Corporation
        202.93.64.0/19          184  Subdomain Name(s)
        118.151.224.0/19        9    Subdomain Name(s)
        182.22.0.0/17           44   Subdomain Name(s)
ASN: 55898 - YAHOO-CORP Yahoo Japan Corporation
        211.14.8.0/24           12   Subdomain Name(s)
        203.141.54.0/24         1    Subdomain Name(s)
        211.14.26.0/23          7    Subdomain Name(s)
        211.14.28.0/23          10   Subdomain Name(s)
ASN: 703 - UUNET - MCI Communications Services, Inc. d/b/a Verizon Business
        210.81.0.0/16           1    Subdomain Name(s)
ASN: 0 - Not routed
        202.239.0.0/20          2    Subdomain Name(s)

The enumeration has finished
Discoveries are being migrated into the local database
```

### exclude optionとinclude optionが共存できない!



### availableじゃないやつ
includeでもむりっぽ
[これ](https://www.hahwul.com/2020/09/23/amass-go-deep-in-the-sea-with-free-apis/)




v4で-includeは使える
-brute -activeも使える
v4で使えないのは -src -ip -json

