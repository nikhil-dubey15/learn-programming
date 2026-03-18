# Phase 2 - 3.3 Relations: Primary & Foreign Keys

We call them "Relational" databases because different tables relate to each other. 

Why don't we just put everything in one giant table? 
Imagine an Amazon database. If you put a user's `Name`, `Address`, and `Order_Item` in the same table, what happens when they buy 50 items? You would have to type their name and address 50 different times! That wastes massive amounts of space.

Instead, we split them into two tables: `Users` and `Orders`. But we need a way to link them together!

## 1. The Primary Key (The ID Badge)
Every single row in a SQL database MUST have a **Primary Key**. 
* **What it is:** A totally unique identifier for that specific row. It is usually a column simply named `id`.
* **The Analogy:** Your Social Security Number, or your Employee ID Badge. Someone else might have the name "Nikhil", but nobody else has your ID Number.

**Users Table:**
| id (Primary Key) | name   | age |
|------------------|--------|-----|
| 1                | Nikhil | 25  |
| 2                | Sarah  | 30  |

## 2. The Foreign Key (The Link)
When Sarah places an order for a Laptop, we create a new row in the `Orders` table. How do we prove Sarah bought it without typing her name?

We use a **Foreign Key**.
* **What it is:** A column in Table B that perfectly matches the Primary Key of Table A.

**Orders Table:**
| order_id (Primary Key) | item_name | user_id (Foreign Key) |
|------------------------|-----------|-----------------------|
| 100                    | Laptop    | 2                     |
| 101                    | Mouse     | 2                     |
| 102                    | Keyboard  | 1                     |

Look at the `Orders` table! 
Because `user_id` is a Foreign Key pointing to the `Users` table, we know instantly that:
* Sarah (User 2) bought the Laptop and the Mouse.
* Nikhil (User 1) bought the Keyboard.

## Why this is Safe (Referential Integrity)
Relational databases are super smart. Because you linked these tables using a Foreign Key, the database will literally **prevent** you from deleting Sarah!

If you try to run `DELETE FROM Users WHERE name = 'Sarah';`, the database will throw a massive error: *"Wait! You can't delete Sarah! She has orders linked to her in the other table! If you delete her, we won't know who bought the Laptop!"*

This forces developers to write careful, safe code.

---

## 📺 Recommended Video Lesson

**Primary & Foreign Keys Explained**
- An excellent visual breakdown of how ID numbers link tables together to prevent duplicate data.
- [Watch on YouTube (approx 6 mins)](https://www.youtube.com/watch?v=5kiMg7GXAsY)

---

**Next Step:** The tables are linked! But how do we write a SQL query that asks for data from *both* tables at the exact same time? Move to the final database lesson: **3.4 Joins**!
