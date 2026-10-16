# Coordinator branch register

Best-effort index of branches opened as part of coordinator-managed work. This is **not** a lock, approval authority, issue tracker or commit history. Reconcile with actual Git branches when resuming work. The shared copy normally lives on `main`; an unmerged topic branch's copy may not yet be visible from `main`.

See [shared coordination rules](../.agents/skills/shared/coordination.md) for opening, committing/pushing, merging and retirement. Branch creation and merging require the **task initiator's** permission; working commits and pushes do not. Branch creation remains optional. No PR or issue is required.

| Branch | Outcome | Created by | Authorizing initiator and evidence | Base | Status / disposition |
|---|---|---|---|---|---|
| `feat/workflow-q1-coordinators` | Implement approved Q1 coordinator foundations | Course-development session agent | Instructor explicitly authorized branch creation, 2026-10-17 (Q1 discussion) | `main@21a7c52` | Active; pending instructor review/merge authorization |

Update an entry when its intended outcome materially changes or the branch is merged, abandoned or removed; include disposition/date. Do not reproduce every commit or active task. A branch created outside this coordination process need not appear here. An absent or stale entry is **not** evidence that an independently opened branch is unauthorized.
