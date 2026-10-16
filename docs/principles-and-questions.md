# Accepted principles and open questions

## Accepted starting constraints

1. **Central Course Coordinator.** A central agentic coordinator will oversee development and coordination of course materials and maintain course-wide coherence. Its detailed responsibilities and implementation remain to be developed with the instructor.
2. **Instructor control.** Work is initiated by the instructor or follows directly from needs revealed by instructor-initiated work. The coordinator surfaces issues, preferably with evidence, possible solutions and recommendations. It may apply a solution without asking only when there is one obvious solution, and it must report that action. All consequential choices, or choices among meaningful alternatives, require specific instructor approval. Silence is not approval.
3. **Agentic review.** Meaningful development stages receive agentic feasibility or quality review, preferably independent where supported. Preserve PML's distinction between build, feasibility-review and revision, its backpressure principles, and its separation of agent assessment from instructor acceptance. Review effort is proportionate to the task.
4. **Two kinds of class development.** Textbook-oriented lectures and research-paper-oriented discussions require distinct instructional-development skills. Their stages are not yet decided.
5. **Shared artifact development.** Slides, assignments, question banks, quizzes/Kahoot, handouts, videos and other artifact capabilities are reusable across kinds of meetings. Instructional purpose is distinguished from artifact type.
6. **Existing resources.** Development draws on existing teaching materials, scientific literature and the previous course. Sources have different authority, to be established explicitly through instructor discussion. Recordings and transcripts are additional evidence about timing, classroom activity and teaching difficulties.
7. **Course goals versus methods.** Educational goals remain conceptually separate from the teaching methods used to achieve them. The goals will be developed through instructor discussion.
8. **Scientific literacy.** Scientific reading, writing and critical reasoning are developed more explicitly, but stay lightweight and supportive of neurophysiology content. Wherever possible, activities serve both scientific-literacy and disciplinary goals.
9. **Reuse versus generation.** Existing resources, written or video, are evaluated alongside newly generated ones. Selection depends on suitability, not a general preference.
10. **No premature curriculum decisions.** The instructor is open-minded about how much of the existing course should change. The process supports considered decisions and does not assume conservative revision or substantial redesign.

## PML conventions reused

Read from [ProbabilisticMachineLearning](https://github.com/opherdonchin/ProbabilisticMachineLearning) (`AGENTS.md`, `.agents/skills/course-development/SKILL.md`, `.agents/skills/lecture-development/SKILL.md`, `.agents/skills/shared/backpressure.md`, `Lectures/course_architecture_scope/reconciliation/instructor_review_queue.md`). These are adopted as conventions for the review queue and for how future processes will record state. No PML skill or pipeline has been copied.

- **Queue is an index, not an authority.** Questions, options, recommendation and evidence live in the owning document; the queue links to them and records status. Accepted answers are recorded in the owner, then the queue records resolution by link.
- **Silence is not approval;** instructor approval must be explicit or already documented. Only the instructor makes consequential decisions; agents may record a decision and mark its question resolved in the owning artifact once explicit approval is documented there. Agent review, favorable automated review or a specialist's self-declared completion is not approval.
- **Deferred review.** Record instructor-owned choices without resolving them, continue independent work, and present one prioritized question when the instructor asks for review.
- **Build / feasibility-review / revision** as distinct modes; a reviewer returns an assessment (`feasible`, `feasible-with-risks`, `blocked`) and never grants approval. Disclose when a review was not independent.
- **Backpressure and decision ownership.** Route an issue to the nearest stage that owns the decision; never silently amend an upstream commitment.
- **Persistent state in owning artifacts.** Approvals recorded with provenance; avoid duplicate task ledgers or histories. PML uses a small committed `development_state.md` for multi-stage work.
- **Git history is the archive;** do not keep superseded drafts in the tree.

## Decisions that remain open

Reusing a convention above does not decide the following, which stay open:

- Whether and where a `development_state.md`-style register is used here, and its format (part of Q1/Q3).
- The stage structure and specialist roles for lectures, paper discussions and artifacts (Q3, Q4); PML's lecture stages (Scope, Section Design, Slide Organization/Design/Authoring) are not adopted.
- Coordinator duties and its relation to specialists (Q1).
- Branch-naming and lifecycle rules (PML `docs/branch-management.md`), authority documents and curriculum maps (Q7).

## Open questions

Status of all questions: open. Each is indexed in the [instructor review queue](instructor-review-queue.md). Options, recommendations and evidence are added under each question as it is investigated.

### Q1. Coordinator duties and boundaries

How are the coordinator's detailed duties and boundaries defined?

### Q2. Goals and scientific literacy

How are course goals, learning objectives and the progression of scientific-literacy skills represented?

### Q3. Lecture vs. paper-discussion workflows

What distinct workflows do textbook lectures and paper discussions need?

### Q4. Shared artifact skills

What shared artifact-development skills are needed, and how are they reviewed?

### Q5. Source authority

How is source authority established, including classroom transcripts and existing teaching materials? Importing existing materials requires an instructor-authorized scope and appropriate consideration of source rights and privacy; settling all of Q5 is not a prerequisite for every individual import.

### Q6. Evaluating existing meetings

How is the effectiveness of existing class meetings evaluated?

### Q7. Further PML reuse

Which further aspects of PML (beyond those listed above) should be reused or modified?
