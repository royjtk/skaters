# Skaters E-Commerce Class Diagram

```plantuml
@startuml Skaters Class Diagram
skinparam classAttributeIconSize 0

class User {
  +id: string
  +email: string
  +name: string
  +image: string
  +createdAt: DateTime
  +updatedAt: DateTime
}

class Store {
  +id: string
  +name: string
  +userId: string
  +description: string
  +createdAt: DateTime
  +updatedAt: DateTime
}

class Category {
  +name: string
  +slug: string
}

class Product {
  +id: string
  +storeId: string
  +categoryId: string
  +name: string
  +price: float
  +isFeatured: boolean
  +isArchived: boolean
  +description: string
  +quantity: integer
  +slug: string
  +createdAt: DateTime
  +updatedAt: DateTime
}

class Order {
  +id: string
  +storeId: string
  +isPaid: boolean
  +phone: string
  +address: string
  +status: string
  +createdAt: DateTime
  +updatedAt: DateTime
}

class OrderItem {
  +id: string
  +orderId: string
  +productId: string
  +storeId: string
  +createdAt: DateTime
  +updatedAt: DateTime
}

class Image {
  +id: string
  +productId: string
  +url: string
  +createdAt: DateTime
  +updatedAt: DateTime
}

User "1" -- "0..*" Store : owns >
Store "1" -- "0..*" Product : sells >
Category "1" -- "0..*" Product : categorizes >
Product "1" -- "0..*" Image : has >
Product "1" -- "0..*" OrderItem : included in >
Order "1" -- "1..*" OrderItem : contains >
Store "1" -- "0..*" Order : receives >

@enduml
```

This Class Diagram illustrates the main entities in the Skaters e-commerce system and their relationships, representing the core data structure of the application.
