# Software Requirements Specification

## Glossary

### General Glossary
| Term | Definition |
| ---- | ---------- |
| Cart |
| Checkout |
| Catalog | 
| Credit Card |
| Customer |
| Dispatch System |
| Order |
| OTP  |
| ISBN |
| User |


## Functional Requirements

The basic functional requirements are:

| ID       | Description  | Module  | 
| -------- |:------------ | :------- | 
|  RF_1    | System shall allow the customer to register. | Registration/Login | 
|  RF_2    | System shall use the customer’s email address as the username for logon purposes. | Registration/Login |
|  RF_3    | System shall require the customer to set multiple authentication factors (password and OTP). | Registration/Login |
|  RF_4    | System shall shall collect customer information consisting of name, address, email address, phone number, credit card information. | Registration/Login | 
|  RF_5    | System shall allow  the customer to view and edit its customer information. | Registration/Login | 
|  RF_6    | System shall authenticate costumers with password to viewing outstanding orders, viewing customer information and write feedback for a book. | Registration/Login | 
|  RF_7    | System shall authenticate costumers with OTP to making payment or edit customer information. | Registration/Login | 
|  RF_8    | System shall display a list of all books of store to users. | Book Details | 
|  RF_9    | System shall organise the list of books by category. | Book Details | 
|  RF_10   | System shall display detailed book description consisting of ISBN, name, author, publisher, cover image, summary, price to users. | Book Details | 
|  RF_11   | System shall display book's feedbacks to users. | Book Details | 
|  RF_12   | System shall accept all major credit cards. | Payment | 
|  RF_13   | System shall validate payment with the credit card processing company. | Payment | 
|  RF_14   | System shall allow the customer to choose payment method: credit cards or cash on delivery. | User Interface | 
|  RF_15   | System shall allow the customer to place items into cart. | User Interface | 
|  RF_16   | System shall allow the customer to remove items from cart. | User Interface | 
|  RF_17   | System shall allow the customer to checkcout cart. | User Interface | 
|  RF_18   | System shall allow the dispatch department to view all orders. | Orders |
|  RF_19   | System shall allow customers to view their order history. | Orders |
|  RF_20   | System shall allow the dispatch department to view all orders. | Orders |
|  RF_21   | System shall allow the administrator to add books to catalog | Stock Managament |
|  RF_22   | System shall allow the administrator to delete books from catalog | Stock Management |
|  RF_23   | System shall display quantity of book in stock. | Stock Management |
|  RF_24   | System shall allow the administrator to update stock | Stock Management |
|  RF_25   | System shall track information about orders | Delivery&Tracking |
|  RF_26   | System shall display track information about customer order. | Delivery&Tracking |
|  RF_27   | System shall allow the dispatch department to update state of order. | Orders |

## Not-Functional Requirements

The basic not-function requirements are:

| ID       |Description  | Type |
| --------|:-------------| ---- |
|  NF_1   | System shall use a browser as its user interface. | ComplianceTo-Standards |
|  NF_2   | System shall collect costumer information in according to GPDR | ComplianceTo-Standards |
|  NF_3   | System shall store sales transaction data. | Availability |
