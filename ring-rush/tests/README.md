# Ring Rush tests

`ui-smoke.mjs` drives the menus (menu, garage/shop, pause, game over) with real touch events on 5 phone
viewports and fails if anything is unscrollable, clipped, covered, or if a purchase does not register.

    node tests/ui-smoke.mjs

Needs Playwright and a Chromium. Environment variables (all optional):
`PLAYWRIGHT_PATH` (module path), `CHROMIUM_PATH` (browser binary), `THREE_JS_PATH` (local three.min.js
so the test works offline).

Run it before every commit or publish that touches `index.html`.
