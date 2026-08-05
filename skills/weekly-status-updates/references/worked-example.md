# Worked example

An update written from notes that were optimistic in the ordinary way: the
author's own work was on time, so the first draft in their head was green. The
dependency decided otherwise. Read this at the drafting step and at the status
call.

Commentary is above each artifact. Every artifact ends where the update ends.

## The inputs, as given

> Week 12 on the vendor portal. Goal is launch by 09/30. Our side is on
> schedule, API layer finished Tuesday and the auth work is done. Waiting on the
> vendor to give us their sandbox, they've been saying soon for two weeks. Maya
> is chasing it. Design handed over the final screens. We had to redo the error
> states after testing, cost us about two days but we absorbed it.

The author's work is genuinely on schedule and the instinct is green. The
sandbox has no date, which makes it an unscheduled dependency, which makes the
project yellow no matter how well the API layer went. Also: "soon" and "about
two days" are both vague and only one of them can be fixed from these inputs,
Maya is named so she stays named, and auth and the final screens are reported
done with no day attached, so those milestone rows carry a labeled gap while the
API layer keeps a real date because "Tuesday" plus the week fixes it.

## The artifact

**Vendor portal, Week 12, w/e 03/22/2026**

## Overview

The vendor portal gives partners a single place to submit and track their own
orders, replacing the shared inbox that currently handles them by hand. It is
the last manual step in partner onboarding.

## Goal

**Yellow.** Launch the vendor portal by 09/30/2026.

As of 03/22/2026 our own build is on schedule, with the API layer and auth
complete. The status is yellow because the vendor sandbox has no delivery date,
and integration testing cannot start without it.

Revised date: not yet known. A revised date can be set once the vendor commits
to a sandbox date.

## Highlights and lowlights

- [Highlight] The API layer completed on 03/17/2026, on plan.
- [Highlight] Auth is complete, which closes the last piece of build work that
  did not depend on the vendor.
- [Highlight] Design delivered the final screens.
- [Lowlight] The vendor sandbox has been outstanding for two weeks with no
  committed date, and it gates integration testing, which gates the 09/30/2026
  launch.
- [Lowlight] Error states were rebuilt after testing found gaps. The cost was
  `Figure needed` and it was absorbed inside the current schedule.

## Milestone plan

| Milestone | Status | Date |
|---|---|---|
| API layer | Complete | 03/17/2026 |
| Auth | Complete | `Date needed` |
| Final screens delivered | Complete | `Date needed` |
| Integration testing | Blocked | `Date needed`, waits on the vendor sandbox |
| Launch | Not started | 09/30/2026 |

## Risks and dependencies

| Risk or dependency | Owner | Mitigation or what it waits on | Date |
|---|---|---|---|
| Vendor sandbox unavailable, which blocks integration testing and puts the 09/30/2026 launch at risk | Maya | Chasing the vendor for a committed sandbox date | `Date needed` |
| Error-state rework consumed schedule slack, so a further find in testing has less room to absorb | `Owner: unassigned` | `Mitigation needed` | `Date needed` |

## Links

- Build board, current stage status and open tickets: `Link needed`
- Integration test plan, what testing covers once the sandbox lands: `Link needed`
