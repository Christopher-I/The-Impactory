# Quick Reference - YWCA Data Platform Project

## ⚡ YOUR ROLE: Product Designer + Developer

**CRITICAL INSIGHT**: They don't know what the platform should look/feel like yet. They hired you to:
1. **Help them figure out the UX/UI** (design collaboration)
2. **Build it** (development)

**This changes everything:**
- Thursday is NOT "tell me your requirements"
- Thursday IS "let's figure out together what makes sense"
- You lead with concepts, they react
- Collaborative design, not requirements extraction

**See**: `DESIGN_COLLABORATION_APPROACH.md` and `WIREFRAME_CONCEPTS.md` for full strategy

---

## The Bottom Line

**What you're building:** Research infrastructure disguised as a simple data platform. Transform a 61-page survey into continuous data collection that serves both operational needs (grant writing) AND research needs (peer-reviewed publications).

**Why they need it:**
- 196 YWCA chapters have zero data infrastructure
- Headquarters surveys them constantly (used to be 800 questions!)
- Chapters spend weeks digging through files to answer questions
- Data goes stale immediately after survey
- Can't generate reports for grants when needed
- Can't see what other chapters are doing
- **10Seven needs research-quality data to publish academic research on collective impact**

**What makes it hard:**
- Users range from 2-person volunteer operations to sophisticated data teams
- Must be "as simple as logging into company intranet"
- Must handle complex data (demographics, programs, impacts, evidence)
- Must serve 196 separate chapters + national headquarters
- Must integrate with 10Seven's trauma graph research tool
- **Must support academic research (correlations, statistical analysis) while being easy to use**
- **Must maintain PhD-level impact framework without overwhelming users**

---

## Two Products in One

### 1. Data Warehouse (Their Data)
- Store chapter data continuously (not once-a-year survey)
- Auto-calculate metrics (percentages, trends, aggregations)
- Generate grant-ready reports on demand
- Allow cross-chapter discovery and learning
- Give national HQ aggregated view

### 2. Trauma Graph (10Seven's Research Data)
- Interactive maps showing financial trauma, domestic violence, etc. by geography
- Side-by-side comparison: chapter's data vs. 10Seven's research
- Never exposes raw research data (only visualizations/percentages)
- Separate license from data warehouse
- HIPAA-compliant data handling

---

## 🔬 The Impact Framework (CRITICAL!)

**NEW INSIGHT:** This isn't just data storage - it's **research infrastructure**. 10Seven has a sophisticated academic framework:

### 4 Impact Measurement Pillars (Data Architecture Foundation):
1. **Influence** - Uplift voices, push for policy
2. **Research** - Groundbreaking insights that change society
3. **Local Relevance** - Meet communities where they are
4. **Collective Disruption** - Bring together best insights nationally

### 3 Types of Impact (What They Measure):
1. **Societal Impacts** - Shifts in norms, policy changes, narrative shifts
2. **Beneficiary Impacts** - Individual changes (access, confidence, belonging)
3. **Institutional Impacts** - Systems change (institutions recognize & undo harm)

### 3 Violence Types (Each With Specific Interventions):
1. **Racial Violence** - 10+ intervention types (redlining, bias training, research, etc.)
2. **Gender-Based Violence** - 7+ intervention types (maternal health, childcare, pay gap, etc.)
3. **Economic Violence** - 10+ intervention types (guaranteed income, financial literacy, housing, etc.)

**Platform Implication:** Need controlled vocabularies, taxonomies, validation against framework, statistical analysis capabilities.

**The Core Tension:** Make it simple for volunteers while supporting PhD-level research.

---

## Core Data Model (From the Survey)

```
ORGANIZATION/CHAPTER
├── Basic Info (name, location, fiscal year)
├── Staffing (FT, PT, volunteers)
├── Financials (revenue, funding sources, 990 uploads)
├── Mission/Strategy
├── Demographics Served (race, gender, income, age)
└── Service Numbers (people served)

PROGRAMS (1-5 per chapter)
├── Name & Objectives
├── Impact Areas (Women & Girls, Health & Safety, Racial Justice)
├── Violence Types (Racial, Gender-Based, Economic)
├── Activities & Approaches
├── Resources Leveraged
├── Likelihood of Impact
└── Evidence (policy changes, surveys, media, funding)

IMPACT EVALUATIONS (by Violence Type)
├── Societal Impacts (policy changes, narrative shifts)
├── Beneficiary Impacts (access, confidence, belonging)
├── Institutional Impacts (engagement, recognition, accountability)
└── Evidence & Documentation

ORGANIZATIONAL EFFORTS (non-program activities)
├── Types (campaigns, research, advocacy, coalition-building)
├── Intended Impacts
└── Tools/Supports (have vs. wish to have)
```

---

## User Types

### 1. Basic Chapter Users (Most Common)
- Small staff (2-10 people)
- Limited tech sophistication
- Need: Simple data entry, one-click reports
- Use case: "I need a grant report by Friday"

### 2. Sophisticated Chapter Users
- Larger staff (20-50 people)
- May have data person
- Need: Advanced analytics, custom reports
- Use case: "Show me correlations between our program and outcomes"

### 3. National Headquarters
- Need: Aggregated view of all 196 chapters
- Network-wide reports
- Chapter health monitoring
- Use case: "Show me total impact across the network"

---

## Key Features (Must-Haves)

1. **Continuous Data Entry**
   - Not one-time survey
   - Update monthly or as things happen
   - Save drafts, come back later

2. **Auto-Calculations**
   - "168 people, 108 ate breakfast" → "64% ate breakfast"
   - Year-over-year trends
   - Percentage of demographics served

3. **Report Generation**
   - Grant-ready reports (PDF/Word)
   - Customizable or templated
   - Include demographics, impact, evidence

4. **Cross-Chapter Discovery**
   - See what other chapters are doing
   - Aggregated/anonymized data
   - No raw client data sharing

5. **File Management**
   - Upload 990s, budgets, strategic plans
   - Version control
   - Secure storage

6. **Split-Screen Trauma Graph**
   - Chapter data on one side
   - 10Seven research maps on other side
   - Geographic comparison

7. **Multi-Tenant Security**
   - 196 separate chapter spaces
   - National HQ can see all
   - HIPAA compliance

---

## Reports Needed

### For Chapters (Grant Writing):
- **Demographics Report**: Who we serve
- **Impact Summary**: What we achieved
- **Program Overview**: What we do
- **Evidence Report**: Proof of impact

### For National HQ:
- **Network Aggregation**: Total across all chapters
- **Geographic Coverage**: Map of where YWCA operates
- **Impact Areas**: Breakdown by violence type
- **Chapter Health**: Revenue, staffing, capacity

### For Cross-Learning:
- **Similar Chapters**: Find chapters doing similar work
- **Best Practices**: What successful programs look like
- **Resource Gaps**: What most chapters wish they had

---

## ⭐ Key Questions for Thursday (Design Collaboration)

**NEW APPROACH**: These aren't requirements questions - they're design constraint questions to inform your UX proposals.

### Part 1: Understand User Context (Inform Design Decisions)

### 1. Usage Pattern
**"Walk me through a typical chapter director's week. When would they open this platform?"**
→ Determines if design should be dashboard (daily check-in) or task-based (monthly data entry)

### 2. The ONE Thing
**"What's the ONE thing that, if this platform did it well, would make chapters actually use it?"**
→ Identifies the killer feature to design around

### 3. Current Workflow
**"Show me how a chapter currently answers 'How many women did you serve?' - where do they get that data?"**
→ Reveals pain points and design opportunities

### 4. User Sophistication
**"Show me your current tools. Do chapters use Excel regularly? Are they comfortable with data entry?"**
→ Determines complexity level (simple forms vs. power features)

### 5. Report Reality Check
**"Show me a grant application you want to fill out with this platform's data"**
→ Shows what report generation actually needs to produce

---

## Part 2: Present Design Concepts (Get Reactions)

**Bring to Thursday**: Wireframes showing 2-3 UX approaches

### Show Option A: Simple Form-Based
"What if adding a program was a step-by-step wizard like this?"
→ Get reaction: Too simple? Too much clicking? Just right?

### Show Option B: Dashboard with Inline Editing
"Or what if it was more like a spreadsheet with dashboard cards?"
→ Get reaction: Too complex? Overwhelming? Powerful?

### Show Option C: Hybrid Approach
"Or a dashboard that guides you but doesn't constrain you?"
→ Get reaction: Best of both? Too busy?

**Key question**: "Which feels closest to what your chapters would use?"

---

## Part 3: Validate Assumptions

### Cross-Chapter Learning
**Show search vs. browse vs. feed concepts**
"If Buffalo wants inspiration from Rochester, which of these feels right?"

### Report Generation
**Show template picker vs. report builder concepts**
"Would chapters want one-click reports or ability to customize?"

### Information Architecture
**Show organization-centric vs. program-centric concepts**
"Do chapters think in terms of 'our organization' or 'our programs'?"

---

## Part 4: Clarify Requirements (But Only the Critical Ones)

### Data Granularity
**"When you say 'we served 168 women,' is that just a number or 168 individual records?"**
**"What validation is needed to ensure research-quality data?"**
- Required fields for research vs. optional for operations?
- Coherence checks (evidence type matches impact type)?
- Review/approval before data used in publications?

### Cross-Chapter Visibility
**"If Buffalo wants to learn from Rochester's childcare program, what exactly should they see?"**
→ Informs permissions model and network discovery UX

### Survey Data Import
**"Should we import the October 2024 survey data as baseline, or start fresh?"**
→ Affects data migration plan

---

## What to Bring Thursday

### 1. Wireframe Sketches (See WIREFRAME_CONCEPTS.md)
- Chapter dashboard (2-3 variations)
- Add program flow (wizard vs. form)
- Report generation (template picker vs. builder)
- Cross-chapter discovery (search vs. browse)

**Keep them rough** - pen and paper is fine. You want reactions, not approvals.

### 2. Your Understanding
- Data model from survey (you have this)
- Impact framework (you understand this)
- Trauma graph integration (you built it)

### 3. Design Principles to Propose
- Simple by default, powerful when needed
- Progress over perfection (autosave, drafts)
- Context-aware help (tooltips, examples)
- Mobile-friendly but desktop-first

---

## Success Metrics

Platform succeeds when:
- ✅ Survey takes 30 minutes/month instead of 3 weeks/year
- ✅ Chapters can generate grant reports in under 5 minutes
- ✅ Data is always current (not stale)
- ✅ Chapters actually want to log in (it helps them, not just HQ)
- ✅ Cross-chapter learning increases
- ✅ Grant success rate improves (better data = better proposals)

---

## Thursday Meeting Structure

### Part 1: Context (30 min)
- Understand usage patterns and frequency
- See current tools/workflows (ask them to show, not tell)
- Identify the ONE killer feature
- Walk through real user scenarios

### Part 2: React to Concepts (45 min)
- Show 2-3 UX approach wireframes
- Get reactions (what feels right/wrong?)
- Sketch screens together
- Validate information architecture

### Part 3: Scope & Next Steps (30 min)
- Based on reactions, propose MVP
- Agree on timeline
- Set expectations for next deliverable (mockups? prototype?)
- Schedule follow-up

### Part 4: Close (15 min)
- Clarify any critical requirements (data granularity, visibility rules)
- Confirm understanding
- Next steps and deliverables

---

## Red Flags to Watch

⚠️ **"We want it to look like [complex enterprise software]"** → Push for simplicity first
⚠️ **"Every field is important!"** → Force prioritization
⚠️ **They can't articulate the primary use case** → Need to talk to real chapter users
⚠️ **Vague on user workflows** → Keep asking for specific examples
⚠️ **No reactions to your wireframes** → They might not understand - simplify more

---

## Your Advantage

✅ You've analyzed the 61-page survey (complete data model)
✅ You understand the pain point (3-week survey marathon)
✅ You built the trauma graph (know the integration)
✅ You understand the framework (research infrastructure)
✅ You have design concepts ready (not starting from scratch)

**Your role: Design partner + developer. Go lead the conversation!**

---

## Quick Prep Checklist

**Before Thursday:**
- [ ] Sketch 2-3 wireframe concepts (dashboard, add program, reports)
- [ ] Review DESIGN_COLLABORATION_APPROACH.md
- [ ] Review WIREFRAME_CONCEPTS.md for options
- [ ] Prepare design principles to propose
- [ ] Have paper/tablet ready to sketch during call

**During Thursday:**
- [ ] LEAD with concepts, not questions
- [ ] Show options, get reactions
- [ ] Sketch together in real-time
- [ ] Use their language back to them
- [ ] Ask "show me" not "tell me"
- [ ] End with: "Based on this, here's what I'll create next"

**After Thursday:**
- [ ] Send summary of what you heard and decisions made
- [ ] Create detailed wireframes based on direction from meeting
- [ ] Build interactive prototype (Figma/similar)
- [ ] Provide technical architecture proposal and timeline
- [ ] Schedule follow-up to review mockups
- [ ] Identify YWCA chapter users to test with

---

## Files You Have

### Design Collaboration Strategy (⭐ READ THESE!)
1. **DESIGN_COLLABORATION_APPROACH.md** - Your role as design partner, not just builder
2. **WIREFRAME_CONCEPTS.md** - UX options to present Thursday
3. **REAL_GAPS_requirements_only.md** - Genuine requirements questions (not project management)

### Project Context
4. **project_analysis_and_context.md** - Full project breakdown from call transcript
5. **survey_analysis_and_data_model.md** - Deep dive on 61-page survey with exact data model
6. **impact_framework_analysis.md** - Theoretical framework and research infrastructure
7. **questions_for_clients.md** - Detailed questions (older version, see newer docs above)

### Reference
8. **QUICK_REFERENCE.md** - This file! Updated for design collaboration approach
9. **UPDATED_GAP_ANALYSIS.md** - Gap analysis (superseded by REAL_GAPS)
10. **GAP_ANALYSIS_critical_unknowns.md** - Original 20 gaps (superseded)

## The Complete Picture

You now understand:
- ✅ **The problem**: 61-page survey, 3 weeks to complete, data goes stale
- ✅ **The users**: 196 chapters ranging from 2-person volunteers to 50-person orgs
- ✅ **The data model**: Every survey question = a database field
- ✅ **The framework**: 4 impact pillars, 3 impact types, 3 violence types
- ✅ **The dual purpose**: Operational tool for chapters + research infrastructure for 10Seven
- ✅ **YOUR ROLE**: Design partner + developer (they need you to help figure out the UX)

---

## Bottom Line for Thursday

**You're not there to take requirements.**
**You're there to collaborate on design.**

Come with:
- ✅ Wireframe concepts
- ✅ Design principles
- ✅ Understanding of the problem

Leave with:
- ✅ Direction on UX approach
- ✅ Validation of assumptions
- ✅ Clear next steps

Then: Build with confidence. 🚀
