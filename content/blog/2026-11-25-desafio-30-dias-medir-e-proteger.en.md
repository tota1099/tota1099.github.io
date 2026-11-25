---
title: "30-day challenge: what five weeks of my calendar showed me"
slug: 30-day-challenge-measure-and-protect
date: 2026-11-25T14:00:00-03:00
description: "The numbers from five weeks of measuring my calendar by category, why I didn't follow the protect step, and what the data actually showed."
categories:
  - Organization
  - Lifestyle
tags:
  - google-calendar
  - productivity
  - time-management
  - 30-day-challenge
---

In the [previous post](/en/2026/10/22/30-day-time-management-challenge/) I started the 30-day time management challenge, inspired by the talk "Time is attention". The first step was to **measure**: give each type of activity a color in Google Calendar and, only after seeing the reality, decide where I want my hours to go. The second was to **protect**: reserve focus blocks in advance, instead of logging them after the work had already happened.

This post brings the numbers and an honest assessment of both steps.

## What changed along the way

The plan was to measure for two weeks and publish. I ended up measuring for five, from Oct 25 to Nov 25, for no special reason: I simply didn't stop to write the post. In the end it was a good thing, because five weeks show a trend and two wouldn't.

Three new categories showed up in the first few days, because the original eight didn't cover what I actually did:

- 🔁 **Company rituals**, separate from team rituals
- 🗓️ **Planning**, which used to be scattered across rituals and leadership
- 👀 **Document review**, separate from code review

And one category turned out to be useless: 🚨 **Support** got only 1.6 hours in five weeks, because we simply had no support requests during the period. I'm going to remove it. The first version of any categorization is wrong, and only using it shows you where.

## The numbers

Hours logged per week, not counting the Personal category:

| Category | Oct 25–31 | Nov 1–7 | Nov 8–14* | Nov 15–21 | Nov 22–25** |
|---|---:|---:|---:|---:|---:|
| 🔨 Development | 11.0 | 10.5 | 4.3 | 16.0 | 14.8 |
| 🔁 Team rituals | 7.3 | 4.0 | 5.8 | 4.5 | 3.0 |
| 🔁 Company rituals | 0 | 0.8 | 0 | 1.5 | 0 |
| 👀 Code review | 4.8 | 3.8 | 2.5 | 7.0 | 1.5 |
| 👀 Document review | 1.0 | 1.0 | 0 | 0 | 0 |
| 🗓️ Planning | 2.8 | 2.5 | 5.3 | 2.0 | 2.0 |
| 🧭 Leadership and people | 3.8 | 1.3 | 1.0 | 0.8 | 0.5 |
| 📚 Learning | 2.5 | 0.8 | 0 | 0 | 0.8 |
| 🚨 Support | 1.3 | 0.3 | 0 | 0 | 0 |
| ✅ QA and validation | 0.5 | 0 | 0 | 0.8 | 0 |
| **Total work** | **35.0** | **25.0** | **18.9** | **32.6** | **22.6** |
| **% in development** | 31% | 42% | 23% | 49% | 65% |

\* A week when I wasn't feeling well and ended up not managing my calendar. Its numbers are here for transparency, but they're left out of the analysis.
\*\* Week in progress: Monday to Wednesday only.

The totals below 40 hours have two explanations: weeks with a public holiday and the week when I wasn't feeling well.

Adding up the four valid weeks, I logged 115 hours of work. Development took 52 (45%), rituals 21 (18%), code review and document review 19 (17%) and planning 9 (8%). Leadership and people added up to 6 hours (6%) and learning to 4 hours (4%).

## What the numbers show

**Development gained ground.** The share of coding went from 31% in the first week to 49% and 65% in the last two. In just the first three days of this week, it was already almost 15 hours.

**Meetings shrank.** Team and company rituals dropped from 7.3 hours to 3 hours per week.

**The important-but-not-urgent disappeared.** This is the number that bothered me the most. Learning went from 2.5 hours in the first week to zero in the week of Nov 15, and only showed up again today: it's the 45 minutes I'm spending writing this post. Leadership and people dropped from 3.8 hours to half an hour. It's exactly what the talk warned about with the *mere urgency effect*: what nobody asks for by a deadline loses ground to what has one, even when it's worth more. I read about it, agreed with it, and it still happened to me in less than a month.

**Measuring is the first thing to go.** In the week I wasn't feeling well, I didn't just stop protecting my calendar: I stopped logging it. A time management system that only works in the good weeks measures exactly the weeks that need it the least.

## Protect: what didn't work (and what already did)

I'll be honest: I didn't follow the protect step the way it was proposed. Creating blocks the day before, with a start, an end, a deliverable and a "when X, I do Y" intention, didn't stick for me.

The reason is that my calendar isn't my biggest problem. It isn't packed with meetings, so most of the time I create the block right when I start doing the thing. Protecting everything in advance would be solving a problem I don't have.

But there's one case where I already protect time, without ever calling it that: **code review**. When PRs start to pile up, I create a block for the next day, something like "review PRs for 2 hours tomorrow". It's selective protection: only for the kind of work that won't happen unless I make room for it.

And the numbers show that learning and leadership are in exactly that situation. My problem isn't fragmentation, it's that the important-but-not-urgent never makes it onto the calendar. The lesson from this step, for me, is that protecting time doesn't have to be the rule for everything, only for what tends to disappear.

## What I'm going to change

1. **Remove the Support category**, which didn't tell me anything.
2. **Protect learning and leadership the same way I already protect code review:** a block reserved in advance, because if it depends on leftover time, it doesn't happen.

## Next steps

The next step is to **automate**: turn a recurring task into an AI routine. The natural candidate is this very measurement. Today I add up the hours by looking at the calendar; the idea is to ask an assistant to produce the weekly summary, compare it with the previous week and warn me when learning or leadership drop to zero.
