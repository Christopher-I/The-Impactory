# Project Understanding - The Impactory

## What We Know

### The Project: "The Impactory"

A data platform with two integrated components:
1. **Data Warehouse** - Store and manage YWCA chapter data continuously
2. **Trauma Graph** - Interactive research visualization (Chris has built a demo and understands its structure)

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
2. **Trauma Graph** (10Seven's research data - Chris has built a demo)

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
✅ **Trauma graph**: Demo built by Chris, understands structure, full implementation needed
✅ **Survey structure**: Complete 61-page survey with all fields defined

---

## NEW INSIGHTS (From Impact Briefing)

### Integration Challenge Validated ✅
**Chris's insight was their #1 finding**: "Impact areas that do not account for intersectionality allow the amazing work of our local associations to get lost."

**Evidence of Integration as Core Challenge**:
- **r = .88** correlation between Racial Violence and Gender-Based Violence
- **r = .853** correlation between Racial Violence and Economic Violence
- **r = .782** correlation between Economic Violence and Beneficiary Impact

**Real LA Quote**: "It is Black maternal health week this week, And I did include that under, I believe, sexual, racial and economic violence [in the survey] because I believe we address all of those issues."

**Platform Implication**: Edge cases are the norm, not the exception. System MUST support multiple violence type tagging.

---

### Program Categorization Strategy (NOW CLEAR) ✅

**Moving From**:
- ❌ Old: "Health & Safety," "Women's Empowerment," "Racial Justice" (rigid categories)

**Moving To**:
- ✅ New: Functional categories that can address multiple violence types

**6 Functional Program Categories**:
1. **Housing** (30+ programs, 20+ LAs) - Emergency, transitional, DV shelters, homeless services
2. **Domestic Violence & Sexual Assault** (35+ programs, 20+ LAs) - Shelters, case management, legal, counseling
3. **Adult Education & Well-Being** (60+ programs, 35+ LAs) - Job training, financial literacy, senior care, language services
4. **Youth Education & Well-Being** (80+ programs, 40+ LAs) - Childcare, early learning, after school, leadership development
5. **Community Education & Awareness** (10+ programs, 15+ LAs) - Outreach, events, community engagement
6. **Policy & Advocacy** (20+ programs, 15+ LAs) - Legislative advocacy, policy training, civic engagement

**Each program can address Racial, Gender-Based, and/or Economic violence simultaneously.**

**This is a tagging system, not a rigid hierarchy.**

---

### The Three Impact Levels (CRITICAL FRAMEWORK) ✅

**Beneficiary Level** (Direct impact on people served):
- Increase access to basic needs
- Increase confidence/skills
- Increase sense of belonging/safety
- **>80% of current programs** operate here

**Institutional Level** (Impact on institutions perpetuating inequity):
- Compel institutions to engage on social issues
- Get institutions to recognize their role in harm
- Get institutions to take steps to undo harm
- **<40% of current programs** operate here

**Societal Level** (Impact on policy, narrative, lasting change):
- Shift public communication about issues
- Reduce/eliminate social denial
- Change public policy
- Position YWCA as leader in solutions
- **<10% of current programs** operate here

**The Gap**: LAs are excellent at beneficiary level but want to move up to institutional/societal levels. This requires **data capability and research support**.

---

### Current Data Challenges (THEIR PAIN POINTS) ✅

**LA Quote**: "So I guess, honestly, more support with our systems and data would be huge from YWCA USA…Our systems are terrible."

**LA Quote**: "So for domestic violence and sexual assault, there is a state mandated program that you have to use for data entry...We do something else for our timekeeping...all of these things are like completely separate systems."

**What LAs Have**:
- Good at measuring **outputs** (how many people served, hotline calls, kids in programs)
- Multiple disconnected systems (DV tracking, timekeeping, case notes all separate)
- State-mandated systems for certain programs

**What LAs Struggle With**:
- Measuring **outcomes** (what actually changed for people)
- Tracking individual stories/progress without good systems
- Consistent data practices across LAs
- Translating data into policy advocacy

**What LAs Want**:
- "Data analytics" (though this means different things to different LAs)
- Tools to demonstrate impact beyond numbers
- Support and guidance on data collection/usage

---

### The "Best Kept Secret" Problem ✅

**Key Finding**: LAs are known for individual programs (e.g., "the childcare place") but not recognized as YWCA brand.

**LA Quote**: "we're the best kept secret in [community], and we're tired of being the best kept secret. Not understanding that means more work, because then you gotta document and prove it."

**Why This Matters for the Platform**:
- Reports must help LAs demonstrate impact beyond beneficiary level
- Need to support policy advocacy and institutional engagement
- Must position LAs as data-backed leaders in their communities

---

### Network Scale & Reach ✅

**Impact Numbers**:
- **1,445,489 beneficiaries** reached (unduplicated)
- **98%** women and girls
- **80%** children
- **>70%** people of color
- **>80%** low income (<$35K annually)
- **250+ unique programs** reported
- **167 LAs** responded to survey (out of 196)

---

### The 3% Who Are Succeeding at Policy Level ✅

**Key Finding**: Among the small 3% of LAs with policy change as a stated goal, **100% say they're achieving it**.

**What They Do**:
- Government counterparts go through Justice Equity and Belonging training
- Meet with bipartisan legislators to understand their priorities
- Align advocacy work with what legislators are actually working on
- Focus on police reform, probation reform, affordable housing, tenant rights
- Use YWCA's mission/data to inform policy conversations

**LA Quote**: "every year, our head of RSJ and advocacy, goes out and actually talks to a whole bunch of [bipartisan] legislators and says, 'What are you focused on this year?' [She] talks about how that ties into our mission and then comes back and goes…Here's our policy pillars, but based on what the legislators are actually going to do, here's what we're going to focus on this year…"

**Lesson**: Data-backed advocacy works. But most LAs don't have the capability.

---

### What's Missing/Aspirational ⚠️

Based on Nina's email: "some of it we don't have immediate access to, or it doesn't exist yet"

**Likely Missing**:
- Trauma graph (might only be concept/demo)
- Published research papers using YWCA data (aspirational)
- Formalized data-to-research pipeline (doesn't exist yet)
- Consistent cross-LA data (everyone uses different systems)

**Likely Available**:
- Impact Survey responses (they have this)
- Program categorization examples (shown in briefing)
- LA quotes/stories from qualitative interviews (shown in briefing)
- Impact framework (detailed in briefing)

---

### Updated Value Proposition ✅

**Not just** "easier data entry" or "grant reports."

**The platform must enable LAs to**:
1. Move from beneficiary-level to institutional/societal-level impact
2. Become data-backed policy advocates
3. Position themselves as community leaders (not "best kept secret")
4. Demonstrate outcomes, not just outputs

---

## What We DON'T Know Yet (Need Thursday Meeting)

### ANSWERED BY IMPACT BRIEFING ✅

✅ **Program Categorization**: Functional categories (Housing, DV/SA, Education, etc.) + violence type tagging
✅ **Impact Framework Enforcement**: Flexible tagging system, not rigid hierarchy
✅ **Edge Cases**: They're the norm (high correlations between violence types), system must support multiple tags
✅ **Real Value Prop**: Enable LAs to move from beneficiary to institutional/societal level impact
✅ **Data Challenges**: Multiple disconnected systems, good at outputs but struggle with outcomes
✅ **Network Scale**: 1.4M+ beneficiaries, 167 LAs, 250+ programs

### Critical Unknowns (PRIORITY FOR THURSDAY):

❌ **What Actually Exists**: Does trauma graph exist or just demo? Published research papers? Data pipelines?
❌ **How Data Flows**: From LA → through platform → to 10Seven research → to publications (show me current process)
❌ **Grant Examples**: Show me actual grant applications that need data
❌ **Research Examples**: Show me research papers using YWCA data (or drafts)
❌ **Data Granularity**: Individual client records or aggregate numbers only?
❌ **Cross-Chapter Visibility**: What can Buffalo see about Rochester's programs/data?
❌ **Survey Data Import**: Import October 2024 data as baseline or start fresh?
❌ **MVP Scope**: What MUST be in v1 for policy advocacy support vs. what can wait?
❌ **Timeline**: When do they need this delivered?

### Important Unknowns:

⚠️ **Update Frequency**: How often do LAs update different data types?
⚠️ **Report Structures**: What sections go in grant reports?
⚠️ **Program Lifecycle**: Do programs have statuses, dates, budgets?
⚠️ **Trauma Graph Integration**: Where accessed, how used in practice?
⚠️ **Permissions Model**: Who can see/edit what? Who can hide data?
⚠️ **Statistical Analysis**: What correlation/analysis capabilities needed?
⚠️ **Data Quality Validation**: Required fields for research vs. optional for operations?
⚠️ **Built-in Help**: What definitions/tooltips needed?
⚠️ **Integration with Existing Tools**: Qualtrics, Max QDA, Tableau - how connect?
⚠️ **Data Governance**: Ownership, usage rights, approval workflows?

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

**What Chris Has Built**:
- Demo of trauma graph visualization tool
- Understanding of the trauma graph structure and geographic data/mapping component

**What Chris Needs to Do**:
- Understand remaining requirements (Thursday meeting)
- Design the data warehouse UX/UI
- Build the data warehouse platform
- Build the full trauma graph (from demo to production)
- Integrate data warehouse with trauma graph
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
