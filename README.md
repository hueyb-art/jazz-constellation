# The Jazz Constellation

An interactive 3D map of jazz history. Over 200 musicians appear as stars in a globe you can spin and zoom, connected by the bands, mentorships, collaborations, and influences that link them across a century of the music. Tap any star for a biography, a full discography (pulled live from MusicBrainz), a photo, links to listen on Spotify / Apple Music / YouTube, and a 30-second preview clip.

**Live site:** https://hueyb-art.github.io/jazz-constellation/

## What's in this repo

- **`index.html`** — the entire app. It is a single, self-contained file: all the code, the data on every musician and connection, the styling, and the interaction logic live inside it. This is both the live website and the complete source. Nothing else is required to run it — open it in any browser.
- **`jazz-constellation.html`** — a labeled backup copy of the source (identical to `index.html`).
- **`itunes-relay-worker.js`** — optional Cloudflare Worker code for a private Apple/iTunes lookup relay, which makes the music previews and Apple Music links reliable on iPhones.
- **`itunes-relay-setup.md`** — step-by-step instructions for deploying that relay.
- **`Jazz_App_Feasibility_Plan.docx`** — the original scoping/feasibility document the project started from.

## How it works

- The constellation is a custom 3D force-directed graph rendered on an HTML canvas — no game engine or 3D library, just math.
- Each musician's **discography** loads live from the free MusicBrainz database; **photos** come from Wikipedia; **previews** and **Apple Music album links** come from Apple's iTunes lookup service.
- Built deliberately as one HTML file: no server, no build step, no dependencies, no accounts. It just runs.

## Updating the live site

Replace `index.html` in this repo and commit. GitHub Pages republishes within a minute or two. (Tip: when viewing on a device, add `?v=` and any new number to the URL to bypass the browser cache, e.g. `…/?v=42`.)

## Editorial note

The roster and the connections between musicians are a curated selection, not an exhaustive census — chosen to tell the story of how the music's figures shaped one another. Biographies are written for the project; discographies, photos, and audio are drawn live from the open sources above.
