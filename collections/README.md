# Collections

This directory contains Project RUN catalog records.

## Planned categories

- `periodicals/` — magazines, newsletters, journals, and individual issues
- `hardware/` — computers, consoles, peripherals, components, and accessories
- `software/` — commercial, shareware, public-domain, and personally created software
- `media/` — disks, tapes, cartridges, optical media, and other carriers
- `books/` — manuals, books, catalogs, and printed reference material
- `ephemera/` — advertisements, receipts, flyers, packaging inserts, and related material
- `recordings/` — audio and video records

Only `periodicals/` has an initial real record. The remaining categories are structural stubs and should be populated through representative cataloging.

## Record format

Records are YAML and should follow `schemas/catalog-item.schema.json` as closely as practical. The schema is deliberately permissive during the foundation stage.

## Sensitive information

Public records should not expose precise home storage locations, private contact information, purchase credentials, or other security-sensitive details. A future private inventory layer may hold operational location data separately from the public catalog.