# Session Context - The Impactory Project (UPDATED AFTER MONDAY FOLLOW-UP)

**Last Updated**: After Monday follow-up call
**Status**: Major scope expansion - survey builder + enhanced quant analysis now required
**Next Step**: Receive materials from team + tech stack decision finalized

---

## 🚨 CRITICAL UPDATE: Everything Changed After Thursday Call

### What I Understood Before Thursday:
Project was for YWCA (196 chapters), replacing 61-page survey, helping write grants. Chris hired to build for YWCA.

### What It Actually Is (After Thursday):
Project is for 10Seven's internal research work. YWCA is just one white-label client (secondary). Chris hired to build 10Seven's research infrastructure.

**Chloe literally said**: "Clients be damned. We should be building for us and retrofitting to clients. Our biggest revenue generator is the trauma graph."

---

## 🆕 MONDAY FOLLOW-UP: Major Scope Additions

### New Requirements Identified:

**1. Survey Builder Platform (NEW - Replacing Qualtrics)**
- Build entire survey creation tool
- Question types: multiple choice, text input, file uploads
- **Skip logic** (conditional questions based on previous answers)
- Data export to spreadsheet
- Doesn't need to be fancy, just functional
- **Goal**: ONE platform for surveys + quant + qual (not multiple tools)

**2. Enhanced Quantitative Analysis (More Critical Than Initially Thought)**
- Statistical analysis comparable to Qualtrics Stats IQ / SPSS
- Correlations, p-values, statistical significance testing
- Cross-tabulation (disaggregate by race, gender, geography)
- Correlation matrices (extensive tables showing question-to-question correlations)
- **Primarily TABLES** (90% of visualizations are tables, occasional pie/line charts)
- Quick preliminary analysis + advanced analysis capabilities

**3. Target Audiences Clarified**
- **B2B Institutional**: Think tanks (Brookings, Aspen), Government bodies (mayors, local governments), Nonprofits
- **B2C Individual**: Researchers, Financial counselors/advisors
- **PARENTS = HUGE NEW MARKET** ⭐ (Most common inquiry, started in K-12 space, massive untapped potential)

**4. Map Technology & Features Finalized**
- **Mapbox confirmed** (Chloe loved the prototype)
- Reference examples: Eviction Lab (Princeton), Mapping Police Violence, Urban Institute Wealth Dashboard
- **Event-based filters (NEW concept)**: Time periods (pre/post admin changes), Policy events (SNAP cuts, federal layoffs), Historical periods (1950s displacement, interstate highways)
- **Two vectors of premium features**:
  - Vector 1: Static vs Dynamic maps (dynamic = zoom, interactive = PREMIUM)
  - Vector 2: Basic vs Multidimensional overlays (severity only vs multiple dimensions overlaid = PREMIUM)
- **Granularity = premium feature** (neighborhood-level detail more valuable than state-level)

**5. Marketing Strategy Decided**
- **DON'T market white label publicly** (except Ed Hub education side)
- **DO market trauma graph licensing** as primary product
- White label only offered when client specifically requests it
- Reasoning: YWCA needs are "so basic" - people want trauma graphs, not white label

**6. Trial Licensing Model (NEW)**
- Conference attendees get **14-day access code** after Chloe's keynote speeches
- Discount if they license after trial expires
- Lead generation strategy for speaking engagements

**7. Pricing Strategy**
- Premium users: Usage-based pricing (so many maps, so much data)
- Basic users: Potentially flat-rate
- Advantage of usage: Easy to adjust rates across the board (e.g., 20 cents per minute)

**8. Mobile Apps Confirmed**
- All products will likely have mobile versions
- This impacts tech stack decision significantly
- Firebase stronger for mobile (native SDKs, offline sync)
- OR hybrid approach (Supabase internal, Firebase mobile white label)

---

## The Real Project: Three Products

### 1. Internal Data Warehouse - "The Patient Chart System" (PRIORITY #1)
**For**: 10Seven internal team only (never shared with clients)
**Purpose**: Collaborative research platform where insights accumulate over time

**The Analogy**: Hospital patient chart - see all labs, but also every doctor's notes from every visit. Click on Philadelphia and see what Chloe discovered 3 years ago, when, and why.

**Core Features**:
- **Survey Builder** (NEW): Replace Qualtrics - question types, skip logic, data collection
- **Quantitative Analysis Suite**: Stats IQ-level analysis (correlations, p-values, cross-tabs, primarily tables)
- Real-time collaborative qualitative coding (like Google Docs, not siloed like Max QDA)
- Highlight transcript → tag with code → auto-tally across interviews
- Split screen: transcript + field notes
- Living insights attached to geographic locations
- Version history: what changed, when, why
- Team sees each other working in real-time
- Automated map coloring from severity spreadsheet

### 2. Trauma Graph (PRIORITY #2 - Revenue Generator)
**For**: Clients who pay to license access (view only)
**Purpose**: Interactive maps + entire research ecosystem
**Technology**: Mapbox (confirmed)

**NOT just a map**. It's:
- Data collection (via survey builder) → qualitative coding → quantitative analysis
- Theme identification → geographic mapping → severity levels
- Map visualization (with event-based filters) → insights repository → version history
- Client licensing (view insights, never raw data)

**Map Features & Filters**:
- **Location-based**: Zip code, county, state, neighborhood (granularity = premium)
- **Event-based (NEW)**: Time periods, policy events, historical periods
- **Map types**: Severity maps, multiple oppressions overlays, historical trauma graphs
- **Premium tiers**: Static vs Dynamic (zoom/interactive), Basic vs Multidimensional overlays

**Reference Examples**: Eviction Lab (Princeton), Mapping Police Violence, Urban Institute Wealth Dashboard

**The Vision**: Every neighborhood in US eventually has complete trauma data. Clients commission graphs, all feeds into one living system.

**Trial Licensing**: 14-day access codes for conference attendees after keynote speeches (lead generation)

### 3. White Label for Clients (SECONDARY - Build Later)
**For**: YWCA and future clients
**Purpose**: Simplified data storage + optional trauma graph access
**Marketing Strategy**: NOT marketed publicly (clients request it), EXCEPT Ed Hub (education side)

**For YWCA**: Data entry, simple queries, replace endless surveys. Optional paid add-on for trauma graph.

**Why not marketed**: Needs are "so basic" - clients want trauma graphs, not white label data storage.

**Andrea's quote**: "I just want to build YWCA so they can leave us alone. They're not in a rush to do anything ever."

---

## Current Pain Points (Why They Need This)

### #0: Multiple Platforms Don't Talk to Each Other (Critical - NEW)
- Currently using: Qualtrics (surveys), Max QDA (qual coding), SPSS/R (advanced stats), Illustrator (maps)
- Data lives in siloed platforms
- Manual export/import between tools
- Wish it was "all in one place"
- Goal: Build ONE platform for entire workflow (surveys → qual → quant → maps)

**What they need**: Integrated platform that handles entire research process.

### #1: Max QDA Is NOT Collaborative (Critical)
- Says it's collaborative, but glitches with multiple users
- Field notes are siloed per person
- Can't see each other's work until done
- Forces Chloe to code all her own interviews

**What they need**: Real-time collaboration like Google Docs for research.

### #2: Manual Map Coloring (High)
- Clicked all 3,000 US counties by hand in Adobe Illustrator
- Used iPad to drag colors into St Paul neighborhoods
- Completely manual, extremely tedious

**What they need**: Feed spreadsheet → system auto-colors map.

### #3: No Living Repository of Insights (High)
- Insights only in Chloe's head or final reports
- Team gets updates "second-hand after it's done"
- Can't see historical decisions from 3 years ago
- No version history
- Texting articles to each other (not captured)

**What they need**: Click on neighborhood → see all historical notes/insights + version history.

---

## Their Research Workflow (Step by Step)

1. **Survey & Data Collection**: 500+ respondents, 100+ per geographic area
2. **Qualitative Interviews**: Pay participants, record, take field notes
3. **Qualitative Coding**: Highlight → tag with codes → identify saturated themes (top 3-5 by tally)
4. **Quantitative Analysis**: Correlations, regression (independently, then compare with qualitative)
5. **Geographic Mapping**: Cross-reference themes with zip codes/neighborhoods
6. **Severity Assignment**: Level 1-4 based on rules and qualitative judgment
7. **Map Coloring**: Color counties/neighborhoods by severity (currently manual)
8. **Write Report**: Synthesize insights into narrative

**Can be automated**: Code tallying, theme ranking, geographic matching, severity assignment, map coloring, version history

**Must stay manual**: Reading transcripts, creating codes, consolidating similar codes, severity judgment, finding base maps, writing insights

---

## The "Patient Chart" Analogy (Critical Concept)

**Chloe's words**: "Like a patient chart at a hospital. You see labs, but also doctor's notes from each visit. Person coming on shift next can read: what was the last doctor thinking? That's what this needs to be."

**What this means**:
- Living knowledge system (not just database)
- Insights accumulate over time
- Click on location → see everything ever discovered there
- Version history: what changed, when, why
- Team adds notes as they discover new things
- No more 2-hour lectures to get people up to speed

**Andrea's addition**: "Click on state, zoom to county, zoom to neighborhood. At each level, read what Chloe wrote, add my own notes, respond, attach NY Times articles."

---

## The Business Strategy Shift

**Current**: Take on client consulting (YWCA, etc.). Good at it, not scalable.

**Future**: Build internal research platform. Pump out trauma graphs. License access. Turnkey products.

**The Vision**:
- Every neighborhood in US has trauma data eventually
- Clients commission trauma graphs
- All feeds into one living system
- Clients pay to license access (view insights, never raw data)
- Stop one-off consulting, focus on scalable products

**Chloe's quote**: "If the trauma graph gets built, we don't have to take on YWCA anymore unless we really want to. It will position me where I should be - pumping out research."

---

## Priority Decision: What to Build First

**Team Consensus**:
1. Internal data warehouse FIRST
2. Trauma graph SECOND (requires warehouse)
3. White label for YWCA THIRD (retrofit later)

**Why**: Trauma graph is revenue generator. YWCA isn't in a rush. Stop prioritizing clients. Build what 10Seven needs first.

---

## Technical Feasibility

**Can This Be Built?** ✅ Yes

**Complexity**: 7.5/10 → 8/10 (Increased due to survey builder + enhanced quant analysis + mobile apps)
**Business Feasibility**: 8/10 (High - clear revenue model, real pain points, multiple target audiences)
**Risk**: 4.5/10 (Medium - slightly higher due to expanded scope, but still internal-first approach)

**Tech Stack Considerations**:
- **Mobile apps confirmed** - impacts database choice
- **Survey builder** adds complexity (skip logic, conditional questions)
- **Statistical analysis** needs robust compute (correlations, p-values, regression)
- **Real-time collaboration** remains critical
- **Geographic queries** with PostGIS preferred
- **Firebase vs Supabase**: Hybrid approach possible (Supabase internal, Firebase mobile white label)

---

## Next Steps

### ✅ Completed:
- Monday follow-up call (conducted)
- Defined standardized language for three products
- Clarified survey builder + quant analysis requirements
- Confirmed Mapbox technology
- Aligned on target audiences and premium features

### Waiting For (From Team):
- ✅ Nina: Qualtrics login credentials (for Chris to explore Stats IQ)
- Pending: St Paul report examples (severity levels, multiple maps)
- Pending: Andrea's architecture sketches
- Pending: YWCA grant examples (if available)

### To Do (Chris):
- Explore Qualtrics Stats IQ (once login received)
- Finalize tech stack decision (Supabase vs Firebase vs Hybrid)
- Create alignment document for client review
- Prepare proposal with cost/timeline estimates
- Travel: Nov 28 - Dec 9 (email access only)

---

## What Changed From My Previous Understanding

### Before Thursday:
- ❌ Project was for YWCA
- ❌ Helping 196 chapters replace survey
- ❌ Grant writing was core
- ❌ Trauma graph was add-on for YWCA
- ❌ You were hired to build for YWCA

### After Thursday:
- ✅ Project is for 10Seven (internal research)
- ✅ YWCA is white-label client (secondary)
- ✅ Qualitative coding collaboration is core
- ✅ Trauma graph + internal warehouse IS the product
- ✅ You were hired to build 10Seven's platform

### After Monday Follow-Up:
- ✅ Survey builder now required (replace Qualtrics entirely)
- ✅ Quantitative analysis much more critical (Stats IQ, correlations, cross-tabs)
- ✅ Parents identified as huge B2C market
- ✅ Event-based filters needed (policy events, historical periods)
- ✅ Two-tier premium model (static/dynamic + basic/multidimensional)
- ✅ White label won't be publicly marketed
- ✅ Mobile apps confirmed (impacts tech stack)
- ✅ Mapbox confirmed as mapping technology

---

## Files Created/Updated

**Thursday Call**:
- thursday_call_transcript.md - Full transcript
- CALL_ANALYSIS_thursday.md - Detailed 29-page analysis
- THURSDAY_SUMMARY.md - Plain English summary

**Monday Follow-Up**:
- monday_followup_transcript.md - Full transcript (pending creation)
- monday_followup_analysis.md - Analysis of new requirements (pending creation)

**Updated Documentation**:
- PROJECT_UNDERSTANDING_UPDATED.md - Updated with Monday findings
- SESSION_CONTEXT_UPDATED.md - This file (updated with Monday findings)
- STANDARDIZED_LANGUAGE_ARCHITECTURE.md - Architecture framework (may need updates)

---

## Key Quotes from Thursday Call

**Chloe on Priority**:
> "Clients be damned. We've always prioritized them. I think we should start deprioritizing them compared to what we need. Our biggest revenue generator that we've never tapped is the trauma graph."

**Chloe on The Decision**:
> "We need to build a trauma graph. To build it, we technically need to build our internal data warehouse. But I think we should retrofit everything to our clients. Build our stuff, everything else is retrofitted."

**Andrea on YWCA**:
> "I just want to build YWCA so they can leave us alone. The dynamic is fraught. I'd love to hand them something simple. But honestly, they're not in any rush. They're not in a rush to do anything ever."

**Andrea on Vision**:
> "It's one big central platform for everything we make. What we make can be accessed by clients if they want to pay us to access it. It just sells itself."

**Chloe on Patient Chart**:
> "I think of it like a patient chart at a hospital. You can see all their labs, but also the doctor's notes. The person coming on shift next can see: what was that person thinking? That's what it needs to be."

## Key Quotes from Monday Follow-Up Call

**Chloe on Survey Builder**:
> "I would honestly love to get away from another platform. If you feel like we can make a survey builder... it is literally a survey where people are inputting their answers. That's it."

**Chloe on Integrated Platform**:
> "If we could get something that gives me some quantitative solution, like this. Like, that's really all I need. If all of that was in one place for us, that would be a huge game changer, huge."

**Chloe on Data Visualization**:
> "Nine times out of 10 we're looking at tables... We're actually reporting the table."

**Chloe on Mapbox**:
> "I did some research like a year ago on Mapbox, and I kind of really liked it. They have heat maps and things that we can kind of make work for us."

**Chloe on White Label Marketing**:
> "Do I think we're going to get a lot of YWCA clients? No... people are going to stop at the trauma graph, like, that's really what they want."

**Chris on Granularity**:
> "The further down you can go in detail, sounds like that's of high value?"
**Chloe**: "Big time."

---

## Bottom Line (Updated After Monday)

**What you're building**: Integrated research platform for 10Seven - survey builder + qual coding + quant analysis + trauma graph licensing. NOT a YWCA project.

**Three products (priority order)**:
1. **Internal data warehouse** - Survey builder + qual coding + quant analysis + maps (BUILD FIRST)
2. **Trauma graph** - Interactive Mapbox maps with event filters + premium tiers (BUILD SECOND)
3. **White label** - Simple storage for YWCA (BUILD THIRD, don't market publicly)

**Build order**: Internal first, clients later. "Build our stuff, retrofit to clients."

**Business model**:
- License trauma graph access (B2B institutional + B2C individual + parents)
- Trial licensing at conferences (14-day access codes)
- Usage-based pricing for premium users
- Stop consulting, focus on scalable products

**Target audiences**: Think tanks, government bodies, nonprofits, researchers, financial advisors, **parents (huge untapped market)**

**Feasibility**: Yes (8/10 complexity due to expanded scope), solid business (8/10), medium risk (4.5/10).

**Tech stack considerations**:
- Mobile apps required
- Supabase recommended for internal (geo queries, version history, quant analysis, CLI workflow)
- Firebase strong for mobile OR hybrid approach
- Mapbox confirmed for maps

**Your role**: Build 10Seven's end-to-end research infrastructure. Replace Qualtrics, Max QDA, SPSS, and Illustrator with ONE integrated platform.

**The Big Reveals**:
1. Thursday: This is 10Seven's platform, not YWCA's
2. Monday: Scope much larger - full survey builder + enhanced quant analysis + mobile apps required
