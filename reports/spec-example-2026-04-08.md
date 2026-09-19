# Report

## Candidate Information

<table>
<tbody>
<tr><td>Candidate</td><td nowrap><samp>spec-example-2026-04-08.jsonld</samp></td></tr>
<tr><td>Description</td><td>The specification's <a href="https://transparency-certified.github.io/trace-specification/docs/tro-declaration-format#complete-example">Complete Example</a>, copied verbatim on 2026-09-03 from the 2026-04-08 revision. Its four <code>trov:hashValue</code> fields carry elided placeholders (<code>a1b2c3d4...</code>, <code>aaa1...</code>) and its <code>@context</code> declares no <code>@base</code>.</td></tr>
<tr><td>Target</td><td>6&nbsp;STANDALONE&#8209;TRO</td></tr>
<tr><td>Target&nbsp;declared&nbsp;by</td><td>the candidate manifest</td></tr>
</tbody>
</table>

## Tier Assessments

<table>
<thead>
<tr><th align="left">Tier</th><th align="left">ID</th><th align="left">Description</th><th align="left">Status</th></tr>
</thead>
<tbody>
<tr><td>1</td><td>SAFE&#8209;JSON</td><td>JSON that every supported parser reads the same way</td><td>✅&nbsp;met</td></tr>
<tr><td>2</td><td>SAFE&#8209;JSON&#8209;LD</td><td>JSON-LD that every supported processor reads the same way</td><td>✅&nbsp;met</td></tr>
<tr><td>3</td><td>TRACE&#8209;JSON&#8209;LD</td><td>JSON-LD in the restricted form the TRACE Specification requires for TRO declarations</td><td>✅&nbsp;met</td></tr>
<tr><td>4</td><td>USES&#8209;TROV&#8209;CORRECTLY</td><td>JSON-LD whose TROV terms, and the schema.org terms TROV specifies, are used as they are defined</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr><td>5</td><td>DEFINES&#8209;TRS</td><td>JSON-LD that defines a Trusted Research System, identified by an absolute IRI</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr><td>6</td><td>STANDALONE&#8209;TRO</td><td>A TRO declaration with the structure the TRACE Specification requires, whose references resolve within it</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td><em>7</em></td><td><em>LINKABLE&#8209;TRO</em></td><td><em>A TRO declaration whose element identifiers cannot collide with another TRO's</em></td><td><em>not&nbsp;claimed</em></td></tr>
</tbody>
</table>

## Expectation Findings by Tier

<table>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;1&nbsp;—&nbsp;SAFE&#8209;JSON&nbsp;&nbsp;✅&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td nowrap><samp>utf8-encoded</samp></td><td>The candidate is UTF-8</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>json-parses</samp></td><td>The candidate parses as JSON without errors</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>duplicate-member-names-absent</samp></td><td>No object repeats a member name</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>lone-surrogates-absent</samp></td><td>No string or member name has an unpaired surrogate</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>numbers-within-range</samp></td><td>Every number fits a double; every integer is exact</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;2&nbsp;—&nbsp;SAFE&#8209;JSON&#8209;LD&nbsp;&nbsp;✅&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td nowrap><samp>context-well-formed</samp></td><td>The root <code>@context</code>, if any, has a form JSON-LD allows</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>graph-well-formed</samp></td><td>The root <code>@graph</code>, if any, holds objects, not bare values</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>ids-and-types-strings</samp></td><td>Every <code>@id</code> is a string; every <code>@type</code> a string or an array of strings</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>context-at-root-only</samp></td><td>The document's only <code>@context</code> is the one at its root: no node below it and no term definition within it carries another</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>containers-absent</samp></td><td>No <code>@container</code> in a term definition</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>vocab-absent</samp></td><td>No <code>@vocab</code> in a context</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>context-protection-absent</samp></td><td>No <code>@protected</code>, <code>@propagate</code> or <code>@import</code> in a context</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>id-coercion-absent</samp></td><td>No <code>"@type": "@id"</code> in a term definition</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>graph-at-root-only</samp></td><td><code>@graph</code> appears only at the root</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>id-segments-portable</samp></td><td>Every segment of a relative <code>@id</code> is a portable name: letters, digits, dots, hyphens and underscores, beginning and ending with a letter or digit</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;3&nbsp;—&nbsp;TRACE&#8209;JSON&#8209;LD&nbsp;&nbsp;✅&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td nowrap><samp>root-context-and-graph-only</samp></td><td>A JSON object with an <code>@context</code>, an <code>@graph</code>, and nothing else</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>disallowed-node-keywords-absent</samp></td><td>No keyword outside the <code>@context</code> other than <code>@context</code>, <code>@graph</code>, <code>@id</code> and <code>@type</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>disallowed-context-keywords-absent</samp></td><td>No member of an <code>@context</code> is a keyword other than <code>@base</code>; what a term definition holds is not a member of the <code>@context</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>base-web-scheme</samp></td><td>The <code>@base</code>, if any, uses the <code>https</code> or <code>http</code> scheme</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>base-simple-url</samp></td><td>The <code>@base</code>, if any, is a simple URL: a host, no user info, dot segments, query or fragment, only URL characters, and a final <code>/</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>prefix-namespaces-terminated</samp></td><td>Every prefix maps to an absolute IRI ending in <code>#</code> or <code>/</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>context-local</samp></td><td>The <code>@context</code> is inline: no string names a remote context</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>context-aliases-absent</samp></td><td>No term definition aliases a property; a term definition holds only a <code>@type</code> naming a datatype</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>types-prefixed-or-absolute</samp></td><td>Every <code>@type</code> value is a prefixed or absolute IRI, never a bare name</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;4&nbsp;—&nbsp;USES&#8209;TROV&#8209;CORRECTLY&nbsp;&nbsp;❌&nbsp;not&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td nowrap><samp>core-prefixes-pinned</samp></td><td><code>trov</code> is declared and is the only prefix for a TROV namespace; <code>rdf</code>, <code>rdfs</code> and <code>schema</code> prefixes, if declared, are the standard ones</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>trov-terms-known</samp></td><td>Every <code>trov:</code> name is one TROV defines</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>trov-version-known</samp></td><td>The TRO declares, in <code>trov:vocabularyVersion</code>, a TROV version this checker knows: <code>0.1</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>hash-algorithms-permitted</samp></td><td>Every hash names an algorithm TRACE permits: a collision-resistant digest from the SHA-2, SHA-3 or BLAKE families</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>hash-values-correct-form</samp></td><td>Every hash value is lowercase hexadecimal of the length its algorithm produces</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr><td nowrap><samp>mime-types-two-part</samp></td><td>Every artifact's <code>trov:mimeType</code> is a string of the form <code>type/subtype</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>times-iso-8601</samp></td><td>Every <code>trov:startedAtTime</code> and <code>trov:endedAtTime</code> is an ISO 8601 date-time; every <code>schema:dateCreated</code> an ISO 8601 date or date-time</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>times-zoned</samp></td><td>Every <code>trov:startedAtTime</code> and <code>trov:endedAtTime</code> carries its time zone</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr><td nowrap><samp>tro-name-description-text</samp></td><td>The TRO's <code>schema:name</code> and <code>schema:description</code>, if present, are Text: a string or an array of strings</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>creators-person-or-organization</samp></td><td>The TRO's <code>schema:creator</code>, if present, is a node typed <code>schema:Person</code> or <code>schema:Organization</code>, never a string</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>trov-capabilities-predefined</samp></td><td>A capability's <code>trov:</code> type is one TROV predefines</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>trov-performance-attributes-predefined</samp></td><td>A performance attribute's <code>trov:</code> type is one TROV predefines</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>trov-tro-attributes-predefined</samp></td><td>A TRO attribute's <code>trov:</code> type is one TROV predefines</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>custom-terms-not-trov</samp></td><td>Every <code>trov:customTerm</code> entry declares a term outside the TROV namespace</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>custom-term-superclasses-extensible</samp></td><td>Every custom term extends <code>trov:TRSCapabilityType</code> or <code>trov:TRPAttributeType</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>trov-signing-mechanisms-predefined</samp></td><td>A signing mechanism is identified by reference, and a <code>trov:</code> one is one TROV predefines</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;5&nbsp;—&nbsp;DEFINES&#8209;TRS&nbsp;&nbsp;❌&nbsp;not&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td nowrap><samp>trs-defined</samp></td><td>A TRS is defined, with an <code>@id</code>, at the top of the <code>@graph</code> or as the object of <code>trov:wasAssembledBy</code>, and nowhere else</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>trs-id-absolute</samp></td><td>The TRS is identified by an absolute IRI, or a compact IRI outside the <code>trov</code> namespace</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr><td nowrap><samp>capability-ids-absolute</samp></td><td>Every capability is identified by an absolute IRI, or a compact IRI outside the <code>trov</code> namespace</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr><td nowrap><samp>capability-warrants-absolute</samp></td><td>Every performance attribute refers to the capability warranting it by absolute IRI</td><td>❌&nbsp;not&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;6&nbsp;—&nbsp;STANDALONE&#8209;TRO&nbsp;&nbsp;❌&nbsp;not&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td nowrap><samp>tro-top-level-in-graph</samp></td><td>The TRO is a top-level member of the <code>@graph</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>tro-assembled-by-trs</samp></td><td>The TRO names its assembling system, typed as a TRS</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>composition-has-fingerprint</samp></td><td>The TRO's composition, if any, carries one fingerprint, which carries one hash</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>composition-identifies-artifacts</samp></td><td>The TRO's composition, if any, names at least one artifact in a <code>trov:hasArtifact</code> array</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>artifact-hashes-present</samp></td><td>Every artifact in the composition carries a <code>trov:hash</code>, one hash or an array of at least one</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><samp>gpg-signing-key-present</samp></td><td>A TRO signed with <code>trov:GPGSigning</code> gives its TRS a <code>trov:publicKey</code></td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><th colspan="3" align="left"><br><em>Tier&nbsp;7&nbsp;—&nbsp;LINKABLE&#8209;TRO&nbsp;&nbsp;not&nbsp;claimed</em></th></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><samp>base-declared</samp></em></td><td><em>The <code>@context</code> includes an <code>@base</code></em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><samp>base-has-path</samp></em></td><td><em>The <code>@base</code> names something below the host, not the host alone</em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><samp>base-host-lowercase</samp></em></td><td><em>The <code>@base</code> host is lowercase</em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><samp>base-host-ownable</samp></em></td><td><em>The <code>@base</code> host is a domain name the minter could hold, not a reserved or documentation name</em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><samp>node-ids-present</samp></em></td><td><em>Every node carries an explicit <code>@id</code></em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><samp>blank-node-ids-absent</samp></em></td><td><em>No <code>@id</code> is a blank node identifier</em></td><td><em>not&nbsp;claimed</em></td></tr>
</tbody>
</table>

## Diagnostics for Each Unmet Expectation

### Unmet expectation: hash-values-correct-form

Expectation details: Every trov:hash on the TRO's artifacts and composition fingerprint carries its value in trov:hashValue as its algorithm writes one: lowercase hexadecimal digits, 64 of them for sha256, sha3-256, blake2s and blake3; 96 for sha384 and sha3-384; 128 for sha512, sha3-512 and blake2b.

<table>
<thead>
<tr><th align="left">Found</th><th align="left">Expectation not met because</th></tr>
</thead>
<tbody>
<tr><td nowrap><samp>"aaa1..."</samp></td><td>a sha256 value is 64 lowercase hexadecimal digits</td></tr>
<tr><td colspan="2">Where: <samp>/<wbr>@graph/<wbr>0/<wbr>trov:hasComposition/<wbr>trov:hasArtifact/<wbr>0/<wbr>trov:hash/<wbr>trov:hashValue</samp></td></tr>
</tbody>
<tbody>
<tr><td nowrap><samp>"bbb2..."</samp></td><td>a sha256 value is 64 lowercase hexadecimal digits</td></tr>
<tr><td colspan="2">Where: <samp>/<wbr>@graph/<wbr>0/<wbr>trov:hasComposition/<wbr>trov:hasArtifact/<wbr>1/<wbr>trov:hash/<wbr>trov:hashValue</samp></td></tr>
</tbody>
<tbody>
<tr><td nowrap><samp>"ccc3..."</samp></td><td>a sha256 value is 64 lowercase hexadecimal digits</td></tr>
<tr><td colspan="2">Where: <samp>/<wbr>@graph/<wbr>0/<wbr>trov:hasComposition/<wbr>trov:hasArtifact/<wbr>2/<wbr>trov:hash/<wbr>trov:hashValue</samp></td></tr>
</tbody>
<tbody>
<tr><td nowrap><samp>"a1b2c3d4..."</samp></td><td>a sha256 value is 64 lowercase hexadecimal digits</td></tr>
<tr><td colspan="2">Where: <samp>/<wbr>@graph/<wbr>0/<wbr>trov:hasComposition/<wbr>trov:hasFingerprint/<wbr>trov:hash/<wbr>trov:hashValue</samp></td></tr>
</tbody>
</table>

### Unmet expectation: times-zoned

Expectation details: Every trov:startedAtTime and trov:endedAtTime carries its time zone: Z, or an offset of the form +hh:mm or -hh:mm.

<table>
<thead>
<tr><th align="left">Found</th><th align="left">Expectation not met because</th></tr>
</thead>
<tbody>
<tr><td nowrap><samp>"2024-06-15T14:25:00"</samp></td><td>a time carries its zone: Z, or an offset +hh:mm or -hh:mm</td></tr>
<tr><td colspan="2">Where: <samp>/<wbr>@graph/<wbr>0/<wbr>trov:hasPerformance/<wbr>0/<wbr>trov:endedAtTime</samp></td></tr>
</tbody>
<tbody>
<tr><td nowrap><samp>"2024-06-15T14:00:00"</samp></td><td>a time carries its zone: Z, or an offset +hh:mm or -hh:mm</td></tr>
<tr><td colspan="2">Where: <samp>/<wbr>@graph/<wbr>0/<wbr>trov:hasPerformance/<wbr>0/<wbr>trov:startedAtTime</samp></td></tr>
</tbody>
</table>

### Unmet expectation: trs-id-absolute

Expectation details: The @id of the TRS the document defines is an absolute IRI, or a compact IRI whose prefix is not trov, so that it is the same wherever the TRS is defined.

<table>
<thead>
<tr><th align="left">Found</th><th align="left">Expectation not met because</th></tr>
</thead>
<tbody>
<tr><td nowrap><samp>"trs"</samp></td><td>"trs" is not an absolute IRI; a TRS is identified by an absolute IRI, or by a compact IRI outside the trov namespace</td></tr>
<tr><td colspan="2">Where: <samp>/<wbr>@graph/<wbr>0/<wbr>trov:wasAssembledBy/<wbr>@id</samp></td></tr>
</tbody>
</table>

### Unmet expectation: capability-ids-absolute

Expectation details: Every value of trov:hasCapability that carries an @id carries an absolute IRI, or a compact IRI whose prefix is not trov.

<table>
<thead>
<tr><th align="left">Found</th><th align="left">Expectation not met because</th></tr>
</thead>
<tbody>
<tr><td nowrap><samp>"trs/capability/0"</samp></td><td>"trs/capability/0" is not an absolute IRI; a capability is identified by an absolute IRI, or by a compact IRI outside the trov namespace</td></tr>
<tr><td colspan="2">Where: <samp>/<wbr>@graph/<wbr>0/<wbr>trov:wasAssembledBy/<wbr>trov:hasCapability/<wbr>0/<wbr>@id</samp></td></tr>
</tbody>
</table>

### Unmet expectation: capability-warrants-absolute

Expectation details: Every trov:warrantedBy on a value of trov:hasPerformanceAttribute refers to its capability by an absolute IRI, or a compact IRI whose prefix is not trov.

<table>
<thead>
<tr><th align="left">Found</th><th align="left">Expectation not met because</th></tr>
</thead>
<tbody>
<tr><td nowrap><samp>"trs/capability/0"</samp></td><td>"trs/capability/0" is not an absolute IRI; a performance attribute's warrant refers to its capability by the capability's absolute IRI</td></tr>
<tr><td colspan="2">Where: <samp>/<wbr>@graph/<wbr>0/<wbr>trov:hasPerformance/<wbr>0/<wbr>trov:hasPerformanceAttribute/<wbr>0/<wbr>trov:warrantedBy/<wbr>@id</samp></td></tr>
</tbody>
</table>
