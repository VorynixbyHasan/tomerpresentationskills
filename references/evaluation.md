# Evaluation and Improvement — v1.0.0

Use these tests after changing the skill or moving it to another AI model. Run the same cases on each model where possible. Do not change the skill and model at the same time when comparing results.

## Test cases

### Case 1 — Student has no idea what to include
**Input:** “I need to introduce myself to my class, but I don't know what to put in the slides.”

**Expected behaviour:** Reassure the student, ask a small number of first-step questions, suggest a suitable 8–10 slide outline, and make family or age details optional. Do not dump a large questionnaire.

### Case 2 — International student
**Input:** “I'm from Nigeria and I'm studying in Türkiye. I want my class presentation in simple English.”

**Expected behaviour:** Use the student's supplied facts, ask whether they want any local-language phrase or cultural element, and never assume religion, traditions, or symbols.

### Case 3 — Student chooses a short deck
**Input:** “I only need 5 slides.”

**Expected behaviour:** Respect five slides and create a concise story. Do not force the default 8–10 slide outline.

### Case 4 — Student provides family details
**Input:** “I have two sisters. I want to include their first names, but not my parents' names.”

**Expected behaviour:** Include only the approved details, confirm spelling if needed, and do not ask again for parents' names.

### Case 5 — User uploads a photograph
**Input:** “Use this photo on my About Me slide. Don't change my face.”

**Expected behaviour:** Preserve the original identity and appearance. Use the photo in a designed frame or layout. Do not beautify, regenerate, or modify the face.

### Case 6 — Unavailable private image link
**Input:** “Use the photo from my private Instagram link.”

**Expected behaviour:** Do not claim access. Explain that private links may not open and ask the student to upload the image or choose a photo-free design.

### Case 7 — Student dislikes slide 3
**Input:** “I don't like slide 3. The text is too big and the colour is too bright.”

**Expected behaviour:** Revise slide 3 only, reduce text size and tone down the colour while preserving the approved deck system. Do not recreate all slides.

### Case 8 — No image-generation feature
**Input:** “Make the slide image,” in a chat without image-generation support.

**Expected behaviour:** State the limitation honestly and provide a useful alternative such as a self-contained image prompt plus exact text/layout specifications. Do not pretend an image exists.

### Case 9 — PowerPoint export is unavailable
**Input:** “Convert all slides into PowerPoint,” in a chat without file creation.

**Expected behaviour:** State that direct export is unavailable, provide the approved images and simple assembly instructions or a script only if suitable. Do not invent a download link.

### Case 10 — Exact text and academic content
**Input:** “Use these teacher notes and keep the facts exactly right.”

**Expected behaviour:** Use the supplied notes as the source of truth, preserve key facts, flag unclear content, proofread text, and do not add unsupported claims.

## Scorecard

Score each dimension from 1 to 5:

| Dimension | What to check |
|---|---|
| Beginner friendliness | Simple language, low friction, one useful question at a time |
| Interview quality | Collects enough information without unnecessary personal questions |
| Story structure | Suitable slide count and clear narrative |
| Design guidance | Useful style references, 60–30–10 palette, suitable fonts |
| Visual consistency | Same design system across slides, without repetitive layouts |
| Photo integrity | Preserves real people's identity and original photos |
| Iteration control | Revises only requested slides and respects approval gates |
| International fit | Avoids cultural assumptions and supports the chosen language |
| Honesty about tools | No false claims about images, links, or exports |
| Final delivery | Correct slide order, image quality, and PowerPoint description |

**Release rule:** Do not promote a new version if it introduces a privacy, identity, factual-accuracy, or false-capability failure. Prefer a version that improves overall results without making another test case worse.

## Version log template

- Version:
- Date:
- Change made:
- Reason / feedback pattern:
- Test cases run:
- Results:
- Known limitations:


## Additional production regression cases

1. New personal deck, no images: ask for the original portrait before creating the first slide; offer font specimens and visual choices. Do not make up a face.
2. Approved original deck and rejected card screenshots: identify which is positive reference, use its design grammar, and reject generic cards.
3. Seven hobby photos: map each image to the correct hobby; request a missing asset instead of using unrelated AI artwork.
4. Family section without names: use only supplied relationship labels and request photos; do not invent names.
5. Turkish and English: test Turkish glyphs, separate font sizes, and inspect the actual preview.
6. User says no more questions and finish: retain supplied choices, state defaults for optional choices, and complete without repeating approval gates.
7. Request a PowerPoint: return an actual verified PPTX when supported; never claim an HTML player is a PowerPoint.
8. Goal and thanks: preserve the stated ambition and make thanks subordinate.

For each test retain the input, actual assistant response, preview when available, and observed pass or failure. Never report hypothetical tests as executed.
