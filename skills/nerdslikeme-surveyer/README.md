# Nerds Like Me — Survey Collector Skill

A Claude skill that turns messy, spoken-into-your-phone observations into polished feedback form answers for [Nerds Like Me](https://nerdslikeme.dream.page/) meetups.

## What it does

You attend a Nerds Like Me event and dictate your thoughts into the Claude mobile app throughout the evening — or all at once afterward. The skill collects your raw observations and maps them to the six questions on the post-event feedback form, then gives you clean copy-paste answers.

## How it works

1. **Fetches event metadata** — Pulls the current event's speaker, topic, date, and description from nerdslikeme.dream.page so it knows what you're giving feedback on.

2. **Collects your observations** — You speak or type freely, in any order, across one or many messages. The skill stays quiet during collection so you're not reading walls of text on your phone mid-event.

3. **Sorts using an agile retro framing** — Your observations are internally categorized as "what went well," "what could be better," and "what to improve." This maps naturally to the form's "keep doing," "stop doing," and "add or improve" questions.

4. **Prompts for improvement suggestions** — If you raise something that could be better but don't suggest a fix, the skill asks how you'd improve it. Your suggestion gets woven into the "add or improve" answer, turning complaints into actionable ideas.

5. **Presents a confidence-flagged summary** — Each form answer is shown with a confidence indicator (high/medium/low) and reasoning, so you can quickly spot anything that needs correction.

6. **Produces final copy-paste output** — Once you confirm, you get a clean block of text to paste directly into the form, field by field.

## The form questions

| # | Question | Required |
|---|----------|----------|
| 1 | How much did you enjoy the event? (1-5) | Yes |
| 2 | Rate the venue (1-5) | Optional |
| 3 | What should we keep doing? | Optional |
| 4 | What should we stop doing? | Optional |
| 5 | What should we add or improve? | Yes |
| 6 | Any other feedback for the organizers? | Yes |

## Installation

1. Enable **Code Execution and File Creation** in Settings → Capabilities
2. Go to **Customize → Skills**
3. Upload the `nerdslikeme-survey-collector.skill` file
4. Make sure the skill is toggled on

## Usage

Start a new conversation on the Claude mobile app and say something like:

- "Here's my feedback from tonight's Nerds Like Me"
- "Let me tell you about the event"
- "I need to fill out the feedback form"

Then just start talking. The skill handles the rest.

## Notes

- The numeric ratings (enjoyment and venue) are inferred from your tone — you don't need to say a number.
- Optional questions you don't mention are left blank, not chased.
- The skill won't soften negative feedback. If you had a bad time, it reflects that honestly.
