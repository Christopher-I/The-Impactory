# Thursday Call Analysis - The Real Project Revealed

**Date**: Today
**Duration**: ~1 hour
**Participants**: Chloe (63%), Andrea (19%), Christopher (13%), Nina (4%)

---

## 🚨 MASSIVE REVELATION: THIS IS NOT THE PROJECT I UNDERSTOOD

### What I Thought:
- Project was primarily for YWCA
- Helping 196 YWCA chapters replace their 61-page survey
- Helping chapters write grants and manage data
- Chris hired to build for YWCA as primary client

### What It Actually Is:
- **Project is primarily for 10Seven's internal research work**
- YWCA is just one client who will get a simplified white-label version
- The real product is **trauma graph + internal data warehouse for 10Seven**
- Chris was hired to build 10Seven's internal research infrastructure
- YWCA white label is **secondary** (and they want to deprioritize clients)

---

## The Three (Actually Four) Products

### 1. **Internal Data Warehouse** (Core - "The Patient Chart System")
**Purpose**: 10Seven's internal research infrastructure
**Users**: Chloe, Nina, Andrea, Allison (internal team only)
**What it needs**:
- Collaborative qualitative coding platform (better than Max QDA)
- Real-time collaboration (see each other working live, like Google Docs)
- Highlight text → create codes → auto-tally across all interviews
- Field notes visible to whole team (not siloed per person)
- Split screen: transcript on left, field notes on right
- Geographic data tracked per interview (zip code, neighborhood)
- Automated severity calculations and map coloring
- Notes/insights attached to geographic locations that persist over time
- Version history ("what changed? why did it change?")
- NOT a spreadsheet - more like old AirTable (notes not buried in comments)
- Living repository of historical insights

**Key Quote from Chloe**: "It's a patient chart system - you can see all their labs, but also the notes from doctors. Andrea shouldn't have to have a 2-hour conversation with me to understand Philadelphia trauma graph from 3 years ago. She should just click on a neighborhood and see what I thought on this day, where I got insights from."

### 2. **Trauma Graph** (Revenue Generator - Never Fully Built)
**Purpose**: Interactive maps showing financial trauma, domestic violence, etc. by geography
**Users**: Clients who license access (view only, never see raw data)
**What it is**:
- NOT just a map visualization
- It's the entire system: data collection → coding → analysis → mapping → insights
- National level (3000 counties), city level (neighborhoods), custom
- Severity levels 1-4 with color coding
- Clients can click on counties/neighborhoods to see insights (not raw data)
- "Living map" - continuously updated as new data comes in
- Team members can add notes, articles, secondary data to locations
- Eventually: every neighborhood in the US completed with all data

**Key Quote from Chloe**: "Our biggest revenue generator that we've never tapped is the trauma graph. If it gets built, we don't have to take on YWCA anymore. It will position me where I should be - pumping out research."

**Key Quote from Andrea**: "Our vision is that every single neighborhood in the US is complete with all the data we could ever find."

### 3. **White Label for Clients** (YWCA Example)
**Purpose**: Simplified version for clients to store their data + optional trauma graph access
**Users**: YWCA (and future clients)
**What it needs**:
- Much simpler than internal tool
- Data entry for their info (how many programs, how many people served, etc.)
- Simple queries ("how many local associations have childcare?")
- Replace their endless surveys with continuous data entry
- Optional add-on: License access to view 10Seven's trauma graph
- Side-by-side: their data + 10Seven's trauma graph insights

**Key Quote from Andrea**: "I just want to build YWCA so they can leave us alone. The dynamic between YWCA USA and local associations is fraught. I feel like the white label option is pretty simple to build and hand over."

**Key Quote from Chloe**: "YWCA white label - they will warehouse their own data. But yes, it is all our internal stuff that we will never share. Yes, you can click on maps and see our insights, but you'll never get the data. You'll always get the insight."

### 4. **ED Hub** (Already Being Built)
**Purpose**: Education platform
**Status**: Already in development, not part of this scope

---

## The Big Business Strategy Question

**Chris asked**: If you had to build one product first, which would it be?

**Andrea's answer**: "Build YWCA first so they can leave us alone" (but really just wants them off her back)

**Nina's answer**: "Trauma graph" (clients aside, what's most exciting and valuable)

**Chloe's answer**: "Trauma graph. To build it, we technically need the internal data warehouse. But I think we should build our stuff and retrofit everything to clients."

**Key Quote from Chloe**: "Clients be damned. We've always prioritized them, and they don't need to feel neglected. But internally we should start deprioritizing them compared to what we need. The trauma graph is our biggest revenue generator. If it gets built, we don't have to take on YWCA anymore unless we really want to."

**The Decision**: Build internal data warehouse + trauma graph FIRST. Then retrofit white label versions for clients.

---

## Their Current Research Workflow (Step by Step)

### Step 1: Survey Design & Data Collection
- Update survey questions (currently in Google Docs/Word - wish it was in one place)
- Build survey in Qualtrics (or cheaper alternative)
- Blast survey via paid firm + partner orgs
- Target: Minimum 500 respondents (ideally 100+ per geographic area)
- Collect both quantitative (survey) and qualitative (interviews) data

### Step 2: Qualitative Interviews
- Recruit interview participants through survey
- Pay people for their time (must do survey + interview to get paid)
- Record interviews, get transcripts
- Take field notes during interviews (note when someone cries, points to object, etc.)
- Field notes are data too, but currently siloed per person

### Step 3: Qualitative Coding (MAJOR PAIN POINT)
**Current tool**: Max QDA
**Process**:
- Read transcript, highlight relevant sentences
- Tag with code (category) - "meaningful community," "housing insecurity," "zip code," etc.
- Tool auto-tallies how many times each code appears across ALL interviews
- Identify "saturated themes" (codes that appear most frequently)
- Do multiple rounds: first pass individual, then team consolidates similar codes

**Current problems with Max QDA**:
- ❌ NOT real-time collaborative (they say it is, but it doesn't work like Google Docs)
- ❌ If Nina and Chloe work simultaneously, it glitches
- ❌ You can't see each other's work until it's done
- ❌ Field notes are siloed - Chloe's field notes aren't visible to Nina in the file
- ❌ Forces Chloe to code all the people she interviewed (can't share field notes)

**What they need**:
- ✅ Real-time collaboration (like Google Docs)
- ✅ Highlight sentence → tag with code → auto-tally across all interviews
- ✅ See codes ranked by frequency (saturated themes)
- ✅ Click on code to see all instances across all transcripts
- ✅ Split screen: transcript on left, field notes on right
- ✅ Team can see each other's field notes
- ✅ Track geographic data (zip code, neighborhood) as codes
- ✅ Special "WOW" highlighting (great quotes for reports, not necessarily themes)

**Key Quote from Chloe**: "Max QDA is very simple and beautiful, but it's not collaborative. Nina and I should be able to work on it together simultaneously, and we cannot. In grad school we'd just do it in Google Docs with comments, but then you have to manually tally everything."

### Step 4: Quantitative Analysis
- Run correlational analysis, regression analysis (not super complex)
- Usually in Qualtrics Stats IQ, SPSS, or R
- Analyze independently from qualitative
- Then compare: do quan and qual insights overlap?

### Step 5: Identify Themes & Geographic Patterns
- Pick top 3-5 codes by tally (saturated themes)
- Cross-reference with geography: Where do these themes appear?
- Look for concentrations: "40 people talked about traumatizing banking events, 20% from same zip code"
- This is where mapping starts

**Can be automated**: Once codes are identified, system could auto-generate report: "Your top theme is X, happening in these neighborhoods"

### Step 6: Assign Severity Levels
- Judgment call based on qualitative severity
- Level 1-4 severity index
- Rules like: "If >40% of respondents from this neighborhood exhibit X, Y, Z = Level 4"
- Example from St Paul: People doing self-harm when unexpected bills arrive = severe

**Can be automated**: Feed spreadsheet with severity rules → system assigns levels → auto-colors map

### Step 7: Map Coloring (MAJOR PAIN POINT)
**Current process**:
- Find "base map" (license US counties map, or pull city neighborhood map from city website)
- Manually click each geographic region and change color
- National map: Clicked all 3000 counties by hand in Adobe Illustrator
- St Paul neighborhood map: Used Procreate app on iPad, dragged colors into streets

**Current problems**:
- ❌ Extremely tedious (clicked 3000 counties by hand)
- ❌ No centralized map source for all cities at neighborhood level
- ❌ Have to find/license different maps for different geographies
- ❌ Manual work every single time

**What they need**:
- ✅ Feed spreadsheet with: [County/Neighborhood, Severity Level 1-4, Color code]
- ✅ System auto-colors map based on spreadsheet
- ✅ Can update map when new data comes in (track changes over time)

**Key Quote from Chloe**: "I could give you a spreadsheet of 3000 answers with severity levels, and the model should go change the color in that geo tag, as opposed to me doing it."

### Step 8: Write Insights & Build Report
- Synthesize themes into narrative
- Write what's happening, why it matters, what's unique to this area
- Create multi-dimensional maps (different themes on different maps)
- Publish report

**Current problems**:
- ❌ Insights only exist in Chloe's head or final report
- ❌ Team gets insights "second-hand when it's done"
- ❌ No record of WHY a decision was made 3 years ago
- ❌ Andrea can't see Chloe working in real-time
- ❌ If Andrea wants to reference Chicago vs. St Paul, she has to ask Chloe or re-read reports

**What they need**:
- ✅ Living repository of insights attached to geography
- ✅ Click on neighborhood → see all historical notes/insights
- ✅ Version history: "What changed? Why did it change?"
- ✅ Team can add notes, respond to each other's insights
- ✅ Ability to reference New York Times articles or secondary data
- ✅ "If you're going to noodle in data today, write down your thoughts and submit it"

---

## The "Patient Chart" Analogy (CRITICAL CONCEPT)

**Chloe's Analogy**: "I think of it like a patient chart at a hospital system. You can see all their labs, but you also might put in your note after rounds. The person coming on shift next can see: what was that person thinking? Oh, they gave a Tylenol. That's what this needs to be."

**What this means**:
- Not just a database of data
- Not just a mapping tool
- It's a **living knowledge system** where insights accumulate over time
- Historical record of: What did we find? When? Why? What changed?
- Team members can "click on Philadelphia" and see everything Chloe discovered 3 years ago
- No more 2-hour lectures to get team up to speed on past work

**Andrea's Addition**: "I should be able to click on a state, zoom to county, zoom to neighborhood. At each level, read what Chloe wrote, add my own notes, respond to her comments, add data points I find (like NY Times articles). Easy to source secondary data and attach to specific locations."

**Key Insight**: They currently text each other interesting articles. They need a system to capture all of this information and attach it to the trauma graph.

---

## What "Trauma Graph" Actually Means

It's NOT just an interactive map. It's the entire ecosystem:

1. **Data Collection** (surveys + interviews)
2. **Qualitative Coding** (collaborative platform)
3. **Quantitative Analysis** (correlations, regression)
4. **Theme Identification** (saturated themes)
5. **Geographic Mapping** (themes → zip codes/neighborhoods)
6. **Severity Assignment** (Level 1-4 index)
7. **Map Visualization** (color-coded by severity)
8. **Insights Repository** (living notes attached to locations)
9. **Version History** (track changes over time)
10. **Client Access** (license to view insights, never raw data)

**The Vision**: Every neighborhood in the US eventually has complete data. They build it piece by piece as they get commissioned for different trauma graphs (St Paul, Philadelphia, national, etc.). All data feeds into one living system.

---

## The Licensing Model

**Internal Access** (10Seven team):
- Full back-end access to everything
- See all data, all codes, all insights, all maps
- Can add/edit/collaborate in real-time

**Client Access** (YWCA, future clients):
- View-only access to trauma graph insights
- Never see raw data, only insights and visualizations
- Can click on neighborhoods to see findings
- Optional add-on to their white label data warehouse

**Education Access**:
- Person who signs up for ED Hub course
- Only sees courses they've enrolled in
- Different tier from YWCA

**Key Quote from Andrea**: "It's one big central platform for everything we make. What we make can be accessed by clients if they want to pay us to access it. It just sells itself."

---

## Current Pain Points (Prioritized)

### 1. **Max QDA is Not Collaborative** (CRITICAL)
- Can't work simultaneously in real-time
- Field notes are siloed per person
- Updates don't sync like Google Docs
- Glitches when multiple people logged in
- Forces Chloe to code all her own interviews

### 2. **Manual Map Coloring is Tedious** (HIGH)
- Clicked 3000 counties by hand
- Used iPad app to drag colors into neighborhoods
- No automation, completely manual every time
- Have to find/license base maps for every new city

### 3. **No Living Repository of Insights** (HIGH)
- Insights only exist in reports or Chloe's head
- Team gets updates "second-hand when it's done"
- Can't see what Chloe discovered in Philadelphia 3 years ago
- No version history of changes
- Constantly texting articles/insights to each other (not captured in system)

### 4. **Siloed Workflows** (MEDIUM)
- Chloe works in Max QDA
- Allison works in Qualtrics/SPSS
- Nina and Andrea get results after the fact
- Can't see work in progress
- No shared visibility until work is done

### 5. **No Standard Platform for Surveys** (LOW)
- Currently use Qualtrics (expensive) or alternatives
- Would be nice to build surveys in the same platform
- Skip logic, blast links, collect responses
- Chris suggested it might be easy to build

---

## What They Need (Detailed Requirements)

### Collaborative Qualitative Coding
- Highlight text in transcript
- Tag with code (category)
- Auto-tally across all interviews
- See ranked list of codes by frequency (saturated themes)
- Click code to see all instances across transcripts
- Multiple highlight colors (blue for themes, yellow for "WOW" quotes)
- Split screen: transcript + field notes side by side
- Field notes visible to whole team
- Real-time collaboration (see each other working, like Google Docs)
- Geographic codes (zip code, neighborhood) tracked automatically

### Automated Map Coloring
- Upload base map (or select from library)
- Label all polygons (counties, neighborhoods) on back end
- Feed spreadsheet: [Location, Severity 1-4, Color code]
- System auto-colors map
- Update map when new data comes in
- Track version history

### Living Insights Repository
- Click on geographic location (state, county, neighborhood)
- See all historical notes/insights for that location
- Add new notes, respond to team members' comments
- Attach secondary data (NY Times articles, external research)
- Split screen: data on left, insights/notes on right
- NOT just spreadsheet - more like old AirTable (notes not buried)
- Version history: what changed, when, why

### Quantitative Analysis
- Import survey data
- Run correlations, regression analysis
- Comparable to Qualtrics Stats IQ, SPSS, R
- Allison should be able to run analyses
- Chloe can see results in real-time

### Survey Builder (Nice to Have)
- Build surveys with skip logic
- Blast links to respondents
- Collect responses
- Track response rates
- Alternative to Qualtrics

---

## What Can Be Automated vs. Manual

### Can Be Automated ✅
- Tally codes across interviews
- Rank codes by frequency (saturated themes)
- Map codes to geography (if zip code/neighborhood is coded)
- Generate report: "Top theme is X, happening in these neighborhoods"
- Assign severity levels based on rules (if >40% = Level 4)
- Color maps based on severity spreadsheet
- Track version history of changes

### Must Remain Manual ❌
- Reading transcripts and deciding what to highlight
- Creating codes (categories) - "let the data tell us"
- Consolidating similar codes across rounds
- Judgment calls on severity (what's "worse" qualitatively)
- Finding base maps for new cities (no universal source)
- Labeling map polygons on back end (one-time setup per city)
- Writing insights and narrative

**Key Quote from Chloe**: "It is a very manual process, and I think that's important. There's not a lot that can be automated. But the automation is: as soon as I tally something under a code or zip code, if that can be automated, that saves me a lot of time."

---

## Ideal User Experience (In Their Words)

### Chloe's Ideal:
"More like old AirTable - a spreadsheet but I can put notes and things. NOT Excel where comments get buried. Split screen: data on left, I can type my thoughts/insights on right. Team can respond, add their own insights. Communication about data as we're looking at it together."

### Andrea's Ideal:
"I can go to the map, click on a state, zoom to county, zoom to neighborhood. At each level, I can read what Chloe wrote or add notes myself. For data we have in those places, I can pull it up on a split screen. Maybe there's an edit button where I can add notes, respond to Chloe's comments, add data points I see. Like: I saw this NY Times stat about this neighborhood, I want to make a note on the trauma graph."

### The "MyChart" Comparison:
"It's like MyChart for a hospital. You can see all your lab results, prescriptions, visit history. But you can also see notes from each doctor visit. That's what we need - data + historical record of insights."

---

## The "Living Map" Concept

**Not a one-time deliverable. It's continuously updated.**

- Maps are built for specific projects (St Paul, Philadelphia, national)
- New data comes in → map gets updated
- Team adds notes, articles, insights over time
- Version history tracks what changed
- Eventually: every neighborhood in US is complete
- Multiple clients can commission trauma graphs for same area
- All data feeds into one system, but clients only see what they license

**Key Quote from Chloe**: "We have that trauma graph for the nation, but Allison and I totally forgot we have 532 new women who have taken the survey. We haven't updated it yet. We want a record of: what changed? Why did it change?"

**Key Quote from Andrea**: "Even though we might have a trauma graph for a city commissioned by three different partnerships, that data we own and we want to put it all into that living map."

---

## YWCA White Label (What They Actually Need)

**Much simpler than internal tool**

What YWCA needs:
- Data entry for their programs/services
- Simple queries: "How many local associations have childcare?"
- Replace endless surveys with continuous data entry
- Store data like: How many buildings do you own? How many people served?
- Generate simple reports
- Optional add-on: License trauma graph access
- Side-by-side view: their data + 10Seven's trauma graph insights

**Key Quote from Andrea**: "They're not super sophisticated around data. It's not like we need Max QDA or complex lookups. It's really simple for them to go: how many local associations have childcare? Pull that number. That's their white label version."

**Current Dynamic**: "The relationship between YWCA USA and local associations is fraught. USA doesn't give them support. They're like independent children trying to raise themselves. USA drags their feet. I just want to build something simple, hand it over, and they can leave us alone."

**Status**: Andrea is creating slides to redefine what they're delivering to YWCA (it's been a while since they talked, YWCA just got new funding).

---

## Key Technical Challenges

### 1. **Real-Time Collaboration**
- Must work like Google Docs (see each other typing/working in real-time)
- Multiple people editing same transcript simultaneously
- Field notes visible to whole team as they're written
- No glitches when multiple users logged in

### 2. **Geographic Data Mapping**
- No universal source for neighborhood-level maps for every US city
- Have to find/license base maps for each new city
- Need to label all polygons on back end (one-time setup)
- Then feed severity data via spreadsheet → auto-color
- Track changes over time (version history)

### 3. **Standardized Language Across Three Products**
- Internal data warehouse
- Trauma graph (client-facing)
- White label (YWCA and future clients)
- All three need to communicate with each other
- Chris will propose architecture after getting more info

---

## Next Steps (Action Items)

### From Chloe:
- ✅ Send step-by-step trauma graph creation process (she already wrote it out)
- ✅ Send St Paul report (shows severity level 1-4 framework)

### From Andrea:
- ✅ Send architecture sketches (how products talk to each other)
- ✅ Send brand access flow (who sees what when they log in)
- ✅ Create slides redefining YWCA deliverables

### From Chris:
- ✅ Define standardized language for how three products communicate
- ✅ Send suggestions after receiving materials
- ✅ Prepare for Monday follow-up meeting (11am PST)

### From Team:
- ✅ Provide YWCA grant examples (if available) - helps understand white label needs
- ✅ Provide mock data if needed for architecture

---

## Critical Quotes (Business Strategy)

**Chloe on Priority**:
"Clients be damned. We've always prioritized them. I think we should start deprioritizing them compared to what we need. Our biggest revenue generator that we've never tapped is the trauma graph. If it gets built, we don't have to take on YWCA anymore unless we really want to. It will position me where I should be - pumping out research."

**Chloe on The Decision**:
"We need to build a trauma graph. To build it, we technically do need to build our internal data warehouse. But I think we should retrofit everything to our clients. Build our stuff, everything else is retrofitted."

**Chloe on YWCA**:
"Stars are aligning now that we have a Chris. We should be building for us and retrofitting what we build to our clients. At the end of the day, we pitched our clients what we're delivering, so they don't know any better. I'm happy to talk about YWCA, but we should focus on what's in the best interest of 10Seven."

**Andrea on YWCA**:
"I just want to build YWCA so they can leave us alone. I feel like the white label option is pretty simple. I'd love to show them an iteration of what it is. But honestly, I don't think they're in any rush. They're not in a rush to do anything ever."

---

## Feasibility Assessment (Updated)

**Technically Feasible**: ✅ Absolutely
- Collaborative text annotation with auto-tally: Standard features
- Geographic map coloring from spreadsheet: Doable with map libraries
- Living insights repository: Database + version control
- Real-time collaboration: WebSockets, operational transform patterns
- User access tiers: Standard auth/permissions

**Complexity Level**: 7/10 (Medium-High)
- Real-time collaboration is always complex
- Geographic mapping at multiple levels requires good data sources
- Three interconnected products need solid architecture
- But nothing impossible - all solved problems

**Business Feasibility**: 8/10 (High)
- Clear revenue model (licensing trauma graph access)
- Real pain points (Max QDA limitations, manual map coloring)
- Client base exists (YWCA already contracted, others want trauma graphs)
- Team is motivated and aligned on vision
- Move away from client consulting toward turnkey products

**Risk Level**: 4/10 (Medium-Low)
- Lower risk than I initially thought
- Internal tool first (controlled users, can iterate)
- Client white labels come later (retrofitted)
- Revenue model proven (people commission trauma graphs already)
- Team knows what they want (detailed pain points, clear workflow)

---

## What Changed From My Previous Understanding

### Before Thursday Call:
- ❌ Project is for YWCA primarily
- ❌ Helping 196 chapters replace 61-page survey
- ❌ Grant writing and chapter data management is core feature
- ❌ Trauma graph is add-on for YWCA
- ❌ Chris hired to build for YWCA

### After Thursday Call:
- ✅ Project is for 10Seven primarily (internal research infrastructure)
- ✅ YWCA is just one white label client (secondary priority)
- ✅ Qualitative coding collaboration is core feature
- ✅ Trauma graph + internal data warehouse is the product
- ✅ Chris hired to build 10Seven's research platform, then retrofit for clients

### What I Got Right:
- ✅ It's research infrastructure disguised as operational tool
- ✅ PhD-level complexity needs simple interface
- ✅ Multi-tenant architecture required
- ✅ Geographic data/mapping is central
- ✅ Collaboration is critical

### What I Completely Missed:
- ❌ This is NOT about YWCA at all
- ❌ Qualitative coding collaboration is the #1 pain point (not survey replacement)
- ❌ "Living map" concept - continuously updated, not one-time
- ❌ "Patient chart" analogy - historical insights attached to geography
- ❌ They want to move away from client consulting entirely
- ❌ Trauma graph is their biggest untapped revenue stream

---

## Bottom Line

**What They're Building**: A collaborative research platform for qualitative + quantitative analysis with geographic mapping and a living repository of insights.

**Three Products**:
1. Internal data warehouse (patient chart system) - PRIORITY
2. Trauma graph (interactive maps for clients to license) - PRIORITY
3. White label for clients (simplified YWCA version) - SECONDARY

**Build Order**: Internal warehouse + trauma graph FIRST. Retrofit white labels for clients SECOND.

**Business Model**: Move away from client consulting → license trauma graph access → Chloe pumps out research → turnkey products

**Feasibility**: Technically feasible (7/10 complexity), business model is solid (8/10), risk is manageable (4/10).

**Next Steps**: Get St Paul report, architecture sketches, define standardized language, Monday follow-up.

**Chris's Role**: Build 10Seven's internal research infrastructure (not YWCA's platform).
