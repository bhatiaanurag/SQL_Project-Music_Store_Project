# Music Store SQL Project

## 1. Project Overview

The Music Store SQL Project is a comprehensive database design and analysis project built using SQL. It simulates a digital music store system that manages customers, invoices, artists, albums, tracks, and employees.

The project focuses on designing a normalized relational database and performing analytical queries to extract meaningful insights about customer behavior, sales performance, and music trends.

---

## 2. Business Objective

The primary objectives of this project are:

* To analyze music sales and revenue generation
* To understand customer purchasing behavior
* To identify top-performing artists, albums, and genres
* To evaluate employee contributions and sales support
* To enable business insights for a digital music platform

---

## 3. Database Schema

The project consists of multiple interconnected tables that represent the music store ecosystem.

### 3.1 Customers

Stores customer information.

| Column Name    | Description                         |
| -------------- | ----------------------------------- |
| customer_id    | Unique identifier for each customer |
| first_name     | Customer's first name               |
| last_name      | Customer's last name                |
| email          | Customer email                      |
| country        | Customer location                   |
| support_rep_id | Assigned employee                   |

---

### 3.2 Employees

Contains employee details.

| Column Name | Description                |
| ----------- | -------------------------- |
| employee_id | Unique employee identifier |
| first_name  | Employee first name        |
| last_name   | Employee last name         |
| title       | Job role                   |
| reports_to  | Manager ID                 |

---

### 3.3 Artists

Represents music artists.

| Column Name | Description              |
| ----------- | ------------------------ |
| artist_id   | Unique artist identifier |
| name        | Artist name              |

---

### 3.4 Albums

Stores album information.

| Column Name | Description             |
| ----------- | ----------------------- |
| album_id    | Unique album identifier |
| title       | Album title             |
| artist_id   | Associated artist       |

---

### 3.5 Tracks

Represents individual songs.

| Column Name  | Description             |
| ------------ | ----------------------- |
| track_id     | Unique track identifier |
| name         | Track name              |
| album_id     | Associated album        |
| genre_id     | Genre classification    |
| milliseconds | Duration                |
| unit_price   | Price per track         |

---

### 3.6 Genres

Defines music categories.

| Column Name | Description             |
| ----------- | ----------------------- |
| genre_id    | Unique genre identifier |
| name        | Genre name              |

---

### 3.7 Invoices

Captures billing information.

| Column Name     | Description               |
| --------------- | ------------------------- |
| invoice_id      | Unique invoice identifier |
| customer_id     | Associated customer       |
| invoice_date    | Date of purchase          |
| billing_country | Customer country          |
| total           | Total invoice amount      |

---

### 3.8 Invoice Line

Stores detailed purchase records.

| Column Name     | Description              |
| --------------- | ------------------------ |
| invoice_line_id | Unique record identifier |
| invoice_id      | Associated invoice       |
| track_id        | Purchased track          |
| unit_price      | Price per unit           |
| quantity        | Quantity purchased       |

---

## 4. Relationships Between Tables

* Customers are linked to Employees via `support_rep_id`
* Invoices are linked to Customers via `customer_id`
* Invoice Line is linked to Invoices via `invoice_id`
* Invoice Line is linked to Tracks via `track_id`
* Tracks are linked to Albums via `album_id`
* Albums are linked to Artists via `artist_id`
* Tracks are linked to Genres via `genre_id`

This relational structure allows complex queries involving multiple joins for deep analysis.

---

## 5. Key Features

* Fully normalized relational database design
* Multiple entity relationships representing a real business model
* Detailed transactional data for analysis
* Support for advanced SQL queries (joins, aggregations, subqueries)
* Scalable and reusable dataset for practice and learning

---

## 6. How to Use

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/music-store-sql-project.git
   ```

2. Open your SQL environment (MySQL, PostgreSQL, SQL Server, etc.)

3. Execute the SQL file:

   ```sql
   SOURCE musicstoreproject.sql;
   ```

4. Verify table creation and data insertion.

5. Start running analytical queries.

---

## 7. Analytical Use Cases

This project enables various business analyses, such as:

* Top customers based on total spending
* Best-selling artists and albums
* Most popular music genres
* Revenue distribution by country
* Employee performance based on customer sales
* Purchase trends over time

---

## 8. Skills Demonstrated

* Relational Database Design
* SQL Query Optimization
* Data Analysis using SQL
* Multi-table Joins
* Aggregation and Grouping
* Business Insight Generation

---

## 9. Project Structure

```id="kz83la"
Music-Store-SQL-Project/
│
├── musicstoreproject.sql
└── README.md
```

---

## 10. Guidance

This project was developed under the guidance of:

Yash Jain
Future Vision Computer

---

## 11. Acknowledgements

This project is inspired by real-world digital music platforms and is intended for educational and analytical purposes.

---

## 12. Contact

For any feedback, suggestions, or collaboration opportunities, feel free to connect.

---

## 13. Support

If you find this project helpful, consider giving it a star on GitHub to support the work.
