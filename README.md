# online-retail-application-database

Here's a summary of your eCommerce database schema along with the key points and keys involved in each table:

### Summary of eCommerce Database Schema

1. **Database Name**: `ecommerces_db`
   
2. **Tables**:
   - **Users**
     - **Purpose**: Stores user information.
     - **Key Fields**:
       - `user_id`: Primary Key (auto-incremented)
       - `email`: Unique identifier for user login

   - **Products**
     - **Purpose**: Contains product details.
     - **Key Fields**:
       - `product_id`: Primary Key (auto-incremented)
       - `price`: Defines the cost of the product

   - **Orders**
     - **Purpose**: Records orders placed by users.
     - **Key Fields**:
       - `order_id`: Primary Key (auto-incremented)
       - `user_id`: Foreign Key referencing `Users(user_id)`

   - **OrderItems**
     - **Purpose**: Links products to specific orders.
     - **Key Fields**:
       - `order_item_id`: Primary Key (auto-incremented)
       - `order_id`: Foreign Key referencing `Orders(order_id)`
       - `product_id`: Foreign Key referencing `Products(product_id)`

   - **Payments**
     - **Purpose**: Manages payment details for orders.
     - **Key Fields**:
       - `payment_id`: Primary Key (auto-incremented)
       - `order_id`: Foreign Key referencing `Orders(order_id)`

### Key Points

- **Relationships**: 
  - Users can have multiple orders (one-to-many).
  - Orders can contain multiple items (one-to-many).
  - Each order item references a specific product (many-to-one).

- **Data Integrity**: Foreign keys ensure that related data across tables remains consistent.

- **Timestamps**: Most tables include a `created_at` timestamp to track when records are created.

- **Security Considerations**: User passwords should be hashed for security.

### Keys Summary

- **Primary Keys**:
  - `Users`: `user_id`
  - `Products`: `product_id`
  - `Orders`: `order_id`
  - `OrderItems`: `order_item_id`
  - `Payments`: `payment_id`

- **Foreign Keys**:
  - `Orders`: `user_id` references `Users(user_id)`
  - `OrderItems`: `order_id` references `Orders(order_id)`, `product_id` references `Products(product_id)`
  - `Payments`: `order_id` references `Orders(order_id)`

This structure provides a solid foundation for managing users, products, orders, order items, and payments within your eCommerce application. If you need further details or assistance, feel free to ask!

![Screenshot 2024-10-25 160046](https://github.com/user-attachments/assets/2f3bcd69-fea1-4d67-b75a-8b6241ae0ab9)
![Screenshot 2024-10-25 160106](https://github.com/user-attachments/assets/cdc3c021-427c-424e-bf2a-9df33936e8a8)
![Screenshot 2024-10-25 160125](https://github.com/user-attachments/assets/40b4983e-5ed0-4069-ac1f-1f15d1b9c3a8)
![Screenshot 2024-10-25 160140](https://github.com/user-attachments/assets/39070e7d-d233-4807-b31e-4fa203ca6911)
![Screenshot 2024-10-25 160203](https://github.com/user-attachments/assets/e7d8589a-121e-48f0-b9d2-f46496df88b2)

