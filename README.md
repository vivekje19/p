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
  
  # Schemas, resolvers, and other common GraphQL terms
  - **Schemas:**  GraphQL describes the functionality available to the client applications that connect to it. A GraphQL schema is made up of object types, which define which kind of object you can request and what fields it has.As queries come in, GraphQL validates the queries against the schema. GraphQL then executes the validated queries. 
```
User Schema
 type User {
    userName: String
    email: String
    address: String
    pincode: Int
  }
  ```
  - **Resovers:** 
 Resolver is a collection of functions that generate response for a GraphQL query. In simple terms, a resolver acts as a GraphQL query handler.

```
fieldName:(root, args, context, info) => { result }

```
<table>
<tbody><tr>
<th style="text-align:center; width:12%;">Sr.No.</th>
<th style="text-align:center;">Arguments &amp; Description</th>
</tr>
<tr>
<td class="ts">1</td>
<td><p><b>root</b></p>
<p>The object that contains the result returned from the resolver on the parent field.</p></td>
</tr>
<tr>
<td class="ts">2</td>
<td><p><b>args</b></p>
<p>An object with the arguments passed into the field in the query.</p></td>
</tr>
<tr>
<td class="ts">3</td>
<td><p><b>context</b></p>
<p>This is an object shared by all resolvers in a particular query.</p></td>
</tr>
<tr>
<td class="ts">4</td>
<td><p><b>info</b></p>
<p>It contains information about the execution state of the query, including the field name, path to the field from the root.</p></td>
</tr>
</tbody></table>
  
  # Working engine of GraphQL
  <img src="https://www.red-gate.com/simple-talk/wp-content/uploads/2021/10/word-image-4.png" />
