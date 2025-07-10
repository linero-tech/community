## Background
The workflows that automatically sets the label to each discussion requires to know the id of each label. To get such ids, we need to go here: `https://docs.github.com/en/graphql/overview/explorer` and run the following query:

```
query {
  repository(owner: "linero-tech", name: "community") {
    labels(first: 100) {
      nodes {
        name
        id
      }
    }
  }
}

```