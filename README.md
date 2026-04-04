# Environmental Artisan Portrait

Official-style BananaHub template for environmental portraits with strong occupational storytelling.

This template is designed around Google Gemini image prompting guidance:

- describe the scene instead of listing keywords
- combine subject, action, setting, lighting, and composition cues
- prefer concrete photographic language for realistic results

## Install

```bash
npx bananahub add zkywalker/nanobanana-artisan-portrait
```

## Use

```text
/bananahub use artisan-portrait
/bananahub use artisan-portrait 一位在陶艺工作室里专注拉坯制碗的老年陶艺师
```

The sample image in this repo validates the default pottery-workshop prompt. The custom example above stays in the same subject family to avoid mismatching the sample preview with a very different occupation.

## Verified Models

- `gemini-3-pro-image-preview` — manually verified with `samples/sample-3-pro-01.png`

## Supported Models

- `gemini-3.1-flash-image-preview` — expected good, not manually verified in this repo
- `gemini-2.5-flash-image` — expected good, not manually verified in this repo

## Sample Outputs

| File | Model | Prompt / Variant |
|---|---|---|
| `samples/sample-3-pro-01.png` | `gemini-3-pro-image-preview` | Default template prompt: elderly Japanese ceramicist shaping a bowl in a rustic pottery workshop |

## What It Produces

Environmental portraits where the person is visually tied to their craft:

- ceramicist in a pottery studio
- watchmaker at a precision bench
- florist arranging stems in a sunlit shop
- baker shaping sourdough in a flour-dusted kitchen

## Files

```text
.
├── template.md
└── samples/
    └── sample-3-pro-01.png
```

## License

MIT
