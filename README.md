# திருவாசகம் · Thiruvasagam

A complete scholarly-quality English translation of *Thiruvasagam* — the 9th-century Tamil devotional masterwork of the poet-saint **Manikkavasagar**, composed mostly at Chidambaram (Thillai). 51 chapters, approximately 900 verses.

> *"திருவாசகத்துக்கு உருகார் ஒரு வாசகத்துக்கும் உருகார்"*
> Those who do not melt at Thiruvasagam will not melt at any other word.

---

## What is Thiruvasagam?

Thiruvasagam (Sacred Utterances) is considered the crown of Tamil Shaiva Bhakti literature. Manikkavasagar (9th century CE) composed these 51 hymns in a white heat of devotion, ranging in register from ecstatic praise to anguished self-abasement to tender folk-song. The work is sung in temples, chanted in homes, and memorised across generations of Tamil-speaking Shaivites.

---

## Project structure

```
translated/          Source .txt files — one per chapter (Tamil + transliteration + gloss + English)
chapters/            Generated HTML pages — rebuilt from translated/ by build-chapter.py
chapters.html        Chapter index
index.html           Home page
dedication.html      Dedication page
locations.html       Sacred locations referenced in the text
siva-names.html      Names and epithets of Shiva used across the chapters
Reference.html       Scholarly reference notes
style.css            Site stylesheet
build-chapter.py     Build script: .txt → HTML
CLAUDE.md            Full translation guidelines and glossary (for AI-assisted sessions)
EDIT-NOTES.md        Editing task list (Task A prose pass, Task B reframes)
SENSITIVE-LOG.md     Content sensitivity log (local only, not git-tracked)
```

---

## Translation format

Each chapter source file (`translated/NN-slug.txt`) uses a four-layer format:

```
1

Tamil    words    spaced    out
transliteration    chunks    here
word-by-word    gloss    here

**Full English prose translation.**
```

**Layer rules:**
- Long vowels: `aa`, `ii`, `uu` — no diacritics
- ழ = `zh` · ள = `L` · ற = `R` · ண = `N` · ச = `ch`
- Each layer must be exactly one line (4-space separators between chunks)
- English prose: plain, clear, natural — no archaic language, no em-dash epithet chains

---

## Building a chapter

```bash
python build-chapter.py translated/NN-slug.txt
```

This writes `chapters/NN-slug.html` and updates `chapters.html`. Rebuild all chapters:

```powershell
.\build-all.ps1
```

---

## Translation status

All 51 chapters translated, built, and published. See `PROGRESS.md` for the edit pass status.

---

## Editorial tasks

| Task | Status |
|---|---|
| Task A — Per-chapter prose edit pass (all 51 chapters) | Complete |
| Task C — Add missing transliteration layer (Ch 41–45, 51) | Complete |
| Task B — Women-as-obstacle verse reframes (Ch 38, 40, 51) | Pending |

See `EDIT-NOTES.md` for full task details.
