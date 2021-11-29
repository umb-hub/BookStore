# Web Services

A Web Service is a system that automatically supports machine-to-machine interactions, facilitating interoperability between heterogeneous systems. The implementation of a system of this type can take place using different architectural styles, including REST,
which is based on the use of HTTP methods, such as GET and POST, uniquely identifying resources through a URI. To define the interface of the reference web service, OpenAPI can be used that is a standard  to define structure and syntax of REST API.

## REST API Inventory

In this project APICUR.IO is been used in order to define REST API, using OpenAPI standard. 

In order to implements differents services of this project, there are 9 endpoints:

- /api/account
- /api/account/card
- /api/book
- /api/cart
- /api/catalog
- /api/checkout
- /api/login
- /api/order
- /api/order/shipping

Let's discuss about them

\newpage

### API /api/login

![Login](./images/API/login.png)

Using this API an user can login using multifactor authentication.

#### 200 OK

![200](./images/API/login_200.png)

User have completed all process login and it obtain an JWT token to authenticate itself.

JWT Token is a signed token that contains public customer information and system signature to avoid crafting of illegal tokens.

![JWT Token](./images/API/login_jwt.png)

This token will be required for all process that require an authentication.

\newpage

#### 307 Temporary Redirect

![307](./images/API/login_307.png)

In this example user have input correct password and system replies sending captcha image to solve.

This method permits to handle multifactor login.

\newpage

### API /api/account

![Account REST](./images/API/account.png)

This endpoint permit different methods for different actions.

#### GET

Customer or administrator can get costumer details accounts. Note that token obtained in login process is required for customer or administrator identification,

![](./images/API/account_get.png)

#### POST

Customer can update its customer details, note that password is not sended in clear but it is hashed in accord to GPDR (NF_2).

![](./images/API/account_post.png)

#### DELETE

Administrator can delete selected costumer account.

![](./images/API/account_delete.png)

\newpage

### API /api/account/card

![Account Card REST](./images/API/account_card.png)

#### GET

Customer can get its credit card info, note that credit card is hidden to itself in order to improve security.

![](./images/API/account_card_get.png)

#### POST

Customer can add a credit card to its account specifing all required parameters.

![](./images/API/account_card_post.png)

#### DELETE

Customer can delete a credit card from its account specifing index.

![](./images/API/account_card_delete.png)

\newpage

### API /api/book

![Book REST](./images/API/book.png)


#### GET

Any user can watch book information using specified query parameter

![](./images/API/book_get.png)

#### POST

Note there is a require parameter **action**, it is used by system to apply different action for different roles.

![](./images/API/book_post.png)

\newpage

### API /api/catalog

![Catalog REST](./images/API/catalog.png)

#### GET/POST

Any user can browse catalog using GET e POST requests to surf on catalog

![](./images/API/catalog_rest.png)

\newpage

### API /api/cart

![Cart REST](./images/API/cart.png)

#### GET/POST

Costumer can watch and manage its cart using GET/POST requests and query parameters.

![](./images/API/cart_rest.png)

\newpage

### API /api/checkout

Customer try to checkout cart using a card selected by index, in response the System will reply *201 Created* if payment is successful else it will reply *400 Bad Request* showing error information to customer.

![Checkout REST](./images/API/checkout.png)

\newpage

### API /api/order

![Order REST](./images/API/order.png)

#### GET

Customer can get its entire order list if id parameter is not specified else it can get informations for a specific order identified by id

![](./images/API/order_get.png)

#### POST

Dispatcher can update order status specifing order id.

![](./images/API/order_post.png)

\newpage

### API /api/order/shipping

![Order Shipping REST](./images/API/order_ship.png)

#### GET

Customer can get list of shipping information associated to orderid required parameter.

![](./images/API/order_ship_get.png)

#### POST

Customer can update list of shipping information associated to orderid required parameter.

![](./images/API/order_ship_post.png)

\newpage

