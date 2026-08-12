# Chethna Sathyanarayan — Content Design Portfolio

A single-page portfolio site showcasing content design work, including case studies on
Great Learning's Pro+ subscription, payment failure recovery flows, programme page
iteration, and an AI-assisted content design system.

**Live site:** _(added after the first Vercel deploy)_

## Structure

```
index.html      the entire site — markup, styles and scripts in one file
images/         case study screenshots (WebP)
vercel.json     static hosting + cache headers
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

Vercel is connected to this repository. Any push to `main` deploys automatically —
pushes to other branches produce preview URLs.

## Notes on the images

The images were originally embedded in `index.html` as base64 data URIs, which made the
file 6.1 MB and forced the browser to download every screenshot before rendering
anything. They are now separate WebP files, so the HTML is 246 KB and the screenshots
load lazily, in parallel, and stay cached between visits.

Filenames are numbered in document order and describe their contents, so the image a
caption refers to is easy to find.
