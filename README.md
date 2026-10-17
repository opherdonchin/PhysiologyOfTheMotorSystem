# Physiology of the Motor System

Repository for developing the graduate course **Physiology of the Motor System**
(Biomedical Engineering Department, Ben-Gurion University), and for the
AI-assisted processes used to develop its instructional materials.

## Status

The previous course has a syllabus, textbook chapters, research papers,
slide decks, assignments and recordings/transcripts. We are currently
**developing the course-development process**, not redesigning the course.
The Q1 Course and Meeting Coordinator skills and shared governance are in place.
The instructor-approved [course goals](docs/course-goals.md) (Q2) are recorded.
The two instructional workflows and reusable artifact skills (Q3/Q4) remain open.
The two-repository publication architecture has been agreed but not implemented.

## Contents

- [`AGENTS.md`](AGENTS.md) - brief guidance for agents working in this repository.
- [`docs/course-goals.md`](docs/course-goals.md) - Q2 instructor-approved course goals and assessment boundaries.
- [`docs/principles-and-questions.md`](docs/principles-and-questions.md) - accepted principles, publishing-architecture decision, reused PML conventions, and open questions.
- [`docs/instructor-review-queue.md`](docs/instructor-review-queue.md) - index of unresolved instructor decisions.
- [`docs/branch-register.md`](docs/branch-register.md) - best-effort record of coordinator-created branches.
- [`docs/pml-reference.md`](docs/pml-reference.md) - exact PML source commit, historical precedents and local adaptations.
- [`course-development`](.agents/skills/course-development/SKILL.md) - course-wide coordinator skill.
- [`meeting-development`](.agents/skills/meeting-development/SKILL.md) - shared meeting coordinator for the future distinct lecture and paper workflows.
- [`shared/coordination.md`](.agents/skills/shared/coordination.md) - delegation, handoffs, reviews, authority and Git conventions.

## License

Original educational materials and documentation are licensed under
[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (see [`LICENSE`](LICENSE)).
Future scripts and software will be licensed separately under MIT. Third-party
materials, such as published readings, are excluded from the CC BY license grant
and remain under their own terms.

## Reference repositories

- [ProbabilisticMachineLearning (PML) at pinned commit](https://github.com/opherdonchin/ProbabilisticMachineLearning/tree/8889ac0a433a784482a7ecf0931a006e3965bd6e) - **historical design reference only**, not a runtime dependency; see [source-by-source provenance](docs/pml-reference.md) and [locally accepted conventions](docs/principles-and-questions.md#pml-conventions-reused).
- [HILD](https://github.com/Motor-Learning-Lab/HILD) - process for developing scientific software. Not installed here; its governance principles may inform later decisions.
