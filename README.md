<h1 align="center"> :ocean: Laravel docker-compose </h1>
<p align="center"> :zap: More detailed write nginx access logs.</p>

## Configuration

```
 log_format log_req_resp '$remote_addr - $remote_user [$time_local] '
        '"$request" $status $body_bytes_sent '
        '"$http_referer" "$http_user_agent" $request_time req_body:"$request_body"' 
        ' resp_body:"$resp_body" resp_header:"$resp_header" req_header:"$req_header"';
```

## Example 

```
192.168.10.1 - - [01/Nov/2019:16:38:59 +0800] "PUT /api/test/1 HTTP/1.1" 204 0 "http://localhost/api/tests" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.87 Safari/537.36" 0.130 req_body:"{\x22id\x22:116,\x22data\x22:[{\x22id\x22:239,\x22id\x22:116,\x22content\x22:\x221\x5Cn2\x5Cn3\x5Cn33333444433333333test3333\x22}]}" resp_body:"" resp_header:"content-type: application/octet-streamconnection: keep-aliveaccess-control-allow-origin: http://localhostx-ratelimit-limit: 500x-ratelimit-remaining: 490date: Fri, 01 Nov 2019 08:38:59 GMTvary: Origincache-control: private, must-revalidateetag: \x22da39a3ee5e6b4b0d3255bfef95601890afd80709\x22" req_header:"accept-language: zh-CN,zh;q=0.9content-type: application/json;charset=UTF-8connection: keep-alivecontent-length: 106accept-encoding: gzip, deflate, brreferer: http://localhostcache-control: no-cachehost: localhostsec-fetch-mode: corsaccept: application/json, text/plain, */*origin: http://localhostuser-agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.87 Safari/537.36pragma: no-cachesec-fetch-site: same-siteauthorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdGFmZl9pZCI6Nzc1fQ.Elplfv34V5hOd_WqMuPRwseokyosookljoYO6GDfeU6M1"
```

