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

![](./images/API/account_get.png)

#### POST

![](./images/API/account_post.png)

#### DELETE

![](./images/API/account_delete.png)

\newpage

### API /api/account/card

![Account Card REST](./images/API/account_card.png)

#### GET

![](./images/API/account_card_get.png)

#### POST

![](./images/API/account_card_post.png)

#### DELETE

![](./images/API/account_card_delete.png)

\newpage

### API /api/book

![Book REST](./images/API/book.png)


#### GET

![](./images/API/book_get.png)

#### POST

![](./images/API/book_post.png)

\newpage

### API /api/catalog

![Catalog REST](./images/API/catalog.png)


#### GET/POST

![](./images/API/catalog_rest.png)

\newpage

### API /api/cart

![Cart REST](./images/API/cart.png)


#### GET/POST

![](./images/API/cart_rest.png)

\newpage

### API /api/checkout

![Checkout REST](./images/API/checkout.png)

\newpage

### API /api/order

![Order REST](./images/API/order.png)


#### GET

![](./images/API/order_get.png)

#### POST

![](./images/API/order_post.png)

\newpage

### API /api/order/shipping

![Order Shipping REST](./images/API/order_ship.png)


#### GET

![](./images/API/order_ship_get.png)

#### POST

![](./images/API/order_ship_post.png)