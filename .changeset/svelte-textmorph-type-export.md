---
"torph": patch
---

Fix the `TextMorph` type not passing through from the Svelte build

`torph/svelte` exported the component without a type declaration, so
TypeScript consumers got an implicit `any` (or an error under
`noImplicitAny`) when importing `TextMorph`. It is now declared as
`Component<TextMorphProps>`.
