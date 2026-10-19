# Contributing

Small repo, simple rules.

## Adding a rule

- Filename: `proc_creation_win_<short-name>.yml` (or the right log-source prefix) -- look at the existing rules first and match the pattern.
- Required fields: `title`, `id` (uuid4), `status`, `description`, `author`, `date`, `logsource`, `detection`, `falsepositives`, `level`, plus MITRE tags (`attack.tactic`, `attack.tXXXX.XXX`) following the current Sigma spec.
- `status: test` unless you have run it against real logs. Do not mark `stable` on syntax validation alone.

## Before you submit

- Make sure the YAML parses and the detection block is well-formed.
- Document known false positives in the `falsepositives` field -- do not leave it empty.
- One rule per PR. Keep the description short: what it detects, how you tested it.

That is it. If a rule is wrong, I would rather hear it than merge it.
