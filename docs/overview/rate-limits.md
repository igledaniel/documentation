### Rate limits

#### Mapping products

##### Tangram

[Tangram](https://mapzen.com/documentation/tangram/), Mapzen's rendering software for web and mobile apps, does not require its own API key. However, if you are using Tangram to draw data from Mapzen's vector tiles service, you need an API key.

##### Mapzen Basemap Styles

Mapzen's [cartography](https://mapzen.com/documentation/cartography/) requires an API key to enable access to Mapzen vector and terrain tiles data sources.

##### Mapzen Vector Tiles

[Mapzen Vector Tiles](https://mapzen.com/documentation/vector-tiles/) provides global basemap coverage and has these limits:

- 50,000 free requests per month

When viewing a map, you commonly use about 15 tiles at a time. The number of map views is an attempt to translate the query rate limits into practical expectations in an app.

The Mapzen Vector Tiles service is built from the [Tilezen](https://github.com/tilezen) open-source project.

##### Mapzen Terrain Tiles

[Mapzen Terrain Tiles](https://mapzen.com/documentation/terrain-tiles/) provides global elevation coverage. This service is 100% cached and there are no rate limits.

_Note: This service is not currently part of Mapzen Flex._

The Mapzen Terrain Tiles service is built from the [Joerd](https://github.com/tilezen/joerd) open-source project.

#### Search and mobility products

##### Mapzen Search

[Mapzen Search](https://mapzen.com/documentation/search/) is a geocoding and place-finding service and has these limits:

- 25,000 free requests per month for forward geocoding, reverse geocoding, and place lookup
- 50,000 free requests per month for autocomplete

The Mapzen Search service is built from the [Pelias](https://github.com/pelias) open-source project.

##### Mapzen Turn-by-Turn

[Mapzen Turn-by-Turn](https://mapzen.com/documentation/turn-by-turn/) is a routing and navigation service and has these limits:

- 5,000 free requests per month
- Pedestrian routes have a limit of 50 locations and 250 kilometers.
- Bicycle routes have a limit of 50 locations and 500 kilometers.
- Automobile routes have a limit of 20 locations and 5,000 kilometers.
- Multimodal routes have a limit of 500 kilometers between locations.

The distance limit is the total straight-line distance (colloquially, as the crow flies) along a path through successive locations.

##### Mapzen Matrix

[Mapzen Matrix](https://mapzen.com/documentation/matrix/) provides time and distance calculations between locations and has these limits:
????
- 2 queries per second
- 5,000 queries per day
- The maximum number of locations is 50 for any type of matrix.
- The maximum straight-line distance between two locations is 200 kilometers.

_Note: This service is not currently part of Mapzen Flex._

##### Mapzen Optimized Route

[Mapzen Optimized Route](https://mapzen.com/documentation/optimized/) finds the most efficient route between many locations. The service has these limits:
????
- 2 queries per second
- 5,000 queries per day
- The maximum number of locations is 50.
- The maximum straight-line distance between two locations is 200 kilometers.

_Note: This service is not currently part of Mapzen Flex._

##### Mapzen Isochrone

[Mapzen Isochrone](https://mapzen.com/documentation/mobility/isochrone/api-reference/) provides a computation of areas that are reachable within specified time periods from a location or set of locations. The service has these limits:

???
- 2 queries per second
- 5,000 queries per day
- The maximum number of locations is one. For isochrones around multiple locations, you need to make multiple requests.
- The maximum time to compute isochrone contours from the location is 120 minutes.
- The maximum number of isochrone contours in a single request is four.

_Note: This service is not currently part of Mapzen Flex._

The Mapzen Turn-by-Turn, Matrix, Optimized Route, and Isochrone services are built from the [Valhalla](https://github.com/valhalla) open-source project.

#### Data products

##### Mapzen Elevation

[Mapzen Elevation](https://mapzen.com/documentation/elevation/) provides the height or elevation at a set of locations and has these limits:

- 2 queries per second
- 20,000 queries per day

There are also limitations on the number of sampling points for which you request elevations.

_Note: This service is not currently part of Mapzen Flex._

The Mapzen Elevation lookup service is built from the [Valhalla](https://github.com/valhalla) open-source project.

##### Who's On First

Retrieve data about places from the [Who's On Firsts](https://mapzen.com/documentation/wof/) gazetteer.

- Queries per day: 25,000
- Queries per minute: 300
- Queries per second: 6

_Note: This service is not currently part of Mapzen Flex._

##### Other data products

Mapzen's other data products do not currently require API keys. These include:

- Metro Extracts, downloadable snapshots of OpenStreetMap data (Note: you will need to sign in with a developer account to download custom extracts)
- Transitland, the open transit data project

#### Mobile products

To use Mapzen's Android or iOS SDKs or any of Mapzen's other products in your mobile apps, you need an API key. You are subject to the rate limits for the service you are integrating.