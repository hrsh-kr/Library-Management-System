# Library Management System

## Project Overview
This Library Management System is a Java-based console application developed for IIITD as part of an Advanced Programming course. The system simulates a real-world library environment with distinct interfaces for librarians and members, allowing for comprehensive management of books, members, and lending operations.

## Key Features

### Librarian Features
- **Member Management:** Register new members, remove existing members
- **Book Management:** Add new books, remove books
- **Inventory Management:** View all available books and their details
- **Member Oversight:** View all members along with their borrowed books and outstanding fines
- **Fine Collection:** Track and collect fines from members

### Member Features
- **Book Browsing:** View all available books in the library
- **Personal Collection:** View books currently borrowed
- **Book Operations:** Borrow and return books
- **Fine Management:** View and pay outstanding fines

## Technical Implementation

### Core Classes
- **`Book`**: Represents a book with attributes like ID, title, author, copies, and availability status
- **`Member`**: Manages member information, borrowed books, and fine calculations
- **`Library`**: Central class that manages collections of books and members
- **`Main`**: Contains the user interface and program execution logic

### OOP Principles Applied
- **Encapsulation**: Private data members with appropriate getters and setters
- **Composition**: `Library` class contains collections of `Book` and `Member`
- **Association**: Relationships between `Member` and `Book` for borrowing operations
- **Unique Identification**: Books use numeric IDs, members use phone numbers as unique identifiers

## Business Rules
- Maximum of **2 books** can be borrowed by a member at any time
- Book lending period is **10 days**
- **Fine calculation**: ₹3 per day after the due date
- Members with outstanding fines **cannot borrow additional books** until fines are paid
- Books currently borrowed by members **cannot be removed** from the library
- Members with borrowed books **cannot be removed** from the system

## How to Use

### System Requirements
- Java Development Kit (**JDK 11** or higher)
- Apache Maven (**3.6.0** or higher)

### Running the Application

Clone this repository:
```sh
git clone https://github.com/yourusername/library-management-system.git
```

Navigate to the project directory:
```sh
cd library-management-system
```

Build the project using Maven:
```sh
mvn clean install
```

Run the application:
```sh
java -jar target/library-management-system-1.0.jar
```

## Navigation
- The application starts with a **main menu** to enter as either a **librarian** or a **member**
- Each role has a specific menu with relevant operations
- **Input validation** is implemented to handle incorrect entries
- Navigation between menus is intuitive with **numbered options**

## Implementation Details

### Phone Number Validation
- Requires **exactly 10 digits**
- Cannot register **duplicate phone numbers**

### Fine Calculation
- For demonstration purposes, **each second represents one day**
- Fines accrue at **₹3 per day** beyond the 10-day lending period

### Book Management
- **Multiple copies** of the same book are supported
- Books are **uniquely identified** by automatically generated IDs
