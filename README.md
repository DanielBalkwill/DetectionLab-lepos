# Detection Lab — a blue-team detection engineering portfolio

A home SOC lab where I simulate attacker techniques, build and tune the
detections that catch them, and run end-to-end investigations. Everything here
is mapped to **MITRE ATT&CK** and written up so it can be read by someone who
wasn't in the room.

> Learning / portfolio project built in a self-contained home lab. No production
> systems or real customer data are involved.

## Why this exists

I'm building toward a detection-engineering / SOC role. This repo is the
evidence: detections I've written and tuned, investigations I've worked
start-to-finish, and the automation I've used to cut response time.

## What's here

| Area | What it is |
|------|------------|
| [`lab/`](lab/) | How the SOC lab is built — SIEM, endpoints, log sources |
| [`detections/`](detections/) | The detection library: a rule + writeup per technique, with ATT&CK coverage |
| [`investigations/`](investigations/) | End-to-end incident writeups (triage → contain → lessons learned) |
| [`automation/`](automation/) | SOAR playbooks and response scripts |
| [`roadmap.md`](roadmap.md) | The build plan and current progress |

## Detection coverage

See [`detections/coverage.md`](detections/coverage.md) for the ATT&CK coverage
matrix. Current count: **1 technique** (just getting started).

## Stack

- **SIEM:** Microsoft Sentinel (KQL) — with Sigma rules for portability
- **Endpoint telemetry:** Sysmon on Windows, auditd on Linux
- **Attack simulation:** Atomic Red Team
- **Detection-as-code:** Sigma rules validated in CI on every commit

## How detections are validated

Every Sigma rule in `detections/` is checked automatically by
[GitHub Actions](.github/workflows/validate-detections.yml) — detection-as-code,
so a broken rule never reaches `main`.
