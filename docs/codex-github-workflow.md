# Codex + GitHub Workflow

Use this workflow to keep agent-assisted changes small, safe, and easy to
review.

## 1. Create a bounded issue

Open an issue before starting work. State the objective, the files or sections
in scope, observable acceptance criteria, and guardrails. A good issue asks for
one coherent change rather than a catalogue-wide rewrite.

## 2. Work on a dedicated branch

Create a branch from `main` named `codex/<work-item>`, for example
`codex/issue-42-check-links`. Keep the branch focused on that issue and inspect
the diff before each commit.

`origin` is this repository's GitHub remote. `upstream` is the public VoltAgent
source used only to compare or selectively bring in upstream changes; it is
configured with no push destination.

## 3. Apply the repository guardrails

Read `AGENTS.md` and `CONTRIBUTING.md` before editing. Do not run code from
linked skills, install third-party packages, add credentials, or introduce
private URLs without explicit approval. Check public source links and keep
catalogue entries concise and in their proper category.

## 4. Verify and open a pull request

Before opening the PR:

- confirm that the issue's acceptance criteria are met;
- confirm the diff contains no unrelated edits;
- run the relevant local checks, or state why no automated check applies;
- summarize validation and any source or security caveats in the PR.

Use the pull-request template and reference the issue with `Closes #<number>`.
Merge only after a human reviews the change and the GitHub workflow passes.
