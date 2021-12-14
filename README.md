# SubQuery - Account Transfer Reverse Lookup (Hero course module #3.6)

## this project is based on the repository of exercice #3.2 (Account Transfer)
the base project address is https://github.com/arnobase/subquery-tutorials-account-transfer
this is my personnal git repository, I used this one because it's based on the v0.2.0 starter package, instead of the v0.0.1 used by the repository mentioned in the excercice

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

##### Accounts with "myToAddress"
````graphql
query{
	accounts(first:5){
		nodes{
			id
			myToAddress{
				nodes{
					id
					amount
				}
			}
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