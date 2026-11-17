# Running Route Roulette 🎲🏃

Pick a distance, hit **Spin**, and get a random running loop that starts and ends where you are.

**Live site:** https://jackflemingcodes.github.io/running-route-roulette/

## Features
- Random loop routes on real footpaths and streets (OpenStreetMap data)
- Miles or kilometers, 1–15 mi / 1–25 km
- Use your location, tap the map, or drag the start pin
- Estimated finish time from your pace
- Export the route as a GPX file for your watch or Strava

## How it works
The site places a few random waypoints on a circle that passes through your start point, then asks the free
[FOSSGIS OSRM](https://routing.openstreetmap.de/) foot-routing service for a loop through them. It rescales the
circle a few times until the routed distance is close to your target.

It's one static `index.html` with no build step and no API keys, using [Leaflet](https://leafletjs.com/) for the map.

## Run locally
Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server
```

(Location access needs `https://` or `localhost`.)

## Credits
Map data © OpenStreetMap contributors. Routing by FOSSGIS e.V.
