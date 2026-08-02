---
"torph": patch
---

Improve enter animation timings

Entering segments animated their transform from a single keyframe with no
explicit end state, and faded in from the moment the morph started — so new
characters appeared before the segments around them had moved into place. The
transform now runs as an explicit two-keyframe animation ending at `none`, and
the fade for new segments is delayed by a quarter of the duration so movement
resolves first.
