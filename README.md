# PHP Developer Test (Mid-Level)

## Overview
Welcome to the PHP Developer Test! This test is designed to assess your problem-solving skills and knowledge of PHP, SQL, and API development. The estimated time for completion is **2 hours**.

### **Instructions**
1. **Fork this repository** to your GitHub account.
2. Complete the tasks outlined below.
3. Submit your solutions by **sending the link to your repository to your contact.**.
4. Ensure your code follows **best practices** (clean code, comments, and structure).

---

## **Task 1: Object-Oriented PHP**
Create a simple **"Order Management" system** using PHP classes and **Object-Oriented Programming** principles.

- Create a class `Order` with the following properties:
  - `id` (int, auto-generated)
  - `customerName` (string)
  - `items` (array of product names)
  - `totalPrice` (float)
  - `status` (string: `"pending"`, `"shipped"`, `"delivered"`)
- Add a method `addItem($item, $price)` that adds an item to the order.
- Add a method `changeStatus($status)` to update the order status.
- Create a subclass `ExpressOrder` that allows an **optional express delivery fee** to be added to the total price.
- Write a script (`order_test.php`) to:
  - Create an `Order`, add items, change the status, and print details.
  - Create an `ExpressOrder`, add items, apply an express fee, and print details.

---

## **Task 2: MySQL & PHP**
Write a script (`database.php`) that connects to a **MySQL database**, creates a table, and inserts data.

1. Create a `customers` table with:
   - `id` (int, primary key, auto-increment)
   - `name` (varchar, 100)
   - `email` (varchar, 100, unique)
   - `created_at` (timestamp, default `CURRENT_TIMESTAMP`)
   
2. Insert **three sample customers** into the database.
3. Write a query to **fetch all customers** and print their details.

**Bonus:** Write a function `getCustomerByEmail($email)` that retrieves a customer by email.

---

## **Task 3: API Development**
Create a **simple REST API** (`api.php`) to manage products.

- Implement the following endpoints:
  - `GET /products` → Returns a JSON list of products (array of associative arrays).
  - `POST /products` → Accepts a JSON payload (`name`, `price`) and adds a new product.
  - `GET /products/{id}` → Returns details of a single product.
  
- Use an **array to store products** (no database needed).
- Handle errors (e.g., product not found, invalid data).
- Example usage:
  ```bash
  curl -X GET http://localhost/api.php/products
  curl -X POST -H "Content-Type: application/json" -d '{"name": "Laptop", "price": 1200}' http://localhost/api.php/products
