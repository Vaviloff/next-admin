---
"@premieroctet/next-admin": patch
"@premieroctet/next-admin-generator-prisma": patch
---

Support React 19 theme resolution and Prisma `importFileExtension = "ts"` schemas.

- Bump `next-themes` to `^0.4.6` (adds React 19 peer support; the `ThemeProvider` props and `useTheme()` API used by next-admin are unchanged).
- Fix the Prisma generator's ESM/CJS specifier rewrite to also strip a trailing `.ts` (e.g. `./enums.ts` emitted for `importFileExtension = "ts"` schemas), so generated `.mjs`/`.js` files reference resolvable paths.
