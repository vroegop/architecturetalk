# Six Floors, One Architect

A talk on software architecture seen from every floor of the building: developers, seniors, Product Owners, Scrum Masters and management. Built on Gregor Hohpe's architect elevator metaphor.

**Live deck:** https://vroegop.github.io/architecturetalk/

- Press `L` on any slide to listen to the narrated version with captions and auto-advance.
- Press `?` for all keys, including the speaker view (`S` or `V`) and the Dutch/English toggle for the speaker notes (`D`).
- On a phone, swipe or use the on-screen arrows. Turn the phone sideways to fill the screen with the slide.
- Add `?debug` to the URL for an on-screen readout of viewport, scale and any errors.
- `architecture-talk-ideas.html` holds the five run-sheet outlines the talk was chosen from.

**Portrait variant:** https://vroegop.github.io/architecturetalk/elevator-deck-portraits.html

`elevator-deck-portraits.html` is the same deck with one addition: a small photo next to each quoted
person, and a photo of the speaker on the title slide. It exists so the two versions can be compared
side by side; the original deck is untouched. Only photos with a licence that allows reuse were used
(public domain, CC BY or CC BY-SA), each cropped to a square and stored in `img/people/`. The
`PEOPLE` table at the top of the file records the author, licence and source of every photo, and the
final reading slide prints the credits. People quoted without a free photo simply have none.

Sources are cited on the slides and in the speaker notes.

## Editing

`elevator-deck.html` is the whole deck and the only source of truth: slides, narration, styles and
the React app in one file. Open it straight from disk and it runs, compiling its own JSX in the
browser. Edit it and reload; there is nothing to install. `elevator-deck-portraits.html` is a full
copy with the portrait additions, so a change to the talk itself has to be made in both files until
one of the two is chosen.

## Building

`node build.js` writes `dist/`, the copy that GitHub Pages serves, with both decks in it. It compiles the JSX ahead of
time so a visitor never downloads or runs Babel, which takes the script a phone must parse before
the first slide from about 3 MB to under 0.2 MB. The build refuses to emit a page whose script
does not parse, so a broken deck cannot reach the site. `dist/` is generated and not committed;
the Pages workflow rebuilds it on every push to `main`.
