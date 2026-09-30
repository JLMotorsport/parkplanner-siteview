# ParkPlanner Site View

The phone viewer for [ParkPlanner](https://github.com/JLMotorsport/ParkPlanner):
a single static page that shows a park plan on site with GPS ("you are here"),
calibration and hazard pins. Served by GitHub Pages at
https://jlmotorsport.github.io/parkplanner-siteview/

**This repo holds no plans.** ParkPlanner's "Send to phone" packs the plan into
the link after the `#` (`…/#d=…`). Browsers never send that part to the server,
so GitHub only serves this empty page; the plan goes straight from the QR code
into the phone. Anyone who has a particular link can open that plan, so treat
the QR/link like the plan itself.

Source of truth: `siteview/` in the private ParkPlanner repo. Copy
`index.html`, `sw.js`, `manifest.webmanifest` and `icon.svg` here after
changing it, and bump `CACHE` in `sw.js` so phones pick up the new version.
