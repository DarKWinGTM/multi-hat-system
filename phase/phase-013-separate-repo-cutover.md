# Phase 013 - Separate repo cutover

> **Summary File:** [SUMMARY.md](SUMMARY.md)
> **Phase ID:** 013
> **Status:** Implemented - Pending Review
> **Design References:** [../design/design.md](../design/design.md)
> **Patch References:** [../patch/phase-013-separate-repo-cutover.patch.md](../patch/phase-013-separate-repo-cutover.patch.md)

---

## Objective

Finalize `multi-hat-system` as its own standalone GitHub repo authority without leaving duplicate public install posture behind in the shared workspace.

## Action points / execution checklist
- [x] finish restart-time visibility validation
- [x] decide the final standalone distribution story for the repo
- [x] create/push `DarKWinGTM/multi-hat-system`
- [x] validate repo-root local marketplace install from `./`
- [ ] switch authority from shared workspace to standalone repo
- [ ] retire shared-workspace authority cleanly
