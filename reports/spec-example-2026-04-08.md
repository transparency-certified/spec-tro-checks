# Report

Candidate: `spec-example-2026-04-08.jsonld`

The specification's [Complete Example](https://transparency-certified.github.io/trace-specification/docs/tro-declaration-format#complete-example), copied verbatim on 2026-09-03 from the 2026-04-08 revision. Its four `trov:hashValue` fields carry elided placeholders (`a1b2c3d4...`, `aaa1...`) and its `@context` declares no `@base`.

Target: Tier 1 -- Self-Contained (from manifest declaration)

## Assessment

- Tier 0 -- Well-Formed: met
- Tier 1 -- Self-Contained: unmet

## Findings

### has-well-formed-context (Tier 0): met

### has-well-formed-graph (Tier 0): met

### node-rooted (Tier 0): met

### composition-fingerprint (Tier 1): met

### hash-form (Tier 1): unmet

- `/@graph/0/trov:hasComposition/trov:hasArtifact/0/trov:hash/trov:hashValue` found `"aaa1..."` — a sha256 value is 64 lowercase hexadecimal digits
- `/@graph/0/trov:hasComposition/trov:hasArtifact/1/trov:hash/trov:hashValue` found `"bbb2..."` — a sha256 value is 64 lowercase hexadecimal digits
- `/@graph/0/trov:hasComposition/trov:hasArtifact/2/trov:hash/trov:hashValue` found `"ccc3..."` — a sha256 value is 64 lowercase hexadecimal digits
- `/@graph/0/trov:hasComposition/trov:hasFingerprint/trov:hash/trov:hashValue` found `"a1b2c3d4..."` — a sha256 value is 64 lowercase hexadecimal digits

### tro-minimal (Tier 1): met

### trov-terms-known (Tier 1): met

### trs-typed (Tier 1): met

### context-base (Tier 2): not claimed

### node-id-present (Tier 2): not claimed
