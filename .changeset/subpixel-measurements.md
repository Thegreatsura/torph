---
"torph": patch
---

Use subpixel measurements for morph layout

Layout previously read `offsetWidth`/`offsetHeight`/`offsetLeft`/`offsetTop`,
which round to whole pixels. At small sizes and on fractional-DPI displays the
rounding accumulated across segments, so characters drifted from their measured
positions and the container size transition landed slightly off. Measurement now
goes through `getBoundingClientRect()`, with exiting segments positioned
relative to the container's rect.
