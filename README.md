# EXIF & Metadata Studio

A single-file, self-contained web app for inspecting, exporting, and stripping the metadata hidden inside your photos — camera settings, GPS location, IPTC/XMP fields, and more. No build step, no server, no dependencies to install: open the HTML file in a browser and go.

## Features

- **Drag, drop, browse, or paste** — load an image by dragging it in, picking it from a file browser, or pasting it straight from your clipboard (`Ctrl+V` / `⌘+V`).
- **Camera & capture details** — make, model, lens, focal length, aperture, shutter speed, ISO, white balance, resolution (MP), and capture date at a glance.
- **GPS & mapping** — if a photo is geotagged, see it pinned on an interactive Leaflet map, with one-click links to Google Maps and OpenStreetMap.
- **Full Tags Inspector** — every raw EXIF, IPTC, and XMP key/value pair found in the file, in a searchable table.
- **Raw data export** — view and copy the complete metadata set as formatted JSON or CSV.
- **Social caption generator** — turn a photo's specs into a ready-to-post caption, in a few different styles (technical, minimal, story, hashtag-ready).
- **Privacy stripper** — re-render the image onto a canvas and download a clean copy (JPEG, PNG, or WebP) with all EXIF and GPS metadata removed.
- **Dark mode, responsive layout** — works on desktop and phone, with a layout that reorders itself so the tool is usable at a glance on a small screen.

## Getting started

1. Download `exif-metadata-studio.html`.
2. Open it in any modern browser (Chrome, Firefox, Safari, Edge).
3. Drop in a photo.

That's it — everything runs client-side in the browser. No image is ever uploaded anywhere.

## Supported formats

JPEG, PNG, WebP, TIFF, HEIC, and most other common image formats for metadata reading (via [`exifr`](https://github.com/MikeKovarik/exifr)). Export formats for the cleaned copy are JPEG, PNG, and WebP.

## Tech

- Plain HTML, CSS, and vanilla JavaScript — no framework, no bundler.
- [`exifr`](https://github.com/MikeKovarik/exifr) for metadata parsing, loaded from a CDN.
- [`Leaflet`](https://leafletjs.com/) + OpenStreetMap tiles for the map, loaded from a CDN.

An internet connection is needed on first load to fetch these two libraries; everything else — including all image processing — happens locally in your browser.

## Privacy

Images are never uploaded to a server. Parsing, mapping, captioning, and metadata stripping all happen locally in your browser using the File and Canvas APIs.

## License

MIT — do whatever you'd like with it.
