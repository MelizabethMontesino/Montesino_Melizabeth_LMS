In-deth Explanation:  

 

Collection management in a library implies directing a series of tasks in order to add and remove books, or list them, for which a library must design an operational system. These applications in Java will help in simplifying these processes where the application will read the book information from a structured text file and ensure there is an updated collection of the books in memory. Some of the function that are assignable and readily removable include managing unique book identifiers, as well as presenting only the current stock view with its purpose to help library staff to work accurately and effectively. It is aimed at delivering the best solution that shall assist the end users to manage their library systems in an easy way, less use of manpower and high efficiency. 

 
1st step: 

Purpose: The system aims to manage a library's collection of books. The core functionalities include adding books from a file, removing books, and listing all books in the collection. The system will help library staff easily update and manage book records. 

Define Requirements: 

1st step: 

Purpose: The system aims to manage a library's collection of books. The core functionalities include adding books from a file, removing books, and listing all books in the collection. The system will help library staff easily update and manage book records. 

Constraints: 

The system should handle invalid input gracefully (e.g., duplicate IDs, non-existent IDs for removal). 

The text file format must strictly follow the specified format: "ID, Title, Author". 

Books should be stored in memory, not in a persistent database. 

Features: 

1st step: 

Add Books from a Text File: The system will allow users to import a list of books from a text file. Each book will have a unique ID, title, and author. The file will be formatted with comma-separated values, where each line represents a book. 

Remove a Book Using its ID: Users will be able to remove a book from the collection by entering its unique ID number. 

List All Books: Users will be able to view a list of all books currently in the collection, displaying each book's ID, title, and author. 

Constraints: 

1st step: 

The system will ensure that duplicate IDs are handled gracefully by checking for uniqueness before adding new books. If a duplicate ID is encountered, the book entry will be skipped, and an appropriate message will be logged or displayed. 

The input text file must strictly follow the "ID, Title, Author" format. The system will validate each line before processing to ensure it adheres to this format. If a line is incorrectly formatted, the system will notify the user without crashing. 

Books will be stored in memory (e.g., using an ArrayList or other suitable data structure) for fast access during the session. There will be no permanent storage, meaning data will only persist during runtime unless explicitly exported or saved externally. 

Intended Users: 

 

1st step: 

Librarians: The primary users are library staff members responsible for managing book collections. 

System Administrators: May occasionally need to use the system for data management or troubleshooting. 

User Interaction: 

1st step: 

Add Books: Librarians will upload a text file containing book information. The system will read the file, validate entries, and add valid books to the collection. 

Remove Books: Librarians will input the book’s ID to remove it from the collection. 

List All Books: Librarians will request a list of all books in the collection to verify or audit the library inventory. 

 

Tasks: 

1st step: 

Reading from a Text File: 

Open and read a text file line-by-line. 

Parse each line to extract the book’s ID, title, and author. 

Store valid book entries in a collection (such as an ArrayList). 

Adding Books to the Collection: 

Verify that each book has a unique ID. 

Store the book’s details in a data structure. 

Removing Books from the Collection: 

Listing All Books: 

Iterate over the collection and print the details of each book. 

Classes and Methods: 

1st step: 

Class: LibraryManager Responsibilities: Handle the collection of books. 

Methods: 

addBooksFromFile(String fileName): Arguments: fileName (String) – the name of the file to read. Return Value: void Algorithm: 

Open the file. 

For each line, split the string by the comma. 

Create a Book object and store it in the collection if the ID is unique. 

removeBookById(int id): Arguments: id (int) – the ID of the book to remove. Return Value: boolean – true if the book was removed, false otherwise. Algorithm: 

Search the collection for the book with the given ID. 

If found, remove the book and return true. 

If not found, return false. 

listAllBooks(): Arguments: None. Return Value: void Algorithm: 

Loop through the collection and print each book’s details. 

Class: Book Attributes: 

int id 

String title 

String author 

Methods: 

Constructor and getter methods. 

Test Case 1: Add Books from a Valid File 

1st step: 

Create a text file with valid book entries. 

Call addBooksFromFile() and check if the books are correctly added. 

Verify that each book’s ID, title, and author are stored correctly. 

Test Case 2: Add Books from an Invalid File 

Create a file with invalid or duplicate IDs. 

Call addBooksFromFile() and ensure the system skips duplicates and handles invalid entries without crashing. 

Test Case 3: Remove a Book by ID 

1st step: 

Add several books to the collection. 

Call removeBookById() with a valid and invalid ID. 

Ensure the book is removed if valid and returns falem.se if invalid. 

Test Case 4: List All Books 

Add several books to the collection. 

Call listAllBooks() and verify that all books are printed in the correct format. 

 

Boundary Testing: 

Test with an empty file (no books added). 

Test with the maximum number of books allowed by memory constraints. 

This approach ensures that each feature works correctly before combining them into the final system. 
