# T<ATT&CK ID> — <Technique name>

| | |
|---|---|
| **ATT&CK** | [T<id>](https://attack.mitre.org/techniques/T<id>/) — <tactic> |
| **Platform** | Windows / Linux / Azure |
| **Data source** | <e.g. Windows Security 4769, Sysmon 1> |
| **Sigma rule** | [`<name>.yml`](<name>.yml) |
| **Status** | experimental / tested / tuned |

## Hypothesis
What does the attacker do, and what observable does it leave behind?

## Simulation
How I generated the telemetry (Atomic Red Team test number, command, or manual steps).

## Detection logic
Plain-English description of what the rule matches and why.

### KQL (Sentinel)
```kql
<query>
```

## Validation
- Fired on the simulated attack? ✅ / ❌
- Evidence (screenshot / result row):

## False positives & tuning
What benign activity trips this, and how I filtered it out. Before/after FP rate
if you have it. **This section is the point** — anyone can write a noisy rule.

## Response
What an analyst should do when this fires: triage questions, containment,
escalation.
