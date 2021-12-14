# SubQuery - Account Transfer (Hero course module #3.2)

# This project uses the subquery Starter Package v0.2.0
follow guidelines in https://github.com/subquery/subql-starter/tree/v0.2.0 to install

#### Query the project

Open your browser and head to `http://localhost:3000`.

##### Accounts
````graphql
query{
  accounts(first: 3){
    nodes{
      id
    }
  }
}
````
##### Transfers
````graphql
query{
  transfers(first: 3){
    nodes{
      id
      amount
      blockNumber
    }
  }
}
````
##### Transfers and display “to” address
````graphql
query{
  transfers(first: 3){
    nodes{
      id
      amount
      blockNumber
      to{
        id
      }
    }
  }
}
````