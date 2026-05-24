# Memact Contributor Handoff

Memact is a playground where apps personalize using context the user can actually see and control.

It is still a playground, even if the old Playground repo is no longer the main place to contribute.

The current playground is Schema: app categories, context shapes, examples, prompts, and tests.

The short version:

Apps send context. App categories give it shape. Wiki gives users control.

## The idea

Most apps personalize quietly. They guess from clicks, isolated profiles, and hidden assumptions.

Memact does something different. Apps can send or propose context, but the user gets a Wiki where that context can be reviewed, edited, rejected, deleted, or shared.

So if a music app notices a user keeps replaying Brazilian phonk, it should not secretly build a weird hidden profile and call it intelligence.

It can propose something readable:

"Prefers Brazilian phonk, especially high-energy tracks."

The user can accept it, edit it, or reject it.

## What contributors do now

Contributors are not expected to build random generic features.

Pick an app category and define how context should work there.

Examples:

- music
- video-streaming
- movie-booking
- shopping
- learning
- news-articles
- fitness
- travel
- food-delivery
- creator-tools
- productivity
- AI assistants

For each category, contributors can add:

- useful context fields
- messy app context examples
- expected Wiki outputs
- simple normalization rules
- user-facing entry templates
- prompts for missing context
- access suggestions
- tests

## Example: music apps

A music app may send:

"User replayed Brazilian phonk playlists 18 times this month and skipped slow acoustic playlists."

A category schema can shape that into:

"Prefers high-energy Brazilian phonk."

But the Wiki is where the user stays in control. The user may edit it to:

"I like Brazilian phonk mostly while working out."

That edited user context is stronger than the app guess.

## Parts

- Access handles consent, apps, API keys, scopes, and permissions.
- Wiki is where users add, edit, approve, reject, delete, and share context.
- Schema defines app category schemas.
- Memory stores accepted context, history, retrieval, and app-safe summaries.
- Contracts defines shared shapes.
- SDK lets apps connect to Memact.

## Rules

- Default visibility should be private.
- Apps should not get full Wiki access.
- Apps should only get relevant category context with permission.
- User-added context is stronger than app-proposed context.
- Important app writes should require approval.
- Do not infer sensitive traits.
- Do not write fake certainty.
- Keep user-facing copy simple.
- Do not bring back Capture, Inference, or Intent as core product language.

## Best explanation

Memact is a playground for user-controlled app context.

Apps bring context. Categories organize it. Wiki keeps the user in charge.
