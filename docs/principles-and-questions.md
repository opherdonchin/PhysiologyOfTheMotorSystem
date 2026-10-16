# Accepted principles and open questions

## Accepted starting constraints

1. **Central Course Coordinator.** A central agentic coordinator oversees development and coordination of course materials and course-wide coherence; its responsibilities and implementation are specified by the accepted Q1 design below.
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

The design comparison used PML at the immutable commit [`8889ac0a433a784482a7ecf0931a006e3965bd6e`](https://github.com/opherdonchin/ProbabilisticMachineLearning/tree/8889ac0a433a784482a7ecf0931a006e3965bd6e). [Pinned file-level provenance and the local adaptations](pml-reference.md) are recorded separately. The conventions below now appear explicitly in the **local** coordination instructions; PML is historical evidence, not a source the coordinators must consult at runtime.

- **Queue is an index, not an authority.** Questions, options, recommendation and evidence live in the owning document; the queue links to them and records status. Accepted answers are recorded in the owner, then the queue records resolution by link.
- **Silence is not approval;** instructor approval must be explicit or already documented. Only the instructor makes consequential decisions; agents may record a decision and mark its question resolved in the owning artifact once explicit approval is documented there. Agent review, favorable automated review or a specialist's self-declared completion is not approval.
- **Deferred review.** Record instructor-owned choices without resolving them, continue independent work, and present one prioritized question when the instructor asks for review.
- **Build / feasibility-review / revision** as distinct modes; a reviewer returns an assessment (`feasible`, `feasible-with-risks`, `blocked`) and never grants approval. Disclose when a review was not independent.
- **Backpressure and decision ownership.** Route an issue to the nearest stage that owns the decision; never silently amend an upstream commitment.
- **Persistent state in owning artifacts.** Approvals recorded with provenance; avoid duplicate task ledgers or histories. PML uses a small committed `development_state.md` for multi-stage work.
- **Git history is the archive;** do not keep superseded drafts in the tree.

## Decisions that remain open

Reusing a convention above does not decide the following, which stay open:

- Specific meeting-local state locations/formats and the stage structure and specialist roles for lectures, paper discussions and artifacts (Q3, Q4); PML's five lecture stages are not adopted.
- Course goals, learning-objective representation and the scientific-literacy progression (Q2).
- Source-authority policy (Q5), evaluation of prior meetings (Q6), and final course-level authority document/map formats and other useful PML conventions (Q7). The Course Coordinator suggests an explicit goals/architecture/planned/actual document ownership model; filenames and content are **proposals**, not accepted curriculum decisions.
- Branch *naming conventions* may evolve with experience; Q1 already settles creation/merge authority and the lightweight branch register.

## Open questions

Q1's architectural design is agreed; Q2–Q7 remain open. Each is indexed in the [instructor review queue](instructor-review-queue.md). Options, recommendations and evidence are added under each question as it is investigated.

### Q1. Coordinator duties and boundaries

**Design status: resolved by explicit instructor discussion.** Implemented on the branch `feat/workflow-q1-coordinators`, pending separate permission to merge. The design is recorded here; software implementation and integration are distinct from instructor acceptance of pedagogical content.

- **Two coordinators:** Course Development handles course-wide resource gathering, course-architecture development/revision with the instructor, authoritative records, coherence and priorities. Meeting Development handles individual class meetings and chooses between the **distinct** textbook lecture and paper discussion workflows when those are defined under Q3. Both may commission shared artifact skills when Q4 defines them.
- **Direct intellectual responsibility:** Course Development itself develops course-level proposals and manages resources. It may delegate web research, reading, evidence summaries and document drafting; no separate course-architecture or resource-management coordinator is required. Course goals, educational methods and source-authority choices remain open for Q2/Q5 and instructor approval.
- **Conversation ownership is local to each chat:** Multiple chats can have different coordinators simultaneously. The coordinator managing a chat remains the instructor-facing conversation owner, even when it commissions substantive work from another coordinator at any level. Work ownership, conversation ownership and decision authority remain separate. A transfer of conversation is **recommended** when materially useful, and only undertaken with instructor agreement.
- **Flexible delegation:** Any coordinator can commission another, above or below it, using a bounded task envelope. The commissioned coordinator reports to its initiator/conversation owner. Consequential decisions remain the instructor's; delegated agents can make technical and other authorized local judgments, with evidence and reporting.
- **Concurrent work:** Discover other work when feasible, warn about overlapping writes, and reconcile semantic as well as Git conflicts. Do not impose global locks or prohibit instructor-chosen parallel work on the same branch or checkout. Branches are recommended for substantial work but never mandatory.
- **Branch authority follows the initiator:** A coordinator or delegate requests permission from its task initiator *before creating a branch*, unless already instructed/preauthorized. After creation, agents **commit and push freely**, including intermediate WIP commits. The **same initiating authority** must authorize the merge. Permission to merge is not instructor acceptance of substantive course changes. Course development requires neither issues nor PRs. Maintain the lightweight [branch register](branch-register.md).
- **Shared protocol:** Common delegation, handoff, authority, persistent-state, independent review, backpressure and Git conventions live in [shared coordination](../.agents/skills/shared/coordination.md), used by both coordinator skills rather than repeated or made a third skill.
- **Review and provenance:** Keep independent assessment, three modes (build / feasibility-review / revision), nearest-owner backpressure, deferred instructor decisions, and lightweight persistent state. These are specified locally. PML's exact source commit and adapted precedents are in [the historical reference](pml-reference.md); PML's five-stage lecture pipeline has not been adopted.

Implementation: [Course Coordinator](../.agents/skills/course-development/SKILL.md) and [Meeting Coordinator](../.agents/skills/meeting-development/SKILL.md). The precise stage/meeting-local state formats and concrete instructional/artifact skills are Q3/Q4 matters.

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
