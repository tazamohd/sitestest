# sitestest

Candidate website designs for SALISCO, published so people can open them on a real
device and say what they think.

**Live:** <https://sites-git-main-salis4.vercel.app/>

Deployed from `main` on every push, by the Vercel project `sites`
(team `salis4`). Deployment protection is off — these pages are meant to be
opened by anyone with the link.

## What is in here

| Entry | Path | What it is |
|-------|------|-----------|
| 01 | [`2060/`](2060/index.html) | **SALIS AUTO — Garage OS 2060.** A six-page speculative design study: the workshop system thirty-five years out. |

## How it is built

Static files. No build step, no dependencies, no bundler, no framework — Vercel
serves the repository as it is. That is deliberate: a design you can open by
double-clicking `index.html` is a design anyone can review, including from a
phone on a bad connection.

```
sitestest/
├─ index.html        the design index
├─ 2060/             entry 01 — its own self-contained site
├─ assets/           shared logo
├─ fonts/            shared faces, self-hosted (no Google Fonts request)
└─ previews/         one preview image per entry
```

## Adding a design

1. Drop it in its own folder with an `index.html` — it may contain anything it
   likes, as long as it does not need a build step.
2. Put a preview image in `previews/` (1440×900 works well).
3. Add one `<article class="entry">` block to the root `index.html`, copying the
   shape of entry 01.
4. Push. Vercel redeploys on every push to `main`.

Shared `assets/` and `fonts/` are there to be used — referencing them from a
design folder (`../fonts/…`) keeps the page weight down and avoids a third-party
font request. A design that wants its own typography should ship it in its own
folder instead.

## Feedback

[Open an issue](https://github.com/tazamohd/sitestest/issues/new). Blunt is
useful; polite and vague is not.

## A note on the content

Nothing published here is live product. Entry 01 in particular is explicitly
speculative fiction — every figure in it is invented and labelled as such on the
page itself. The real SALIS AUTO product lives elsewhere.
