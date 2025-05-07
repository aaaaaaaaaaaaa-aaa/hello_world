# aquatone

[リンク](https://github.com/michenriksen/aquatone?tab=readme-ov-file)

## usage
最強コマンド
```
cat subdomains.txt | aquatone -chrome-path "/mnt/c/Program Files/Google/Chrome/Application/chrome.exe" -out outdir -threads 10 -ports xlarge -save-body -http-timeout 10000 -scan-timeout 500 -screenshot-timeout 60000
 ```
 結果は-outで指定したoutdirというディレクトリに保存される
 オプションの順番は割とシビア
 
 サブドメインのホストのみを箇条書きにしたテキストファイルを与える。
 またはテキストファイルでなくても可。
 ```
  subfinder -d amiya.co.jp | aquatone -chrome-path /mnt/c/Program\ Files/Google/Chrome/Application/chrome.exe
  ```
subfinder -d amiya.co.jpはamiya.co.jpのサブドメインを列挙する
 
 
 また、jsonファイルを使う場合はjqでドメイン名だけを切り出す
 こういった結果の時(res_small.json)
 ```
{"host":"bid10.auctions.yahoo.co.jp","input":"yahoo.co.jp","source":"crtsh"}
{"host":"ev22.ciso.ssk.ynwm.yahoo.co.jp","input":"yahoo.co.jp","source":"crtsh"}
{"host":"omggw7021-vm11.mail.djm.yahoo.co.jp","input":"yahoo.co.jp","source":"hackertarget"}
```
これで切り出す
```
cat res_small.json | jq -r '.host' > subdomains.txt
```


### options
```
  -chrome-path string
    	Full path to the Chrome/Chromium executable to use. By default, aquatone will search for Chrome or Chromium
  -debug
    	Print debugging information
  -http-timeout int
    	Timeout in miliseconds for HTTP requests (default 3000)
  -nmap
    	Parse input as Nmap/Masscan XML
  -out string
    	Directory to write files to (default ".")
  -ports string
    	Ports to scan on hosts. Supported list aliases: small, medium, large, xlarge (default "80,443,8000,8080,8443")
  -proxy string
    	Proxy to use for HTTP requests
  -resolution string
    	screenshot resolution (default "1440,900")
  -save-body
    	Save response bodies to files (default true)
  -scan-timeout int
    	Timeout in miliseconds for port scans (default 100)
  -screenshot-timeout int
    	Timeout in miliseconds for screenshots (default 30000)
  -session string
    	Load Aquatone session file and generate HTML report
  -silent
    	Suppress all output except for errors
  -template-path string
    	Path to HTML template to use for report
  -threads int
    	Number of concurrent threads (default number of logical CPUs)
  -version
    	Print current Aquatone version
```



他オプション
Use **-nmap** when your data comes from Nmap or Masscan scans instead of Subfinder.
Use **-session** when you want to view past results without scanning again.
 
### Result
最強コマンドのオプションを使った結果。標準出力はこちら。(抜粋)
```
aquatone v1.7.0 started at 2025-03-31T12:52:42+09:00

Targets    : 50
Threads    : 10
Ports      : 80, 81, 300, 443, 591, 593, 832, 981, 1010, 1311, 2082, 2087, 2095, 2096, 2480, 3000, 3128, 3333, 4243, 4567, 4711, 4712, 4993, 5000, 5104, 5108, 5800, 6543, 7000, 7396, 7474, 8000, 8001, 8008, 8014, 8042, 8069, 8080, 8081, 8088, 8090, 8091, 8118, 8123, 8172, 8222, 8243, 8280, 8281, 8333, 8443, 8500, 8834, 8880, 8888, 8983, 9000, 9043, 9060, 9080, 9090, 9091, 9200, 9443, 9800, 9981, 12443, 16080, 18091, 18092, 20720, 28017
Output dir : outdir3

mycar.yahoo.co.jp: port 80 open
cn02.yahoo.co.jp: port 80 open
pr.mail.yahoo.co.jp: port 80 open
noticeymobilemail.yahoo.co.jp: port 80 open
forms.business.yahoo.co.jp: port 80 open
listing.yahoo.co.jp: port 80 open
http://cn02.yahoo.co.jp/: 404 Not Found on Accelerator
http://mycar.yahoo.co.jp/: 200 OK
http://forms.business.yahoo.co.jp/: 404 Not Found
http://noticeymobilemail.yahoo.co.jp/: 200 OK
http://mycar.yahoo.co.jp/: screenshot successful
insurance.yahoo.co.jp: port 443 open
mycar.yahoo.co.jp: port 443 open
http://forms.business.yahoo.co.jp/: screenshot successful
cn02.yahoo.co.jp: port 443 open
place.yahoo.co.jp: port 443 open
card.yahoo.co.jp: port 443 open
pr.mail.yahoo.co.jp: port 443 open
http://noticeymobilemail.yahoo.co.jp/: screenshot successful
forms.business.yahoo.co.jp: port 443 open
suica.yahoo.co.jp: port 443 open
listing.yahoo.co.jp: port 443 open
sports.yahoo.co.jp: port 443 open
https://insurance.yahoo.co.jp/: 200 OK
http://listing.yahoo.co.jp/: 200 OK
https://cn02.yahoo.co.jp/: 404 Not Found on Accelerator
https://place.yahoo.co.jp/: 404 Not Found on Accelerator
https://pr.mail.yahoo.co.jp/: 200 OK
https://forms.business.yahoo.co.jp/: 404 Not Found
https://listing.yahoo.co.jp/: 404 Not Found on Accelerator
https://sports.yahoo.co.jp/: 200 OK
https://insurance.yahoo.co.jp/: screenshot successful
http://listing.yahoo.co.jp/: screenshot successful
https://cn02.yahoo.co.jp/: screenshot successful
https://place.yahoo.co.jp/: screenshot successful
https://pr.mail.yahoo.co.jp/: screenshot successful
https://card.yahoo.co.jp/: 200 OK
https://forms.business.yahoo.co.jp/: screenshot successful
https://listing.yahoo.co.jp/: screenshot successful
https://suica.yahoo.co.jp/: 200 OK
https://sports.yahoo.co.jp/: screenshot successful
http://pr.mail.yahoo.co.jp/: request timeout
https://card.yahoo.co.jp/: screenshot successful
https://suica.yahoo.co.jp/: screenshot successful
https://mycar.yahoo.co.jp/: 200 OK
https://mycar.yahoo.co.jp/: screenshot successful
http://cn02.yahoo.co.jp/: screenshot timed out
Calculating page structures... done
Clustering similar pages... done
Generating HTML report... done

Writing session file...Time:
 - Started at  : 2025-03-31T12:52:42+09:00
 - Finished at : 2025-03-31T12:54:32+09:00
 - Duration    : 1m50s

Requests:
 - Successful : 15
 - Failed     : 1

 - 2xx : 9
 - 3xx : 0
 - 4xx : 6
 - 5xx : 0

Screenshots:
 - Successful : 14
 - Failed     : 1

Wrote HTML report to: outdir3/aquatone_report.html

``

 
### Output
- aquatone_report.html: An HTML report to open in a browser that displays all the collected screenshots and response headers clustered by similarity.
- aquatone_urls.txt: A file containing all responsive URLs. Useful for feeding into other tools.
- aquatone_session.json: A file containing statistics and page data. Useful for automation.
- html/: A folder with files containing the raw response bodies from processed targets. If you are processing a large amount of hosts, and don't need this for further analysis, you can disable this with the save-body=false flag to save some disk space.
- screenshots/: A folder with PNG screenshots of the processed targets

 
 
 ## 特徴
 google chromeを使うっぽい。
 どちらかというと可視化ツール
