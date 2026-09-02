---
"torph": patch
---

Numbers morph by place value, and a morph is readable to screen readers.

#### New

- Numeric words are matched digit by digit, so a figure that changes reads as one
  number moving. On by default — `numbers={false}` for the old behaviour.
- `update()` and the components accept a `number`, formatted with `locale` and the
  new `decimals` option.
- `cursorIndex` matches by caret instead of by column, for editable fields.
- Exports `segmentNumber`, `isNumericWord`, `decimalSeparator`, and the
  `NumberSegment` and `DiffOptions` types.

#### Improved

- Digits keep their column: `99 → 199` grows a digit on the left, and
  `999,999 → 1,000,000` slides its comma along by one group.
- Currency symbols, percent signs and units stay put.
- Only whole numeric tokens qualify, so `COVID-19` and `2024-01-01` still morph as text.
- A run of characters with nothing surviving inside it is replaced as one gesture.

#### Fixed

- Mid-morph fragments are `aria-hidden` and the value is written once in a clipped
  `[torph-sr]` node, so assistive technology reads the value and not its leftovers.
  Put `aria-live` on the element to have changes announced.
- `prefers-reduced-motion` turning off mid-session left the instance without a
  stylesheet, so the next morph animated against nothing.
- React's `onAnimationStart` and `onAnimationComplete` no longer go stale when they
  close over component state.
