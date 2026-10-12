# Detection Rules

Sigma rules I'm writing while learning detection engineering. Windows-focused, mapped to MITRE ATT&CK.

## Rules

| Rule | ATT&CK | Level |
|------|--------|-------|
| [LSASS credential dumping via ProcDump](rules/windows/proc_creation_win_lsass_procdump.yml) | T1003.001 | high |

## Notes

- `status: test` means what it says — syntax validated, not yet tested against real logs.
- Detection logic always needs tuning to the environment. Don't deploy blind.
