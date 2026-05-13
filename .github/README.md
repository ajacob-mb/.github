# Label Taxonomy Platform (DevEx)

This repository provides a centralized platform to standardise and enforce GitHub labels across repositories using a GitHub App.

---

## Purpose

- Standardise label taxonomy across repositories
- Safely migrate legacy labels
- Enforce consistency over time

---

## Files

- .github/label-config/labels.json -> Source of truth (desired labels)
- .github/label-config/label-mapping.json -> Maps old labels to new ones
- .github/label-config/staged-migration.json -> Defines stage1, stage2, and all rollout groups
- .github/workflows/label-taxonomy.yml -> Executes introduce, migrate, enforce

---

## Modes

### introduce
- Creates missing labels
- Updates color and description
- Does NOT modify issues
- Does NOT delete labels

### migrate
- Creates labels
- Adds mapped labels to issues
- Keeps old labels

### enforce
- Creates labels
- Migrates issues
- Deletes all labels not in labels.json

---

## How to Run

1. Go to your repository in GitHub
2. Click Actions
3. Select the Label Taxonomy workflow
4. Click Run workflow
5. Choose mode:
   - introduce
   - migrate
   - enforce
6. Choose stage:
   - stage1
   - stage2
   - all
7. Click Run workflow

---

## Recommended Order

1. introduce
2. migrate
3. enforce

---

## Notes

- The workflow is safe to run multiple times
- It will only change what is out of sync
- Enforcement removes any labels not defined

---

## Future

Add a schedule to run automatically.

Example: run daily at 2am

This enables continuous enforcement.
