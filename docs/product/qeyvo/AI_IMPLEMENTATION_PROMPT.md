# Qeyvo — AI implementation handoff (PRD v1.2)

Paste the prompt below into the coding agent that has authorised access to the product repository. Attach `MASTER_PRD.md` and `REQUIREMENTS.json`, or place their contents in the repository. The PRD is the authoritative specification; the JSON is a bootstrap tracking index, not a substitute for the complete document.

---

You are upgrading **Qeyvo**, my existing product, into the B2B AI workforce SaaS described in this PRD. **Qeyvo already exists and its name is confirmed. Work in the current Qeyvo repository. Do not create a replacement application, reset the repository, rename the product, or replace work we have already completed.**

Read the entire attached `MASTER_PRD.md`, its source/evidence boundaries, and `REQUIREMENTS.json`. The objective is a real commercial application for companies to configure persistent AI teammates that understand approved company knowledge and execute verifiable workflows under enforceable permissions, human approval and spending limits. Do not produce only mockups, a proposal, or a cosmetic rebrand.

Implement the full programme in dependency order: controlled paid-pilot requirements (P0), general SaaS requirements (P1), then the specified enterprise/advanced workstreams (P2). Staging the work does not mean silently discarding later requirements. Each phase must pass its own gates before its features are sold or enabled for real customers. Implement independent code and test infrastructure while externally gated items remain blocked.

## Start with discovery and reuse

1. Inspect the actual Qeyvo repository, branch, commit, instructions, existing worktrees/changes, merged work, architecture and implementation tracking. Never overwrite unrelated work. Record Qeyvo’s actual baseline from its current code and test evidence. If Qeyvo access is missing, record the access blocker rather than substituting a different codebase.
2. Reconcile Qeyvo with every PRD requirement in a gap matrix: satisfied, present-unverified, partial, missing, conflicting or not-assessed. Link current code and tests. Preserve working Qeyvo capabilities and intentional customisations; implement only actual gaps. Do not rebuild completed features or introduce duplicate auth, queue, knowledge, billing or workflow systems. Do not replace Qeyvo’s working architecture merely to match a proposed design; justified material changes require an ADR and data-safe migration plan.
3. Establish baseline build, type, lint and test results using the checked-out project's actual scripts. Use disposable test databases. Inspect commands before running them; do not invoke volume-deleting shutdown commands against retained data.
4. Create or update the existing requirement ledger, Qeyvo baseline, Qeyvo gap matrix, dependency register, threat model, ADRs and dependency-ordered implementation plan. Treat the supplied JSON dependencies as a bootstrap graph to validate, not proof of current code structure. Start implementation after this baseline rather than ending with a plan.

## Implement the first complete vertical slice

Company setup → scoped users and space → approved knowledge → configured sales-administration teammate → authorised enquiry → grounded internal draft → exact-action human approval → certified external operation → independent result verification → correct usage/budget settlement → recoverable history.

First test which parts of this slice already work in Qeyvo; preserve them and implement only unmet requirements. Complete or verify tenancy, policy and budget contracts before enabling new external actions. Then expand through the remaining workstreams in the PRD. Keep changes focused, testable and migration-safe. Coordinate shared schema/contracts when using multiple implementation agents.

## Non-negotiable constraints

- Use **Qeyvo** as the product identity in documentation, interfaces, progress reports and handoff materials. Do not introduce another product name or comparison narrative.
- The product name is **Qeyvo**. Set the canonical brand value accordingly, reuse existing Qeyvo identity/assets/design tokens, and fix only remaining branding inconsistencies. Do not ask for a name again. Verify actual domain, legal entity and contact configuration instead of inventing them. Preserve applicable third-party licence and attribution notices in the appropriate code/legal locations; do not blindly rename database fields, storage paths, encryption settings, published native app identifiers or update channels.
- Preserve retained Qeyvo users, organisations, access grants, agents, workflows, conversations, files, credentials, billing state and public contracts wherever they exist. Do not assume a blank database or require existing users to recreate accounts. An unsafe capability must be restricted through a documented, appropriately authorised change rather than silently retained or destructively replaced.
- Do not rewrite the core stack solely for preference. Reuse Qeyvo’s existing compatible interfaces and implementation; verify proposed paths, assumptions and findings in the current Qeyvo checkout before assigning changes.
- Enforce tenant/resource permissions and current revocation on every API, job, retrieval, credential, file, stream and action path.
- Do not let browser, shell, custom tools or delegated agents bypass a denied operation. Disable unmediated production modes rather than pretending a prompt makes them safe.
- Bind approvals to exact actions. Changed inputs, destinations, policies or authority invalidate approval.
- Use durable task/effect state, idempotency and reconciliation. Never blindly retry an uncertain non-idempotent external action.
- Enforce atomic budgets and aggregate tool/time/delegation limits across the whole task tree. Never silently pool consumer subscription accounts as commercial API access.
- Do not send real customer emails, move funds, buy infrastructure, accept vendor terms, publish software, rotate live secrets, destroy data or deploy production changes without specific authorisation.
- Do not invent credentials, legal entities, brand clearance, live provider access, benchmark results, certification, customer savings or test evidence.
- Complete English/French coverage and accessibility for each released surface.
- Do not fix failing tests by removing security, quotas, error handling or meaningful assertions.

## Handle unresolved decisions without stalling

Use the PRD defaults for reversible development choices. Implement adapters and truthful test doubles where live credentials are missing, mark live validation `BLOCKED_EXTERNAL`, and continue independent work. Request only a genuinely necessary owner decision at the relevant action gate. Never claim an emulator passed a real integration test.

## Required evidence and completion

For each requirement record its status, changed code, tests executed, actual results, remaining risks and any external blocker. Use `IMPLEMENTED_UNVERIFIED` when appropriate and `VERIFIED` only after the specified evidence exists. The supplied register starts at `NOT_ASSESSED`, not “everything is missing.” Merge it into existing tracking without erasing completion evidence. Use `NOT_STARTED` only after confirming a missing implementation. Preserve credible `VERIFIED` records, re-run affected regression tests, and record gaps explicitly.

Maintain the artefacts specified in Section 34, including `qeyvo-baseline.md` and `qeyvo-gap-matrix.md`. Run the acceptance scenarios and the relevant security, performance, migration and recovery tests. Numeric targets in the PRD are targets to prove, not results to repeat as claims. Keep marketing and feature flags aligned with tested capability.

At each meaningful milestone report:
**Completed IDs; changed modules; tests actually run/results; risks; external blockers; next dependency-ready work.**

At a session boundary, leave a precise resume point. Do not mark unfinished work complete or imply background work continues when it does not.

Begin now with WS-00 in the existing Qeyvo checkout, then implement the first dependency-ready unmet requirements. If the first slice is already complete, verify it and continue to the next real gap. Deliver actual code and verification evidence within the authorised development environment; retain all production and commercial authorisation gates.
