# Jill's Needs Analysis — Role-play

A single self-contained HTML training activity (the "Discovery & Needs Analysis — Do section"
role-play) for Wall Street English sales training. No build step, no dependencies beyond Google
Fonts — open `discovery_roleplay.html` directly in a browser to preview or deliver it.

## What it is

A photo-based consultation role-play: the learner reads a real consultation scene (Jill, the
prospective student, on the left; "You", the consultant, on the right), makes multiple-choice
responses at each phase, and watches a "warmth" relationship meter react to each choice. It ends
with a recap/transcript screen and a completion code.

## Localization

Everything a learner sees lives in two JavaScript objects near the top of the `<script>` block:

- `UI` — interface labels and buttons
- `SCENARIO` — the conversation itself

To produce a new language version, translate the string values inside these two objects and
re-host the file. Nothing else needs to change.

Each spoken line also has an `audio` field (currently `null`). Set it to a path such as
`audio/en/p1_jill.mp3` to auto-play a per-language ElevenLabs voice clip for that line; leaving
it `null` keeps the activity text-only.

## Design system

This activity is the reference implementation of the shared "Do section" visual/interaction
style used across Wall Street English sales training activities — see `_ref-SALESDOSTYLEGUIDE`
for the full design tokens, component inventory, the panel budget, and a blank template for
building new activities in the same style.
