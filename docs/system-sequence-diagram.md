# Skaters E-Commerce System Sequence Diagram

```plantuml
@startuml Skaters E-Commerce System Sequence Diagram

actor User
participant System

== Authentication ==

group Sign In
    User -> System: Click Sign In
    User -> System: Choose Authentication Provider (Google)
    System -> System: Redirect to OAuth Provider
    System --> User: Display Sign In Form
    User -> System: Provide Credentials
    System -> System: Validate Credentials
    System --> User: Authentication Success/Failure
end

== Product Browsing ==

group Browse Products
    User -> System: Access Homepage
    System --> User: Display Products, Categories, Featured Items
    User -> System: Filter by Category
    System --> User: Update Product List Based on Category
    User -> System: Search Products
    System --> User: Display Search Results
    User -> System: Scroll for More Products
    System --> User: Load Additional Products (Infinite Scroll)
end

== Shopping Cart Management ==

group Add to Cart
    User -> System: View Product Details
    System --> User: Display Product Information
    User -> System: Add to Cart
    System -> System: Update Cart in Local Storage
    System --> User: Display Cart Updated Notification
end

group Manage Cart
    User -> System: Open Cart
    System --> User: Display Cart Items
    User -> System: Update Quantity
    System -> System: Recalculate Cart Totals
    System --> User: Update Cart Display
    User -> System: Remove Item
    System -> System: Remove Item from Local Storage
    System --> User: Update Cart Display
end

== Checkout Flow ==

group Checkout Process
    User -> System: Initiate Checkout
    System --> User: Display Checkout Form
    User -> System: Submit Order Details
    System -> System: Validate Order Details
    System -> System: Process Payment
    System --> User: Display Payment Status
    System -> System: Generate Invoice
    System -> System: Send Order Confirmation
    System --> User: Display Order Confirmation
end

== Order Management ==

group View Orders
    User -> System: Access Order History
    System --> User: Display List of Orders
    User -> System: Select Order
    System --> User: Display Order Details
    User -> System: Track Order Status
    System --> User: Display Current Order Status
end

@enduml
```

## System Sequence Diagram Description

This System Sequence Diagram (SSD) shows the interactions between a User and the Skaters E-Commerce System. It illustrates the main user flows in chronological order:

### Authentication Flow
Shows how users sign in to the platform using Google OAuth authentication.

### Product Browsing Flow
Demonstrates how users browse products, including filtering by categories, searching, and infinite scrolling for more products.

### Shopping Cart Management Flow
Illustrates the process of adding items to the cart and managing cart items (updating quantities, removing items).

### Checkout Flow
Shows the complete checkout process from initiating checkout to receiving order confirmation.

### Order Management Flow
Demonstrates how users view their order history and track the status of specific orders.

The diagram focuses on the direct interactions between the user and the system without showing internal system components or database interactions. This high-level view helps understand the main user interactions with the system.
