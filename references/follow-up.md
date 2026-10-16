# Finding follow-up and minimal checkpoints

Follow only actual human replies to your finding or new commits plausibly addressing your finding, within the owner's authorized follow-up scope. Ignore your own comments, reactions, edits, and automation echoes as triggers. A new commit alone does not authorize another broad review.

Start a fresh isolated verifier with item/head, the canonical finding, relevant human reply or fix diff, and necessary local context. Check the original trigger against the new head, affected paths, and tests. Distinguish fully fixed, partly fixed, unchanged, disproven, and blocked; never infer a fix from the author's claim or green unrelated CI.

Resolve only your own actual review thread when the entire finding is demonstrably fixed and resolution is authorized. Verify thread identity/ownership and current head immediately before resolution. An issue comment is not a resolvable PR thread. Do not resolve someone else's thread or mark a partial/untested fix complete.

Correct your own material errors with a dated clarification on the canonical comment/thread. Preserve the original evidence and explain what changed; do not silently erase or delete it. If the root cause remains, update the same finding rather than posting a duplicate. Editing others' content is never part of this workflow.

Checkpoint only what is needed for idempotency and continuation:
- Repository/item IDs and canonical item URL; event ID/hash and reviewed base/head
- Outcome, coverage/test status, and publication status (including uncertain)
- Finding IDs/root-cause fingerprints, canonical own comment/thread IDs, status, and last verified head
- Own reaction IDs/targets and content hashes; material correction dates

Do not store credentials, full emails, unrelated source content, private conversation history, or unnecessary personal data. Content hashes are for deduplication, not substitutes for live authorization/head checks. Reconcile live state before each write, including after restart. A duplicate event at the same head with no meaningful new human input should produce no duplicate review or publication.

A stale pass reaction may be mistaken for current validation. If a later authorized finding check invalidates your own earlier pass, report that mismatch and remove only your own stale reaction when removal is authorized; do not treat a new head as passed or alter others' reactions.
