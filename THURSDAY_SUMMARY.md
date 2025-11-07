# Thursday Call - Key Takeaways (Plain English)

## The Big Reveal: This Is NOT What I Thought

**I thought you were building**: A platform for YWCA to replace their 61-page survey and help chapters write grants.

**You're actually building**: 10Seven's internal research platform. YWCA is just one client who'll get a simplified white-label version later.

**Chloe literally said**: "Clients be damned. We should be building for us and retrofitting to clients. Our biggest revenue generator that we've never tapped is the trauma graph."

---

## What You're Actually Building (Three Products)

### 1. Internal Data Warehouse - "The Patient Chart System" (PRIORITY #1)
**For**: 10Seven's internal research team only
**Purpose**: Collaborative research platform where insights accumulate over time

**Think of it like**: A hospital patient chart. You can see all their labs, but also every doctor's notes from every visit. When Andrea wants to know about Philadelphia trauma graph from 3 years ago, she shouldn't need a 2-hour conversation with Chloe. She should click on Philadelphia and read what Chloe discovered, when, and why.

**Core features**:
- Real-time collaborative qualitative coding (like Google Docs, but for research)
- Highlight transcript text → tag with code → auto-tally across all interviews
- Split screen: transcript on left, field notes on right
- Living insights attached to geographic locations
- Version history: what changed, why, when
- Team can see each other working in real-time (not siloed like Max QDA)

### 2. Trauma Graph (PRIORITY #2 - The Revenue Generator)
**For**: Clients who pay to license access (view only)
**Purpose**: Interactive maps showing financial trauma, etc. by geography

**It's NOT just a map**. It's the entire ecosystem:
- Data collection (surveys + interviews)
- Qualitative coding (themes from interviews)
- Quantitative analysis (correlations, stats)
- Geographic mapping (which neighborhoods have which trauma)
- Severity levels (1-4 color-coded)
- Living insights repository (notes attached to every neighborhood)
- Client access (license to view insights, never raw data)

**The vision**: Every neighborhood in the US eventually has complete trauma data. They build it piece by piece as clients commission different trauma graphs. All feeds into one living system.

**Why it matters**: This is how they want to make money. Stop doing client consulting, license trauma graph access instead. Chloe pumps out research, clients pay to view insights.

### 3. White Label for Clients (SECONDARY - Do This Later)
**For**: YWCA and future clients
**Purpose**: Simplified version where clients store their own data + optionally license trauma graph access

**For YWCA**: Data entry (how many programs, how many people served), simple queries ("how many associations have childcare?"), replace endless surveys.

**Andrea literally said**: "I just want to build YWCA so they can leave us alone. The dynamic between YWCA USA and local associations is fraught. I'd love to hand them something simple. But honestly, they're not in any rush. They're not in a rush to do anything ever."

---

## Their Current Painful Workflow (Why They Need This)

### Problem #1: Max QDA Is NOT Collaborative (Their #1 Pain Point)
**What they do now**:
- Chloe reads interview transcripts
- Highlights sentences, tags with "codes" (categories like "housing insecurity" or "zip code")
- Max QDA tallies how many times each code appears across all interviews
- Top codes = "saturated themes" (what to write about in report)

**Why Max QDA sucks**:
- Says it's collaborative, but it's NOT (doesn't work like Google Docs)
- If Nina and Chloe work at the same time, it glitches
- Field notes are siloed - Chloe's notes aren't visible to Nina
- No one can see work in progress - team gets results "second-hand when it's done"
- Forces Chloe to code all her own interviews (can't share field notes with Nina)

**What they need**: Real-time collaboration like Google Docs, but for research. Highlight → code → auto-tally. Split screen with field notes. Team sees each other working live.

### Problem #2: Manual Map Coloring Is Tedious
**What they do now**:
- Find a base map (license US counties, or pull neighborhood map from city website)
- Click every single county/neighborhood and change the color by hand
- National map: Chloe clicked all 3,000 counties in Adobe Illustrator
- St Paul neighborhood map: Used iPad app to drag colors into streets

**What they need**: Feed a spreadsheet with [Location, Severity Level 1-4, Color code] → system auto-colors the map. Update map when new data comes in.

### Problem #3: No Living Repository of Insights
**What happens now**:
- Chloe does all the analysis
- Insights live in her head or in final reports
- Team gets updates "after the fact"
- If Andrea wants to know about Philadelphia from 3 years ago, she has to ask Chloe or re-read the report
- They constantly text each other interesting articles - nothing is captured in a system

**What they need**: Click on a neighborhood → see all historical notes/insights. Version history: what changed, when, why. Team can add notes, respond to each other, attach NY Times articles or secondary data. Living knowledge base.

---

## The "Patient Chart" Analogy (Critical Concept)

**Chloe's words**: "I think of it like a patient chart at a hospital. You can see all their labs, but you also see the doctor's notes from each visit. The person coming on shift next can read: what was the last doctor thinking? Oh, they gave a Tylenol. That's what this needs to be."

**What this means**:
- Not just a database
- Not just a mapping tool
- It's a **living knowledge system** where insights accumulate over time
- Andrea clicks on "Philadelphia" and sees everything Chloe discovered 3 years ago
- Version history shows: what changed, when, why
- Team adds notes as they discover new things
- No more 2-hour lectures to get people up to speed

**Andrea's addition**: "I should be able to click on a state, zoom to county, zoom to neighborhood. At each level, read what Chloe wrote, add my own notes, respond to her comments, attach data points I find (like NY Times articles)."

---

## What Can Be Automated vs. Must Stay Manual

### Can Be Automated ✅
- Tally codes across interviews
- Rank codes by frequency (saturated themes)
- Map themes to geography
- Generate report: "Top theme is X, happening in these neighborhoods"
- Assign severity levels based on rules (if >40% = Level 4)
- Color maps from severity spreadsheet
- Track version history

### Must Stay Manual ❌
- Reading transcripts and deciding what to highlight
- Creating codes (let the data tell us)
- Consolidating similar codes
- Judgment calls on severity (what's "worse" qualitatively)
- Finding base maps for new cities
- Writing insights and narrative

**Chloe's quote**: "It is a very manual process, and I think that's important. But the automation is: as soon as I tally something under a code, if that can be automated, that saves me a lot of time."

---

## The Business Strategy Shift

**Current state**: They take on client consulting projects like YWCA. Good at it, but it's not scalable.

**Future state**: Build internal research infrastructure. Pump out trauma graphs. License access to clients. Turnkey products, not consulting.

**Chloe's quote**: "Our biggest revenue generator that we've never tapped is the trauma graph. If it gets built, we don't have to take on YWCA anymore unless we really want to. It will position me where I should be - pumping out research."

**The vision**:
- Every neighborhood in the US eventually has trauma data
- Clients commission trauma graphs (St Paul, Philadelphia, national, etc.)
- All data feeds into one living system
- Clients pay to license access (view insights, never raw data)
- Stop doing one-off consulting, focus on scalable products

**Andrea's quote**: "It's one big central platform for everything we make. What we make can be accessed by clients if they want to pay us to access it. It just sells itself."

---

## Priority Decision: What to Build First

**Chris asked**: If you had to build one of the three products first, which would it be?

**Andrea**: "Build YWCA so they can leave us alone" (but really just wants them off her back)
**Nina**: "Trauma graph" (most exciting, most valuable)
**Chloe**: "Trauma graph + internal data warehouse. Build our stuff, retrofit clients later."

**The team decision**: Build internal data warehouse + trauma graph FIRST. White label for YWCA comes SECOND (retrofitted).

**Why**: Trauma graph is their revenue generator. YWCA isn't in a rush. They should stop prioritizing clients and start building what they need.

---

## Technical Feasibility (Your Question)

**Can this be built?** Yes, absolutely.

**Complexity**: 7/10 (Medium-High, but nothing impossible)
- Real-time collaboration: Solved problem (Google Docs, Figma, etc.)
- Geographic mapping: Standard map libraries
- Living insights repository: Database + version control
- User access tiers: Standard auth/permissions

**Business feasibility**: 8/10 (High)
- Clear revenue model (license trauma graph access)
- Real pain points (Max QDA sucks, manual map coloring)
- Client base exists (YWCA contracted, others want trauma graphs)
- Team is motivated and aligned

**Risk**: 4/10 (Medium-Low)
- Internal tool first (controlled users, can iterate)
- Client white labels later (retrofitted, simpler)
- Revenue model proven (people already commission trauma graphs)
- Team knows exactly what they want

---

## What I Got Completely Wrong

### I Thought:
- Project was for YWCA
- Helping 196 chapters replace 61-page survey
- Grant writing was core feature
- Trauma graph was add-on for YWCA
- You were hired to build for YWCA

### Reality:
- Project is for 10Seven (internal research)
- YWCA is just one white-label client (secondary)
- Qualitative coding collaboration is core feature
- Trauma graph + internal warehouse IS the product
- You were hired to build 10Seven's research platform

### What I Got Right:
- Research infrastructure disguised as operational tool ✅
- PhD-level complexity with simple interface ✅
- Multi-tenant architecture ✅
- Geographic mapping is central ✅
- Collaboration is critical ✅

---

## Next Steps

### From Team to You:
- Chloe: Sending step-by-step trauma graph process + St Paul report (severity levels)
- Andrea: Sending architecture sketches (how products connect) + brand access flow
- Team: Provide YWCA grant examples if available

### From You to Team:
- Define standardized language for how three products communicate
- Send architecture suggestions after receiving their materials
- Monday follow-up meeting (11am PST)

---

## Bottom Line

**What you're building**: Collaborative research platform for 10Seven's internal work. Qualitative coding + quantitative analysis + geographic mapping + living insights repository.

**Three products**: Internal warehouse (priority #1), Trauma graph (priority #2), White label for clients (secondary - do later).

**Build order**: Internal first, clients later. "Build our stuff, retrofit to clients."

**Business model**: Stop consulting, license trauma graph access, Chloe pumps out research, turnkey products.

**Feasibility**: Yes (7/10 complexity), business model is solid (8/10), risk is low (4/10).

**Your role**: Build 10Seven's internal research infrastructure. YWCA is a side project to retrofit later.
