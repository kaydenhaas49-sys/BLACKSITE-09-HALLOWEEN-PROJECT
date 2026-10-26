# BLACKSITE-09 — Wrist Terminal

A compact, hardware-inspired wrist terminal built with vanilla HTML, CSS, and JavaScript. It uses a recessed display, rugged bezel, function keys, monochrome phosphor text, scanlines, and animated status output.

## Commands that do real work

- `dns example.com [A|AAAA|MX|TXT|NS|CNAME|SOA|CAA|SRV]` — query Google Public DNS over HTTPS and display returned records. See the [official JSON API documentation](https://developers.google.com/speed/public-dns/docs/doh/json).
- `rdap example.com` — request public domain registration data through the RDAP bootstrap service. Displays public domain status, registrar when published, nameservers, and registration dates. It intentionally omits personal contact details. RDAP is the current standard for gTLD registration information; see [ICANN's RDAP information](https://www.icann.org/en/contracted-parties/registry-operators/registration-data-access-protocol/information-for-rdap-users-31-08-2018-en).
- `hash hello world` — calculate a real SHA-256 digest locally using the browser's Web Crypto API.
- `netcheck` — make an actual HTTPS request to a public DNS resolver and report HTTP/DNS result and measured round-trip time. This is a service check, not a full network audit.
- `motion on|off|status` — read actual device motion data where supported and permitted.
- `pulse` — request a short vibration pattern on supported devices.
- `time` / `date` — local device time, date, timezone, and UTC offset.
- `status` — browser-reported connectivity and security status.
- `battery` — battery level and charge state, if exposed by the browser.
- `wake on|off|status` — control the Screen Wake Lock API where supported.
- `weather` — request location permission and retrieve actual weather from Open-Meteo.
- `compass on|off|status` — device heading when a usable sensor is available.
- `tools` — report available browser APIs.
- `clear` — clear terminal output.
- `about` — explain the interface's limitations.

The terminal runs only these documented browser operations. It is not an operating-system shell and does not scan hosts, execute arbitrary commands, inspect private processes, invent CPU/RAM readings, or simulate file decryption. Network commands may fail due to network availability, browser CORS policy, service rate limits, or API support.

## Run locally

Open `index.html` in a modern browser. No framework, package manager, build step, or backend is needed. Web Crypto, wake lock, and device sensors may require HTTPS or localhost; support varies by browser and hardware.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose branch `main` and folder `/(root)`, then save.
4. Expected URL: https://kaydenhaas49-sys.github.io/BLACKSITE-09-HALLOWEEN-PROJECT/

## Privacy

- Time, hashes, and motion readings are processed in the browser.
- DNS and RDAP commands send the requested domain to the corresponding public service.
- Weather requests location only after the user requests it; coordinates are sent to Open-Meteo to retrieve weather and are not saved by this page.
- No account, analytics, backend, or local-storage persistence is used.

## File

- `index.html` — terminal UI, animations, and all functionality.
