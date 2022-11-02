
# Writing-and-Presentation-Test week 6
## Day 1 : Web Server & API
**Senin, 24 Oktober 2022**
#### **Web Server**
- **Web Server** adalah sebuah website yang berfungsi menerima permintaan dan mengembalikan permintaan.
- **Web Server memiliki 2 komponen**
    -    Hardware : perangkat keras atau komputer yang menyimpan soft web server beserta filenya.
    -    Software : aplikasi web server  yang digunakan untuk menngotrol pennguna mengakses file yang di hosting.


- **Static Web Server VS Dynamic Web Server**
    - Static Web Server adalah web yang mengirimkan data sesuai yang ada diserver dan hanya dapat di ubah melalui server.
    - Dynamic Web Server adalah web yang mengirimkan data dari server dan datanya selalu update.

- **Server Side Programming adalah web server yang menunggu client request message, melakukan proses ketika request sampai, lalu memberikan response ke web browser dengan HTTP response message.**

#### **RESTful API**
- REST (Representational State Transfer) adalah gaya arsitektur design untuk menyediakan standar antara sistem komputer di web dan membuat web service.
- Rules REST
  - Uniform Interface
  - Client Server
  - Stateless
  - Cacheable 
  - layered system
  - code on demand

 - RESTful API adalah API yang menggunakan rules milik REST


- HTTP Verbs adalah request untuk berinteraksi dengan resource pada REST System
  - GET
  - POST
  - PUT
  - DELETE


- Header dan Accept Parameters
  - Image - image/png, image/jpeg, image/gif
  - Audio - audio/wav, audio/mpeg - Video - video/mp4, video/ogg
  - Audio - audio/wav, audio/mpeg - Video - video/mp4, video/ogg
  - Application - application/json, application/pdf, application/xml, application/octet-stream
  - 
 
- Path adalah request yang mengandung path pada resource
   - skilvulstore.com/customers/223/orders/12 

- Response Code adalah sebuah response dari konfirmasi web
   - skilvulstore.com/customers/223/orders/12 
   - Macam - macam response codes : - 200 (OK) - 201 (CREATED) - 204 (NO CONTENT) - 400 (BAD REQUEST) - 403 (FORBIDDEN) - 404 (NOT FOUND) - 500 (INTERNAL SERVER ERROR) Response codes sesuai HTTP verb : - GET - 200 (OK) - POST - 201 (CREATED) - PUT - 200 (OK) - DELETE - 204 (NO CONTENT)


## Day 2 : Intro Node.Js
**Selasa, 25 Oktober 2022**

#### **Intro Node.Js**
- **Node.Js** adalah sebuah runtime JavaScript yang berjalan pada V8. Node.Js bisa bejalan sebagai backend atau server side.

- **Fitur Node.js**
  - file system
  - http/https
  - Read Evak Print Loop
  - Console

- **Install Node.Js**  
    https://nodejs.org/en/

- **Build In Module Node.js**
    -  console
        ```
        console.log("Hello world");
         ```
         
    -  Process
         ```
        require("dotenv").config();
        process.env.TOKEN_KEY = 'kf-token'
        console.log(process.env.CLIENT_URL)
         ```
         
    -  OS
         ```
        const os = require('os')
        console.log(os.version())
        console.log(os.release())
        console.log(os.networkInterfaces())
         ```
         
    - Util
         ```
        const os = require('os')
        console.log(os.version())
        console.log(os.release())
        console.log(os.networkInterfaces())
        ```
        
    - Event
         ```
        const EventEmitter = require("events");
        const event = new EventEmitter();
        event.on("connected", (params) => {
          console.log("user connect", params.username);
        });
        event.emit("connected", {
          username: "irfan",
        });
        ```
        
    - fs
         ```
        const fs = require("fs");
        fs.readFile("process.js", (err, data) => {
          console.log(data.toString());
        });
        ```

- **Web Server dengan Node.js**    
  ```
    const http = require("http");
    http.createServer((req, res) => {
        res.write("haii");
        res.end();
      }).listen(8000, () => {
        console.log("http://localhost:8000");
      });
    ```

## Day 3 : Express JS
**Rabu, 26 Oktober 2022**

#### **Express JS**
- **Express Js** package Node JS yang dapat membuat aplikasi web dan membuat HTTP REST API.

- **Installasi**
    ```
    npm init
    npm install express
    
    - nodemon
        npm install nodemon
    ```

- **Routes adalah sebuah jalur endpoint yang dapat diakses menggunakan URL website**
     ```
    app.get('/', (req, res) => {
        res.send('Hello World')
    })
    ```
- **Method adalah sebuah perilaku terhadap data ke server**
    - POST
    - PUT
    - PATCH
    - DELETE
    
- **Query adalah parameter yang digunakan untuk menspesifikasi router**
    ```
    https://localhost:3000/hello/irfan/21
    ```

#### **Middleware** 
- **Middleware** adalah fungsi untuk mengakses ke object request(req), response(res),next dalam request-response cycle.

- **Middleware : memodifikasi Object Request dan Object Response**
    ```
    const express = require('express')
    const app = express()
    const addRequestTime = function (req, res, next) => {
        req.requestTime = Date.now()
        next()
    }
    app.use(addRequestTime)
    app.get('/', function (req, res) {
        let responseText = 'Hello World<br>'
        responseText += '<small>Requested at: ' + req.requestTime + '</small>'
        res.send(responseText)
    })
    app.listen(3000)
    ```
- **Middleware : menghentikan Request-Response cycle **
    ```
    const express = require('express')
    const app = express()
    const stopHere = function (req, res, next) => {
        res.send("<p>request stop from middleware</p>")
    }
    app.use(stopHere)
    app.get('/', function (req, res) {
        let responseText = 'Hello Skilvul!'
        res.send(responseText)
    })
    app.listen(3000)
    ```
- **cara penggunaaan**
    - Application Level Middleware
        ```
        const addRequestTime = funtion (req, res, next) {
        req.requestTime = Date.now()
        next()
        }
        app.user(addRequestTime)
        ```
    - Router Level Middleware
        ```
        const express = require('express')
        const UserRouter = express.Router()
        const AdminRouter = express.Router()
        const logUserAction = function(req, res, next) {
        const username = req.body.username
        console.log(`username ${username} access the API`)
        next()
        }
        userRouter.use(logUserAction)
        UserRouter.get('/users', function(req, res) {
        res.send('all user data')
        })
        AdminRouter.get('/admins', function(req, res) {
            res.send('all admin data')
        })
        ```
        
        - Application Level Middleware
        ```
        const express = require('express')
        const app = express()

        const errorHandling = function(err, req, res, next) {
          console.error(err.stack)
        res.status(500).send('Something broke')
        }

        app.use(errorHandling)
        ```
## Day 4 & 5 : Design Database
**Kamis & JUmat, 27 & 28 Oktober 2022**

#### **Design Database dengan MySQL**
- **MySQL** adalah manajemen database relasional (RDBMS) berbasis SQL.

- **Entity** adalah sebuah tempat yang mengidentifikasi sebuah data.
    - User
    - Film
    - Genre
    
- **Atribute** adalah karakteristik dari sebuah object data.

    ```
    User
    id int NOT NULL
    name varchar(255)
    email varchar(255)
    password varchar(255)
    
    Film
    id int NOT NULL
    name varchar(255)
    release_date date
    
    Genre
    id int NOT NULL
    name varchar(255)
    ```
- **Relasi** adalah hubungan antar tabel.
        - User & Film (Many to Many)
        - Film & Genre (Many to Many)
        - 
        ```
        User
        id int NOT NULL
        name varchar(255)
        email varchar(255)
        password varchar(255)
        
        UserFilmFavorite
        id int NOT NULL
        userId int
        filmId int

        Film
        id int NOT NULL
        name varchar(255)
        release_date date
        
        FilmGenre
        id int NOT NULL
        filmId int
        genreId int
        
        Genre
        id int NOT NULL
        name varchar(255)
        ```