# Project Understanding - The Impactory

## What We Know

### The Project: "The Impactory"

A data platform with two integrated components:
1. **Data Warehouse** - Store and manage YWCA chapter data continuously
2. **Trauma Graph** - Interactive research visualization (already built by Chris)

---

## The Problem They're Solving

### Current Pain Points:
- 196 YWCA chapters spend **3 weeks** filling out a **61-page survey** annually
- Data goes **stale immediately** after submission
- Chapters **can't access their own data** afterward
- Can't generate **grant reports** when needed
- Can't see **what other chapters are doing**
- National HQ has to **keep surveying** to get updates
- Survey used to be **800 questions** (now reduced to 61 pages)

### The Core Problem:
No data infrastructure. Chapters are operating blind, can't leverage their own data, and headquarters is stuck in a constant survey cycle.

---

## The Solution

Transform that 61-page annual survey into a **living platform** where:

### For Chapters:
- Update data **continuously** (not once a year)
- System **auto-calculates** metrics and percentages
- **Generate grant-ready reports** on demand (PDF/Word)
- **Discover and learn** from other chapters' work
- Access **trauma graph** research data for their geography
- **Side-by-side comparison**: their data vs. 10Seven's research

### For National HQ (YWCA USA):
- See **aggregated view** of all 196 chapters
- **Network-wide statistics** and trends
- Stop surveying chapters to death
- **Monitor chapter health** and activity

### For 10Seven:
- **Research-quality data** for academic publications
- Correlation analysis across variables
- Support **peer-reviewed research** on collective impact
- Validate trauma graph findings with real program data

---

## Dual Purpose

This is **research infrastructure disguised as an operational tool**:

1. **Operational**: Help chapters write better grants and manage their data
2. **Research**: Support 10Seven's academic publications on collective impact

The platform must serve both without overwhelming users with academic complexity.

---

## The Data Model

Based on the 61-page YWCA Impact Survey structure:

### 1. Organizations/Chapters
- Basic info (name, location, addresses, fiscal year)
- Staffing (FT, PT, volunteers)
- Financials (revenue, funding sources, 990 uploads)
- Mission/Strategy
- Demographics Served (race, gender, income, age)
- Service Numbers (people served)

### 2. Programs (1-5 per chapter)
- Name & Objectives
- Impact Areas (Women & Girls, Health & Safety, Racial Justice, Economic Advancement)
- Violence Types Addressed (Racial, Gender-Based, Economic)
- Activities & Approaches
- Resources Leveraged
- Likelihood of Impact
- Evidence (policy changes, surveys, media, funding)

### 3. Impact Evaluations (by Violence Type)
- Societal Impacts (policy changes, narrative shifts)
- Beneficiary Impacts (access, confidence, belonging)
- Institutional Impacts (engagement, recognition, accountability)
- Evidence & Documentation

### 4. Organizational Efforts (non-program activities)
- Types (campaigns, research, advocacy, coalition-building)
- Intended Impacts
- Tools/Supports (have vs. wish to have)

---

## The Impact Framework (CRITICAL!)

10Seven has a sophisticated academic framework that underpins the platform:

### 4 Impact Measurement Pillars:
1. **Influence** - Uplift voices, push for policy
2. **Research** - Groundbreaking insights that change society
3. **Local Relevance** - Meet communities where they are
4. **Collective Disruption** - Bring together best insights nationally

### 3 Types of Impact:
1. **Societal Impacts** - Shifts in norms, policy changes, narrative shifts
2. **Beneficiary Impacts** - Individual changes (access, confidence, belonging)
3. **Institutional Impacts** - Systems change (institutions recognize & undo harm)

### 3 Violence Types (Each With Specific Interventions):
1. **Racial Violence** - 10+ intervention types (redlining, bias training, research, etc.)
2. **Gender-Based Violence** - 7+ intervention types (maternal health, childcare, pay gap, etc.)
3. **Economic Violence** - 10+ intervention types (guaranteed income, financial literacy, housing, etc.)

**Platform Implication**: Need controlled vocabularies, taxonomies, validation against framework.

**The Core Tension**: Make it simple for 2-person volunteer chapters while supporting PhD-level research.

---

## Users

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

### 3. National Headquarters (YWCA USA)
- Need: Aggregated view of all 196 chapters
- Network-wide reports
- Chapter health monitoring
- Use case: "Show me total impact across the network"

### 4. 10Seven Research Team
- Need: Research-quality data for publications
- Statistical analysis capabilities
- Correlation studies
- Use case: "Prove collective impact in peer-reviewed journals"

---

## Technical Architecture

### Multi-Tenancy:
- 196 separate chapter spaces
- National HQ can see all
- HIPAA compliance standard (even though not legally required)

### Two Components:
1. **Data Warehouse** (their data)
2. **Trauma Graph** (10Seven's research data - already built)

### Integration:
- Side-by-side view: chapter data + trauma graph
- Geographic matching (zip code/neighborhood)
- Never expose raw research data (only visualizations)

### Licensing:
- Separate licenses for warehouse vs. trauma graph
- Some chapters may only license one component
- Urban Institute example: licenses trauma graph only

---

## Key Features (Must-Haves)

### 1. Continuous Data Entry
- Not one-time survey
- Update monthly or as things happen
- Save drafts, come back later
- Auto-save everything

### 2. Auto-Calculations
- "168 people, 108 ate breakfast" → "64% ate breakfast"
- Year-over-year trends
- Percentage of demographics served
- Geographic aggregations

### 3. Report Generation
- Grant-ready reports (PDF/Word)
- Customizable or templated
- Include demographics, impact, evidence
- Example: "70% of our programs deal with SNAP-eligible women"

### 4. Cross-Chapter Discovery
- See what other chapters are doing
- Aggregated/anonymized data
- No raw client data sharing
- Example: "In Buffalo they're doing X, Y, Z"

### 5. File Management
- Upload 990s, budgets, strategic plans
- Version control
- Secure storage
- Evidence documentation

### 6. Split-Screen Trauma Graph
- Chapter data on one side
- 10Seven research maps on other side
- Geographic comparison
- Example: "Look at shame indicators by neighborhood"

### 7. Multi-Tenant Security
- 196 separate chapter spaces
- National HQ can see all
- HIPAA compliance
- Chapters own their data

---

## What We KNOW (From Analysis)

✅ **The problem**: 61-page survey, 3 weeks to complete, data goes stale
✅ **The users**: 196 chapters ranging from 2-person volunteers to 50-person orgs
✅ **The data model**: Every survey question = a database field
✅ **The framework**: 4 impact pillars, 3 impact types, 3 violence types
✅ **The dual purpose**: Operational tool for chapters + research infrastructure for 10Seven
✅ **The challenge**: Make it simple while supporting PhD-level research
✅ **Trauma graph**: Already built by Chris, integration needed
✅ **Survey structure**: Complete 61-page survey with all fields defined

---

## What We DON'T Know Yet (Need Thursday Meeting)

### Critical Unknowns:

❌ **MVP Scope**: What MUST be in v1 vs. what can wait for v2?
❌ **Cross-Chapter Visibility**: What can Buffalo see about Rochester's data?
❌ **Survey Data Import**: Import October 2024 data or start fresh?
❌ **Data Granularity**: Individual client records or aggregate numbers only?
❌ **Update Frequency**: How often do chapters update different data types?
❌ **Report Structures**: What sections go in grant reports?
❌ **Program Lifecycle**: Do programs have statuses, dates, budgets?
❌ **Trauma Graph Integration**: Where accessed, how used?
❌ **Permissions Model**: Who can see/edit what?
❌ **Timeline**: When do they need this delivered?

### Important Unknowns:

⚠️ Research vs. Operations balance
⚠️ Impact framework enforcement (rigid or flexible?)
⚠️ Statistical analysis capabilities needed
⚠️ Data quality validation requirements
⚠️ Built-in help/definitions
⚠️ Licensing architecture details
⚠️ Integration with existing tools (Qualtrics, Max QDA, Tableau)
⚠️ Data governance and ownership specifics
⚠️ Support and maintenance model

---

## Success Metrics

Platform succeeds when:
- ✅ Survey takes **30 minutes/month** instead of **3 weeks/year**
- ✅ Chapters can generate grant reports in **under 5 minutes**
- ✅ Data is **always current** (not stale)
- ✅ Chapters **actually want to log in** (it helps them, not just HQ)
- ✅ **Cross-chapter learning** increases
- ✅ **Grant success rate** improves (better data = better proposals)
- ✅ 10Seven can **publish peer-reviewed research** using platform data

---

## Client Team

### 10Seven:
- **Chloe** (65% of call) - Likely lead researcher
- **Andrea** (15% of call) - Role unclear
- **Nina** (9% of call) - Role unclear

### YWCA:
- Not yet directly involved in conversations
- 196 chapters will be end users
- National HQ will use aggregated view

---

## Chris's Role

**Full-Service Product Agency**:
1. **Discovery & Strategy**: Help them understand their pain points better
2. **Product Design**: Design the UX/UI collaboratively with them
3. **Development**: Build and deliver the platform

**What Chris Already Built**:
- Trauma graph visualization tool
- Understanding of the geographic data/mapping component

**What Chris Needs to Do**:
- Understand remaining requirements (Thursday meeting)
- Design the data warehouse UX/UI
- Build the data warehouse platform
- Integrate with existing trauma graph
- Deliver complete solution

---

## Next Steps

### Before Thursday:
- Review all analysis documents
- Prepare questions from questions_for_clients.md
- Have notepad ready to sketch during call

### During Thursday:
- Ask deep questions to fill in the unknowns
- Get clarity on MVP scope
- Understand cross-chapter visibility rules
- Clarify survey data import strategy
- Define timeline and next deliverables

### After Thursday:
- Should be able to answer: "What am I building, for whom, and by when?"
- Create technical architecture proposal
- Define feature prioritization (MVP vs. v2)
- Provide realistic timeline estimate
- List any remaining unknowns/blockers

---

## Files in Repository

### Design Collaboration Strategy:
1. **DESIGN_COLLABORATION_APPROACH.md** - UX design approach (for later)
2. **WIREFRAME_CONCEPTS.md** - UX options (for later)

### Project Context:
3. **project_analysis_and_context.md** - Full project breakdown from call transcript
4. **survey_analysis_and_data_model.md** - Deep dive on 61-page survey
5. **impact_framework_analysis.md** - Theoretical framework and research infrastructure
6. **questions_for_clients.md** - Comprehensive questions for Thursday

### Gap Analysis:
7. **REAL_GAPS_requirements_only.md** - 10 genuine requirements questions
8. **UPDATED_GAP_ANALYSIS.md** - 5 critical gaps
9. **GAP_ANALYSIS_critical_unknowns.md** - Original 20 gaps

### Reference:
10. **QUICK_REFERENCE.md** - Quick prep for Thursday
11. **PROJECT_UNDERSTANDING.md** - This file! Current understanding summary

---

## Bottom Line

**We understand the WHAT and the WHY very well.**

**We need Thursday to clarify the HOW and the WHEN.**

Then Chris can design and build with confidence.
