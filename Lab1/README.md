# 📚 Library Management System - Tree Structure (DBMS)

A simple representation of a **Library Management System** using the **Hierarchical (Tree) Database Model**. This project demonstrates parent-child relationships and the one-to-many constraint in a tree structure.

---

## 📖 Overview

The tree model organizes data in a hierarchical format where every child node has **only one parent**. This project models the following entities:

- Library
- Staff
- Member
- Loan

---

## 🌳 Tree Structure

```text
Library
├── Staff
└── Member
    └── Loan
```

---

## 🗂️ Record Types

### 📚 Library
- Library_ID (PK)
- Library_Name
- Address

### 👨‍💼 Staff
- Staff_ID (PK)
- Staff_Name
- Position
- Email

### 👤 Member
- Member_ID (PK)
- Member_Name
- Phone_No
- Membership_Type

### 📕 Loan
- Loan_ID (PK)
- Book_ID (FK)
- Issue_Date
- Due_Date
- Return_Date

---

## 🔗 Parent → Child Relationships

| Parent | Child | Relationship |
|---------|-------|--------------|
| Library | Staff | 1 : Many |
| Library | Member | 1 : Many |
| Member | Loan | 1 : Many |

---

## ⚠️ One-to-Many Constraint Limitation

The hierarchical database model allows each child node to have **only one parent**.

### Example

```
Book
 ▲
 │
Member A

Member B ❌
```

A **Book** cannot be reserved by multiple **Members** in a pure tree structure because it would require the Book node to have multiple parents. This represents a **many-to-many relationship**, which is not supported in the hierarchical model.

---

## ✅ Advantages

- Simple and easy to understand
- Fast parent-to-child navigation
- Efficient for hierarchical data
- Maintains clear data hierarchy

---

## ❌ Limitations

- Supports only one-to-many relationships
- Cannot directly represent many-to-many relationships
- May cause data duplication
- Less flexible than the relational model

---

## 🛠️ Tools Used

- **draw.io (diagrams.net)** – Diagram Design
- **GitHub** – Version Control
- **DBMS Concepts** – Hierarchical Database Model

---

## 📌 Conclusion

This project demonstrates how a Library Management System can be represented using a hierarchical tree structure. It effectively models one-to-many relationships but also highlights the main limitation of the tree model: **a child node cannot have multiple parents**, making many-to-many relationships difficult to represent.

---
**Author:** Arpit Patni
