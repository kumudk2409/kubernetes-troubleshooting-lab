# Kubernetes Troubleshooting Lab

## Overview
This repository contains intentionally broken Kubernetes configurations designed to simulate
common production incidents and demonstrate a structured troubleshooting approach.

The focus is on **operational debugging**, not application development.

---

## Scenarios Covered
- CrashLoopBackOff
- ImagePullBackOff
- Pending pods due to scheduling constraints
- Readiness probe failures

---

## Troubleshooting Methodology
For each scenario:
1. Observe pod status (`kubectl get pods`)
2. Inspect events (`kubectl describe pod`)
3. Review container logs
4. Identify the root cause
5. Apply the smallest possible fix

This mirrors real-world incident response workflows used by SRE and platform teams.

---

## Example: CrashLoopBackOff

**Symptom**
- Pod repeatedly restarts

**Diagnosis**
- Logs show immediate container exit

**Root Cause**
- Application process exits with non-zero status

**Resolution**
- Correct container command to keep process alive

---

## Why This Project Exists
Most Kubernetes outages are caused by:
- Misconfiguration
- Incorrect assumptions
- Missing resource or health definitions

This lab demonstrates how these failures surface and how to resolve them quickly and safely.

---

## Production Improvements
In a real production environment, this would be complemented by:
- Centralized logging
- Metrics and alerting
- Automated health validation in CI
- Runbooks for common failure modes