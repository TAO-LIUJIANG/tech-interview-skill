# Tech Industry Interview Skill

**English** | [中文](README.md)

![license](https://img.shields.io/badge/license-MIT-green)

> Give it your resume and a target company; get back an industry map, a gap list, interview scripts, and a mock interviewer.

## What it does

1. **An industry map** — a five-layer value chain, where your target companies sit on it, how their competitors (domestic and international) play, and which gap between academia and industry is still unfilled.
2. **A gap list** — P0/P1/P2, each backed by evidence from both sides: "what the company asks" vs. "what your resume actually says".
3. **Interview scripts** — the four-sentence pipeline pattern (where data comes from → what I transform it into → who consumes it → how success is measured), plus the one-sentence gap pitch. Blind-reviewed at 9/10.
4. **Practice loops** — scored mock interviews, independent blind review, and a learning queue re-prioritized by where you actually got stuck.

## Design philosophy

| Principle | In plain words |
|---|---|
| **Ability first** | Not how many terms you can recite — whether you can build it and explain it. |
| **Anti-hype** | Every concept must be explainable to a non-expert. Buzzwords without understanding lose points. |
| **Human-machine teamwork** | Humans confirm the important calls (rejections); machines check the boring stuff (word counts, structure, sources). |
| **Pipeline positioning** | Don't list skills — describe the pipeline: inputs, your transformation, consumers, feedback. |
| **Two-line contrast** | Tag every technique as academic-line or industry-line; the gap between them is where research roles add value. |

## Quick start

```bash
cp -r tech-interview-skill ~/.zcode/skills/   # or ~/.claude/skills/
```

Then just say: "help me practice interviews" / "can my resume survive follow-up questions?" / "run Stage 0 and analyze my gaps against company X".

## Key features

- **Evidence-chain scoring** — every score must quote your exact words; no quote, no score.
- **Honesty line** — every sentence in a rehearsed answer must trace back to your resume. Made-up stuff falls apart on stage.
- **Independent blind review** — reviewers only see the Q&A pair, nothing else.
- **Three-tier paper verification** — local library (10s probe) → arXiv/OpenReview → secondhand interpretations never enter your talking points.
- **Multilingual research** — English sources always checked; Japanese/German/etc. first-hand content too. Tech, product, market, and finance — not just finance.

## Example: bad answer vs. good answer

Same question ("walk me through your paper"), independent blind review:

- **7/10** — "I did LiDAR-3DGS reconstruction with a cross-modal encoding module, +1.5dB PSNR, trained from scratch on nuScenes." (Correct, but it reads like an abstract.)
- **9/10** — "Upstream is crowdsourced vehicle data — six surround cameras plus a 32-line LiDAR covering only 1.4% of pixels; that's my input constraint. I transform it into a differentiable 3D scene representation: sparse metric depth injected into initialization and supervision, fixing under-constrained drift — and it has to happen at this layer because downstream can't fix representation-level drift. Output feeds map updates and world-model training. On verification: my reproduction is within 0.08dB of the paper, so the accuracy is auditable."

The 2 points aren't about technique — they're about structure.

## Structure

```text
tech-interview-skill/
├── SKILL.md            # entry point: philosophy + hard rules R1–R9 + modes + main loop
├── references/         # six knowledge files (interviewers, scoring, selection, matching, industry DB, output spec)
├── examples/ · docs/   # sample outputs and design documents
```

## License

[MIT](LICENSE)
