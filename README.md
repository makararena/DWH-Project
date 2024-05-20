## Chain of Stores Database Schema

This project involves creating a database schema for a chain of stores selling various goods, primarily electronics. The schema includes ER diagrams created according to Inmon, Kimball, Data Vault 2.0, and Anchor Modeling methodologies. For Anchor Modeling, only 3 entities were included to maintain diagram readability. The diagrams were created using the Vertabelo application.

### Entities

The schema consists of the following 8 entities:

1. **Account**
    - Contains information about user accounts for the online store.
    - **Attributes**:
        - `username`: Username of the account holder
        - `employee_id`: Related employee identifier
        - `email`: Email address of the account holder
        - `expiration_date`: Account expiration date

2. **Product**
    - Describes the products available for sale in the store.
    - **Attributes**:
        - `product_id`: Unique identifier for the product
        - `name`: Name of the product
        - `description`: Description of the product
        - `category`: Category of the product
        - `price`: Price of the product
        - `available_quantity`: Quantity available in stock
        - `quantity_sold`: Quantity sold

3. **Purchase**
    - Contains information about purchases made by users.
    - **Attributes**:
        - `purchase_id`: Unique identifier for the purchase
        - `sale_date`: Date of sale
        - `quantity`: Quantity of items purchased
        - `store_id`: Store identifier where the purchase was made
        - `customer_id`: Identifier of the customer who made the purchase

4. **Retailer**
    - Contains information about retail companies providing goods for sale in the store.
    - **Attributes**:
        - `name`: Name of the retail company
        - `description`: Description of the retail company
        - `website`: Link to the company's website
        - `contact_number`: Contact number of the company
        - `location`: Location coordinates of the company

5. **Shop**
    - Describes the stores where purchases can be made.
    - **Attributes**:
        - `shop_id`: Unique identifier for the shop
        - `retailer_name`: Name of the retail company
        - `status`: Open/closed status of the shop
        - `shop_name`: Name of the shop
        - `short_name`: Short name of the shop
        - `location`: Location coordinates of the shop

6. **Task**
    - Contains information about tasks that need to be completed.
    - **Attributes**:
        - `task_id`: Unique identifier for the task
        - `description`: Description of the task
        - `importance`: Importance level of the task
        - `complexity`: Complexity level of the task
        - `start_date`: Start date of the task
        - `completion_date`: Completion date of the task

7. **Worker**
    - Contains information about store employees.
    - **Attributes**:
        - `worker_id`: Unique identifier for the worker
        - `shop_id`: Identifier of the shop where the worker is employed
        - `full_name`: Full name of the worker
        - `date_of_birth`: Date of birth of the worker
        - `job_title`: Job title of the worker
        - `annual_salary`: Annual salary of the worker
        - `start_date`: Employment start date
        - `end_date`: Employment end date

8. **Customer**
    - Describes the store's customers.
    - **Attributes**:
        - `customer_id`: Unique identifier for the customer
        - `full_name`: Full name of the customer
        - `location`: Location coordinates of the customer
