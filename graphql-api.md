# GraphQL API

All surveys and submissions reside on [Arweave](http://arweave.org), a decentralized storage network. You can retrieve surveys and submissions using [Arweave's GraphQL API endpoint](https://arweave.net/graphql), with the parameters described below. Alternatively, you can use [arweave-js](https://github.com/ArweaveTeam/arweave-js) to query using JavaScript.

You can use the following tags in combination to filter data.

* App-Name: Storyform
* Type: Form | Submission
* Form-Id: \[formId]
* For example, you can retrieve the first 10 submissions of a form as follows:

Query

```graphql
query transactions($first: Int!, $after: String, $tags: [TagFilter!]) {
  transactions(first: $first, after: $after, tags: $tags) {
    edges {
      node {
        id
        tags {
            name
            value
        }
      }
    }
  }
}
```

Variables

```json
{
  "first": 10,
  "tags": [
    {
      "name": "App-Id",
      "values": [
        "Storyform"
      ],
      "op": "EQ"
    },
    {
      "name": "Form-Id",
      "values": [
        "0x0b68bb57437fcc55850af68abe42cc45c72e2ec3030fa6074d44a43af51442c1"
      ],
      "op": "EQ"
    },
    {
      "name": "Type",
      "values": [
        "Submission"
      ],
      "op": "EQ"
    }
  ]
}
```
