# classroomdiagram
classDiagram
    class Book {
        +int ISBN
        +string Title
        +string Genre
        +int Year
    }
    
    class Author {
        +int AuthorID
        +string Name
        +string Country
    }
    
    class Member {
        +int MemberID
        +string Name
        +date MembershipDate
    }
    
    class Loan {
        +int LoanID
        +date LoanDate
        +date DueDate
        +date ReturnDate
    }

    Book "1" -- "many" Author : "written by"
    Book "1" -- "many" Loan : "borrowed in"
    Member "1" -- "many" Loan : "borrows"
Class Diagram in Mermaid to represent a simple Library Management System. This diagram will have four main classes: Book, Author, Member, and Loan.
Book: Represents the book in the library, containing attributes like ISBN, Title, Genre, and Year.
Author: Represents the author of a book, with attributes like AuthorID, Name, and Country.
Member: Represents a library member, containing attributes such as MemberID, Name, and MembershipDate.
Loan: Represents the transaction of borrowing a book, linking a member to a book, with attributes like LoanID, LoanDate, DueDate, and ReturnDate.
Book: The Book class stores details about the books available in the library, including attributes like ISBN, title, genre, and year of publication. 
Author: The Author class stores information about authors, like a unique AuthorID, name, and country. .
Member: The Member class represents a library member, identified by a MemberID. It also includes the member's name and their membership start date. 
Loan: The Loan class manages the borrowing process. Each loan is a record of a specific book borrowed by a member, along with details like loan date, due date, and return date. 


Book to Author:  shows that an author can write multiple books, but a book can have one primary author.
Book to Loan: A Book can appear in multiple loans as many members might borrow the same book over time.
Member to Loan: indicates that a member can borrow multiple books, but each loan represents a single transaction involving one member and one book.
