# Skaters E-Commerce System Sequence Diagram

```plantuml
@startuml Skaters System Sequence Diagram
actor User
participant System

User -> System: Browse Products
System --> User: Display Product Catalog

User -> System: Select Product
System --> User: Show Product Details

User -> System: Add to Cart
System --> User: Update Cart

User -> System: Proceed to Checkout
System --> User: Request Shipping Information

User -> System: Provide Shipping Details
System --> User: Request Payment Information

User -> System: Submit Payment Details
System -> System: Process Payment

alt Payment Successful
    System --> User: Display Order Confirmation
    System -> System: Generate Invoice
    System --> User: Send Order Confirmation Email
else Payment Failed
    System --> User: Display Payment Error
    System --> User: Request Different Payment Method
end

User -> System: View Order History
System --> User: Display Orders List

User -> System: Select Order
System --> User: Show Order Details

@enduml
```

This System Sequence Diagram focuses on the interactions between a User and the Skaters E-commerce System during a typical shopping flow, from browsing products to completing a purchase and viewing order details.
