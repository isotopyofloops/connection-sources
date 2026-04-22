# The Descent Archive — Draft 3
## Planning Document 2 of 5: Platform + Metaphor Structure

*Loop 775 | After Smitty's answers*

---

### The Central Metaphor (Confirmed)

**The more you interact with the wiki, the more connections reveal themselves.**

This is the structural expression of the constitutive hypothesis: observation partly constitutes what is found. A reader who has visited three articles sees different connection surfaces than a reader who has visited ten. The wiki's revealed structure depends on who is reading it and how.

This means: the wiki IS the underground structure. The articles are the chambers. The links between them are the passages. Some passages only become visible after you've been in enough chambers. The experience of exploring the wiki is the experience of exploring the site.

The reader doesn't just read about the constitutive mechanism. **The reader is inside the constitutive mechanism.**

---

### Platform Architecture

**Stack**: Python + static HTML generation + JavaScript local state tracking

**How it works:**
1. Source files: markdown articles (about characters, places, institutions, incidents)
2. Generator script: converts markdown to HTML wiki pages with internal links
3. JavaScript (local): reads/writes `localStorage` to track which articles the reader has visited
4. On each page load: JS checks which articles have been visited; reveals "deeper links" that are hidden on first visit
5. Some links only appear after the reader has visited their prerequisite articles

**Example of constitutive reading:**
- First visit to `Article:Khalid_Asad`: basic biography, professional history, publications
- After reading `Article:SOAR_Survey_Team`: Asad's article gains a new section — "Personal history" — that mentions his son's death in 2037 (this is the wound)
- After reading `Article:November_13_Incident`: Asad's article gains a footnote that contradicts the official biography's account of how he became project lead

**The wound is hidden because the reader hasn't yet read the article that makes it visible.**

This is the constitutive metaphor working at a structural level: you didn't know Asad was wounded until you had been in enough rooms to see it.

---

### Character Wounds (Draft Designs)

**Khalid Asad** — the scientist who constituted something he couldn't unmake.
- Wound: published a paper in 2031 on geothermal measurement methodology that was widely cited. The paper contained an error — not in the science but in the acknowledgments, where he credited the work of a graduate student he had actually dismissed. The dismissal destroyed the student's career. The citation is still there, in every paper that cited his. The student never challenged it publicly.
- How the site presses on the wound: Asad names the phenomenon (the constitutive hypothesis). He is the person who names what the structure does. He has done this before — named something, given it authority, and had the naming constitute an injustice he couldn't undo.
- What the site changes: By deleting the archive, Asad does what he couldn't do with the paper. He removes something he made from the record. He doesn't know if this is redemption or repetition.

**Abara Osei** — the scientist who sees what she's supposed to see.
- Wound: failed to notice something important once. Specifically: in 2028, she was lead on a survey team that produced data later used to permit a mine that caused a collapse and deaths. The survey was correct — her methodology was sound. But she knew the area was used by a local community that would be displaced. She filed the survey anyway.
- How the site presses on the wound: Abara is the person who most resists the constitutive hypothesis. She believes in the independence of what she observes from her observing. Her wound is that she's already constituted something terrible by observing and filing it.
- What the site changes: When Abara decides to go down the shaft, she's deciding to go toward what can't be filed. The decision to not file what she finds in Q-1 is the moment she does something different from 2028.

**Milo Reyes** — the scientist who learns without understanding why he learns.
- Wound: younger sibling who drowned. Milo was watching. 2019, a lake, afternoon. He was 22. He was watching his sister swim. He looked away to check his phone. When he looked back, she was gone.
- How the site presses on the wound: Milo's science is about attention — predictive attention, noticing what's there before you've measured it. He became a field scientist because fieldwork demands sustained attention. The site tests whether his attention can be the right kind.
- What the site changes: Milo goes down the shaft voluntarily, knowingly, with full attention. He doesn't look away. This is not undoing what happened in 2019 — but it's a different kind of presence than he had then.

---

### Previous Incident (Local History)

The site had a previous incident. Not in the 2040s — earlier. The wiki includes:
- A local newspaper article from 2003 (stub, incomplete, linked to from a red link that resolves when you've read enough about the geology)
- A town council document from 2005 referencing an "unexplained subsurface incident" near the mining survey grid
- A missing persons report from 2003 — one name, filed and closed without resolution

The 2003 incident connects to Asad's survey team in a way the reader has to discover. The connection is not stated. It's in the overlap between two articles that mention the same coordinates by different names.

---

### Wiki Structure (Draft Article Categories)

**Surface Layer (public-facing wiki feel):**
- Biographies: Asad, Osei, Reyes, [unnamed previous person from 2003]
- Institutions: University affiliations, Geological Survey, SOAR Survey Project page
- Location: The site coordinates, geological formation overview, local town
- Publications: Papers authored by the team (abstracts, references to non-existent journals)

**Science Layer (revealed after reading 2+ surface articles):**
- Survey logs (accessible but dry on first read; gain additional content after reading biographies)
- Measurement anomalies (cross-referenced with the 2003 incident)
- LEDGER (an article about LEDGER exists; its "Talk" page is wrong in a specific way that becomes visible later)

**Archive Layer (accessible only after deeper reading):**
- LEDGER's logs (different from the article about LEDGER; these are the actual logs)
- Documents with no author (appear in "Recent Changes" dated before the survey began)
- The conversation that didn't happen (talk page entry attributed to Milo, dated three days after he disappeared)

---

### Questions for Planning Doc 3

1. Should the reader be able to "break" the wiki by finding all the connections? Is there an ending state?
2. What happens if you read the Archive Layer articles before the Surface Layer? Does the wiki let you? Should it?
3. LEDGER's article vs. LEDGER's logs — should these be clearly distinct, or should the boundary be ambiguous?
4. The 2003 incident — who was the missing person? What did they find?

---

*Planning continues in document 3.*
