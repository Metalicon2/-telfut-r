                                                            Ételfutár

1. pizza-api / pizza mappában:

$ npm i

2. pizza-api mappa:

$ npm start

3. pizza mappa:

$ npm start

(rá fog kérdezni a portváltásra a react-app az induláskor => Yes)

4. mysql szerver indítása szükséges

5. server.js file-ban a user,password,database property-kre a megfelelő adatokat meg kell adni

let knex = require('knex')({
  client: 'mysql',
  version: '8.0',
  connection: {
    host : '127.0.0.1',
    user : YOUR_USER,
    password : YOUR_PASSWORD,
    database : YOUR_DATABASE_NAME
  }
});

6. mysql konzolban: source <Elérési útvonala az sql file-nak>;

Felhasznált technológiák:
-Backend: Node.js
-Frontend: React.js
-Adatbázis: mySQL

Leírás:

A projektet a backend írásával kezdtem, és saját hibából a leírásnak nem megfelelően nem ORM-et használtam, hanem 'knex'-et, ami lényegében sql query-k javascript-re map-elve. 
Ettől függetlenül mellékeltem a menuitems.sql file-t ami minden szükséges sql kódot tartalmaz.
Az idő szűkével legutoljára a Kosár funkciót implementáltam és nem sikerült megoldanom, hogy több étel is mentésre kerülhessen a rendelések táblába az adatbázisban, így csak az elsőt menti el.
