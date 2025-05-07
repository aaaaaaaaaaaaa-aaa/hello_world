# findomain

## usage
basic command
```
./findomain --ip -t yahoo.co.jp --pscan -u out.txt
```
-t: target


ほかのオプション
-o: ファイルに出力 (-oオプションのみつければよい。yahoo.co.jp.txtが生成される)
-u: 指定したファイルに出力 (-u test.txtなど)
--ip: ipアドレスを出力



## 特色

最後に実行時間が出てくる
```
Job finished in 163 seconds.

Good luck Hax0r 💀!


real    2m43.151s
user    0m1.029s
sys     0m0.861s
```
嘘はついてないっぽい


jsonアウトプットに対応してなさそう

Discover subdomains without brute-force, it tool uses Certificate Transparency Logs and APIs.
Discover only resolved subdomains.


--external-subdomains オプションを使うと、amass,subdomainを裏で動かして結果に追加するっぽい
10分たっても実行が終わらないのであきらめる
