# LittleLemonAPI
API system for a restaurant
### Restaurant Management System API
This is a Django Rest Framework based API project for a restaurant management system. The API provides the functionality for managing categories, menu items, carts, orders, and user groups.

## Requirements

- Python 3.6+
- Django 3.0+
- Django Rest Framework 3.0+

## Installation

- Clone the repository
- Install the required packages with pip install -r requirements.txt
- Run python manage.py migrate to apply database migrations
- Run python manage.py runserver to start the server

# Usage

# Categories
- GET /categories/: Get all categories
- POST /categories/: Create a new category (admin only)

# Menu Items

- GET /menuitems/: Get all menu items
- POST /menuitems/: Create a new menu item (admin only)
- GET /menuitems/{id}/: Get a specific menu item by ID
- PUT /menuitems/{id}/: Update a specific menu item by ID (admin only)
- DELETE /menuitems/{id}/: Delete a specific menu item by ID (admin only)

# Cart

- GET /cart/: Get the cart items of the current user
- POST /cart/: Add an item to the cart of the current user
- DELETE /cart/: Remove all items from the cart of the current user

# Order
- GET /orders/: Get all orders of the current user (customer) or all orders (admin)
- POST /orders/: Create a new order
- GET /orders/{id}/: Get a specific order by ID
- PUT /orders/{id}/: Update a specific order by ID (manager or delivery crew only)

# User Groups

- GET /groups/: Get all users in the "Manager" group (admin only)
- POST /groups/: Add a user to the "Manager" group (admin only)
- DELETE /groups/: Remove a user from the "Manager" group (admin only)

# Permissions
- IsAuthenticated: Only authenticated users can access the resource.
- IsAdminUser: Only admin users can access the resource.
