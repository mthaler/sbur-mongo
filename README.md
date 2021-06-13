# sbur-mongo
Demo project from the Spring Boot Up &amp; Running book that queries the PlaneFinder service and stores received data in MongoDB. It uses an embedded MongoDB database.

## Usage

The *sbur-mongo* service will connect to the [planefinder](https://github.com/mthaler/planefinder) service to receive aircraft locations, thus the *planefinder* service needs to be started first.

The *sbur-mongo* service will store received aircraft locations using MongoDB and will also print out received data.

It also provides a REST API to query aircraft locations from the Redis database.

The [httpie](https://httpie.io/) is a user-friendly HTTP client that can be used to test the API:

```bash
$ http :8080/aircraft
HTTP/1.1 200 OK
Content-Length: 1397
Content-Type: application/json

[
    {
        "adsb": false,
        "altitude": 30000,
        "barometer": 0.0,
        "bds40_seen_time": "2021-06-13T12:02:44.260Z",
        "callsign": "SAL001",
        "category": "ct",
        "flightno": "SAL001",
        "heading": 280,
        "id": "562",
        "is_on_ground": true,
        "last_seen_time": "2021-06-13T12:02:44.260Z",
        "lat": 39.2979849,
        "lon": -94.71921,
        "polar_bearing": 0.0,
        "polar_distance": 0.0,
        "pos_update_time": "2021-06-13T12:02:44.260Z",
        "reg": "N12345",
        "route": "route",
        "selected_altitude": 0,
        "speed": 440,
        "squawk": "sqwk",
        "type": "LJ",
        "vert_rate": 0
    },
    {
        "adsb": false,
        "altitude": 40000,
        "barometer": 0.0,
        "bds40_seen_time": "2021-06-13T12:02:44.260Z",
        "callsign": "SAL002",
        "category": "ct",
        "flightno": "SAL002",
        "heading": 65,
        "id": "563",
        "is_on_ground": true,
        "last_seen_time": "2021-06-13T12:02:44.260Z",
        "lat": 39.8560963,
        "lon": -104.6759263,
        "polar_bearing": 0.0,
        "polar_distance": 0.0,
        "pos_update_time": "2021-06-13T12:02:44.260Z",
        "reg": "N54321",
        "route": "route",
        "selected_altitude": 0,
        "speed": 440,
        "squawk": "sqwk",
        "type": "LJ",
        "vert_rate": 0
    },
    {
        "adsb": false,
        "altitude": 40000,
        "barometer": 0.0,
        "bds40_seen_time": "2021-06-13T12:02:44.260Z",
        "callsign": "SAL002",
        "category": "ct",
        "flightno": "SAL002",
        "heading": 65,
        "id": "564",
        "is_on_ground": true,
        "last_seen_time": "2021-06-13T12:02:44.260Z",
        "lat": 39.8412964,
        "lon": -105.0048267,
        "polar_bearing": 0.0,
        "polar_distance": 0.0,
        "pos_update_time": "2021-06-13T12:02:44.260Z",
        "reg": "N54321",
        "route": "route",
        "selected_altitude": 0,
        "speed": 440,
        "squawk": "sqwk",
        "type": "LJ",
        "vert_rate": 0
    }
]
```
