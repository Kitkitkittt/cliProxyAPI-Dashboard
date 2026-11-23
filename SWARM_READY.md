# Swarm-ready handoff

Repository: `Kitkitkittt/cliProxyAPI-Dashboard`. Contract: `swarm-ready/v1`. Source inspection: 2026-11-23.
Default branch: `main`. Inspected base: [af6a73fa46c7](https://github.com/Kitkitkittt/cliProxyAPI-Dashboard/commit/af6a73fa46c73f4796d440e7ad7950978b37d086).

**Status: documented; runtime qualification is unverified.** This file defines an agent workflow. It does not install a shell command, enroll the repository in a scheduler, certify test success, or activate VMs. Follow the current user task and existing repository instructions; retain prior authorization within its actual scope.

## Invoke

Give the working agent this prompt:

```text
swarm ready: <one measurable repository objective>
Read SWARM_READY.md and CONTRIBUTING.md. Continue the current owned
work or ready issue, establish the baseline and acceptance check, then prepare
a bounded worker handoff. Use existing authorized tools and capacity. Report
what is documented, implemented, tested, and observed separately.
```

If a `swarm-ready` skill is installed, load it. Otherwise execute the documented workflow directly. Treat the phrase as an agent instruction unless the installed CLI explicitly advertises it. Inspect help/version before using optional command adapters.

## Repository starting point

Read [CONTRIBUTING.md](CONTRIBUTING.md), [README.md](README.md), and the [Dashboard guide](docs/DASHBOARD.md). Continue the existing fork PR or scoped work order when fork issues are unavailable. For a new slice, record the outcome and verifier before editing. Do not treat an upstream issue as a fork work order.

Start with one writer. Add workers only for disjoint changes or independent experiments whose results can be checked separately. Keep shared interfaces and final integration with one owner.

The base above is an inspection snapshot, not a permanent working branch. Refresh the actual target branch, current issues, incumbent worker and applicable nested instructions before editing. Preserve unrelated changes and upstream/fork boundaries.

## Execution logic

1. **Recover context.** Read the current issue, work order and last evidence-backed handoff. Keep useful work and the active worker. Record source commit, unresolved criteria and the next action; avoid repeating completed investigation.
2. **Define success.** State one outcome, baseline, target, changed paths, verification command and expected result. Keep acceptance criteria and reference data fixed unless the user changes the requirement.
3. **Bound the attempt.** Reuse the existing owner/task/attempt identities, action scope, resource limits, time/cost budget and retry allowance. Do not demand a new user-written permission receipt for already authorized work. If a real capability or grant is missing, name the exact blocked action and continue independent work.
4. **Partition only useful work.** Use one writer per branch/worktree and non-overlapping change scope. Reuse the existing task ledger and dependency graph. Reserve verification capacity before adding workers; avoid recursive worker growth and duplicate coordinators.
5. **Implement and measure.** Make the smallest coherent change. Use differential checks when a trusted reference exists, and deterministic failure simulation when it materially improves reproduction. Record the seed/configuration and counterexamples. Do not weaken tests, rewrite baselines or hide pre-existing failures to claim success.
6. **Verify and integrate.** Verify the exact returned commit independently in a clean environment. Recheck the final integrated revision when changes interact. Follow existing review, merge and deployment rules; a green worker report alone cannot override them. Use the narrowest checks that resolve a concrete risk.
7. **Checkpoint and finish.** Save candidate SHA, evidence, measured outcome, remaining blockers and a precise next action before context/lease expiry. Reconcile lost or duplicate completions before retrying. Release only the run's owned resources after preserving evidence. Stop when the requested outcome is met or a concrete blocker prevents the next required action.

## Offline setup and verification

For docs-only work, start at the repository root with Git. Set `base` to the agreed review-base SHA. Confirm scope with `git status --short` and `git diff --name-status "$base"`, check paths with `git ls-files --error-unmatch -- README.md CONTRIBUTING.md SWARM_READY.md go.mod cmd/server/main.go static/management.html .github/workflows/pr-test-build.yml`, resolve the changed relative links and headings locally, and require `git diff --check "$base"` to pass. No dependency install, build, or proxy instance is needed.

For separately authorized source work, [go.mod](go.mod) declares Go 1.24.0, and [the contributor setup](CONTRIBUTING.md#running-locally) uses `go mod download` from the root. Read the [server entry point](cmd/server/main.go) or the [tracked Dashboard HTML](static/management.html) for the scoped surface; there is no declared Node package install for the Dashboard in this checkout.

The [PR build definition](.github/workflows/pr-test-build.yml) uses the module toolchain and compiles `./cmd/server`. It does not run the `go test ./...` command listed in [Running Tests](CONTRIBUTING.md#running-tests). These are source declarations, not proof of workflow registration, successful builds, or live authentication, client, or provider behavior.

## Required handoff result

Return a concise record with `repository`, `objective`, `issue_or_work_order`, `base_sha`, `candidate_sha`, `owner`, `task_id`, `attempt_id`, `worker/session`, `branch/worktree`, `changed_paths`, `environment`, `resource/budget limits`, `acceptance`, `commands_and_results`, `evidence_refs`, `known_failures`, `blocker_owner`, `next_action`, and `cleanup_status`. Use null/unknown when a field is unavailable; never manufacture evidence or authority.

Keep documentation readiness, command availability, source tests, live environment qualification and accepted outcome as separate states. Count verified outcomes, regressions, elapsed time, cost and human interventions. Commits, lines, tokens and worker count describe activity only.
