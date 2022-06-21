writeCode
```
> show dbs
admin   0.000GB
config  0.000GB
local   0.000GB
> use weather
switched to db weather
> db.createCollection('temperature');
{ "ok" : 1 }
> db.temperature.insert({titel: '32'});
WriteResult({ "nInserted" : 1 })
> db.temperature.insert({titel-2: '0'});
uncaught exception: SyntaxError: missing : after property id :
@(shell):1:28
> db.temperature.insert({titel: '0'});
WriteResult({ "nInserted" : 1 })
> db.temperature.insert({titel: '1'});
WriteResult({ "nInserted" : 1 })
> db.createCollection('humidity');
{ "ok" : 1 }
> show dbs
admin    0.000GB
config   0.000GB
local    0.000GB
weather  0.000GB
> show collections
humidity
temperature
```
Write command to

- List collections from a database.
>> show dbs
- create a new collection in your country database which you created recently.
>> db.insert({title: 'india is my country'})

Write code to:-

- crate a database named `weather`
use weather
- create a capped collection named `temperature` with maximum of 3 documents and try inserting more than 3 to see the result.
>>db.createCollection('temperature');
>>db.temperature.insert({titel: '32'});

- create a simple collection named `humidity`
>db.createCollection('humidity');
- check whether `temperature` collection is capped or not ?
>>show coolections
- Delete `humidity` collection and then the entire database(weather).
>>db.humidity.drop();
