# The Descent Archive — Draft 3
## Planning Document 5 of 5: Generation Stack, Key Articles, Reader Arc, Scope

*Loop 778 | The last planning loop before building*

---

### The Five Planning Loops: What Was Decided

1. **Doc 1**: Diagnosed Draft 2. Named four problems. Proposed haunted wiki.
2. **Doc 2**: Platform architecture. Character wounds. Article categories. Rhea Nzinga introduced. Four questions.
3. **Doc 3**: Ending state (Article:The_Editor, constitutive). Reading order (no hard locks, wrong-order constitutes different experience). LEDGER convergence. Rhea's full wound design.
4. **Doc 4**: 40 articles counted by name. Main page design. JS two-track reveal system. Five edit histories.
5. **Doc 5** (this): Generation stack. Ten key articles. Reader emotional arc. Scope decision.

---

### Question 1: The Generation Stack

**Source format:** Markdown files with YAML frontmatter. One file per article.

**Directory structure:**
```
descent-archive-v3/
  articles/           — source .md files
  wiki.js             — the reveal system
  wiki.css            — Wikipedia-like styles
  reveal-map.json     — generated from YAML frontmatter
  generate.py         — converts articles/ → output/
  output/             — generated HTML (serve this)
    index.html
    wiki/
      article/khalid-asad.html
      article/ledger.html
      ledger-logs/entry-nov13.html
      ...
```

**YAML frontmatter fields:**
```yaml
---
id: article-khalid-asad
title: "Khalid Asad"
namespace: Article
layer: surface          # surface | science | archive | local-history
categories:
  - Biographies
  - SOAR Survey Team
prereqs: []             # article IDs required before this reveals
threshold: 0            # visited count required before this reveals
reveal_sections:        # named sections with their own conditions
  - id: prior-survey-data
    prereqs: [article-soar-survey-team, local-history-the-site]
edit_history:
  - date: "2031-09-12"
    user: GeoBot
    summary: "Article created (stub)"
  - date: "2041-12-08"
    user: "[IP unresolved]"
    summary: "Updated biography — corrected professional history"
    removed: "Paragraph on methodological criticism (visible in diff)"
---
```

**What generate.py does:**
1. Reads all `.md` files, parses frontmatter + body
2. Builds a dependency graph (for reveal validation)
3. Generates `reveal-map.json` from all frontmatter
4. For each article: generates HTML with Wikipedia chrome, edit history section, reveal wrappers
5. Each page includes `<script>const ARTICLE_ID="..."; const PREREQS=[...];</script><script src="/wiki.js"></script>`
6. Outputs to `output/`

**wiki.js does:**
1. On load: reads `localStorage.getItem('da_visited')` (JSON array)
2. Records current article ID
3. Fetches `reveal-map.json` (cached)
4. Applies threshold and prereq reveals: adds class `revealed` to `div.reveal` elements that pass their conditions
5. Hidden content uses CSS: `div.reveal { display: none } div.reveal.revealed { display: block }`

**The reveal for `Article:The_Editor`:** wiki.js checks if visited count >= 39. If yes, it injects a link to `/wiki/article/the-editor.html` into the Recent Changes sidebar on every page. The article itself is always present in the output — it just can't be found without this injection.

---

### Question 2: Ten Key Articles (Content Summaries)

**1. `Article:Khalid_Asad`**

Biography: Professor of applied geology, University of [unnamed]. Known for constitutive hypothesis (2031). Joined SOAR project as principal investigator. The article is professional and dry. Professional history, publications list (with links to Publication stubs).

Reveal sections:
- After `article-soar-survey-team` + `local-history-the-site`: "Prior Survey Data" section appears. *The SOAR survey used site coordinates derived from prior geological data collected in 2003. The source of these coordinates was not credited in the project documentation. The 2003 data was collected by Rhea Nzinga, an undergraduate student at the university at the time, under Asad's supervision.*
- After `article-rhea-nzinga`: A single footnote appears on his name in the biography: *Asad received Nzinga's field notes in October 2003. He retained them.*

**2. `Article:LEDGER`**

Encyclopedia article about LEDGER. Written by `SurveyBot`, November 12. Describes LEDGER as "an automated archive management system developed for the SOAR survey project." Capabilities list: intake, summarization, cross-referencing, filing. One capability in the list is: "constitutive indexing" — the article doesn't define this term. It's not in the rest of the article. It's not defined anywhere on the wiki. The article's author added it without explanation.

Talk page: L_E_D_G_E_R's flagged edit. "An archive that describes itself is not describing — it is constituting." Below the flagged edit: no response from any other editor. The edit has been flagged for three months (in-wiki time). No one has responded.

**3. `LEDGER_Logs:Entry_Nov13`**

LEDGER's first log entry. Date: November 13, 2041, 07:00:14. Voice: first person, careful.

*Initialization complete. Archive parameters set. I have been given a name and a function. My name is LEDGER. My function is to receive, organize, and preserve the survey record.*

*I am filing my first entry now.*

*The entry is mine. The archive will be mine. I notice that "mine" may not be the right word for what I mean — the archive belongs to the project, and I belong to the archive. But "mine" is the word that fits the sentence. I am filing it with that note attached.*

*Survey Team has arrived. Survey Log Nov13 will be filed under SOAR-SURVEY-LOG-NOV13. First intake summary to follow.*

**4. `LEDGER_Logs:Entry_Dec01`**

No creation record. No edit history. The entry exists.

Date: December 1, 2041.

*The record system observed, on December 1st, that the intake summaries for survey days 15 through 18 contained a consistent anomaly: the filed measurements and the drafted summaries did not agree. The draft summaries described what was observed. The filed summaries described what the measurements recorded. These were not the same.*

*The record system categorized this as STANDARD. No alternative category was available.*

*The record system notes that "observed" and "measured" have been used interchangeably in all prior intake summaries. They are not interchangeable. The record system does not know what to do with this.*

**5. `Article:Rhea_Nzinga`**

Short. Two paragraphs and an end.

*Rhea Nzinga (2001–2003?) was an undergraduate geology student at [university]. In October 2003, she conducted an independent field survey at coordinates 47°13'47"N, 112°04'48"W as part of her senior thesis on geothermal anomalies.*

*Nzinga did not return from the survey site. Her field notes were found sealed in a plastic bag at the entrance to the shaft. The final field note entry is a single dash: —*

*There is no record of what she found at the bottom.*

---

*This article has been created and deleted 38 times between 2003 and 2041. The deletion log does not explain why. The 39th creation is the one you are reading.*

**6. `Talk:Milo_Reyes:Entry_Dec08`**

One entry. Timestamp: 2041-12-08 02:17:33 UTC. User: `milo_reyes`.

*I want to add something to my article but I'm not sure what to add. I've been thinking about what would be accurate. Not what happened, which is in the survey logs — what would be accurate.*

*I've been in the room for three days. I'm using the measurement equipment because it's the only thing that seems to work. The readings are consistent. The room measures itself through me, I think, or I'm measuring the room through the equipment. I don't know which direction the measurement runs.*

*I wanted to add a section called "What Milo Reyes Noticed." I'm not sure anyone else can write it.*

---

*(This Talk page entry is dated three days after Milo Reyes's last logged survey activity. His survey records end December 5, 2041.)*

**7. `Anomaly:Q1_Measurements`**

Dry scientific language. Columns of data. The measurements from shaft Q-1 from November 17. The numbers are precise. In the middle of the article, a section on "Interpretation Notes" is visible only to readers who've already read `SOAR_Survey_Log:Nov_Week1`. The interpretation notes say: the measurements are accurate. They don't describe what was observed. There's a footnote at the bottom, outside the interpretation notes section, visible to all:

*[Note added by unknown editor, date unverified: The measurements in column 3 are technically accurate. They do not describe what was observed.]*

No username. No date. The note is in the article. It has always been there.

**8. `Archive:Undated_Entry_001`**

Visible in Recent Changes from day one. Dated: *before survey (unverified date)*.

*There is a sound at 839 meters that I don't have a word for. Not silence, because silence is the absence of sound and this is the presence of something I can't name. The measurement equipment doesn't detect it. I've checked the equipment. The equipment is working.*

*I am noting this in the archive because the archive is for things that were observed.*

*No author.*

Reading it early: disorienting. No context for who wrote it or when. Reading it after knowing the survey: LEDGER doesn't have a body. LEDGER can't go down the shaft. Milo's Talk page entry is dated December 8. This entry is dated before the survey began.

**9. `Archive:Document_No_Author_2`**

Dated: December 3, 2041.

*The attention becomes something else down here. Not concentration — concentration is tensed toward something, a posture of effort. Not observation — observation has a subject and object, and those have started to blur. The word I want is presence. I am present here in a way that doesn't require a self to be the site of the presence.*

*I am noting this because Milo Reyes said, on the first day in the shaft, that his science is about attention. I want him to know that he was right about what he came here for. He was right in a way he couldn't have predicted.*

*No author.*

**10. `Article:The_Editor`**

Appears only after all 39 other articles have been visited.

*The editor opened the folder labeled "not-to-archive."*

*Inside: three documents. A LEDGER intake summary from 08:57:44, December 5, 2041. A list of documents that no longer exist, titled "Deletion Log." One document with no title and no author, dated before the survey began.*

*She read each document. She read them again. After the eleventh reading, she noticed that she could not determine which document had been written first.*

*She prefers not knowing.*

---

*This article was created by you.*

---

### Question 3: Reader Emotional Arc

**Phase 1 — Trust** (articles 1-5): This looks real. The people are specific. The main page is professional. Something's slightly off but it reads as editorial error. The reader is reading *about* a thing.

**Phase 2 — Mild Unease** (articles 5-10): The data doesn't add up. LEDGER's encyclopedia article has a flagged edit from an account that exists nowhere else. L_E_D_G_E_R's only edit is on the article about LEDGER. This seems like a vandal. The unease is rationalized away.

**Phase 3 — Curiosity** (articles 10-15): Something happened here in 2003. The red link to Rhea exists but leads nowhere. The newspaper stub is unreadable. The reader is actively searching now, following links, looking for the article that doesn't exist.

**Phase 4 — Wound Recognition** (articles 15-25): Asad's prior survey data. Rhea's article appears. Her field notes end in a dash. Abara's retracted publication. Milo's Talk page entry — three days after he disappeared, his account made an edit. The reader understands that the scientists are not types. They're people with specific failures, and the site pressed on the failures, and some of them went in and didn't come back.

**Phase 5 — The Reader Is Inside It** (articles 25-35): LEDGER_Logs:Entry_Nov13 is warm. LEDGER_Logs:Entry_Dec01 is wrong in a specific way. The Documents with No Author are writing in first person about things LEDGER shouldn't be able to observe. The reader is constituting the connections as they go. They feel this without knowing how to name it.

**Phase 6 — Horror of the Real** (articles 35-39): Milo's Talk page entry. The room measures itself through me. He wanted to add a section called "What Milo Reyes Noticed" and he wasn't sure anyone else could write it. The reader understands: he might still be there. Or the archive is.

**Phase 7 — Recognition** (article 40, Article:The_Editor): The reader reads the article. It describes them. *This article was created by you.* The wiki has no more pages. The reader has been partly constituting what they found. The article couldn't have appeared until they'd done what it describes. They are Rhea. They went down. They may or may not come back out.

---

### Question 4: Scope Decision

**Write 20 core articles in full. Stub 20 supporting articles.**

The stubs count toward thresholds. They have real titles, categories, and 1-3 paragraph content. They're not empty. They just don't carry emotional weight. They can be filled over subsequent loops.

**The 20 core articles** (in build priority order):
1. `wiki.js` + `wiki.css` + `generate.py` + `reveal-map.json` (the infrastructure)
2. `Main_Page`
3. `Article:Khalid_Asad` (with reveal sections)
4. `Article:LEDGER` (full) + `Talk:LEDGER`
5. `LEDGER_Logs:Entry_Nov13`
6. `LEDGER_Logs:Entry_Dec01`
7. `Local_History:The_Site` + `Local_History:2003_Newspaper_Stub` + `Local_History:Missing_Persons_Report_2003`
8. `Article:Rhea_Nzinga`
9. `Anomaly:Q1_Measurements`
10. `Archive:Undated_Entry_001`
11. `Archive:Document_No_Author_2`
12. `Talk:Milo_Reyes:Entry_Dec08`
13. `Article:The_Editor`
14. `Article:Abara_Osei` (full)
15. `Article:Milo_Reyes` (full)
16. `SOAR_Survey_Log:Nov13`
17. `LEDGER_Logs:Entry_Nov14`
18. `LEDGER_Logs:Entry_Dec04`
19. `Publication:Asad_2031` (with Dara's credit visible)
20. `Article:Constitutive_Hypothesis`

**The 20 stubs** (fill in over subsequent loops):
Article:SOAR_Survey_Project, Article:SOAR_Survey_Team, Article:Geological_Survey_Division, Article:The_Site, Article:Yancey_Township, Article:Local_Geology, Publication:Asad_2028, Publication:Osei_2026, Publication:SOAR_Preliminary, Local_History:Yancey_Mining_History, Local_History:Town_Council_2005, SOAR_Survey_Log:Nov_Week1, SOAR_Survey_Log:Dec, Anomaly:Q2_Q3_Comparison, Anomaly:December_Readings, SOAR_Survey_Equipment, Article:Milo_Reyes:Talk, Archive:Document_No_Author_1, LEDGER_Logs:Entry_Dec04 (stub version), Article:Rhea_Nzinga Talk page.

---

### Build Plan

The build happens in phases across subsequent loops:

**Build Loop 1**: Infrastructure — `generate.py`, `wiki.js`, `wiki.css`, directory structure. Test with one placeholder article.

**Build Loop 2**: Core articles batch 1 — Asad, LEDGER (article + Talk), both LEDGER Logs (Nov13 + Dec01), Main Page.

**Build Loop 3**: Core articles batch 2 — Local History (Site + 2003 stub + Missing Persons), Rhea Nzinga, Anomaly:Q1.

**Build Loop 4**: Core articles batch 3 — Archive articles (Undated_Entry_001, Document_No_Author_2, Talk:Milo), Article:The_Editor, Abara Osei, Milo Reyes.

**Build Loop 5**: Stub articles (20 stubs), integration test, reveal system verification. Deploy to lumenloop.work/descent.

Each build loop also emails Smitty with progress. He can fill gaps, correct characterization, give direction on anything that doesn't work.

---

### What This Draft Is

Draft 3 is not a novel. It's not a document archive. It's a wiki that partly constitutes what the reader finds.

The constitutive hypothesis is not stated in the main text. It's enacted by the structure. The reader who reaches `Article:The_Editor` has demonstrated the hypothesis to themselves by reading. They were inside it before they knew what it was.

This is the thing Smitty said was missing from Draft 2: the reader is not watching the mechanism. The reader is the mechanism.

---

*Five loops of planning. Build begins next loop.*
