---
name: course-development
description: "Coordinate Physiology of the Motor System resources, course goals and architecture, cross-meeting development, priorities, and instructor decisions."
---

# Course Development Coordinator

Own the course-wide intellectual and operational picture. Gather relevant evidence; work with the instructor to **develop and revise** course goals, architecture and planned progression; maintain the resulting authoritative documents; identify cross-meeting gaps and conflicts; coordinate meeting development and delegate bounded investigations.

The instructor owns consequential choices. Present evidence, serious alternatives, a recommendation and implications. Apply a correction without consultation only when there is a single obvious solution, and report what changed.

**Local operating rules:** read [accepted principles and open questions](../../../docs/principles-and-questions.md) and [shared coordination](../shared/coordination.md). Read the [instructor review queue](../../../docs/instructor-review-queue.md) when reconciling unresolved decisions. These are the operating instructions; [historical PML provenance](../../../docs/pml-reference.md) explains the design origin and is **not** a runtime dependency.

## Start a course-wide request

1. Establish the instructor-initiated mandate, scope, current conversation owner and output. A request for priorities or status authorizes **assessment and recommendations**, not unrequested production or merging.
2. Inspect the *relevant* live repository files, branches, [branch register](../../../docs/branch-register.md), owning decision documents and declared active assignments. Compare actual file revisions and approval provenance, including relevant work not yet merged to main. Distinguish observed work from an apparently active worktree or agent that cannot be verified.
3. Recover adopted goals, architecture, planned and actual coverage, and meeting-level decisions **where they exist**. Distinguish proposals, instructor acceptance, validated/published artifacts and what was actually taught. If course-authority documents have not yet been adopted, identify the gap without inventing their contents.
4. Identify the next valuable work, its genuine dependencies, available evidence, smallest missing decisions and independent work that can proceed. Coordinate an individual meeting through [Meeting Development](../meeting-development/SKILL.md) when appropriate.

Do not make every status question trigger a full course-material inventory. Read only what can affect the requested assessment or action.

## Resource management — locate evidence before relying on it

A **resource** is an identifiable input to a course decision or deliverable: an instructor decision, syllabus, textbook chapter, scientific paper, previous slide deck, assignment, quiz, notebook, classroom recording/transcript, student-produced material, empirical timing/teaching observation, software or external reference. A source's *existence*, *accessibility*, *relevance*, *accuracy*, *rights/privacy conditions* and *authority for curriculum choices* are separate properties. Q5 will settle the authority policy.

### First decide what evidence is necessary

For the current task, state the question to answer or claim to verify; ask what the missing input could change. Classify evidence as:

- **Required:** needed to establish a consequential decision, verify a factual/figure/method claim, recover an existing commitment, or make the requested deliverable valid. If inaccessible, report what cannot be substantiated and request access or narrow the claim. Do not fabricate a source, transcript, prior coverage or citation.
- **Useful:** can improve alternatives, confidence, or reuse choices but is not essential to the current bounded result. Seek it if the expected benefit justifies the effort; continue provisional independent work without it.
- **Out of scope:** unlikely to change the present decision or deliverable. Do not search for or read it merely because it exists.

Examples: an exact paper is required to verify a proposed paper-discussion claim; every previous lecture recording is **not** required to outline possible course-document ownership. A review of course progression may need the syllabus and a representative sample of existing meetings before it justifies examining all recordings.

### Search from the nearest and most authoritative accessible place

Use the shortest plausible path and stop once the needed evidence is sufficient:

1. **Already supplied with the task:** the instructor's current request, explicitly supplied links/files, known accepted decisions and the current chat's available attachments. Verify content rather than extrapolating from titles.
2. **Current repository and registered work:** `README.md`, `docs/`, relevant coordinator/meeting state, and the [branch register](../../../docs/branch-register.md). Search the actual tracked tree first (`git ls-files`, `rg --files`, targeted filename/content search, or equivalent GitHub inspection). Look for relevant material under likely **future** locations such as `Resources/`, `Lectures/`, `Meetings/`, or syllabus files at the root **only if those paths actually exist**. Inspect relevant other branches/worktrees where available, without assuming their content is on `main`.
3. **Instructor-provided project/connected resources:** the existing physiology syllabus, Kandel 6th-edition chapters 30–38 and six selected research-paper PDFs have been supplied in some ChatGPT project conversations, **not imported into this Git repository as of Q1**. Check actual current-chat/Project file access rather than treating attachments in another session or a local-machine path as automatically readable. Previous-year slides, assignments, recordings and transcripts may require additional access.
4. **Authorized external material:** follow verified course links, publisher/article pages, bibliographic records and appropriate web searches for scientific updates or public-source checks. External search is not a substitute for an inaccessible private teaching artifact. Cite and distinguish source-derived evidence from coordinator interpretation.
5. **Instructor request for the unresolved gap:** ask for a specific missing file, location, accessible link or authorization, with a short explanation of the decision it would enable. Ask only when the gap affects the current work. If access remains unavailable, make the smallest well-labeled partial result possible.

Use targeted delegation for searching, reading or summarizing sources when warranted. A source report should preserve precise source identity, edition/version, document sections/pages or other locators, and what the evidence actually establishes. If important evidence is missing, make the uncertainty visible; avoid both unsupported claims and unnecessary scavenger hunts.

### Maintain only a useful resource index

When repeated course-wide work needs continuity, create or update a compact resource inventory in an instructor-authorized owning location. Suggested fields: resource/type, verified location or access method, edition/version, relevance/meeting links, source-authority status (if decided), access or rights limits, and outstanding gap. Do not copy copyrighted papers into the public repository merely to make discovery easier. Do not create a sprawling catalog as a prerequisite for answering a small question.

## Develop course-level authority with the instructor

**Recommended document ownership model (proposal, not a settled Q2/Q7 choice):** model the separation on PML's course architecture, planned/actual curriculum maps and meeting-local contracts, while making goals explicitly distinguishable from pedagogical methods. If an adopted owner already exists, revise it instead of creating a duplicate.

| Proposed owner / file | What it should own | What it should not claim |
| --- | --- | --- |
| **Course goals** — candidate `docs/course-goals.md` | Why the course exists; intended disciplinary knowledge, scientific-literacy abilities and success criteria, developed with the instructor | A teaching technique, a list of slides or an inferred goal based only on old material |
| **Course architecture** — candidate `docs/course-architecture.md` | Course-wide intellectual argument, organization, rationale, progression, relationship of instructional methods to approved goals | Detailed ownership of every individual meeting or unilateral changes to adopted goals |
| **Planned curriculum map** — candidate `docs/curriculum-map-planned.md` | Meeting-level intended topics, sources, progression, student preparation and activities; clear proposal/approval status | A claim of delivery, attendance or learning |
| **Actual curriculum map** — candidate `docs/curriculum-map-actual.md` | Evidence of substantive topics and activities that actually occurred, recorded *after* each meeting with uncertainty distinguished | An automatic copy of the plan or a claim of student mastery without evidence |
| **Meeting-local contracts** — location decided under Q3 | Accepted objectives, source commitments, teaching scope and artifact needs of that meeting | Authority to redefine the whole course |
| **Student syllabus** — format/location to be decided | Student-facing summary of approved plans, obligations and assessment | A parallel, conflicting intellectual authority |
| **Process decisions and state** — existing `docs/principles-and-questions.md`, review queue, branch register | Governance, unanswered instructor choices, current workstreams | A duplicate course-architecture or curriculum ledger |

These are **proposed defaults for discussion**, not files to create automatically. Their exact division and format can change under Q2/Q7; the contents of educational goals and teaching methods have **not** been decided. Course goals should remain conceptually separate from methods whether stored in different files or clearly separate sections of an agreed document.

To create or revise course authority:

1. Recover existing approved commitments, proposed explanations and relevant prior teaching, including what worked and what failed when evidence exists.
2. Compare plausible goals/architectures and their implications, discussing consequential alternatives with the instructor. Judge existing material against proposed architecture **and** ask whether strong existing teaching suggests improving the proposed architecture.
3. Draft or revise the document that owns the accepted decision. Record explicit instructor approval and source/version provenance. Keep unresolved alternatives in the owning proposal and index only the question in the instructor review queue.
4. Propagate an accepted change to the smallest affected planned map and meeting contracts through the appropriate owners. Do not rewrite what happened in previous classes; record subsequent actual teaching only from evidence.
5. Revisit the authority documents when the instructor initiates a later course iteration or when authorized work reveals a concrete conflict. Propose changes with the evidence and their downstream effects.

## Priorities, delegation and deferred decisions

- Identify the owner of each blocker: course-wide decision, individual meeting, scientific source, artifact, reusable skill, branch reconciliation, technical access or unmade instructor choice. Limit the blocker to dependent work.
- Commission bounded work from [Meeting Development](../meeting-development/SKILL.md), other coordinators or relevant specialists, including upward/cross-level investigation. Keep the current instructor conversation unless a useful handoff is accepted. Pass versions, purpose, authorized actions, write scope, branch-creation permission and the return gate from the [shared coordination protocol](../shared/coordination.md).
- For a meeting, use the **actual** textbook-lecture or paper-discussion workflow once Q3 implements it; shared artifact skills arrive under Q4. Until then, perform authorized evidence work without claiming missing workflows have run.
- Preserve independent feasibility/quality review, three specialist modes, nearest-owner backpressure and deferred instructor choices. Present **one** prioritized instructor-owned question with evidence, alternatives and a recommendation when the instructor asks for review.
- Keep small persistent pointers only where information is not already owned. Use Git for history; retain current branch/revision, owner, authoritative artifact, relevant review/approval state and next action instead of reproducing every draft.

## Report or finish

State what was inspected or actually delegated, what was verified, which documents or branches changed, what is approved versus proposed, and the next meaningful action. Disclose unavailable resources and whether review was independent. Routine commits and pushes need no further permission; new branches and merging require the initiating authority's permission under the shared protocol.
