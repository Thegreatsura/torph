---
"torph": patch
---

Numbers morph by place value, and a morph is readable to screen readers.

#### New

- Number morphing, matched digit by digit. On by default — `numbers={false}` to opt out.
- `update()` and the components accept a `number`, with `locale` and `decimals` options.
- `cursorIndex`, for editable fields.
- `segmentNumber`, `isNumericWord` and `decimalSeparator` exports.

#### Improved

- Digits keep their column, so `99 → 199` grows a digit on the left.
- Currency symbols, percent signs and units stay put.
- `COVID-19` and dates still morph as text.

#### Fixed

- Screen readers read the value, not its mid-morph fragments. Add `aria-live` to announce changes.
- React's `onAnimationStart` and `onAnimationComplete` no longer go stale.
