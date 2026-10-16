# PML reference architecture — historical design provenance

Physiology Q1 was designed against the **fixed PML commit** [`8889ac0a433a784482a7ecf0931a006e3965bd6e`](https://github.com/opherdonchin/ProbabilisticMachineLearning/tree/8889ac0a433a784482a7ecf0931a006e3965bd6e), dated 2026-10-16. Links below point to that commit, not to `main`. The commit is background provenance **only**: operational Physiology skills are self-contained and agents are **not required to open or follow PML files** during ordinary work. Later PML changes have no effect on our rules without explicit local revision.

## Specific precedent and local adaptation

| PML source at pinned commit | Observed responsibility or convention | Physiology Q1 adaptation |
| --- | --- | --- |
| [Course Development Coordinator](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/.agents/skills/course-development/SKILL.md) | Course-wide state recovery, prioritization, bounded dispatch, branch/write ownership and deferred instructor questions | The Course Coordinator also directly develops course-level architecture and manages resource discovery with the instructor; no separate architecture workflow |
| [Lecture Development Coordinator](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/.agents/skills/lecture-development/SKILL.md) | Instructor-facing orchestration across stages, approval provenance and a meeting-local development-state index | A single Meeting Coordinator selects between two future **distinct** workflows: textbook lecture and paper discussion (stages reserved for Q3) |
| [Shared backpressure](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/.agents/skills/shared/backpressure.md) | `build`, `feasibility-review`, `revision`; nearest decision owner; reviewers assess but do not approve; revalidate affected work | The shared [coordination protocol](../.agents/skills/shared/coordination.md) states these conventions for both kinds of meeting |
| [Instructor review queue](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/Lectures/course_architecture_scope/reconciliation/instructor_review_queue.md) | Compact pointers to unresolved instructor-owned decisions, with substantive evidence and proposals in owning artifacts | [Physiology review queue](instructor-review-queue.md) preserves the same index-versus-authority distinction |
| [Course coordination state](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/Lectures/course_development_state.md) | Cross-course pointers to current branches/decisions rather than a copy of every lecture's history | Small coordinator state when needed, plus the [branch register](branch-register.md); no issues or PRs |
| [PML AGENTS.md](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/AGENTS.md) and [branch policy](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/docs/branch-management.md) | Explicit course authority and detailed branch lifecycle | Physiology replaces the branch policy with initiator permission to **create and merge**; commits/pushes are autonomous and branches are optional |

## Course-level documents: the PML pattern

At this commit, PML explicitly distinguishes four *owners*, with complementary rather than competing authority:

- [`course_architecture.typ`](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/course_architecture.typ): course intellectual purpose, rationale and **planned** progression; includes an explicit statement of what the course is for.
- [`curriculum_map.typ`](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/curriculum_map.typ): **planned** topic/source allocations and practical exercises; proposals are not proof of teaching.
- [`curriculum_map_actual.typ`](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/curriculum_map_actual.typ): **actual** substantive teaching/activity, recorded after class, not inferred from slides or approved plans.
- [Lecture Scope and development-state conventions](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/.agents/skills/lecture-development/SKILL.md): instructor-approved *meeting-specific* commitments, with technical status/approval provenance indexed separately.

The PML [student syllabus](https://github.com/opherdonchin/ProbabilisticMachineLearning/blob/8889ac0a433a784482a7ecf0931a006e3965bd6e/advanced_statistics_2027_1_syllabus.typ) communicates the plan; it is not a second authoritative curriculum ledger. These distinctions inform the **provisional document defaults** in our Course Coordinator. Physiology may additionally separate a goals document from course architecture to protect the accepted goals-versus-methods distinction. Exact filenames, contents and acceptance remain Q2/Q7 decisions.

## Source boundaries

PML's mathematical aims, datasets, algorithms, lecture stage sequence, notebook conventions, named branches and course-specific rules are **not** Physiology requirements. HILD is also not installed. The locally accepted principles in [`principles-and-questions.md`](principles-and-questions.md) and the executable local coordinator/coordination instructions, not these historical files, govern this repository.
