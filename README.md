# BLACKSITE-09 — Wrist Terminal

A compact, terminal-style wrist-device interface built with vanilla HTML, CSS, and JavaScript. The design uses a monochrome green phosphor display, fixed section menu, compact readouts, and a rugged terminal bezel.

## Real features

- **Live local clock:** device time, date, and timezone.
- **Connectivity status:** browser-reported online/offline state. Online does not guarantee internet reachability.
- **Secure-context status:** reports whether the page is in a browser secure context.
- **Screen wake lock:** requests that the browser keep the display awake when supported.
- **Battery status:** battery level and charging state if the browser exposes the Battery Status API.
- **Weather:** fetches current weather and daily high/low from Open-Meteo after the user presses the request button and grants location permission.
- **Compass:** displays an absolute heading when the browser and device provide a usable sensor.

The interface is designed as a single scrollable terminal screen and adapts to mobile widths. It does not contain fake networks, made-up CPU/RAM stats, simulated scan results, pretend decryption, or fake command execution.

## Run it locally

Open `index.html` in a modern browser. No framework, package manager, build step, or backend is needed. Wake lock and orientation sensors may require HTTPS or localhost; API availability varies by browser and device.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose branch `main` and folder `/(root)`, then save.
4. Expected URL: https://kaydenhaas49-sys.github.io/BLACKSITE-09-HALLOWEEN-PROJECT/

The page may take a few minutes to publish after Pages is enabled.

## Privacy

- Time and status readouts are processed in the browser.
- Weather requests location only after the user presses the button; coordinates are sent to Open-Meteo for weather data and are not saved by this page.
- No account, analytics, backend, or local-storage persistence is used.

## File

- `index.html` — interface, styles, and all functionality.
