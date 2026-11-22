# Manga Guided View (iPhone Web App)

A lightweight, single-file web app built to read PDF manga comfortably on iPhone using a guided quadrant pan-and-zoom view. Everything runs locally on your device via `PDF.js`—your PDFs are never uploaded to an external server.

## Features

- **Reading Direction Toggle:** Switch between **Right-to-Left (Manga)** and **Left-to-Right (Western)**.
- **Grid Modes (4 or 6 Zones):** Split each page into a **2×2 (4 zones)** or **2×3 (6 zones)** reading sequence so panels and dialogue bubbles are easier to read on a phone screen.
- **Tap Navigation:**
  - **Tap right / center (75% of screen):** Advance to the next zone (and automatically move to the next page at the end of the grid).
  - **Tap left edge (25% of screen):** Go back to the previous zone or page.
- **Full-Page Overview Toggle:** Switch between zoomed zone view and full-page view at any time.
- **Manual Zoom Slider:** Adjust zoom level from `1.20x` to `2.80x` directly from the top HUD (saved automatically).
- **Automatic Reading Progress:** Saves your last page, zone, reading direction, and grid mode per PDF file using `localStorage`, prompting you to resume or start over when reopened.

## How to Host & Install on iPhone (GitHub Pages)

1. Upload `index.html` to a GitHub repository (e.g., `manga-reader`).
2. Go to **Settings → Pages** (on mobile, you can also append `/settings/pages` to your repository URL).
3. Under **Build and deployment → Branch**, select `main` and `/ (root)`, then click **Save**.
4. Wait 1–2 minutes for your site URL (`https://<your-username>.github.io/<repo-name>/`) to go live.
5. Open the URL in **Safari** on your iPhone, tap **Share**, and select **Add to Home Screen** for a full-screen app icon.

## Usage

1. Open the app and select your preferred **reading direction** and **grid mode (4 or 6 zones)**.
2. Tap **Scegli PDF da File** to pick a PDF from the iOS **Files** app.
3. Tap through the zoomed zones to read, or tap the top HUD to adjust zoom or return to the full page.

## Notes & Limitations

- **Local File Access:** Due to iOS browser sandboxing, you pick each PDF manually from the Files app when starting a reading session.
- **Quadrant Grid vs. Panel Detection:** Instead of heavy AI panel detection, the reader uses an overlapping grid sequence for fast, predictable navigation across varied manga layouts.
- **Progress Storage:** Reading progress is tied to the browser/Home Screen web app storage on your device and filename/size/page count metadata.
