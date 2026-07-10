# Contributing

Project RUN is currently a small, evolving archive. Contributions should improve accuracy, accessibility, context, or preservation without making uncertain information appear settled.

## General approach

- Prefer useful, reviewable increments over large speculative reorganizations.
- Cite sources for factual claims that are not directly observable from an item.
- Preserve uncertainty explicitly.
- Do not invent missing metadata to satisfy a schema.
- Keep personal stories attributed and distinguish memory from verified fact.
- Avoid committing private addresses, precise home storage locations, credentials, or sensitive personal information.

## Catalog records

Catalog records are YAML files under `collections/`.

Before marking a record `verified`, check the relevant facts against the physical object or a reliable primary source. External scans should be compared for edition, date, and completeness rather than assumed to be identical.

## Documents

Documents marked **Stub** are invitations for later development, not finalized policy. When replacing a stub, retain useful open questions or explain the decision that resolved them.

## Commit style

Use concise imperative commit messages, for example:

```text
Add Commodore 128 catalog record
Link RUN issue to Internet Archive scan
Document floppy imaging workflow
```

## Licensing

A project license has not yet been chosen. Do not add third-party copyrighted material unless its inclusion and redistribution are clearly permitted. Links and descriptive metadata are generally preferable to copying source material into the repository.