# Amass



## ツールと環境
使用ツール: Amass v.3.19.2
実行環境: WSLのUbuntu 22.04.05 LTS
プロセッサ: Intel(R) Core(TM) i5-10210U CPU @ 1.60GHz   2.11 GHz
RAM: 8.00GB


## 使い方

### 基本的な使い方
```
amass enum -d amiya.co.jp
```
`enum`:列挙モード
`-d`: 調べるドメインを指定


標準出力はこんな感じ
```
ns2.amiya.co.jp
doc.amiya.co.jp
www.amiya.co.jp
staging-www.amiya.co.jp
amiya.co.jp
smtpaws01.amiya.co.jp
support-qa.amiya.co.jp
smtpaws03.amiya.co.jp
support.amiya.co.jp
product.amiya.co.jp
wwwsc.amiya.co.jp
tsubuyaki.amiya.co.jp
smtpaws.amiya.co.jp
ns3.amiya.co.jp
mail1.amiya.co.jp
ns.amiya.co.jp
partner.amiya.co.jp
autodiscover.amiya.co.jp

OWASP Amass v3.19.2                               https://github.com/OWASP/Amass
--------------------------------------------------------------------------------
18 names discovered - api: 14, dns: 1, brute: 3
--------------------------------------------------------------------------------
ASN: 7682 - HOTNET HOKKAIDO TELECOMMUNICATIONS NETWORK Co., Inc.
        211.128.64.0/19         1    Subdomain Name(s)
ASN: 13335 - CLOUDFLARENET - Cloudflare, Inc.
        162.159.128.0/17        4    Subdomain Name(s)
ASN: 16509 - AMAZON-02 - Amazon.com, Inc.
        54.238.0.0/16           1    Subdomain Name(s)
        18.180.0.0/15           2    Subdomain Name(s)
        3.112.0.0/14            6    Subdomain Name(s)
ASN: 4713 - OCN NTT Communications Corporation, JP
        218.44.0.0/16           3    Subdomain Name(s)
ASN: 8075 - MICROSOFT-CORP-MSN-AS-BLOCK - Microsoft Corporation
        2603:1000::/26          4    Subdomain Name(s)

The enumeration has finished
Discoveries are being migrated into the local database
```

### jsonファイルに結果を出力する
`json`オプションをつけることで、jsonファイルへの出力が可能。ただし、amassはバージョン3のものを使う必要がある
```
amass_old enum -d amiya.co.jp -json out.json
```

結果のjsonファイルの一部をは以下に示す
```json
{"name":"ns2.amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"211.128.79.157","cidr":"211.128.64.0/19","asn":7682,"desc":"HOTNET HOKKAIDO TELECOMMUNICATIONS NETWORK Co., Inc."}],"tag":"api","sources":["HackerTarget"]}
{"name":"doc.amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"162.159.135.42","cidr":"162.159.128.0/19","asn":13335,"desc":"CLOUDFLARENET - Cloudflare, Inc."}],"tag":"api","sources":["HackerTarget"]}
{"name":"smtpaws01.amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"54.238.66.138","cidr":"54.238.0.0/16","asn":16509,"desc":"AMAZON-02 - Amazon.com, Inc."}],"tag":"api","sources":["HackerTarget"]}
{"name":"www.amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"162.159.135.42","cidr":"162.159.128.0/19","asn":13335,"desc":"CLOUDFLARENET - Cloudflare, Inc."}],"tag":"scrape","sources":["HackerTarget","Yahoo","AlienVault"]}
{"name":"amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"162.159.135.42","cidr":"162.159.128.0/19","asn":13335,"desc":"CLOUDFLARENET - Cloudflare, Inc."}],"tag":"archive","sources":["DNS","SiteDossier","DuckDuckGo","Bing","HackerTarget","Searchcode","RapidDNS","AlienVault","HAW","Yahoo","HyperStat"]}
{"name":"staging-www.amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"162.159.135.42","cidr":"162.159.128.0/19","asn":13335,"desc":"CLOUDFLARENET - Cloudflare, Inc."}],"tag":"api","sources":["HackerTarget"]}
```

### IPアドレス,データソースを結果に含める
- `ip`: 見つけたドメインのIPアドレスを表示する
- `src`: データソースを表示

```
amass enum -d amiya.co.jp -ip -src -json out2.json
```

標準出力が次のようになる
```
[HackerTarget]    ns2.amiya.co.jp 211.128.79.157
[AlienVault]      doc.amiya.co.jp 162.159.135.42
[AlienVault]      www.amiya.co.jp 162.159.135.42
[DNS]             amiya.co.jp 162.159.135.42
[AlienVault]      staging-www.amiya.co.jp 162.159.135.42
[HackerTarget]    smtpaws01.amiya.co.jp 54.238.66.138
[HackerTarget]    smtpaws.amiya.co.jp 3.112.160.16
[AlienVault]      wwwsc.amiya.co.jp 3.115.195.230
[HackerTarget]    tsubuyaki.amiya.co.jp 3.115.195.230
[HackerTarget]    support.amiya.co.jp 3.115.195.230
[AlienVault]      product.amiya.co.jp 3.115.195.230
[Brute Forcing]   partner.amiya.co.jp 3.115.195.230
[HackerTarget]    smtpaws03.amiya.co.jp 18.181.121.91
[HackerTarget]    support-qa.amiya.co.jp 18.180.176.143
[HackerTarget]    mail1.amiya.co.jp 218.44.242.102
[Brute Forcing]   ns3.amiya.co.jp 218.44.242.102
[AlienVault]      ns.amiya.co.jp 218.44.242.98
[Brute Forcing]   autodiscover.amiya.co.jp 2603:1036:302:4028::8,2603:1036:303:2820::8,2603:1036:303:303c::8,2603:1036:302:880::8

OWASP Amass v3.19.2                               https://github.com/OWASP/Amass
--------------------------------------------------------------------------------
18 names discovered - api: 8, scrape: 2, dns: 1, cert: 4, brute: 3
--------------------------------------------------------------------------------
ASN: 4713 - OCN NTT Communications Corporation, JP
        218.44.0.0/16           3    Subdomain Name(s)
ASN: 8075 - MICROSOFT-CORP-MSN-AS-BLOCK - Microsoft Corporation
        2603:1000::/26          4    Subdomain Name(s)
ASN: 7682 - HOTNET HOKKAIDO TELECOMMUNICATIONS NETWORK Co., Inc.
        211.128.64.0/19         1    Subdomain Name(s)
ASN: 13335 - CLOUDFLARENET - Cloudflare, Inc.
        162.159.128.0/19        4    Subdomain Name(s)
ASN: 16509 - AMAZON-02 - Amazon.com, Inc.
        3.112.0.0/14            6    Subdomain Name(s)
        18.180.0.0/15           2    Subdomain Name(s)
        54.238.0.0/16           1    Subdomain Name(s)

The enumeration has finished
Discoveries are being migrated into the local database
```
jsonファイルは次のような感じ(一部)
```json
{"name":"ns2.amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"211.128.79.157","cidr":"211.128.64.0/19","asn":7682,"desc":"HOTNET HOKKAIDO TELECOMMUNICATIONS NETWORK Co., Inc."}],"tag":"api","sources":["HackerTarget"]}
{"name":"doc.amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"162.159.135.42","cidr":"162.159.128.0/19","asn":13335,"desc":"CLOUDFLARENET - Cloudflare, Inc."}],"tag":"api","sources":["AlienVault","HackerTarget","RapidDNS"]}
{"name":"www.amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"162.159.135.42","cidr":"162.159.128.0/19","asn":13335,"desc":"CLOUDFLARENET - Cloudflare, Inc."}],"tag":"scrape","sources":["AlienVault","RapidDNS","Bing","Baidu"]}
{"name":"amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"162.159.135.42","cidr":"162.159.128.0/19","asn":13335,"desc":"CLOUDFLARENET - Cloudflare, Inc."}],"tag":"dns","sources":["DNS","HackerTarget","Bing","SiteDossier","DuckDuckGo","Baidu","Yahoo","Mnemonic","AlienVault","HAW","RapidDNS","HyperStat","Searchcode"]}
{"name":"staging-www.amiya.co.jp","domain":"amiya.co.jp","addresses":[{"ip":"162.159.135.42","cidr":"162.159.128.0/19","asn":13335,"desc":"CLOUDFLARENET - Cloudflare, Inc."}],"tag":"scrape","sources":["AlienVault","HackerTarget","Yahoo"]}
```
jsonの内容については、`ip`や`src`オプションをつける前と変わっていないようにも見える。








### アクティブ列挙

amassのenumモードはさらに下のような三つのモードがある
- Normal
- Passive
- Active

Normal: デフォルトの動作。外部のデータソースを参照しつつ、DNSクエリを投げて結果を検証する。バランスの取れたスキャンをしたいときに最適
Passive: 完全に外部データソースのみを使用する。見つかった情報をそのまま使い、DNSの照会などを行わない。ステルス性を重視したいときに最適
Active: Normalモードのすべての処理に加え、発見したホストに対してのTLS証明書の取得、DNSゾーン転送の試行、NSECウォーキング、Webクロールなどのよりつっこんだ調査を行う。最大限の情報収集を行いたいときに最適。

より多くの結果を得たい場合にはアクティブ列挙をするといいかもしれない。

アクティブ列挙は`active`オプションをつける。

```
amass　enum -d amiya.co.jp -active -ip -src -json out3.json
```

標準出力
```
[HackerTarget]    www.amiya.co.jp 162.159.135.42
[HackerTarget]    smtpaws01.amiya.co.jp 54.238.66.138
[DNS]             amiya.co.jp 162.159.135.42
[AlienVault]      staging-www.amiya.co.jp 162.159.135.42
[AlienVault]      doc.amiya.co.jp 162.159.135.42
[HackerTarget]    ns2.amiya.co.jp 211.128.79.157
[AlienVault]      wwwsc.amiya.co.jp 3.115.195.230
[AlienVault]      support.amiya.co.jp 3.115.195.230
[HackerTarget]    smtpaws.amiya.co.jp 3.112.160.16
[AlienVault]      tsubuyaki.amiya.co.jp 3.115.195.230
[AlienVault]      product.amiya.co.jp 3.115.195.230
[HackerTarget]    support-qa.amiya.co.jp 18.180.176.143
[HackerTarget]    smtpaws03.amiya.co.jp 18.181.121.91
[HackerTarget]    mail1.amiya.co.jp 218.44.242.102
[AlienVault]      ns.amiya.co.jp 218.44.242.98
[Brute Forcing]   ns3.amiya.co.jp 218.44.242.102
[Brute Forcing]   partner.amiya.co.jp 3.115.195.230
[Brute Forcing]   autodiscover.amiya.co.jp 52.96.3.136

OWASP Amass v3.19.2                               https://github.com/OWASP/Amass
--------------------------------------------------------------------------------
18 names discovered - scrape: 4, archive: 1, api: 10, brute: 2, crawl: 1
--------------------------------------------------------------------------------
ASN: 16509 - AMAZON-02 - Amazon.com, Inc.
        54.238.0.0/16           1    Subdomain Name(s)
        3.112.0.0/14            6    Subdomain Name(s)
        18.180.0.0/15           2    Subdomain Name(s)
ASN: 7682 - HOTNET HOKKAIDO TELECOMMUNICATIONS NETWORK Co., Inc.
        211.128.64.0/19         1    Subdomain Name(s)
ASN: 4713 - AS4713 - NTT Communications Corporation
        218.44.0.0/16           3    Subdomain Name(s)
ASN: 8075 - MICROSOFT-CORP-MSN-AS-BLOCK - Microsoft Corporation
        52.96.0.0/19            1    Subdomain Name(s)
ASN: 13335 - CLOUDFLARENET - Cloudflare, Inc.
        162.159.128.0/19        4    Subdomain Name(s)

The enumeration has finished
Discoveries are being migrated into the local database
```

### brute
```
amass_old enum -d amiya.co.jp -brute -ip -src -json out4.json
```
`brute`オプションでサブドメインの列挙に総当たりを使うことができる

標準出力
```
[Brute Forcing]   ns2.amiya.co.jp 211.128.79.157
[HackerTarget]    doc.amiya.co.jp 162.159.135.42
[DNS]             amiya.co.jp 162.159.135.42
[HackerTarget]    www.amiya.co.jp 162.159.135.42
[HackerTarget]    smtpaws01.amiya.co.jp 54.238.66.138
[HackerTarget]    mail1.amiya.co.jp 218.44.242.102
[Brute Forcing]   ns.amiya.co.jp 218.44.242.98
[HackerTarget]    staging-www.amiya.co.jp 162.159.135.42
[HackerTarget]    support-qa.amiya.co.jp 18.180.176.143
[HackerTarget]    smtpaws03.amiya.co.jp 18.181.121.91
[HackerTarget]    wwwsc.amiya.co.jp 3.115.195.230
[HackerTarget]    tsubuyaki.amiya.co.jp 3.115.195.230
[Brute Forcing]   ns3.amiya.co.jp 218.44.242.102
[Brute Forcing]   partner.amiya.co.jp 3.115.195.230
[Brute Forcing]   support.amiya.co.jp 3.115.195.230
[HackerTarget]    product.amiya.co.jp 3.115.195.230
[HackerTarget]    smtpaws.amiya.co.jp 3.112.160.16
[Brute Forcing]   autodiscover.amiya.co.jp 2603:1036:307:486a::8,2603:1036:307:294b::8,2603:1036:307:4000::8,2603:1036:307:2854::8

OWASP Amass v3.19.2                               https://github.com/OWASP/Amass
--------------------------------------------------------------------------------
18 names discovered - api: 7, dns: 1, scrape: 3, cert: 2, brute: 5
--------------------------------------------------------------------------------
ASN: 7682 - HOTNET HOKKAIDO TELECOMMUNICATIONS NETWORK Co., Inc.
        211.128.64.0/19         1    Subdomain Name(s)
ASN: 13335 - CLOUDFLARENET - Cloudflare, Inc.
        162.158.0.0/15          4    Subdomain Name(s)
ASN: 16509 - AMAZON-02 - Amazon.com, Inc.
        54.238.0.0/16           1    Subdomain Name(s)
        18.180.0.0/15           2    Subdomain Name(s)
        3.112.0.0/14            6    Subdomain Name(s)
ASN: 4713 - AS4713 - NTT Communications Corporation
        218.44.0.0/16           3    Subdomain Name(s)
ASN: 8075 - MICROSOFT-CORP-MSN-AS-BLOCK - Microsoft Corporation
        2603:1000::/26          4    Subdomain Name(s)

The enumeration has finished
Discoveries are being migrated into the local database
```
何が変わったのかはよくわからないが、付けられるならつけておくといった感じである。
`active`や`brute`をつけた時は列挙が終わってからプログラムが終了するまでの時間がかかっていない印象を受ける。Ctrl+Cで終了しなくてもすぐ終わってくれる。

### 使用するデータソースを指定する
`include`オプションを使うと使うデータソースを指定できる。
コマンド例
```
amass enum -include crtsh -d example.com
```
ここではcrtshをデータソースとして指定している。

また、利用可能なデータソースは`list`オプションで確認できる
```
amass enum -list
```
結果は次のような感じになる
```
Data Source               | Type                    | Available
--------------------------------------------------------------------------------
360PassiveDNS               api
ARIN                        api                         *
AbuseIPDB                   scrape                      *
Ahrefs                      api
AlienVault                  api                         *
Alterations                 alt                         *
AnubisDB                    api                         *
ArchiveIt                   archive                     *
Arquivo                     archive                     *
Ask                         scrape                      *
AskDNS                      scrape                      *
BGPTools                    misc                        *
BGPView                     api                         *
Baidu                       scrape                      *
BinaryEdge                  api
Bing                        scrape                      *
Brute Forcing               brute                       *
BufferOver                  api                         *
BuiltWith                   api
C99                         api
CIRCL                       api
Censys                      cert                        *
CertSpotter                 cert                        *
Chaos                       api
Cloudflare                  api                         *
CommonCrawl                 crawl                       *
Crtsh                       cert                        *
DNSDB                       api
DNSDumpster                 scrape                      *
DNSRepo                     api
DNSlytics                   api
Detectify                   api
Digitorus                   cert                        *
DuckDuckGo                  scrape                      *
FOFA                        scrape
FacebookCT                  cert
FullHunt                    api                         *
Gists                       scrape                      *
GitHub                      api
GitLab                      api
GoogleCT                    cert                        *
Greynoise                   api                         *
HAW                         archive                     *
HackerOne                   scrape                      *
HackerTarget                api                         *
Hunter                      api
HyperStat                   scrape                      *
IPdata                      api
IPinfo                      api
IPv4Info                    scrape                      *
IntelX                      api
LeakIX                      api
Maltiverse                  api                         *
Mnemonic                    api                         *
N45HT                       api                         *
NetworksDB                  scrape                      *
ONYPHE                      api
PKey                        scrape                      *
PassiveTotal                api
PentestTools                api
Quake                       api
RADb                        api                         *
RapidDNS                    scrape                      *
Riddler                     scrape                      *
Robtex                      api                         *
Searchcode                  scrape                      *
Searx                       scrape                      *
SecurityTrails              api
ShadowServer                misc                        *
Shodan                      api
SiteDossier                 scrape                      *
SonarSearch                 api                         *
Spamhaus                    api
SpyOnWeb                    scrape                      *
Spyse                       api
Sublist3rAPI                api                         *
TeamCymru                   misc                        *
ThreatBook                  api
ThreatCrowd                 api                         *
ThreatMiner                 api                         *
Twitter                     api
UKWebArchive                archive                     *
URLScan                     api                         *
Umbrella                    api
VirusTotal                  api
Wayback                     archive                     *
WhoisXMLAPI                 api
Yahoo                       scrape                      *
ZETAlytics                  api
ZoomEye                     api
```





## 僕の考えた最強コマンド
```
 amass enum -d amiya.co.jp -active -brute -src -ip -json aeiueoao.json \
 -include arin, abuseipdb, alientvault, alterations, anubisdb, archiveit, arquivo, ask,\
 askdns, bgptools, bgpview, baidu, bing, brute forcing, bufferover , censys, certspotter,\
 cloudflare, commoncrawl, crtsh, dnsdumpster, digitorus, duckduckgo, fullhunt, gists,\
 googlect, greynoise, haw, hackerone, hackertarget, hyperstat, ipv4info, maltiverse,\
 mnemonic, n45ht, networksdb, pkey, radb, rapiddns, riddler, robtex, searchcode, searx,\
 shadowserver, sitedossier, sonarsearch, spyonweb, sublist3rapi, teamcymru, threatcrowd,\
 threatminer, ukwebarchive, urlscan, wayback, yahoo
```
- `-d`:ドメイン名の指定
- `-active`: アクティブな調査を有効にする (e.g., DNS resolution, probing)
- `-brute`:	サブドメインの列挙にブルートフォースを使う
- `-src`: データソースの表示をする
- `-ip`: サブドメインのIPアドレスを表示する
- `-json`: jsonファイルに結果を出力する
- `-include`: 使うデータソースの指定でいっぱい指定する



## 公式サイトのリンク

[リポジトリリンク](https://github.com/owasp-amass/amass)
[ユーザガイド](https://github.com/owasp-amass/amass/blob/master/doc/user_guide.md)
