# Ring Rush

Single-file mobile arcade game: `index.html` (Three.js r128 from cdnjs). UI language is Hebrew (RTL).

## Rules
- Before every commit or artifact publish that touches `index.html`, run `node tests/ui-smoke.mjs`.
  It must end with all checks passing. Do not publish with a failing UI test.
- Menus (`.panel`) must stay scrollable by touch. Never add a global `touchmove` `preventDefault`;
  never center a scrollable flex container with `justify-content:center` (it clips the top).
  Primary actions in tall panels live in a sticky footer (`.sfoot`).
- Test menus with real touch events (CDP `Input.dispatchTouchEvent`), not only mouse clicks or `scrollTop`.
- Artifact publishing: build from `index.html` by stripping the `<html>/<head>/<body>` wrappers, keeping
  `<title>`, `<style>` and the body content; add `color-scheme:dark` to `:root` and `dir="rtl"` on `#app`.
