**GraphQL + Deno + Oak Framework + PostgresQL**

# Introduction GraphQL
GraphQL is a query language for APIs, not a database and a runtime for fulfilling application queries with existing data.
The real secret is that GraphQL ensures that the developer and application only loads the relevant and absolute necessary data, even if it's from multiple sources(tables).
GraphQL server returns predicted data in responses that are described in request by the client, so it is fast in loading.

GraphQL gives permission to the client that what do they want to fetch the exact data, but the client only fetches the data by a query that is described in the schema of the requested query on the server.

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
          User {
            userName
            email
          }
        }
 ```
  **Get predictable results**    
  ```
   {
      "User": {
        "UserName": "Krishna",
        "email": "krishna@gmail.com"
      },
      {
        "UserName": "Ram",
        "email": "ram@gmail.com"
      }
    }

  ```
  
  <img src="https://lighthouse-php.com/assets/img/flow.f9dcf86d.png" />
