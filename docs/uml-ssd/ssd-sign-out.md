# Sign Out - System Sequence Diagram

```plantuml
@startuml Sign Out - System Sequence Diagram

actor Customer
participant System

Customer -> System: Click Sign Out Button
System -> System: Validate User Session

System -> System: Invalidate Session Token
System -> System: Clear Authentication Cookies
System -> System: Clear User Context

System --> Customer: Redirect to Homepage
System --> Customer: Display Signed Out State

@enduml
```

This System Sequence Diagram illustrates the interaction between a Customer and the System during the sign-out process.
