# Roadmap

Six projects that build toward a detection-engineering / SOC role, each mapped
to the competencies that kind of role hires for. Checked boxes are done.

## 1. Home SOC lab — *foundation*
- [ ] Sentinel workspace stood up
- [ ] Windows VM + Sysmon (SwiftOnSecurity config) shipping logs
- [ ] Linux VM + auditd shipping logs
- [ ] Architecture diagram + build notes in [`lab/`](lab/)

**Proves:** standing up and operating SIEM / telemetry pipelines.

## 2. Detection library — *centerpiece*
- [ ] 15 ATT&CK techniques simulated with Atomic Red Team and detected
- [ ] Each has a KQL query + a portable Sigma rule + a writeup
- [ ] False-positive analysis and tuning documented per rule
- [ ] ATT&CK coverage matrix kept current in [`detections/coverage.md`](detections/coverage.md)

**Proves:** building, validating and tuning detections; reducing false
positives; MITRE ATT&CK; detection coverage.

## 3. Identity & cloud attack paths
- [ ] AD lab (or GOAD) + free Entra/Azure tenant
- [ ] Simulate + detect: Kerberoasting, pass-the-hash, token/session theft, priv-esc
- [ ] 2+ cloud detections (risky sign-in, OAuth consent abuse, cloud audit log)

**Proves:** identity attack paths — credential theft, privilege escalation,
session/token abuse — and cloud security.

## 4. SOAR automation & response
- [ ] Shuffle (or Tines) playbook: alert → enrich via threat-intel API → ticket → (simulated) isolate host
- [ ] Python scripts for the API integrations in [`automation/`](automation/)
- [ ] Before/after showing the manual steps removed and time saved

**Proves:** SOAR workflows, API integrations, scripted response, lower MTTR.

## 5. Investigation portfolio — *runs in parallel, start now*
- [ ] 5–10 CyberDefenders / Blue Team Labs Online writeups in [`investigations/`](investigations/)
- [ ] Each: triage → scope → contain → root cause → the detection I'd add

**Proves:** end-to-end investigations from triage to post-incident improvement;
clear communication for technical and non-technical readers.

## 6. Differentiators
- [ ] Detection-as-code: CI validates every Sigma rule on commit *(scaffolded — see the workflow)*
- [ ] AI-assisted triage: LLM summarizes an alert, pulls related logs, suggests a verdict

**Proves:** improving operational effectiveness and detection coverage; plus a
research angle few junior candidates have.

---

### Cert track (parallel)
- [ ] Microsoft **SC-200** — maps almost line-for-line to the target role
- [ ] **BTL1** (hands-on) — later
