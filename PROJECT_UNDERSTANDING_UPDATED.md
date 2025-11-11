# Project Understanding - The Impactory (UPDATED AFTER MONDAY FOLLOW-UP)

**Last Updated**: After Monday follow-up call
**Status**: Major scope expansion confirmed
**What Changed**: Full survey builder + enhanced quant analysis + mobile apps now required

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

## 🆕 MONDAY FOLLOW-UP: Scope Expansion

### Critical New Requirements:

**1. Survey Builder Platform (NEW)**
- Replace Qualtrics entirely with custom survey tool
- Question types: Multiple choice, text input, file uploads, rating scales
- **Skip logic** (conditional questions: "if answer A, show question B")
- Data export to spreadsheet
- Survey distribution and response collection
- Not fancy, but functional - focus on research needs

**Chloe's quote**: "I would honestly love to get away from another platform. It is literally a survey where people are inputting their answers."

---

**2. Enhanced Quantitative Analysis (Much More Critical)**
- Comparable to Qualtrics Stats IQ + SPSS functionality
- Statistical functions needed:
  - Correlations (Pearson, Spearman)
  - P-values and statistical significance testing
  - Regression analysis
  - Cross-tabulation (disaggregate by demographics + geography)
  - Correlation matrices (extensive tables showing all variable relationships)
- **Data visualization preference: 90% TABLES**
  - Cross-tabs are primary output
  - Occasional pie charts or line graphs
  - Tables are what gets reported, not fancy charts
- Quick preliminary analysis (like Stats IQ) + advanced analysis (like SPSS/R)

**Chloe's quote**: "If we could get something that gives me some quantitative solution... If all of that was in one place for us, that would be a huge game changer, huge."

---

**3. Target Audiences Expanded & Clarified**

**B2B Institutional Clients**:
- **Think tanks**: Brookings Institute, Aspen Institute, policy research organizations
- **Government bodies**:
  - White House councils (pre-admin)
  - Mayors and local governments (use for policy testing, reparations distribution, impact modeling)
  - Example: St Paul used trauma graph to distribute reparations + model medical debt cancellation impact
- **Nonprofits**: Strategy planning, community outreach, program placement

**B2C Individual Users**:
- **Researchers**: Academic, independent researchers
- **Financial professionals**: Financial counselors, financial advisors (trauma data for client work)
- **Parents**: ⭐ **MASSIVE UNTAPPED MARKET**
  - "Parents would go berserk over our content"
  - Most common email inquiry: "How do I get access? You're not in my kid's school"
  - 10Seven started in K-12 financial education space
  - Content exists, market is proven, just needs access infrastructure

---

**4. Map Features & Filters Finalized**

**Technology Confirmed**: **Mapbox** (Chloe researched it, loves the features, prototype validated it)

**Reference Examples They Want to Emulate**:
- **Eviction Lab (Princeton)**: Dynamic zoom, national→state→county→neighborhood, uses Mapbox, clean design
- **Mapping Police Violence**: Living/real-time updates, neighborhood-level detail, event tracking over time
- **Urban Institute Wealth Dashboard**: Census tract filtering, multiple metric overlays, demographic disaggregation

**Filter Types Required**:

1. **Location-based filters** (standard):
   - Zip code, county, state, neighborhood
   - Drill-down hierarchy (national → state → county → neighborhood)
   - **Granularity = premium feature** (neighborhood-level detail more valuable than state-level)

2. **Event-based filters** (NEW CONCEPT):
   - **Time periods**: Pre/post administration changes, specific policy eras
   - **Policy events**: SNAP benefit cuts, federal layoffs, stimulus payments, eviction moratoriums
   - **Historical periods**: 1950s redlining, interstate highway displacement, historical trauma mapping
   - Example: "Show financial trauma in DC/VA/MD before and after federal worker layoffs"
   - Allows tracking how specific events impact trauma levels

3. **Map type selection**:
   - Severity maps (basic)
   - Multiple oppressions overlays (trauma + other public issues)
   - Historical trauma graphs (archival maps overlaid with trauma data)

**Premium Feature Structure - Two Vectors**:

**Vector 1: Map Interactivity**
- **Static maps**: General shading, minimal interaction (like basic state-level choropleth)
- **Dynamic maps** (PREMIUM): Zoom in/out, click bubbles for details, explore data interactively

**Vector 2: Dimensionality**
- **Basic**: Severity map only (single dimension)
- **Premium**: Multiple dimensions overlaid
  - Example: Financial trauma + domestic violence rates + childcare deserts all on one map
  - Example: Financial trauma + maternity care deserts + food deserts
  - "Multiple oppressions" analysis - most valuable to clients

**Chloe's quote**: "Granularity... that's of high value?" Chris: "Big time."

---

**5. Marketing Strategy Finalized**

**DO market publicly**:
- Trauma graph licensing (primary product)
- Ed Hub white label (education side)

**DON'T market publicly**:
- White label for institutional clients (YWCA-type)
- Only offer when client specifically requests it

**Reasoning**:
- "Do I think we're going to get a lot of YWCA clients? No"
- "People are going to stop at the trauma graph, like, that's really what they want"
- YWCA needs are "so basic" - simple data storage, not sophisticated research tools
- Focus marketing on high-value product (trauma graphs), not low-value white label

---

**6. Trial Licensing Model (NEW)**
- Chloe does keynote speeches at conferences
- Attendees receive **14-day access code** to trauma graph
- Can explore full functionality during trial
- Receive discount if they purchase license after trial expires
- **Lead generation strategy**: Convert speaking engagements into licensed clients

---

**7. Pricing Strategy**
- **Premium users** (extensive trauma graph access): **Usage-based pricing**
  - Rationale: "So many maps, so much data" - hard to price as flat rate
  - Example: 20 cents per minute of access, or per map view
  - Allows easy rate adjustments (raise/lower across the board)
- **Basic/Standard users**: Potentially flat-rate tiers
- Packaging into bundles/tiers to simplify selection (à la carte gets overwhelming)

---

**8. UX Challenge Identified**
- Competitors (Eviction Lab, Mapping Police Violence) focus on **ONE dimension** (just evictions, just police violence)
- 10Seven looks at financial trauma across **MANY dimensions** (housing + health + food + childcare + historical + policy events)
- This is powerful but potentially overwhelming
- Need to make multi-dimensional data selection **not overwhelming**
- Solution: Package into tiers/bundles, à la carte add-ons, clear progressive disclosure

---

**9. Mobile Apps Confirmed**
- All products will likely have mobile versions (not just desktop web apps)
- Impacts tech stack decision significantly:
  - Firebase has native iOS/Android SDKs, excellent offline sync, proven at mobile scale
  - Supabase mobile support is newer, more manual (REST + websockets)
- Possible hybrid approach: Supabase for internal desktop tool, Firebase for mobile white label apps

---

**10. Current Tool Ecosystem (Why They Need This)**
- **Qualtrics**: Survey building + basic stats
- **Max QDA**: Qualitative coding (doesn't collaborate well)
- **SPSS / R** (Allison uses): Advanced statistical analysis
- **Adobe Illustrator / Procreate**: Manual map coloring (3,000 counties by hand!)
- **Google Docs / Email / Text**: Sharing insights, articles (not captured in system)

**Problem**: "I wish it was all in one place"

**Goal**: Build ONE platform that replaces all of these tools and integrates the entire workflow.

---

## The Three Products (In Priority Order)

### 1. Internal Data Warehouse - "The Patient Chart System" (PRIORITY #1)

**Purpose**: 10Seven's internal collaborative research platform
**Users**: Chloe, Nina, Andrea, Allison (internal team only)
**Never shared with clients**

**The "Patient Chart" Analogy (Chloe's Words)**:
> "I think of it like a patient chart at a hospital. You can see all their labs, but you also see the doctor's notes from each visit. Andrea shouldn't have to have a 2-hour conversation with me to understand Philadelphia from 3 years ago. She should click on Philadelphia and see what I discovered, when, and why."

**What It Needs**:

**Survey Builder (NEW - Replaces Qualtrics)**:
- Question types: Multiple choice, text input, file uploads, rating scales, Likert scales
- **Skip logic**: Conditional question display based on previous answers
- Survey distribution (links, embeds)
- Response collection and management
- Data export to spreadsheet (for analysis)
- Simple, functional, research-focused (not marketing-focused)
- reCAPTCHA integration
- Preview mode before publishing
- Logo and color customization (minimal branding)

**Quantitative Analysis Suite (MUCH More Important Than Initially Thought)**:
- **Statistical tests**:
  - Correlations (Pearson, Spearman)
  - P-values and statistical significance testing (< 0.05)
  - Regression analysis (linear, logistic)
  - Chi-square tests
- **Cross-tabulation**:
  - Disaggregate by demographics (race, gender, age)
  - Disaggregate by geography (zip, county, state)
  - Multi-dimensional cross-tabs
- **Correlation matrices**:
  - Show all variable-to-variable correlations in table format
  - Extensive tables (can be quite large)
  - Helps identify which questions to analyze deeper
- **Quick preliminary analysis** (like Qualtrics Stats IQ):
  - Click two questions → see if they're correlated
  - See p-value immediately
  - See statistical test results
  - Export tables/charts
- **Data visualization: 90% TABLES**:
  - Cross-tabulation tables (primary output)
  - Correlation matrices
  - Occasional pie charts, line graphs (secondary)
  - Tables are what gets reported in final documents
- **Comparable to**: Qualtrics Stats IQ for quick analysis, SPSS/R for advanced analysis
- Team members can run their own analyses (not just Allison)
- Real-time visibility (others can see analysis in progress)

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

**Complexity**: 7/10 → 8/10 (Medium-High → High, but nothing impossible)
- **Survey builder**: Standard but requires skip logic implementation (4/10)
- **Statistical analysis**: Correlations, p-values, regression (6/10 - needs compute)
- **Real-time collaboration**: Solved problem with CRDT libraries (7/10)
- **Geographic map coloring**: Standard libraries + Mapbox (5/10)
- **Living insights repository**: Database + version control (6/10)
- **Mobile apps**: Native SDKs or React Native (7/10)
- **User access tiers**: Standard auth/permissions (4/10)
- **Event-based filtering**: Temporal queries (5/10)

**Increased Complexity Due To**:
- Survey builder with skip logic (NEW)
- Enhanced quantitative analysis suite (expanded scope)
- Mobile app versions (NEW)
- Event-based filters (NEW)

**Business Feasibility**: 8/10 (High)
- Clear revenue model (license trauma graph, usage-based pricing)
- Real pain points (Max QDA, Qualtrics, manual coloring, siloed tools)
- Multiple target audiences identified (B2B institutional, B2C individual, parents)
- Trial licensing model for lead generation
- Client base exists + massive untapped market (parents)
- Team motivated and aligned

**Risk Level**: 4/10 → 4.5/10 (Medium-Low → Medium)
- Internal tool first (controlled users) ✅
- Client white labels later (retrofitted) ✅
- Revenue model proven (people commission graphs already) ✅
- Team knows what they want ✅
- **Slightly higher risk**: Expanded scope (survey builder + enhanced quant) increases development time and complexity

**Tech Stack Considerations** (Post-Monday Analysis):
- **Mobile apps required**: Impacts database choice significantly
  - Firebase: Native iOS/Android SDKs, excellent offline sync, proven mobile scale
  - Supabase: Newer mobile support, more manual (REST + websockets)
- **Statistical analysis**: PostgreSQL has native stats functions (corr, regr_slope) - advantage for Supabase
- **Geographic queries**: PostGIS (Supabase) >> GeoFirestore (Firebase) for polygons/hierarchies
- **Version history**: PostgreSQL temporal tables (Supabase) vs manual implementation (Firebase)
- **CLI workflow**: Supabase SQL migrations vs Firebase manual data migration scripts
- **Real-time collaboration**: Both support (Firestore listeners vs Supabase subscriptions)
- **Recommendation**: **Hybrid approach** or **Supabase + mobile optimization**
  - Option A: Supabase for internal warehouse (desktop), Firebase for mobile white label apps
  - Option B: Supabase for everything, invest in mobile optimization (React Native + Supabase client)

---

## Next Steps

### ✅ Completed:
- Thursday call (project pivot discovered)
- Monday follow-up call (scope expansion confirmed)
- Defined standardized language for three products
- Clarified survey builder + quant analysis requirements
- Confirmed Mapbox + mobile apps
- Aligned on target audiences and premium features

### Waiting For (From Team):
- ✅ Nina: Qualtrics login credentials (for Chris to explore Stats IQ functionality)
- Pending: St Paul report with severity level examples and multiple map types
- Pending: Andrea's architecture sketches (how products connect, brand access flow)
- Pending: YWCA grant examples (if available)

### To Do (Chris):
- Explore Qualtrics Stats IQ (once login credentials received from Nina)
- Finalize tech stack recommendation (Supabase vs Firebase vs Hybrid approach)
- Create client alignment document (for team review before proposal)
- Prepare comprehensive proposal:
  - Cost estimate
  - Timeline estimate (considering expanded scope)
  - Phased roadmap (survey builder + quant + qual + maps)
  - Tech stack justification
- **Travel dates**: Nov 28 - Dec 9 (email access only, no calls)

---

## Files Updated

**Thursday Call**:
- **thursday_call_transcript.md** - Full transcript
- **CALL_ANALYSIS_thursday.md** - Detailed analysis (29 pages)
- **THURSDAY_SUMMARY.md** - Plain English summary

**Monday Follow-Up**:
- **monday_followup_transcript.md** - Full transcript (to be created)
- **monday_followup_analysis.md** - Analysis of scope expansion (to be created)

**Updated Documentation**:
- **PROJECT_UNDERSTANDING_UPDATED.md** - This file (updated with Monday findings)
- **SESSION_CONTEXT_UPDATED.md** - Session context (updated with Monday findings)
- **STANDARDIZED_LANGUAGE_ARCHITECTURE.md** - May need updates for survey builder integration

**Tech Stack Analysis**:
- **Firebase vs Supabase comparison** - Comprehensive analysis completed
- **Recommendation**: Hybrid approach or Supabase with mobile optimization

---

## Bottom Line (Updated After Monday)

**What You're Building**: End-to-end integrated research platform for 10Seven - survey builder + qualitative coding + quantitative analysis + trauma graph licensing + mobile apps. NOT a YWCA project.

**Goal**: Replace Qualtrics, Max QDA, SPSS, and Adobe Illustrator with ONE integrated platform.

**Three Products (Priority Order)**:
1. **Internal data warehouse** ("patient chart system") - BUILD FIRST
   - Survey builder (replace Qualtrics)
   - Quantitative analysis suite (Stats IQ + SPSS-level)
   - Collaborative qualitative coding (replace Max QDA)
   - Living insights repository
   - Automated map coloring (Mapbox)
   - Version history and real-time collaboration

2. **Trauma graph** (interactive maps for licensing) - BUILD SECOND
   - Mapbox-based dynamic maps
   - Event-based filters (policy events, historical periods)
   - Two-tier premium model (static/dynamic + basic/multidimensional)
   - Trial licensing (14-day conference codes)
   - Multiple target audiences

3. **White label** for clients (YWCA simplified version) - BUILD THIRD
   - Basic data storage
   - Simple queries
   - Optional trauma graph license add-on
   - NOT marketed publicly (except Ed Hub)
   - Mobile versions likely

**Business Model**:
- License trauma graph access (primary revenue)
- Usage-based pricing for premium users
- Trial licensing at speaking engagements (lead generation)
- Stop consulting, focus on scalable products
- Multiple market segments: B2B institutional, B2C individual, **parents (huge untapped market)**

**Target Audiences**:
- Think tanks (Brookings, Aspen), Government bodies (mayors, councils), Nonprofits
- Researchers, Financial advisors
- **Parents** (K-12 financial education - most common inquiry, massive potential)

**Feasibility**: Yes (8/10 complexity due to expanded scope), solid business model (8/10), medium risk (4.5/10)

**Tech Stack**:
- **React + Node** (Chris's comfort zone)
- **Supabase recommended** for internal warehouse (PostgreSQL + PostGIS for geo queries, native stats functions, CLI workflow, version history)
- **Mapbox** for maps (confirmed)
- **Mobile**: Hybrid approach (Supabase internal, Firebase mobile) OR Supabase + React Native optimization
- **Yjs** for collaborative text editing (CRDT layer)

**Your Role**: Build 10Seven's end-to-end research infrastructure. Replace their entire tool stack with one integrated platform. YWCA is a side project to retrofit later.

**Key Insights**:
1. **Thursday**: This is 10Seven's platform, not YWCA's
2. **Monday**: Scope is much larger - full survey platform + enhanced quant analysis + mobile apps required
3. **Parents market**: Massive untapped B2C opportunity (K-12 financial education)
4. **Integration is key**: "If all of that was in one place... that would be a huge game changer, huge"
