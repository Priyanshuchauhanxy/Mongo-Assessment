\--> Create Collection Restaurant:

&#x20; 

use restaurantDB



db.restaurants.insertMany(\[

{

&#x20;   name: "Pizza Palace",

&#x20;   cuisine: "Italian",

&#x20;   location: "Ahmedabad",

&#x20;   rating: 4.7

},

{

&#x20;   name: "Little Italy",

&#x20;   cuisine: "Italian",

&#x20;   location: "Surat",

&#x20;   rating: 4.5

},

{

&#x20;   name: "Dragon Wok",

&#x20;   cuisine: "Chinese",

&#x20;   location: "Ahmedabad",

&#x20;   rating: 4.3

},

{

&#x20;   name: "Spice Villa",

&#x20;   cuisine: "Indian",

&#x20;   location: "Ahmedabad",

&#x20;   rating: 4.8

},

{

&#x20;   name: "Burger Hub",

&#x20;   cuisine: "Fast Food",

&#x20;   location: "Vadodara",

&#x20;   rating: 4.2

},

{

&#x20;   name: "Cafe Delight",

&#x20;   cuisine: "Cafe",

&#x20;   location: "Ahmedabad",

&#x20;   rating: 4.6

},

{

&#x20;   name: "Pizza Corner",

&#x20;   cuisine: "Italian",

&#x20;   location: "Rajkot",

&#x20;   rating: 4.1

},

{

&#x20;   name: "Royal Biryani",

&#x20;   cuisine: "Indian",

&#x20;   location: "Surat",

&#x20;   rating: 4.4

},

{

&#x20;   name: "China Town",

&#x20;   cuisine: "Chinese",

&#x20;   location: "Ahmedabad",

&#x20;   rating: 4.5

},

{

&#x20;   name: "Urban Cafe",

&#x20;   cuisine: "Cafe",

&#x20;   location: "Surat",

&#x20;   rating: 4.0

]);



\- View all restaurants



&#x20; db.restaurants.find().pretty();





\-->Query Italian Restaurants and Measure Execution Time:



&#x20;   db.restaurants.find({

&#x20;   cuisine: "Italian"

&#x20;   }).explain("executionStats");



\-->Create Index on Curisine:



&#x20;  db.restaurants.createIndex({

&#x20;    cuisine: 1

&#x20;  });



&#x20;- Run again



&#x20;    db.restaurants.find({

&#x20;       cuisine: "Italian"

&#x20;    }).explain("executionStats");





\-->Compound Index:



&#x20;   db.restaurants.createIndex({

&#x20;   location: 1,

&#x20;   rating: 1

&#x20;   });



&#x20;- Query Ahmedabad restaurants with rating greater than 4 

&#x20;   

&#x20;  db.restaurants.find({

&#x20;     location:"Ahemdabad",
      rating:{$gt:5}}).explain("executionStats");



\--> Drop All Custom Indexes :
    db.restaurants.dropIndexes();

&#x20;  

&#x20; - Verify remaining indexes 

&#x20;    db.restaurants.getIndexes();

