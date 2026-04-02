# Use Case Specification

## 1. General Information

* **Use Case Name:** Return Book
* **Primary Actor:** Student
* **Secondary Actors:** Library System, Librarian
* **Description:** A student returns a borrowed book to the library. The system updates the book's status, checks for overdue fines, and notifies any students who have reserved that book.

---

## 2. Preconditions

* The student has an active borrowing record for the book being returned.
* The book is physically present and identifiable (barcode intact).

---

## 3. Main Flow

1. The student brings the borrowed book to the library return desk.
2. The Librarian scans the book's barcode using the Library System.
3. The Library System retrieves the borrowing record associated with the book.
4. The Library System checks the return date against the due date.
5. If the book is returned on time, the system marks the transaction as "Returned" and updates the book's status to "Available".
6. The system prints or sends a return confirmation to the student.
7. The Librarian hands the student the confirmation and places the book back on the shelf.

---

## 4. Alternative Flows

### 4.1 Book Is Returned Overdue

* At step 4, if the current date exceeds the due date, the Library System calculates the overdue fine.
* The Librarian informs the student of the fine amount.
* The student pays the fine (cash or online).
* The Library System registers the fine payment and proceeds with step 5.

### 4.2 Book Is Damaged

* At step 2, the Librarian inspects the book and identifies visible damage.
* The Librarian marks the book as "Damaged" in the system rather than "Available".
* The system generates a damage report linked to the student's record.
* A replacement or repair fee is applied to the student's account.
* The use case ends after fee registration.

---

## 5. Postconditions

* The borrowing record is marked as "Returned" in the Library System.
* The book's status is updated to "Available" (or "Damaged" in the alternative flow).
* If the book was reserved by another student, the Library System sends them a notification.
* Any overdue fines or damage fees are recorded in the student's account.

---

## 6. Business Rules (optional)

* Overdue fine is calculated at a fixed rate per day past the due date.
* A damaged book fee equals the replacement cost of the book.
* Reserved books must be held for 48 hours after the return notification is sent.

---

## 7. Notes

* Students may also return books using a self-service return kiosk, which performs the same system steps without Librarian involvement.
