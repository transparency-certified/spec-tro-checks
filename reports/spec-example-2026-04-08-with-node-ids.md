# Report

## Candidate Information

|  |  |
| --- | --- |
| Candidate | `spec-example-2026-04-08-with-node-ids.jsonld` |
| Description | The preceding candidate with an `@id` on each of its five remaining bare node objects: `trov:createdWith` and the four `trov:hash` nodes. |
| Target | Tier 2 — Linkable-Data |
| Target declared by | the candidate manifest |

## Assessments

### By Representation Tier

| Tier | Name | Description | Status |
| --- | --- | --- | --- |
| 0 | Well-Formed | Valid JSON-LD conforming to the profile TRACE tooling expects | ✅ met |
| 1 | Self-Contained | References within the TRO resolve; its identifiers need not be unique outside it | ✅ met |
| 2 | Linkable-Data | Element identifiers cannot collide with another TRO's; TRO elements can be published | ✅ met |

### By Individual Expectation

| Tier | Expectation | Summary | Status |
| --- | --- | --- | --- |
| 0 | has-well-formed-context | The `@context` takes a shape JSON-LD allows | ✅ met |
| 0 | has-well-formed-graph | The `@graph` holds nodes, not scalars | ✅ met |
| 0 | node-rooted | The document is a node object, not a scalar | ✅ met |
| 1 | composition-fingerprint | Includes a digest of the artifact composition | ✅ met |
| 1 | hash-form | Every hash is a checkable sha256 value | ✅ met |
| 1 | tro-minimal | The declaration has the two parts a TRO needs | ✅ met |
| 1 | trov-terms-known | No `trov:` name is misspelt or invented | ✅ met |
| 1 | trs-typed | The assembling system declares itself a TRS | ✅ met |
| 2 | context-base | Identifiers expand into a namespace of its own | ✅ met |
| 2 | node-id-present | No node is unreferenceable from outside | ✅ met |
