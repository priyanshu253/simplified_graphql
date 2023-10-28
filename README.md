# Simplified GraphQL Repository

This repository provides a simplified GraphQL server running on port 5000 with the endpoint `/graphql`. It supports two schemas for managing books and authors and provides mutation services to add new books and authors.

## Table of Contents
- [Getting Started](#getting-started)
- [Schema](#schema)
- [Mutations](#mutations)
- [Example Query](#example-query)

## Getting Started

1. Clone this repository to your local machine.
2. Install the required dependencies using npm or yarn:

   ```bash
   npm install
   ```

3. Start the GraphQL server:
   ```bash
   npm start
   ```

   Your GraphQL server is now running on http://localhost:5000/graphql

## Schema
  
  **Books**

  * **`id`**: Unique identifier for the book.
  * **`name`**: Name of the book.
  * **`genre`**: Genre of the book.
  * **`authorId`**: ID of the author associated with the book.
  
  **Authors**
  
  * **`id`**: Unique identifier for the author.
  * **`name`**: Name of the author.

## Mutations

  **Add a Book**
  
  You can use the following mutation to add a new book:
  ```bash
  mutation {
    addBook(name: "New Book", genre: "Fiction", authorId: 1) {
      id
      name
    }
  }
  ```
  
  Replace "New Book", "Fiction", and 1 with your desired book details.
  
  **Add an Author**
  
  You can use the following mutation to add a new author:
  ```bash
  mutation {
    addAuthor(name: "New Author") {
      id
      name
    }
  }
  ```
  
  Replace "New Author" with the desired author's name.

## Example Query

  You can use the following query to fetch books and their authors using the sample data provided in this repository:
  ```bash
  query {
    books {
      name
      genre
      author {
        name
      }
    }
  }
  ```
  
  This query will return a list of books along with their genres and respective authors.
  
  Enjoy using this simplified GraphQL server for managing books and authors!
