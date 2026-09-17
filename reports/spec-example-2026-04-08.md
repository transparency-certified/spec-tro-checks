# Report

## Candidate Information

<table>
<tbody>
<tr><td>Candidate</td><td><code>spec-example-2026-04-08.jsonld</code></td></tr>
<tr><td>Description</td><td>The specification's <a href="https://transparency-certified.github.io/trace-specification/docs/tro-declaration-format#complete-example">Complete Example</a>, copied verbatim on 2026-09-03 from the 2026-04-08 revision. Its four <code>trov:hashValue</code> fields carry elided placeholders (<code>a1b2c3d4...</code>, <code>aaa1...</code>) and its <code>@context</code> declares no <code>@base</code>.</td></tr>
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
<tr><td>3</td><td>TRACE&#8209;JSON&#8209;LD</td><td>JSON-LD in the restricted form the TRACE Specification defines for TRO declarations</td><td>✅&nbsp;met</td></tr>
<tr><td>4</td><td>STANDALONE&#8209;TRO</td><td>A TRO declaration with the structure the TRACE Specification requires, whose references resolve within it</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td><em>5</em></td><td><em>LINKABLE&#8209;TRO</em></td><td><em>A TRO declaration whose element identifiers cannot collide with another TRO's</em></td><td><em>not&nbsp;claimed</em></td></tr>
</tbody>
</table>

## Expectation Findings by Tier

<table>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;1&nbsp;—&nbsp;SAFE&#8209;JSON&nbsp;&nbsp;✅&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td>duplicate-member-names-absent</td><td>No object repeats a member name</td><td>✅&nbsp;met</td></tr>
<tr><td>json-parses</td><td>The candidate parses as JSON without errors</td><td>✅&nbsp;met</td></tr>
<tr><td>lone-surrogates-absent</td><td>No string or member name has an unpaired surrogate</td><td>✅&nbsp;met</td></tr>
<tr><td>numbers-within-range</td><td>Every number fits a double; every integer is exact</td><td>✅&nbsp;met</td></tr>
<tr><td>utf8-encoded</td><td>The candidate is UTF-8</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;2&nbsp;—&nbsp;SAFE&#8209;JSON&#8209;LD&nbsp;&nbsp;✅&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td>containers-absent</td><td>No <code>@container</code> in a term definition</td><td>✅&nbsp;met</td></tr>
<tr><td>context-at-root-only</td><td>The document's only <code>@context</code> is the one at its root: no node below it and no term definition within it carries another</td><td>✅&nbsp;met</td></tr>
<tr><td>context-protection-absent</td><td>No <code>@protected</code>, <code>@propagate</code> or <code>@import</code> in a context</td><td>✅&nbsp;met</td></tr>
<tr><td>context-well-formed</td><td>The root <code>@context</code>, if any, has a form JSON-LD allows</td><td>✅&nbsp;met</td></tr>
<tr><td>graph-at-root-only</td><td><code>@graph</code> appears only at the root</td><td>✅&nbsp;met</td></tr>
<tr><td>graph-well-formed</td><td>The root <code>@graph</code>, if any, holds objects, not bare values</td><td>✅&nbsp;met</td></tr>
<tr><td>id-coercion-absent</td><td>No <code>"@type": "@id"</code> in a term definition</td><td>✅&nbsp;met</td></tr>
<tr><td>ids-and-types-strings</td><td>Every <code>@id</code> is a string; every <code>@type</code> a string or an array of strings</td><td>✅&nbsp;met</td></tr>
<tr><td>relative-ids-plain</td><td>Every relative <code>@id</code> is a plain path, with no leading <code>/</code> or <code>@</code>, no <code>.</code> or <code>..</code> segments, and no <code>?</code> or <code>#</code></td><td>✅&nbsp;met</td></tr>
<tr><td>vocab-absent</td><td>No <code>@vocab</code> in a context</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;3&nbsp;—&nbsp;TRACE&#8209;JSON&#8209;LD&nbsp;&nbsp;✅&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td>base-simple-url</td><td>The <code>@base</code>, if any, is a simple URL: a host, no user info, dot segments, query or fragment, only URL characters, and a final <code>/</code></td><td>✅&nbsp;met</td></tr>
<tr><td>base-web-scheme</td><td>The <code>@base</code>, if any, uses the <code>https</code> or <code>http</code> scheme</td><td>✅&nbsp;met</td></tr>
<tr><td>context-aliases-absent</td><td>No term definition aliases a property; a term definition holds only a <code>@type</code> naming a datatype</td><td>✅&nbsp;met</td></tr>
<tr><td>context-local</td><td>The <code>@context</code> is inline: no string names a remote context</td><td>✅&nbsp;met</td></tr>
<tr><td>disallowed-context-keywords-absent</td><td>No member of an <code>@context</code> is a keyword other than <code>@base</code>; what a term definition holds is not a member of the <code>@context</code></td><td>✅&nbsp;met</td></tr>
<tr><td>disallowed-node-keywords-absent</td><td>No keyword outside the <code>@context</code> other than <code>@context</code>, <code>@graph</code>, <code>@id</code> and <code>@type</code></td><td>✅&nbsp;met</td></tr>
<tr><td>prefix-namespaces-terminated</td><td>Every prefix maps to an absolute IRI ending in <code>#</code> or <code>/</code></td><td>✅&nbsp;met</td></tr>
<tr><td>root-context-and-graph-only</td><td>A JSON object with an <code>@context</code>, an <code>@graph</code>, and nothing else</td><td>✅&nbsp;met</td></tr>
<tr><td>types-prefixed-or-absolute</td><td>Every <code>@type</code> value is a prefixed or absolute IRI, never a bare name</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr><th colspan="3" align="left"><br>Tier&nbsp;4&nbsp;—&nbsp;STANDALONE&#8209;TRO&nbsp;&nbsp;❌&nbsp;not&nbsp;met</th></tr>
<tr><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr><td>composition-fingerprinted</td><td>The TRO's composition, if any, carries a fingerprint</td><td>✅&nbsp;met</td></tr>
<tr><td>core-prefixes-pinned</td><td><code>trov</code> is declared and is the only prefix for a TROV namespace; <code>rdf</code>, <code>rdfs</code> and <code>schema</code> prefixes, if declared, are the standard ones</td><td>✅&nbsp;met</td></tr>
<tr><td>hashes-well-formed</td><td>The TRO's artifact and fingerprint hashes are well-formed sha256</td><td>❌&nbsp;not&nbsp;met</td></tr>
<tr><td>tro-assembled-by-trs</td><td>The TRO names its assembling system, typed as a TRS</td><td>✅&nbsp;met</td></tr>
<tr><td>tro-top-level-in-graph</td><td>The TRO is a top-level member of the <code>@graph</code></td><td>✅&nbsp;met</td></tr>
<tr><td>trov-terms-known</td><td>Every <code>trov:</code> name is one TROV defines</td><td>✅&nbsp;met</td></tr>
</tbody>
<tbody>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><th colspan="3" align="left"><br><em>Tier&nbsp;5&nbsp;—&nbsp;LINKABLE&#8209;TRO&nbsp;&nbsp;not&nbsp;claimed</em></th></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><th align="left">Expectation</th><th align="left">Summary</th><th align="left">Status</th></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td><em>base-declared</em></td><td><em>The <code>@context</code> includes an <code>@base</code></em></td><td><em>not&nbsp;claimed</em></td></tr>
<tr style="color: var(--vscode-descriptionForeground, #767676)"><td><em>node-ids-present</em></td><td><em>Every node carries an explicit <code>@id</code></em></td><td><em>not&nbsp;claimed</em></td></tr>
</tbody>
</table>

## Details

### Unmet expectation: hashes-well-formed

Expectation details: Each trov:hash on the TRO's artifacts and composition fingerprint names sha256 as its algorithm and carries a value of 64 lowercase hexadecimal digits.

<table>
<thead>
<tr><th align="left">Found</th><th align="left">Where</th><th align="left">Expectation not met because</th></tr>
</thead>
<tbody>
<tr><td><code>"aaa1..."</code></td><td><code>/@graph/0/trov:hasComposition/trov:hasArtifact/0/trov:hash/trov:hashValue</code></td><td>a sha256 value is 64 lowercase hexadecimal digits</td></tr>
<tr><td><code>"bbb2..."</code></td><td><code>/@graph/0/trov:hasComposition/trov:hasArtifact/1/trov:hash/trov:hashValue</code></td><td>a sha256 value is 64 lowercase hexadecimal digits</td></tr>
<tr><td><code>"ccc3..."</code></td><td><code>/@graph/0/trov:hasComposition/trov:hasArtifact/2/trov:hash/trov:hashValue</code></td><td>a sha256 value is 64 lowercase hexadecimal digits</td></tr>
<tr><td><code>"a1b2c3d4..."</code></td><td><code>/@graph/0/trov:hasComposition/trov:hasFingerprint/trov:hash/trov:hashValue</code></td><td>a sha256 value is 64 lowercase hexadecimal digits</td></tr>
</tbody>
</table>
