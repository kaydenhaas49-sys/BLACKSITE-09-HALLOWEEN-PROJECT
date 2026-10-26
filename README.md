# BLACKSITE-09 — Field Console

A single-page, code-generated field terminal built with vanilla HTML, CSS, and JavaScript. The interface keeps the BLACKSITE visual style while only showing information available to the browser or explicitly retrieved after user action.

## Features

- **Live clock:** local device time, date, timezone, local-day progress, and time since this page was opened.
- **Browser/device status:** browser-reported online/offline state, optional connection type, browser platform, current viewport dimensions, pixel ratio, language, and secure-context state.
- **Screen wake lock:** asks the browser to keep the display awake when supported.
- **Battery status:** current percentage and charging state when the browser exposes the Battery Status API.
- **Weather:** on button press, requests browser location permission and uses Open-Meteo to retrieve current weather and daily high/low.
- **Compass:** requests permission where applicable and displays a heading only when the browser provides an absolute heading source.
- **Unified scrolling menu:** jumps between sections and updates its highlight as you scroll.
- **Responsive layout:** adapts to mobile, desktop, and reduced-motion preferences.

## Important limitations

The browser does not generally expose system CPU load, RAM usage, true device uptime, local IP addresses, nearby Wi-Fi networks, or detailed hardware telemetry to a normal web page. BLACKSITE-09 does not invent those values.

The page contains no fake network topology, fictional scan results, simulated shell, fake decryption, or pretend clearance system. It has no backend, account, analytics, or local-storage persistence.

## Run it locally

Open `index.html` in a modern browser. No framework, package manager, build step, or backend is required. Some device APIs require HTTPS or localhost; browser support varies.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/(root)`, then save.
4. The expected URL is:

   https://kaydenhaas49-sys.github.io/BLACKSITE-09-HALLOWEEN-PROJECT/

Publishing may take a few minutes after Pages is enabled.

## Privacy

- Local time and browser/device status are processed in the page.
- Weather asks for location only when the user presses **Get Weather**. Coordinates are sent to Open-Meteo to retrieve weather; this page does not save them.
- No location is requested for any other feature.
- Battery, orientation, and wake-lock access only use browser APIs and user interactions. Availability depends on the device and browser.

## Project file

- `index.html` — complete interface, styling, and functionality.
