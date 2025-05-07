# assetfinder

[リンク](https://github.com/tomnomnom/assetfinder)

## 雑魚

コマンド
```
 ./assetfinder --subs-only yahoo.co.jp > out_subsonly.txt
```
--subs-onlyをつけないと、サブドメイン以外のものも取ってくるっぽい
```
./assetfinder yahoo.co.jp > out.txt
```
ファイルに書き出すオプションがないっぽいので、リダイレクトでテキストファイルに書き出す。
```
$ cat out.txt |grep -v "yahoo" (抜粋)
www.fnn.jp
37.gigafile.nu
caishuo.lol
www.store-express.com
newsdig.tbs.co.jp
vblzc.cn
click.dm.aoki-style.com
ln.run
qepem.cn
dutgu.cn
www.sateraito.jp
rakutensec16.com
shunmang.lol
gongmang.lol
rongmang.lol
mangchua.lol
chongmang.lol
taomang.lol
yangmang.lol
zhongmang.lol
fenmang.lol
mangshang.lol
manghuang.lol
mangbin.lol
ninmang.lol
mangjiang.lol
cuimang.lol
mangyang.lol
```


### 特色
機能が少なすぎる。ただし速い。すごく速い。

```
# cat out.txt|tail -n 15
remodel.auctions.yahoo.co.jp
beta.order.shopping.yahoo.co.jp
tool.bylines.news.yahoo.co.jp
b92.yahoo.co.jp
dailyplus.yahoo.co.jp
achart.yahoo.co.jp
rmc.grmtrez.yahoo.co.jp
jp.mg3.mail.yahoo.co.jp
myorder.ec.yahoo.co.jp
secure.loco.yahoo.co.jp
sales.ec.yahoo.co.jp
tool.safety.yahoo.co.jp
tool.safety.yahoo.co.jp_2012
asia_ad2007@yahoo.co.jp
order.ec.yahoo.co.jp
```

サブサブドメインとかも調べられる。
ただし、データソース,IP,データ出力などに対応していないっぽい
