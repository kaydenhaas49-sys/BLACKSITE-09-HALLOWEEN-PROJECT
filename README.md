# BLACKSITE-09 — Personal Field Display

An animated, mobile-friendly clock with four practical phone utilities.

## Features

- **Animated local clock:** live time, date, timezone, and day-progress indicator, with a 12/24-hour switch.
- **Keep screen awake:** requests the browser Screen Wake Lock so the screen can stay on while the page is visible. Support depends on browser/device and usually requires HTTPS.
- **Battery status:** displays charge percentage and charging state when the browser exposes the Battery Status API; otherwise it shows an unavailable status.
- **Local weather:** on request, asks for device location and fetches current conditions plus today's high/low from [Open-Meteo](https://open-meteo.com/). Coordinates are sent to the weather provider only after the user presses the weather button; the page does not save them. Weather API data is attributed to Open-Meteo.
- **Compass:** requests device-orientation permission and reads a real heading if the browser/device supplies absolute compass data. Some devices or browsers won't provide it.

## Run it

Open `index.html` in a modern browser. No installation or build step is needed. HTTPS is recommended for device APIs.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/(root)`, then save.
4. After GitHub Pages publishes it, the expected address is:

   https://kaydenhaas49-sys.github.io/BLACKSITE-09-HALLOWEEN-PROJECT/

## Privacy and limitations

The clock uses the device's local time and timezone. Battery and compass data are read from browser APIs when available. Weather only requests geolocation after a button press; the coordinates are sent to Open-Meteo to retrieve weather. No coordinates are stored by this app.

The browser may revoke a wake lock when the page is hidden, may not expose battery information, and may not provide absolute compass heading. The site shows fallbacks for unsupported features rather than displaying fabricated readings.

## File

- `index.html` — complete app, styles, and feature logic.
