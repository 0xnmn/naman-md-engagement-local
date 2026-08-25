# naman-md-engagement-local

Public JSON storage for local and preview engagement on [naman.md](https://naman.md).

Each canonical website path maps to one file under `pages/`. For example:

- `/writings/on-weak-men` -> `pages/writings/on-weak-men.json`
- `/stuff/ipad-mini` -> `pages/stuff/ipad-mini.json`
- `/running/example-race` -> `pages/running/example-race.json`
- `/` -> `pages/index.json`

The naman.md backend is the only supported writer. Comments and replies are append-only through the API, replies are limited to one level, and likes are one-way per anonymous browser identity. Repository owners may edit files directly for moderation.

See [schema.json](./schema.json) for the stored document shape.

## Pixel Wall

Each 64 × 64 screen is stored independently at `pixels/<id-prefix>/<id>.json`. A screen contains its creation date, optional display name, anonymous actor hash when available, and the exact base64 RGB grid. The newest 12 screens rotate on the physical wall; archival status is derived rather than written.

See [pixel-schema.json](./pixel-schema.json) for the stored screen shape.
