# Example run

One Mode A pass, from a handful of project notes to the update. The notes are incomplete on
purpose: one milestone is done with no date attached, and the dependency that decides the
color has no date at all. Nothing here is invented to fill those gaps.

This is a real run of the packaged skill, not a hand-written illustration.

## What was asked

> Write the week 7 status update for the checkout redesign, week ending 02/15/2026. Goal is
> to ship the new checkout by 04/30/2026. Payment integration finished 02/11 and cart logic
> is done. We are waiting on legal to approve the refund copy, Tom is chasing it, no date
> yet.

## What came back

```
**Checkout Redesign, Week 07, w/e 02/15/2026**

## Overview

The Checkout Redesign replaces the current checkout flow with a rebuilt experience covering
cart management, payment processing, and refund handling. The goal is to deliver the new
checkout by 04/30/2026.

## Goal

**Yellow.** Deliver the new checkout by 04/30/2026.

As of 02/15/2026, payment integration and cart logic are complete. Legal approval of the
refund copy has no scheduled date, and that approval gates the remaining work before the
checkout can ship. Revised date: not yet known; can be set once legal confirms the approval
date.

## Highlights and lowlights

- Payment integration complete as of 02/11/2026.
- Cart logic complete as of Date needed.
- Legal has not confirmed a date for refund copy approval; the 04/30/2026 ship date cannot
  be confirmed until it does.

## Milestone plan

| Milestone | Status | Date |
|---|---|---|
| Payment integration | Complete | 02/11/2026 |
| Cart logic | Complete | Date needed |
| Legal approval, refund copy | Blocked | Date needed |
| Ship new checkout | Not started | 04/30/2026 |

## Risks and dependencies

| Risk or dependency | Owner | Mitigation or what it waits on | Date |
|---|---|---|---|
| Legal has not approved refund copy; checkout cannot ship until it does | Tom | Tom is chasing legal for a confirmed approval date | Date needed |

## Links

- Link needed
```

## What to notice

- **It calls yellow when the team's own work is green.** Payment integration and cart logic
  are both done and nothing the team owns is late. The color is yellow anyway, because
  legal approval has no date and green is a claim about dependencies too. This is the
  single most common miscall, and it is the one that costs the most.
- **The week and its date agree.** Week 7 of 2026 ends Sunday 02/15/2026. A week number
  fixes a date range, so the update takes its week-ending date from week 7 rather than from
  whatever week it happens to be run in.
- **The revised date says what has to happen.** Not yet known, plus the condition that
  would let one be set. Yellow without a revised date, or without an explicit note that one
  is not yet known, is an unfinished status.
- **Cart logic is complete with `Date needed`.** The notes said it was done and never said
  when. The milestone stays Complete, which is what the notes support, and its date is
  labeled rather than borrowed from the week or from the payment integration date beside
  it.
- **Tom stays where the notes put him.** He owns the dependency because the notes said he
  was chasing it. Nobody else is assigned, and no job function stands in as an owner.
- **The justification names the dependency, not the mood.** "Legal approval of the refund
  copy has no scheduled date" rather than "the project is at risk". A stakeholder can act on
  the first one.
- **The update stops at the links list.** No closing summary, no count of open fields, no
  offer to revise. This is an email someone forwards, and a note attached to the top of it
  travels with it.

## Then the human does the part that is theirs

Get legal to commit to a date, fill in the cart logic completion date, and add the real
links. The skill drafts and refuses to guess; the color and what it commits to stay with
the person sending the update.
