# Gita Chapter Presentation — Authoring Instructions

This file is the standing specification for creating the remaining Gita chapter presentations. Follow it automatically so the design and verification requirements do not need to be repeated.

## What the user needs to provide

For the next batch, the user only needs to say:

> Process chapters **X–Y** from **PDF filename**.

Use the PDF in the repository and continue the established system. Ask a question only when chapter boundaries or source material are genuinely ambiguous.

## Deliverables

- Create one independent, self-contained HTML presentation per chapter.
- Name chapter files numerically: `lessons/6.html`, `lessons/7.html`, … `lessons/48.html`.
- Do not create or modify the chapter index until explicitly requested.
- Each presentation must work directly without depending on another chapter file or index.
- Generate one original background artwork per chapter and save it as:
  `images/generated/chapter-NN-bg.png`, using a two-digit chapter number.
- Publish completed chapters to the existing GitHub Pages repository.

Public URL pattern:

```text
https://netvision.github.io/gita-core-objective/lessons/N.html
```

## Source verification

1. Read the actual PDF before drafting slides.
2. Identify the exact chapter title, page range, प्रसंग, सिद्धान्त, examples, stories, practices, questions and cited shlokas.
3. Preserve the intended relationship between every shloka and the slide’s meaning.
4. Never insert a shloka merely because it sounds thematically similar.
5. If the PDF gives only a verse range without quoting the Sanskrit, show the reference only. Do not invent or import verse text.
6. Quote Sanskrit exactly as it appears in the source, correcting only unmistakable Unicode/OCR corruption after verification.
7. Resolve apparent source typos through context and mention material corrections in the handoff.

## Presentation structure

Keep each chapter brief, pointed, concise and complete for a speaker-led presentation. Usually use 5–7 slides:

1. Chapter title and central question
2. Gita context or principal shloka
3. Core distinction or teaching
4. Example, analogy or story from the PDF
5. Practical implication or second supporting shloka
6. Reflection, discussion or daily practice

Add or remove a slide when the source genuinely requires it. Do not compress multiple important ideas into unreadable panels.

## Writing rules

- Default language is Hindi.
- Every visible slide must also have a concise, natural English version.
- Preserve the philosophical meaning rather than translating mechanically.
- Keep slide text short enough to support a speaker instead of replacing the speaker.
- Put additional explanation in the optional speaker cue.
- Speaker cues must exist in both Hindi and English.
- Retain important source terminology such as समता, विवेक, तितिक्षा and अचाह where translation would lose precision; explain it briefly in English.
- Include the PDF’s reflection questions and practices when they materially complete the lesson.

## Shloka formatting

- Shlokas must be prominent and placed in the dedicated verse panel.
- Each two-line shloka must break after the first danda `।`.
- The closing `॥` must remain on the second line and must never wrap onto a third line.
- Multiple consecutive shlokas should appear as two lines per shloka.
- Show the exact chapter and verse number.
- The Hindi/English language toggle changes the explanation, not the Sanskrit.
- On mobile, keep each Sanskrit line intact with an appropriately reduced but still prominent font size.

## Visual system

Continue the established refined Indian manuscript/watercolor aesthetic:

- Warm handmade-paper texture
- Saffron, antique gold, vermilion and restrained Krishna/peacock blue
- `Yatra One` for display typography
- `Hind` for Hindi body and Sanskrit
- `Cormorant Garamond` / `Source Sans 3` for English support
- Generous negative space
- Thin manuscript-like borders
- Dark title/reflection slides and pale explanatory slides
- No generic corporate gradients, stock-photo look or decorative clutter

Use an existing numbered chapter file as the implementation reference, preferably the latest completed chapter.

## Background artwork workflow

Use the built-in image-generation tool. The images in `images/1.jpg` through `images/18.jpg` are **style references only**. Do not copy them, edit them or publish them unless explicitly requested.

Create one original 16:9 panoramic image for each chapter. The artwork must express that chapter’s central metaphor and remain usable behind text.

Prompt template:

```text
Use case: stylized-concept.
Asset type: widescreen presentation background for Bhagavad Gita chapter NN, “TITLE”.
Input images: loose style references only for translucent watercolor, handmade paper,
restrained Indian narrative linework and generous negative space; do not copy.
Primary request: create an original 16:9 abstract Indian watercolor expressing CORE IDEA
through METAPHOR/MOTIFS from the chapter.
Composition: keep the central/primary text area calm and low-detail; place visual energy
near the outer edges and corners; allow alternate crops across slides.
Palette: warm parchment, saffron and antique gold with chapter-appropriate restrained accents.
Constraints: sophisticated, contemplative, presentation-safe, no readable text, no letters,
no logo, no watermark, no photorealism, no detailed faces, no dominant unrelated deity figure.
```

After generation:

1. Inspect the result for relevance, negative space and unwanted text/symbols.
2. Copy the chosen asset into `images/generated/chapter-NN-bg.png`.
3. Reference it from that chapter’s HTML using a relative URL.
4. Use warm translucent overlays so text contrast remains strong.
5. Use a darker overlay on title and reflection slides.
6. Vary `background-position` across slides to avoid a mechanically repeated crop.
7. On mobile, prioritize text and shloka readability over artwork visibility.

## Required presentation behavior

Every numbered chapter file must retain:

- Hindi/English toggle
- Left/right arrow, Page Up/Page Down and Space navigation
- Home/End slide navigation
- Swipe navigation on touch devices
- Fullscreen control and `F` shortcut
- Optional speaker cues and `N` shortcut
- Progress dots and slide counter
- Direct slide URL support: `?slide=N`
- Direct English URL support: `?lang=en`
- Combined parameters, for example: `?lang=en&slide=3`
- Reduced-motion support
- Minimum 44 × 44 px touch targets for actual controls; progress dots must remain visually small

## Responsive and visual verification

Before publishing, inspect representative slides at:

- Mobile: approximately 375–414 px
- Tablet: 768 px
- Desktop: 1440 px

Always verify:

- No horizontal scrolling or clipped English headings
- No overlapping navigation controls
- No isolated danda or `॥` on a third Sanskrit line
- Shlokas remain prominent
- Background art is visible but subordinate to content
- Text and controls have sufficient contrast on light and dark slides
- Long stories or lists fit without crowding
- Language switching updates all explanations and speaker cues
- Direct `slide` and `lang` query parameters work

## Content audit before release

For every chapter, confirm:

- [ ] Slide claims match the PDF
- [ ] Shlokas are actually relevant to the slide meaning
- [ ] Sanskrit and verse numbers are accurate
- [ ] No verse was fabricated where the PDF provided only a reference
- [ ] Hindi summary is concise but complete
- [ ] English meaning is faithful and natural
- [ ] Examples, stories and practices retain their original purpose
- [ ] Speaker cues add value without repeating the slide
- [ ] Artwork metaphor matches the chapter

## Git and publishing rules

- Preserve unrelated and untracked user files.
- Stage only the new/modified numbered chapter files and their generated backgrounds.
- Do not commit source PDFs or the 18 reference images unless explicitly requested.
- Run Git whitespace checks before committing.
- Use a descriptive commit message, for example:

```text
Add Gita chapter presentations 6 through 10
```

- Push to `main` in `https://github.com/netvision/gita-core-objective.git`.
- Wait for the GitHub Pages deployment to complete.
- Verify every new public chapter URL and at least one generated image URL returns HTTP 200.
- Report the chapter links and commit hash to the user.

## Current completed set

- `lessons/1.html` — मोह
- `lessons/2.html` — परिस्थिति का स्वरूप एवं प्रभाव
- `lessons/3.html` — नित्य/अनित्य का भेद
- `lessons/4.html` — उद्देश्य परिवर्तन
- `lessons/5.html` — करने योग्य

The planned complete collection contains 48 chapters.
