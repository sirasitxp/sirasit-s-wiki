
# What is GraphQL
GraphQL is a query language for your API, and a server-side runtime for executing queries using a type system you define for your data. GraphQL isn't tied to any specific database or storage engine and is instead backed by your existing code and data.
A GraphQL service is created by defining types and fields on those types, then providing functions for each field on each type.

# Queries Vs Mutations

## What is Queries?
A GraphQL operation can either be a read or a write operation. A GraphQL query is used to read or fetch values while a mutation is used to write or post values. In either case, the operation is a simple string that a GraphQL server can parse and respond to with data in a specific format. The popular response format that is usually used for mobile and web applications is JSON.

### Syntax
```graphql
//syntax 1
query query_name{ someField }

//syntax 2
{ someField }
```

### Example
```graphql
//query with name myQuery
query myQuery{
   greeting
}

// query without any name
{
   greeting
}
```

## What is Mutations?
Mutation queries modify data in the data store and returns a value. It can be used to insert, update, or delete data. Mutations are defined as a part of the schema.

### Syntax
```graphql
mutation{
someEditOperation(dataField:"valueOfField"):returnType
}
```
### Example
```graphql
type Mutation {
  createLink(category: String!, description: String!, imageUrl: String!, title: String!, url: String!): Link!
  deleteLink(id: String!): Link!
  updateLink(category: String, description: String, id: String, imageUrl: String, title: String, url: String): Link!
}
```
## What is Resolvers?
Resolvers is an object where you will define the implementation for each query and mutation.
Resolver is a collection of functions that generate response for a GraphQL query. In simple terms, a resolver acts as a GraphQL query handler. Every resolver function in a GraphQL schema accepts four positional arguments as given below.

```graphql
fieldName:(root, args, context, info) => { result }
```
