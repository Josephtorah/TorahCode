# The inheritance visualizer

One page, no server needed — open `inheritance.html` in any browser (or
double-click it).

It draws the chapter's proven inheritance as a flow: on the left, the 20
**donor blocks** — 11 from Genesis, 8 from Exodus, 1 from Leviticus —
whose verses the law of Exodus 21 imports from; on the right, the 11
**law groups** of the chapter that consume them; between them, the **31
verified edges** of the dependency proof (every edge on this page is one
the machine's `verify_dependencies()` proved — the page's data was
cross-checked against the machine's proof, edge for edge).

Interaction:

* **Click a donor block** — its edges light up, showing every law that
  inherits from it. Click a law group — the reverse: every donor it
  draws on.
* **The "verse + code" chip** on any block opens the full detail: the
  Hebrew verse with its English gloss, what the verse contributes, and
  the actual declaration from the machine code in `machines/exo21/`
  with the proof line that verified it.
* **Step** walks the flow one donor at a time, in canon order.

Note the double donors: the Decalogue's theft-ban (Exodus 20:13) feeds
three different laws (the murder warning, the theft warning, and the
pierced ear), and the Joseph sale (Genesis 37:28) feeds two (the
kidnapping test case and the national precedent) — single verses serving
as load-bearing beams across the chapter.
