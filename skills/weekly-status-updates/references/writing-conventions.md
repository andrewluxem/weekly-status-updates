# Writing conventions

The language and formatting contract for a weekly project status update. Read at
the drafting step of Mode A and at the numbers and voice sections of Mode C.

## Written for a phone

Assume the reader is on a phone, between two other things, and has not thought
about this project since the last update. That assumption decides most of the
formatting: the status near the top, short paragraphs, bullets that carry their
detail rather than pointing at it, and no table wider than a few columns.

It also decides the overview, which is the section authors quietly stop writing
around week six because everyone involved already knows. Everyone involved is
not the audience. The stakeholder who missed a month is, and rewriting three
lines each week is what lets them act on the update instead of asking someone
what it means.

## Numbers

State both sides of a change and the unit. "Signups moved from 1.2k to 1.5k,
+25% WoW" survives being forwarded; "signups are up nicely" does not.

Millions are MM and thousands are k, with no space before the unit. Never write
a figure that was not in the inputs; an estimate placed in a status update
becomes the baseline the next update is measured against.

## Dates

Dates are mm/dd/yyyy. Vague time references do not survive: next week, soon,
shortly, end of month, in the coming weeks. Each becomes an exact date from the
inputs, or a labeled gap. "Next week" is the phrase that lets a date slip
without anyone noticing, because it is true again seven days later.

A week number fixes a date range. Weeks run Monday to Sunday and are numbered
ISO, so WK31 of 2026 is 07/27/2026 through 08/02/2026 and its week-ending date
is 08/02/2026. A week-ending date that is not the Sunday of the week it sits
beside is a defect regardless of which of the two was supplied, and an
internally inconsistent title is worse than a labeled gap because the reader
cannot tell which value to trust. Derive the one that was not supplied rather
than assuming it, and never assume against the one that was.

Quarters derive from the date, not from the week number's neighborhood.
04/06/2026 sits in the second quarter, so its period is 02-2026.

## Progress against the plan, not against effort

"We worked on the migration" reports effort. "The migration is 3 of 5 stages
complete, with stage 4 due 08/14/2026" reports position. A reader cannot act on
effort, and an update built from effort reads as busy right up until the date
is missed.

The same applies to the highlights section. What was completed, and what was
learned, both count. What was attempted does not.

## Voice

Active voice. Cut weasel words: significantly, substantially, various, several,
a number of, fairly, quite, arguably, it was decided. Josh Bernoff's *Writing
Without Bullshit* is the reference Andrew's playbooks lean on for this.

Say the consequence, not just the event. A slipped dependency matters because of
what it gates, and the reader does not necessarily know what it gates.

## Links belong here

A status update points outward. The reader who wants the detail follows a link
to the board, the dashboard, or the spec, and the update stays short because of
it. Label each link with what the reader will find rather than with the name of
the tool it lives in.

This is the convention that differs from a 4-block business review, which stands
alone with no outbound links because it is read inside a meeting rather than on
a phone. Do not carry that habit across in either direction.
