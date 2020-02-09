# Backend Developer Application Challenge

**Mock Shop** is a simple shopping server. You are required to develop the backend API. 
You can fork this git repository and get to work!

**Due Date:** 6 days after Test email receipt (Usually places due date on Friday, at noon).

## Features

- User can Sign Up.
- User can Sign in.
- Admin can add a Product.
- Admin can delete a Product.
- Admin can edit a Product.
- Users/Admin can see all products.
- Users can add product to a Cart.
- A user can see product in his/her cart.
- User can delete a product from his/her cart.

## Tools
- Server side Framework: ***Nodejs/Express***
- Linting: ***ESLint***
- Style Guide: ***Airbnb***
- Testing: ***Mocha Chai***
- DB: ***Postgres***
- Documentation: ***Swagger***
- Hosting: ***Heroku***

## Requirements
1. Make sure your endpoints are well documented with Swagger. This will help evaluators better test your code.
2. Seed the database with enough data to aid in evaluation (i.e. lots of products to work with).
3. You're expected to use `BEARER TOKEN` and `JWT` to handle all authentications and Authorizations.
4. Host code on Github repository, with a well detailed readme.
5. Host the API on a heroku live server.
6. API versioning is expected, for example: `https://exampleapp.com/api/v1`
7. Use appropriate HTTP status codes.


## Stand out
1. Thorough Swagger Documentation.
2. Design a simple user interface with a React framework to comsume the API
3. implement `Sequelize` ORM for postgres.

## Guide
### API Specifications
The API endpoints should respond with a JSON object specifying the HTTP ***status*** code, and either a ***data*** property (on success) or an ***error*** property (on failure).

```javascript
// Sucess
{
  "status": 'success',
  "data": {...}
}

// Failure
{
  "status": 'error',
  "error": 'endpoint-error-message'
}
```

### Data Specifications
These specifications are only a guide to aid in developing the application. You have the freedom to come up with your own specifications, as long as the API functions properly and returns appropriate responses. 

```javascript
// user
{
  "id": INTEGER,
  "firstName": STRING,
  "lastName": STRING,
  "email": STRING,
  "password": STRING,
  "isAdmin": BOOLEAN,
}

// product
{
  "id": INTEGER,
  "name": STRING,
  "description": STRING,
  "category": STRING, // clothes, electronics, book
  "price": FLOAT,
  "imageUrl": STRING,
  "inStock": BOOLEAN,
}

// cart
{
  "id": INTEGER,
  "productId": INTEGER, //association with product.id
  "userId": INTEGER, //association with user.id
}
```
