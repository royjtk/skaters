# Skaters E-Commerce Use Case Diagram

```plantuml
@startuml Skaters Use Case Diagram
left to right direction
skinparam packageStyle rectangle

actor Customer
actor StoreOwner

rectangle "Skaters E-Commerce System" {
  usecase "Browse Products" as UC1
  usecase "Search Products" as UC2
  usecase "Filter by Category" as UC3
  usecase "Add to Cart" as UC4
  usecase "Checkout" as UC5
  usecase "Track Orders" as UC6
  usecase "Create Store" as UC7
  usecase "Manage Products" as UC8
  usecase "View Store Orders" as UC9
  usecase "Authenticate" as UC10
}

Customer --> UC1
Customer --> UC2
Customer --> UC3
Customer --> UC4
Customer --> UC5
Customer --> UC6
Customer --> UC10

StoreOwner --> UC7
StoreOwner --> UC8
StoreOwner --> UC9
StoreOwner --> UC10

@enduml
```

This Use Case Diagram presents a focused view of the core functionalities in the Skaters e-commerce platform. It identifies two primary actors (Customer and Store Owner) and their interactions with the system's key features.
