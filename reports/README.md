# Reports

One report for each target of each candidate.

## `01-spec-example-2026-04-08`

Created with: `tro-utils 0.2.2`

The specification's [Complete Example](https://transparency-certified.github.io/trace-specification/docs/tro-declaration-format#complete-example), copied verbatim on 2026-09-03 from the 2026-04-08 revision. Its four `trov:hashValue` fields carry elided placeholders (`a1b2c3d4...`, `aaa1...`) and its `@context` declares no `@base`.

This candidate is expected to satisfy `Tier 6 - STANDALONE-TRO` at version `trace-2026-04-19`.

<table>
<thead>
<tr><th align="left">Target version</th><th align="left">Target tier</th><th align="left">Tier Status</th><th align="left">Expectation Status</th><th align="left">Report</th></tr>
</thead>
<tbody>
<tr><td><samp>trace&#8209;2026&#8209;04&#8209;19</samp></td><td><samp>Tier&nbsp;6&nbsp;&#8209;&nbsp;STANDALONE&#8209;TRO</samp></td><td>❌&nbsp;not&nbsp;met</td><td><a href="01-spec-example-2026-04-08__at__trace-2026-04-19__to__tier-6.md#diagnostics">❌ 1 unmet</a></td><td><a href="01-spec-example-2026-04-08__at__trace-2026-04-19__to__tier-6.md">01-spec-example-2026-04-08__at__trace-2026-04-19__to__tier-6.md</a></td></tr>
</tbody>
</table>

## `02-spec-example-2026-04-08-with-base-and-hashes`

Created with: `tro-utils 0.2.2`

The 2026-04-08 example with an `@base` in its `@context` and a sha256 value in each of the four hash fields. Every value is computed from the artifact's own `@id` for reproducibility's sake only.

This candidate is expected to satisfy `Tier 6 - STANDALONE-TRO` at version `trace-2026-04-19`, and `Tier 6 - STANDALONE-TRO` at version `trace-main`.

<table>
<thead>
<tr><th align="left">Target version</th><th align="left">Target tier</th><th align="left">Tier Status</th><th align="left">Expectation Status</th><th align="left">Report</th></tr>
</thead>
<tbody>
<tr><td><samp>trace&#8209;2026&#8209;04&#8209;19</samp></td><td><samp>Tier&nbsp;6&nbsp;&#8209;&nbsp;STANDALONE&#8209;TRO</samp></td><td>✅&nbsp;met</td><td>✅&nbsp;all&nbsp;met</td><td><a href="02-spec-example-2026-04-08-with-base-and-hashes__at__trace-2026-04-19__to__tier-6.md">02-spec-example-2026-04-08-with-base-and-hashes__at__trace-2026-04-19__to__tier-6.md</a></td></tr>
<tr><td><samp>trace&#8209;main</samp></td><td><samp>Tier&nbsp;6&nbsp;&#8209;&nbsp;STANDALONE&#8209;TRO</samp></td><td>❌&nbsp;not&nbsp;met</td><td><a href="02-spec-example-2026-04-08-with-base-and-hashes__at__trace-main__to__tier-6.md#diagnostics">❌ 3 unmet</a></td><td><a href="02-spec-example-2026-04-08-with-base-and-hashes__at__trace-main__to__tier-6.md">02-spec-example-2026-04-08-with-base-and-hashes__at__trace-main__to__tier-6.md</a></td></tr>
</tbody>
</table>

## `03-spec-example-2026-04-08-with-node-ids`

Created with: `tro-utils 0.2.2`

The preceding candidate with an `@id` on each of its five remaining bare node objects, `trov:createdWith` and the four `trov:hash` nodes, and a time zone, `Z`, on each of its three times.

This candidate is expected to satisfy `Tier 7 - LINKABLE-TRO` at version `trace-2026-04-19`, and `Tier 7 - LINKABLE-TRO` at version `trace-main`.

<table>
<thead>
<tr><th align="left">Target version</th><th align="left">Target tier</th><th align="left">Tier Status</th><th align="left">Expectation Status</th><th align="left">Report</th></tr>
</thead>
<tbody>
<tr><td><samp>trace&#8209;2026&#8209;04&#8209;19</samp></td><td><samp>Tier&nbsp;7&nbsp;&#8209;&nbsp;LINKABLE&#8209;TRO</samp></td><td>✅&nbsp;met</td><td>✅&nbsp;all&nbsp;met</td><td><a href="03-spec-example-2026-04-08-with-node-ids__at__trace-2026-04-19__to__tier-7.md">03-spec-example-2026-04-08-with-node-ids__at__trace-2026-04-19__to__tier-7.md</a></td></tr>
<tr><td><samp>trace&#8209;main</samp></td><td><samp>Tier&nbsp;7&nbsp;&#8209;&nbsp;LINKABLE&#8209;TRO</samp></td><td>❌&nbsp;not&nbsp;met</td><td><a href="03-spec-example-2026-04-08-with-node-ids__at__trace-main__to__tier-7.md#diagnostics">❌ 2 unmet</a></td><td><a href="03-spec-example-2026-04-08-with-node-ids__at__trace-main__to__tier-7.md">03-spec-example-2026-04-08-with-node-ids__at__trace-main__to__tier-7.md</a></td></tr>
</tbody>
</table>
