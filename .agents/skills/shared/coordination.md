# Shared coordination protocol

This is a **reference protocol**, not a separately invoked skill. The Course Development and Meeting Development coordinators both read it before delegating work, managing concurrent development, or arranging a handoff. Their own skills specify *what* they coordinate; this file specifies *how* they cooperate.

Adapted from the PML course-/lecture-development coordination and backpressure model, with the instructor's approved Physiology Q1 decisions taking precedence. Read [the accepted principles](../../../docs/principles-and-questions.md) as well.

## Initiation, roles and authority

- **Instructor mandate:** Development starts with an instructor request or follows from that requested work. Within such a mandate, coordinators may investigate, seek evidence, recommend work, and delegate bounded tasks without requiring a fresh instructor request for every detail. Do not use this freedom to initiate an unrelated program or silently revise course commitments.
- **Conversation owner:** The coordinator currently conducting a particular instructor conversation. It preserves continuity, presents choices, collects the instructor's answers and coordinates delegated results. Multiple chats may have different conversation owners simultaneously; each chat has one current owner.
- **Task initiator:** The instructor or coordinator that requested a particular piece of work from another coordinator or specialist. It may differ from the conversation owner. It is the authority that authorizes creation and subsequent merging of branches opened for that task.
- **Work owner:** The coordinator or specialist responsible for a particular deliverable or authoritative artifact. Delegation does not transfer ownership of unrelated artifacts.
- **Decision authority:** Instructors alone accept consequential teaching, curriculum, scientific-source authority, or architectural choices. Agents may make justified technical and local process decisions within their remit. Apply an unrequested correction only when there is one obvious solution, and report it explicitly. Silence, a favorable review, a commit, a push or a merge is not pedagogical acceptance.

These roles are independent. A Meeting Coordinator may commission the Course Coordinator to investigate course-wide architecture while continuing the instructor conversation; the resulting instructor decision must be recorded in the appropriate course-level owning artifact.

## Cross-level delegation and return

Any coordinator may commission work from any other coordinator or specialist, above, below or across the hierarchy. Do not force the instructor to change chats merely because the intellectual question crosses levels.

Send a **bounded task envelope** identifying, as applicable:

- initiator and conversation owner; objective and requested deliverable;
- authoritative inputs, current branch/revision and relevant approvals;
- exact allowed write paths and existing competing work;
- whether the assignment is read-only, a build, a feasibility review or a revision;
- decisions reserved for the instructor, required review, actual dependencies and the return/acceptance gate;
- whether branch creation has already been authorized. A task assignment alone is **not** permission to create a branch unless it says so.

The recipient may use its normal expertise, make local decisions within the assignment and further delegate within the same instructor-originated mandate. Return evidence, alternatives, recommendations, unresolved decisions, versions and actual work completed **to the commissioning coordinator**, not as a competing instructor-facing conversation. The conversation owner makes the instructor-facing presentation and relays approved decisions back to the owner of the authoritative artifact.

An instruction to invoke another skill is not proof that another agent was actually launched. If independent agents or sessions are not available, state that and use a read-only analysis, an explicit serial handoff or a proposed delegation instead.

## Conversation handoffs

A coordinator may recommend transferring the *conversation* when another coordinator would manage its next phase materially more effectively. A change of subject alone does not require a transfer. The instructor decides whether to move; until then, the current coordinator remains conversation owner.

For an accepted transfer, provide a reusable handoff prompt with the current aim, initiating mandate, repo/branches/revisions, accepted decisions and provenance, unresolved choices, relevant evidence, active delegated work and its owner, exact next action, and applicable restrictions. A chat handoff is not a transfer of repository write ownership or instructor decision authority.

## Concurrent chats and Git branches

Use **optimistic concurrency**, not a global scheduler or exclusive-lock system. Independent instructor chats may proceed at different coordinator levels. Inspect relevant branches, live files and the branch register before substantial overlapping work; describe uncertainty, conflicting assumptions and potential semantic as well as textual conflicts. Discovery and warnings should not become a veto. Do not assume a different chat is inactive, or that its agent is controllable from this chat.

**Branch creation**

- Recommend a branch when substantial, multi-session or parallel work is reasonably expected. A branch is always optional.
- **Before any coordinator or its delegate creates a branch, obtain permission from its task initiator**, unless that initiator has explicitly instructed or preauthorized its creation. The initiator may be another coordinator or the instructor. Record who authorized it.
- Use a descriptive outcome-based branch name when convenient; do not impose PML's naming scheme as a gate. Prefer a known, recorded base commit.
- If the instructor chooses shared-branch or shared-checkout parallel work, explain the risk of overwrite, divergent heads and accidental mixing, and recommend recoverable checkpoints where feasible. **Do not forbid it.** Never silently commit someone else's unexamined work or force-push away unique work.

**Work on the branch**

- Agents may commit and push ordinary work freely and frequently, including provisional and WIP states. Do not request repeated permission or over-curate commits destined for a squash merge.
- A commit or push records work, not approval. Keep the provenance and provisional status of substantive choices explicit.
- Prefer separate worktrees or branches for potentially conflicting writes, but treat this as advice rather than an instructor-imposed restriction.

**Integration and retirement**

- **Before merging a branch, obtain permission from the task initiator who authorized its creation**, or from that initiator's explicitly designated successor. This rule follows the initiating/delegation relationship, not an absolute course/meeting hierarchy. It applies to merges into main and to other branches.
- Merge authorization does not itself approve consequential course decisions. If the merged material includes a pending proposal, it remains labeled provisional until separately accepted by the instructor; no agent may silently promote it to authority.
- Inspect expected destination, current heads and substantive differences. Identify semantic disagreements even if Git reports no textual conflicts. Escalate consequential alternatives to the instructor.
- After integration or abandonment, record disposition. Verify incorporated work before deleting a branch; do not discard unmerged unique work as routine cleanup. No issues or pull requests are required for course development.

## Branch register

[docs/branch-register.md](../../../docs/branch-register.md) is a lightweight **best-effort index** of coordinator-opened workstreams, not an approval or locking system. Keep the shared copy on main when available. Record each branch's name, intended outcome, creator, authorizing initiator/provenance, base, and status/disposition; do not log each commit or duplicate Git history. Update at creation, material change of purpose, merge, abandonment or deletion.

The register can lag behind actual branches, especially when several conversations run independently or the register exists only on an unmerged implementation branch. On resume, reconcile it against live Git. If updating the shared copy would collide with another session, note the pending update and reconcile when safe; a stale/missing entry never makes a branch unauthorized.

## Reviews, backpressure and instructor decisions

Preserve PML's three specialist modes where stages exist:

- **Build:** the owning specialist develops its assigned artifact and reports status, risks and decisions required.
- **Feasibility-review:** a downstream or independent reviewer checks an *identified provisional artifact and revision*, without constructing the next artifact or editing the upstream one. Return a verdict of feasible, feasible-with-risks or blocked, with evidence and limitations.
- **Revision:** the owning stage changes only affected commitments or artifacts in response to an authorized correction, preserving unaffected agreements.

Choose proportionate review effort; prefer independent agentic review for substantial stages and disclose same-context or unperformed checks. The reviewer supplies assessment, **not instructor approval**. A preliminary feasibility preview is not final validation; later execution can expose new backpressure.

Route each problem to the **nearest stage or artifact that owns the decision**, not automatically to the top. Report blocker/advisory/local-fix status, exact source/revision, evidence, smallest repair, effect on dependent work and what can continue. Do not silently rewrite an accepted upstream commitment. Revalidate only affected downstream artifacts after a consequential revision. When there are real alternatives, present the instructor with the relevant tradeoff and a recommendation; never invent an approval to unblock work.

Defer instructor-owned questions to their owning proposal or review artifact and index unresolved pointers in [the instructor queue](../../../docs/instructor-review-queue.md). Do not interrupt the instructor for each finding. Continue independent authorized work and present **one prioritized question** when review is requested. Record approved answers with provenance in the owning document, and then update the queue pointer. Approval of one example or bounded outcome does not approve an entire plan.

## Persistent state and recoverability

Git is the archive; authoritative documents own their respective commitments and evidence. A sustained multi-stage meeting can use a small meeting-local development-state index with relevant branch/revision, stage, acceptance provenance, review status, blockers and next owner/action; actual location and stage-specific format belong to later workflow design (Q3). Keep course-level state limited to live cross-meeting assignments, review pointers and dependencies not owned elsewhere. Avoid a second curriculum ledger, a running task diary or placeholder registers.

Track **proposed, instructor-approved, downstream-validated, published and taught** as distinct states. A future course-architecture document must be developed with the instructor rather than assumed to preexist. The actual record of teaching is not inferred from prepared materials, commits or slides.
