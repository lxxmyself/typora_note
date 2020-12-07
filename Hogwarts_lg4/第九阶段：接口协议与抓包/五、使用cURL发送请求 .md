# 使用cURL发送请求 

![image-20201130142834679](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20201130142835.png)

1、熟悉chrome开发者工具

xhr：异步请求



![image-20201130143204442](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20201130143204.png)



![image-20201130143423756](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20201130143424.png)



![image-20201130143445013](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20201130143445.png)



![image-20201130143512712](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20201130143513.png)



![image-20201130143856582](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20201130143857.png)

![image-20201130144140101](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20201130144140.png)



```
Usage: curl [options...] <url>
Options: (H) means HTTP/HTTPS only, (F) means FTP only
     --anyauth       Pick "any" authentication method (H)
 -a, --append        Append to target file when uploading (F/SFTP)
     --basic         Use HTTP Basic Authentication (H)
     --cacert FILE   CA certificate to verify peer against (SSL)
     --capath DIR    CA directory to verify peer against (SSL)
 -E, --cert CERT[:PASSWD]  Client certificate file and password (SSL)
     --cert-status   Verify the status of the server certificate (SSL)
     --cert-type TYPE  Certificate file type (DER/PEM/ENG) (SSL)
     --ciphers LIST  SSL ciphers to use (SSL)
     --compressed    Request compressed response (using deflate or gzip)
 -K, --config FILE   Read config from FILE
     --connect-timeout SECONDS  Maximum time allowed for connection
     --connect-to HOST1:PORT1:HOST2:PORT2 Connect to host (network level)
 -C, --continue-at OFFSET  Resumed transfer OFFSET
 -b, --cookie STRING/FILE  Read cookies from STRING/FILE (H)
 -c, --cookie-jar FILE  Write cookies to FILE after operation (H)
     --create-dirs   Create necessary local directory hierarchy
     --crlf          Convert LF to CRLF in upload
     --crlfile FILE  Get a CRL list in PEM format from the given file
 -d, --data DATA     HTTP POST data (H)
     --data-raw DATA  HTTP POST data, '@' allowed (H)
     --data-ascii DATA  HTTP POST ASCII data (H)
     --data-binary DATA  HTTP POST binary data (H)
     --data-urlencode DATA  HTTP POST data url encoded (H)
     --delegation STRING  GSS-API delegation permission
     --digest        Use HTTP Digest Authentication (H)
     --disable-eprt  Inhibit using EPRT or LPRT (F)
     --disable-epsv  Inhibit using EPSV (F)
     --dns-servers   DNS server addrs to use: 1.1.1.1;2.2.2.2
     --dns-interface  Interface to use for DNS requests
     --dns-ipv4-addr  IPv4 address to use for DNS requests, dot notation
     --dns-ipv6-addr  IPv6 address to use for DNS requests, dot notation
 -D, --dump-header FILE  Write the received headers to FILE
     --egd-file FILE  EGD socket path for random data (SSL)
     --engine ENGINE  Crypto engine (use "--engine list" for list) (SSL)
     --expect100-timeout SECONDS How long to wait for 100-continue (H)
 -f, --fail          Fail silently (no output at all) on HTTP errors (H)
     --fail-early    Fail on first transfer error, do not continue
     --false-start   Enable TLS False Start.
 -F, --form CONTENT  Specify HTTP multipart POST data (H)
     --form-string STRING  Specify HTTP multipart POST data (H)
     --ftp-account DATA  Account data string (F)
     --ftp-alternative-to-user COMMAND  String to replace "USER [name]" (F)
     --ftp-create-dirs  Create the remote dirs if not present (F)
     --ftp-method [MULTICWD/NOCWD/SINGLECWD]  Control CWD usage (F)
     --ftp-pasv      Use PASV/EPSV instead of PORT (F)
 -P, --ftp-port ADR  Use PORT with given address instead of PASV (F)
     --ftp-skip-pasv-ip  Skip the IP address for PASV (F)
     --ftp-pret      Send PRET before PASV (for drftpd) (F)
     --ftp-ssl-ccc   Send CCC after authenticating (F)
     --ftp-ssl-ccc-mode ACTIVE/PASSIVE  Set CCC mode (F)
     --ftp-ssl-control  Require SSL/TLS for FTP login, clear for transfer (F)
 -G, --get           Send the -d data with a HTTP GET (H)
 -g, --globoff       Disable URL sequences and ranges using {} and []
 -H, --header LINE   Pass custom header LINE to server (H)
 -I, --head          Show document info only
 -h, --help          This help text
     --hostpubmd5 MD5  Hex-encoded MD5 string of the host public key. (SSH)
 -0, --http1.0       Use HTTP 1.0 (H)
     --http1.1       Use HTTP 1.1 (H)
     --http2         Use HTTP 2 (H)
     --http2-prior-knowledge  Use HTTP 2 without HTTP/1.1 Upgrade (H)
     --ignore-content-length  Ignore the HTTP Content-Length header
 -i, --include       Include protocol headers in the output (H/F)
 -k, --insecure      Allow connections to SSL sites without certs (H)
     --interface INTERFACE  Use network INTERFACE (or address)
 -4, --ipv4          Resolve name to IPv4 address
 -6, --ipv6          Resolve name to IPv6 address
 -j, --junk-session-cookies  Ignore session cookies read from file (H)
     --keepalive-time SECONDS  Wait SECONDS between keepalive probes
     --key KEY       Private key file name (SSL/SSH)
     --key-type TYPE  Private key file type (DER/PEM/ENG) (SSL)
     --krb LEVEL     Enable Kerberos with security LEVEL (F)
     --libcurl FILE  Dump libcurl equivalent code of this command line
     --limit-rate RATE  Limit transfer speed to RATE
 -l, --list-only     List only mode (F/POP3)
     --local-port RANGE  Force use of RANGE for local port numbers
 -L, --location      Follow redirects (H)
     --location-trusted  Like '--location', and send auth to other hosts (H)
     --login-options OPTIONS  Server login options (IMAP, POP3, SMTP)
 -M, --manual        Display the full manual
     --mail-from FROM  Mail from this address (SMTP)
     --mail-rcpt TO  Mail to this/these addresses (SMTP)
     --mail-auth AUTH  Originator address of the original email (SMTP)
     --max-filesize BYTES  Maximum file size to download (H/F)
     --max-redirs NUM  Maximum number of redirects allowed (H)
 -m, --max-time SECONDS  Maximum time allowed for the transfer
     --metalink      Process given URLs as metalink XML file
     --negotiate     Use HTTP Negotiate (SPNEGO) authentication (H)
 -n, --netrc         Must read .netrc for user name and password
     --netrc-optional  Use either .netrc or URL; overrides -n
     --netrc-file FILE  Specify FILE for netrc
 -:, --next          Allows the following URL to use a separate set of options
     --no-alpn       Disable the ALPN TLS extension (H)
 -N, --no-buffer     Disable buffering of the output stream
     --no-keepalive  Disable keepalive use on the connection
     --no-npn        Disable the NPN TLS extension (H)
     --no-sessionid  Disable SSL session-ID reusing (SSL)
     --noproxy       List of hosts which do not use proxy
     --ntlm          Use HTTP NTLM authentication (H)
     --ntlm-wb       Use HTTP NTLM authentication with winbind (H)
     --oauth2-bearer TOKEN  OAuth 2 Bearer Token (IMAP, POP3, SMTP)
 -o, --output FILE   Write to FILE instead of stdout
     --pass PASS     Pass phrase for the private key (SSL/SSH)
     --path-as-is    Do not squash .. sequences in URL path
     --pinnedpubkey FILE/HASHES Public key to verify peer against (SSL)
     --post301       Do not switch to GET after following a 301 redirect (H)
     --post302       Do not switch to GET after following a 302 redirect (H)
     --post303       Do not switch to GET after following a 303 redirect (H)
     --preproxy [PROTOCOL://]HOST[:PORT] Proxy before HTTP(S) proxy
 -#, --progress-bar  Display transfer progress as a progress bar
     --proto PROTOCOLS  Enable/disable PROTOCOLS
     --proto-default PROTOCOL  Use PROTOCOL for any URL missing a scheme
     --proto-redir PROTOCOLS   Enable/disable PROTOCOLS on redirect
 -x, --proxy [PROTOCOL://]HOST[:PORT]  Use proxy on given port
     --proxy-anyauth  Pick "any" proxy authentication method (H)
     --proxy-basic   Use Basic authentication on the proxy (H)
     --proxy-digest  Use Digest authentication on the proxy (H)
     --proxy-cacert FILE CA certificate to verify peer against for proxy (SSL)
     --proxy-capath DIR CA directory to verify peer against for proxy (SSL)
     --proxy-cert CERT[:PASSWD] Client certificate file and password for proxy (SSL)
     --proxy-cert-type TYPE Certificate file type (DER/PEM/ENG) for proxy (SSL)
     --proxy-ciphers LIST SSL ciphers to use for proxy (SSL)
     --proxy-crlfile FILE Get a CRL list in PEM format from the given file for proxy
     --proxy-insecure Allow connections to SSL sites without certs for proxy (H)
     --proxy-key KEY Private key file name for proxy (SSL)
     --proxy-key-type TYPE Private key file type for proxy (DER/PEM/ENG) (SSL)
     --proxy-negotiate  Use HTTP Negotiate (SPNEGO) authentication on the proxy (H)
     --proxy-ntlm    Use NTLM authentication on the proxy (H)
     --proxy-header LINE Pass custom header LINE to proxy (H)
     --proxy-pass PASS Pass phrase for the private key for proxy (SSL)
     --proxy-ssl-allow-beast Allow security flaw to improve interop for proxy (SSL)
     --proxy-tlsv1   Use TLSv1 for proxy (SSL)
     --proxy-tlsuser USER TLS username for proxy
     --proxy-tlspassword STRING TLS password for proxy
     --proxy-tlsauthtype STRING TLS authentication type for proxy (default SRP)
     --proxy-service-name NAME  SPNEGO proxy service name
     --service-name NAME  SPNEGO service name
 -U, --proxy-user USER[:PASSWORD]  Proxy user and password
     --proxy1.0 HOST[:PORT]  Use HTTP/1.0 proxy on given port
 -p, --proxytunnel   Operate through a HTTP proxy tunnel (using CONNECT)
     --pubkey KEY    Public key file name (SSH)
 -Q, --quote CMD     Send command(s) to server before transfer (F/SFTP)
     --random-file FILE  File for reading random data from (SSL)
 -r, --range RANGE   Retrieve only the bytes within RANGE
     --raw           Do HTTP "raw"; no transfer decoding (H)
 -e, --referer       Referer URL (H)
 -J, --remote-header-name  Use the header-provided filename (H)
 -O, --remote-name   Write output to a file named as the remote file
     --remote-name-all  Use the remote file name for all URLs
 -R, --remote-time   Set the remote file's time on the local output
 -X, --request COMMAND  Specify request command to use
     --resolve HOST:PORT:ADDRESS  Force resolve of HOST:PORT to ADDRESS
     --retry NUM   Retry request NUM times if transient problems occur
     --retry-connrefused  Retry on connection refused (use with --retry)
     --retry-delay SECONDS  Wait SECONDS between retries
     --retry-max-time SECONDS  Retry only within this period
     --sasl-ir       Enable initial response in SASL authentication
 -S, --show-error    Show error. With -s, make curl show errors when they occur
 -s, --silent        Silent mode (don't output anything)
     --socks4 HOST[:PORT]  SOCKS4 proxy on given host + port
     --socks4a HOST[:PORT]  SOCKS4a proxy on given host + port
     --socks5 HOST[:PORT]  SOCKS5 proxy on given host + port
     --socks5-hostname HOST[:PORT]  SOCKS5 proxy, pass host name to proxy
     --socks5-gssapi-service NAME  SOCKS5 proxy service name for GSS-API
     --socks5-gssapi-nec  Compatibility with NEC SOCKS5 server
 -Y, --speed-limit RATE  Stop transfers below RATE for 'speed-time' secs
 -y, --speed-time SECONDS  Trigger 'speed-limit' abort after SECONDS (default: 30)
     --ssl           Try SSL/TLS (FTP, IMAP, POP3, SMTP)
     --ssl-reqd      Require SSL/TLS (FTP, IMAP, POP3, SMTP)
 -2, --sslv2         Use SSLv2 (SSL)
 -3, --sslv3         Use SSLv3 (SSL)
     --ssl-allow-beast  Allow security flaw to improve interop (SSL)
     --ssl-no-revoke    Disable cert revocation checks (WinSSL)
     --stderr FILE   Where to redirect stderr (use "-" for stdout)
     --suppress-connect-headers  Suppress proxy CONNECT response headers
     --tcp-nodelay   Use the TCP_NODELAY option
     --tcp-fastopen  Use TCP Fast Open
 -t, --telnet-option OPT=VAL  Set telnet option
     --tftp-blksize VALUE  Set TFTP BLKSIZE option (must be >512)
     --tftp-no-options  Do not send TFTP options requests
 -z, --time-cond TIME   Transfer based on a time condition
 -1, --tlsv1         Use >= TLSv1 (SSL)
     --tlsv1.0       Use TLSv1.0 (SSL)
     --tlsv1.1       Use TLSv1.1 (SSL)
     --tlsv1.2       Use TLSv1.2 (SSL)
     --tlsv1.3       Use TLSv1.3 (SSL)
     --tls-max VERSION  Use TLS up to VERSION (SSL)
     --trace FILE    Write a debug trace to FILE
     --trace-ascii FILE  Like --trace, but without hex output
     --trace-time    Add time stamps to trace/verbose output
     --tr-encoding   Request compressed transfer encoding (H)
 -T, --upload-file FILE  Transfer FILE to destination
     --url URL       URL to work with
 -B, --use-ascii     Use ASCII/text transfer
 -u, --user USER[:PASSWORD]  Server user and password
     --tlsuser USER  TLS username
     --tlspassword STRING  TLS password
     --tlsauthtype STRING  TLS authentication type (default: SRP)
     --unix-socket PATH    Connect through this Unix domain socket
     --abstract-unix-socket PATH Connect to an abstract Unix domain socket
 -A, --user-agent STRING  Send User-Agent STRING to server (H)
 -v, --verbose       Make the operation more talkative
 -V, --version       Show version number and quit
 -w, --write-out FORMAT  Use output FORMAT after completion
     --xattr         Store metadata in extended file attributes
 -q, --disable       Disable .curlrc (must be first parameter)

```

```
url=http://www.baidu.com

## get请求加json解析 
curl -s 'https://xueqiu.com/stock/search.json?code=sogo&size=3&page=1' -H 'Connection: keep-alive' -H 'Pragma: no-cache' -H 'Cache-Control: no-cache' -H 'Accept: application/json, text/plain, */*' -H 'Sec-Fetch-Dest: empty' -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.149 Safari/537.36' -H 'elastic-apm-traceparent: 00-760301b0a132e9a4c0f5ac7448a3419e-8823be75504fc61f-00' -H 'Sec-Fetch-Site: same-origin' -H 'Sec-Fetch-Mode: cors' -H 'Referer: https://xueqiu.com/k?q=sogo' -H 'Accept-Language: zh-CN,zh;q=0.9,en-US;q=0.8,en;q=0.7' -H 'Cookie: device_id=24700f9f1986800ab4fcc880530dd0ed; cookiesu=841584103115161; aliyungf_tc=AQAAAIPytE8aVQoAXhjf3cw3R+j5DD/s; acw_tc=2760824b15851452106833674e25941ad47588d5d7ded79b38a04dad8f9444; xq_a_token=2ee68b782d6ac072e2a24d81406dd950aacaebe3; xqat=2ee68b782d6ac072e2a24d81406dd950aacaebe3; xq_r_token=f9a2c4e43ce1340d624c8b28e3634941c48f1052; xq_id_token=eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJ1aWQiOi0xLCJpc3MiOiJ1YyIsImV4cCI6MTU4NzUyMjY2MSwiY3RtIjoxNTg1MTQ1MTYxMDIwLCJjaWQiOiJkOWQwbjRBWnVwIn0.TPrw6_M2Th9QTVz5spwUybqN1790nJANu9kxXl4GfNb1eQ2p2zD43CStgogOGQ8yRXYmSCfURp0343wgjnnCdnQX5698Jl-brdP94wiYKwv11q8QjBYMXFWJGRj0g69C2nxVrRF8K-ETGEked3KjYfk8Xy2wPuZtyGUhORWeCvMhmBdcRKIlWj4d7wp-w_LjMbSLigJAT29F03wBZIxR0r3eMNUhUsXh8dCsWNb6wzhtg8dT4gcd91mQmR5ToR_SFrzQfOopY4vQGcaOHWaAwUMPLUopZwD4ajWzm1kpoBZnf_n_9uBfT4j0nGk95E8J8EmTfBlq-1p019xkhgp87w; u=431585145210698; Hm_lvt_1db88642e346389874251b5a1eded6e3=1583285031,1584102200,1585145180; Hm_lpvt_1db88642e346389874251b5a1eded6e3=1585145192' --compressed | jq
{
  "q": "sogo",
  "page": 1,
  "size": 3,
  "stocks": [
    {
      "code": "SOGO",
      "name": "搜狗",
      "enName": "",
      "hasexist": "false",
      "flag": null,
      "type": 0,
      "stock_id": 1029472,
      "ind_id": 0,
      "ind_name": "通讯业务",
      "ind_color": null,
      "_source": "sc_1:1:sogo"
    }
  ]
}


#post请求
curl 'http://sonarqube.testing-studio.com:9000/api/authentication/login' -H 'Connection: keep-alive' -H 'Pragma: no-cache' -H 'Cache-Control: no-cache' -H 'Accept: application/json' -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.149 Safari/537.36' -H 'Content-Type: application/x-www-form-urlencoded' -H 'Origin: http://sonarqube.testing-studio.com:9000' -H 'Referer: http://sonarqube.testing-studio.com:9000/sessions/new' -H 'Accept-Language: zh-CN,zh;q=0.9,en-US;q=0.8,en;q=0.7' -H 'Cookie: _ga=GA1.2.232181868.1566982077; experimentation_subject_id=IjNlYzgxODQ1LTU2MDAtNGIyNy1iNTgzLTE1MzRkY2IwMDI0ZSI%3D--b1f29d33f6a2c85a81be66e4774d437f710c102f; _gid=GA1.2.482544306.1585051015' --data 'login=admin&password=1234' --compressed --insecure

#百度的一个url提交脚本
curl -H 'Content-Type:text/plain' --data-binary @urls.txt "http://data.zz.baidu.com/urls"

#对参数编码并发送get请求
    curl -G $url  \
        --data-urlencode "current=$current" \
        --data-urlencode "pageSize=$pageSize" 


#认证与put上传都ElasticSearch里
    curl -X PUT "$ES_HOST/$index/_doc/$id?pretty" \
        --user username:password \
        -H 'Content-Type: application/json' \
        -d "$content"


#查看邮箱
curl -s --user $mail_username:$mail_password "imaps://imap.exmail.qq.com/inbox?all"
```

![image-20201130145002646](https://typora-lxx.oss-cn-beijing.aliyuncs.com/img/20201130145002.png)



1、解决curl乱码，chcp 65001 当前窗口有效，然后执行curl命令

