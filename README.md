# The Endless Shelf

Static, build-free bookshop demo: endless 3D shelves, hover to pull a book out, click to open it.

```
python3 -m http.server 8000   # then open http://localhost:8000/
```

- `index.html` — everything (HTML, CSS, JS). Design tokens (colour, type, shape) are the CSS variables at the top of `:root`.
- `covers/` — cover art named `<slug>.jpg`; missing files fall back to a generated cover.
- About / Contact copy: the `SITE` object in the script. The current text is placeholder.
- Book data: the `BOOKS` array; shelves: `SECTIONS` + `SEC_ORDER`.
- Optional `logo.png` next to `index.html` appears in the header.

## Focus model (UX)
One shelf is the **main** shelf (60% of the viewport, full colour, big title). The others are quiet strips that show only the tops of the spines and are dimmed. Wheel, ↑/↓, vertical swipe, the dots on the right, or a click on a strip makes another shelf the main one (the stack slides, strips grow/shrink with the same easing). Tuning: `activeH()` / `stripH()` and `--dur`, `--ease` in `:root`.

## Palette
Chalk & Sage: neutral chalk room, sage-grey shelf wall, stone boards, ink-green accent (`--accent`), neutral shadows (`--shadow-rgb`). Only the books bring colour. All colours are tokens at the top of `:root`; `--p-*` are the same roles for text on paper (book pages, About/Contact).
