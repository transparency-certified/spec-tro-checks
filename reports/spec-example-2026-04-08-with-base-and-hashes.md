# Report

## Candidate Information

|  |  |
| --- | --- |
| Candidate | `spec-example-2026-04-08-with-base-and-hashes.jsonld` |
| Description | The 2026-04-08 example with an `@base` in its `@context` and a sha256 value in each of the four hash fields. Every value is computed from the artifact's own `@id` for reproducibility's sake only. |
| Target | Tier 1 — Self-Contained |
| Target declared by | the candidate manifest |

## Assessments

### By Representation Tier

| Tier | Name | Description | Status |
| --- | --- | --- | --- |
| 0 | Well-Formed | Valid JSON-LD conforming to the profile TRACE tooling expects | ✅ met |
| 1 | Self-Contained | References within the TRO resolve; its identifiers need not be unique outside it | ✅ met |
| *2* | *Linkable-Data* | *Element identifiers cannot collide with another TRO's; TRO elements can be published* | *not claimed* |

### By Individual Expectation

| Tier | Expectation | Summary | Status |
| --- | --- | --- | --- |
| 0 | context-well-formed | The root `@context`, if any, has a form JSON-LD allows | ✅ met |
| 0 | document-rooted-in-nodes | The document is an object or an array of objects | ✅ met |
| 0 | graph-well-formed | The root `@graph`, if any, holds objects, not bare values | ✅ met |
| 1 | composition-fingerprinted | The TRO's composition, if any, carries a fingerprint | ✅ met |
| 1 | context-and-graph-present | A JSON object with an `@context` and an `@graph` | ✅ met |
| 1 | hashes-well-formed | The TRO's artifact and fingerprint hashes are well-formed sha256 | ✅ met |
| 1 | tro-assembled-by-trs | The TRO names its assembling system, typed as a TRS | ✅ met |
| 1 | tro-top-level-in-graph | The TRO is a top-level member of the `@graph` | ✅ met |
| 1 | trov-terms-known | Every `trov:` name is one TROV defines | ✅ met |
| *2* | *base-declared* | *The `@context` includes an `@base`* | *not claimed* |
| *2* | *node-ids-present* | *Every node carries an explicit `@id`* | *not claimed* |
