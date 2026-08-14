# The simulation sketch

```
python3 sim/house_of_david.py
```

The Exodus 21 machine as a **world**, not a judge: laws fire
automatically on every event, liability persists as ledger state, and
the computed consequences are checked against what the narrative
reports. This prototype runs the recorded events of the house of David
through the real chapter machines and prints the ledger as it unfolds —
ending, correctly, with David's Heaven-debt OPEN at 1 (the blood of
Uriah, which the text never closes).

The two findings of the first run are documented in the file's header.
The full design — nine components, and the fence against invented
events — is `docs/ROADMAP_SIMULATION.md`.
