# Chethna Sathyanarayan — Content Design Portfolio

A single-page portfolio site showcasing content design work, including case studies on
Great Learning's Pro+ subscription, payment failure recovery flows, programme page
iteration, and an AI-assisted content design system.

**Live site:** https://cheydesign.github.io/chethnacontentportfolio/

## Structure

```
index.html      the entire site — markup, styles and scripts in one file
images/         case study screenshots (WebP)
.nojekyll       tells GitHub Pages to serve the files as-is
```

There is no build step and no dependencies. The site is plain HTML, CSS and vanilla
JavaScript, with Poppins loaded from Google Fonts.

## Running it locally

Open `index.html` directly in a browser, or serve the folder so relative image paths
resolve the same way they do in production:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying

Hosted on GitHub Pages from the `main` branch, root folder. Any push to `main`
republishes the site automatically — the Pages build runs as a GitHub Action and
usually finishes within a minute.

All asset paths are relative, so the site works correctly when served from a
subpath such as `/chethnacontentportfolio/`.

## Notes on the images

The images were originally embedded in `index.html` as base64 data URIs, which made the
file 6.1 MB and forced the browser to download every screenshot before rendering
anything. They are now separate WebP files, so the HTML is 246 KB and the screenshots
load lazily, in parallel, and stay cached between visits.

Filenames are numbered in document order and describe their contents, so the image a
caption refers to is easy to find.
