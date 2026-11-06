# Demos

Small interactive demos, served as a plain static site by GitHub Pages at https://demo.divo.link

There is no build step: every file here is served as-is.

```
index.html        front page; lists the demos from demos.js
demos.js          the list of demos (one entry per folder)
assets/site.css   minimal shared base (system font, light/dark)
assets/cmu.css    optional Computer Modern font for demos
assets/fonts/     Computer Modern (CMU Serif) and its license, OFL.txt
_template/        starting point for a new demo
404.html          shown for unknown addresses
orbitals/         Orbital Explorer
CNAME             the custom domain (demo.divo.link)
LICENSE           MIT
.nojekyll         tells Pages to serve files untouched
```

## Add a demo

1. Copy `_template/` to a new folder, e.g. `pendulum/`, and build the demo in its `index.html`.
   Each demo can have its own look; demos can also be fully self-contained (like `orbitals/`).
2. Add an entry to `demos.js`:
   ```js
   { path: "pendulum/", title: "Pendulum", description: "One line on what it shows." },
   ```
3. Commit and push. Pages redeploys within a minute or two, and the demo is live at
   `https://demo.divo.link/pendulum/`.

Use relative links (`../assets/site.css`) so pages also work when opened straight from disk.

## License

MIT, see [LICENSE](LICENSE). The Computer Modern fonts are under the SIL Open Font License ([assets/fonts/OFL.txt](assets/fonts/OFL.txt)).
