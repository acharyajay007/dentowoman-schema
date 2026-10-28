# Dentowoman Book JSON Schema

Public, versioned JSON Schema for structured educational books prepared for Dentowoman Studio.

## Current contract: 0.9

- Schema: https://raw.githubusercontent.com/acharyajay007/dentowoman-schema/main/schemas/book-0.9.schema.json
- Standard: JSON Schema Draft 2020-12
- Canonical `$id`: the schema URL above
- Content: ordered chapters/topics, 15 content-component types, image references, design settings, and optional 12-column row placement.
- Contract 0.9 adds image-grid `sizing` (`fixed` or `flexible`), optional `columns` (1-4), and supports retaining one image after removal. Omitted settings preserve the legacy flexible two-column presentation.
- Contract 0.8 adds optional per-component font overrides using the nine bundled font families. Omit `font` to inherit book typography; tables honor the book body font or their explicit override.
- Contract 0.7 adds generic Note/Info/Success/Important/Warning/Error callouts and persistent table widths, alignment and styles. Legacy callout kinds and earlier supported book versions remain importable.
- Contract 0.6 introduced multiple components per column using `grid.stack`; legacy optional component labels remain accepted.

## Previous contracts

- Contract 0.8: https://raw.githubusercontent.com/acharyajay007/dentowoman-schema/main/schemas/book-0.8.schema.json
- Contract 0.7: https://raw.githubusercontent.com/acharyajay007/dentowoman-schema/main/schemas/book-0.7.schema.json
- Contract 0.6: https://raw.githubusercontent.com/acharyajay007/dentowoman-schema/main/schemas/book-0.6.schema.json
- Contract 0.5: https://raw.githubusercontent.com/acharyajay007/dentowoman-schema/main/schemas/book-0.5.schema.json

Agents should fetch the selected version before preparing JSON. If retrieval fails, request the offline schema instead of guessing its fields. A book's `schemaVersion` selects the content contract; do not add unsupported fields to the book merely to associate an editor schema.

Structural JSON Schema validation does not replace semantic/reference validation, local image integrity checks, provenance and permissions review, or actual PDF print preflight. The schema contains no source notes or private educational material.

New incompatible contracts receive new versioned paths. This repository hosts the schema, not the Studio desktop application or source-conversion service.
