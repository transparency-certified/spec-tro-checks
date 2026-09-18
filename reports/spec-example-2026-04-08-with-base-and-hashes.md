# Report

## Candidate Information

<table>
<tbody>
<tr><td>Candidate</td><td nowrap><code>spec-example-2026-04-08-with-base-and-hashes.jsonld</code></td></tr>
<tr><td>Description</td><td>The 2026-04-08 example with an <code>@base</code> in its <code>@context</code> and a sha256 value in each of the four hash fields. Every value is computed from the artifact's own <code>@id</code> for reproducibility's sake only.</td></tr>
<tr><td>Target</td><td>4&nbsp;STANDALONE&#8209;TRO</td></tr>
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
<tr><td>4</td><td>STANDALONE&#8209;TRO</td><td>A TRO declaration with the structure the TRACE Specification requires, whose references resolve within it</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td><em>5</em></td><td><em>LINKABLE&#8209;TRO</em></td><td><em>A TRO declaration whose element identifiers cannot collide with another TRO's</em></td><td><em>not&nbsp;claimed</em></td></tr>
</tbody>
</table>

## Expectation Findings by Tier

<table>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;1&nbsp;—&nbsp;SAFE&#8209;JSON&nbsp;&nbsp;✅&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td nowrap><code>duplicate-member-names-absent</code></td><td>No object repeats a member name</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>json-parses</code></td><td>The candidate parses as JSON without errors</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>lone-surrogates-absent</code></td><td>No string or member name has an unpaired surrogate</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>numbers-within-range</code></td><td>Every number fits a double; every integer is exact</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>utf8-encoded</code></td><td>The candidate is UTF-8</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;2&nbsp;—&nbsp;SAFE&#8209;JSON&#8209;LD&nbsp;&nbsp;✅&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td nowrap><code>containers-absent</code></td><td>No <code>@container</code> in a term definition</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>context-at-root-only</code></td><td>The document's only <code>@context</code> is the one at its root: no node below it and no term definition within it carries another</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>context-protection-absent</code></td><td>No <code>@protected</code>, <code>@propagate</code> or <code>@import</code> in a context</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>context-well-formed</code></td><td>The root <code>@context</code>, if any, has a form JSON-LD allows</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>graph-at-root-only</code></td><td><code>@graph</code> appears only at the root</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>graph-well-formed</code></td><td>The root <code>@graph</code>, if any, holds objects, not bare values</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>id-coercion-absent</code></td><td>No <code>"@type": "@id"</code> in a term definition</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>id-segments-portable</code></td><td>Every segment of a relative <code>@id</code> is a portable name: letters, digits, dots, hyphens and underscores, beginning and ending with a letter or digit</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>ids-and-types-strings</code></td><td>Every <code>@id</code> is a string; every <code>@type</code> a string or an array of strings</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>vocab-absent</code></td><td>No <code>@vocab</code> in a context</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;3&nbsp;—&nbsp;TRACE&#8209;JSON&#8209;LD&nbsp;&nbsp;✅&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td nowrap><code>base-simple-url</code></td><td>The <code>@base</code>, if any, is a simple URL: a host, no user info, dot segments, query or fragment, only URL characters, and a final <code>/</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>base-web-scheme</code></td><td>The <code>@base</code>, if any, uses the <code>https</code> or <code>http</code> scheme</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>context-aliases-absent</code></td><td>No term definition aliases a property; a term definition holds only a <code>@type</code> naming a datatype</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>context-local</code></td><td>The <code>@context</code> is inline: no string names a remote context</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>disallowed-context-keywords-absent</code></td><td>No member of an <code>@context</code> is a keyword other than <code>@base</code>; what a term definition holds is not a member of the <code>@context</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>disallowed-node-keywords-absent</code></td><td>No keyword outside the <code>@context</code> other than <code>@context</code>, <code>@graph</code>, <code>@id</code> and <code>@type</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>prefix-namespaces-terminated</code></td><td>Every prefix maps to an absolute IRI ending in <code>#</code> or <code>/</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>root-context-and-graph-only</code></td><td>A JSON object with an <code>@context</code>, an <code>@graph</code>, and nothing else</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>types-prefixed-or-absolute</code></td><td>Every <code>@type</code> value is a prefixed or absolute IRI, never a bare name</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;4&nbsp;—&nbsp;STANDALONE&#8209;TRO&nbsp;&nbsp;❌&nbsp;not&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td nowrap><code>artifact-hashes-present</code></td><td>Every artifact in the composition carries a <code>trov:hash</code>, one hash or an array of at least one</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>composition-has-fingerprint</code></td><td>The TRO's composition, if any, carries one fingerprint, which carries one hash</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>composition-identifies-artifacts</code></td><td>The TRO's composition, if any, names at least one artifact in a <code>trov:hasArtifact</code> array</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>core-prefixes-pinned</code></td><td><code>trov</code> is declared and is the only prefix for a TROV namespace; <code>rdf</code>, <code>rdfs</code> and <code>schema</code> prefixes, if declared, are the standard ones</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>creators-person-or-organization</code></td><td>The TRO's <code>schema:creator</code>, if present, is a node typed <code>schema:Person</code> or <code>schema:Organization</code>, never a string</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>hash-algorithms-permitted</code></td><td>Every hash names an algorithm TRACE permits: a collision-resistant digest from the SHA-2, SHA-3 or BLAKE families</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>hash-values-correct-form</code></td><td>Every hash value is lowercase hexadecimal of the length its algorithm produces</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>mime-types-two-part</code></td><td>Every artifact's <code>trov:mimeType</code> is a string of the form <code>type/subtype</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>times-iso-8601</code></td><td>Every <code>trov:startedAtTime</code> and <code>trov:endedAtTime</code> is an ISO 8601 date-time; every <code>schema:dateCreated</code> an ISO 8601 date or date-time</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>times-zoned</code></td><td>Every <code>trov:startedAtTime</code> and <code>trov:endedAtTime</code> carries its time zone</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr><td nowrap><code>tro-assembled-by-trs</code></td><td>The TRO names its assembling system, typed as a TRS</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>tro-name-description-text</code></td><td>The TRO's <code>schema:name</code> and <code>schema:description</code>, if present, are Text: a string or an array of strings</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>tro-top-level-in-graph</code></td><td>The TRO is a top-level member of the <code>@graph</code></td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>trov-terms-known</code></td><td>Every <code>trov:</code> name is one TROV defines</td><td>✅&nbsp;met</td></tr>
<tr><td nowrap><code>trov-version-known</code></td><td>The TRO declares, in <code>trov:vocabularyVersion</code>, a TROV version this checker knows: <code>0.1</code></td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><th colspan="3" align="left"><br><em>Tier&nbsp;5&nbsp;—&nbsp;LINKABLE&#8209;TRO&nbsp;&nbsp;not&nbsp;claimed</em></th></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><code>base-declared</code></em></td><td><em>The <code>@context</code> includes an <code>@base</code></em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><code>base-has-path</code></em></td><td><em>The <code>@base</code> names something below the host, not the host alone</em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><code>base-host-lowercase</code></em></td><td><em>The <code>@base</code> host is lowercase</em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><code>base-host-ownable</code></em></td><td><em>The <code>@base</code> host is a domain name the minter could hold, not a reserved or documentation name</em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><code>blank-node-ids-absent</code></em></td><td><em>No <code>@id</code> is a blank node identifier</em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td nowrap><em><code>node-ids-present</code></em></td><td><em>Every node carries an explicit <code>@id</code></em></td><td><em>not&nbsp;claimed</em></td></tr>
</tbody>
</table>

## Diagnostics for Each Unmet Expectation

### Unmet expectation: times-zoned

Expectation details: Every trov:startedAtTime and trov:endedAtTime carries its time zone: Z, or an offset of the form +hh:mm or -hh:mm.

<table>
<thead>
<tr><th align="left">Found</th><th align="left">Where</th><th align="left">Expectation not met because</th></tr>
</thead>
<tbody>
<tr><td nowrap><code>"2024-06-15T14:25:00"</code></td><td nowrap><code>/@graph/0/trov:hasPerformance/0/trov:endedAtTime</code></td><td>a time carries its zone: Z, or an offset +hh:mm or -hh:mm</td></tr>
<tr><td nowrap><code>"2024-06-15T14:00:00"</code></td><td nowrap><code>/@graph/0/trov:hasPerformance/0/trov:startedAtTime</code></td><td>a time carries its zone: Z, or an offset +hh:mm or -hh:mm</td></tr>
</tbody>
</table>
