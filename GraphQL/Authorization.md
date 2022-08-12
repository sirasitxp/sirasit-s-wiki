# Authorization
In express.js (and other Node.js frameworks) we use middleware for this, like passport.js or the custom ones. However, in GraphQL's resolver architecture we don't have middleware so we have to imperatively call the auth checking function and manually pass context data to each resolver, which might be a bit tedious.

## How to use
First, we need to use the @Authorized decorator as a guard on a field, query or mutation.
```graphql
@ObjectType()
class MyObject {
  @Field()
  publicField: string;

  @Authorized()
  @Field()
  authorizedField: string;

  @Authorized("ADMIN")
  @Field()
  adminField: string;

  @Authorized(["ADMIN", "MODERATOR"])
  @Field({ nullable: true })
  hiddenField?: string;
}
```
