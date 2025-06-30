# Assignment Description

## 1. Create a database to manage a book library according to the structure below.
Use DDL commands to create the necessary tables and their relationships.

### Database Structure

**a) Schema name — `LibraryManagement`**

**b) Table `authors`:**
- `author_id` (INT, auto-incremented PRIMARY KEY)
- `author_name` (VARCHAR)

**c) Table `genres`:**
- `genre_id` (INT, auto-incremented PRIMARY KEY)
- `genre_name` (VARCHAR)

**d) Table `books`:**
- `book_id` (INT, auto-incremented PRIMARY KEY)
- `title` (VARCHAR)
- `publication_year` (YEAR)
- `author_id` (INT, FOREIGN KEY referencing `authors`)
- `genre_id` (INT, FOREIGN KEY referencing `genres`)

**e) Table `users`:**
- `user_id` (INT, auto-incremented PRIMARY KEY)
- `username` (VARCHAR)
- `email` (VARCHAR)

**f) Table `borrowed_books`:**
- `borrow_id` (INT, auto-incremented PRIMARY KEY)
- `book_id` (INT, FOREIGN KEY referencing `books`)
- `user_id` (INT, FOREIGN KEY referencing `users`)
- `borrow_date` (DATE)
- `return_date` (DATE)

---

## 2. Populate the tables with simple fictional test data.
One or two rows per table are sufficient.

---

## 3. Return to the database used in Topic 3.
Write a query using the `FROM` and `INNER JOIN` clauses that joins all the following tables:
- `order_details`
- `orders`
- `customers`
- `products`
- `categories`
- `employees`
- `shippers`
- `suppliers`

Use the appropriate keys to connect the tables.  
Check if the query executes correctly.

---

## 4. Execute the following queries:

- Determine how many rows are returned (using the `COUNT` operator).  
  💡 Don’t forget to take screenshots of your results and queries.

- Replace several `INNER JOIN` operators with `LEFT` or `RIGHT JOIN`.  
  Check how the row count changes and explain why in a text file.

- From the query in step 3, select only rows where `employee_id > 3` and `employee_id ≤ 10`.

- Group the results by category name.  
  Count the number of rows in each group and calculate the average product quantity  
  (use `order_details.quantity`).

- Filter out groups where the average product quantity is greater than 21.

- Sort the result in descending order by the number of rows per group.

- Display four rows, skipping the first one.

---
