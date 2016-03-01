# GraphQL Schema

```graphql
type User {
  id: ID!,
  name: String,
  email: String,
  picture(size: Int = 50): ProfilePicture,
  friends: [User]!
  events: [Event]!
}

type ProfilePicture {
  width: Int!,
  height: Int!,
  url: String!
}

type Event {
  id: ID!,
  title: String!,
  location: String!,
  attendees: [User]!
}

type QueryRoot {
  me: User,
  events: [Event]!
}
```
