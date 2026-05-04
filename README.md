# Piano Ear Training

A browser-based ear training app for practicing movable-Do listening on piano.
It helps you hear a tonal center, identify hidden notes or short phrases, and
resolve them back to Do.

## What It Trains

- **Resolve mode:** hear a hidden target note in context, then resolve to Do.
- **Phrase mode:** hear and identify short melodic patterns.
- **Anchor awareness:** establish key center before recognition work.
- **Transposition mindset:** move the same solfege idea across keys.

## Features

- Playable source and target keys.
- Configurable difficulty, mode, phrase length, tempo, and anchor type.
- Replay controls split by role:
  - replay anchor
  - replay notes
- Reveal playback that:
  - replays the exercise notes
  - resolves from the highest note to the nearest Do path.
- Optional Salamander piano samples (`piano-samples/`) with synth fallback.

## Run Locally

From the project folder:

```bash
python3 -m http.server 8000
```

or:

```bash
python -m http.server 8000
```

Then open:

[http://localhost:8000](http://localhost:8000)

## Run From Any Directory

```bash
python3 -m http.server 8000 --directory /path/to/ear-training
```

Then open:

[http://localhost:8000](http://localhost:8000)

## Audio Notes

- The app uses Web Audio scheduling (timed playback on the audio clock).
- Note timing is tempo-aware and role-aware (anchor vs target/reveal).
- Playback is designed to be connected/legato with controlled overlap.
- If Salamander samples are missing, playback automatically falls back to synth.
