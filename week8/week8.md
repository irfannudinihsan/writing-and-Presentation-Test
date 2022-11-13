# Writing-and-Presentation-Test week 8

## Day 1 : Sequelize

**Senin, 7 November 2022**

#### **Sequelize**

- **Sequelize** ORM (Object Relational Mapping) Node JS yang berbasis promise.
- **Perintah-perintah di Sequelize**

  - Install Sequielize-cli
    ` npm install -g sequelize-cli `
  - Install driver mysql
    ` npm install save mysql2 `
  - Sequelize init
    ` npx sequelize-cli init `
  - Generate Model
    ` npx sequelize model:create --name User --attributes name:string,email:string,password:string `
  - Generate Model Database
    ` npx sequelize db:migrate `
  - Generate Model Database
    ` npx sequelize db:migrate:undo `
  - Generate Seed, Seed adalah data awal yang digunakan untuk mengisi database
    ` npx sequelize seed:create --name demo-user `
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

    ` npx sequelize-cli db:seed:all `
