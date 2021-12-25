user : santa 
after brute forcing using burp intuder with sniper mode with passowrd list : 
https://assets.tryhackme.com/additional/aoc2021/day4/passwords.txt

u get cookie with redirect status 

```bash
curl -i -s -k -X $'POST' \
    -H $'Host: 10.10.53.238' -H $'Content-Length: 43' -H $'Cache-Control: max-age=0' -H $'Upgrade-Insecure-Requests: 1' -H $'Origin: http://10.10.53.238' -H $'Content-Type: application/x-www-form-urlencoded' -H $'User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.45 Safari/537.36' -H $'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9' -H $'Referer: http://10.10.53.238/' -H $'Accept-Encoding: gzip, deflate' -H $'Accept-Language: en,en-US;q=0.9,fr-FR;q=0.8,fr;q=0.7,ar;q=0.6' -H $'Connection: close' \
    -b $'PHPSESSID=bpfjgnqjls5t37ht7anl01q2ci; __utma=128042636.1286790851.1638640873.1638640873.1638640873.1; __utmc=128042636; __utmz=128042636.1638640873.1.1.utmcsr=(direct)|utmccn=(direct)|utmcmd=(none); __utmb=128042636.2.9.1638640915503' \
    --data-binary $'username=santa&password=cookie&submit=Login' \
    $'http://10.10.53.238/'
```