# weekly-status-updates

A small, static agent skill for the weekly project status update. Ask it for one thing and it hands back a working document, not advice about reporting.

Three artifacts:

- **Weekly Status Update**: what one stakeholder needs on a phone, between other things. What the project is for, whether it will land on time, and what would change that. Position against the plan, never effort.
- **Status Call**: the color underneath the update, worked through the tests in order, with the dates that color commits to and one sentence of justification naming the specific part of the goal that is off schedule.
- **Draft Check**: an update scored line by line starting with the status call, with a verdict of ready to send, one pass needed, or not ready, and one sentence naming the single most important thing to fix.

It executes the [Weekly Status Updates playbook](https://andrewluxem.com/playbooks/weekly-status-updates) from andrewluxem.com. The playbook page teaches the framework. This skill runs it.

**Static by construction: no network calls, no remote fetch, no auto-update, nothing scheduled, no background behavior. Model-invocable by design: an agent may pick it up when you ask for a weekly status update or a project status, and naming the skill is the reliable path.** It reads nothing outside its own folder, never edits your global agent config, and never updates itself in place. The whole thing is one `SKILL.md` you can read in five minutes, plus templates and reference files it loads only when a step needs them.

## The loop

Pick the mode from what you asked for. Mode B sits inside Mode A, so a request for a full update runs the status call as part of it. Run Mode B alone when the color itself is the question, which is usually when someone suspects the answer is not the one they want.

| Mode | You bring | You get |
|---|---|---|
| **A. Write the update** | Project notes, last week's update, dates | Weekly Status Update |
| **B. Call the status** | Goal, dates, what is on and off schedule | Status Call with justification |
| **C. Check the draft** | A written update | Draft Check with a verdict |

The tests run in order and the first one that fires wins. Complete and did not meet are decided by the date and the work. Green, yellow and red are decided by the schedule and the dependencies.

What it refuses to shortcut, because these are the failure modes that turn an update into a green light nobody should have trusted:

- **Green is a claim about dependencies too.** Never green because the team's own work is on schedule while something it waits on has no date. This is the most common miscall and the one that costs the most, because the dependency is somebody else's problem right up until it is the reason the date moved.
- **Unknowns resolve downward.** If it cannot be established that a dependency is scheduled, it is not scheduled. The cost of a yellow that turns out fine is one question. The cost of a green that turns out red is a plan somebody else built on it.
- **No invented number, owner, or date.** An estimate placed in a status update becomes the baseline the next update is measured against. Missing values are labeled in position: `Owner: unassigned`, `Date needed`, `Figure needed`, `Link needed`. Arithmetic on supplied figures is welcome, and the line is whether a reader holding only the inputs could reach the same number.
- **A status without its required date is not finished.** Yellow and red carry a revised date, or an explicit note that it is not yet known and what has to happen before one can be set. Complete late still shows the original date beside the completion date.
- **When the inputs cannot support a call, it says so.** `Status: call needed`, naming in one line exactly what has to be known. The evidence is never averaged into yellow to avoid the question.
- **Effort is not progress.** Worked on, spent time on, and made progress on each become what completed, what stage it reached, or what it is waiting on, with the date. An update that reports effort reads as busy right up until the date is missed.
- **No artifact measures itself.** No count of items, no reading time, no note of how many gaps were labeled, inside the artifact or around it.

See [`examples/example-run.md`](examples/example-run.md) for a full Mode A pass, including the call that goes yellow while the team's own work is green.

## Install

**Manual (recommended, clone and copy):**

```bash
git clone https://github.com/andrewluxem/weekly-status-updates.git
cp -r weekly-status-updates/skills/weekly-status-updates ~/.claude/skills/
```

Then invoke it by name when you want it for certain: `use the weekly-status-updates skill to write this week's update`.

**As a Claude Code plugin (version-pinned, no auto-update):**

```
/plugin marketplace add andrewluxem/weekly-status-updates
/plugin install weekly-status-updates@weekly-status-updates
```

The skill lives under `skills/weekly-status-updates/`, which is where a plugin looks by default, so `plugin.json` declares no `skills` key. The frontmatter `name` field is what the skill is called once installed, whatever the install directory happens to be. `plugin.json` carries an explicit `version`. Installing pins that version. It does not silently pull new commits. Taking an update means bumping the version and reinstalling, so the update is a decision rather than a background event.

**As a zip:** the packaged skill is on the playbook page at [andrewluxem.com/playbooks/weekly-status-updates](https://andrewluxem.com/playbooks/weekly-status-updates), for platforms that want a folder upload instead of a clone. Same files.

Portable by design: it is plain Markdown with no runtime, so it works anywhere a folder of skill files works.

## Usage

```
Write the week 7 status update for the checkout redesign from these notes
Are we green or yellow? The build is on time but legal has not come back on the refund copy
Is this update ready to send to the stakeholder list?
```

Naming the skill is the reliable path: `use the weekly-status-updates skill to draft the update`. It has no background behavior and nothing scheduled, so nothing happens until a request goes to it.

## Where it hands off

`4-blocker-business-reviews` when the subject is a business area's full weekly picture with metrics and a recurring review meeting, rather than one project against one date. `3ps-framework` when the update is a person's or team's week in Progress, Plans and Problems. `successful-meetings` for the meeting the update might replace. `silent-meetings` when the update has grown into a document a room needs to read together.

## Iterating

The skill is the folder [`skills/weekly-status-updates/`](skills/weekly-status-updates/):

- `SKILL.md` is the procedure, and it is the only file loaded every time.
- `assets/` holds the update template, the status call tests, and the draft check.
- `references/` is the depth: the phone reader, numbers, dates, effort versus position, and a full worked update where the honest color is worse than the author's own work. Each is read only at the step that needs it.
- `meta.yaml` carries the version, the invocation examples, the three test prompts with the bar each has to clear, and the changelog.

Edit it, invoke it on a project you actually report on, and see whether the artifact earns its place. The bar is that the update would survive being forwarded without you attached to it.

The three prompts in `meta.yaml` under `test_prompts` are the regression suite. Each one records what a passing run looks like, so a change to the procedure can be scored against the same bar rather than a fresh guess.

When you change behavior meaningfully, bump `version` in both `.claude-plugin/plugin.json` and `meta.yaml` so plugin installs pick it up deliberately, and add the changelog line.

## Testing

Tested on Claude Code. The three prompts in `meta.yaml` were run against this version in an isolated rig, with the skill hash-pinned to the copy under test and the host's global instruction files suppressed, so a run that never loaded the skill fails visibly instead of returning a plausible answer. Other hosts are untested rather than unsupported.

## License

MIT, see [`LICENSE`](LICENSE). The skill folder carries the same MIT text in [`skills/weekly-status-updates/LICENSE.md`](skills/weekly-status-updates/LICENSE.md), so the whole repository is one license.
