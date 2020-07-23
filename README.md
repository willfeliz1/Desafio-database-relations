<h1 align="center">
  Desafio GoStack #09
</h1>
<h1 align="center">
  <img src="https://ik.imagekit.io/l4en7xyqq3/68747470733a2f2f73746f726167652e676f6f676c65617069732e636f6d2f676f6c64656e2d77696e642f626f6f7463616d702d676f737461636b2f6865616465722d6465736166696f732e706e67_u7F4RKLkz.png">
</h1>

## 📕 About

The main objective of this challenge is to allow the creation of customers, products and orders, where the customer can generate new purchase orders for certain products.

## ⚡ Techs

* [Node.js] - evented I/O for the backend
* [Express] - fast node.js network app framework
* [Typescript] - typed superset of JavaScript that compiles to plain JavaScript.
* [TypeORM] - an ORM that can run in Nodej, browser, Cordova, PhoneGap, Ionic, React Native, NativeScript, Expo, and Electron platforms and can be used with TypeScript and JavaScript
* [Yarn] - package manager that doubles down as project manager.
* [Tsyringe] - A lightweight dependency injection container for TypeScript/JavaScript for constructor injection.
* [DotEnv] - A module that loads environment variables from a .env file. 

## 💻 Installation

### Docker

With docker hub installed, follow the commands:

```sh

$ docker run --name postgres -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgrees

$ docker start postgres

```
### Start server

Install dependencies and start the server.

```sh

$ yarn
$ yarn typeorm migrations:run
$ yarn dev:server

```

### Routes 

- **`POST /customers`**: This route must receive `name` and `email` inside body of request.
- **`POST /products`**: This route must receive `name`, `price` e `quantity` inside body of request.
- **`POST /orders`**: This route must receive in inside body of request the `customer_id` e an array of products, containing the `id` and `quantity` that you want to add
to a new order.


## If you want to see the unit testing 😊

Before running the tests, create a database with the name "gostack_desafio09_tests" so that all tests can run correctly

```sh

$ yarn test

```
### what he expects

```
📌 should be able to create a new customer
📌 should not be able to create a customer with one e-mail thats already registered
📌 should be able to create a new product
📌 should not be able to create a duplicated product
📌 should be able to create a new order
📌 should not be able to create an order with a invalid customer
📌 should not be able to create an order with invalid products
📌 should not be able to create an order with products with insufficient quantities
📌 should be able to subtract an product total quantity when it is ordered
📌 should be able to list one specific order

```



[node.js]: <http://nodejs.org>
[express]: <http://expressjs.com>
[typescript]: <https://www.typescriptlang.org/>
[typeORM]: <https://typeorm.io/#/>
[Yarn]: <https://yarnpkg.com/>
[Tsyringe]: <https://github.com/microsoft/tsyringe>
[DotEnv]: <https://www.npmjs.com/package/dotenv>
