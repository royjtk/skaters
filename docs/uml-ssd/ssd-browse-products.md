# Browse Products - System Sequence Diagram

```plantuml
@startuml Browse Products - System Sequence Diagram

actor Customer
participant System

Customer -> System: Access Homepage
System -> System: Fetch Featured Products
System -> System: Fetch Categories
System --> Customer: Display Homepage with Products

Customer -> System: Scroll Down for More Products
System -> System: Fetch Additional Products
System --> Customer: Display More Products (Infinite Scroll)

Customer -> System: Click on Category
System -> System: Filter Products by Category
System --> Customer: Display Filtered Products

@enduml
```

This System Sequence Diagram shows the interactions between a Customer and the System when browsing products, including the infinite scroll feature and category filtering.
