# The derivation units

Each file here is one **derivation unit**: a contiguous span of verses
(Genesis 1:1 through Exodus 21:37, continuously) whose content was derived
under the method laws and frozen. The file walks the span verse by verse —
the Hebrew text, its English translation, and the machine calls that
register every event, fact, standing constraint, and open flag the verses
carry — and ends with an assertion block baked from the derivation
machine's actual final state. **Running a unit file re-proves it**: if the
library ever drifted from the machine that derived the unit, the
assertions go red.

```
python3 units/gen_01_creation_boot.py     # run one unit
python3 units/run_all.py                  # run all 97, in canon order
```

`machine.py` is the six-register machine library the units run on
(TIME / WORLD / REGISTRY / SPECS / TESTS / LEDGER, plus a FLAGS side
channel). Its contract: flags never auto-resolve, verdicts are data, and
disputed or uncertain readings stay open rather than being silently
settled.

These are **generated files** — renderings of the project's canonical
frozen derivation records, produced by the research repository's
generator. Do not hand-edit them; a unit that needs improving is
regenerated at the source. The index of all 97 units (spans and titles) is
`data/units_index.json` — the same index the Exodus 21 machines' dependency
proofs resolve against.

The full oral-inversion depth (scan ledgers, witnessed-claim manifests)
exists for the Exodus 21 law units — see `scans/`. The earlier narrative
units were derived under the same reading laws with a lighter recorded
witness layer; re-derivation of all units at full law-era depth is ordered
and ongoing in the research repository.
