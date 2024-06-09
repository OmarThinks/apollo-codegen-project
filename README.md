# apollo-codegen-project

Generating react hooks using apollo codegen

## Code:

Schema:

```graphql
type User {
  id: ID!
  name: String!
}

type Query {
  users: [User!]!
  user(id: ID!): User
}

type Mutation {
  createUser(name: String!): User!
}

schema {
  query: Query
  mutation: Mutation
}
```

## Queries:

```graphql
query GetUsers {
  users {
    id
    name
  }
}
```

## Mutations:

```graphql
mutation CreateUser($name: String!) {
  createUser(name: $name) {
    id
    name
  }
}
```

## To generate the hooks:

```bash
cd app
npm run generate
```

# Final Result:

https://github.com/OmarThinks/apollo-codegen-project/blob/master/app/src/graphql/generated/graphql.tsx
