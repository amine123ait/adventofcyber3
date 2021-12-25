```
ffuf -c -w [path]/common.txt -u http://10.10.26.191/FUZZ
```
result 
```
.hta                    [Status: 403, Size: 277, Words: 20, Lines: 10]
.htaccess               [Status: 403, Size: 277, Words: 20, Lines: 10]
.htpasswd               [Status: 403, Size: 277, Words: 20, Lines: 10]
admin                   [Status: 301, Size: 312, Words: 20, Lines: 10]
assets                  [Status: 301, Size: 313, Words: 20, Lines: 10]
index.html              [Status: 200, Size: 5061, Words: 1073, Lines: 85]
javascript              [Status: 301, Size: 317, Words: 20, Lines: 10]
server-status           [Status: 403, Size: 277, Words: 20, Lines: 10]
```

/admin admin login page

default creads : administrator:administrator