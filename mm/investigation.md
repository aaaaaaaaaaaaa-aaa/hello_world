## investigation_operator_strict

### 項目
#### 必須情報
- IPとFQDN
- 調べた元のドメイン
- サブドメインを見つけた手段
#### オプション
できるだけ多くの情報を得るために使うオプション
#### 各ツールの特色
そのツールでできること
そのツールでしかできないこと
実行コマンドとアウトプットをメモ
#### 各種ツールのアウトプットの統合
jsonだと良き

=
=
### tools
- amass
- subfinder
- assetfinder
- findomain
- aquatone
- naabu
- dirsearch



- dnsmap
- fierce
- subbrute
- puredns
- sublist3r

dnsmap sublist3rは探してきた数が少ない



### 実行時間比較
とりあえず、各ツールの最強コマンドを同じドメインに対して使用。対象はgoogle.com
出力結果はsuper_result

#### amass
コマンド
```
 time amass_old enum -d google.com -active -brute -src -ip -json super_result.json -include arin,
abuseipdb, alientvault, alterations, anubisdb, archiveit, arquivo, ask, askdns, bgptools, bgpview, baidu, bing, brute forcing, bu
fferover, censys, certspotter, cloudflare, commoncrawl, crtsh, dnsdumpster, digitorus, duckduckgo, fullhunt, gists, googlect, gre
ynoise, haw, hackerone, hackertarget, hyperstat, ipv4info, maltiverse, mnemonic, n45ht, networksdb, pkey, radb, rapiddns, riddler
, robtex, searchcode, searx, shadowserver, sitedossier, sonarsearch, spyonweb, sublist3rapi, teamcymru, threatcrowd, threatminer,
 ukwebarchive, urlscan, wayback, yahoo
```

#### subfinder




### 僕的tier表

#### S
- amass
- subfinder
#### A
- findomain
#### B
- assetfind

#### others
- aquatone
- naabu
- dirsearch


### 調べること
- [ ] amassはrecursiveできるのか。defaultでやっているのか->サブサブくらいまで見えるので、やってると思いたい。
別プロセスで同時に動かせるか。amassとamassなど。amassは二つ同時に動かせないっぽ

- [ ] ~~公開情報から情報を得たいならamassの-activeはダメなんじゃないか説~~ -> スキャンはいいっぽい。

- [ ] subdomain比較
- [ ] data source表(readmeにあるリストとか)

やること
- 実行時間の比較
- 出てくる結果の比較
- ぬけるやつはなにか



### 実行時間と結果
#### amass
1. 10m51.189s
2. 10m56.755s
3. 11m4.516s


#### subfinder
1. 37.837s
2. 48.403s
3. 15.896s
4. 12.926s
5. 10.187s
6. 35s

sourceでの揺れあり。
host,ip同じでもsourceが違うとか


#### findomain
1. 2m2s
2. 1m47s
3. 1m52s

揺れなし
#### assetfinder
1. 2.496s
2. 1.560s
3. 1.517s
4. 1.635s
5. 1.545s

同一の実行で重複あり
揺れなし


### 結果
---
### 🔍 Unique Subdomains Found (By Tool)

| Subdomain                      | Amass | Subfinder | Findomain | Assetfinder |
|-------------------------------|:-----:|:---------:|:---------:|:-----------:|
| amiya.co.jp                   | ✅    | ❌        | ✅        | ✅          |
| autodiscover.amiya.co.jp      | ✅    | ❌        | ❌        | ❌          |
| doc.amiya.co.jp               | ✅    | ✅        | ✅        | ✅          |
| mail1.amiya.co.jp             | ✅    | ✅        | ❌        | ✅          |
| ns.amiya.co.jp                | ✅    | ✅        | ✅        | ✅          |
| ns2.amiya.co.jp               | ✅    | ✅        | ❌        | ✅          |
| ns3.amiya.co.jp               | ✅    | ❌        | ❌        | ❌          |
| partner.amiya.co.jp           | ✅    | ❌        | ❌        | ❌          |
| product.amiya.co.jp           | ✅    | ✅        | ✅        | ✅          |
| smtpaws.amiya.co.jp           | ✅    | ✅        | ❌        | ✅          |
| smtpaws01.amiya.co.jp         | ✅    | ✅        | ❌        | ✅          |
| smtpaws03.amiya.co.jp         | ✅    | ✅        | ❌        | ✅          |
| staging-www.amiya.co.jp       | ✅    | ✅        | ✅        | ✅          |
| support-qa.amiya.co.jp        | ✅    | ✅        | ❌        | ✅          |
| support.amiya.co.jp           | ✅    | ✅        | ✅        | ✅          |
| tsubuyaki.amiya.co.jp         | ✅    | ✅        | ✅        | ✅          |
| www.amiya.co.jp               | ✅    | ✅        | ✅        | ✅          |
| wwwsc.amiya.co.jp             | ✅    | ✅        | ✅        | ✅          |
| support-test.amiya.co.jp      | ❌    | ❌        | ❌        | ✅          |
| test.furuno.amiya.co.jp       | ❌    | ❌        | ❌        | ✅          |
| corporatesiteproduction.kinsta.cloud | ❌ | ❌ | ❌ | ✅ |
| alogtest.app                  | ❌    | ❌        | ❌        | ✅          |
| satr.jp                       | ❌    | ❌        | ❌        | ✅          |

