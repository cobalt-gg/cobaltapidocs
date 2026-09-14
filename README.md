# Cobalt internal API reference

This Mintlify site documents the backend contract used by Cobalt app developers and AI agents. Read it to change a client without inspecting or modifying the backend.

Start with `index.mdx`, `quickstart.mdx` (client workflows), and `architecture.mdx` (request conventions). Feature pages document authentication, inputs, outputs, validation, side effects, pagination, and limitations.

The reference was checked against the active CobaltBackend checkout at revision `2ebf4c8c6923286ebee5192c9a3fcc1ae37c4a25` on September 13, 2026. Cobalt ID was inspected as a consumer. This is not a live production-version assertion.

## Maintaining a contract

- Update the affected endpoint and workflow together.
- Preserve exact wire casing and response envelopes.
- Document non-200 success states, nullability, retry semantics, and side effects.
- Distinguish provider pass-through responses from fixed Cobalt schemas.
- Describe implemented behavior, including limitations. Do not turn client comments or planned routes into capabilities.
- Keep deployment instructions and backend extension authoring outside this client reference.

## Preview and validation

Run the Mintlify CLI from this directory:

```sh
npx mint dev
npx mint validate
npx mint broken-links
```

Navigation is defined in `docs.json`.
