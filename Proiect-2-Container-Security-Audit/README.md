# Project 2 - Container Image Security Audit

Continuous vulnerability scanning of container images using Trivy, integrated with GitHub Actions and automated issue tracking.

## Full writeup

Read the complete walkthrough with methodology, findings, and CI integration patterns:

**[mihaitapalaga.dev/blog/container-security-audit](https://mihaitapalaga.dev/blog/container-security-audit)**

## What's in this folder

| Path | Description |
|------|-------------|
| `workflows/container-scan.yml` | Reusable GitHub Actions workflow that runs Trivy on push and on schedule, uploads SARIF results to the GitHub Security tab. |
| `workflows/auto-issue.yml` | Companion workflow that opens GitHub Issues per Critical CVE for ownership tracking. |
| `methodology/triage-process.md` | Documented triage process for filtering, prioritizing, and assigning vulnerability findings. |
| `methodology/hardening-checklist.md` | Base image hardening patterns derived from real audits. |

## Quick summary

- Target type: containerized PHP web application (legacy base image)
- Tool: Trivy (open-source, integrates natively with GitHub Actions)
- Integration: SARIF upload to GitHub Security + Issues API for explicit ownership
- Outcome: continuous scan workflow that turns CVE findings into tracked engineering work, not a one-off dashboard
- Key insight: most Critical findings live in transitive base-image dependencies (zlib, libxml2, openssl), not in application code

The application code itself is private and cannot be shared. The workflow templates, methodology, and hardening patterns in this folder are generic and applicable to any container image scan.

Full repository at the root README: [../README.md](../README.md)
