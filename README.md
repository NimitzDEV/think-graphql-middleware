# think-graphql-middleware

> A ThinkJS middleware that handles GraphQL queries, built atop apollo-server-core.

#### Install

```bash
npm install think-graphql-middleware --save
```

#### Usage

Require the middleware at `src/config/middleware.js`

```javascript
const graphql = require('think-graphql-middleware');
```

Set-up `match` for your desired GraphQL endpoint, and use `graphql` for `handle` parameter.

```javascript
{
    match: '/graphql',
    handle: graphql,
    options: {}
}
```

Then pass your `GraphQLSchema`instance to `schema` option. 

```javascript
options: {
    schema: schemaInstant
}
```

#### More details

This middleware is based on `apollo-server-core`,  more usages can be found at the [Apollo Official Site.](https://www.apollographql.com/docs/apollo-server/api/apollo-server.html)