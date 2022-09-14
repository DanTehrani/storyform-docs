# GraphQL API

All the forms and submissions reside on [Arweave](http://arweave.org), a decentralized storage network. You can retrieve forms and submissions using [Arweave's GraphQL API endpoint](https://arweave.net/graphql), with parameters described below. Alternatively, you can use [arweave-js](https://github.com/ArweaveTeam/arweave-js) to query using JavaScript.

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
        "StoryForm"
      ],
      "op": "EQ"
    },
    {
      "name": "Form-Id",
      "values": [
        "e9bdca2f07515aafeeab712bef57d79097f78a6ef43869994b9712b9bf8dbbcf"
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
