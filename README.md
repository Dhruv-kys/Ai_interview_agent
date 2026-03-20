## Instructions

1. Set environment variables in `.env`:
```env
ELEVENLABS_API_KEY=...
OPENAI_API_KEY=...
```

2. Run:
```bash
cd /Users/dhruvdiwakirti/Downloads/allystack/allystack
./.venv/bin/python -m realtime_interview_agent.live_voice
```

## Model Reading

- Speech-to-Text (ASR): `ELEVENLABS_STT_MODEL` -> default `scribe_v1`
- Text-to-Speech (TTS): `ELEVENLABS_TTS_MODEL` -> default `eleven_turbo_v2`

## Diagram

```text
Audio Input
  ↓
VAD
  ↓
Streaming ASR (ElevenLabs)
  ↓
NLU
  ↓
Dialogue Manager
  ↓
Follow-up Generator (LLM)
  ↓
Response (Text/TTS)
  ↓
Metrics Logger
```
