# Purple Prop — POTA Companion (prototype v0.1)

A purple-themed mobile web app for HF operators. Includes NOAA SFI and Kp feeds (subject to NOAA endpoint availability), a GPS-centered map with approximate day/night terminator, general HF band suggestions, UTC midnight countdown, local POTA logbook, duplicate warnings, optional current POTA spot lookup, and ADIF/CSV export.

## Publish for free with GitHub Pages
1. Create a new **public** GitHub repository called `purple-prop` and upload **all five files** from this folder to its root.
2. On GitHub.com open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, `main`, `/ (root)`, then **Save**.
3. After deployment, open `https://YOUR-USERNAME.github.io/purple-prop/` in Chrome on Android. Use Chrome's menu → **Add to Home screen** / **Install app**.
4. Tap **GPS** and grant location access. GPS works only on HTTPS (GitHub Pages qualifies) or localhost.

## Important limitations
- The app stores logs in **this browser's local storage**, not in GitHub or a cloud account. Export regularly; changing browsers or clearing site data may erase them.
- NOAA endpoint schemas and POTA public spots access can change. Failed requests show unavailable rather than invented values.
- A-index is deliberately left blank until a validated feed is connected.
- The map shows an approximate solar terminator, not live propagation paths. Use the linked PSK Reporter site for live reception paths until an approved feed integration is implemented.
- The early/late shift panel shows sunrise/sunset only; it does **not** assert official POTA shift eligibility.
- Duplicate alerts use callsign + band + mode + UTC date + your park. Always verify official POTA counting rules before submitting.
- POTA spot lookup is best-effort and may be blocked by CORS or a changed API. It only auto-fills when exactly one park is found.
- ADIF export includes one park reference per QSO; multiple simultaneous park references and more sophisticated P2P handling are planned.
- External Leaflet script/styles and map tiles need connectivity on first load; the logger and cached core app work offline after installation.

## Future milestones
Validate official POTA shift rules and add a verified shift clock; integrate real reception-report map overlay; multiple park references; station-to-radio CAT frequency/mode integration; more complete offline map support; robust NOAA A-index feed.

This is a field-test prototype, not a guaranteed propagation prediction or official POTA application.
