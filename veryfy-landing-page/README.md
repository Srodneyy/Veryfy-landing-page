# Veryfy Landing Page

Static, mobile-responsive landing page implementation based on the Figma handoff frame **Landing Page** (`2658:60193`) in the supplied Veryfy design.

## Run

Open `index.html` in a browser, or serve the folder using `python3 -m http.server 8000` and visit `http://localhost:8000`.

## Deploy

Copy the three files into the web root of the target repository (or an appropriate static/public directory if an existing framework is present). No dependencies or build step are required.

## Integration

The product checker intentionally **does not invent verification results**. To connect a live backend, set `window.VERYFY_VERIFY_ENDPOINT` to a same-origin or CORS-enabled endpoint in a script before `script.js`. The example client sends `POST { "identifier": "VF-4829-7610", "method": "code" }` and expects a JSON response containing a safe user-facing `message`. The backend must perform real validation, authorization/rate limiting, and product-safety outcome mapping. The live scanning, alerts and reporting services also require integrations. Never trust a code match as sufficient evidence of authenticity.

## Design status

Matches handoff copy, layout sections and core color palette. Some illustrations are CSS-generated **placeholders**, because original Figma asset files were not accessible from this environment. Replace these with exported Figma artwork for exact asset fidelity. The repository could not be inspected or pushed to from this workspace, so this package is not claimed to be merged or deployed.
