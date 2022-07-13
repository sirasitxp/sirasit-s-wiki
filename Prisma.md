# Prisma

## What is Prisma?
Prisma is an open-source ORM that allows you to connect with database.

## What is ORM?
Object–relational mapping (ORM, O/RM, and O/R mapping tool) in computer science is a programming technique for converting data between type systems using object-oriented programming languages.

## What is REST API
Representational State Transfer (REST) is a software architecture that imposes conditions on how an API should work. REST was initially created as a guideline to manage communication on a complex network like the internet.

### How do RESTful APIs work?
The basic function of a RESTful API is the same as browsing the internet. The client contacts the server by using the API when it requires a resource. API developers explain how the client should use the REST API in the server application API documentation. These are the general steps for any REST API call:
The client sends a request to the server. The client follows the API documentation to format the request in a way that the server understands.
The server authenticates the client and confirms that the client has the right to make that request.
The server receives the request and processes it internally.
The server returns a response to the client. The response contains information that tells the client whether the request was successful. The response also includes any information that the client requested.

## What is GraphQL API
GraphQL is a query language for your API, and a server-side runtime for executing queries using a type system you define for your data. GraphQL isn't tied to any specific database or storage engine and is instead backed by your existing code and data.

## What is Database Seeding?
Database seeding is populating a database with an initial set of data. It's common to load seed data such as initial user accounts or dummy data upon initial setup of an application.

## Creating Database
```prisma
npx prisma db push
```

## Seeding Database
```prisma
npx prisma db seed --preview-feature
```

## What is Mutations?
Mutation queries modify data in the data store and returns a value. It can be used to insert, update, or delete data. Mutations are defined as a part of the schema.

### Syntax
```prisma
mutation{
someEditOperation(dataField:"valueOfField"):returnType
}
```
### Example
``` 
type Mutation {
  createLink(category: String!, description: String!, imageUrl: String!, title: String!, url: String!): Link!
  deleteLink(id: String!): Link!
  updateLink(category: String, description: String, id: String, imageUrl: String, title: String, url: String): Link!
}
```
## What is Resolvers?
Resolvers is an object where you will define the implementation for each query and mutation.



