# 0x02. Redis Basic

This project is focused on learning the basics of Redis and how to use it in Python applications. Redis is a fast, open-source, in-memory key-value data store that supports various data structures like strings, hashes, lists, sets, and more. The goal of this project is to implement a cache system using Redis, track method calls, and manage caching for a web application.

## Learning Objectives
- Use Redis for basic operations.
- Implement Redis as a simple cache.
- Track function call history and count using Redis.
- Store and retrieve data (strings, lists) in Redis.
- Implement an expiring cache for a web page.

## Requirements
- All code is written in Python 3.7 and must be interpreted/compiled on Ubuntu 18.04 LTS.
- Files must end with a new line.
- Code should conform to the **pycodestyle** style guide (version 2.5).
- All functions and methods must be documented.
- Functions and coroutines must be type-annotated.
- Redis should be installed and running locally or inside a container.

## Project Setup
1. **Install Redis on Ubuntu 18.04**:
   ```bash
   sudo apt-get -y install redis-server
   ```
2. **Start Redis Server**:
   ```bash
   service redis-server start
   ```
3. **Install Redis Python Client**:
   ```bash
   pip3 install redis
   ```

## Tasks

### 0. Writing Strings to Redis
- Implement a `Cache` class to store data in Redis. 
- The `store` method saves data with a randomly generated key and returns the key.
- Data can be of type `str`, `bytes`, `int`, or `float`.

### 1. Reading from Redis and Recovering Original Type
- Implement a `get` method to retrieve data by key, with optional conversion back to the original type.
- Additional methods `get_str` and `get_int` automatically retrieve and convert the data.

### 2. Incrementing Values
- Implement a decorator `count_calls` to track how many times a method of the `Cache` class is called.
- The method's qualified name is used as the key for counting.

### 3. Storing Lists
- Implement a decorator `call_history` to store the history of inputs and outputs for a function in two separate Redis lists (one for inputs and one for outputs).

### 4. Retrieving Lists
- Implement a `replay` function to display the history of calls for a particular function, using the input/output lists stored in Redis.

### 5. Implementing an Expiring Web Cache and Tracker (Advanced)
- Implement a `get_page` function that caches the HTML content of a URL for 10 seconds.
- Track how many times a particular URL was accessed using Redis.

## Usage
To run the project, execute the following example:

```bash
$ python3 main.py
