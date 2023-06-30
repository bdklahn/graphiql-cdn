# graphiql-cdn
Example GraphiQL web page to access Github's Graphql API.

This is adapted from [here](https://github.com/graphql/graphiql/blob/main/examples/graphiql-cdn/index.html). This "cdn" (Content Delivery Network) example version dynamically pulls the required Javascript from url, vs. using code on the local filesystem (e.g. installed via NodeJS).

The example queries were found [here](https://gist.github.com/MichaelCurrin/6777b91e6374cdb5662b64b8249070ea).

Just make a copy of index_example.html, edit to put in your Github token, and open in your web browser.

e.g.:
```bash
cp index_example.html index.html
# edit to add your token
google-chrome index.html
```
**Don't expose your edited file with your token to anywhere others might see it, like a web site or Github repository.** This is only a quick way to get a **local** "app" to interactively create valid GraphQL queries. Ideally the code might be written to dynamically get a token from the local environment. But a browser process might not have access to that. Thus you'd have to add more code/library which can do that.