

:-Create Database and Collection



&#x20;  use spotifyDB

&#x20;  db.createCollection("playlists")



:-Create restaurant collection



&#x20;  db.createCollection("zomatoRestaurants")



:-Insert Sample Restaurant Data



db.zomatoRestaurants.insertMany(\[

{

&#x20;   name: "Spice Villa",

&#x20;   cuisine: "Indian",

&#x20;   rating: 4.7

},

{

&#x20;   name: "Little Italy",

&#x20;   cuisine: "Italian",

&#x20;   rating: 4.5

},-

{

&#x20;   name: "Dragon Wok",

&#x20;   cuisine: "Chinese"

&#x20;   rating: 4.3

},

{

&#x20;   name: "Burger Hub",

&#x20;   cuisine: "Fast Food",

&#x20;   rating: 4.2

},

{

&#x20;   name: "Pizza Palace",

&#x20;   cuisine: "Italian",

&#x20;   rating: 4.8

},

{

&#x20;   name: "Cafe Coffee",

&#x20;   cuisine: "Cafe",

&#x20;   rating: 4.4

},

{

&#x20;   name: "South Spice",

&#x20;   cuisine: "South Indian",

&#x20;   rating: 4.6

},

{

&#x20;   name: "Royal Biryani",

&#x20;   cuisine: "Hyderabadi",

&#x20;   rating: 4.9

},

{

&#x20;   name: "Mexican Fiesta",

&#x20;   cuisine: "Mexican",

&#x20;   rating: 4.1

},

{

&#x20;   name: "Sushi House",

&#x20;   cuisine: "Japanese",

&#x20;   rating: 4.5

}

]);



:- Verify Data



&#x20;  db.zomatoRestaurants.find().pretty();

&#x20;  db.zomatoRestaurants.countDocuments();





\-> Next we have export Collection:

&#x20;    " mongoexport --db=spotifyDB --collection=zomatoRestaurants --out=restaurants.json --jsonArray"



\-->Next we have to create MongoDB Atlas Cluster where we create database "instaClone",then 

&#x20;  we have to create username password ,Allow your IP address.

&#x20;  Copy the Atlas connection string. ex: (mongodb+srv://atlasUser:Atlas@123@cluster0.xxxxx.mongodb.net/).



\-->Now we import into Atlas:

&#x20;   (mongoimport --uri="mongodb+srv://atlasUser:Atlas@123@cluster0.xxxxx.mongodb.net/instaClone" 

&#x20;    --collection=zomatoRestaurants --file=restaurants.json --jsonArray)

&#x20;   - we replace with default username or password with our credential.



\-->Verify Data:
     use instaClone

&#x20;    show collections

&#x20;    db.zomatoRestaurants.find().pretty() 

&#x20;    db.zomatoRestaurants.countDocuments()

   

