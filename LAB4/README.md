# DBMS Lab 4 – MongoDB Social Media Database

## 📘 Overview

This folder contains my **Database Management Systems Lab 4 Practical Assignment**, based on MongoDB and NoSQL database concepts.

The practical focuses on designing and managing a Social Media Database named `smdb` using MongoDB. The database consists of four main collections: users, posts, comments and likes.

The assignment covers document-based database design, data population, CRUD operations, aggregation pipelines, indexing, key-value store design, MongoDB Atlas deployment and ETL pipeline architecture.

All practical tasks are performed using MongoDB document-model concepts without using relational or SQL tables.

---

## 🗄️ Database Structure

The Social Media Database contains the following four collections:

| Collection | Description | Main Fields |
|---|---|---|
| users | Stores user information | id, name, email, joinedDate |
| posts | Stores user posts | id, userId, content, createdAt, likeCount |
| comments | Stores comments on posts | id, postId, userId, commentText, createdAt |
| likes | Stores post likes | id, postId, userId, likedAt |

### Collection Relationships

- `posts.userId` references `users.id`.
- `comments.postId` references `posts.id`.
- `comments.userId` references `users.id`.
- `likes.postId` references `posts.id`.
- `likes.userId` references `users.id`.

A referenced data model is used to avoid unnecessary duplication of user information across collections.

---

## 📝 Topics Covered (7 Questions)

| Q. No. | Topic | Main Concepts |
|---|---|---|
| Q1 | Collections | createCollection(), embedded vs referenced design |
| Q2 | Data Population and CRUD | insertMany(), find(), updateOne(), deleteOne() |
| Q3 | Aggregation Pipelines | $match, $group, $sort, $lookup, $avg |
| Q4 | Indexing | Single-field index, compound index, explain() |
| Q5 | Key-Value Store Layout | Cache keys, values, sessions and feeds |
| Q6 | MongoDB Atlas Deployment | Cluster tier, replica set, shard key |
| Q7 | ETL Pipeline | Data lake, data warehouse, analytics reporting |

**Total Marks: 35**

---

## 💻 Practical Implementation

The practical work includes:

1. **Collections:** Creating users, posts, comments and likes collections, choosing between embedded and referenced data models, inserting sample documents and displaying records using find().

2. **Data Population and CRUD:** Populating the collections with 8 users, 10 posts, 15 comments and 20 likes. Performing filtered searches, updating a post and deleting a comment.

3. **Aggregation Pipelines:** Calculating total likes per post, total posts per user, average comments per post and joining posts with user information using $lookup.

4. **Indexing:** Creating a single-field index on posts.userId and a compound index on comments.postId and comments.createdAt. Comparing query execution statistics before and after indexing using explain("executionStats").

5. **Key-Value Store Layout:** Designing cache keys for user sessions, feeds and post statistics, explaining TTL, cache hits, cache misses and cache invalidation.

6. **MongoDB Atlas Deployment:** Designing a cloud deployment using an M30 cluster, a three-member replica set and a compound shard key for the posts collection.

7. **ETL Pipeline:** Designing a nightly ETL process to extract posts and likes, store raw documents in a data lake, transform them using aggregation logic and load summarized information into a data warehouse for analytics.

---

## 🛠️ Technologies Used

- **MongoDB** – NoSQL document-oriented database.
- **MongoDB Shell (mongosh)** – Executing database commands.
- **MongoDB Atlas** – Cloud database deployment.
- **MongoDB Aggregation Framework** – Data processing and analysis.
- **Indexing** – Improving query performance.
- **Redis-style Key-Value Design** – Cache architecture for sessions and feeds.
- **ETL Concepts** – Extract, Transform and Load for analytics.

---

## 📊 Key Results

Some important results obtained during the practical include:

| Operation | Result |
|---|---|
| Total Users | 8 |
| Total Posts | 10 |
| Total Comments after deletion | 14 |
| Total Likes | 20 |
| Average Comments per Post | 1.4 |
| Average Likes per Post | 2 |
| Posts by User 1 | 3 |

### Index Performance Comparison

The aggregation query was tested before and after creating the userId index.

| Metric | Before Index | After Index |
|---|---|---|
| Query Plan | COLLSCAN | IXSCAN |
| Documents Examined | 10 | 0 |
| Keys Examined | 0 | 3 |
| Documents Returned | 3 | 3 |
| Work Units | 11 | 4 |

The indexed aggregation used an index-covered query plan, reducing the number of documents examined.

---

## 🎯 Learning Outcomes

Through this practical assignment, I gained experience in:

- Understanding NoSQL and document-oriented databases.
- Creating and managing MongoDB collections.
- Understanding embedded and referenced document models.
- Performing CRUD operations using MongoDB.
- Writing aggregation pipelines for data analysis.
- Joining collections using $lookup.
- Creating single-field and compound indexes.
- Understanding query execution plans and performance statistics.
- Designing key-value caching systems.
- Understanding MongoDB Atlas deployment and replication.
- Learning the concepts of sharding and shard keys.
- Designing ETL pipelines for analytical reporting.
- Understanding the difference between data lakes and data warehouses.

---

## 📁 Files Included

This folder contains the main Lab 4 report and supporting practical assignment files:

- `DBMS_Lab4_Arpit_Patni_2501730111.pdf` – Complete Lab 4 practical report.
- `DBMS_Arpit_2501730111_Q1_LAB4.pdf` – Collections and document design.
- `DBMS_Arpit_2501730111_Q2_LAB4.pdf` – Data population and CRUD.
- `DBMS_Arpit_2501730111_Q3_LAB4.pdf` – Aggregation pipelines.
- `DBMS_Arpit_2501730111_Q4_LAB4.pdf` – Indexing and performance.
- Supporting PDFs for Q5 – Key-Value Store Layout.
- Supporting PDFs for Q6 – MongoDB Atlas Deployment.
- Supporting PDFs for Q7 – ETL Pipeline.

---

## 👨‍💻 Student Details

**Name:** Arpit Patni  
**Roll Number:** 2501730111  
**Course:** B.Tech CSE (AI & ML)  
**Section:** A  
**University:** K.R. Mangalam University, Gurugram  
**Subject:** Database Management System (DBMS)  
**Lab:** 4 – MongoDB Social Media Database

---

*This repository contains my academic practical work completed as part of the DBMS course.*
