
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