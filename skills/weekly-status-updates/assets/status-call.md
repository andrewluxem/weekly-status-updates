# Status call

The color is the only part of an update most readers act on, and it is the part
most often called wrong, in one direction: toward green. Work the tests in
order and take the first that fires.

## The tests

**Complete.** Every part of the goal is done. Requires a completion date. Not
usable while anything remains open, however small.

**Complete late.** Every part of the goal is done, and it finished after the
original date. Requires the completion date, and the original date stays visible
beside it. Do not quietly restate the original date as the one that was met.

**Did not meet.** The date has passed and all or part of the goal was not
achieved. Written DNM. This is a status, not a failure to report; a goal that
silently rolls into next week without ever being called DNM is how a project
runs a year behind on paper it never wrote.

**Red.** At least one part of the goal will certainly miss the final date, even
though that date has not yet passed. Red is a prediction and it is allowed to be
made early. Requires a revised date, or an explicit note that the revised date
is not yet known and what has to happen before it can be set.

**Yellow.** At least one part of the goal is not on schedule and that adds
significant risk to the final date. Requires a revised date if one is known.

**Green.** Every part of the goal is on schedule, and every dependency has been
identified and scheduled. Both halves are required. A project whose own work is
on time but whose dependency has no date is not green, and this is the single
most common miscall: the dependency is somebody else's problem right up until it
is the reason the date moved.

## When it is not clear

If you cannot tell whether a dependency is scheduled, it is not scheduled, so
the project is not green. Unknown resolves downward, because the cost of a
yellow that turns out fine is a question, and the cost of a green that turns out
red is a plan somebody else built on it.

If the inputs do not say enough to call the status at all, write
`Status: call needed` and name in one line exactly what has to be known to make
the call. Do not average the evidence into yellow to avoid the question.

## What the call carries

| Status | Requires |
|---|---|
| Green | Nothing beyond the goal date, and every dependency scheduled |
| Yellow | Revised date if known |
| Red | Revised date, or what has to happen before one can be set |
| Complete | Completion date |
| Complete late | Completion date, with the original date still shown |
| Did not meet | What was and was not achieved |

## One line of justification

Every call carries one sentence saying what drove it, naming the specific part
of the goal that is off schedule rather than the project's general condition.
"Yellow because the vendor integration has no start date and it gates the launch
sequence" is a call. "Yellow because there is some risk" is a mood.
