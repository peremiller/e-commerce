# Automatic full-app offline saving

Open the canonical URL `https://peremiller.github.io/e-commerce/` once while connected. All app pages and the local images, fonts, scripts, stylesheets and data required by the interface is saved automatically. The status bar confirms completeness; no Save click is needed. Keep site data and a charged device. Product browsing and browser-local demo orders work offline. This app does not process real online payments.

After editing public files run `python3 scripts/build-offline.py` before publishing. This regenerates the release hash and full asset manifest. The worker is limited to this repository’s GitHub Pages subpath; it excludes APIs, authenticated requests, writes and other origins, and retains the previous complete release during a failed update. Existing browser-local records are unchanged.
