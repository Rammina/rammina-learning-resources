Good morning, everyone!

Today, it could be pretty challenging to keep up with the 100 days of code challenge because of impediments. Not only am sleep-deprived, I also have to go out for five hours for my weekly physical therapy session, as well as buy some groceries.

However, I will do my best to commit to my plans!

## Yesterday

I began to finally understand ApolloProvider, ApolloClient, createHttpLink, and InMemoryCache. I also practiced useQuery and useMutation, but I couldn't understand them yet.

## Today

Pretty rough day and I got distracted a lot, but I managed to commit anyway!

Here are some of the things I've learned:

### GraphQL

- I prefer making a `graphql` folder to separate the definitions, it also makes my files cleaner and organized
- `useQuery` - used to retrieve data from the server. it takes in a query document and returns `loading`, `error`, and `data`.
  - `data` - typically is what the frontend developer is concerned, which contains the data retrieved from the server
  - `error` - if ever the request fails, it will contain information about what went wrong
  - `loading` - indicates whether the request is ongoing if it's `true`
- `useMutation` - used to change data in the server, it takes in a mutation document and `options` object as the second parameter which contains properties such as `variables`

### Scrum

The Scrum Master serves the Product Owner in several ways, including:

- Ensuring that goals, scope, and product domain are understood by everyone on the Scrum Team as well as possible
- Finding techniques for effective Product Backlog management
- Helping the Scrum Team understand the need for clear and concise Product Backlog items
- Understanding product planning in an empirical environment
- Ensuring the Product Owner knows how to arrange the Product Backlog to maximize value
- Understanding and practicing agile practices
- Facilitating Scrum events as requested or needed

How is everyone doing in their learning journey? Feel free to chat with me in the comments and/via DM!

### DISCLAIMER

This post only expresses my thoughts and opinions (based on my limited knowledge) and is in no way a substitute for actual references. If I ever make a mistake or if you disagree, I would appreciate corrections in the comments!
