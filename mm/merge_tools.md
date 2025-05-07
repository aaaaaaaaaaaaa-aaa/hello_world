## merge tools

### tools
- amass
- subfinder
- findomain
- assetfinder


## implementation
- lang: Python
- framework: None
- environment: WSL2



## output for now
```json
{"domain": "amiya.co.jp", "name": "mail1.amiya.co.jp", "addresses": [{"ip": "218.44.242.102"}], "sources": ["hackertarget", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "product.amiya.co.jp", "addresses": [{"ip": "3.115.195.230"}], "sources": ["alienvault", "findomain", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "support-qa.amiya.co.jp", "addresses": [{"ip": "18.180.176.143"}], "sources": ["hackertarget", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "doc.amiya.co.jp", "addresses": [{"ip": "162.159.135.42"}], "sources": ["alienvault", "findomain", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "smtpaws.amiya.co.jp", "addresses": [{"ip": "3.112.160.16"}], "sources": ["hackertarget", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "ns2.amiya.co.jp", "addresses": [{"ip": "211.128.79.157"}], "sources": ["hackertarget", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "staging-www.amiya.co.jp", "addresses": [{"ip": "162.159.135.42"}], "sources": ["alienvault", "findomain", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "ns.amiya.co.jp", "addresses": [{"ip": "218.44.242.98"}], "sources": ["alienvault", "findomain", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "smtpaws03.amiya.co.jp", "addresses": [{"ip": "18.181.121.91"}], "sources": ["hackertarget", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "smtpaws01.amiya.co.jp", "addresses": [{"ip": "54.238.66.138"}], "sources": ["hackertarget", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "www.amiya.co.jp", "addresses": [{"ip": "162.159.135.42"}], "sources": ["alienvault", "findomain", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "wwwsc.amiya.co.jp", "addresses": [{"ip": "3.115.195.230"}], "sources": ["alienvault", "findomain", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "tsubuyaki.amiya.co.jp", "addresses": [{"ip": "3.115.195.230"}], "sources": ["alienvault", "findomain", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "support.amiya.co.jp", "addresses": [{"ip": "3.115.195.230"}], "sources": ["findomain", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "amiya.co.jp", "addresses": [{"ip": "162.159.135.42"}], "sources": ["findomain", "assetfinder"]}
{"domain": "amiya.co.jp", "name": "test.furuno.amiya.co.jp", "addresses": [], "sources": ["assetfinder"]}
{"domain": "amiya.co.jp", "name": "support-test.amiya.co.jp", "addresses": [], "sources": ["assetfinder"]}
{"domain": "amiya.co.jp", "name": "corporatesiteproduction.kinsta.cloud", "addresses": [], "sources": ["assetfinder"]}
{"domain": "amiya.co.jp", "name": "alogtest.app", "addresses": [], "sources": ["assetfinder"]}
{"domain": "amiya.co.jp", "name": "satr.jp", "addresses": [], "sources": ["assetfinder"]}

```


- domain: original domain
- name: found subdomains
- ip: ip addrs for subdomain
- sources: used data source or tools


findomain and assetfinder don't have feature to include data sources in their result, so I'll include the tool's name itself instead.




##  time vs quality

## 目標？
何が目標か。期待するアウトプットは
使うツールにはこだわるか
プラットフォームは何か win,lin
ポートスキャンは空いてるポートがわかるだけでいいのか
並列処理のしかた。amassを同時に動かそうとするのか
ポートの情報は別ファイルでいいか=>よい



### 今のコマンドでopen portのみを調べる
#### 少ないips
10.255.255.1
3.115.195.230
162.159.135.42
218.44.242.98
218.44.242.102
----- 266.48431634902954 seconds ---

#### 多いips
211.128.79.157
218.44.242.102
10.255.255.1
10.255.253.6
10.255.253.5
18.180.176.143
218.44.242.98
54.199.231.181
18.180.255.20
3.115.195.230
54.238.66.138
35.76.191.139
18.176.32.243
162.159.135.42
18.181.121.91
3.112.160.16
10.224.255.2
----- 266.7598216533661 seconds ---

変わらねぇ


retry 1
Execution time: 0:06:50.018267

retry 3
Execution time: 0:27:06.532917

実行時間は三倍以上になっているが、ほとんどamassのせいである



## 展望
naabuで一つのipアドレスのポートを調べるのに、5~10分くらいかかってしまう。
amiya.co.jpでもサブドメインのipアドレスは20個くらいあるため、時間がかかりすぎてしまう。

naabuは並列化機能がついているので、それで何とかなる。




良いですね
・ドメインが増えるほど一次関数的に調査時間が増えるのであれば、パイプライン処理にして回避できそうですがどうでしょう(個人的なナレッジですがnmap等の場合は20IP程度なら並列処理で調査時間が増えることなないです。)





### amiya.co.jpの結果
run_num:3
Execution time: 27分43秒72
OUTPUT=>output_amiya_co_jp_20250507110019

run_num:1
Execution time: 12分43秒92
OUTPUT=>output_amiya_co_jp_20250507113009