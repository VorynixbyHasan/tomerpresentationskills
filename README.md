# Student Presentation Creator

A reusable AI skill by Hasan / Vorynix for students creating personal introductions, TÖMER presentations, and class projects.

## What it does

- Helps plan a clear story and slide order.
- Uses a consistent visual style, readable typography, and a 60–30–10 colour palette.
- Preserves original personal photos and checks names and facts.
- Reviews slides individually and exports an image-based PowerPoint when the AI environment supports it.
- Supports different countries, languages, and subjects without assuming personal details.

## Quick start

1. Download this repository using **Code → Download ZIP** and extract it.
2. In an AI tool supporting skills, install the folder containing `SKILL.md`, keeping `references/` and `agents/` beside it. Follow that tool's own installation instructions.
3. If your AI tool cannot install skills, upload `SKILL.md` and `references/evaluation.md` to a chat and ask it to follow the workflow. This is a manual fallback, not an installed skill.
4. Start with the example below and supply your own information and photos.

> Use the Student Presentation Creator skill. Help me make a short personal introduction for my class in simple Turkish with small English translations. Keep my original photos unchanged. Ask only for missing details and help me choose a clear slide order.

## Files

- `SKILL.md`: main workflow and rules.
- `references/evaluation.md`: evaluation cases for checking behaviour.
- `agents/openai.yaml`: display metadata for compatible skill tools.

## Requirements and limits

This repository contains instructions, not a standalone app or a PowerPoint generator. Image generation, browsing, file creation, and PowerPoint export depend on the host AI tool and its plan. Uploading the repository to GitHub does not activate it automatically. Format validation has passed; behaviour has not been verified on every platform.

The default PowerPoint output uses full-slide images. Text in that version is not individually editable. An editable deck requires suitable presentation tools.

Only upload information and photographs you have permission to use. Personal details are optional. The workflow does not guarantee model compliance: always review text, facts, photos, and the exported file before presenting.

## License

MIT — see [LICENSE](LICENSE).
