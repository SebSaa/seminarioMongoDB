Instalar MongoDB en ambiente local.  
Conectarse a MongoDB vía CLI.  
Crear una nueva base de datos llamada futbolfifa.  
```
> use futbolfifa
switched to db futbolfifa
```
Crear una nueva collection llamada players.  
```
> db.createCollection("players")
{ "ok" : 1 }
```
Insertar 5 documentos en la collection players con datos básicos (nombre, apellido, posición, fecha de nacimiento, etc). 
```
> db.players.insert({nombre: "Sebastian", apellido: "Saavedra", posicion: 9, nac: "12-8-1974"})
WriteResult({ "nInserted" : 1 })
> db.players.insert({
...     nombre: "Juan",
...     apellido: "Riquelme",
...     posicion: 10,
...     nac: "12-8-1974"})
WriteResult({ "nInserted" : 1 })
> db.players.insert({
...     nombre: "Esteban",
...     apellido: "Andrada",
...     posicion: 1,
...     nac: "12-8-1974"})
WriteResult({ "nInserted" : 1 })
> db.players.insert({
...     nombre: "Mauro",
...     apellido: "Zarate",
...     posicion: 7,
...     nac: "12-8-1974"})
WriteResult({ "nInserted" : 1 })
> db.players.insert({
...     nombre: "Frank",
...     apellido: "Fabra",
...     posicion: 4,
...     nac: "12-8-1974"})
WriteResult({ "nInserted" : 1 })
```
Listar todos los documentos de la collection players.  
```
> db.players.find()
{ "_id" : ObjectId("5f9a1824be805f50cbd3e74d"), "nombre" : "Sebastian", "apellido" : "Saavedra", "posicion" : 9, "nac" : "12-8-1974" }
{ "_id" : ObjectId("5f9a18acbe805f50cbd3e74e"), "nombre" : "Juan", "apellido" : "Riquelme", "posicion" : 10, "nac" : "12-8-1974" }
{ "_id" : ObjectId("5f9a1994be805f50cbd3e74f"), "nombre" : "Esteban", "apellido" : "Andrada", "posicion" : 1, "nac" : "12-8-1974" }
{ "_id" : ObjectId("5f9a199dbe805f50cbd3e750"), "nombre" : "Mauro", "apellido" : "Zarate", "posicion" : 7, "nac" : "12-8-1974" }
{ "_id" : ObjectId("5f9a19aebe805f50cbd3e751"), "nombre" : "Frank", "apellido" : "Fabra", "posicion" : 4, "nac" : "12-8-1974" }
```
Crear otras collections con documentos (ej. teams, games, etc).  
```
> db.createCollection("teams")
{ "ok" : 1 }
> db.createCollection("games")
{ "ok" : 1 }
> db.teams.insert([
...         {
...         name: "Boca Juniors",
...         barrio: "La Boca",
...         },
...         {
...         name: "Chacarita Juniors",
...         barrio: "Chacarita",
...         },
...         {
...         name: "San Lorenzo",
...         barrio: "Almagro",
...         },
...         {
...         name: "Defensa y Justicia",
...         barrio: "Florencio Varela",
...         },
...     ])
BulkWriteResult({
        "writeErrors" : [ ],
        "writeConcernErrors" : [ ],
        "nInserted" : 4,
        "nUpserted" : 0,
        "nMatched" : 0,
        "nModified" : 0,
        "nRemoved" : 0,
        "upserted" : [ ]
})
> db.teams.find()
{ "_id" : ObjectId("5f9a1c83be805f50cbd3e753"), "name" : "Boca Juniors", "barrio" : "La Boca" }
{ "_id" : ObjectId("5f9a1c83be805f50cbd3e754"), "name" : "Chacarita Juniors", "barrio" : "Chacarita" }
{ "_id" : ObjectId("5f9a1c83be805f50cbd3e755"), "name" : "San Lorenzo", "barrio" : "Almagro" }
{ "_id" : ObjectId("5f9a1c83be805f50cbd3e756"), "name" : "Defensa y Justicia", "barrio" : "Florencio Varela" }
