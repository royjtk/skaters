# Sign In - System Sequence Diagram

```plantuml
@startuml Sign In - System Sequence Diagram

actor Customer
participant System

Customer -> System: Click "Sign In" Button
System --> Customer: Display Authentication Options

Customer -> System: Select Google Authentication
System -> System: Redirect to Google OAuth
System --> Customer: Display Google Sign In Form

Customer -> System: Input Credentials
System -> System: Authenticate with Google
System -> System: Validate User Account

alt Successful Authentication
    System -> System: Create Session
    System --> Customer: Redirect to Homepage with Signed-in State
else Failed Authentication
    System --> Customer: Display Authentication Error
end

@enduml
```

This System Sequence Diagram illustrates the interaction between a Customer and the System during the sign-in process, specifically using Google OAuth authentication.
