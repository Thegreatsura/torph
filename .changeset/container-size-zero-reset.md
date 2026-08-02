---
"torph": patch
---

Fix the container staying collapsed at `0px` after text is cleared and retyped

When text was cleared and a new character typed before the fade completed,
`element.offsetWidth` measured 0 and hit the early-return guard in
`transitionContainerSize`, leaving inline `width`/`height` pinned at `0px`
permanently. The guard now resets both to `auto` before returning, so the
container reverts to natural content sizing.

Fixes #43
