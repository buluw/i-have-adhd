<p align="center">
  <img src="./logo.png" alt="i-have-adhd-codex" width="140" />
</p>
<p align="center">
  <strong>ADHD-friendly + Focused Coding Execution for Codex</strong>
</p>

# i-have-adhd-codex

This is the `codex-personal` branch of [buluw/i-have-adhd](https://github.com/buluw/i-have-adhd), maintained only for personal Codex use. The fork's `main` stays close to [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd) for upstream sync.

The plugin keeps the useful ADHD-friendly behavior from upstream while making Codex finish the current coding task with the smallest sufficient implementation and targeted validation.

## Install

```bash
codex plugin marketplace add buluw/i-have-adhd --ref codex-personal
codex plugin add i-have-adhd-codex@i-have-adhd-codex
```

Start a new Codex task, then invoke the skill with `$i-have-adhd`.

See [INSTALL.md](INSTALL.md) for verify, update, and uninstall commands.

## Behavior

- Lead with the current action or result.
- Keep the goal, current work, blockers, and completed work visible without process noise.
- Continue autonomously when no user decision or authorization is required.
- Suppress tangents and record non-blocking issues without expanding them.
- Reuse existing capability after one targeted duplicate check.
- Prefer minimal code and targeted validation, then stop when the requirement works.
- Stop blind trial and error after three consecutive failed fixes and re-check the underlying assumption.

The full behavior is in [skills/i-have-adhd/SKILL.md](skills/i-have-adhd/SKILL.md).

## Sync upstream

Keep the fork's `main` aligned first, then merge it into the personal branch:

```bash
git fetch upstream
git switch main
git merge --ff-only upstream/main
git push origin main
git switch codex-personal
git merge main
git push origin codex-personal
```

Resolve conflicts only in `codex-personal`; do not add personal changes to `main`.

## Credits

Based on [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd). Licensed under the [MIT License](LICENSE).
