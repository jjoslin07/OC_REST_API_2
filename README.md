# Can you implement CRUD?
## Evaluated skills

Create a RESTful web API using Node, Express and MongoDB

## Description 

> **In this practical exercise, you will test your new skills by coding a functioning API!**

In order to answer the single question in this quiz, you will be required to code a fully functioning API just like the one we have been creating throughout this course. Your API will also need to be connected to a database, as various CRUD operations will be tested!

You will create a basic API for an online store which allows users to create, read, update and delete products (  `Product`  ) from a database. Each  `Product`  must have the following four fields:

- `name`  : the name of the product, of type String ;
- `description`  : the description of the product, of type String ;
- `price`  : the price of the product, of type Number ;
- `inStock`  : whether the product is in stock or not, of type Boolean.

You will implement five routes:

- GET  `/api/products`
Returns all products in the database as  `{ products: Product[] }`
- GET  `/api/products/:id`
Returns the product with the provided  _id  as  `{ product: Product }`
- POST  `/api/products`
Creates a new product in the database

The request body must contain:
```js
{
  "name": string,
  "description": string,
  "price": number,
  "inStock": boolean
}
```

Returns the new product (including its  `_id`  field) as  `{ product: Product }`

Mongoose's save method returns a Promise which receives the created object:
```js
product.save()
.then(product => ... ... .json({ product })
.catch(error => ...);
```
- PUT  `/api/products/:id`

Updates the product with the provided  `_id`  with the data provided in the request body

The request body must contain:
```js
{
  "name": string,
  "description": string,
  "price": number,
  "inStock": boolean
}
```
Returns the following object:  `{ message: 'Modified!' }`

- DELETE  `/api/products/:id`
Deletes the product with the provided  `_id`
Returns the following object:  `{ message: 'Deleted!' }`

Your API will run on your local machine on  `localhost`  (preferably on port 3000, but the front-end app allows you to modify the port number if need be) and accept HTTP requests from all origins (don't forget your CORS configuration!).

To test your API, you will need to install a small frontend app. Clone [the repo with the frontend code following this link.](https://github.com/OpenClassrooms-Student-Center/fullstack-activity)

From within the cloned directory, run  `npm install`  , followed by  `npm start`  . Your browser should open to this interface:

<div align="center">
  <img src="https://user-images.githubusercontent.com/73438491/124810715-85ae4f80-df16-11eb-9027-df394ec6fc8b.png" alt="front end app" />
  </div>

With your server running, click the `TEST ROUTES` button to run the tests. These tests will allow you to check that you have correctly implemented the required routes and whether you have validated this quiz!  Success or error messages will be displayed as each test is passed or failed to inform you which routes work and which do not.

>**If your web browser shows a 404 error, wait a few seconds and hit refresh.**
>
>**Sometimes, when first running a new instance of the test app, the first test can fail even though your API is running correctly. Click `TEST ROUTES` again; if the error persists, it is likely that there is an issue with your API.**

 

## Question 1
**When all tests pass successfully, a secret word is displayed. Which of the following is that secret word?**

- [ ] GIRAFFE
- [ ] GORILLA
- [ ] ELEPHANT
- [ ] ZEBRA

