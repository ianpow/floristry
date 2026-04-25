# Floristry Quiz – CLAUDE.md

## What this is
A single-page HTML practice quiz for Sharon, who is studying the **City & Guilds Level 2 Technical Certificate in Floristry (0175-20)**. The quiz helps her prepare for the multiple-choice theory assessment.

## File
- `index.html` – the entire app (HTML + CSS + JavaScript, no build step, no dependencies)

## Deployed
- GitHub: `ianpow/floristry`
- Hosted on Vercel (auto-deploys on push to `main`)

## Current sections
The quiz covers the three topics Sharon needs for her assessment:
1. **Colour Theory** – colour wheel, harmonies (complementary, analogous, monochromatic, triadic), tints/shades/tones
2. **Elements of Design** – line, form, texture, space, focal/filler/line materials
3. **Principles of Design** – balance, proportion, scale, dominance, rhythm, contrast

## How questions are structured
All questions live in the `SECTIONS` array at the top of the `<script>` block in `index.html`. Each section looks like this:

```js
{
  id: "colour-theory",          // unique slug
  title: "Colour Theory",       // shown in the tab bar
  subtitle: "...",              // shown under the section heading
  questions: [
    {
      q: "Question text here?",
      options: ["A answer", "B answer", "C answer", "D answer"],
      answer: 0,                // zero-based index of the correct option
      feedback: "Explanation shown after answering.",
      hint: "A nudge shown when the hint button is clicked."
    },
    // ... more questions
  ]
}
```

## Adding new questions
1. Open `index.html`
2. Find the relevant section in the `SECTIONS` array
3. Add a new object to its `questions` array following the structure above
4. To add a whole new section, add a new object to `SECTIONS` with a unique `id`
5. Commit and push – Vercel deploys automatically

## Pass mark
50%, matching the City & Guilds standard. Shown per-section and in the overall results screen.
