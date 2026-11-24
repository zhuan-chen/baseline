# Commit message

Commit messages have a subject, an optional body, and optional trailers.

When referencing a commit hash, use its 7-character prefix when that is
unambiguous in the repository; otherwise, lengthen it until it is unambiguous.

## Subject

Use the `<subsystem>: <description>` form, with a 50-character maximum including
the prefix and no trailing period.

`<subsystem>` is the code area touched and keeps `git log` skimmable by area.
Use the deepest directory that contains every file in the change, and omit the
`<subsystem>` prefix when that path is empty (i.e., the repository root).

`<description>` names the change in imperative mood. It starts with a lowercase
imperative verb unless a proper noun, path, or API name requires capitalization.

## Body

Write a body when the subject alone does not provide enough context about the
change. Separate it from the subject with a blank line.

Body lines wrap at 72 columns. Pack words up to that limit, and break to the
next line only when the next word would overflow.

The diff already shows every file, line, and expression. The body earns its
space by carrying context the diff cannot:

- The conceptual "what", not a file-by-file recap.
- The "why": motivation, trade-offs, or constraints that drove the choice.
- Non-obvious decisions or consequences.

Skip mechanical details already visible in the diff. Keep code-level "how" in
comments next to the code it describes. Keep process detail in issues or pull
requests.

## Trailers

Trailers attach machine-readable metadata, such as issue links and revert
markers. Put the trailers after the body, or after the subject when there is no
body. A blank line comes before the trailers. The trailers then sit on
consecutive lines.

A trailer is one `key: value` line. Do not wrap, even if it exceeds 72 columns.

- `Fixes: #123` closes an issue on merge.
- `Refs: #456` references an issue without closing it.
- `Reverts: 1a2b3c4` names the commit this change reverts.
