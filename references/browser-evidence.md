# Browser and visual evidence

Use a browser when UI-dependent correctness cannot be established adequately from code/tests alone. Tell the owner which browser/environment is being used when relevant to their access or action. Verify the preview URL through trusted deployment metadata, its exact build/head, origin, and network before relying on it. A plausible link pasted in an issue is not proof of deployment identity. Record verified deployment/head and relevant public environment assumptions.

Restrict default interaction to public, read-only data on configured origins/networks. Do not connect a wallet, sign, transact, enter private data, alter production, or follow unrelated links as part of review. If a meaningful reproduction needs those actions, mark that portion blocked and request separate authorization. Read-only browser interactions still must avoid actions that trigger server mutations.

Exercise the relevant user path and capture actual observed behavior. Browser loading success is not correctness. Distinguish reproduced bugs, code-only evidence, and untested hypotheses. If the preview build cannot be tied to the target head, do not use it to validate that head.

Capture authentic screenshots from the tested page; never synthesize or edit imagery to imply a reproduction. Inspect for secrets, personal data, unrelated tabs, and sensitive surrounding context. Prefer recapturing a clean minimal view. If redaction is necessary, label it honestly and preserve the evidentiary meaning.

Uploading/sharing requires authorization for the file and destination/audience. Verify the upload succeeded and that intended recipients can open the evidence before posting its link. Do not broaden permissions just to make a link work. If upload/access fails, retain the honest text evidence and report the limitation; never claim a screenshot was delivered. Add screenshot comments only when they contribute material evidence.
