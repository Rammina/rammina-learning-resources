Happy new week, everyone!

Ugh, Mondays... the day that ends a lot of people's fun and freedom. However, I'm on the 100 Days of Code and Scrum challenge, so I can't exactly stop coding on the weekends. But I have to admit, I'm kind of lazy today.

I have to deal with 2 interviews, and I am a little bit worried about them. Also, I should be studying GraphQL, because it is part of my weekly goal.

## Yesterday

I learned how to setup GraphQL, specifically ApolloClient for React frontend. I managed to set that up and have it connect to my React application, but I still couldn't really understand what it was about.

## Today

Well, I had to decline a technical interview (because refusing it is a better use of my time), and I passed a phone screening. I managed to continue learning about GraphQL, and I believe I now know some answers to my questions yesterday. And of course, I also continued to expand my network.

Here are some of the things I've learned:

### GraphQL

- `ApolloClient` is a constructor that creates an instance of an ApolloClient, and it returns an initialized ApolloClient object
- `createHttpLink` is constructor function that returns a ApolloLink
- `createHttpLink` creates the HTTP link that connects the Apollo client with the GraphQL API
- practiced query and mutation using the GraphQL playground

This here is an example of `client` initialization using `ApolloClient`

```
  const client = new ApolloClient({
    link: httpLink,
    cache: new InMemoryCache()
  });
```

### Scrum

- a Sprint can be canceled if Sprint Goal becomes obsolete or cannot be achieved
- when a Sprint is canceled, these can happen:
  - any completed and "done" Product Backlog Items will be reviewed
  - the Product Owner typically accepts potentially releasable work
  - all incomplete Product Backlog Items will be re-estimated and put back on the PB

I'm still having a difficulty with useQuery and useMutation, and I'm not sure if I should initialize the definitions on a different file/folder to keep them clean.

How is everyone doing in their learning journey? Feel free to chat with me in the comments and/via DM!

### DISCLAIMER

This post only expresses my thoughts and opinions (based on my limited knowledge) and is in no way a substitute for actual references. If I ever make a mistake or if you disagree, I would appreciate corrections in the comments!
