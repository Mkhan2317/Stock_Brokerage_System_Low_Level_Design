# Stock_Brokerage_System_Low_Level_Design
# Stock Brokerage System  

This repository contains an implementation of a stock brokerage system, designed to facilitate trading operations, user account management, and order execution. The system is structured using object-oriented principles, incorporating key classes, interfaces, and enumerations to ensure modularity and scalability.  

## **Key Components**  

### **Classes & Interfaces**  

- **User**: Represents a system user with attributes such as user ID, name, and email.  
- **Account**: Represents a user's trading account, managing account ID, associated user, and balance. Includes methods for depositing and withdrawing funds.  
- **Stock**: Represents a tradable stock with properties like symbol, name, and price. Includes a method for updating stock prices.  
- **Order (Abstract Class)**: Base class for user orders, containing attributes like order ID, associated account, stock, quantity, price, and status. Declares an abstract `execute()` method for order execution.  
- **BuyOrder & SellOrder**: Concrete subclasses of `Order`, implementing `execute()` to handle buy and sell transactions.  
- **Portfolio**: Represents a user's portfolio, managing owned stocks with methods for adding and removing stocks.  
- **StockBroker (Singleton Pattern)**: Central component of the system, ensuring a single instance for managing users, accounts, stocks, and order processing. Provides functionalities for account creation, stock management, and order execution.  
- **StockBrokerageSystem**: Serves as the main entry point, demonstrating the system's functionality.  

### **Enumerations**  

- **OrderStatus**: Defines possible order statuses, including `PENDING`, `EXECUTED`, and `REJECTED`.  

### **Custom Exceptions**  

- **InsufficientFundsException**: Raised when an account lacks sufficient funds for a transaction.  
- **InsufficientStockException**: Raised when an account lacks enough stock to complete a sell order.  

This project showcases a structured approach to implementing a trading system, ensuring robust account handling, order execution, and stock management.
