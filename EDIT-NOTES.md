# Thiruvasagam — English Editing Session Notes

All 51 chapters are translated and built.

| Task | Status |
|---|---|
| Task A — Per-chapter prose edit pass (all 51 chapters) | ✅ Complete |
| Task C — Add transliteration layer (Ch 41–45, 51) | ✅ Complete |
| Task B — Women-as-obstacle verse reframes (Ch 38, 40, 51) | ⏳ Pending |

---

## Task A — Per-chapter edit pass

Work through each `translated/NN-slug.txt` file in order. One pass per chapter covers everything below.

### Per-chapter checklist

```
1. SUMMARY — Check the summary paragraph at the top of the file.
   - Missing: write one covering form/metre, location, refrain, arc, register (4–6 sentences)
   - Present: fix awkward phrasing, do not change facts

2. 4-LAYER CHECK — Every verse must have all four layers in order:
      [Tamil text]
      [Transliteration — Layer 1b]
      [Word-by-word gloss]

      **[English prose]**
   Add any missing layer:
   - Transliteration: phonetic English per CLAUDE.md rules — long vowels aa/ii/uu,
     ழ=zh, ள=L, ற=R, த=th, ட=t, ண=N, ங=ng, ஞ=ny, ச=ch, no diacritics, one line only
   - Gloss: word-by-word, each Tamil word/phrase glossed in English
   - English prose: a **...** block per prose rules below

3. PROSE EDIT — Rewrite every **...** block to plain, natural English prose.
   Fix these problems:
   - O-epithet chains ("O Truth! O Spotless One! O Rider!") → sentences
   - Em-dash lists ("O Honey — O Ambrosia") → sentences
   - Archaic connectives ("thus", "thereof", "alas", "wherefore") → remove or rephrase
   - Run-ons (80+ word sentences) → split into 3–4 short sentences
   Do NOT change: theological terms, proper nouns, self-abasement terms (dog, ghost,
   wretch — these are theologically intentional), or meaning

4. VOCABULARY ROTATION — Vary owner/slave phrases across chapters:
   - "claimed me as his own" → also: "drew me in", "took me", "made me his", "brought me close"
   - "took me as his servant" → also: "made me serve him", "enrolled me among his own"
   - "rules me" → also: "governs me", "holds me", "keeps me"
   - "this servant" → also: "I your servant", "I who serve him", "me"

5. SENSITIVE LOG — Flag any verse a modern reader might find sensitive.
   Append to SENSITIVE-LOG.md:
      ## Ch NN — [Title]
      **Verse [#]**
      Translation: [paste **...** block]
      Sensitive element: [one sentence on what the issue is]
   What to flag: women as obstacles/temptations, graphic degrading body descriptions,
   caste language, violence described approvingly, anything easily misread out of context

6. BUILD & COMMIT
   python build-chapter.py translated/NN-slug.txt
   git add translated/NN-slug.txt chapters/NN-slug.html
   git commit -m "Improve English prose in Ch NN: Title"
```

---

## Task B — Women-as-obstacle verse reframes

Shift the framing from "women caused my trouble" → "my own desire/attachment caused my trouble". The Tamil is first-person confession; the English translations accidentally made the *women* sound like the problem rather than the *poet's own state*.

**Do NOT soften or remove the meaning** — just reframe the agency.

Example:
- Before: `"I fell into trouble through the sidelong glances of women with cotton-soft feet"`
- After: `"I was lost to my own desire, drawn by the glances of women with cotton-soft feet"`

| Chapter | Verse | Current problematic phrase |
|---|---|---|
| Ch 38 | v6 | "I fell into trouble through the sidelong glances of women with cotton-soft feet" |
| Ch 40 | v2 | "Through desire for the shoulders of pure-voiced women with waists narrow as drums — though I commit countless foul sins" |
| Ch 51 | v3 | "I, who took all falsehood for truth and was destined to drown in sensual pleasure" — also mentions "women with full breasts" as the draw |
| Ch 51 | v5 | "I would have stood helpless, afflicted by the sidelong glance of women with cotton-soft feet" |
| Ch 51 | v6 | "destined to fall upon the rounded breasts of bangle-clad women" |
| Ch 51 | v7 | "I, destined to sink and fall in delusion" — reference to women's delusion |
| Ch 51 | v8 | "destined to fall in desire into the embrace of jeweled women" |

**Note:** Ch 40 v10 and Ch 49 describe Parvati/Uma (Shiva's consort) — no reframe needed.

After editing: `python build-chapter.py` for Ch 38, 40, 51 and rebuild.

---

## Files reference

| File | Purpose |
|---|---|
| `translated/NN-slug.txt` | Source of truth — edit here |
| `chapters/NN-slug.html` | Generated — rebuilt by build-chapter.py, do not hand-edit |
| `chapters.html` | Chapter index — updated automatically by build-chapter.py |
| `build-chapter.py` | Build script |
| `CLAUDE.md` | Full project instructions and translation glossary |
| `SENSITIVE-LOG.md` | Sensitive content log — appended during Task A |
