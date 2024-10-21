# 0x01. NoSQL - README

## Overview
This project focuses on **NoSQL** databases, specifically **MongoDB**. It covers basic operations such as listing databases, inserting, querying, updating, and deleting documents, and interacting with MongoDB using Python. The project also explores more advanced MongoDB operations like aggregation and working with specific topics in collections.

### Key Concepts:
- **NoSQL**: A category of database management systems that do not use traditional SQL for data storage and retrieval.
- **MongoDB**: A NoSQL document database that uses JSON-like documents to store data.

## Learning Objectives
By the end of this project, you will be able to:
- Understand what NoSQL is and how it differs from SQL.
- Explain key NoSQL concepts such as ACID, document storage, and NoSQL types.
- Use MongoDB to insert, update, and delete documents.
- Query data from a NoSQL database using MongoDB commands and Python.

## Project Requirements
- **Environment**: 
  - Ubuntu 18.04 LTS
  - MongoDB 4.2
  - Python 3.7 and PyMongo 3.10
- **Code Style**: 
  - Python files must adhere to **pycodestyle** guidelines.
  - Each script should start with `#!/usr/bin/env python3`.
  - All files should end with a new line.

## Setup Instructions

### MongoDB Installation
To install MongoDB 4.2 on Ubuntu 18.04, follow these commands:

```bash
$ wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | sudo apt-key add -
$ echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list
$ sudo apt-get update
$ sudo apt-get install -y mongodb-org
$ sudo service mongod start
$ mongo --version
```

### PyMongo Installation
To install PyMongo for Python:

```bash
$ pip3 install pymongo
```

## Tasks Overview

### 0. List all databases
Write a script that lists all databases in MongoDB.
- **File**: `0-list_databases`

### 1. Create a database
Write a script that creates or switches to a database.
- **File**: `1-use_or_create_database`

### 2. Insert document
Write a script that inserts a document with the name "Holberton school" in the `school` collection.
- **File**: `2-insert`

### 3. List all documents
Write a script to list all documents in the `school` collection.
- **File**: `3-all`

### 4. Match documents
Write a script to list all documents where the name is "Holberton school".
- **File**: `4-match`

### 5. Count documents
Write a script to count the number of documents in the `school` collection.
- **File**: `5-count`

### 6. Update document
Write a script to add an attribute `address` with value "972 Mission street" to all documents with name "Holberton school".
- **File**: `6-update`

### 7. Delete by match
Write a script to delete all documents with name "Holberton school".
- **File**: `7-delete`

### 8. List documents in Python
Write a Python function to list all documents in a collection.
- **File**: `8-all.py`

### 9. Insert a document in Python
Write a Python function to insert a new document in a collection.
- **File**: `9-insert_school.py`

### 10. Update topics
Write a Python function to update the topics of a school based on its name.
- **File**: `10-update_topics.py`

### 11. Search by topic
Write a Python function that returns all schools with a specific topic.
- **File**: `11-schools_by_topic.py`

### 12. Log stats
Write a Python script that provides stats about Nginx logs stored in MongoDB.
- **File**: `12-log_stats.py`

## Usage
Each task includes a specific MongoDB or Python command that performs operations on the MongoDB database. To run these scripts:

```bash
$ mongo <script_name>
$ python3 script_name.py
```

Ensure that MongoDB is running in the background before executing the commands.

## Author
- **Abdelrhman Fikri** - ALX Backend Storage Module

GitHub Repository: [alx-backend-storage](https://github.com/yourusername/alx-backend-storage)
