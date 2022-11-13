
# Writing-and-Presentation-Test week 8
## Day 1 : Sequelize
**Senin, 7November 2022**
#### **Sequelize**
- **Sequelize** ORM (Object Relational Mapping) Node JS yang berbasis promise.
- **Perintah-perintah di Sequelize**
    - Install Sequielize-cli 
        ``
        npm install -g sequelize-cli
        ``
    - Install driver mysql
        ``
        npm install save mysql2
        ``
    - Sequelize init
        ``
        npx sequelize-cli init
        ``
    - Generate Model
        ``
        npx sequelize model:create --name User --attributes name:string,email:string,password:string
        ``
    - Generate Model Database
        ``
        npx sequelize db:migrate
        ``
    - Generate Model Database
        ``
        npx sequelize db:migrate:undo
        ``
    - Generate Seed, Seed adalah data awal yang digunakan untuk mengisi database
        ``
        npx sequelize seed:create --name demo-user
        ``
        
    ``
        module.exports = {
        async up (queryInterface, Sequelize) {
    
         await queryInterface.bulkInsert("Users", [
          {
            name: "Auzan",
            email: "auzan@gmail.com",
            password: "123",
            createdAt: new Date(),
            updatedAt: new Date(),
          },
          {
            name: "Bravo",
            email: "braov@gmail.com",
            password: "123",
            createdAt: new Date(),
            updatedAt: new Date(),
          },
          {
            name: "Charlie",
            email: "chalie@gmail.com",
            password: "123",
            createdAt: new Date(),
            updatedAt: new Date(),
          },
        ]);
        },
        async down (queryInterface, Sequelize) {
        }
        };
    ``
        
        ``
        npx sequelize-cli db:seed:all
        ``
## Day 2 : MongoDB
**Selasa, 8 November 2022**
#### **MongoDB**
- **MongoDB** adalah database open source berbasis NoSQL dan menggunakan struktur data JSON untuk menyimpan data.
- **NoSQL** adalah singkatan dari Not Only SQL. Database management system yang bersifat tanpa relasi (non-relational). NoSQL mengelola database dengan skema yang flexsibel dan tidak membutuhkan query yang komplek.
- **Anatomi Database MongoDB**
    - Database adaalah wadah untuk menyimpan collection.
    - Colletion adalah tempat kumpulan berbagai macam document, collection mirip dengan tabel.
    - Document adalah data yang disimpan dalam collection
- **Installasi MongoDB**
    - **Download** [MongoDB Server](https://www.mongodb.com/try/download/community) beserta [MongoDB Compass](https://www.mongodb.com/try/download/compass).
- **Perintah di MongoDB**
    -  buat dan gunakan database
        ``
        Use sekolah
        ``
    -  meihat daftar database
        ``
        show dbs
        ``
    -  menambahkan collection
        ``
        db.createCollection("siswa")
        ``
    -  menambahkan data di collection
        ``
        db.siswa.insertOne({nama : "irfan",umur : 17, address : "jalanin aja"})
        ``
- **Desain Skema MongoDB**
    - Embedding
    - Referencing
## Day 3 : Mongoose
**Selasa, 8 November 2022**
#### **Mongoose**
- **Mongoose** adalah library Object Modelling MongoDB pada NodeJS.
- **Installasi Mongoose**
    ``
    npm install mongoose
    ``
- **Buat koneksi Mongoose**
    ``
    npm install mongoose
    ``
    ``
    const mongoose = require("mongoose");
    const DB_URL = "mongodb://localhost:27017/sekolahku"
    const db = mongoose.connect(DB_URL);
    module.exports = db;
    ``
- **Buat koneksi Mongoose**
    ``
    const mongoose = require("mongoose");
    const DB_URL = "mongodb://localhost:27017/sekolahku"
    const db = mongoose.connect(DB_URL);
    module.exports = db;
    ``
- **Skema Mongoose**
    ``
    const mongoose = require("mongoose");
    const DB_URL = "mongodb://localhost:27017/sekolahku"
    const db = mongoose.connect(DB_URL);
    module.exports = db;
    ``
    ``
    mongoose = require("mongoose");
        const { Schema } = mongoose;
        const userSchema = new Schema({
          // name: String,
          email: {
            type: String,
            require: true,
              },
              password: String,
              address: {
                name: String,
                no: Number,
                kecamatan: String,
                },
                });
        const User = mongoose.model("User", userSchema);
        ``
- **Populate** adalah proses penggabungan 2 collection menjadi objek JSON.

## Day 4 : Docker
**Kamis, 11 November 2022**
#### **Mongoose**
- **Docker** adalah aplikasi yang menjalankan suatu aplikasi di dalam container.
- **Docker Fundamental**
    - Docker file : Blueprint untuk membuat image.
    - Image : Template untuk menjalankan container.
    - Container : perwujudan dari image.
    - Docker resgistry : tempat untuk upload/download image

- **Perintah Docker**
    - Docker Pull : Download image dari docker hub.
        ``
        docker pull chuanwen/cowsay
        ``
    - Docker Image : Melihat kumpulan images yang sudah terdownload
         ``
        docker pull image
        ``
     - Docker run : Menjalankan container
         ``
        docker run chuanwen/cowsay
        ``
    - Docker ps : Melhat container yang berjalan
         ``
        docker ps
        ``
