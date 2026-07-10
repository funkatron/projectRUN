# Metadata Model

Project RUN uses human-readable YAML records backed by a JSON Schema. The model is intentionally small at first: enough structure for search and migration, without requiring every field before an item can be recorded.

## Core rules

- One catalog record per intellectual or physical item.
- Use stable lowercase identifiers such as `run-1988-01`.
- Record unknown values as omitted or `null`; never guess.
- Use ISO 8601 dates where possible.
- Preserve observations and stories separately from normalized facts.
- Mark unverified records as `provisional`.
- Keep external identifiers with their source.

## Recommended fields

| Field | Purpose |
|---|---|
| `id` | Stable project identifier |
| `record_type` | Broad kind of record, such as `periodical_issue`, `hardware`, or `software` |
| `title` | Display title |
| `date` | Publication, release, or approximate date |
| `creators` | Publishers, manufacturers, authors, or other responsible entities |
| `platforms` | Relevant computer or console platforms |
| `identifiers` | ISBN, ISSN, serial number, model number, external IDs, and similar values |
| `physical` | Condition, completeness, dimensions, packaging, and storage location |
| `provenance` | Acquisition and ownership history |
| `stories` | Personal memories, use history, and human context |
| `subjects` | Searchable topical terms |
| `related` | Relationships to other Project RUN records |
| `external_resources` | Scans, manuals, databases, and related public sources |
| `media` | Local photographs, scans, audio, or video |
| `verification_status` | `provisional`, `partially_verified`, or `verified` |
| `notes` | Free-form cataloging notes |
| `record_history` | Creation and update information |

## Periodical issues

Periodical issue IDs should normally use the publication slug and cover date:

```text
run-1988-01
compute-gazette-1989-06
```

Suggested path:

```text
collections/periodicals/run/1988-01.yaml
```

Associated media may later be stored under:

```text
collections/periodicals/run/1988-01/
```

## External resources

Each external resource should state the relationship rather than merely provide a URL:

```yaml
external_resources:
  - provider: internet_archive
    identifier: example_identifier
    relationship: probable_match
    checked: 2026-07-09
    notes: Cover date matches; edition not yet compared page by page.
```

## Human context

Stories are first-class metadata, but should retain attribution and uncertainty:

```yaml
stories:
  - kind: personal_memory
    attribution: collection_owner
    text: This issue was retained because...
    certainty: remembered
```

## Evolution

The schema will change as real cataloging exposes useful distinctions. Changes should favor migration and backward compatibility. A field should not become mandatory unless the project can reliably supply it for most applicable records.