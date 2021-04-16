![portada](https://github.com/ironhack-datalabs/datamad1020-rev/blob/master/projects/W4-geospatial-data-project/portada.jpg)

# GeoSpatial Data Project

## TODO's

You recently created a new company in the `GAMING industry`. The company will have the following scheme:

- 20 Designers
- 5 UI/UX Engineers
- 10 Frontend Developers
- 15 Data Engineers
- 5 Backend Developers
- 20 Account Managers
- 1 Maintenance guy that loves basketball
- 10 Executives
- 1 CEO/President

As a data engineer you have asked all the employees to show their preferences on where to place the new office. Your goal is to place the **new company offices** in the best place for the company to grow. You have to find a place that more or less covers all the following requirements (note that **it's impossible to cover all requirements**, so you have to prioritize at your glance):

- Designers like to go to design talks and share knowledge. There must be some nearby companies that also do design.
- 30% of the company staff have at least 1 child.
- Developers like to be near successful tech startups that have raised at least 1 Million dollars.
- Executives like Starbucks A LOT. Ensure there's a starbucks not too far.
- Account managers need to travel a lot.
- Everyone in the company is between 25 and 40, give them some place to go party.
- The CEO is vegan.
- If you want to make the maintenance guy happy, a basketball stadium must be around 10 Km.
- The office dog—"Dobby" needs a hairdresser every month. Ensure there's one not too far away.

## How to approach it

Notice you'll have to do two things: 

1. Query the database
2. Use an API to get venues (and for this, you'll need a starting point; some coordinates from which you will call the API)
3. Justify your decision using data, not just visualization. How? Maybe measuring distances, maybe assinging weights depending on the importance of your criteria, maybe calculating the density of schools/Starbucks, etc.

There is a couple of ways you can do this: 
#### Option A
From the existing **companies**, choose one to steal their current venue 🥷: query and filter the database based on some of your criteria. Then use an API to do queries (from those companies) and check the companies' surroundings to check the other criteria.

Your result will be `coordinates`.

#### Option B
Choose three **cities** that exist in your database. From these cities, query and filter the database according to any other criteria if necessary. Then, make API calls to see if the rest of your criteria are met. Then, compare the three cities. Are any of them better than the other two? Using data, justify why. 

Once you chose the city, what would be an approximate location?

Your result will be `a city` and a neighbourhood/zip code or adress/coordinates.

#### Option C
Be creative. But remember: always try to follow a general-to-specific approach and base your decisions always using data. 


# BONUS

You found a perfect location for your company: but it's either taken by another company or there's too many options in the city you chose. After all, a whole city is not too specific.

Web scrape real state sites 🏠 to get the best prices and choose a neighbourhood, a block or an adress.
## Help

- Always use standard GeoJSON Point `{ type: "Point", coordinates: [ 40, 5 ] }`
- Create sphere2d index in python with pymongo: `db.collection.createIndex( { <location field> : "2dsphere" } )`
- MongoDB `$near` operator: <https://docs.mongodb.com/manual/reference/operator/query/near/#op._S_near>

## How to deliver the project

- Create a new repo in your github account.
- Create an issue with the link of your repo copy pasted inside `my-project.md` (within the parentheses) on this repo.
- You must justify your decision with data
- You may use visualization tools like (tableau, folium, cartoframes, etc.)
- **You must provide `lat` and `long` for the new office proposals.**

## Links & Resources

- [https://developers-dot-devsite-v2-prod.appspot.com/maps/documentation/javascript/examples/geocoding-reverse]
- [https://docs.mongodb.com/manual/geospatial-queries/]
- [https://developers.google.com/maps/documentation/geocoding/intro]
- [https://developers.google.com/maps/documentation/geocoding/start]
- [https://data.crunchbase.com/docs]
- [https://developers.google.com/places/web-service/search]
- [https://www.youtube.com/watch?v=PtV-ZnwCjT0]
- [https://developer.foursquare.com/]
- [https://cloud.google.com/maps-platform/places/]
- [https://www.meetup.com/meetup_api/]
