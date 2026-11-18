# GitHub publication contract

Immediately before EACH write, verify:
1. The authenticated account's stable ID equals the configured bot account and the operation is authorized.
2. The exact live repository, item, head SHA, original body/thread target, and current ownership match the reviewed evidence.
3. Live comments, reactions, and checkpoint state show no already-applied equivalent action. Check finding identity by root cause and location, not wording alone.
4. The content is still correct, audience-safe, and relevant. Re-read a human-edited thread before replying or resolving.

Any failed gate stops that write. A moved head invalidates publication of the old review result, including a heart. Revalidate only the authorized scope in a fresh reviewer; do not silently launch a broad new-commit review. If needed, ask for expanded scope. Re-check again immediately before publishing the revalidated result.

## Findings

For PRs, use an inline review comment tied to the reviewed commit and the smallest relevant changed line range. Submit only COMMENT review events. Never APPROVE or REQUEST_CHANGES. If the tool cannot address the correct commit/line or cannot guarantee COMMENT, stop and report that limitation rather than moving the finding to a misleading location.

For an eligible issue, use an ordinary issue comment only for a verified factual error, reproduction difference, or concrete proposal defect. Include a stable evidence reference rather than inventing a diff line.

Suggested body (fill only supported details):

```
[P2] Short actionable title

When <specific trigger>, <actual behavior> causes <concrete impact>.
<Brief evidence and expected behavior, bound to the reviewed head.>
Tests: <actual status and relevant command/result>.

<details>
<summary>Suggested fix</summary>

<Concrete direction; distinguish a tested fix from an untested proposal.>

</details>

<configured attribution>
```

Use the configured attribution exactly. Keep one canonical own comment/thread per distinct finding. Do not repeat it on every event or across multiple comment types. For substantive follow-up results caused by new progress or discussion, append a new reply to that thread instead of editing an old report; use a new COMMENT review for a distinct finding/round when appropriate. Keep the earlier report and its head/evidence intact. A canonical finding may have multiple chronological replies, but not repeated equivalent reports. Reserve edits for correcting the same output. Each new reply must add meaningful authorized evidence or a verified status change, not another summary of the same finding.

## No qualifying finding

For validated_pass only, add a heart to the original PR/issue body if that reaction is authorized and absent. Do not leave a routine pass comment or review approval. This does not suppress an authorized new reply reporting a substantive follow-up on an existing finding, such as verification of a fix prompted by new commits or discussion; follow the chronological-reply rules in follow-up.md. Incomplete results get neither a heart nor a speculative finding/comment; privately surface an actionable blocker as configured.

Read back every write to verify the target and resulting content/reaction. Capture returned stable IDs. Successful API acceptance alone does not prove the intended object changed. If verification fails, mark publication uncertain and reconcile without a duplicate write.
