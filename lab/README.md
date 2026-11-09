# Lab build

How the SOC lab is wired together. Fill this in as you build it.

## Architecture

_Add a diagram here (e.g. draw.io / Excalidraw export) showing:_
- SIEM (Microsoft Sentinel) and its Log Analytics workspace
- Windows endpoint(s) with Sysmon → Azure Monitor Agent → Sentinel
- Linux endpoint(s) with auditd → Sentinel
- Attack host (Kali / your box) running Atomic Red Team

## Build notes

### 1. SIEM — Microsoft Sentinel
- [ ] Azure free account + Log Analytics workspace
- [ ] Sentinel enabled on the workspace
- Notes:

### 2. Windows telemetry
- [ ] Windows VM
- [ ] Sysmon installed with the SwiftOnSecurity config
- [ ] Azure Monitor Agent forwarding Security + Sysmon logs
- Notes:

### 3. Linux telemetry
- [ ] Linux VM with auditd
- [ ] Logs forwarding to Sentinel
- Notes:

## Data sources live

| Source | Table in Sentinel | Status |
|--------|-------------------|--------|
| Windows Security | `SecurityEvent` | ☐ |
| Sysmon | `Event` / `Sysmon` | ☐ |
| Linux auditd | `Syslog` | ☐ |

## Cost control

Sentinel bills on ingestion. Keep volume tiny: filter to the tables you need,
tear down VMs when they're idle, and watch the free-tier daily cap.
