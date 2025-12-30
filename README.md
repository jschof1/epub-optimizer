# EPUB Image Optimizer

A simple, client-side web app to reduce the size of EPUB files by compressing images.

## Features
- **100% Client-Side**: Your files never leave your computer. Everything happens in the browser.
- **Image Compression**: Reduces JPEG/PNG quality to save space.
- **EPUB Standard Compliant**: Preserves the `mimetype` storage requirement.

## How to use
1. Open `index.html` in any modern web browser.
2. Select your EPUB file.
3. Wait for the optimized file to download automatically.

## Deployment to Cloudflare Pages (Free)
1. Log in to your [Cloudflare Dashboard](https://dash.cloudflare.com/).
2. Go to **Workers & Pages** > **Pages**.
3. Click **Connect to git** or **Upload assets**.
4. If uploading:
   - Create a folder with only `index.html`.
   - Drag and drop it into the Cloudflare upload zone.
5. Give your project a name (e.g., `epub-optimizer`).
6. Click **Deploy site**.

Your app will be live at `https://epub-optimizer.pages.dev`.

