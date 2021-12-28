**GraphQL + Deno + Oak Framework + PostgresQL**

# Introduction GraphQL
GraphQL is a query language for APIs, not a database and a runtime for fulfilling application queries with existing data.
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
