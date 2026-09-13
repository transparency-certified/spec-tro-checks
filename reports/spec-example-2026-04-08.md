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
| 0 | has-well-formed-context | The `@context` takes a shape JSON-LD allows | ✅ met |
| 0 | has-well-formed-graph | The `@graph` holds nodes, not scalars | ✅ met |
| 0 | node-rooted | The document is a node object, not a scalar | ✅ met |
| 1 | composition-fingerprint | Includes a digest of the artifact composition | ✅ met |
| 1 | hash-form | Every hash is a checkable sha256 value | ❌ not met |
| 1 | tro-minimal | The declaration has the two parts a TRO needs | ✅ met |
| 1 | trov-terms-known | No `trov:` name is misspelt or invented | ✅ met |
| 1 | trs-typed | The assembling system declares itself a TRS | ✅ met |
| *2* | *context-base* | *Identifiers expand into a namespace of its own* | *not claimed* |
| *2* | *node-id-present* | *No node is unreferenceable from outside* | *not claimed* |

## Details

### Unmet expectation: hash-form

Expectation details: Every hash in the declaration names its algorithm and carries a value of the right shape for it.

| Found | Where | Expectation not met because |
| --- | --- | --- |
| `"aaa1..."` | `/@graph/0/trov:hasComposition/trov:hasArtifact/0/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
| `"bbb2..."` | `/@graph/0/trov:hasComposition/trov:hasArtifact/1/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
| `"ccc3..."` | `/@graph/0/trov:hasComposition/trov:hasArtifact/2/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
| `"a1b2c3d4..."` | `/@graph/0/trov:hasComposition/trov:hasFingerprint/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
