# Report

## Candidate Information

|  |  |
| --- | --- |
| Candidate | `spec-example-2026-04-08-with-node-ids.jsonld` |
| Description | The preceding candidate with an `@id` on each of its five remaining bare node objects: `trov:createdWith` and the four `trov:hash` nodes. |
| Target | 5 LINKABLE-TRO |
| Target declared by | the candidate manifest |

## Assessments

### By Representation Tier

| Tier | ID | Description | Status |
| --- | --- | --- | --- |
| 1 | SAFE-JSON | JSON that every parser reads the same way | ✅ met |
| 2 | VALID-JSON-LD | Valid JSON-LD, whatever vocabulary it uses | ✅ met |
| 3 | TRACE-JSON-LD | JSON-LD in the restricted form the TRACE Specification defines for TRO declarations | ✅ met |
| 4 | STANDALONE-TRO | A TRO declaration with the structure the Specification requires, whose references resolve within it | ✅ met |
| 5 | LINKABLE-TRO | A TRO declaration whose element identifiers cannot collide with another TRO's | ✅ met |

### By Individual Expectation

| Tier | Expectation | Summary | Status |
| --- | --- | --- | --- |
| 1 | duplicate-member-names-absent | No object repeats a member name | ✅ met |
| 1 | json-parses | The candidate is JSON | ✅ met |
| 1 | lone-surrogates-absent | No string or member name has an unpaired surrogate | ✅ met |
| 1 | numbers-within-range | Every number fits a double; every integer is exact | ✅ met |
| 1 | utf8-encoded | The candidate is UTF-8 | ✅ met |
| 2 | context-well-formed | The root `@context`, if any, has a form JSON-LD allows | ✅ met |
| 2 | graph-well-formed | The root `@graph`, if any, holds objects, not bare values | ✅ met |
| 2 | ids-and-types-strings | Every `@id` is a string; every `@type` a string or an array of strings | ✅ met |
| 3 | base-simple-url | The `@base`, if any, is a simple URL: a host, no user info, dot segments, query or fragment, only URL characters, and a final `/` | ✅ met |
| 3 | base-web-scheme | The `@base`, if any, uses the `https` or `http` scheme | ✅ met |
| 3 | disallowed-context-keywords-absent | No keyword in the `@context` other than `@base` | ✅ met |
| 3 | disallowed-node-keywords-absent | No keyword outside the `@context` other than `@context`, `@graph`, `@id` and `@type` | ✅ met |
| 3 | prefix-namespaces-terminated | Every prefix maps to an absolute IRI ending in `#` or `/` | ✅ met |
| 3 | relative-ids-plain | Every relative `@id` is a plain path, with no leading `/`, no `.` or `..` segments, and no `?` or `#` | ✅ met |
| 3 | root-context-and-graph-only | A JSON object with an `@context`, an `@graph`, and nothing else | ✅ met |
| 4 | composition-fingerprinted | The TRO's composition, if any, carries a fingerprint | ✅ met |
| 4 | hashes-well-formed | The TRO's artifact and fingerprint hashes are well-formed sha256 | ✅ met |
| 4 | tro-assembled-by-trs | The TRO names its assembling system, typed as a TRS | ✅ met |
| 4 | tro-top-level-in-graph | The TRO is a top-level member of the `@graph` | ✅ met |
| 4 | trov-terms-known | Every `trov:` name is one TROV defines | ✅ met |
| 5 | base-declared | The `@context` includes an `@base` | ✅ met |
| 5 | node-ids-present | Every node carries an explicit `@id` | ✅ met |
