jenkins-graphql
===============

GraphQL server for Jenkins API

-	https://github.com/graphql/graphql-js
-	https://github.com/rmosolgo/graphql-ruby
-	https://blog.risingstack.com/graphql-overview-getting-started-with-graphql-and-nodejs/
-	https://github.com/RisingStack/graphql-server
-	https://github.com/RisingStack/graffiti
-	https://github.com/RisingStack/graffiti-example

Use [Octokat.js](https://github.com/philschatz/octokat.js) API wrapper for a nice DSL.

This project will integrate with [Github-graphQL]() project

Perhaps use Mongoose to store github data with project data. Can we then simply use graffiti to expose entire data model as GraphQL?

```js
var koa = require('koa');
var graffiti = require('@risingstack/graffiti');
var graffitiMongoose = require('@risingstack/graffiti-mongoose');

var app = koa();
app.use(graffiti.koa({
  prefix: '/graphql',
  adapter: graffitiMongoose,
  models: []
}));

app.listen(3000);
```
