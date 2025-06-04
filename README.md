# 📚 PLP Bookstore MongoDB Project

This project demonstrates the use of MongoDB to manage a bookstore database using CRUD operations, advanced queries, aggregation pipelines, and indexing techniques.

---

## ⚙️ Setup Instructions

### 📌 Option 1: Install MongoDB Locally

1. Download and install MongoDB Community Edition from:
   👉 [https://www.mongodb.com/try/download/community](https://www.mongodb.com/try/download/community)
2. Make sure MongoDB server is running:

   ```bash
   mongod
   ```
3. Open the MongoDB Shell (mongosh):

   ```bash
   mongosh
   ```

### 📌 Option 2: Use MongoDB Atlas (Cloud)

1. Go to: 👉 [https://www.mongodb.com/cloud/atlas](https://www.mongodb.com/cloud/atlas)
2. Create a free cluster.
3. Whitelist your IP address and create a database user.
4. Get your **connection string**, replace the `uri` in `insert_books.js` with it:

   ```js
   const uri = 'your-mongodb+srv://<username>:<password>@cluster0.mongodb.net/';
   ```

---

## 🚀 How to Run `insert_books.js`

### Step 1: Install Node.js

Download and install from:
👉 [https://nodejs.org/](https://nodejs.org/)

### Step 2: Install Dependencies

In your project directory, open a terminal and run:

```bash
npm install mongodb
```

### Step 3: Run the Script

```bash
node insert_books.js
```

This will:

* Connect to MongoDB
* Drop the `books` collection if it exists
* Insert 12 sample books
* Print a summary of inserted data

---

## 🧪 How to Test Queries

### ✅ Using MongoDB Shell

1. Open the shell:

   ```bash
   mongosh
   ```
2. Switch to the database:

   ```js
   use plp_bookstore
   ```
3. Run queries, for example:

   ```js
   db.books.find({ genre: "Fiction" })
   db.books.find({ published_year: { $gt: 2010 }, in_stock: true })
   ```

### ✅ Using MongoDB Compass

1. Open MongoDB Compass.
2. Connect to your local server (`mongodb://localhost:27017`) or Atlas URI.
3. Select the `plp_bookstore` database and `books` collection.
4. Use the **Filter** bar to run queries, like:

   ```js
   { author: "George Orwell" }
   ```

---

## 📁 Files Included

* `insert_books.js` — Script to populate MongoDB with sample books.
* `queries.js` — Contains all required MongoDB queries.
* `README.md` — Instructions and project documentation.
* `screenshot.png` — Screenshot showing your data in MongoDB Compass

---
