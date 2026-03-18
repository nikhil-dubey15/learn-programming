# Phase 2 - 3.2 Basic SQL Queries: Talking to the Tables

SQL (Structured Query Language) is surprisingly easy to read. It's designed to sound almost exactly like English!

There are 4 main actions you can do to a database table. In the industry, we call this **CRUD**:
1. **C**reate (`INSERT`)
2. **R**ead (`SELECT`)
3. **U**pdate (`UPDATE`)
4. **D**elete (`DELETE`)

Let's imagine we have a rigid SQL table named `Users`. It has three columns: `id`, `name`, and `age`.

## 1. R: Reading Data (`SELECT`)
This is the one you will use 90% of the time as a QA or Junior Dev!

**"Give me everything in the Users table."**
The asterisk `*` means "All Columns".
```sql
SELECT * FROM Users;
```

**"Give me just the names of users who are older than 18."**
The `WHERE` clause filters the rows!
```sql
SELECT name FROM Users 
WHERE age > 18;
```

## 2. C: Creating Data (`INSERT`)
When someone registers for your website, the backend code runs this command to add a new row to the table.

```sql
INSERT INTO Users (id, name, age) 
VALUES (1, 'Nikhil', 25);
```

## 3. U: Updating Data (`UPDATE`)
If a user has a birthday, we need to update their specific row.

**⚠️ WARNING:** If you forget to add the `WHERE` clause in an UPDATE command, you will accidentally update EVERY SINGLE ROW in the entire database! (Many developers have been fired for this!).

```sql
-- Safe Update: Only changes Nikhil's age.
UPDATE Users 
SET age = 26 
WHERE name = 'Nikhil';
```

## 4. D: Deleting Data (`DELETE`)
If a user deletes their account. Again, do NOT forget the `WHERE` clause!

```sql
DELETE FROM Users 
WHERE name = 'Nikhil';
```

---

## 🛠️ Practical Exposure: Write Your Own Query!

Normally, you need a server to run SQL. But there are free websites that let you practice in your browser!

1. Go to this website: [SQL Tryit Editor](https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all)
2. You will see a box where you can type. Type this:
   ```sql
   SELECT CustomerName, City FROM Customers WHERE Country = 'Mexico';
   ```
3. Click the green **Run SQL** button.
4. Look at the results below! You just successfully queried a real live database!

---

## 📺 Recommended Video Lesson

**SQL Basics for Beginners**
- Watch a developer write these exact 4 commands and see the visual tables update in real-time.
- [Watch on YouTube (approx 12 mins)](https://www.youtube.com/watch?v=POx-8XRHzUM)

---

**Next Step:** Writing queries on one table is easy. But what if we have multiple tables? How do they talk to each other? Move to **3.3 Relations (Keys)**!
