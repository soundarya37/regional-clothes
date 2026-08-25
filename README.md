# regional-clothes
Rebozo Decoder

A single-file browser toy that steps through five regional wrapped-cloth traditions — four Mexican rebozos and one Tamil Nadu saree drape — how each is worn, why, and the craft behind it.

Description

Rebozo Decoder is built on one idea: a rebozo and a saree are both, at heart, a single uncut length of woven cloth — no seams, no darts — shaped entirely by folding, tucking, and knotting. It covers five wraps, each distinct in technique and use:

Tenancingo (State of Mexico) — prized for its hand-knotted fringe (punta), worn formally with the knotwork left visible
Santa María del Río (San Luis Potosí) — famously fine, near-transparent weave, worn snug for elegance rather than warmth
Aranza (Michoacán, Purépecha) — bold indigo-and-black striped cloth, worn for daily warmth or knotted into a sling for carrying
Jalisco — less a weaving tradition of its own, more a piece adopted into charro/folklórico dress, worn as a swept, dance-ready accent
Madisar (Tamil Nadu) — the nine-yard saree drape, worn without an underskirt, pleated so both legs move independently; traditional daily wear for many Iyer and Iyengar women, and ceremonial wear more broadly

Each region has its own step-by-step wrap sequence, animated as hand-drawn thread lines over a simple body silhouette, alongside a short cultural note on when and why it's worn that way.

Visual language
Palette — raw cotton background (
#EDEAE0), charcoal ink (
#262A24), añil indigo (
#33415C), cochineal red (
#8C3B3B), thread-green accent (
#6E7B5C) — colors drawn from natural dyes historically used in Mexican weaving (añil/indigo, cochineal/grana)
Type — Fraunces (serif, headlines), IBM Plex Mono (region labels, step counters), Inter (body copy)
No build step — vanilla HTML/CSS/JS in a single file, no dependencies
Installation

No installation needed. Open rebozo-decoder.html in any modern browser.

bash
open rebozo-decoder.html
Usage
Open the file in a browser.
Pick a region from the pill buttons at the top.
Use Prev / Next to step through that region's wrap sequence — each step draws in a new thread line over the body outline.
Read the info panel on the right for the cultural context: who wears it, when, and what the weaving technique is called.
Extending the regions

Each region lives in the REGIONS array near the top of the script, with a matching set of thread paths in threadPathsFor(). To add a region:

Add an object to REGIONS with id, name, place, threadColor, swatches, intro, context, and a steps array (one caption per wrap step).
Add a matching array of SVG path strings to the paths object in threadPathsFor(), keyed by the same id — one path per step.

The step controls, dots, and captions all update automatically from the array lengths.

Accessibility
All controls are keyboard-focusable with visible focus rings
prefers-reduced-motion disables the thread-drawing animation
Layout stacks to a single column below 760px
Roadmap
Add a second Tamil Nadu drape (the more common six-yard nivi-adjacent style) alongside the madisar for contrast
Add a Mexican region from Chiapas or Oaxaca once source material on wrap sequence is confirmed
Add audio pronunciation for region and drape names
Link each region to a source on its weaving cooperative, where one is publicly documented
License

For personal use.
