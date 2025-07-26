# Santander Dev Week

RESTful Java API created for Santander Dev Week.

## Class Diagram

```mermaid
classDiagram
    class User {
        - Account account
        - List~Feature~ features
        - Card card
        - List~News~ news
    }

    class Account {
        - String name
        - String agency
        - String accountNumber
        - float balance
        - float accountLimit
    }

    class Feature {
        - String icon
        - String description
    }

    class Card {
        - String number
        - float limit
    }

    class News {
        - String icon
        - String description
    }

    User --> Account
    User --> Feature : features
    User --> Card
    User --> News : news
