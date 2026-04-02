# Use Case Specification

## 1. General Information

* **Use Case Name:** Search Book
* **Primary Actor:** Student
* **Secondary Actors:** Library System
* **Description:** A student searches the library catalog to find a book by title, author, ISBN, or category and views its availability status.

---

## 2. Preconditions

* The student has access to the library catalog (either via the online portal or an in-library terminal).
* The Library System is operational and the catalog is up to date.

---

## 3. Main Flow

1. The student opens the library catalog (web portal or terminal).
2. The student enters a search query (title, author name, ISBN, or subject/category).
3. The Library System processes the query and retrieves matching records from the catalog database.
4. The system displays a list of matching books with details: title, author, ISBN, edition, location (shelf number), and availability status.
5. The student selects a book from the results to view its full details.
6. The system displays the full book details including the current borrowing status (Available / Borrowed / Reserved).
7. The student notes the book's location or proceeds to reserve it if unavailable.

---

## 4. Alternative Flows

### 4.1 No Results Found

* At step 3, if the Library System finds no matching records for the search query, it displays a "No results found" message.
* The system suggests checking the spelling or broadening the search terms.
* The student may modify the query and repeat the search, or exit the use case.

### 4.2 Multiple Editions Available

* At step 4, if multiple editions of the same book exist in the catalog, each edition is listed separately.
* The student can filter results by year, edition, or language.
* The student selects the preferred edition and the use case continues from step 5.

---

## 5. Postconditions

* The student has viewed the book details and its current availability.
* No data is modified in the Library System as a result of a search.
* (Optional) The search query may be logged for catalog analytics.

---

## 6. Business Rules (optional)

* The search is case-insensitive and supports partial matches.
* Books marked as "Lost" or "Under Maintenance" are shown in the results but cannot be borrowed or reserved.
* Results are paginated: a maximum of 20 results per page are displayed.

---

## 7. Notes

* The search catalog is accessible without logging in; however, reserving a book requires authentication.
* Future enhancement: support for advanced filters (language, publication year range, availability only).
