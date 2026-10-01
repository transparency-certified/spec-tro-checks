# Reports

One report for each target of each candidate.

## `spec-example-2026-04-08`

The specification's [Complete Example](https://transparency-certified.github.io/trace-specification/docs/tro-declaration-format#complete-example), copied verbatim on 2026-09-03 from the 2026-04-08 revision. Its four `trov:hashValue` fields carry elided placeholders (`a1b2c3d4...`, `aaa1...`) and its `@context` declares no `@base`.

<table>
<thead>
<tr><th align="left">Target version</th><th align="left">Target tier</th><th align="left">Status</th><th align="left">Report</th></tr>
</thead>
<tbody>
<tr><td>trace&#8209;spec&#8209;2026&#8209;04&#8209;19</td><td>6&nbsp;STANDALONE&#8209;TRO</td><td>❌&nbsp;not&nbsp;met</td><td><a href="spec-example-2026-04-08_trace-spec-2026-04-19_tier-6.md">spec-example-2026-04-08_trace-spec-2026-04-19_tier-6.md</a></td></tr>
</tbody>
</table>

## `spec-example-2026-04-08-with-base-and-hashes`

The 2026-04-08 example with an `@base` in its `@context` and a sha256 value in each of the four hash fields. Every value is computed from the artifact's own `@id` for reproducibility's sake only.

<table>
<thead>
<tr><th align="left">Target version</th><th align="left">Target tier</th><th align="left">Status</th><th align="left">Report</th></tr>
</thead>
<tbody>
<tr><td>trace&#8209;spec&#8209;2026&#8209;04&#8209;19</td><td>6&nbsp;STANDALONE&#8209;TRO</td><td>❌&nbsp;not&nbsp;met</td><td><a href="spec-example-2026-04-08-with-base-and-hashes_trace-spec-2026-04-19_tier-6.md">spec-example-2026-04-08-with-base-and-hashes_trace-spec-2026-04-19_tier-6.md</a></td></tr>
</tbody>
</table>

## `spec-example-2026-04-08-with-node-ids`

The preceding candidate with an `@id` on each of its five remaining bare node objects, `trov:createdWith` and the four `trov:hash` nodes, and a time zone, `Z`, on each of its three times.

<table>
<thead>
<tr><th align="left">Target version</th><th align="left">Target tier</th><th align="left">Status</th><th align="left">Report</th></tr>
</thead>
<tbody>
<tr><td>trace&#8209;spec&#8209;2026&#8209;04&#8209;19</td><td>7&nbsp;LINKABLE&#8209;TRO</td><td>❌&nbsp;not&nbsp;met</td><td><a href="spec-example-2026-04-08-with-node-ids_trace-spec-2026-04-19_tier-7.md">spec-example-2026-04-08-with-node-ids_trace-spec-2026-04-19_tier-7.md</a></td></tr>
</tbody>
</table>
