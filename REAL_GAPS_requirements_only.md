# Real Requirements Gaps - What's Actually Missing from the Call

## Assumption: You (Chris) have handled all project management concerns
- MVP scope ✓
- Timeline ✓
- Budget ✓
- Technical architecture ✓
- Previous proposal ✓
- Trauma graph built ✓
- Your capacity ✓

## So what's ACTUALLY missing from a requirements perspective?

---

## GAP 1: Data Model - Client/Beneficiary Data

**What the call says:**
- Chapters serve clients (women, survivors, program participants)
- Survey asks "How many people did you serve?"
- Chloe mentions "case profiles" for domestic violence survivors
- They provide "diagnostic tools" to clients

**What's unclear:**
- Do you store individual client records or just aggregate counts?
- If individual records: What PII? (names, addresses, case notes?)
- If aggregate only: How granular? (by program? by demographic? by month?)

**From the survey:**
Survey asks for aggregate numbers:
- "How many people did you serve last fiscal year?"
- Demographics served (race, gender, income levels)
- No mention of individual client tracking

**Likely answer:**
Probably aggregate only to avoid HIPAA complexity. But confirm.

**Why it matters:**
- Individual client records = major HIPAA, security, and UX implications
- Aggregate only = much simpler, just numbers and percentages

**Question for Thursday:**
"When a chapter says 'we served 168 women,' is that just a number they type in, or are there 168 individual client records in the system?"

---

## GAP 2: Data Update Workflow - When and How Data Changes

**What the call says:**
- Current state: Survey once a year, data goes stale
- Future state: "Update monthly" or "as things happen"
- Goal: Replace survey with continuous data entry

**What's unclear:**
- When a program ends, do they mark it closed? Archive it? Delete it?
- When funding changes, do they edit the program or create new entry?
- When serving clients, do they update "people served" daily? Weekly? Monthly?
- How do they track things over time? (Q1 we served 50, Q2 we served 75)

**Why it matters:**
This determines if you need:
- Versioning/history (track changes over time)
- Time-series data (served 50 in Jan, 75 in Feb)
- Audit trails (who changed what when)
- Or just "current state" snapshots

**Question for Thursday:**
"Walk me through a year in the life of a program. January: program launches with projected budget $50K, serve 0 people. June: budget revised to $75K, served 100 people. December: program ends, served 250 total. How does this show up in the platform?"

---

## GAP 3: Report Generation - What Actually Goes in Reports

**What the call says:**
- Chapters need "grant-ready reports"
- Example: "70% of our programs deal with SNAP-eligible women"
- Reports should be "pretty and comprehensive"
- Help them "build a narrative to raise money"

**What's unclear:**
- What sections does a grant report have? (Executive summary? Demographics? Outcomes? Evidence? Budget?)
- How much is auto-generated vs. custom text they add?
- Do they need different reports for different funder types? (foundation vs. government vs. individual)
- Can they include custom narrative/stories or just data?
- Do reports include trauma graph data/maps?

**Why it matters:**
Report generation could be:
- Simple: Fill-in-the-blank template with data
- Complex: Rich text editor where they compose custom narrative around data
- Medium: Pre-written sections with data merged in, plus ability to add notes

**Question for Thursday:**
"Show me an example grant report you've written or want to write. Let's mark which parts should come from the platform vs. which parts they write themselves."

---

## GAP 4: Cross-Chapter Discovery - What's the Actual UX

**What the call says:**
- Chapters want to see "what other organizations are up to"
- Example: "Oh, in Buffalo they're doing X, Y, Z"
- "I can actually just take this program for how I see it"
- Facilitates "collaboration and learning"

**What's unclear:**
- Is this a search interface? ("Find chapters doing childcare")
- Is this a browse interface? ("Show me all programs in New York")
- Is this a feed/timeline? ("Recent programs launched")
- Can they filter by program type, impact area, violence type, geography?
- Do they contact each other through platform or just get inspired?

**Possible models:**
1. **Program directory**: Browse/search all programs across network
2. **Chapter profiles**: Click on a chapter, see their programs
3. **Network activity feed**: "Chapter X launched program Y"
4. **Recommendations**: "Chapters similar to you are doing..."

**Why it matters:**
Different UX patterns require different data structures and complexity levels.

**Question for Thursday:**
"Buffalo chapter wants to learn about childcare programs in New York. Walk me through: What do they click? What screen do they see? What info is shown?"

---

## GAP 5: National HQ Dashboard - What Do They Actually See

**What the call says:**
- "USA gets its own version where it kind of collates all of the data"
- They want network-wide statistics
- They're being "surveyed to death" so this should replace surveys

**What's unclear:**
- Do they see all 196 chapters on one screen? (long table? map? cards?)
- Can they drill down into individual chapters?
- What metrics do they care about most? (total served? total revenue? program count?)
- Do they compare chapters to each other? (rank by performance?)
- Do they get alerts? ("Chapter X hasn't updated in 3 months")

**Why it matters:**
HQ dashboard could be:
- Simple: Big numbers across top (total served, total programs, total chapters), table below
- Complex: Interactive map, filtering, comparing, trend analysis

**Question for Thursday:**
"National HQ logs in Monday morning. What do they want to see first? What questions are they trying to answer?"

---

## GAP 6: Trauma Graph Integration - How Do They Actually Use It

**What the call says:**
- "Side by side view" of their data and trauma graph
- "Look at shame indicators by neighborhood about where they are"
- Helps them "tell a story about the impact they're having"
- Geographic matching by zip code/neighborhood

**What's unclear:**
- Where in the platform do they access trauma graph? (main nav? inside reports? when viewing programs?)
- Do they manually select trauma graph layer or auto-matched to their service area?
- Can they export trauma graph visualizations for their reports?
- Do trauma graph metrics show up in their data dashboard? ("67% of your clients experience financial shame - which matches the 65% trauma graph shows for your zip code")

**Why it matters:**
This determines integration points between warehouse and trauma graph.

**Question for Thursday:**
"A chapter is writing a grant about their domestic violence program. Walk me through: How do they bring up relevant trauma graph data? What do they see? How do they use it?"

---

## GAP 7: File Uploads - What Gets Uploaded and Why

**What the survey shows:**
- Chapters can upload 990s, budgets, strategic plans
- Evidence documentation (reports, materials)

**What's unclear:**
- Are these just for reference or does anything happen with them?
- Who can see uploaded files? (just the chapter? national HQ? other chapters?)
- Do files expire or get archived?
- Can they upload client testimonials, photos, case studies?

**Why it matters:**
Simple file storage is easy. If you need to extract data from files or share files across chapters, more complex.

**Likely answer:**
Probably just reference storage, like Dropbox for each chapter. Nothing fancy needed.

**Question for Thursday:**
"When a chapter uploads their 990, who needs to see it and what do they do with it?"

---

## GAP 8: Program Lifecycle - How Programs Work

**What the survey shows:**
- Programs have: name, objectives, languages, impact areas, violence types, activities, resources, likelihood of impact, evidence

**What's unclear:**
- Are programs always active or do they have statuses? (planned, active, completed, archived)
- Do programs have start/end dates?
- Do programs have budgets attached?
- Do programs have staff assigned?
- Can programs be templates that chapters copy from each other?

**Why it matters:**
Determines program data model complexity.

**Question for Thursday:**
"Tell me about a program from birth to death. How does it start? What changes during its life? How does it end?"

---

## GAP 9: Diagnostic Tools Distribution - How Does This Work

**What the call says:**
- Chapters can "pull a diagnostic tool from the platform"
- "We use this diagnostic survey tool on all of our people that we have cases for"
- "You have to have a license in order to access those tools"

**What's unclear:**
- Do these exist already or need to be built?
- Are these PDFs they download? Online forms they send links to? Paper forms they print?
- How do results come back? (manual entry? automatic if online?)
- What diagnostic tools exist? (financial trauma assessment? domestic violence severity? housing needs?)

**Why it matters:**
If you're building an assessment library with distribution and results tracking, that's a whole feature.

**Question for Thursday:**
"Show me one of these diagnostic tools. How does a chapter use it with their clients? How do results get back into the platform?"

---

## GAP 10: Permissions and Data Privacy - Who Sees What

**From call:**
- HIPAA compliance standard (even though not required)
- Chapters own their data
- Never share 10Seven's raw research data
- Cross-chapter learning but also privacy

**What's unclear:**
- Can chapters hide programs from the network? (opt out of sharing)
- Can national HQ see everything or do chapters have privacy controls?
- Is there a public-facing view? (for funders or general public)
- Can chapters export all their data?
- What happens to data if a chapter closes?

**Why it matters:**
Privacy controls add significant complexity.

**Likely answer:**
Probably simple:
- Chapters see own data fully
- Chapters see others' data in aggregate/limited
- National HQ sees everything
- No public view

**Question for Thursday:**
"If a chapter doesn't want to share a particular program with the network, can they mark it private?"

---

## ACTUAL REQUIREMENTS GAPS - SUMMARY

### Critical (Need for data model):
1. **Client data**: Individual records or aggregate numbers?
2. **Program lifecycle**: Statuses, dates, budgets, staff?
3. **Time-series data**: Track changes over time or just current state?

### Important (Need for features):
4. **Report structure**: What sections, what's auto vs. manual?
5. **Cross-chapter UX**: Search? Browse? Feed? What do they see?
6. **HQ dashboard**: What metrics, what views?

### Nice to know (Can probably infer):
7. **Trauma graph integration**: Where accessed, how used?
8. **File uploads**: What files, who sees them?
9. **Diagnostic tools**: Exist or build? How distributed?
10. **Privacy controls**: Who can hide what from whom?

---

## WHAT YOU ACTUALLY UNDERSTAND WELL

From the call + survey + framework doc, you have a solid understanding of:

✅ **The entities**: Organizations, Programs, Impact Evaluations, Organizational Efforts
✅ **The fields**: Survey gives you 95% of fields needed
✅ **The framework**: Violence types, impact types, evidence types, impact pillars
✅ **The pain**: Survey fatigue, data going stale, can't write grants
✅ **The goal**: Continuous data tracking, grant reports, cross-chapter learning
✅ **The users**: 196 chapters, national HQ, varying sophistication
✅ **The tech**: You've built trauma graph, you know the architecture

---

## WHAT'S GENUINELY UNCLEAR

### Data Model Questions:
- Aggregate vs. individual client data?
- Versioning/history or current state only?
- How granular is time-series? (monthly updates? quarterly?)

### UX Questions:
- What do the main screens actually look like?
- What does cross-chapter discovery UX look like?
- What sections are in grant reports?

### Business Logic Questions:
- When/how does data get updated?
- What's the program lifecycle?
- How do diagnostic tools work?

---

## RECOMMENDATION FOR THURSDAY

Focus on these 3 questions:

### 1. Data Model Clarity:
**"When you say 'we served 168 women,' talk me through what data that represents. Is it just a number, or are there 168 records? How do you track this over time?"**

### 2. User Flows:
**"Let's walk through the 3 most common tasks: Add a program, update data, generate a report. Show me what that looks like."**

### 3. Cross-Chapter Learning:
**"Show me how Buffalo discovers and learns from Rochester's programs. What screens, what information?"**

Everything else you can probably figure out or it's not critical for v1.

---

## BOTTOM LINE

You're actually in **very good shape** on understanding this project.

The survey gives you the data model.
The framework doc gives you the taxonomies.
The call gives you the context and pain points.

What you're missing is:
- **Specifics on data granularity** (aggregate vs. detail)
- **Specifics on UX flows** (what screens look like)
- **Specifics on time-based data** (how to track changes)

These are the kind of things you can figure out in a 30-minute walkthrough on Thursday.

**You don't have 20 gaps. You have maybe 3-5 real questions that need answers.**
