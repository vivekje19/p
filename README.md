**GraphQL + Deno + Oak Framework + PostgresQL**
<table>
  <thead>
    <tr>
      <th>Describe your data</th>
      <th>Ask for what you want</th>
      <th>Get predictable results</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        type Project {
          name: String
          tagline: String
          contributors: [User]
        }
      </td>
      <td>
         {
          project(name: "GraphQL") {
            tagline
          }
        }
      </td>
      <td>
        {
            "project": {
              "tagline": "A query language for APIs"
            }
          }
      </td>
    </tr>
  </tbody>
  </table>
