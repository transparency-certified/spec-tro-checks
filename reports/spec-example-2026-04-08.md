# Report

## Candidate Information

|  |  |
| --- | --- |
| Candidate | `spec-example-2026-04-08.jsonld` |
| Description | The specification's [Complete Example](https://transparency-certified.github.io/trace-specification/docs/tro-declaration-format#complete-example), copied verbatim on 2026-09-03 from the 2026-04-08 revision. Its four `trov:hashValue` fields carry elided placeholders (`a1b2c3d4...`, `aaa1...`) and its `@context` declares no `@base`. |
| Target | Tier 1 — Self-Contained |
| Target declared by | the candidate manifest |

## Assessments

### By Representation Tier

| Tier | Name | Description | Status |
| --- | --- | --- | --- |
| 0 | Well-Formed | Valid JSON-LD conforming to the profile TRACE tooling expects | ✅ met |
| 1 | Self-Contained | References within the TRO resolve; its identifiers need not be unique outside it | ❌ not met |
| *2* | *Linkable-Data* | *Element identifiers cannot collide with another TRO's; TRO elements can be published* | *not claimed* |

### By Individual Expectation

| Tier | Expectation | Summary | Status |
| --- | --- | --- | --- |
| 0 | context-well-formed | The root `@context`, if any, has a form JSON-LD allows | ✅ met |
| 0 | disallowed-context-keywords-absent | No keyword in the `@context` other than `@base` | ✅ met |
| 0 | disallowed-node-keywords-absent | No keyword outside the `@context` other than `@context`, `@graph`, `@id` and `@type` | ✅ met |
| 0 | document-rooted-in-nodes | The document is an object or an array of objects | ✅ met |
| 0 | graph-well-formed | The root `@graph`, if any, holds objects, not bare values | ✅ met |
| 0 | ids-and-types-strings | Every `@id` is a string; every `@type` a string or an array of strings | ✅ met |
| 1 | composition-fingerprinted | The TRO's composition, if any, carries a fingerprint | ✅ met |
| 1 | context-and-graph-present | A JSON object with an `@context` and an `@graph` | ✅ met |
| 1 | hashes-well-formed | The TRO's artifact and fingerprint hashes are well-formed sha256 | ❌ not met |
| 1 | tro-assembled-by-trs | The TRO names its assembling system, typed as a TRS | ✅ met |
| 1 | tro-top-level-in-graph | The TRO is a top-level member of the `@graph` | ✅ met |
| 1 | trov-terms-known | Every `trov:` name is one TROV defines | ✅ met |
| *2* | *base-declared* | *The `@context` includes an `@base`* | *not claimed* |
| *2* | *node-ids-present* | *Every node carries an explicit `@id`* | *not claimed* |

## Details

### Unmet expectation: hashes-well-formed

Expectation details: Each trov:hash on the TRO's artifacts and composition fingerprint names sha256 as its algorithm and carries a value of 64 lowercase hexadecimal digits.

| Found | Where | Expectation not met because |
| --- | --- | --- |
| `"aaa1..."` | `/@graph/0/trov:hasComposition/trov:hasArtifact/0/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
| `"bbb2..."` | `/@graph/0/trov:hasComposition/trov:hasArtifact/1/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
| `"ccc3..."` | `/@graph/0/trov:hasComposition/trov:hasArtifact/2/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
| `"a1b2c3d4..."` | `/@graph/0/trov:hasComposition/trov:hasFingerprint/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
