# postgraphile-upsert-plugin

add postgres `upsert` mutations to [postgraphile](https://www.graphile.org/postgraphile)

## install

`yarn add postgraphile-upsert-plugin`

## usage

```ts
import { PgMutationUpsertPlugin } from 'postgraphile-upsert-plugin'

postgraphile(pgClient, 'yourSchema', {
  appendPlugins: [PgMutationUpsertPlugin as any]
})
```

fire open `PostGraphiQL` and look for `mutation { upsert<ModelName> { ... } }`

this is a typescript-ified knock off of [the original upsert plugin](https://github.com/einarjegorov/graphile-upsert-plugin/blob/master/index.js)
