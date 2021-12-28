**GraphQL + Deno + Oak Framework + PostgresQL**

# Introduction GraphQL
GraphQL is a query language for APIs and a runtime for fulfilling those queries with your existing data.
The real secret is that GraphQL ensures that the developer and application only loads the relevant and absolute necessary data, even if it's from multiple sources(tables).
GraphQL server returns predicted data in responses that are described in request by the client, so it is fast in loading.

  **Describe your data**
  ```
   type User {
      userName: String
      email: String
      address: String
      pincode: Int
    }
 ``` 
 
 **Ask for what you want**
 ```     
      {
          User(name: "Krishna") {
            userName
          }
        }
 ```
  **Get predictable results**    
  ```
   {
      "User": {
        "UserName": "Krishna"
      }
    }

  ```
