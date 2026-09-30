# ParkPlanner Site View

The phone viewer for [ParkPlanner](https://github.com/JLMotorsport/ParkPlanner):
a single static page that shows a park plan on site with GPS ("you are here"),
calibration and hazard pins. Served by GitHub Pages at
https://jlmotorsport.github.io/parkplanner-siteview/

**This repo holds no plans.** ParkPlanner's "Send to phone" packs the plan into
the link after the `#` (`…/#e=…`), **encrypted with the Site View passcode**
(AES-256-GCM, key from PBKDF2-SHA256 with 600,000 rounds). Browsers never send
that part to the server, so GitHub only serves this empty page. A copied link or
photographed QR is unreadable without the passcode; the phone keeps only the
locked copy.

Source of truth: `siteview/` in the private ParkPlanner repo. Copy
`index.html`, `sw.js`, `manifest.webmanifest` and `icon.svg` here after
changing it, and bump `CACHE` in `sw.js` so phones pick up the new version.
