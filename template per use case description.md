# Use Case Specification

## 1. General Information

* **Use Case Name: Reserve Book
* **Primary Actor: Student
* **Secondary Actors: Library System
* **Description: A student reserves a book that is currently unavailable so they can borrow it later.

---

## 2. Preconditions
- Student is registered in the system
- Student is logged in
- Book exists in the system
- Book is currently unavailable

---

## 3. Main Flow

1. Student searches for a book
2. System displays search results
3. Student selects a book
4. System shows that the book is unavailable
5. Student clicks the "Reserve" button
6. System records the reservation
7. System confirms the reservation to the student

---

## 4. Alternative Flows

#### 4.1 Book is available
- System informs the student that the book is available for borrowing instead of reservation

#### 4.2 Student already reserved the book
- System shows a message that the reservation already exists

#### 4.3 Reservation limit reached
- System informs the student that they cannot reserve more books

---

## 5. Postconditions

*

---

## 6. Business Rules (optional)

*

---

## 7. Notes

*
