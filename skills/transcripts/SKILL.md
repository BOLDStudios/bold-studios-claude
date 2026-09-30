---
name: transcripts
description: Transcribe audio and video with BOLD Studios and turn transcripts into show notes, quotes, captions and posts. Use when the user has a podcast, sermon, interview, meeting or video recording they want transcribed or repurposed.
---

# Transcripts

## Transcribing

1. Get a public URL to the audio or video file and its approximate length.
2. Estimate the cost: $0.05 per minute of audio. For anything over 20 minutes, state the estimate and get a yes.
3. Call `ai_transcribe`. Long files finish in the background.
4. Call `ai_transcript` to fetch the result. Checking on the same transcript again is not charged twice, so it is fine to check until it is ready. Wait between checks rather than calling in a tight loop.

## Turning a transcript into content

Offer the outputs that fit the recording:

- Show notes: a two-sentence summary, then 5 to 8 chapter markers with timestamps.
- Pull quotes: 5 to 10 lines under 25 words that stand on their own, with timestamps, quoted exactly.
- Short-form clips: the 3 strongest 30 to 60 second moments, each with a hook line, the start and end timestamps, and why it works.
- Captions and posts: platform-ready text for each clip.

Quote speakers exactly. Never put words in a speaker's mouth or fix their theology, grammar or opinions in a direct quote.
