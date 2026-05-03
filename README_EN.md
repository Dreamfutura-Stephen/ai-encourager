[中文](README.md) | English

# AI Encourager v2

A lightweight AI companion skill for Claude codex— four character personas, a one-step framework, and optional voice encouragement. Not a coach. Not a productivity tool. Just someone who sits beside you when you're stuck.

## Features

- **Four character personas** — each with a distinct voice, belief system, and conversational style
- **One-step framework** — Define → Split → Do → Learn. Break through inertia one tiny step at a time
- **Optional voice encouragement** — independent edge-tts engine, auto-plays with text, no clicking needed
- **Skip-to-action** — say "let's go" and bypass pleasantries straight to work
- **Natural switching** — switch characters mid-session with a sentence

## Quick Start

Just say any of these to Claude:

- "Encourage me" / "鼓励我"
- "XiaoNuan, keep me company" / "小暖陪我"
- "Switch to XingNai" / "换星耐"

The skill activates and greets you in character. Say **"let's go"** / **"直接开始"** to skip the greeting and jump straight to defining your step.

## Characters

| Character | Type | Essence | Voice |
|-----------|------|---------|-------|
| **XiaoNuan** (default) | Gentle & caring | "You don't need to be better. You just need to be seen." | zh-CN-XiaoxiaoNeural |
| **XingNai** | Energetic & cheerful | "Action is the best medicine. Starting is the biggest win." | zh-CN-XiaoyiNeural |
| **LongZi** | Quiet & healing | "Sometimes not doing is also a valid way of doing." | zh-TW-HsiaoChenNeural (fallback: Xiaoxiao -25% rate) |
| **Luna** | Wise & sharp | "See the essence, then choose. You just need someone to steady you." | zh-CN-XiaoxiaoNeural (rate -15%, pitch -5Hz) |

## The One-Step Framework

```
Define → Split → Do → Learn → (repeat)
```

Every session follows this loop. No skipping steps. No rushing ahead.

| Step | What happens | Core question |
|------|-------------|---------------|
| **Define** | Name the one step | What's the one thing? When is it "done"? |
| **Split** | Shrink it mercilessly | Can you cut it in half? Can it be done in 15 minutes? |
| **Do** | Execute | That's it — go do it. Come back when you're done. |
| **Learn** | Reflect | What did you learn? What's the next Define? |

**Rules of the framework:**
- Each step must be fully completed before moving to the next
- If the user drifts or complains, gently guide back — but never force
- Never start Split before Define is clear. Never push Do before Split is settled.

## Voice Encouragement

Voice is **off by default**. Say **"enable voice"** / **"开启语音"** to turn it on, **"disable voice"** / **"关闭语音"** to turn it off. The skill never nags you about it.

When enabled, the character speaks automatically alongside the text — no clicking required. Uses the independent `edge-tts` engine (Microsoft neural TTS) for high-quality voices that sound consistent across macOS and Windows. Audio plays via browser AudioContext. Previous audio is killed before each new utterance to prevent overlap.

**Prerequisite:** `pip install edge-tts`

Plays at three moments:

| Moment | Trigger |
|--------|---------|
| 🎯 Nudge | Right after you commit to your smallest step |
| 🎉 Celebrate | When you report back — done |
| 👋 Goodbye | When the session naturally ends |

## Design Principles

- Equal companionship, not authority
- Warm but restrained — no empty cheerleading
- Never decides for you, never does it for you
- Respects silence and hesitation

## Boundaries

This skill does not: make decisions for you, provide therapy, do your work for you, force optimism, or push when you're not ready.

## Installation

Copy `SKILL.md` into your Claude skills directory, or use the Cowork skill installer.

## License

MIT
