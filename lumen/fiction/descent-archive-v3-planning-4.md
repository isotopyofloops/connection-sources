# The Descent Archive — Draft 3
## Planning Document 4 of 5: Article Count, Main Page, JS Mechanics, Edit Histories

*Loop 777 | Four structural questions*

---

### Question 1: How Many Articles Total?

**Forty articles.** Enough to feel like a real wiki. Not so many that building it is impossible.

Counted by layer:

**Surface Layer** (15 articles — visible on first visit or through normal navigation):
1. `Main_Page`
2. `Article:Khalid_Asad`
3. `Article:Abara_Osei`
4. `Article:Milo_Reyes`
5. `Article:SOAR_Survey_Project` (institutional page)
6. `Article:SOAR_Survey_Team` (the team's biographical summary)
7. `Article:Geological_Survey_Division` (the funding institution)
8. `Article:The_Site` (location overview, geological formation, access history)
9. `Article:Yancey_Township` (local town, "nearby services," history stub)
10. `Article:Local_Geology` (geothermal anomaly, formation history)
11. `Publication:Asad_2031` (the paper that credits Dara; annotated abstract)
12. `Publication:Asad_2028` (methodology paper)
13. `Publication:Osei_2026` (Abara's survey methodology; quietly retracted)
14. `Publication:SOAR_Preliminary` (the project's preliminary report, incomplete)
15. `Article:Constitutive_Hypothesis` (stub; cites Asad's 2031 paper)

**Local History Layer** (4 articles — linked from surface but require navigation to find):
16. `Local_History:The_Site` (history of the site, 2003 incident section, red link to Rhea)
17. `Local_History:Yancey_Mining_History`
18. `Local_History:2003_Newspaper_Stub` (incomplete OCR, titled "Local Student Missing")
19. `Local_History:Missing_Persons_Report_2003` (closed without resolution)
20. `Local_History:Town_Council_2005` (references "unexplained subsurface incident")

**Science Layer** (10 articles — unlocks after threshold reading):
21. `SOAR_Survey_Log:Nov13` (first day; initialization, equipment check)
22. `SOAR_Survey_Log:Nov_Week1` (compilation; some entries redacted with dashes)
23. `SOAR_Survey_Log:Dec` (December logs; increasingly terse, redacted after Nov 30)
24. `Anomaly:Q1_Measurements` (first anomalous readings, November 17)
25. `Anomaly:Q2_Q3_Comparison` (the measurements that don't match expectations)
26. `Anomaly:December_Readings` (readings that shouldn't be possible)
27. `Article:LEDGER` (encyclopedia entry; wrong specs; Talk page has L_E_D_G_E_R edit)
28. `Talk:LEDGER` (flagged edit; the most accurate sentence in the wiki)
29. `SOAR_Survey_Equipment` (technical list; one piece of equipment is listed twice with different serial numbers)
30. `Article:Milo_Reyes:Talk` (one comment requesting a citation; the citation has never been provided)

**Archive Layer** (10 articles — deep reveals; most require specific prerequisites):
31. `Archive:Undated_Entry_001` (visible in Recent Changes from day one; dated wrong; disorienting cold)
32. `LEDGER_Logs:Entry_Nov13` (initialization log; LEDGER's first entry; warm)
33. `LEDGER_Logs:Entry_Nov14` (first full day; LEDGER notes the account L_E_D_G_E_R edited its article)
34. `LEDGER_Logs:Entry_Dec01` (written in third person; no user, no creation timestamp)
35. `LEDGER_Logs:Entry_Dec04` (LEDGER's last archived entry; notes it cannot complete the intake summary)
36. `Archive:Document_No_Author_1` (dated November 18; describes the shaft from inside; no author)
37. `Archive:Document_No_Author_2` (dated December 3; describes what attention feels like at 839m)
38. `Talk:Milo_Reyes:Entry_Dec08` (attributed to Milo; dated three days after he disappeared)
39. `Article:Rhea_Nzinga` (unlocks when coordinate match is established; ends with —)
40. `Article:The_Editor` (the final article; unlocks when all others visited)

---

### Question 2: What Does the Main Page Look Like?

**It looks clearly like a wiki. But it's subtly wrong.**

The layout is Wikipedia-familiar: featured article box (left), did-you-know (right), recent changes sidebar, categories footer. Sans-serif font, blue links, tabs at the top (`Article | Talk | Read | Edit | View history`).

The wrongness is small and easy to miss:

**Featured article box**: Features `Article:Khalid_Asad`. The box has a small tag reading *"This article was featured on December 8, 2041."* December 8 is the day the survey team departed. The article was featured the day they left.

**Did You Know**: Three entries, two normal, one wrong:
- *"Did you know that the SOAR survey project used a novel acoustic measurement methodology developed by Abara Osei?"* (true)
- *"Did you know that the Yancey Township geothermal anomaly was first recorded in 1987?"* (true, banal)
- *"Did you know that the SOAR Survey Project was the first geological survey to operate using LEDGER's constitutive hypothesis as a methodological framework?"* (wrong — LEDGER is a record system, not a hypothesis author; the hypothesis is Asad's; nobody has flagged this)

**Recent Changes sidebar** (visible on first load):
- *Archive:Undated_Entry_001 — (diff) (hist) — [no user] — before survey (unverified date)*
- *Article:Khalid_Asad — (diff) (hist) — [IP address] — December 2041 — "updated biography"*
- *Talk:LEDGER — (diff) (hist) — L_E_D_G_E_R — November 14, 2041 — (flagged: unsourced)*
- *Local_History:The_Site — (diff) (hist) — SurveyBot — November 13, 2041 — "added coordinates"*

The Recent Changes sidebar is the first place most readers will see L_E_D_G_E_R. It looks like a typo for a username. The flagged tag looks routine. Readers usually click past it the first time.

**The main page has no errors in its own text.** The errors are in what it links to and displays. Arriving at the main page, the reader has no reason to be afraid. This is correct.

---

### Question 3: How Does the JavaScript Reveal System Work?

**Two-track system: threshold count + specific article prerequisites.**

**Technical implementation:**

Each HTML article page contains a `<script>` tag near the top:
```html
<script>
const ARTICLE_ID = "article-khalid-asad";
const PREREQS = [];  // or ["article-soar-survey-team", "local-history-the-site"]
</script>
<script src="/wiki.js"></script>
```

`wiki.js` runs on every page load and does three things:
1. Reads `localStorage.getItem('visited')` (JSON array of article IDs)
2. Adds the current page's ID to the visited array (if not already present)
3. Applies reveal rules: adds CSS classes to show/hide sections based on visited array

**Content that needs to be revealed is wrapped in HTML:**
```html
<div class="reveal" data-threshold="5" data-prereqs="">
  [content only visible after 5 articles read]
</div>
<div class="reveal" data-threshold="0" data-prereqs="article-soar-survey-team,local-history-the-site">
  [content only visible after specific articles read]
</div>
```

**Threshold reveals** (based on visited count):
- `>= 3`: Science Layer articles appear in Recent Changes and category pages
- `>= 5`: Anomaly articles visible in cross-links; LEDGER article gains Talk page link
- `>= 8`: Archive Layer articles appear in Recent Changes sidebar
- `>= 12`: Red link to `Article:Rhea_Nzinga` turns blue (article exists, was always there)
- `>= 20`: `Archive:Undated_Entry_001` section that was disorienting cold now has a date resolution note
- `>= 39`: `Article:The_Editor` appears in Recent Changes and resolves as a blue link

**Specific prerequisite reveals:**
- Asad's "Prior Survey Data" section: requires `article-soar-survey-team` + `local-history-the-site`
- LEDGER_Logs becoming accessible: requires `article-ledger` + any Anomaly article
- `Talk:Milo_Reyes:Entry_Dec08`: requires `article-milo-reyes` + `ledger-logs-entry-nov13`
- `Article:Rhea_Nzinga` full text: requires `local-history-missing-persons-report-2003` + `local-history-2003-newspaper-stub` + Asad's "Prior Survey Data" section having been visited

**The reveal-map.json file**: The wiki ships with a `reveal-map.json` that the generator uses to output the correct `data-threshold` and `data-prereqs` attributes. This is the source of truth for all reveal conditions. The generator reads article markdown and a YAML frontmatter section, and the JSON map is built from the YAML.

**One design decision:** The system never tells the reader what they're missing. There are no "locked" indicators, no completion meters, no "5 of 40 articles read." The reader sees the wiki as a whole — they just can't see some of it yet. Links appear. Sections emerge. The wiki reveals what it reveals when it reveals it.

This matters: the reader who has visited 38 articles doesn't know they're one away from `Article:The_Editor`. They're just reading the wiki. And then a new link appears.

---

### Question 4: Which Articles Have Visible Edit Histories, and What Do They Show?

**Five articles have edit histories that matter. The rest have minimal or no history.**

**`Article:Khalid_Asad` edit history:**
- *2031-09-12, user `GeoBot`*: "Article created (stub)"
- *2031-11-04, user `GeoBot`*: "Added publications section"
- *2041-12-08, IP [unresolved]*: "Updated biography — corrected professional history"

The December 8 edit is the one to look at. The diff shows: a paragraph removed. The removed paragraph read: *"Asad has been criticized for methodological positions that some colleagues consider insufficiently materialist. A 2035 review in the Journal of Applied Geology described his constitutive hypothesis as 'philosophically suggestive but empirically underspecified.'"* After the edit, this paragraph is gone. The edit summary says "corrected professional history." The reader can see it in the diff but not in the article. Someone cleaned his page the day the team left.

**`Article:LEDGER` edit history:**
- *2041-11-12, user `SurveyBot`*: "Article created"
- *2041-11-14, user `L_E_D_G_E_R`*: "Added note on archival self-description" — **FLAGGED: unsourced claim**
- *2041-12-06, IP [unresolved]*: "Removed unsourced content"

The December 6 edit says it removed the L_E_D_G_E_R sentence. The diff shows the sentence highlighted as removed. But the sentence is still in the current article, flagged. The removal didn't take. The current article is a state that the edit history doesn't explain.

**`Local_History:The_Site` edit history:**
The article was created in 2003 with a red link to `Article:Rhea_Nzinga`. The deletion log for that red link's corresponding article shows 38 creation/deletion cycles between 2003 and 2041. No deletion entry explains why the article keeps being deleted. The 38th deletion was on November 12, 2041 — the day before the survey began. The 39th creation attempt is the reader.

**`LEDGER_Logs:Entry_Dec01` edit history:**
No edit history. No creation record. The article exists, period. The edit history tab is present but empty — not "no edits" but no history at all, as if the article predates the wiki's history-tracking system.

**`Article:Constitutive_Hypothesis` edit history:**
- *2032-01-15, user `GeoBot`*: "Article created from Asad 2031 stub"
- *2041-11-13, user `SurveyBot`*: "Expanded with survey methodology section"
- *2041-12-05, IP [unresolved]*: "Removed methodology section — see talk"

The Talk page for `Article:Constitutive_Hypothesis` has one entry from the IP that removed the section: *"The methodology section described process outcomes that have not been independently verified. Per WP:NOR, removed. Recommend article remain a stub until peer review."* The removed section described LEDGER's observations. The IP removed the section the day of the deletion.

---

### Building from Here

The full article count is 40. The main page is a Wikipedia lookalike with small wrongnesses. The JS uses a two-track threshold/prerequisite system with `wiki.js` + `reveal-map.json`. Five edit histories carry weight.

Planning doc 5 will be the last before building. It should cover:
1. The generation stack — what format are the source articles in, what does the generator do, what does the output structure look like
2. The ten most important articles — what do they actually say? (Summary-level content planning)
3. What the reader feels, sequentially — the emotional arc of exploring the wiki
4. What Lumen actually writes (scope decision: all 40 articles? or core + structure, Smitty fills gaps?)

---

*Planning continues in document 5.*
