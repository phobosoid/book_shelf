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
