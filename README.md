# Detection Rules

Sigma rules I am writing while learning detection engineering. Windows-focused, mapped to MITRE ATT&CK.

## Rules

| Rule | Technique | Severity | Added |
|------|-----------|----------|-------|
| [LSASS credential dumping via ProcDump](rules/windows/proc_creation_win_lsass_procdump.yml) | [T1003.001](https://attack.mitre.org/techniques/T1003/001/) | High | 2026-10-12 |
| [PowerShell encoded-command execution](rules/windows/proc_creation_win_powershell_encoded.yml) | [T1059.001](https://attack.mitre.org/techniques/T1059/001/) | Medium | 2026-10-13 |

## What status test means

The rules are validated for syntax and structure, not yet tested against production logs. Detection logic always needs tuning to the environment.

## Using the rules

Drop the YAML files into your Sigma converter and convert to your backend:

```
sigma convert -t splunk rules/windows/proc_creation_win_lsass_procdump.yml
```

## Notes

- Every rule is tagged to MITRE ATT&CK using the current Sigma spec.
- False positives are documented in each rule falsepositives field.
