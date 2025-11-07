# Project Understanding - The Impactory (UPDATED AFTER THURSDAY CALL)

**Last Updated**: After Thursday call with team
**Status**: Complete pivot in understanding
**What Changed**: This is NOT a YWCA project - it's 10Seven's internal research platform

---

## 🚨 MAJOR CORRECTION: THE REAL PROJECT

### What I Understood Before Thursday:
- Project was for YWCA (196 chapters)
- Replace 61-page annual survey
- Help chapters write grants and manage data
- Trauma graph was add-on for YWCA
- Chris hired to build for YWCA

### What It Actually Is (After Thursday Call):
- **Project is for 10Seven's internal research work**
- YWCA is just one white-label client (secondary priority)
- Core: Collaborative qualitative coding + trauma graph + living insights repository
- Trauma graph is their biggest untapped revenue generator
- Chris hired to build 10Seven's internal research infrastructure

**Key Quote from Chloe**: "Clients be damned. We should be building for us and retrofitting to clients. Our biggest revenue generator that we've never tapped is the trauma graph. If it gets built, we don't have to take on YWCA anymore."

---

## The Three Products (In Priority Order)

### 1. Internal Data Warehouse - "The Patient Chart System" (PRIORITY #1)

**Purpose**: 10Seven's internal collaborative research platform
**Users**: Chloe, Nina, Andrea, Allison (internal team only)
**Never shared with clients**

**The "Patient Chart" Analogy (Chloe's Words)**:
> "I think of it like a patient chart at a hospital. You can see all their labs, but you also see the doctor's notes from each visit. Andrea shouldn't have to have a 2-hour conversation with me to understand Philadelphia from 3 years ago. She should click on Philadelphia and see what I discovered, when, and why."

**What It Needs**:

**Collaborative Qualitative Coding (Biggest Pain Point)**:
- Highlight text in transcripts → tag with codes → auto-tally across all interviews
- Real-time collaboration (like Google Docs, not siloed like Max QDA)
- Split screen: transcript on left, field notes on right
- Field notes visible to whole team (not siloed per person)
- See codes ranked by frequency (saturated themes)
- Click code to see all instances across transcripts
- Multiple highlight colors (blue for themes, yellow for "WOW" quotes)
- Team can see each other working in real-time

**Living Insights Repository (Critical Feature)**:
- Click on geographic location (state, county, neighborhood)
- See all historical notes/insights for that location
- Add new notes, respond to team members' comments
- Attach secondary data (NY Times articles, external research)
- Version history: what changed, when, why
- Split screen: data on left, insights/notes on right
- NOT just spreadsheet - more like old AirTable (notes not buried)

**Automated Map Coloring**:
- Upload base map or select from library
- Label all polygons (counties, neighborhoods) on back end
- Feed spreadsheet: [Location, Severity 1-4, Color code]
- System auto-colors map
- Update when new data comes in
- Track version history of changes

**Quantitative Analysis**:
- Import survey data
- Run correlations, regression analysis
- Comparable to Qualtrics Stats IQ, SPSS, R
- Team members can run analyses
- Real-time visibility of results

### 2. Trauma Graph (PRIORITY #2 - The Revenue Generator)

**Purpose**: Interactive maps clients pay to license (view only, never raw data)
**Users**: External clients who commission trauma graphs
**Business Model**: This is how they make money

**What "Trauma Graph" Actually Means** (Not Just a Map):
- Data collection (surveys + interviews)
- Qualitative coding (collaborative platform)
- Quantitative analysis (correlations, stats)
- Theme identification (saturated themes)
- Geographic mapping (themes → zip codes/neighborhoods)
- Severity assignment (Level 1-4 index)
- Map visualization (color-coded by severity)
- Insights repository (living notes attached to locations)
- Version history (track changes over time)
- Client access (license to view insights, never raw data)

**The "Living Map" Concept**:
- Maps are continuously updated (not one-time deliverables)
- Team adds notes, articles, insights over time
- Multiple clients can commission trauma graphs for same area
- All data feeds into one living system
- Eventually: every neighborhood in US has complete data

**Geographic Levels**:
- National: 3,000 counties
- State/City: Neighborhoods
- Custom geographic areas

**Severity Levels**:
- Level 1-4 color-coded
- Rules-based: "If >40% of respondents exhibit X, Y, Z = Level 4"
- Qualitative judgment on what's "worse"

**Client Access Model**:
- View only (never see raw data, only insights)
- Can click on counties/neighborhoods to see findings
- Licensed access (pay to view)
- Side-by-side with their own data (if white label client)

**Key Quote from Andrea**: "Our vision is that every single neighborhood in the US is complete with all the data we could ever find."

### 3. White Label for Clients (SECONDARY - Build Later)

**Purpose**: Simplified version for clients to store their data + optional trauma graph access
**Users**: YWCA (and future clients)
**Much simpler than internal tool**

**For YWCA Specifically**:
- Data entry (how many programs, how many people served, how many buildings owned)
- Simple queries ("how many local associations have childcare?")
- Replace their endless surveys with continuous data entry
- Generate simple reports
- Optional add-on: License trauma graph access (paid)
- Side-by-side view: their data + 10Seven's trauma graph insights

**Not Sophisticated**:
- No Max QDA-level complexity
- No complex qualitative coding
- Just basic data storage and retrieval
- Simple reports

**Current Dynamic (Andrea's Words)**:
> "I just want to build YWCA so they can leave us alone. The dynamic between YWCA USA and local associations is fraught. USA doesn't give them support. I'd love to hand them something simple. But honestly, they're not in any rush. They're not in a rush to do anything ever."

---

## Their Current Workflow (Step by Step)

### 1. Survey Design & Data Collection
- Update survey questions (currently Google Docs/Word - wish it was in one place)
- Build survey in Qualtrics or cheaper alternative
- Blast via paid firm + partner orgs
- Target: 500+ respondents minimum (ideally 100+ per geographic area)

### 2. Qualitative Interviews
- Recruit through survey
- Pay participants (must do survey + interview)
- Record interviews, get transcripts
- Take field notes (note when someone cries, points to object, etc.)

### 3. Qualitative Coding (BIGGEST PAIN POINT)
**Current Tool**: Max QDA
**Process**:
- Read transcript, highlight sentences
- Tag with "code" (category: "housing insecurity," "zip code," "meaningful community")
- Tool tallies code frequency across ALL interviews
- Top codes = "saturated themes"
- Multiple rounds: first pass individual, then consolidate similar codes

**Why Max QDA Sucks**:
- ❌ NOT real-time collaborative (glitches with multiple users)
- ❌ Field notes are siloed per person
- ❌ Can't see each other's work until done
- ❌ Updates don't sync like Google Docs

**What They Need**:
- ✅ Real-time collaboration (like Google Docs)
- ✅ Highlight → code → auto-tally
- ✅ Split screen: transcript + field notes
- ✅ Team sees each other working live
- ✅ Field notes visible to whole team

### 4. Quantitative Analysis
- Run correlations, regression (Qualtrics, SPSS, R)
- Analyze independently from qualitative
- Then compare: do insights overlap?

### 5. Identify Themes & Geographic Patterns
- Pick top 3-5 codes by tally (saturated themes)
- Cross-reference with geography: where do themes appear?
- Look for concentrations: "40 people mentioned housing, 20% from same zip code"

**Can Be Automated**: System could generate report: "Top theme is X, happening in these neighborhoods"

### 6. Assign Severity Levels
- Judgment call based on qualitative severity
- Level 1-4 severity index
- Rules like: "If >40% exhibit X, Y, Z = Level 4"
- Example: Self-harm when unexpected bills arrive = severe

**Can Be Automated**: Feed severity rules via spreadsheet → system assigns levels

### 7. Map Coloring (MAJOR PAIN POINT)
**Current Process**:
- Find base map (license US counties, pull city map from website)
- Manually click each county/neighborhood and change color
- National: Clicked all 3,000 counties by hand in Adobe Illustrator
- St Paul: Used iPad Procreate app to drag colors into streets

**What They Need**:
- ✅ Feed spreadsheet: [Location, Severity, Color]
- ✅ System auto-colors map
- ✅ Update when new data comes in
- ✅ Track version history

### 8. Write Insights & Build Report
- Synthesize themes into narrative
- Create multi-dimensional maps
- Publish report

**Current Problem**: Insights only exist in Chloe's head or final reports. No living repository.

---

## The Current Pain Points (Prioritized)

### 1. Max QDA Is Not Collaborative (CRITICAL)
- Can't work simultaneously in real-time
- Field notes are siloed per person
- Updates don't sync like Google Docs
- Glitches when multiple people logged in
- Forces Chloe to code all her own interviews (can't share field notes)

### 2. Manual Map Coloring Is Tedious (HIGH)
- Clicked 3,000 counties by hand
- Used iPad to drag colors into neighborhoods
- No automation, completely manual every time
- Have to find/license base maps for every new city

### 3. No Living Repository of Insights (HIGH)
- Insights only in reports or Chloe's head
- Team gets updates "second-hand when it's done"
- Can't see historical decisions from years ago
- No version history
- Constantly texting articles/insights (not captured in system)

### 4. Siloed Workflows (MEDIUM)
- Chloe works in Max QDA alone
- Allison works in Qualtrics/SPSS alone
- Nina and Andrea get results after the fact
- Can't see work in progress

---

## What Can Be Automated vs. Manual

### Can Be Automated ✅
- Tally codes across interviews
- Rank codes by frequency
- Map codes to geography
- Generate theme reports
- Assign severity levels based on rules
- Color maps from spreadsheet
- Track version history

### Must Stay Manual ❌
- Reading transcripts, deciding what to highlight
- Creating codes (let the data tell us)
- Consolidating similar codes
- Judgment calls on severity
- Finding base maps for new cities
- Writing insights and narrative

**Chloe's Quote**: "It is a very manual process, and I think that's important. But the automation is: as soon as I tally something, if that can be automated, that saves me a lot of time."

---

## The Business Strategy Shift

### Current State:
- Take on client consulting projects (YWCA, etc.)
- Good at client work
- Not scalable

### Future State:
- Build internal research infrastructure
- Pump out trauma graphs
- License access to clients
- Turnkey products, not consulting

**Chloe's Quote**: "Our biggest revenue generator that we've never tapped is the trauma graph. If it gets built, we don't have to take on YWCA anymore unless we really want to. It will position me where I should be - pumping out research."

**The Vision**:
- Every neighborhood in US eventually has trauma data
- Clients commission trauma graphs
- All feeds into one living system
- Clients pay to license access
- Move away from one-off consulting

---

## The Licensing Model

### Internal Access (10Seven Team):
- Full back-end access to everything
- See all data, all codes, all insights, all maps
- Can add/edit/collaborate in real-time

### Client Access (YWCA, Future Clients):
- View-only trauma graph insights
- Never see raw data, only insights and visualizations
- Click on neighborhoods to see findings
- Optional add-on to white label warehouse

### Education Access (ED Hub Users):
- Only see courses enrolled in
- Different tier from research clients

**Andrea's Quote**: "It's one big central platform for everything we make. What we make can be accessed by clients if they want to pay us. It just sells itself."

---

## Priority Decision (What to Build First)

**Team Consensus**:
1. Internal data warehouse FIRST
2. Trauma graph SECOND (requires warehouse)
3. White label for YWCA THIRD (retrofit later)

**Chloe's Quote**: "We need to build a trauma graph. To build it, we technically need to build our internal data warehouse. But I think we should retrofit everything to our clients. Build our stuff, everything else is retrofitted."

**Why This Order**:
- Trauma graph is revenue generator
- YWCA isn't in a rush ("not in a rush to do anything ever")
- Should stop prioritizing clients
- Build what 10Seven needs first

---

## Technical Feasibility

**Can This Be Built?** ✅ Yes, absolutely

**Complexity**: 7/10 (Medium-High, but nothing impossible)
- Real-time collaboration: Solved problem
- Geographic map coloring: Standard libraries
- Living insights repository: Database + version control
- User access tiers: Standard auth/permissions

**Business Feasibility**: 8/10 (High)
- Clear revenue model (license trauma graph)
- Real pain points (Max QDA, manual coloring)
- Client base exists
- Team motivated and aligned

**Risk Level**: 4/10 (Medium-Low)
- Internal tool first (controlled users)
- Client white labels later (retrofitted)
- Revenue model proven (people commission graphs already)
- Team knows what they want

---

## Next Steps

### From Team to Chris:
- ✅ Chloe: Step-by-step trauma graph process + St Paul report
- ✅ Andrea: Architecture sketches + brand access flow
- ✅ Team: YWCA grant examples (if available)

### From Chris to Team:
- ✅ Define standardized language for three products
- ✅ Architecture suggestions after receiving materials
- ✅ Monday follow-up meeting (11am PST)

---

## Files Updated

- **thursday_call_transcript.md** - Full transcript
- **CALL_ANALYSIS_thursday.md** - Detailed analysis (29 pages)
- **THURSDAY_SUMMARY.md** - Plain English summary
- **PROJECT_UNDERSTANDING_UPDATED.md** - This file

---

## Bottom Line

**What You're Building**: Collaborative research platform for 10Seven's internal work (not YWCA).

**Three Products (Priority Order)**:
1. Internal data warehouse ("patient chart system") - BUILD FIRST
2. Trauma graph (interactive maps for licensing) - BUILD SECOND
3. White label for clients (YWCA simplified version) - BUILD THIRD

**Business Model**: Stop consulting, license trauma graph access, Chloe pumps out research, turnkey products.

**Feasibility**: Yes (7/10 complexity), solid business model (8/10), low risk (4/10).

**Your Role**: Build 10Seven's internal research infrastructure. YWCA is a side project to retrofit later.

**Key Insight**: Everything I understood before Thursday was wrong. This is NOT a YWCA project.
