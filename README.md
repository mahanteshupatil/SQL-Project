# Music Store SQL Analysis - SSMS

## About
Analyzed digital music store database in SQL Server to solve 8 business questions on employees, sales, customers, artists, and tracks.

## Files
- `SQLQuery1.sql` - Employee, Invoice, Customer analysis
- `SQLQuery2.sql` - Genre, Artist, Track analysis

## Business Questions Solved

### **SQLQuery1.sql**
1. **Senior employee** - `ORDER BY levels DESC` + `OFFSET FETCH`
2. **Top country by invoices** - `GROUP BY billing_country`, `COUNT(*)`
3. **Top 3 invoice totals** - `ORDER BY total DESC` 
4. **Best city for event** - `SUM(total)` grouped by city
5. **Best customer** - `JOIN` customer + invoice, `SUM(total)`

### **SQLQuery2.sql** 
6. **Rock music listeners** - 4-table `JOIN`, `DISTINCT email`, `WHERE genre='ROCK'`
7. **Top 10 Rock artists** - `JOIN` track+album+artist+genre, `COUNT()`, `GROUP BY`
8. **Tracks longer than avg** - Subquery `AVG(milliseconds)`, `WHERE > avg`

## SQL Concepts Used
`JOIN`, `GROUP BY`, `ORDER BY`, `COUNT()`, `SUM()`, `AVG()`, `DISTINCT`, `OFFSET FETCH`, Subqueries

## Tools
SQL Server Management Studio 20, SQL server 2025

## How to Run
1. Download both `.sql` files
2. Open in SSMS → Connect to `Music_Database` → Run queries
