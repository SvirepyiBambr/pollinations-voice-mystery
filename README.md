# 🕵️ Whisper Manor — Voice Murder Mystery

A browser voice murder-mystery game powered by [Pollinations](https://pollinations.ai), submitted for **quest #15724**.

**Play:** https://svirepyibambr.github.io/pollinations-voice-mystery/

## How it works
- **New case every playthrough** — the case, 4 suspects, alibis and the hidden truth are generated fresh by the Pollinations text API each game.
- **Interrogate by voice** — speak via the Web Speech API (typing as fallback); suspects answer in character and are **spoken aloud** with the Pollinations `openai-audio` TTS model, each suspect with a distinct voice.
- **Detective notebook** — a lightweight model extracts factual claims from every answer into your notebook, so contradictions are easy to spot.
- **Accuse** — a noir narrator delivers the verdict; wrong accusations reveal the real culprit.
- **Bring your own Pollen** — players paste their own key from [BRING_YOUR_OWN_POLLEN](https://github.com/pollinations/pollinations/blob/main/BRING_YOUR_OWN_POLLEN.md); no secrets are embedded.

## API usage (all against gen.pollinations.ai, paid with the player's own Pollen)
- `POST /v1/chat/completions` — case generation, suspect dialogue, claim extraction, verdict narration
- `POST /v1/audio/speech` — spoken suspect answers (`openai-audio`, distinct voice per suspect)

## Live demo
The app itself is the live demo: every case, answer and verdict is a real API call. Open the URL above, paste your Pollen key, press **New case**.
