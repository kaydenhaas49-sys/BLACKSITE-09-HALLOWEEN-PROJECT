# BLACKSITE-09 — Security Workbench

A browser-based security workbench built with vanilla HTML, CSS, and JavaScript. The interface uses a three-column workspace with a command terminal, quick-run tools, live browser/session status, and restrained green accents. No framework, build step, or backend is required.

## Commands that do real work

- `dns example.com [A|AAAA|MX|TXT|NS|CNAME|SOA|CAA|SRV]` — query Google Public DNS over HTTPS and display the returned records. See the [official JSON API documentation](https://developers.google.com/speed/public-dns/docs/doh/json).
- `rdap example.com` — request public domain registration data through the RDAP bootstrap service. Shows published domain status, registrar organization when available, nameservers and registration dates. Contact details are intentionally omitted. See [ICANN's RDAP information](https://www.icann.org/en/contracted-parties/registry-operators/registration-data-access-protocol/information-for-rdap-users-31-08-2018-en).
- `hash hello world` — calculate a real SHA-256 digest locally using the browser's Web Crypto API.
- `netcheck` — make an actual HTTPS request to a public DNS resolver and report its HTTP/DNS result and measured round-trip time. This is a service check, not a full network audit.
- `motion on|off|status` — read actual device motion data where supported and permitted.
- `pulse` — request a short vibration pattern on supported devices.
- `time` / `date` — local device time, date, timezone and UTC offset.
- `status` — browser-reported connectivity and security status.
- `battery` — battery level and charging state if exposed by the browser.
- `wake on|off|status` — control the Screen Wake Lock API where supported.
- `weather` — request location permission and retrieve actual weather from Open-Meteo.
- `compass on|off|status` — device heading when a usable sensor is available.
- `fullscreen` — enter or exit the Fullscreen API on supported browsers.
- `tools` — report exposed browser APIs and configured network services.
- `clear` — clear terminal output.
- `about` — explain console limitations.

Animated operation lines reflect the current request state, actual elapsed time, sensor readings, and returned data. Network operations can fail due to internet availability, browser CORS policy, API rate limits or service errors; the terminal reports those failures instead of making up results.

The terminal is not an operating-system shell and does not scan hosts, execute arbitrary commands, inspect private processes, invent CPU/RAM readings or simulate file decryption.

## Run locally

Open `index.html` in a modern browser. No framework, package manager, build step or backend is needed. Web Crypto, wake lock and device sensors may require HTTPS or localhost; browser support varies by device.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose branch `main` and folder `/(root)`, then save.
4. Expected URL: https://kaydenhaas49-sys.github.io/BLACKSITE-09-HALLOWEEN-PROJECT/

## Privacy

- Time, SHA-256 hashes and motion readings are processed in the browser.
- DNS and RDAP commands send the domain you enter to the respective public service.
- Weather asks for location only after you request it; coordinates are sent to Open-Meteo for weather and are not saved by this page.
- No account, analytics, backend or local-storage persistence is used.

## File

- `index.html` — terminal UI, animations and all functionality.
