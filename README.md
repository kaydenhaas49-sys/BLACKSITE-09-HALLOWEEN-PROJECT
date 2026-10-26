# BLACKSITE-09 — Operations Console

A code-generated, animated fictional cyber-operations interface built with vanilla HTML, CSS, SVG, Canvas, and JavaScript.

## Console modules

- **Overview:** status tiles, clickable network topology, node intelligence, animated demo telemetry, command terminal, and event stream.
- **Network map:** expanded procedural node graph with selectable nodes and a registry.
- **Signal lab:** animated Canvas spectrum and a scan simulation that generates fictional readings.
- **Data archive:** fictional dossiers with animated local decode effects and clearance requirements.
- **Access control:** animated clearance handshake and simulated access levels.
- **Field tools:** screen wake lock, battery status, on-demand local weather, and device compass, where supported by the browser and hardware.

## Terminal commands

Type `help` in the console for the full list. Common commands include `status`, `scan`, `nodes`, `trace`, `decrypt`, `access`, `clock`, `sysinfo`, `whoami`, and `clear`.

All terminal commands, network nodes, telemetry, signal scans, archive records, and clearance changes are simulations. The network diagram does not represent real hosts, and the app does not scan or contact external targets.

## Run it locally

Open `index.html` in a modern browser. No framework, package manager, build step, or backend is required.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/(root)`, then save.
4. The expected URL is:

   https://kaydenhaas49-sys.github.io/BLACKSITE-09-HALLOWEEN-PROJECT/

Publishing may take a few minutes after Pages is enabled.

## Browser features and privacy

- Screen wake lock, battery access, and compass availability vary by browser and device.
- HTTPS is needed for certain APIs, including location and device sensors.
- Weather requests location only after the user presses the weather button. Coordinates are sent to Open-Meteo to retrieve weather; they are not stored by this app.
- Network maps, signal values, system telemetry, logs, and archive content are generated locally in the page.

## Project file

- `index.html` — the complete interface, effects, and logic.
