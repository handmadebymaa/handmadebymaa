# Handmade by Maa

Static website for Handmade by Maa (crochet studio). No build step required — plain HTML pages that render themselves in the browser.

## Project structure

```
/Home.dc.html        Home page
/Gallery.dc.html      Gallery page (product photos)
/Contact.dc.html      Contact page
/index.html            Redirects "/" to Home.dc.html
/support.js            Page runtime (loads React/ReactDOM from CDN and renders each page)
/assets/                Team photos + logo
/public/                Product photos (gallery)
vercel.json             Routes "/" to the homepage on Vercel
```

## Local preview

Serve the folder with any static file server, e.g.:

```bash
npx serve .
```

Then open `http://localhost:3000/Home.dc.html` (or just `/`, which redirects).

Do not open the files with `file://` directly — the runtime needs to be served over http(s).

## Deploying to Vercel

1. Push this folder to a GitHub repo (or drag-and-drop the folder into the Vercel dashboard).
2. In Vercel, choose **"Other"** as the framework preset (no build command, no output directory needed).
3. Deploy. The included `vercel.json` routes `/` to `Home.dc.html` automatically.

No environment variables or build steps are required.
