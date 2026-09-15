# Report

## Candidate Information

|  |  |
| --- | --- |
| Candidate | `spec-example-2026-04-08.jsonld` |
| Description | The specification's [Complete Example](https://transparency-certified.github.io/trace-specification/docs/tro-declaration-format#complete-example), copied verbatim<br>on 2026-09-03 from the 2026-04-08 revision. Its four<br>`trov:hashValue` fields carry elided placeholders<br>(`a1b2c3d4...`, `aaa1...`) and its `@context` declares no<br>`@base`. |
| Target | 4 STANDALONE-TRO |
| Target declared by | the candidate manifest |

## Tier Assessments

| Tier | ID | Description | Status |
| --- | --- | --- | --- |
| 1 | SAFE-JSON | JSON that every parser reads the same way | ✅ met |
| 2 | VALID-JSON-LD | Valid JSON-LD | ✅ met |
| 3 | TRACE-JSON-LD | JSON-LD in the restricted form the TRACE Specification<br>defines for TRO declarations | ✅ met |
| 4 | STANDALONE-TRO | A TRO declaration with the structure the Specification<br>requires, whose references resolve within it | ❌ not met |
| *5* | *LINKABLE-TRO* | *A TRO declaration whose element identifiers cannot<br>collide with another TRO's* | *not claimed* |

## Expectation Findings by Tier

### Tier 1 — SAFE-JSON

| Expectation | Summary | Status |
| --- | --- | --- |
| duplicate-member-names-absent | No object repeats a member name | ✅ met |
| json-parses | The candidate parses as JSON without errors | ✅ met |
| lone-surrogates-absent | No string or member name has an unpaired surrogate | ✅ met |
| numbers-within-range | Every number fits a double; every integer is exact | ✅ met |
| utf8-encoded | The candidate is UTF-8 | ✅ met |

Assessment status: ✅ met

### Tier 2 — VALID-JSON-LD

| Expectation | Summary | Status |
| --- | --- | --- |
| context-well-formed | The root `@context`, if any, has a form JSON-LD allows | ✅ met |
| graph-well-formed | The root `@graph`, if any, holds objects, not bare values | ✅ met |
| ids-and-types-strings | Every `@id` is a string; every `@type` a string or an array<br>of strings | ✅ met |

Assessment status: ✅ met

### Tier 3 — TRACE-JSON-LD

| Expectation | Summary | Status |
| --- | --- | --- |
| base-simple-url | The `@base`, if any, is a simple URL: a host, no user<br>info, dot segments, query or fragment, only URL<br>characters, and a final `/` | ✅ met |
| base-web-scheme | The `@base`, if any, uses the `https` or `http` scheme | ✅ met |
| disallowed-context-keywords-absent | No keyword in the `@context` other than `@base` | ✅ met |
| disallowed-node-keywords-absent | No keyword outside the `@context` other than `@context`,<br>`@graph`, `@id` and `@type` | ✅ met |
| prefix-namespaces-terminated | Every prefix maps to an absolute IRI ending in `#` or `/` | ✅ met |
| relative-ids-plain | Every relative `@id` is a plain path, with no leading `/`,<br>no `.` or `..` segments, and no `?` or `#` | ✅ met |
| root-context-and-graph-only | A JSON object with an `@context`, an `@graph`, and nothing<br>else | ✅ met |

Assessment status: ✅ met

### Tier 4 — STANDALONE-TRO

| Expectation | Summary | Status |
| --- | --- | --- |
| composition-fingerprinted | The TRO's composition, if any, carries a fingerprint | ✅ met |
| hashes-well-formed | The TRO's artifact and fingerprint hashes are<br>well-formed sha256 | ❌ not met |
| tro-assembled-by-trs | The TRO names its assembling system, typed as a TRS | ✅ met |
| tro-top-level-in-graph | The TRO is a top-level member of the `@graph` | ✅ met |
| trov-terms-known | Every `trov:` name is one TROV defines | ✅ met |

Assessment status: ❌ not met

### Tier 5 — LINKABLE-TRO

| Expectation | Summary | Status |
| --- | --- | --- |
| *base-declared* | *The `@context` includes an `@base`* | *not claimed* |
| *node-ids-present* | *Every node carries an explicit `@id`* | *not claimed* |

Assessment status: *not claimed*

## Details

### Unmet expectation: hashes-well-formed

Expectation details: Each trov:hash on the TRO's artifacts and composition fingerprint names sha256 as its algorithm and carries a value of 64 lowercase hexadecimal digits.

| Found | Where | Expectation not met because |
| --- | --- | --- |
| `"aaa1..."` | `/@graph/0/trov:hasComposition/trov:hasArtifact/0/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
| `"bbb2..."` | `/@graph/0/trov:hasComposition/trov:hasArtifact/1/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
| `"ccc3..."` | `/@graph/0/trov:hasComposition/trov:hasArtifact/2/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
| `"a1b2c3d4..."` | `/@graph/0/trov:hasComposition/trov:hasFingerprint/trov:hash/trov:hashValue` | a sha256 value is 64 lowercase hexadecimal digits |
