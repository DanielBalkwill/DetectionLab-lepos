# Detection library

One folder per ATT&CK tactic. Each detection is two files:

- `T<id>-<name>.md` — the writeup (hypothesis, logic, validation, FP analysis, tuning, response)
- `<name>.yml` — the portable **Sigma** rule (validated in CI)

Start from [`_TEMPLATE.md`](_TEMPLATE.md) for the writeup.

## Tactics

- `credential-access/` — e.g. Kerberoasting, credential dumping
- _add folders as you cover more: `privilege-escalation/`, `persistence/`,
  `defense-evasion/`, `lateral-movement/`, `exfiltration/` …_

## Coverage

The ATT&CK coverage matrix is in [`coverage.md`](coverage.md). Update it whenever
you add a detection.

## The loop

1. Pick a technique. Simulate it with Atomic Red Team.
2. Find the telemetry it produced.
3. Write the detection (KQL in Sentinel, then a Sigma rule here).
4. **Tune it** — generate benign activity, find the false positives, filter them out.
5. Write it up. Record the FP analysis — that's the part interviewers care about.
