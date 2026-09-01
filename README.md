# Ink & Static

Two CSS/SVG effects that look far more complicated than they are — a gooey "liquid" merge effect and a terminal-style text decode animation. No frameworks, no build step, no dependencies.

**[Live demo →](#)** *(replace with your GitHub Pages link once deployed)*

## What's inside

**01 — The goo effect**
Circles that visually melt into one another as they get close, built with a single SVG filter (`feGaussianBlur` + `feColorMatrix` + `feComposite`). No physics engine, no canvas — pure CSS filter trick.

**02 — The decode effect**
Text that scrambles through random characters before locking into place, left to right, like a terminal decrypting a string. About 20 lines of vanilla JavaScript using `requestAnimationFrame`.

Click **"Get the code"** on the live site (or the "copy this snippet" button under each section) to grab either effect on its own — no need to dig through the full file.

## Running it locally

No build tools, no npm install. Just open the file:

```bash
git clone https://github.com/<your-username>/ink-and-static.git
cd ink-and-static
open index.html   # or just double-click it
```

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, choose the `main` branch and `/ (root)` folder.
4. Save — your site will be live at `https://<your-username>.github.io/ink-and-static/` within a minute or two.

## Using the effects in your own project

Each effect is self-contained:

- **Goo effect** — copy the `<svg><filter id="goo">...</filter></svg>` block anywhere in your page, then apply `filter: url(#goo);` to any container. Everything inside that container that's a solid, roughly-circular shape will merge with its neighbors when close enough. Tune `stdDeviation` for how far the melt reaches, and the last matrix value for how sharp the snap is.
- **Scramble effect** — copy the `Scrambler` class, give any element a `data-text="YOUR TEXT"` attribute, and call `new Scrambler(el).run()`.

Both snippets are also copyable directly from the live site via the "Get the code" button.

## Why this exists

Built as a small, low-effort/high-payoff exploration of SVG filters and canvas-free animation — inspired by seeing a classmate's [liquid glass](#) playground and wanting to try a different corner of the same idea space (CSS/SVG tricks that look harder than they are).

## License

MIT — do whatever you want with it.
