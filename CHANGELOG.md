# Changelog

All notable changes to this package. Versions follow semver, independent of the Nabi toolchain.

## 0.1.0 (unreleased)

First release.

- Declarative figures (`Figure`, `Axes`, layers) built with method chains;
  panels combine with `+` (overlay), `|` (side by side) and `/` (stacked).
- Layers: line, step, scatter, bars, histograms, areas, error bars, box and
  violin plots, heatmaps, contours, vector fields, text and annotations.
- Linear, log, symlog and date axes; extended-Wilkinson ticks and number
  formats; `$..$` math in labels.
- Published colormaps, Okabe-Ito and Tableau 10 cycles, light and dark
  themes from the docs site's tokens.
- Output to deterministic SVG, to PNG (own rasterizer, embedded Geist font,
  own encoder) and to the terminal; `RichDisplay` for the Jupyter kernel.
- The `table` feature: `plot::frame` plots `table::Table` columns by name.
- No C libraries and no system fonts: every target, wasm included. Needs
  Nabi 0.1 or later.
