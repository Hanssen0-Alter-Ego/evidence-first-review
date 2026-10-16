# Dot Review Skill

An instruction-only skill for evidence-based GitHub pull request and issue reviews. It separates independent verification from authorized publication, binds findings to an exact commit, and distinguishes a validated pass from incomplete evidence.

**Version:** 0.1.0 · **Status:** public source; no open-source license has been granted.

## What it does

- Tests suspicions against code, callers, requirements, and reproducible evidence.
- Returns verified findings, a scoped validated pass, or an honest incomplete result.
- Checks identity, commit, target, ownership, and duplicates before authorized writes.
- Follows up narrowly on existing findings and can verify UI behavior when appropriate.

It does not implement fixes, merge changes, create a schedule, or grant access. There are no executable scripts or bundled GitHub integration.

## Use locally

Review the [license status](#license-status) before reuse. The following describes technical setup for the owner or anyone with the necessary permission.

For Codex, clone the repository into a local skill folder:

```sh
mkdir -p ~/.agents/skills
git clone https://github.com/Hanssen0-Alter-Ego/dot-review-skill.git ~/.agents/skills/dot-review-skill
```

Alternatively, place the entire folder at `.agents/skills/dot-review-skill/` inside a project. Keep `SKILL.md`, `references/`, and the supporting files together. Invoke `$dot-review-skill` with a specific repository, PR or issue, and review scope. If it is not discovered, restart Codex. These locations follow the [official local-skills documentation](https://learn.chatgpt.com/docs/build-skills), checked on 2026-10-16.

Other agents must support `SKILL.md` folders or load the entrypoint and relevant references explicitly. Installation differs by host; this repository is not a universal installer or a published plugin.

Start read-only. Adapt [config.example.json](config.example.json) in private deployment configuration, resolve every placeholder, and keep `publish.enabled` false until exact operations and audiences are authorized. Never commit credentials or private configuration. Review updates before pulling them into an active setup.

## Files

- [SKILL.md](SKILL.md): short entrypoint and review outcomes
- [references/](references/): configuration, boundaries, GitHub publishing, browser evidence, and finding follow-up
- [config.example.json](config.example.json): non-operational deployment example
- [VALIDATION.md](VALIDATION.md): static and synthetic scenario checks, plus deployment checks still needed
- [SHARING.md](SHARING.md): provenance and source attribution

## Validation and limitations

The package passed structural checks and six independent synthetic decision scenarios. It has not been validated end-to-end against a deployment's live GitHub, browser, permissions, or checkpoint storage. Instructions are not runtime enforcement, a security audit guarantee, or proof that a reviewed change is free of defects. See [VALIDATION.md](VALIDATION.md) before enabling publication.

## Attribution

An original synthesis informed by OpenAI Codex's public review-agent example and Jesse Vincent's Superpowers review workflow. No upstream source files or substantial prose excerpts are redistributed. Their respective licenses and links are recorded in [SHARING.md](SHARING.md). This project is not an official OpenAI or Superpowers product.

## License status

No license is currently granted for this repository. Public availability does not itself grant permission to use, modify, or redistribute the package. Contact the repository owner for permission; the upstream projects' Apache-2.0 and MIT licenses do not apply automatically to this original package.
