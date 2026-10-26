# BLACKSITE-09 — Field Console

A compact, single-page field console built with vanilla HTML, CSS, and JavaScript. The interface keeps the BLACKSITE look without fake telemetry or fictional hacking panels.

## Features

- **Live clock:** device-local time, date, and timezone.
- **Connectivity:** browser-reported online/offline state and secure-context status.
- **Screen wake lock:** asks the browser to keep the display awake when supported.
- **Battery status:** battery percentage and charging state when exposed by the browser.
- **Weather:** when requested, asks for location permission and uses Open-Meteo for current conditions and daily high/low.
- **Compass:** displays a heading only when the browser and device provide a usable absolute heading source.
- **Responsive layout:** menu navigation for desktop and mobile, with reduced-motion support.

## What it does not do

It does not show invented CPU or memory data, fake networks, simulated scan results, fake decryption, pretend access clearance, or shell commands. A regular webpage cannot access detailed system performance, local IP addresses, or nearby Wi-Fi networks without additional permissions/software.

## Run it locally

Open `index.html` in a modern browser. No framework, package manager, build step, or backend is required. Some device APIs work only over HTTPS or localhost, and support varies by browser.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/(root)`, then save.
4. The expected URL is:

   https://kaydenhaas49-sys.github.io/BLACKSITE-09-HALLOWEEN-PROJECT/

The page may take a few minutes to publish after Pages is enabled.

## Privacy

- Time and browser connection status are handled locally.
- Weather asks for location only after the **Get Weather** button is pressed. Coordinates are sent to Open-Meteo for weather data and are not saved by this page.
- No account, analytics, backend, or local storage is used.
- Wake-lock, battery, and compass access depend on browser/device support and permissions.

## Project file

- `index.html` — complete interface, styling, and functionality.
