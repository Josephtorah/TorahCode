# The Tanakh-run web app

The live demonstration: the assembled Exodus 21 machine tested against 64
recorded cases harvested from all 24 books of the Hebrew Bible.

```
python3 app/app.py          # then open http://127.0.0.1:8021
```

Standard library only — no packages to install. Local only: the server
binds 127.0.0.1 (your machine, not the network). Pass a port number to
use one other than 8021.

## The four tabs

* **Scenes** — run any of the 64 catalog scenes. Each run makes real
  calls into the machines in `machines/exo21/` and shows the machine's
  verdict beside the narrative's own outcome, stamped **CONFIRM** (they
  match), **DIVERGE** (they disagree — reported, never hidden),
  **FORWARD** (depends on law not yet derived), or **NO-VERDICT-IN-TEXT**
  (the text records no ruling to compare). Current scoreboard:
  43 / 5 / 7 / 9. Every verse cited renders as Hebrew with word-by-word
  English underneath, from `data/tanakh.sqlite` + `data/lexicon.json`.
  A minority of scenes (22 of 64: lexicon surveys, forward stubs, and
  parallel-passage comparisons) are recorded observations rather than
  machine runs — their panels carry notes and citations but no
  machine-call list.

* **Custom facts** — twelve form-bound engines (homicide, the goring ox,
  theft tariffs, injury awards, and the rest): enter your own fact
  pattern, watch the chapter rule on it.

* **Replay** — the chronology fold: the scenes in narrative-time order,
  the world's standing rules and open debts accumulating as you scrub.

* **Summary** — the scoreboard by stamp and mode, and the machine
  underneath: three blocks, 117 witnessed claims, the 60-edge dependency
  proof.

`scene_catalog.json` is the scene data: fact patterns, references, the
text's own outcome, chronology keys, and replay-state notes for every
scene.
