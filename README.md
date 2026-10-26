# BLACKSITE-09 — Wrist Terminal

A compact, hardware-inspired wrist terminal built with vanilla HTML, CSS, and JavaScript. Its physical-console styling uses a recessed screen, rugged bezel, fastener details, fixed function keys, monochrome phosphor text, scanlines, and compact status output.

## Real terminal commands

Type `help` for a complete list. Supported commands:

- `time` / `date` — local device time, date, timezone, and UTC offset.
- `status` — browser-reported online/offline state, secure context, timezone, and platform.
- `battery` — battery level and charging status if the browser exposes its Battery Status API.
- `wake on`, `wake off`, `wake status` — control the Screen Wake Lock API where supported.
- `weather` — asks for location permission and then queries Open-Meteo for current weather and daily high/low.
- `compass on`, `compass off`, `compass status` — enable or disable device orientation events where available.
- `tools` — check which browser APIs are exposed.
- `clear` — clear the terminal.
- `about` — explain console limitations.

The terminal only runs these documented browser actions. It is not an operating-system shell and does not scan hosts, run arbitrary commands, access private processes, invent CPU/RAM data, or simulate file decryption.

## Run locally

Open `index.html` in a modern browser. No framework, package manager, build step, or backend is required. Wake lock and orientation sensors may require HTTPS or localhost; support varies by browser and hardware.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose branch `main` and folder `/(root)`, then save.
4. Expected URL: https://kaydenhaas49-sys.github.io/BLACKSITE-09-HALLOWEEN-PROJECT/

Publishing may take a few minutes after Pages is enabled.

## Privacy

- Time and connection details are read locally in the browser.
- Weather requests device location only after the user enters `weather` or selects the weather shortcut. Coordinates are sent to Open-Meteo to retrieve weather and are not saved by this page.
- No account, analytics, backend, or local-storage persistence is used.

## File

- `index.html` — terminal UI, styling, and all functionality.
