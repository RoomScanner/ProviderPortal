# Contributing

These rules follow the course's teamwork requirements (Common Requirements, section 4). The marker checks the project board and the commit history, so the habits below are how we keep marks.

## Project board

Every piece of work, including design, reports and meetings, is an issue on the **Provider Portal** board in the RoomScanner organization. The board columns are the stages the course requires:

| Stage | What it means |
| --- | --- |
| Product Backlog | Every known feature, fix and technical task. Keep it prioritized. |
| Sprint Backlog | Picked for this sprint. From here on the task **must** have an assignee, a due date, an estimate and a Definition of Done checklist. |
| In Progress | Work has started. Comment on the issue if something will make it late. |
| Review | Done by the owner and waiting for the reviewer. Set the Reviewer field. The owner replies to each piece of feedback on the issue or PR before moving on. |
| Staging | Reviewed and merged. Check that it works with the rest of the subsystem and with Customer Portal. |
| Deployment | Running in the Docker deployment on the target machine. Skip for Milestone 1. |
| Done | Every Definition of Done box is ticked. |
| Documentation | Stand-up minutes, sprint reviews and API-contract records. |

Don't skip stages. A task that jumps straight to Done, or reaches Done with unticked boxes, counts as invalid, and invalid tasks must stay under 10% of everything moved to Done (TW-U02). The same 10% check applies to missing assignees, due dates and estimates.

### Board fields

- **Status**: the stage above.
- **Estimate**: effort in hours.
- **Due date**: the target date.
- **Reviewer**: the GitHub username of the person reviewing. It must be someone other than the owner.
- **Sprint**: the two-week sprint the task belongs to.
- **Priority**: P0 (blocking) to P2 (nice to have).
- **Level**: Simplex, Medium or Ultimo, for feature tasks.

## Stand-ups

Hold at least two stand-ups a week. Within 24 hours, open a **Stand-up minutes** issue, fill in each member's did, doing and blocked, and put it in the Documentation column. Also commit a copy under `docs/meetings/standups/YYYY-MM-DD.md`. If a blocker comes from Customer Portal, name it and say who is waiting; the lecturer reads these when integration slips.

## Sprint review and retrospective

At the end of each two-week sprint, open a **Sprint review** issue covering what was demonstrated, what worked, what didn't, risks and what changes next sprint.

## Branches

`main` is protected. Branch from it and open a pull request.

```
feat/<issue-number>-short-name     e.g. feat/12-provider-registration
fix/<issue-number>-short-name
docs/<issue-number>-short-name     e.g. docs/5-erd-v1
chore/<issue-number>-short-name
```

## Commits

Use [Conventional Commits](https://www.conventionalcommits.org/) and commit small and often. Graders look at contribution graphs, so one giant commit at the end hurts the whole team.

```
feat(rooms): archive deleted rooms instead of hard delete (#23)
fix(auth): count email and phone login failures together (#31)
docs(c4): add backend container diagram (#8)
```

Commit with the GitHub account listed in the README so your work is counted.

## Pull requests

1. Link the issue with `Closes #<number>`.
2. Request a review from the issue's Reviewer.
3. The reviewer leaves comments, and the owner answers each one, either with a change or a reason. This answer is the evidence for TW-M02.
4. Merge after approval and move the issue to Staging.

## Definition of Done

Each task carries its own checklist. Most tasks need at least:

- [ ] Meets the requirement IDs listed on the issue
- [ ] Tested (unit or manual test steps written on the issue)
- [ ] Reviewed by the assigned reviewer, with every comment answered
- [ ] Merged to `main` and checked in staging
- [ ] Included in the Docker deployment (Milestone 2 only)
- [ ] Docs and API contract updated if behaviour changed

## If someone falls behind

First, give them a smaller task that can be done within 48 hours. If that doesn't come back at acceptable quality, tell the course coordinator straight away. The coordinator acts on reported cases within 48 hours.
