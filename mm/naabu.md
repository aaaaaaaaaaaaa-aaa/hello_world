# naabu

## usage
```
 naabu -host yahoo.co.jp -json -o out.json -rate 2000 -c 50 -retries 5 -timeout 2s -display-cdn -verbose -debug  -scan-all-ips -scan-type c

```

```

                  __
  ___  ___  ___ _/ /  __ __
 / _ \/ _ \/ _ \/ _ \/ // /
/_//_/\_,_/\_,_/_.__/\_,_/

                projectdiscovery.io

[WRN] host discovery requires syn scan, automatically switching to syn scan
[INF] Running host discovery scan
[DBG] Received ICMP response from 182.22.24.252
[DBG] Received ICMP response from 182.22.16.123
[DBG] Received ICMP response from 182.22.25.124
[DBG] Received ICMP response from 182.22.16.251
[DBG] Received ICMP response from 182.22.24.124
[DBG] Received ICMP response from 182.22.24.124
[DBG] Received ICMP response from 182.22.31.124
[DBG] Received ICMP response from 182.22.28.252
[DBG] Received ICMP response from 182.22.16.123
[DBG] Received ICMP response from 182.22.31.124
[DBG] Received ICMP response from 182.22.24.252
[DBG] Received ICMP response from 182.22.16.251
[DBG] Received ICMP response from 182.22.16.123
[DBG] Received ICMP response from 182.22.16.251
[DBG] Received ICMP response from 182.22.24.252
[DBG] Received ICMP response from 182.22.24.124
[DBG] Received ICMP response from 182.22.25.252
[DBG] Received ICMP response from 182.22.31.252
[DBG] Received ICMP response from 182.22.28.252
[DBG] Received ICMP response from 182.22.28.252
[DBG] Received ICMP response from 182.22.25.124
[DBG] Received ICMP response from 182.22.31.124
[DBG] Received ICMP response from 182.22.25.124
[DBG] Received ICMP response from 182.22.31.252
[DBG] Received ICMP response from 182.22.31.252
[DBG] Received ICMP response from 182.22.25.252
[DBG] Received ICMP response from 182.22.25.252
[DBG] Received ICMP response from 124.83.185.124
[DBG] Received ICMP response from 124.83.185.124
[DBG] Received ICMP response from 183.79.219.124
[DBG] Received ICMP response from 124.83.185.252
[DBG] Received ICMP response from 124.83.184.252
[DBG] Received ICMP response from 124.83.184.124
[DBG] Received ICMP response from 124.83.185.252
[DBG] Received ICMP response from 183.79.219.252
[DBG] Received ICMP response from 183.79.219.124
[DBG] Received ICMP response from 124.83.184.124
[DBG] Received ICMP response from 124.83.185.252
[DBG] Received ICMP response from 124.83.185.124
[DBG] Received ICMP response from 183.79.250.251
[DBG] Received ICMP response from 183.79.219.252
[DBG] Received ICMP response from 183.79.249.252
[DBG] Received ICMP response from 183.79.219.252
[DBG] Received ICMP response from 124.83.184.252
[DBG] Received ICMP response from 124.83.184.124
[DBG] Received ICMP response from 183.79.249.124
[DBG] Received ICMP response from 183.79.249.124
[DBG] Received ICMP response from 183.79.250.251
[DBG] Received ICMP response from 183.79.249.252
[DBG] Received ICMP response from 183.79.250.251
[DBG] Received ICMP response from 183.79.249.252
[DBG] Received ICMP response from 183.79.219.124
[DBG] Received ICMP response from 183.79.249.124
[INF] Running SYN scan with CAP_NET_RAW privileges
{"host":"yahoo.co.jp","ip":"182.22.31.124","timestamp":"2025-03-31T04:39:19.120805561Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.31.124 ipv6:5d3a:918c:800:4500:28:4800:4000:3e06 port:2000
{"host":"yahoo.co.jp","ip":"182.22.16.251","timestamp":"2025-03-31T04:39:19.127412259Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.16.251 ipv6:5d3a:918c:800:4500:28:4800:4000:3e06 port:2000
{"host":"yahoo.co.jp","ip":"124.83.184.252","timestamp":"2025-03-31T04:39:19.133607557Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.184.252 ipv6:5d3a:918c:800:4500:2c:4c76:0:3e06 port:5060
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-03-31T04:39:19.138951056Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.24.252 ipv6:5d3a:918c:800:4500:2c:4c77:0:3e06 port:443
{"host":"yahoo.co.jp","ip":"182.22.16.123","timestamp":"2025-03-31T04:39:19.139307756Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.16.123 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:443
{"host":"yahoo.co.jp","ip":"182.22.31.252","timestamp":"2025-03-31T04:39:19.150208952Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.31.252 ipv6:5d3a:918c:800:4500:28:4b00:4000:3e06 port:80
{"host":"yahoo.co.jp","ip":"182.22.28.252","timestamp":"2025-03-31T04:39:19.173866445Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.28.252 ipv6:5d3a:918c:800:4500:28:4d00:4000:3e06 port:5060
{"host":"yahoo.co.jp","ip":"183.79.219.124","timestamp":"2025-03-31T04:39:19.174077745Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.219.124 ipv6:5d3a:918c:800:4500:28:4d00:4000:3e06 port:5060
{"host":"yahoo.co.jp","ip":"182.22.16.123","timestamp":"2025-03-31T04:39:19.174264045Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.16.123 ipv6:5d3a:918c:800:4500:2c:4c78:0:3e06 port:80
{"host":"yahoo.co.jp","ip":"182.22.25.124","timestamp":"2025-03-31T04:39:19.195958338Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.25.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3506 port:80
{"host":"yahoo.co.jp","ip":"182.22.31.124","timestamp":"2025-03-31T04:39:19.22386473Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.31.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:5060
{"host":"yahoo.co.jp","ip":"182.22.25.252","timestamp":"2025-03-31T04:39:19.22402643Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.25.252 ipv6:5d3a:918c:800:4500:2c:4c80:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-03-31T04:39:19.22411493Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.24.252 ipv6:5d3a:918c:800:4500:2c:4c7f:0:3e06 port:5060
{"host":"yahoo.co.jp","ip":"124.83.185.252","timestamp":"2025-03-31T04:39:19.22425733Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.185.252 ipv6:5d3a:918c:800:4500:2c:4c7d:0:3e06 port:443
{"host":"yahoo.co.jp","ip":"183.79.219.252","timestamp":"2025-03-31T04:39:19.22435113Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.219.252 ipv6:5d3a:918c:800:4500:2c:0:4000:3306 port:2000
{"host":"yahoo.co.jp","ip":"182.22.31.252","timestamp":"2025-03-31T04:39:19.22438723Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.31.252 ipv6:5d3a:918c:800:4500:2c:4c86:0:3e06 port:5060
{"host":"yahoo.co.jp","ip":"124.83.184.252","timestamp":"2025-03-31T04:39:19.224636929Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.184.252 ipv6:5d3a:918c:800:4500:2c:4c7e:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"183.79.250.251","timestamp":"2025-03-31T04:39:19.224699629Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.250.251 ipv6:5d3a:918c:800:4500:2c:4c87:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"124.83.185.252","timestamp":"2025-03-31T04:39:19.225112629Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.185.252 ipv6:5d3a:918c:800:4500:2c:4c7c:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-03-31T04:39:19.225211929Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.24.252 ipv6:5d3a:918c:800:4500:2c:4c8f:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"182.22.16.251","timestamp":"2025-03-31T04:39:19.225397629Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.16.251 ipv6:5d3a:918c:800:4500:2c:4c90:0:3e06 port:5060
{"host":"yahoo.co.jp","ip":"183.79.249.124","timestamp":"2025-03-31T04:39:19.225491129Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.249.124 ipv6:5d3a:918c:800:4500:2c:4c7b:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"182.22.25.252","timestamp":"2025-03-31T04:39:19.225563529Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.25.252 ipv6:5d3a:918c:800:4500:2c:4c8e:0:3e06 port:5060
{"host":"yahoo.co.jp","ip":"124.83.185.124","timestamp":"2025-03-31T04:39:19.225637129Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.185.124 ipv6:5d3a:918c:800:4500:2c:4c88:0:3e06 port:5060
{"host":"yahoo.co.jp","ip":"182.22.16.123","timestamp":"2025-03-31T04:39:19.225769529Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.16.123 ipv6:5d3a:918c:800:4500:2c:4c7a:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"124.83.185.124","timestamp":"2025-03-31T04:39:19.225876229Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.185.124 ipv6:5d3a:918c:800:4500:2c:4c91:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"183.79.219.252","timestamp":"2025-03-31T04:39:19.225912129Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.219.252 ipv6:5d3a:918c:800:4500:28:5200:4000:3e06 port:443
{"host":"yahoo.co.jp","ip":"183.79.219.124","timestamp":"2025-03-31T04:39:19.225944129Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.219.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3006 port:80
{"host":"yahoo.co.jp","ip":"182.22.25.252","timestamp":"2025-03-31T04:39:19.225975629Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.25.252 ipv6:5d3a:918c:800:4500:2c:0:4000:3006 port:80
{"host":"yahoo.co.jp","ip":"182.22.31.252","timestamp":"2025-03-31T04:39:19.226041529Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.31.252 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:2000
{"host":"yahoo.co.jp","ip":"182.22.24.124","timestamp":"2025-03-31T04:39:19.226090129Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.24.124 ipv6:5d3a:918c:800:4500:2c:4c8d:0:3e06 port:5060
{"host":"yahoo.co.jp","ip":"182.22.25.252","timestamp":"2025-03-31T04:39:19.226216329Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.25.252 ipv6:5d3a:918c:800:4500:2c:4c92:0:3e06 port:443
{"host":"yahoo.co.jp","ip":"124.83.184.252","timestamp":"2025-03-31T04:39:19.226392029Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.184.252 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:443
{"host":"yahoo.co.jp","ip":"182.22.16.123","timestamp":"2025-03-31T04:39:19.226434229Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.16.123 ipv6:5d3a:918c:800:4500:2c:0:4000:3306 port:5060
{"host":"yahoo.co.jp","ip":"124.83.184.124","timestamp":"2025-03-31T04:39:19.226472829Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.184.124 ipv6:5d3a:918c:800:4500:2c:4c81:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"124.83.185.252","timestamp":"2025-03-31T04:39:19.226505529Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.185.252 ipv6:5d3a:918c:800:4500:2c:4c82:0:3e06 port:5060
{"host":"yahoo.co.jp","ip":"183.79.250.251","timestamp":"2025-03-31T04:39:19.226588929Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.250.251 ipv6:5d3a:918c:800:4500:2c:4c83:0:3e06 port:5060
{"host":"yahoo.co.jp","ip":"182.22.16.251","timestamp":"2025-03-31T04:39:19.226671629Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.16.251 ipv6:5d3a:918c:800:4500:2c:4c84:0:3e06 port:80
{"host":"yahoo.co.jp","ip":"183.79.249.252","timestamp":"2025-03-31T04:39:19.226881929Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.249.252 ipv6:5d3a:918c:800:4500:2c:0:4000:3506 port:2000
{"host":"yahoo.co.jp","ip":"182.22.28.252","timestamp":"2025-03-31T04:39:19.227000529Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.28.252 ipv6:5d3a:918c:800:4500:2c:4c85:0:3e06 port:443
{"host":"yahoo.co.jp","ip":"182.22.24.124","timestamp":"2025-03-31T04:39:19.227209229Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.24.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:2000
{"host":"yahoo.co.jp","ip":"182.22.31.124","timestamp":"2025-03-31T04:39:19.227403829Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.31.124 ipv6:5d3a:918c:800:4500:2c:4c89:0:3e06 port:443
{"host":"yahoo.co.jp","ip":"183.79.219.252","timestamp":"2025-03-31T04:39:19.227611929Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.219.252 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:80
{"host":"yahoo.co.jp","ip":"183.79.249.124","timestamp":"2025-03-31T04:39:19.227782029Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.249.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3006 port:5060
{"host":"yahoo.co.jp","ip":"182.22.31.252","timestamp":"2025-03-31T04:39:19.227960728Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.31.252 ipv6:5d3a:918c:800:4500:2c:4c8c:0:3e06 port:443
{"host":"yahoo.co.jp","ip":"182.22.24.124","timestamp":"2025-03-31T04:39:19.228097228Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.24.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:443
{"host":"yahoo.co.jp","ip":"182.22.31.124","timestamp":"2025-03-31T04:39:19.228173228Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.31.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:80
{"host":"yahoo.co.jp","ip":"183.79.219.252","timestamp":"2025-03-31T04:39:19.228377328Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.219.252 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:5060
{"host":"yahoo.co.jp","ip":"183.79.219.124","timestamp":"2025-03-31T04:39:19.228521928Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.219.124 ipv6:5d3a:918c:800:4500:2c:4c8b:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"182.22.28.252","timestamp":"2025-03-31T04:39:19.228682528Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.28.252 ipv6:5d3a:918c:800:4500:2c:4c8a:0:3e06 port:80
{"host":"yahoo.co.jp","ip":"182.22.25.124","timestamp":"2025-03-31T04:39:19.228858928Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.25.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:443
{"host":"yahoo.co.jp","ip":"182.22.24.124","timestamp":"2025-03-31T04:39:19.229028328Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.24.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:80
{"host":"yahoo.co.jp","ip":"124.83.184.124","timestamp":"2025-03-31T04:39:19.229241628Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.184.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:5060
{"host":"yahoo.co.jp","ip":"183.79.249.252","timestamp":"2025-03-31T04:39:19.229480128Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.249.252 ipv6:5d3a:918c:800:4500:2c:4c96:0:3e06 port:5060
{"host":"yahoo.co.jp","ip":"182.22.28.252","timestamp":"2025-03-31T04:39:19.229624728Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.28.252 ipv6:5d3a:918c:800:4500:2c:4c94:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"182.22.25.124","timestamp":"2025-03-31T04:39:19.229794628Z","port":2000,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.25.124 ipv6:5d3a:918c:800:4500:2c:4c95:0:3e06 port:2000
{"host":"yahoo.co.jp","ip":"182.22.25.124","timestamp":"2025-03-31T04:39:19.229996428Z","port":5060,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.25.124 ipv6:5d3a:918c:800:4500:28:5200:4000:3e06 port:5060
{"host":"yahoo.co.jp","ip":"182.22.16.251","timestamp":"2025-03-31T04:39:19.230337128Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.16.251 ipv6:5d3a:918c:800:4500:28:5200:4000:3e06 port:443
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-03-31T04:39:19.230505828Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:182.22.24.252 ipv6:5d3a:918c:800:4500:2c:0:4000:3506 port:80
{"host":"yahoo.co.jp","ip":"124.83.185.124","timestamp":"2025-03-31T04:39:19.237801325Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.185.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3806 port:443
{"host":"yahoo.co.jp","ip":"183.79.219.124","timestamp":"2025-03-31T04:39:19.238061325Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.219.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3306 port:443
{"host":"yahoo.co.jp","ip":"183.79.250.251","timestamp":"2025-03-31T04:39:19.238194025Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.250.251 ipv6:5d3a:918c:800:4500:2c:0:4000:3006 port:80
{"host":"yahoo.co.jp","ip":"124.83.185.252","timestamp":"2025-03-31T04:39:19.238349625Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.185.252 ipv6:5d3a:918c:800:4500:2c:0:4000:3306 port:80
{"host":"yahoo.co.jp","ip":"183.79.250.251","timestamp":"2025-03-31T04:39:19.238572925Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.250.251 ipv6:5d3a:918c:800:4500:2c:0:4000:3306 port:443
{"host":"yahoo.co.jp","ip":"124.83.184.124","timestamp":"2025-03-31T04:39:19.238759025Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.184.124 ipv6:5d3a:918c:800:4500:28:8718:4000:3006 port:443
{"host":"yahoo.co.jp","ip":"124.83.184.252","timestamp":"2025-03-31T04:39:19.239097525Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.184.252 ipv6:5d3a:918c:800:4500:2c:0:4000:3306 port:80
{"host":"yahoo.co.jp","ip":"124.83.184.124","timestamp":"2025-03-31T04:39:19.239264725Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:124.83.184.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3306 port:80
{"host":"yahoo.co.jp","ip":"183.79.249.124","timestamp":"2025-03-31T04:39:19.239610825Z","port":443,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.249.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3306 port:443
{"host":"yahoo.co.jp","ip":"183.79.249.124","timestamp":"2025-03-31T04:39:19.239781725Z","port":80,"protocol":"tcp","tls":false}
[DBG] Received Transport (TCP) scan response from ipv4:183.79.249.124 ipv6:5d3a:918c:800:4500:2c:0:4000:3306 port:80
[INF] Found 4 ports on host yahoo.co.jp (182.22.16.251)
[INF] Found 4 ports on host yahoo.co.jp (182.22.24.124)
[INF] Found 4 ports on host yahoo.co.jp (182.22.28.252)
[INF] Found 4 ports on host yahoo.co.jp (182.22.31.252)
[INF] Found 4 ports on host yahoo.co.jp (183.79.219.124)
[INF] Found 3 ports on host yahoo.co.jp (124.83.185.124)
[INF] Found 4 ports on host yahoo.co.jp (182.22.24.252)
[INF] Found 4 ports on host yahoo.co.jp (182.22.16.123)
[INF] Found 4 ports on host yahoo.co.jp (182.22.25.124)
[INF] Found 4 ports on host yahoo.co.jp (182.22.25.252)
[INF] Found 4 ports on host yahoo.co.jp (124.83.185.252)
[INF] Found 4 ports on host yahoo.co.jp (182.22.31.124)
[INF] Found 4 ports on host yahoo.co.jp (183.79.219.252)
[INF] Found 4 ports on host yahoo.co.jp (183.79.250.251)
[INF] Found 4 ports on host yahoo.co.jp (183.79.249.124)
[INF] Found 2 ports on host yahoo.co.jp (183.79.249.252)
[INF] Found 4 ports on host yahoo.co.jp (124.83.184.124)
[INF] Found 4 ports on host yahoo.co.jp (124.83.184.252)
```

ctrl+Cをして打ち切れる。


output
jsonのoutputはこんな感じになる
```
{"host":"yahoo.co.jp","ip":"183.79.219.252","timestamp":"2025-04-16T07:55:26.904530183Z","port":443,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.219.252","timestamp":"2025-04-16T07:55:26.904530183Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.219.252","timestamp":"2025-04-16T07:55:26.904530183Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.219.252","timestamp":"2025-04-16T07:55:26.904530183Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.250.251","timestamp":"2025-04-16T07:55:26.905132193Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.250.251","timestamp":"2025-04-16T07:55:26.905132193Z","port":443,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.250.251","timestamp":"2025-04-16T07:55:26.905132193Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.250.251","timestamp":"2025-04-16T07:55:26.905132193Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.185.252","timestamp":"2025-04-16T07:55:26.905393897Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.185.252","timestamp":"2025-04-16T07:55:26.905393897Z","port":443,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.185.252","timestamp":"2025-04-16T07:55:26.905393897Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.185.252","timestamp":"2025-04-16T07:55:26.905393897Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.249.124","timestamp":"2025-04-16T07:55:26.9056136Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.249.124","timestamp":"2025-04-16T07:55:26.9056136Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.249.124","timestamp":"2025-04-16T07:55:26.9056136Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.249.124","timestamp":"2025-04-16T07:55:26.9056136Z","port":443,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.252","timestamp":"2025-04-16T07:55:26.905706802Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.252","timestamp":"2025-04-16T07:55:26.905706802Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.252","timestamp":"2025-04-16T07:55:26.905706802Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.252","timestamp":"2025-04-16T07:55:26.905706802Z","port":443,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.124","timestamp":"2025-04-16T07:55:26.905943206Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.124","timestamp":"2025-04-16T07:55:26.905943206Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.124","timestamp":"2025-04-16T07:55:26.905943206Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.124","timestamp":"2025-04-16T07:55:26.905943206Z","port":443,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.16.251","timestamp":"2025-04-16T07:55:26.906139609Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.16.251","timestamp":"2025-04-16T07:55:26.906139609Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.16.251","timestamp":"2025-04-16T07:55:26.906139609Z","port":443,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.16.251","timestamp":"2025-04-16T07:55:26.906139609Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.252","timestamp":"2025-04-16T07:55:26.906341812Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.252","timestamp":"2025-04-16T07:55:26.906341812Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.252","timestamp":"2025-04-16T07:55:26.906341812Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.252","timestamp":"2025-04-16T07:55:26.906341812Z","port":443,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-04-16T07:55:26.906709618Z","port":443,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-04-16T07:55:26.906709618Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-04-16T07:55:26.906709618Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-04-16T07:55:26.906709618Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.124","timestamp":"2025-04-16T07:55:26.906926422Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.124","timestamp":"2025-04-16T07:55:26.906926422Z","port":5060,"protocol":"tcp","tls":false}
```



### options

#### -wn でhost discoveryを有効にする

#### -nmapを使えば、nmap使える

#### -passiveはないほうがたくさん出る。
-passiveなし
```
^C[INF] Found 4 ports on host yahoo.co.jp (182.22.24.252) 
[INF] Found 4 ports on host yahoo.co.jp (182.22.31.124)   
[INF] Found 4 ports on host yahoo.co.jp (183.79.250.251)  
[INF] Found 4 ports on host yahoo.co.jp (183.79.249.124)  
[INF] Found 4 ports on host yahoo.co.jp (182.22.28.252)   
[INF] Found 4 ports on host yahoo.co.jp (124.83.184.124)  
[INF] Found 4 ports on host yahoo.co.jp (182.22.24.124)   
[INF] Found 4 ports on host yahoo.co.jp (183.79.219.252)  
[INF] Found 4 ports on host yahoo.co.jp (124.83.185.252)  
[INF] Found 4 ports on host yahoo.co.jp (183.79.249.252)  
[INF] Found 4 ports on host yahoo.co.jp (182.22.16.123)   
[INF] Found 4 ports on host yahoo.co.jp (182.22.25.124)   
[INF] Found 4 ports on host yahoo.co.jp (182.22.25.252)   
[INF] Found 4 ports on host yahoo.co.jp (182.22.16.251)   
[INF] Found 4 ports on host yahoo.co.jp (183.79.219.124)  
[INF] Found 4 ports on host yahoo.co.jp (124.83.185.124)  
[INF] Found 4 ports on host yahoo.co.jp (182.22.31.252)   
[INF] Found 4 ports on host yahoo.co.jp (124.83.184.252)  
[INF] CTRL+C pressed: Exiting                                                                                                  
```
-passiveあり
```
[INF] Found 2 ports on host yahoo.co.jp (124.83.184.124)
[INF] Found 2 ports on host yahoo.co.jp (182.22.24.124) 
[INF] Found 2 ports on host yahoo.co.jp (182.22.16.251) 
[INF] Found 2 ports on host yahoo.co.jp (182.22.28.252) 
[INF] Found 2 ports on host yahoo.co.jp (182.22.24.252) 
[INF] Found 2 ports on host yahoo.co.jp (124.83.184.252)
[INF] Found 2 ports on host yahoo.co.jp (183.79.219.124)
[INF] Found 2 ports on host yahoo.co.jp (183.79.250.251)
[INF] Found 2 ports on host yahoo.co.jp (124.83.185.124)
[INF] Found 2 ports on host yahoo.co.jp (182.22.31.252) 
[INF] Found 2 ports on host yahoo.co.jp (182.22.31.124) 
[INF] Found 2 ports on host yahoo.co.jp (183.79.249.252)
[INF] Found 2 ports on host yahoo.co.jp (183.79.219.252)
[INF] Found 2 ports on host yahoo.co.jp (124.83.185.252)
[INF] Found 2 ports on host yahoo.co.jp (182.22.16.123) 
[INF] Found 2 ports on host yahoo.co.jp (182.22.25.252) 
[INF] Found 2 ports on host yahoo.co.jp (182.22.25.124) 
[INF] Found 2 ports on host yahoo.co.jp (183.79.249.124)
```

### -dbg, verboseなし の標準出力　result -> out2.json
```
[INF] Running host discovery scan
[INF] Running SYN scan with CAP_NET_RAW privileges
{"host":"yahoo.co.jp","ip":"183.79.249.252","timestamp":"2025-04-01T01:23:03.640249614Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.28.252","timestamp":"2025-04-01T01:23:03.656407098Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.124","timestamp":"2025-04-01T01:23:03.679295764Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.185.252","timestamp":"2025-04-01T01:23:03.736738864Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.16.251","timestamp":"2025-04-01T01:23:03.736854889Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.252","timestamp":"2025-04-01T01:23:03.736942748Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.219.252","timestamp":"2025-04-01T01:23:03.737071989Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.185.124","timestamp":"2025-04-01T01:23:03.737197873Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.185.252","timestamp":"2025-04-01T01:23:03.737350948Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-04-01T01:23:03.737460906Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.31.252","timestamp":"2025-04-01T01:23:03.737573573Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.252","timestamp":"2025-04-01T01:23:03.737654823Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.31.124","timestamp":"2025-04-01T01:23:03.737688839Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.252","timestamp":"2025-04-01T01:23:03.737736939Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.124","timestamp":"2025-04-01T01:23:03.737816781Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.219.252","timestamp":"2025-04-01T01:23:03.737896514Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.219.124","timestamp":"2025-04-01T01:23:03.737962056Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.185.124","timestamp":"2025-04-01T01:23:03.738083606Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.16.123","timestamp":"2025-04-01T01:23:03.738171139Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-04-01T01:23:03.738297673Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.249.124","timestamp":"2025-04-01T01:23:03.738387806Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.250.251","timestamp":"2025-04-01T01:23:03.738450206Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.25.124","timestamp":"2025-04-01T01:23:03.738545756Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.31.124","timestamp":"2025-04-01T01:23:03.740892148Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.252","timestamp":"2025-04-01T01:23:03.755221831Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.16.251","timestamp":"2025-04-01T01:23:03.755375339Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.124","timestamp":"2025-04-01T01:23:03.755465473Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.24.124","timestamp":"2025-04-01T01:23:03.755532531Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.249.252","timestamp":"2025-04-01T01:23:03.755636314Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.219.124","timestamp":"2025-04-01T01:23:03.755768481Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.31.124","timestamp":"2025-04-01T01:23:03.755861323Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.16.123","timestamp":"2025-04-01T01:23:03.755940298Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.31.252","timestamp":"2025-04-01T01:23:03.756038556Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.252","timestamp":"2025-04-01T01:23:03.756158914Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.124","timestamp":"2025-04-01T01:23:03.756249806Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"182.22.28.252","timestamp":"2025-04-01T01:23:03.756369948Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.249.124","timestamp":"2025-04-01T01:23:03.756468531Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.250.251","timestamp":"2025-04-01T01:23:03.756535156Z","port":2000,"protocol":"tcp","tls":false}
[INF] Found 2 ports on host yahoo.co.jp (124.83.184.252)
[INF] Found 2 ports on host yahoo.co.jp (182.22.25.252)
[INF] Found 2 ports on host yahoo.co.jp (124.83.185.252)
[INF] Found 2 ports on host yahoo.co.jp (183.79.249.252)
[INF] Found 2 ports on host yahoo.co.jp (182.22.28.252)
[INF] Found 2 ports on host yahoo.co.jp (182.22.24.124)
[INF] Found 3 ports on host yahoo.co.jp (182.22.24.252)
[INF] Found 2 ports on host yahoo.co.jp (182.22.16.251)
[INF] Found 2 ports on host yahoo.co.jp (124.83.184.124)
[INF] Found 2 ports on host yahoo.co.jp (183.79.250.251)
[INF] Found 2 ports on host yahoo.co.jp (182.22.31.252)
[INF] Found 2 ports on host yahoo.co.jp (124.83.185.124)
[INF] Found 2 ports on host yahoo.co.jp (183.79.249.124)
[INF] Found 2 ports on host yahoo.co.jp (183.79.219.124)
[INF] Found 2 ports on host yahoo.co.jp (183.79.219.252)
[INF] Found 2 ports on host yahoo.co.jp (182.22.25.124)
[INF] Found 3 ports on host yahoo.co.jp (182.22.31.124)
[INF] Found 2 ports on host yahoo.co.jp (182.22.16.123)
```


### wn option
#### wnなし
```
{"host":"yahoo.co.jp","ip":"124.83.184.124","timestamp":"2025-04-01T01:28:15.203713626Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.124","timestamp":"2025-04-01T01:28:15.203713626Z","port":5060,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.124","timestamp":"2025-04-01T01:28:15.203713626Z","port":80,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"124.83.184.124","timestamp":"2025-04-01T01:28:15.203713626Z","port":443,"protocol":"tcp","tls":false}
```
#### wnあり
```
{"host":"yahoo.co.jp","ip":"183.79.219.124","timestamp":"2025-04-01T01:29:25.560623143Z","port":2000,"protocol":"tcp","tls":false}
{"host":"yahoo.co.jp","ip":"183.79.219.124","timestamp":"2025-04-01T01:29:25.560623143Z","port":5060,"protocol":"tcp","tls":false}
```
wnがあるとすぐ終わる。wnないと探す時間が長いのか、なかなか終わらない。C-cで終わらせる


### 調べること
~~wnオプションをつけるのとつけないのでどう変わるか
pingを送って帰ってきた奴だけポート調べる。速くなる？
しかしping返さないやつも調べたいなら、ないほうがいいか。~~
