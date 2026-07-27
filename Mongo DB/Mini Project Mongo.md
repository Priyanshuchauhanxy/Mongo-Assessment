##### **Mini Project**



\-Create Database

\-use quickeats\_db



&#x20;

* **RESTAURANTS COLLECTION** 



db.restaurants.insertMany(\[

{

&#x20;   restaurantId: 1,

&#x20;   name: "Spice Hub",

&#x20;   cuisine: "Indian",

&#x20;   rating: 4.6,

&#x20;   address: {

&#x20;       city: "Ahmedabad",

&#x20;       area: "Navrangpura"

&#x20;   },

&#x20;   menu: \[

&#x20;       { itemId: 101, name: "Paneer Butter Masala", price: 250, category: "Main Course" },

&#x20;       { itemId: 102, name: "Butter Naan", price: 40, category: "Bread" },

&#x20;       { itemId: 103, name: "Jeera Rice", price: 120, category: "Rice" }

&#x20;   ]

},

{

&#x20;   restaurantId: 2,

&#x20;   name: "Pizza Planet",

&#x20;   cuisine: "Italian",

&#x20;   rating: 4.4,

&#x20;   address: {

&#x20;       city: "Ahmedabad",

&#x20;       area: "Satellite"

&#x20;   },

&#x20;   menu: \[

&#x20;       { itemId: 201, name: "Margherita Pizza", price: 299, category: "Pizza" },

&#x20;       { itemId: 202, name: "Veg Supreme Pizza", price: 399, category: "Pizza" },

&#x20;       { itemId: 203, name: "Garlic Bread", price: 149, category: "Sides" }

&#x20;   ]

},

{

&#x20;   restaurantId: 3,

&#x20;   name: "Dragon Bowl",

&#x20;   cuisine: "Chinese",

&#x20;   rating: 4.5,

&#x20;   address: {

&#x20;       city: "Ahmedabad",

&#x20;       area: "CG Road"

&#x20;   },

&#x20;   menu: \[

&#x20;       { itemId: 301, name: "Hakka Noodles", price: 180, category: "Noodles" },

&#x20;       { itemId: 302, name: "Manchurian", price: 220, category: "Starter" },

&#x20;       { itemId: 303, name: "Fried Rice", price: 190, category: "Rice" }

&#x20;   ]

},

{

&#x20;   restaurantId: 4,

&#x20;   name: "Burger Town",

&#x20;   cuisine: "Fast Food",

&#x20;   rating: 4.3,

&#x20;   address: {

&#x20;       city: "Ahmedabad",

&#x20;       area: "Maninagar"

&#x20;   },

&#x20;   menu: \[

&#x20;       { itemId: 401, name: "Veg Burger", price: 120, category: "Burger" },

&#x20;       { itemId: 402, name: "French Fries", price: 90, category: "Sides" },

&#x20;       { itemId: 403, name: "Cold Coffee", price: 110, category: "Drink" }

&#x20;   ]

},

{

&#x20;   restaurantId: 5,

&#x20;   name: "Healthy Bites",

&#x20;   cuisine: "Healthy",

&#x20;   rating: 4.8,

&#x20;   address: {

&#x20;       city: "Ahmedabad",

&#x20;       area: "Prahlad Nagar"

&#x20;   },

&#x20;   menu: \[

&#x20;       { itemId: 501, name: "Caesar Salad", price: 220, category: "Salad" },

&#x20;       { itemId: 502, name: "Fruit Bowl", price: 180, category: "Dessert" },

&#x20;       { itemId: 503, name: "Green Smoothie", price: 150, category: "Drink" }

&#x20;   ]

}

]);





* **ORDERS COLLECTION**



db.orders.insertMany(\[

{

&#x20;   orderId: 1001,

&#x20;   customerId: 1,

&#x20;   restaurantId: 1,

&#x20;   restaurantName: "Spice Hub",

&#x20;   status: "Delivered",

&#x20;   totalAmount: 330,

&#x20;   items: \[

&#x20;       { name: "Paneer Butter Masala", quantity: 1, price: 250 },

&#x20;       { name: "Butter Naan", quantity: 2, price: 40 }

&#x20;   ]

},

{

&#x20;   orderId: 1002,

&#x20;   customerId: 2,

&#x20;   restaurantId: 2,

&#x20;   restaurantName: "Pizza Planet",

&#x20;   status: "Preparing",

&#x20;   totalAmount: 448,

&#x20;   items: \[

&#x20;       { name: "Margherita Pizza", quantity: 1, price: 299 },

&#x20;       { name: "Garlic Bread", quantity: 1, price: 149 }

&#x20;   ]

},

{

&#x20;   orderId: 1003,

&#x20;   customerId: 3,

&#x20;   restaurantId: 3,

&#x20;   restaurantName: "Dragon Bowl",

&#x20;   status: "Out for Delivery",

&#x20;   totalAmount: 400,

&#x20;   items: \[

&#x20;       { name: "Hakka Noodles", quantity: 1, price: 180 },

&#x20;       { name: "Manchurian", quantity: 1, price: 220 }

&#x20;   ]

},

{

&#x20;   orderId: 1004,

&#x20;   customerId: 4,

&#x20;   restaurantId: 4,

&#x20;   restaurantName: "Burger Town",

&#x20;   status: "Delivered",

&#x20;   totalAmount: 330,

&#x20;   items: \[

&#x20;       { name: "Veg Burger", quantity: 2, price: 120 },

&#x20;       { name: "French Fries", quantity: 1, price: 90 }

&#x20;   ]

},

{

&#x20;   orderId: 1005,

&#x20;   customerId: 5,

&#x20;   restaurantId: 5,

&#x20;   restaurantName: "Healthy Bites",

&#x20;   status: "Pending",

&#x20;   totalAmount: 370,

&#x20;   items: \[

&#x20;       { name: "Caesar Salad", quantity: 1, price: 220 },

&#x20;       { name: "Green Smoothie", quantity: 1, price: 150 }

&#x20;   ]

}

]);



* **CUSTOMERS COLLECTION**



db.customers.insertMany(\[

{

&#x20;   customerId: 1,

&#x20;   name: "Rahul Sharma",

&#x20;   loyaltyPoints: 100,

&#x20;   addresses: \[

&#x20;       {

&#x20;           type: "Home",

&#x20;           city: "Ahmedabad",

&#x20;           area: "Navrangpura"

&#x20;       }

&#x20;   ]

},

{

&#x20;   customerId: 2,

&#x20;   name: "Priya Patel",

&#x20;   loyaltyPoints: 50,

&#x20;   addresses: \[

&#x20;       {

&#x20;           type: "Home",

&#x20;           city: "Ahmedabad",

&#x20;           area: "Satellite"

&#x20;       }

&#x20;   ]

},

{

&#x20;   customerId: 3,

&#x20;   name: "Amit Verma",

&#x20;   loyaltyPoints: 80,

&#x20;   addresses: \[

&#x20;       {

&#x20;           type: "Home",

&#x20;           city: "Ahmedabad",

&#x20;           area: "CG Road"

&#x20;       }

&#x20;   ]

},

{

&#x20;   customerId: 4,

&#x20;   name: "Neha Shah",

&#x20;   loyaltyPoints: 120,

&#x20;   addresses: \[

&#x20;       {

&#x20;           type: "Home",

&#x20;           city: "Ahmedabad",

&#x20;           area: "Maninagar"

&#x20;       }

&#x20;   ]

},

{

&#x20;   customerId: 5,

&#x20;   name: "Karan Mehta",

&#x20;   loyaltyPoints: 60,

&#x20;   addresses: \[

&#x20;       {

&#x20;           type: "Home",

&#x20;           city: "Ahmedabad",

&#x20;           area: "Prahlad Nagar"

&#x20;       }

&#x20;   ]

}

]);





* **READ QUERIES**



&#x20;1. Restaurants with rating greater than 4 :

db.restaurants.find(

&#x20;   { rating: { $gt: 4 } },

&#x20;   { \_id: 0, name: 1, cuisine: 1, rating: 1 }

);



&#x20;2. Orders with Delivered or Preparing status :

db.orders.find(

&#x20;   { status: { $in: \["Delivered", "Preparing"] } },

&#x20;   { \_id: 0, orderId: 1, status: 1, totalAmount: 1 }

);



&#x20;3. Customers from Ahmedabad :

db.customers.find(

&#x20;   { "addresses.city": { $eq: "Ahmedabad" } },

&#x20;   { \_id: 0, name: 1, addresses: 1 }

);



&#x20;4. Restaurants with rating less than 4.5 :

db.restaurants.find(

&#x20;   { rating: { $lt: 4.5 } },

&#x20;   { \_id: 0, name: 1, rating: 1 }

);



* **UPDATE OPERATIONS**





&#x20;Update order status

db.orders.updateOne(

&#x20;   { orderId: 1002 },

&#x20;   { $set: { status: "Delivered" } }

);

&#x20;Append delivery log

db.orders.updateOne(

&#x20;   { orderId: 1002 },

&#x20;   {

&#x20;       $push: {

&#x20;           deliveryLog: {

&#x20;               time: new Date(),

&#x20;               message: "Order Delivered Successfully"

&#x20;           }

&#x20;       }

&#x20;   }

);

&#x20;Increment loyalty points

db.customers.updateOne(

&#x20;   { customerId: 1 },

&#x20;   { $inc: { loyaltyPoints: 50 } }

);





&#x20;**- AGGREGATION PIPELINE**





db.orders.aggregate(\[

&#x20;   {

&#x20;       $match: {

&#x20;           status: "Delivered"

&#x20;       }

&#x20;   },

&#x20;   {

&#x20;       $group: {

&#x20;           \_id: "$restaurantName",

&#x20;           totalRevenue: { $sum: "$totalAmount" },

&#x20;           totalOrders: { $sum: 1 }

&#x20;       }

&#x20;   },

&#x20;   {

&#x20;       $project: {

&#x20;           \_id: 0,

&#x20;           restaurantName: "$\_id",

&#x20;           totalRevenue: 1,

&#x20;           totalOrders: 1

&#x20;       }

&#x20;   },

&#x20;   {

&#x20;       $sort: {

&#x20;           totalRevenue: -1

&#x20;       }

&#x20;   }

]);



&#x20;**- INDEXING :**

db.orders.find(

&#x20;   {

&#x20;       customerId: 1,

&#x20;       status: "Delivered"

&#x20;   }

).explain("executionStats");



&#x20;Create compound index:

db.orders.createIndex({

&#x20;   customerId: 1,

&#x20;   status: 1

});



&#x20;Explain AFTER creating index:

db.orders.find(

&#x20;   {

&#x20;       customerId: 1,

&#x20;       status: "Delivered"

&#x20;   }

).explain("executionStats");



* **VERIFY DATA**



show collections;



db.restaurants.find().pretty();



db.orders.find().pretty();



db.customers.find().pretty();

