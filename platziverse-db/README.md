# Lab IoT
## MQTT
.
MQTT (Message Queue Telemetry Transport) es un protocolo de transporte de mensajes Cliente/Servidor basado en publicaciones y subscripciones a los denominados “tópicos”. Cada vez que un mensaje es publicado será recibido por el resto de dispositivos adheridos a un tópico del protocolo.
.
El protocolo MQTT sirve mucho para conectar dispositivos de Internet de las Cosas, lo cual simplifica y hace más sencilla la recogida de datos de sensores, la publicación de los diferentes valores obtenidos y la configuración remota de los nodos.

JWT
.
JSON Web Token (abreviado JWT) es un estándar abierto basado en JSON para la creación de tokens de acceso que permiten la propagación de identidad y privilegios o claims en inglés (autorización).

1
![Descripción de la imagen](.\\img/project.png)



Instalamos el modulo de standar como dependencia de desarrollo para correcciond e errores
```console
npm init 
npm i --save-dev standard
```

ejecutamos standar para ver si hay erorres
```console
npm run lint
```
si hay errores podemos corregirlos con 
```console
npm run lint -- --fix
```
instlando las dependendias para manejode la db
```console
npm i pg pg-hstore --save
```
Creamos los modelos de db en lian/db.js



## Usage
requiero una funcion para la db
esta funcion va a retornar una promesa que va a retornar la configuracion de base de datos.

```js
const setupDatabase = require('db')
setupDatabase(config).then(db=> {
    const { Agent, Metric } = db
}).catch(err => console.error(err))
```
## Postgres
```console
su postgres
psql -l
psql postgres
postgres=# CREATE ROLE platzi WITH LOGIN PASSWORD 'platzi';
postgres=# CREATE DATABASE platziverse;
postgres=# GRANT ALL PRIVILEGES ON DATABASE platziverse TO platzi;
```

