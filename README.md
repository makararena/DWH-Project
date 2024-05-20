## Chain of Stores Database Schema

This project involves creating a database schema for a chain of stores selling various goods, primarily electronics. The schema includes ER diagrams created according to Inmon, Kimball, Data Vault 2.0, and Anchor Modeling methodologies. For Anchor Modeling, only 3 entities were included to maintain diagram readability. The diagrams were created using the Vertabelo application.

### Entities

The schema consists of the following 8 entities:

1. **Account**
    - Contains information about user accounts for the online store.
    - **Attributes**:
        - `Username`: Username of the account holder
        - `Worker_ID`: Related employee identifier
        - `Mail`: Email address of the account holder
        - `Expiration_Date`: Account expiration date

2. **Product**
    - Describes the products available for sale in the store.
    - **Attributes**:
        - `ID`: Unique identifier for the product
        - `Name`: Name of the product
        - `Description`: Description of the product
        - `Category`: Category of the product
        - `Price_USD`: Price of the product
        - `Qty_Availablity`: Quantity available in stock
        - `Qty_Sold`: Quantity sold

3. **Purchase**
    - Contains information about purchases made by users.
    - **Attributes**:
        - `ID`: Unique identifier for the purchase
        - `Sell_Date`: Date of sale
        - `Items_Number`: Quantity of items purchased
        - `Shop_ID`: Store identifier where the purchase was made
        - `Сustomer_ID`: Identifier of the customer who made the purchase

4. **Retailer**
    - Contains information about retail companies providing goods for sale in the store.
    - **Attributes**:
        - `Name`: Name of the retail company
        - `Description`: Description of the retail company
        - `Link`: Link to the company's website
        - `Contact_Number`: Contact number of the company
        - `Address_Longitude`: Location longitude of the company
        - `Address_Latitude`: Location latitude of the company

5. **Shop**
    - Describes the stores where purchases can be made.
    - **Attributes**:
        - `ID`: Unique identifier for the shop
        - `Retailer_Name`: Name of the retail company
        - `Openness`: Open/closed status of the shop
        - `Name`: Name of the shop
        - `Address_Longitude`: Location longitude of the shop
        - `Address_Latitude`: Location latitude of the shop

6. **Task**
    - Contains information about tasks that need to be completed.
    - **Attributes**:
        - `ID`: Unique identifier for the task
        - `Task_Description`: Description of the task
        - `Importance`: Importance level of the task
        - `Complexity`: Complexity level of the task
        - `Start_Date`: Start date of the task
        - `End_Date`: Completion date of the task

7. **Worker**
    - Contains information about store employees.
    - **Attributes**:
        - `ID`: Unique identifier for the worker
        - `Shop_ID`: Identifier of the shop where the worker is employed
        - `Full_Name`: Full name of the worker
        - `Date_Of_Birth`: Date of birth of the worker
        - `Position_Name`: Job title of the worker
        - `Year_Salary_USD`: Annual salary of the worker
        - `Start_Date`: Employment start date
        - `End_Date`: Employment end date

8. **Customer**
    - Describes the store's customers.
    - **Attributes**:
        - `ID`: Unique identifier for the customer
        - `Full_Name`: Full name of the customer
        - `Address_Longitude`: Location longitude of the customer
        - `Address_Latitude`: Location latitude of the customer
        - `Date_Of_Birth`: Date of birth of the customer
