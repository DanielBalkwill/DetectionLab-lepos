# Automation & response

SOAR playbooks and the scripts behind them. Goal: cut mean-time-to-respond by
automating the boring, repeatable parts of triage and containment.

## Playbooks

| Playbook | Trigger | Actions | Status |
|----------|---------|---------|--------|
| enrich-and-triage | New alert | Enrich IP/hash via threat-intel API → score → open ticket | ☐ |
| contain-host | Confirmed malicious | (Simulated) isolate host → notify | ☐ |

## Stack
- **SOAR:** Shuffle (open-source) or Tines (free tier)
- **Scripts:** Python for the API integrations (keep secrets out of git — use `.env`)

## Measure it
For each playbook, record the manual steps it replaced and the time saved —
that's the MTTR story the target role asks for.

_Scripts go here. Never commit API keys; `.env` is gitignored._
