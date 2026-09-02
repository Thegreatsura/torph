# torph

## 0.1.0

### Minor Changes

- c86b1e0: Word- and character-level diffing, multi-line text, and a rewritten container animation

  #### New
  - Multi-line text.
  - Words that survive a change travel to their new position instead of crossfading.
  - `onAnimationCancel`, so a superseded morph can still be awaited.
  - `segmentText` and `diffSegments` exports.

  #### Fixed
  - Markup in a value could execute scripts in React.
  - The container no longer gets stuck at the wrong size.

## 0.0.10

### Patch Changes

- 4462d5e: Fix the container getting stuck collapsed after text is cleared and retyped (#43).
- 4462d5e: Smoother enter animation timings.
- 4462d5e: Sharper positioning at small text sizes.
- 4462d5e: Fix missing `TextMorph` types in Svelte.
- b063c2e: Fix Vue `TextMorph` rendering empty until the `text` prop changes.

## 0.0.9

### Patch Changes

- Fix Svelte SSR, and shrink the framework bundles.

## 0.0.8

### Patch Changes

- 08b3274: Fix the Vue build failing to resolve the `torph` package entry.

## 0.0.7

### Patch Changes

- 83b06a8: Spring easing — new `spring()` helper, and `ease` accepts a `SpringParams` object.
- eb7bce0: Smaller package, 64.9 kB → 11.8 kB, with fixed Vue and Svelte types.
- 83b06a8: Fix animation spam when text changes rapidly.
- f6cb510: Animations redirect smoothly when text changes mid-animation instead of snapping.

## 0.0.6

### Patch Changes

- 7fe6190: Svelte 5 support.
- bcc7d14: `scale` prop on the Vue and Svelte components.
- 48754a5: No longer require string literals for morph targets.
- 48754a5: Fix text overlap during morphing.
- 48754a5: Fix SSR cleanup, tree-shaking and the types export.

## 0.0.5

### Patch Changes

- Better animation.

## 0.0.4

### Patch Changes

- Fix a missing type export.

## 0.0.3

### Patch Changes

- Fix FOUC under SSR.

## 0.0.2

### Patch Changes

- Remove dependencies.

## 0.0.1

- First release.
