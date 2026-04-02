# Use Case Specification

## 1. General Information

* **Use Case Name:** Borrow Book
* **Primary Actor:** Student
* **Secondary Actors:** Library System, Librarian
* **Description:** A student borrows an available book from the library after providing their library card details.

---

## 2. Preconditions

* The student has a valid, active library account.
* The book is available (not currently borrowed or lost).
* The student has not exceeded the maximum number of books allowed to borrow simultaneously.

---

## 3. Main Flow

1. The student approaches the librarian desk and presents the book along with their library card.
2. The librarian scans the student's library card and the book barcode into the Library System.
3. The Library System checks availability and the student's borrowing status.
4. The Library System registers the borrowing transaction, sets the due date (e.g., 14 days), and updates the book status to "Borrowed".
5. The system prints or sends a confirmation with the due date to the student.
6. The student takes the book.

---

## 4. Alternative Flows

### 4.1 Student Has Exceeded Borrowing Limit

* At step 3, if the Library System detects the student already has the maximum number of books borrowed, it displays a warning message.
* The Librarian informs the student that they must return a book first before borrowing another.
* The use case ends without completing the borrow.

### 4.2 Book Is Reserved by Another Student

* At step 3, if the Library System detects the book is reserved by another student, it notifies the Librarian.
* The Librarian informs the current student that the book cannot be borrowed.
* The student may choose to reserve a different copy or another book.

---

## 5. Postconditions

* The book's status is updated to "Borrowed" in the Library System.
* A borrowing record is created with the student's ID, book ID, borrow date, and due date.
* The student's available borrowing slot count decreases by one.

---

## 6. Business Rules (optional)

* A student may borrow a maximum of 5 books at the same time.
* The default borrowing period is 14 days.
* Overdue books result in a daily fine.

---

## 7. Notes

* If the student is borrowing digitally (e-book), this flow is handled entirely through the online portal without the Librarian's involvement.
