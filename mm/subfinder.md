# subfinder

[リンク](https://github.com/projectdiscovery/subfinder)


## 最強コマンド
```
subfinder -d yahoo.co.jp -all -recursive -active -ip -cs -json -o out.json
```

-ip: ipを結果に含める(-activeオプションが必要)
-o, -output :file to write output to
-oJ, -json :write output in JSONL(ines) format
-all: 利用可能なデータソースをすべて含める(slow)
-recursive: 見つかったサブドメインを新たなドメインとみなし、再帰的に調査する


他オプション
-s: 含めたいデータソースを指定
-ls: 利用可能なデータソースの一覧を表示
-up: アップデート

-cs: 使用したデータソースをすべて表示(json only)
違いは次のような感じ
-csなし
```
{"host":"staging-www.amiya.co.jp","input":"amiya.co.jp","source":"alienvault"}
```
-csあり
```
{"host":"staging-www.amiya.co.jp","input":"amiya.co.jp","sources":["hackertarget","alienvault","crtsh"]}
```
## 
調査手段はとくにオプションなしで出力可能。標準出力には出力されないが、jsonファイルなどにアウトプットすると含まれる。txtファイルでは含まれなかった。

実行時間
コマンド
``` time subfinder -d yahoo.co.jp -all -recursive -active -ip -json -o out.json```
結果
```
[INF] Found 821 subdomains for yahoo.co.jp in 8 minutes 9 seconds

real    8m13.274s
user    0m24.192s
sys     0m47.036s
```

recursiveの機能はほかのツールにあるのか？
また-allオプションが提供されているのはとても良い。
使用したデータソースを全部表示する-csもこれにしかないかな。


-recursiveをyahoo.co.jpに対して使ってみた
```
 wc -l recursive.txt
4518 recursive.txt
```
```
wc -l nonrecursive.txt
2259 nonrecursive.txt
```
確かに、結果は違いそう。ただ、nonrecursiveでもサブサブドメインまで調べられているっぽい。何が増えているのかはうーんといった感じ。



結果はfinal.jsonに入れといた。



