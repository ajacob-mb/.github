# GitHub Organisation Standards

This repository defines organisation-wide standards for how work is created, structured, and reviewed across all repositories.

It is part of the DevEx platform architecture:

- `.github` → Developer Experience (UX + templates)
- `platform-devex-governance` → Governance + automation
- Template repositories → Project bootstrap

---

## 🎯 Purpose

These standards ensure that:

- Issues are clear, structured, and actionable
- Pull requests are traceable and reviewable
- Work is consistent and automatable across repositories
- Developers can focus on delivery rather than process

---

## 🧱 What This Repository Provides

### 1. Issue Templates

All issues must be created using structured templates:

- Bug
- Feature
- Task
- Documentation

These ensure:
- Required fields are present
- Acceptance criteria are defined
- Issues are AI-friendly and automatable

---

### 2. Pull Request Template

All pull requests must follow a standard structure:

- Jira reference  
- GitHub issue linkage  
- Summary and changes  
- Validation steps  
- Risk and rollout  

---

### 3. Contribution Guidance

Defines how developers:

- Create issues
- Link work to Jira
- Create and manage pull requests

---

## 🔁 How This Works with the Platform

This repository works together with:

### `platform-devex-governance`

- Applies label taxonomy across all repositories
- Migrates legacy labels
- Enforces consistency through scheduled reconciliation

---

## 🧠 Workflow Overview

```text
Issue → Branch → Pull Request → Merge