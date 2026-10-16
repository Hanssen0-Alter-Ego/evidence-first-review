# Runtime adapters and capability requirements

The core defines review decisions and evidence standards. A runtime adapter maps those requirements to a host's available tools; this package ships no executable adapter. Do not assume that a skill format supplies tools, isolation, credentials, storage, or authorization.

## Read-only review

Required: load the entrypoint and relevant references; read the scoped change, exact base/head refs, surrounding source, requirements, and discussion. Return findings and coverage limits to the authorized requester. A host without source/ref access can discuss a supplied excerpt but cannot claim an exact-head repository review.

Independent verification additionally requires a fresh worker or process with only the allowed review context and no remote write capability. If unavailable, disclose the lack of independence rather than simulating a second reviewer or claiming isolation.

Tests require a safe execution environment. Browser evidence requires a browser, a verified preview/build-to-head relationship, and authorized interactions. If missing capabilities leave a material evidence gap, use the incomplete outcome; do not invent results. A demonstrated finding may still be returned alongside coverage gaps.

## Optional GitHub publisher

Keep the verifier read-only. An authorized publisher must independently establish the authenticated account's stable ID, live repository/item/head, target ownership, duplicate state, and permitted operation. Its tools must support the exact commit and changed-line range, COMMENT-only reviews, and read-after-write verification. If they cannot, retain the review result without publishing. A generic text box or access token alone does not satisfy this contract.

Use the host's credential and approval mechanisms. Do not include credentials in prompts or configuration. Browser, API, CLI, or connector choices are adapter details and do not relax [publication gates](github-publishing.md) or [trust boundaries](boundaries.md).

## Optional follow-up

Follow-up needs durable minimal finding/checkpoint IDs and a live read path for current commits and human replies. Resolution additionally needs own-thread identity and a supported resolution operation. Apply only the owner's authorized follow-up scope. A scheduler or event collector is separate and must not be created merely because this skill is loaded.

## Host-specific setup

- A host that understands `SKILL.md` folders can discover this package through its supported installation mechanism.
- A different agent can read the entrypoint and relevant references as instructions when its own rules allow that; verify capabilities individually.
- Product names, selected models, account IDs, destinations, tool mappings, attribution, and schedules belong in private deployment configuration. The optional dot attribution example in [configuration](configuration.md) is not a core dependency.

Do not claim compatibility with every agent. Record which capabilities were actually available and tested in the chosen deployment.
