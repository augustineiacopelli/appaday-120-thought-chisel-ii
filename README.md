# Thought Chisel II

A voice-driven Socratic idea refiner, upgraded from App 067. Speak a raw thought into the mic and Claude works it through a chosen number of rounds, clarifying terms, probing assumptions, and exploring implications, before delivering a chiseled final sentence and naming the sharpest remaining tension in it.

## What's new in this build

- **Depth selection.** Before recording starts, choose Quick (2 rounds: one clarifying pass, then the chiseled idea) or Deep (5 rounds moving through clarifying, assumption-probing, and implication-exploring questions before the final cut).
- **Typed rounds.** Each round now carries a type (clarifying, assumption-probing, implication-exploring, or final) that shapes the system prompt Claude receives, so the follow-up questions vary in kind rather than repeating the same move five times.
- **Named tension.** The final round now asks Claude to state the single sharpest unresolved tension in the idea, separate from the supporting dimensions.
- **Session library.** Every completed session is saved automatically to local storage (capped at 50) and is browsable from the header library icon, newest first. Opening a saved session shows a read-only summary: raw thought, final sentence, and key tension.
- **Continue as new chisel.** From any completed session, live or reopened from the library, you can branch into a new session that starts with the prior session's final sentence as its opening thought, keeping a record of which session it grew out of.

## How it works

Tap the mic and talk. Speech recognition transcribes what you say; on stop, the transcript and prior round history go to Claude, which distills the thought into one sentence and asks a follow-up question suited to that round's type. The follow-up is read aloud, then the mic reopens automatically for the next round. On the final round, Claude returns the chiseled idea and its key tension instead of a question, and the session is saved.

## Settings

Tap the gear icon to add a Claude API key (stored only in local storage, never committed) and pick a voice for the read-aloud follow-ups.

## Requirements

A browser with Web Speech API support (Chrome desktop or mobile, or Safari on iOS 14.5+). Requires a Claude API key with your own usage costs.

---

App #0NN &middot; AI-Powered &middot; Part of [AppADay](https://augustineiacopelli.github.io/appaday/)
