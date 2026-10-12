# Detection Rules

Sigma detection rules I write and test, focused on Windows environments and mapped to **MITRE ATT&CK**.

## What is Sigma?

[Sigma](https://github.com/SigmaHQ/sigma) is an open, generic signature format for SIEM systems — write once, convert to Splunk, Elastic, Sentinel, and more. Contributing rules here is one of the most practical ways to learn defensive detection.

## Structure

```
rules/
└── windows/
    └── proc_creation_win_lsass_procdump.yml
```

## Testing a rule

1. Validate syntax with the [Sigma CLI](https://github.com/SigmaHQ/sigma-cli) or [uncoder.io](https://uncoder.io)
2. Convert to your SIEM's query language and run against test logs
3. Tune `level` and `falsepositives` based on what you observe — a rule is only done after it survives real data

## Rules

| Rule | MITRE ATT&CK | Level | Status |
|------|--------------|-------|--------|
| [Potential LSASS Credential Dumping via ProcDump](rules/windows/proc_creation_win_lsass_procdump.yml) | T1003.001 | high | test |

## Contributing

Issues and improvements welcome. If you use these rules, test them in your own environment first — detection logic always needs local tuning.
