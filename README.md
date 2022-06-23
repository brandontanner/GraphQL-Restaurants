# GraphQL Restaurants

### Description

This program demostrates how to create, read, update, and delete data using GraphQL. For this example, we are using restaurants: creating new restaurants, reading information about the restaurants, updating their information, and deleting them from the list of restaurants. This takes place in the GraphQL playground and allows for better understanding and exploration of how to manipulate and utilize GraphQL.

### How to Run

1. Download the zip file in github and navigate to the **GraphQL-Restaurants-main** directory in the terminal.
2. Run `npm install`.
3. Run `node index.js`.
4. When that is complete, load **localhost:5500/graphql** in the browser. This will load the project in the browser.
5. Paste the following on the left-hand side: 
`mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    name: "Granite",
    description: "American",
  }) {
    name
    description
  }
}

mutation deleterestaurants($iid: Int!) {
  deleterestaurant(id: $iid) {
    ok
  }
}

query getrestaurants {
  restaurants {
    name
    description
    dishes {
      name
      price
    }
  }
}

query findrestaurant($iidd:Int!) {
  restaurant(id:$iidd){
    name
    description
    dishes {
      name
      price
    }
  }
}`
6. Paste the following on the left-hand side under **query variables**:
`{
  "iid": 0,
  "idd": 0,
  "iidd": 1
}`
7. Run the program by clicking the play button at the top and clicking a query or mutation you would like to run.

### Roadmap of Future Improvements

- **Update more information** - I plan to add the ability to update each element of each restaurant rather than only a few of the properties. 
- **Connecting to a Database** - Currently, this program is not connected to an actual database. I plan to create and connect this to a database in the future to broaden the scope of this program. 

### License Information
Completed as an assignment for the [MIT Professional Certificate in Coding: Full Stack Development with MERN](https://executive-ed.xpro.mit.edu/professional-certificate-coding?utm_source=Google&utm_medium=c&utm_term=mit%20coding&utm_location=1027726&utm_campaign=B-365D_US_GG_SE_PCC_Brand&utm_content=MIT-Coding___School_Duration&gclid=Cj0KCQiAweaNBhDEARIsAJ5hwbe5iGViYiDsRYlBGKAHHLbH-GiiJ16dKOBbV7tvosiu9UTfbS7tAygaAkW1EALw_wcB).

See [MIT license](https://github.com/brandontanner/GraphQL-Restaurants/blob/main/LICENSE).
