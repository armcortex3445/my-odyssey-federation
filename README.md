# Tutorial memo

## How to local run 

1. run all subgraph server without using 4002 port.
2. run below command on root project.

```sh
rover dev --supergraph-config ./router/supergraph-config.yaml --supergraph-port 4002
```

## How to use rover

### schema checking
- use `rover subgraph check` to run build checks, operation checks, linter checks.
- below command is example. so you need to change `--schema` option to your schema path and `--name` options to your subgraph name published on your Apollo studio 

```sh
rover subgraph check <APOLLO_GRAPH_REF> \
  --schema <SCHEMA_FILE_PATH> \
  --name <SUBGRAPH_NAME>
```

### publishing

- when you want to publish subgraph for registration or updating, use `rover subgraph publish`

```sh
rover subgraph publish <APOLLO_GRAPH_REF> \
  --schema <SCHEMA_FILE_PATH> \
  --name <SUBGRAPH_NAME>
  ----routing-url <SUBGRAPH_SERVER_URL>
```

# (Odyssey Course) Federation with TypeScript
Welcome to the starter code for **Federation with TypeScript**. You can find the [course lessons and instructions](https://apollographql.com/tutorials/federation-typescript) on Odyssey, [Apollo](https://apollographql.com)'s learning platform.

## How to use this repo

The course will walk you step by step on what to do. This codebase is the starting point of your journey!

In order to install and run the project locally, navigate into the `listings` directory and run:

```shell
npm install && npm run dev
```

Right now, `listings` is a GraphQL server returning listing and amenity data at `http://localhost:4000`. You can visit `http://localhost:4000` directly, or use [Apollo Sandbox](https://studio.apollographql.com/sandbox?endpoint=http://localhost:5059/graphql) to connect to the endpoint and send queries.

Try running this query:

```graphql
query GetFeaturedListings {
  featuredListings {
    id
    title
    description
    amenities {
      id
      name
      category
    }
  }
}
```

The `final` branch of this repo contains the final stage of the course, with all of the steps and code completed! If you get stuck, you can refer to it and compare your code.

## Getting Help

This repo is _not regularly monitored_.

For any issues or problems concerning the course content, please refer to the [Odyssey topic in our community forums](https://community.apollographql.com/tags/c/help/6/odyssey). You can also [join the Apollo Discord](https://discord.gg/graphos).
