# JRM Scooters — PWA

Installable web app (like Dewy Dreams). Built with Vite + React + vite-plugin-pwa.
Runs in any browser and installs to the phone home screen with its own icon, full-screen.

## Run it locally (optional)
    npm install
    npm run dev      # opens a local preview
    npm run build    # production build into /dist

## Deploy to Cloudflare Pages (recommended — gives you a live link + auto-updates)
1. Put this folder in a new GitHub repo (push it).
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git → pick the repo.
3. Build settings:
   - Framework preset: Vite
   - Build command:    npm run build
   - Output directory: dist
4. Save & Deploy. You get a link like https://jrm-scooters.pages.dev
5. Every time you push to GitHub, it rebuilds automatically.

## Quick deploy WITHOUT GitHub
    npm install && npm run build
Then drag the /dist folder onto https://app.netlify.com/drop  (or Cloudflare Pages → Upload assets).

## Custom domain (later)
In the Pages project → Custom domains → add jrmscooters.com (DNS is one click if the domain is on Cloudflare).

## Install on a phone
Open the link → Share → "Add to Home Screen". It opens full-screen with the JRM icon.

## Notes
- Prototype: bookings don't persist or charge yet (see the backend scope doc).
- Operator dashboard PIN: 0000 (replace with real auth before launch).
- App code lives in src/App.jsx. Icons in public/icons. PWA config in vite.config.js.
