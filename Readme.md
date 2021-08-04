# E-Commerce infrastructure

This project is about creating a sample infrastructure for an e-commerce use case that demonstrates the use of Micro-services together with event based communication.

## User Stories

1. As a user I want to get a list of products together with the available amounts for each product, so that he can choose from them.

Products marked as reserved are not showing as available.

2. As a user I want to be able to add a product from the list to my cart, so that I can buy them afterwards.

3. As a product storage service I want to be informed when a product is added into a cart, so that I can update the product amount status to RESERVED.

4. As a user I want to be able to buy the products from a cart, so that I'm able to see them I'm my to be delivered list.

Before proceeding to buy a product, check if the product is marked as reserved, and if not - reserve it first.
Only if all products are marked as reserved, we should be able to process the buy. If this is not possible, inform the user about the error.

5. As a product storage service I want to be informed when a product was added to the delivery list, so that I can update the product amount.

6. As a delivery service I want to be informed when a product from a cart is buy, so that I can create a new entry with the products in the delivery list.

7. As a user O want to get a my full delivery list, so that I can see my history.

8. As product storage service I want to restore the status from RESERVED back to AVAILABLE if the status is longer then 10 min, so that I don't keep the products to much time blocked.

## Technical Stack

- Java 11
- Spring Boot
- Kafka
- PostgreSQL
- Docker

## Identified services

1. storage-service
2. cart-service
3. delivery-service
