# Thiruvasagam — Progress Tracker

Quick-reference for AI-assisted sessions. Update this file when work is done so the next session can orient without re-reading chapters.

---

## Overall status

| Task | Status |
|---|---|
| All 51 chapters translated | ✅ Done |
| All 51 HTML pages built | ✅ Done |
| Task A — prose edit pass | ✅ Done (all 51 chapters) |
| Task C — missing transliteration | ✅ Done (Ch 41, 42, 43, 44, 45, 51) |
| Task B — women-as-obstacle reframes | ⏳ Pending |

---

## Task B — Women-as-obstacle reframes (PENDING)

Shift agency from "women caused my trouble" → "my own desire caused my trouble".
Do NOT soften meaning — just reframe who is the agent of the problem.

After each edit: `python build-chapter.py translated/NN-slug.txt`

| Chapter | File | Verse | Current phrase | Done? |
|---|---|---|---|---|
| Ch 38 | `translated/38-tiru-ecaravu.txt` | v6 | "I fell into trouble through the sidelong glances of women with cotton-soft feet" | ☐ |
| Ch 40 | `translated/40-kulap-pattu.txt` | v2 | "Through desire for the shoulders of pure-voiced women with waists narrow as drums" | ☐ |
| Ch 51 | `translated/51-acco-patikam.txt` | v3 | "women with full breasts" as enthrallment | ☐ |
| Ch 51 | `translated/51-acco-patikam.txt` | v5 | "afflicted by the sidelong glance of women with cotton-soft feet" | ☐ |
| Ch 51 | `translated/51-acco-patikam.txt` | v6 | "fall upon the rounded breasts of bangle-clad women" | ☐ |
| Ch 51 | `translated/51-acco-patikam.txt` | v7 | "sink and fall in delusion of women" | ☐ |
| Ch 51 | `translated/51-acco-patikam.txt` | v8 | "fall in desire into the embrace of jeweled women" | ☐ |

**Extended candidates** (not yet decided — see SENSITIVE-LOG.md for context):
- Ch 05 v23, v31, v44, v61
- Ch 06 multiple verses
- Ch 24 v411–414
- Ch 25 v427
- Ch 41 multiple verses

---

## Task A — Chapter edit pass (COMPLETE)

All 51 chapters have been through the full checklist:
1. Summary paragraph present and edited
2. 4-layer verse structure verified (Tamil / Transliteration / Gloss / English)
3. English prose edited (O-epithet chains broken, em-dashes removed, archaic language removed, run-ons split)
4. Vocabulary rotation applied ("claimed" / "drew in" / "took me" / "made me his" / "holds me" / "governs me")
5. Sensitive content logged to SENSITIVE-LOG.md

Notable edits per chapter:

| Chapter | Key changes |
|---|---|
| Ch 43 | Added summary; rotated v4, v9; logged v8 sensitive content |
| Ch 44 | Added summary; rotated v3 |
| Ch 45 | Added summary; rotated v1, v2 |
| Ch 46 | Added internal line breaks to prose blocks |
| Ch 47 | Rotated v6 |
| Ch 49 | Rotated v4, v5; logged v3 sensitive content |
| Ch 50 | Added summary; rotated v3, v4, v5 |
| Ch 51 | Added summary; rotated v1, v4, v6, v12; logged v3/v5/v6/v7/v8 sensitive content |

---

## Task C — Missing transliteration (COMPLETE)

Six chapters were missing the transliteration layer (Layer 1b). All added using hyphen-joined style (`muththi-neRi-aRiyaadha`).

| Chapter | File | Status |
|---|---|---|
| Ch 41 | `translated/41-arrputa-pattu.txt` | ✅ Added |
| Ch 42 | `translated/42-cenni-pattu.txt` | ✅ Added |
| Ch 43 | `translated/43-tiru-vartai.txt` | ✅ Added |
| Ch 44 | `translated/44-enna-patikam.txt` | ✅ Added |
| Ch 45 | `translated/45-yattirai-pattu.txt` | ✅ Added |
| Ch 51 | `translated/51-acco-patikam.txt` | ✅ Added |

Ch 07–21 use space-separated transliteration style (`aathiyum anthamum illaa`) — this is correct, not missing.

---

## Sensitive content log

See `SENSITIVE-LOG.md` (local only — not git-tracked).

Chapters with logged entries: Ch 01, 02, 03, 04, 05, 06, 09, 24, 25, 26, 29, 35, 38, 39, 40, 41, 43, 49, 51.

---

## Build commands

```bash
# Rebuild one chapter
python build-chapter.py translated/NN-slug.txt

# Rebuild all chapters
# PowerShell:
.\build-all.ps1

# Git workflow
git add translated/NN-slug.txt chapters/NN-slug.html
git commit -m "..."
git push origin HEAD
```
