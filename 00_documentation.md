# ElectroMart -- Project Documentation

## 1. Project Overview

**Project Name:** ElectroMart\
**Project Type:** Electronics E-commerce Website

ElectroMart is an online shopping website for electronic products.
Customers can create an account, log in, view products, add products to
a cart, and place orders. The admin can manage products and customer
orders.

## 2. Project Objectives

-   Build a simple and user-friendly electronics shopping website.
-   Display electronics with names, images, prices, and descriptions.
-   Allow customers to register and log in.
-   Allow customers to add products to a shopping cart.
-   Allow customers to place and view orders.
-   Allow the admin to manage products and orders.
-   Store website information safely in a database.

## 3. Users of the Website

There are two main types of users:

### 3.1 Customer Section

Customers can: - Register for a new account. - Log in and log out. -
View all available electronics. - Search for products. - View product
details. - Add products to the shopping cart. - Update or remove cart
items. - Place an order. - View their order history.

### 3.2 Admin Section

The admin manages the website. The admin can: - Log in to the admin
section. - View the admin dashboard. - Add new products. - Edit product
details. - Delete products. - View customer orders. - Update order
status. - View the list of customers.

## 4. Main Website Pages

  Page              Purpose
  ----------------- ----------------------------------------------------
  Home              Shows the website name and featured products
  Register          Creates a customer account
  Login             Allows an existing customer to log in
  Products          Displays all electronics
  Product Details   Shows information about one product
  Cart              Shows products selected by the customer
  Checkout          Collects order and delivery information
  My Orders         Shows the customer's orders
  Admin Login       Allows the admin to log in
  Admin Dashboard   Shows admin options
  Manage Products   Allows the admin to add, edit, and delete products
  Manage Orders     Allows the admin to view and update orders

## 5. Product Categories

ElectroMart can include these categories:

-   Mobiles
-   Laptops
-   Headphones
-   Keyboards and Mice
-   Monitors
-   Speakers
-   Smart Watches
-   Accessories

Each product should have: - Product ID - Product name - Category -
Description - Price - Image - Available quantity

## 6. Technology We Will Use

We will use beginner-friendly technologies:

  Technology           Use
  -------------------- -------------------------------------------
  HTML                 Creates the structure of web pages
  CSS                  Adds colors, layouts, and styles
  JavaScript           Adds interactions to pages
  PHP                  Handles server-side operations
  MySQL                Stores users, products, carts, and orders
  XAMPP                Runs PHP and MySQL on our laptop
  Visual Studio Code   Used to write and edit code
  GitHub               Stores and tracks our project files

We will learn each technology step by step. We do not need to know
everything before starting.

## 7. Database Plan

The first version of the database may contain these tables:

### 7.1 users

Stores customer account details.

-   user_id (Primary Key)
-   name
-   email
-   password
-   phone
-   address

### 7.2 admins

Stores admin login details.

-   admin_id (Primary Key)
-   username
-   password

### 7.3 categories

Stores product categories.

-   category_id (Primary Key)
-   category_name

### 7.4 products

Stores electronics product details.

-   product_id (Primary Key)
-   category_id (Foreign Key)
-   product_name
-   description
-   price
-   image
-   stock_quantity

### 7.5 cart

Stores each customer's cart information.

-   cart_id (Primary Key)
-   user_id (Foreign Key)
-   created_at

### 7.6 cart_items

Stores products added to a cart.

-   cart_item_id (Primary Key)
-   cart_id (Foreign Key)
-   product_id (Foreign Key)
-   quantity

### 7.7 orders

Stores customer orders.

-   order_id (Primary Key)
-   user_id (Foreign Key)
-   order_date
-   total_amount
-   order_status
-   delivery_address

### 7.8 order_items

Stores the products included in each order.

-   order_item_id (Primary Key)
-   order_id (Foreign Key)
-   product_id (Foreign Key)
-   quantity
-   price_at_purchase

## 8. Project Development Steps

We will build the project in this order:

1.  Install Visual Studio Code and XAMPP.
2.  Create the ElectroMart project folder.
3.  Learn basic HTML and create the home page.
4.  Learn CSS and design the website.
5.  Learn basic JavaScript and add simple interactions.
6.  Create the MySQL database and tables.
7.  Create the customer registration page.
8.  Create the customer login and logout pages.
9.  Display products from the database.
10. Create the product details page.
11. Build the shopping cart.
12. Build the checkout and order pages.
13. Create the admin login page.
14. Build the admin dashboard.
15. Add product and order management.
16. Test the complete website.

## 9. Basic Project Folder Structure

``` text
ElectroMart/
|
|-- index.php
|-- register.php
|-- login.php
|-- logout.php
|-- products.php
|-- product-details.php
|-- cart.php
|-- checkout.php
|-- my-orders.php
|
|-- admin/
|   |-- login.php
|   |-- dashboard.php
|   |-- manage-products.php
|   |-- manage-orders.php
|
|-- css/
|   |-- style.css
|
|-- js/
|   |-- script.js
|
|-- images/
|
|-- includes/
|   |-- db.php
|   |-- header.php
|   |-- footer.php
|
|-- documentation/
    |-- 00_documentation.md
    |-- 01_databaseSetup.md
    |-- 02_registrationPageSetup.md
    |-- 03_loginPageSetup.md
```

This is our planned structure. We will create files gradually as we
learn.

## 10. Important Notes

-   This is the first version of the project plan. We can improve it as
    we build.
-   We will first make the basic website work before adding advanced
    features.
-   We will not store plain-text passwords. Passwords must be securely
    hashed.
-   Database queries must use prepared statements.
-   We will use test data while learning.
-   Online payment integration can be considered later. We will not
    collect real card details in this beginner version.

## 11. Expected Result

At the end, ElectroMart will be a working beginner-level electronics
e-commerce website with:

-   A customer section.
-   An admin section.
-   Product listings and product details.
-   A shopping cart.
-   Customer orders.
-   A MySQL database.
-   A responsive and user-friendly design.
