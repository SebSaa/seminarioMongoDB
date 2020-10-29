Crear una nueva base de datos de un sistema de streaming de video (ej. Netflix, Flow, Amazon Prime) que permita almacenar movies.
```
> use Netflix
switched to db Netflix
> db.createCollection("movies")
{ "ok" : 1 }
```
Para cada movie, se debería guardar información como título (String), year (Number), rating (Number, entre 1.0 y 5.0), genre (String), description (String), actors (Array<String>), country (String), income (Number), duration (Number).
Agregar películas usando insert(), insertOne() & insertMany().
```
> db.movies.insert ({
...         title: "Proyecto Geminis",
...         year: 2019,
...         rating: 3.8,
...         genre: "Accion",
...         description: "Henry Bogan, un asesino a sueldo, pretende retirarse porque se siente viejo. Sin embargo, hay alguien que no está dispuesto a permitírselo porque tiene la misión de matarlo: un clon suyo más joven, más rápido y más fuerte.",
...         actors : ["Will Smith","Mary Elizabeth Winstead","Clive Owen"],
...         country: "EEUU",
...         income: 173500000,
...         duration: "1h 57m"
...     })
WriteResult({ "nInserted" : 1 })

> db.movies.insertOne ({
...         title: "Rapidos y Furiosos 8",
...         year: 2017,
...         rating: 4.4,
...         genre: "Accion",
...         description: "Con Dom y Letty de luna de miel, Brian y Mia retirados y el resto de la pandilla viviendo en paz, parece que todo está tranquilo. Sin embargo, una misteriosa mujer seducirá a Dom para adentrarlo en el mundo del crimen y traicionar a la pandilla.",
...         actors : ["Vin Diesel","Dwayne Johnson","Jason Statham","Charlize Theron"],
...         country: "EEUU",
...         income: 1239000000,
...         duration: "1h 57m"
...     })
{
        "acknowledged" : true,
        "insertedId" : ObjectId("5f9a35b2be805f50cbd3e758")
}

> db.movies.insertMany ([
...     {
...         title: "Mr. Deeds",
...         year: 2002,
...         rating: 4.3,
...         genre: "Comedia",
...         description: "Una reportera intenta crear un escándalo que involucra al bondadoso heredero de la fortuna de un magnate de los medios.",
...         actors : ["Adam Sandler","Winona Ryder","John Turturro"],
...         country: "EEUU",
...         income: 39000000,
...         duration: "96m"
...     },
...     {
...         title: "El hombre araña",
...         year: 2002,
...         rating: 4.6,
...         genre: "Accion",
...         description: "Luego de sufrir la picadura de una araña genéticamente modificada, un estudiante de secundaria tímido y torpe adquiere increíbles capacidades como arácnido. Pronto comprenderá que su misión es utilizarlas para luchar contra el mal y defender a sus vecinos.",
...         actors : ["Tobey Maguire","Kirsten Dunst","Willem Dafoe","James Franco"],
...         country: "EEUU",
...         income: 825000000,
...         duration: "2h 1m"
...     }
...     ])
{
        "acknowledged" : true,
        "insertedIds" : [
                ObjectId("5f9a3a6bbe805f50cbd3e759"),
                ObjectId("5f9a3a6bbe805f50cbd3e75a")
        ]
}
```
Actualizar películas agregando el field highlighted=true a aquellas con rating > 4.5.
```
> db.movies.updateMany(
...         {rating :{$gt: 4.5}},
...         {
...             $set : {
...                 highlighted : true
...             }
...         },
...         {upsert : true}
...     )
{ "acknowledged" : true, "matchedCount" : 1, "modifiedCount" : 1 }
```
Actualizar películas cambiando el genre “drama” por “bored”.
Borrar todas las películas que tengan más de 30 años.
Buscar todas las películas argentinas.
Buscar todas las películas de acción con un buen rating (ej. > 4.0) que hayan salido los últimos 2 años.
