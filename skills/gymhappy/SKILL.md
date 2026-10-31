---
name: gymhappy
description: Use when a gym owner asks about their GymHappy account - review performance and trends, coach reviews, review-request fatigue, message delivery, setup checklist, monthly highlights, member lookups, or changing GymHappy gym, messaging, coach or member settings.
---

# Working with GymHappy

GymHappy is a reputation and member-engagement product for PushPress gyms on the Grow Pro plan. The GymHappy MCP tools act on the gym that the signed-in user can access. Use them to answer questions with real data from that gym.

## Pick the right tool

| The owner asks about | Tool to use | Notes |
| --- | --- | --- |
| Review totals, average rating, trends over time | `get-analytics` | Pass `from_date` and `to_date` as `YYYY-MM-DD`, and `group_by` (`day`, `week`, or `month`) when they want a breakdown |
| Which coaches can receive reviews | `get-coaches` | No arguments needed. Report `coach_count` as returned |
| Whether members are tired of review requests | `get-review-fatigue` | Pass `days_back` for the window they named (for example `90`) |
| What is left to set up | `get-setup-checklist` | No arguments. Report incomplete items using their status and context |
| Monthly highlights | `get-monthly-highlight` | Use `list=true` for history |

For member searches, message delivery, and settings changes, use the GymHappy tool whose title matches the request. Read each tool's description and input schema before calling it.

## Dates

- Turn relative ranges ("last month", "this quarter", "since Labor Day") into explicit `YYYY-MM-DD` dates using today's date, and state the range you used in your answer.
- If the owner gives no range for a trend question, use the last 30 days and say so.

## Reporting results

- Report only what the tools return. Never invent ratings, counts, names or trends to fill gaps. If a value is missing or a list is empty, say so plainly.
- Lead with the answer (for example "Average rating was 4.8 across 42 reviews in September, up from 4.6 in August"), then the supporting breakdown.
- For review fatigue, describe what the conversion and repeat-request numbers show without claiming they prove a cause.
- Keep member personal details to what the owner needs for the task at hand.

## Changing settings

- Read-only questions never need a write tool. Don't change settings while answering a question.
- Before a change, confirm exactly what will change (which setting, coach or member, old value and new value) unless the owner already stated it precisely.
- After a change, report what the tool confirmed. If it returned an error, say what failed and don't claim success.

## Out of scope

GymHappy can't charge members or process payments, book or cancel classes, or delete reviews from Google Maps or other review sites. When asked, say GymHappy doesn't support it and don't call a GymHappy tool. For billing and class scheduling, point the owner to PushPress.

## Access problems

If a tool reports that the account isn't eligible or has no gym access, explain that GymHappy requires a PushPress Grow Pro account with access to the gym in GymHappy, and point them to https://app.gymhappy.co/support.
