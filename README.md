# 451proj

# Ecommerce Distributed Database Documentation

## Introduction
This documentation provides a comprehensive guide on creating a distributed heterogeneous database environment. The project involves setting up three different database platforms across multiple sites with varying operating systems. The primary objective is to demonstrate the concepts of fragmentation and reconstruction within this environment.

## Assignment Overview
The assignment required the creation of a distributed heterogeneous database environment that includes:

Three sites
Three different database platforms
At least two different operating systems
This environment was used to showcase fragmentation and reconstruction techniques using a domain area with at least four distributed relations.

## Environment Setup
To establish the environment, the following setup was used:

Host: Windows PC hosting VMware virtual machines
VMs: Two Ubuntu virtual machines
Database Platforms: PostgreSQL, MariaDB, and MySQL
Network Configuration: All computers were placed in a VLAN (192.168.52.0) using a host-only network configuration
Software Details
Windows PC: Running MySQL
Ubuntu VM 1: Running PostgreSQL
Ubuntu VM 2: Running MariaDB

## Domain and Tables
The chosen domain for this project was  Ecommerce looking at an application like Jumia. The main tables used were:

customers: Containing customer information
products: Containing product information
orders: Containing order details
payment: Containing payment information

## Fragmentation Approach
The fragmentation was carried out as follows:

Customers Table:

Horizontally fragmented based on customer country (Nairobi and Mombasa)
Resulted in two tables: customers_nairobi and customers_mombasa
Products Table:

Vertically fragmented based on product category (electronics and clothing)
Resulted in two tables: products_electronics and products_clothing
Orders Table:

Horizontally fragmented based on region
Resulted in multiple tables based on location
Payment Table:

Vertically fragmented based on payment method (PayPal and credit cards)
Resulted in two tables: payment_paypal and payment_creditcards

## Reconstruction Approach
Reconstruction was performed using Python modules to communicate with the databases:

PostgreSQL: Used psycopg2 module
MariaDB and MySQL: Used pymysql module
Techniques Used
Views
Functions
Stored procedures

## Reports Generated
The following reports were generated from the distributed database:

Sales by Payment Method per Region
Customer Order Summary
To show fragmentation,

  * the customer tables was horizontally fragmented based on the customer country in this case Nairobi and Mombasa to create two tables.

  * the products were vertically fragmented based on the product category, in this case electronics and clothing to create two tables. 

  * the orders were horizontally fragmented based on the region to emulate that orders based on their location.

  * the payment was vertically fragmented based on the payment method in this case it was paypal and credit cards.



## Modifications and Improvements
Modifications made during the project include:

Using Python's config module to create a configuration file for database connection information
Cleaning up the logic and removing any stray variables to improve code quality
## Conclusion
This project demonstrated the creation of a distributed heterogeneous database environment and the application of fragmentation and reconstruction techniques. Despite the complexity, it was completed successfully through effective problem-solving skills.
