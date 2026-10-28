# Dentowoman Book JSON Schema

Public, versioned JSON Schema for structured educational books prepared for Dentowoman Studio.

## Contract 0.5

- Schema: https://raw.githubusercontent.com/acharyajay007/dentowoman-schema/main/schemas/book-0.5.schema.json
- Standard: JSON Schema Draft 2020-12
- Canonical `$id`: the schema URL above
- Content: ordered chapters/topics, 15 content-component types, image references, design settings, and optional 12-column row placement.

Agents should fetch the selected version before preparing JSON. If retrieval fails, request the offline schema instead of guessing its fields. A book's `schemaVersion` selects the content contract; do not add unsupported fields to the book merely to associate an editor schema.

Structural JSON Schema validation does not replace semantic/reference validation, local image integrity checks, provenance and permissions review, or actual PDF print preflight. The schema contains no source notes or private educational material.

New incompatible contracts receive new versioned paths. This repository hosts the schema, not the Studio desktop application or source-conversion service.