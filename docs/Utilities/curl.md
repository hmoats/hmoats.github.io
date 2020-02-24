# Utilities / curl

**Table of contents**
* [Using curl to test a connection and then write out metrics in json](#using-curl-to-test-a-connection-and-then-write-out-metrics-in-json)

---

### Using curl to test a connection and then write out metrics in json

```
hmoats@ubuntu:~$ curl --silent -o /dev/null -I --write-out "{\"url_effective\": \"%{url_effective}\", \"time_namelookup\": %{time_namelookup}, \"time_connect\": %{time_connect}, \"time_appconnect\": %{time_appconnect}, \"time_total\": %{time_total}, \"http_code\": %{http_code}}" https://www.google.com | jq .
{
  "url_effective": "https://www.google.com/",
  "time_namelookup": 0.068,
  "time_connect": 0.123,
  "time_appconnect": 0.409,
  "time_total": 0.495,
  "http_code": 200
}
```
