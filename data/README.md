# The data layer

Three files, all self-contained — nothing here requires a download or an
account. Provenance and licenses for everything below: see
`ATTRIBUTION.md` at the repository root.

* **`tanakh.sqlite`** (25 MB) — the complete Hebrew Bible (all 24 books,
  23,213 verses): the Westminster Leningrad Codex text (public domain)
  with word-level Strong's lemma numbers and morphology codes from the
  Open Scriptures Hebrew Bible project (CC BY 4.0). Tables: `verses`
  (book, chapter, verse), `words` (Hebrew form, lemma, morphology, in
  verse order).

* **`lexicon.json`** (439 KB) — the English gloss layers for interlinear
  display: Strong's-number → gloss (3,409 entries, the bridge that lets
  Torah-derived glosses annotate any verse in the 24 books),
  unpointed-spelling → gloss (12,847 entries, the fallback), and a small
  hand supplement. Derived from Strong's Concordance (1890, public
  domain) plus project hand glosses. A reading aid, not a translation.

* **`units_index.json`** — the 97 derivation units (id, book, verse span,
  title). The dependency proofs in `machines/` resolve backward edges
  against these spans; the full runnable derivations are in `units/`.
