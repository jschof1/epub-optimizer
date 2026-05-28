# EPUB Image Optimizer

A static, client-side web app that reduces EPUB size by resizing and recompressing embedded JPEG and PNG images.

The app runs entirely in the browser: files are not uploaded, accounts are not required, and the original EPUB is never modified.

## Features

- Browser-only EPUB optimization using JSZip.
- JPEG recompression with an adjustable quality slider.
- Optional large-image downscaling before repackaging.
- PNG files remain PNG files so EPUB image paths and reader compatibility stay intact.
- Size-aware output: if an optimized image is larger than the original, the app keeps the original.
- EPUB-safe packaging: the required `mimetype` file is preserved as the first, uncompressed ZIP entry.
- Static-host friendly: deploy the repo as-is to GitHub Pages, Cloudflare Pages, Netlify, Vercel, or any plain web server.

## Use Locally

Open `index.html` in a modern browser, choose an `.epub` file, and wait for the optimized copy to download.

For a local server:

```sh
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Deploy

### GitHub Pages

1. Push this repository to GitHub.
2. Open the repository settings.
3. Go to **Pages**.
4. Set the source to the `main` branch and `/root`.
5. Save the setting.

GitHub Pages will publish the app at the repository's Pages URL.

### Cloudflare Pages

1. Open **Workers & Pages** in Cloudflare.
2. Create a Pages project.
3. Connect this GitHub repository.
4. Use no build command and `/` as the output directory.
5. Deploy.

## Notes

- Best savings come from EPUBs with oversized cover art, photography, or scanned page images.
- DRM-protected books cannot be optimized.
- Unsupported image formats are copied through unchanged.
- The app currently uses JSZip from CDNJS with subresource integrity enabled.

## Repository Hygiene

- Keep generated files such as `.DS_Store` out of commits.
- Add a `LICENSE` file before advertising the project as open source.
- Add a custom domain or canonical URL once the production host is chosen.
