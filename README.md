# Ejercicio-NoSQL-MongoDB

## Crear bbdd - Red social intercambio de patitos personalizados

```
use myFirstDB
```

## 1. Desarrollar el Proyecto

### A continuación, creará su propia base de datos de red social con las siguientes colecciones:

- users
- posts

```
db.createCollection('users')
{ ok: 1 }
myFirstDB> db.createCollection('posts')
{ ok: 1 }
```

## 2.1 INSERTAR DATOS

### Insertar al menos 15 publicaciones nuevas con al menos 2 comentarios por publicación:

- title
- body
- username
- comments
- username
- body

```
myFirstDB> db.post.insertMany([
...   {
...     "title": "¡Nuevo patito pirata disponible!",
...     "body": "He creado un patito con parche y sombrero pirata. ¿Quién quiere intercambiar?",
...     "comments": [
...       { "username": "ducklover22", "body": "¡Me encanta! Tengo uno de sirena para cambiar." },
...       { "username": "quackster", "body": "¿Aceptas uno de vaquero a cambio?" }
...     ]
...   },
...   {
...     "title": "Patito astronauta en busca de hogar",
...     "body": "Perfecto para los fans del espacio. ¡Tiene casco y todo!",
...     "comments": [
...       { "username": "spacequack", "body": "¿Tiene detalles fosforescentes?" },
...       { "username": "moonduck", "body": "Interesado, te escribo por privado." }
...     ]
...   },
... {
...     "title": "Colección de patitos de series",
...     "body": "Tengo patitos de personajes de series famosas. ¿Alguien colecciona también?",
...     "comments": [
...       { "username": "flixfan", "body": "¿Tienes uno de Stranger Things?" },
...       { "username": "bingequack", "body": "¡Me interesa uno de Breaking Bad!" }
...     ]
...   },
...   {
...     "title": "Intercambio patito gótico",
...     "body": "Con ojos oscuros y sombrero de copa. ¿Quién quiere algo diferente?",
...     "comments": [
...       { "username": "darkduck", "body": "¡Te cambio uno punk!" },
...       { "username": "emoquack", "body": "Me interesa mucho, ¿está disponible aún?" }
...     ]
...   } ])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('68402d4b008df87e1050eb67'),
    '1': ObjectId('68402d4b008df87e1050eb68'),
    '2': ObjectId('68402d4b008df87e1050eb69'),
    '3': ObjectId('68402d4b008df87e1050eb6a')
  }
}
```

continuación para insertar otros 4 comentarios:

```
myFirstDB> db.post.insertMany([ {
...     "title": "Busco patito medieval",
...     "body": "Necesito un caballero o dragón para completar mi colección.",
...     "comments": [
...       { "username": "castlequack", "body": "Tengo uno con armadura. ¿Tienes uno ninja?" },
...       { "username": "rubberknight", "body": "Tengo un patito dragón, ¿intercambiamos?" }
...     ]
...   },
...   {
...     "title": "Patito samurái para intercambio",
...     "body": "Con armadura y katana. ¡Súper detallado!",
...     "comments": [
...       { "username": "duckdojo", "body": "Lo quiero, tengo uno egipcio." },
...       { "username": "katanafan", "body": "¡Qué pasada! ¿Aún lo tienes?" }
...     ]
...   },
...   {
...     "title": "Edición limitada: Patito mago",
...     "body": "Inspirado en Harry Quacker. ¡Varita incluida!",
...     "comments": [
...       { "username": "magicduck", "body": "¿Tiene bufanda de colores?" },
...       { "username": "quackwarts", "body": "Lo necesito. ¿Qué quieres a cambio?" }
...     ]
...   },
...   {
...     "title": "Mini patito chef disponible",
...     "body": "Perfecto para cocineros amantes de los patos.",
...     "comments": [
...       { "username": "cookquack", "body": "Tengo uno panadero. ¿Te interesa?" },
...       { "username": "gourmetduck", "body": "¡Lo quiero para mi colección de profesiones!" }
...     ]
...   },
...   {
...     "title": "Patito vampiro para trueque",
...     "body": "Con capa y colmillos. ¡Ideal para Halloween!",
...     "comments": [
...       { "username": "nightquack", "body": "¿Lo cambias por uno zombie?" },
...       { "username": "hallowduck", "body": "¡Perfecto! ¿Dónde intercambiamos?" }
...     ]
...   }])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('68402ff2008df87e1050eb6b'),
    '1': ObjectId('68402ff2008df87e1050eb6c'),
    '2': ObjectId('68402ff2008df87e1050eb6d'),
    '3': ObjectId('68402ff2008df87e1050eb6e'),
    '4': ObjectId('68402ff2008df87e1050eb6f')
  }
}
```

Continuación para insertar los comentarios que faltan:

```
myFirstDB> db.post.insertMany([{
...     "title": "Patito viajero en busca de nuevo hogar",
...     "body": "Con mochila y gorro de explorador. Listo para nuevas aventuras.",
...     "comments": [
...       { "username": "wanderduck", "body": "Me interesa, tengo uno montañista." },
...       { "username": "adventurequack", "body": "¡Es justo el que me falta!" }
...     ]
...   },
...   {
...     "title": "Busco patito con temática musical",
...     "body": "¿Alguien tiene uno que parezca un rockero o DJ?",
...     "comments": [
...       { "username": "soundduck", "body": "Tengo uno con guitarra eléctrica." },
...       { "username": "quackbeats", "body": "¡Intercambio uno de batería!" }
...     ]
...   },
...   {
...     "title": "Patito unicornio para intercambio",
...     "body": "Con cuerno brillante y alas. ¡Muy kawaii!",
...     "comments": [
...       { "username": "fantasyquack", "body": "¿Tiene purpurina?" },
...       { "username": "sparkleduck", "body": "¡Lo quiero! Te ofrezco uno de hada." }
...     ]
...   },
...   {
...     "title": "Intercambio patito con traje de buzo",
...     "body": "Ideal para amantes del mar. ¡Incluye mini tanque de oxígeno!",
...     "comments": [
...       { "username": "oceanduck", "body": "Tengo uno de pulpo, ¿te interesa?" },
...       { "username": "deepquack", "body": "¡Perfecto para mi set acuático!" }
...     ]
...   },
...   {
...     "title": "Patito gamer en 8-bits",
...     "body": "Estilo pixelado retro. Muy raro.",
...     "comments": [
...       { "username": "arcadequack", "body": "¡Increíble! ¿Qué buscas a cambio?" },
...       { "username": "pixeldude", "body": "¿Funciona con pilas? 😂" }
...     ]
...   },
...   {
...     "title": "¡Patito Jedi disponible!",
...     "body": "Con sable de luz azul y bata marrón. Que la fuerza te acompañe.",
...     "comments": [
...       { "username": "darkquack", "body": "Tengo un patito Sith, hacemos intercambio épico." },
...       { "username": "forcefeather", "body": "¡Es el pato que estoy buscando!" }
...     ]
...   }])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('684031ca008df87e1050eb70'),
    '1': ObjectId('684031ca008df87e1050eb71'),
    '2': ObjectId('684031ca008df87e1050eb72'),
    '3': ObjectId('684031ca008df87e1050eb73'),
    '4': ObjectId('684031ca008df87e1050eb74'),
    '5': ObjectId('684031ca008df87e1050eb75')
  }
}
```

### Insertar al menos 10 nuevos usuarios (5 usuarios se repiten del listado de post):

- username
- email
- age

```
myFirstDB> db.user.insertMany([
...   {
...     "username": "ducklover22",
...     "email": "ducklover22@example.com",
...     "age": 28
...   },
...   {
...     "username": "quackster",
...     "email": "quackster@example.com",
...     "age": 34
...   },
...   {
...     "username": "flixfan",
...     "email": "flixfan@example.com",
...     "age": 22
...   },
...   {
...     "username": "magicduck",
...     "email": "magicduck@example.com",
...     "age": 30
...   },
...   {
...     "username": "cookquack",
...     "email": "cookquack@example.com",
...     "age": 26
...   },
...   {
...     "username": "rubberfan88",
...     "email": "rubberfan88@example.com",
...   }])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('684034ae008df87e1050eb76'),
    '1': ObjectId('684034ae008df87e1050eb77'),
    '2': ObjectId('684034ae008df87e1050eb78'),
    '3': ObjectId('684034ae008df87e1050eb79'),
    '4': ObjectId('684034ae008df87e1050eb7a'),
    '5': ObjectId('684034ae008df87e1050eb7b')
  }
}
```

los usuarios que faltan:

```
myFirstDB> db.user.insertMany([
...   {
...     username: "ducktastic",
...     email: "ducktastic@example.com",
...     age: 24
...   },
...   {
...     username: "patitocollector",
...     email: "patitocollector@example.com",
...     age: 29
...   },
...   {
...     username: "quackorama",
...     email: "quackorama@example.com",
...     age: 35
...   },
...   {
...     username: "swimfeather",
...     email: "swimfeather@example.com",
...     age: 27
...   }
... ])
...
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('68404dda008df87e1050eb7c'),
    '1': ObjectId('68404dda008df87e1050eb7d'),
    '2': ObjectId('68404dda008df87e1050eb7e'),
    '3': ObjectId('68404dda008df87e1050eb7f')
  }
}
```

## 2.2 ACTUALIZAR DATOS

### Actualizar publicaciones:

- Actualiza todos los valores de los campos de una publicación.

```
myFirstDB> db.post.updateOne({title:"¡Nuevo patito pirata disponible!"},{$rename:{title:"titulo", body:"contenido",comments:"comentario"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
```

- Cambiar el valor del campo “body” de una publicación.

```
myFirstDB> db.post.updateOne({title:"Intercambio patito con traje de buzo"},{$rename:{body:"contenido"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
```

- Actualiza el comentario de una publicación.

```
myFirstDB> db.post.updateOne({title:"¡Patito Jedi disponible!"}, {$set:{title:"comentario actualizado"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
```

### Actualizar usuarios:

- Actualiza todos los valores de los campos de un usuario:

```
myFirstDB> db.user.updateOne({username:"ducklover22"},{$rename:{username:"usuario", email:"correo", age:"edad"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
```

- Cambiar el email de dos usuarios, es decir, hacer la query dos veces.

```
myFirstDB> db.user.updateOne({username:"quackorama"},{$set:{email:"correito@correito.com"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
```

```
myFirstDB> db.user.updateOne({username:"patitocollector"},{$set:{email:"correito@correito.com"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
```

- Aumenta en 5 años la edad de un usuario.

```
myFirstDB> db.user.updateOne({username:"patitocollector"},{$inc:{age:4}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
```

## OBTENER DATOS

- Seleccionar todas las publicaciones.

```
myFirstDB> db.post.find()
```

- Selecciona las publicaciones que coincidan con el username indicado.

```
db.post.find({comments:{$elemMatch:{username:"oceanduck"}}})
```

- Seleccione todos los usuarios con una edad mayor a 20.

```
myFirstDB> db.user.find({age:{$gt:20}})
```

- Seleccione todos los usuarios con una edad inferior a 23.

```
myFirstDB> db.user.find({age:{$lt:23}})
```

- Seleccione todos los usuarios que tengan una edad entre 25 y 30 años.

```
 db.user.find({age:{$lt:30, $gt:25}})
```

- Muestra los usuarios de edad menor a mayor y viceversa.

```
myFirstDB> db.user.find().sort({age:1})
```

```
myFirstDB> db.user.find().sort({age:-1})
```

- Seleccione el número total de usuarios.

```
myFirstDB> db.user.find().count()
```

- Seleccione todas las publicaciones y haz que se muestren con la siguiente estructura: Título de la publicación: "title one".

```
myFirstDB> db.post.find().forEach((doc)=>{print("Título de la publicación: "+ doc.title)})
```

- Selecciona solo 2 usuarios.

```
myFirstDB> db.user.find().limit(2)
```

- Busca por title 2 publicaciones.(haz la misma consulta 2 veces)

```
myFirstDB> db.post.find({body:"Estilo pixelado retro. Muy raro."})
```

```
myFirstDB> db.post.find({body:"Con sable de luz azul y bata marrón. Que la fuerza te acompañe."})
```
