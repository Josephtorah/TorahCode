# Roadmap — the simulation direction

The instrument so far is a **judge**: you bring it a case, it rules
(step 7 of `PROCESS_OVERVIEW.md`). The next stage turns the same laws into
**physics**: a world where every event passes through every law
automatically, where liability persists as state across years and
generations, and where the computed consequences can be checked against
what the narrative itself reports.

## The prototype that exists

`sim/house_of_david.py` — run it (`python3 sim/house_of_david.py`). It
loads the real Exodus 21 machines, registers three laws as physics
(homicide, the theft tariff, collection), and folds the recorded events
of the house of David through them: the taking of Bathsheba as the ewe of
Nathan's parable, the killing of Uriah, the four discharges, Joab's
murders, Solomon's execution of Joab.

Its first run surfaced two findings, both kept in the file's header:

1. **The correct ledger ends OPEN.** After the fourfold discharges,
   David's Heaven-debt stands at 1 — and that is right, not a bug: the
   four answer the *ewe*; the open 1 is the blood of Uriah, which the
   text never closes ("the sword shall never depart from your house").
   The naive balance check expected zero; the doctrine says one. Lesson:
   validation must encode doctrine, not arithmetic.
2. **A live dispute surfaced by itself.** Joab's blood-debts sit on
   Heaven's docket; the coded execution clears only the court docket —
   which is exactly the recorded dispute between the Vilna Gaon and the
   Netziv on whether the crown collects Heaven's ledger (Solomon's own
   words: "the LORD shall RETURN his blood"). The simulation reproduced
   a centuries-old machloket ("division," a recorded dispute) as a
   design decision, uninvited.

## The nine components of the full simulation

The design of record. Each names what exists and what is missing.

1. **The clock and the era table.** World-time with named eras; laws gate
   on era (before Sinai, only the Genesis 9 blood-charter physics
   operates). Exists: chronology keys on the catalog scenes. Missing:
   the era table as a first-class object.

2. **Entities with persistent identity.** People, **houses** (debts
   attach to houses across generations — David's, Saul's, Ahab's),
   animals with legal state (the תם/מועד, "innocent/forewarned," ox),
   property, places. Missing: the house-lineage layer.

3. **The ledgers — liability as state.** The court docket, Heaven's
   docket, ownership, slave-term clocks, standing verdicts, covenant
   states (the broken release-covenant of Jeremiah 34 as a breachable
   world object). The sketch's two dockets are the seed. This is the
   simulation's heart.

4. **The law layer — chapter machines as pluggable physics.** Every
   event passes through every registered law, unasked. Each further
   chapter derived under the method laws becomes a new physics module
   (the Leviticus 13 quarantine timers, the Leviticus 25 land
   schedulers, the Numbers 35 refuge system). Exists: one chapter of
   roughly ten planned. **The simulation and the derivation program are
   the same project** — deriving law *is* building the world.

5. **The jurisdiction router.** Every event routes to its forum: court
   (witnesses + warning + a seated court), crown, war, foreign, ban, or
   Heaven. The Tanakh run proved routing is load-bearing — several of
   its hardest cases were routing questions, not verdict questions.
   Missing: one explicit router all laws consult.

6. **Institutional state flips.** The law's own runtime flags change
   with narrative events: refuge exists only after the conquest;
   Shiloh's asylum lapses; the Temple turns capital jurisdiction on; the
   high court's exile from its chamber turns it off; the jubilee
   stopping puts the Hebrew-slave module to sleep (the machines already
   carry the flag). Same act, different century — lawfully different
   process.

7. **The prophet channel.** Prophets read Heaven's ledger aloud — Nathan
   announces exactly what the dockets already hold. As a component: an
   observer that reports open ledger state at narrative moments, and the
   validation it enables — does every prophetic indictment in the corpus
   match an open entry in the simulated ledger?

8. **The diff engine.** Computed state vs. declared state, sharpened by
   the sword-clause lesson above: balance checks must encode doctrine —
   a ledger that ends OPEN can be the correct ending.

9. **The validation harness and display.** The 64 scene stamps as a
   regression baseline (any simulation change that flips a CONFIRM must
   answer for it); the web app as the window; every surface glossed per
   method law 8.

## The fence

**No invented events — ever.** The simulation computes law over the
text's own events; it never generates history. A what-if sandbox may
exist someday, fenced and labeled, never mixed into the record. This is
method law 6, and it is what keeps the simulation an instrument of
verification rather than of fiction.
