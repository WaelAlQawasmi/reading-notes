## GraphQL @connection
- we can create relations between the tables in GraphQL
- So we can  one-to-many relation in  GraphQL using **@hasMany**  between two models

- example
> type Post @model {

> id: ID!

> title: String!

> comments: [Comment] @hasMany
}

> type Comment @model {
id: ID!
content: String!
}

## Completable Future
- CompltableFuture It  a class in Java belongs to java.util.cocurrent package it implements CompletionStage and Future interface.
- we can use it for asynchronous programming(writing non-blocking code)
It runs separated task on a one thread than the main app thread and make the
 main thread notifies  about its , completion or failure, in this case  the main thread does not block
 but the other tasks execute in parallel


### resources
* [docs amplify aws](https://docs.amplify.aws/cli/graphql/data-modeling/#belongs-to-relationship)
* [javatpoint](https://www.javatpoint.com/completablefuture-in-java)
* [baeldung](https://www.baeldung.com/java-completablefuture)