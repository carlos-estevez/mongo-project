# The Perfect Spot

<img src="https://specials-images.forbesimg.com/imageserve/1136647427/960x0.jpg?fit=scale" width="650" height="325" />

## Description
This is a **MongoDB - Geospatial Queries** project for *Ironhack*. 

The purpose of the project is to find the best location for a tech startup based on their employee preferences:

- Designers want some nearby companies that also do design.
- Developers like to be near successful tech startups that have raised at least 1 Million dollars.
- 30% of the company have at least 1 child.
- Executives like Starbucks A LOT. Ensure there's a starbucks not to far.
- Account managers need to travel a lot, an airport must be around.
- All people in the company have between 25 and 40 years, they want to go to the club.
- The CEO is Vegan.
- If you want to make the maintenance guy happy, a basketball stadium must be around 10 Km.

​For this project we thought that the vegan Restaurant and the basketball Stadium was not relevant, so we did not include it in the *Nearby Model*.


## We divided the work in two parts:

1) Extract relevant information from MongoDB
2) Extract relevant information from *Foursquare's*
Places API

In order to achieve all the objectives of the project, we worked with:
- Standard GeoJSON Point `{ type: "Point", coordinates: [ 40, 5 ] }`
- Sphere2d index in python with pymongo: `db.collection.createIndex( { <location field> : "2dsphere" } )`
- MongoDB `$near` operator: <https://docs.mongodb.com/manual/reference/operator/query/near/#op._S_near>

 
