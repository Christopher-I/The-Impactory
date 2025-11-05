# Quick Reference - YWCA Data Platform Project

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

## ⭐ The 5 MUST-ANSWER Questions for Thursday

**UPDATED - Chris already built trauma graph, budget not a concern. Focus on these:**

### The Critical Five:

### 1. Survey Replacement Strategy
**"Is the platform meant to completely replace this annual survey, or transform it into continuous data entry?"**
- If replace: Do some questions still need to be asked annually?
- If transform: Which survey questions become ongoing data entry vs. one-time setup?
- What happens to the survey workflow after the platform launches?

### 2. Data Import from Existing Survey
**"You have October 2024 survey data. Should we import this as baseline data for chapters?"**
- Do chapters need to see their historical survey responses?
- Is this data editable or locked as historical reference?
- Does this become the "starting point" for their platform data?

### 3. Update Frequency by Data Type
**"How often should chapters update different types of data?"**
- **Organization info** (address, staff count, locations): Annually? As changes occur?
- **Demographics served**: Monthly? Quarterly? Annually?
- **Financial data**: After fiscal year? Monthly? When 990 filed?
- **Programs**: Added immediately when launched? Updated how often?
- **Impact evaluations**: Continuous assessment? Quarterly? Annually?
- **Service numbers** (people served): Real-time? Monthly? Annually?

### 4. MVP Scope Definition
**"What MUST be in version 1 for this to be useful to chapters?"**
- Data warehouse only, or must include trauma graph?
- Which entities: Organizations + Programs only? Or all entities?
- Which reports: Grant reports only? Or all report types?
- Can we launch with basic features and add advanced analytics later?
- What's the absolute minimum for YWCA to say "yes, this is useful"?

### 5. Cross-Chapter Data Visibility
**"What can chapters see about other chapters' data?"**
- Can Buffalo see Rochester's program names? Descriptions? Impact data?
- Only aggregated/anonymized data? ("20 chapters in NY do childcare programs")
- Can they see individual chapter identities or just aggregate numbers?
- What's public within the network vs. private to each chapter?
- Does this change if chapters opt-in to sharing?

### Important (But Not Blockers) (6-10):

### 6. Research vs. Operations Balance
**"I see this is research infrastructure with an impact measurement framework. What's the balance between research needs and operational needs?"**
- Primary purpose: 10Seven's research or chapters' operations?
- Should chapters even see the impact framework or should we abstract it?

### 7. Impact Framework Enforcement
**"How rigidly should the platform enforce the impact framework categories?"**
- Must all programs fit into the 3 violence types?
- Can chapters add their own categories or must use controlled vocabulary?
- How flexible should the system be as the framework evolves?

### 8. Statistical Analysis Capabilities
**"You plan correlation analysis. What statistical capabilities need to be in the platform?"**
- Basic (percentages, averages) or advanced (correlations, regressions)?
- Export to Qualtrics/SPSS/R for analysis?
- Generate correlation tables in platform?

### 9. Data Quality for Research
**"What validation is needed to ensure research-quality data?"**
- Required fields for research vs. optional for operations?
- Coherence checks (evidence type matches impact type)?
- Review/approval before data used in publications?

### 10. Built-In Definitions and Help
**"The survey toolkit has a glossary. Should these definitions be built into the platform?"**
- Tooltip/help text on every field?
- Searchable glossary within platform?
- Contextual help explaining the framework?

---

## Other Important Questions

11. **Report customization**: Fixed templates or customizable by chapters?

12. **Licensing architecture**: How does licensing affect what users see and can do?

13. **Audit trail**: Do you need to track who entered what data and when for accountability?

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

## What to Show/Ask Thursday

### Show:
- Quick database schema sketch
- Mockup of chapter dashboard
- Mockup of "Add Program" form
- Mockup of grant report output

### Ask:
- Walk through real user scenarios (not hypothetical)
- Show me their current tools (Max QDA, Qualtrics, Tableau)
- Show me example reports they wish they could generate
- Show me what chapters currently struggle with

### Clarify:
- What's MVP vs. future
- What's the timeline
- How does licensing work
- What's the relationship between data warehouse and trauma graph

---

## Red Flags to Watch

⚠️ **"Everything is must-have"** → Push back, prioritize ruthlessly
⚠️ **Vague on user workflows** → Keep asking for specific examples
⚠️ **No YWCA users involved** → Who validated these requirements?
⚠️ **Unrealistic timeline** → This is a significant platform, not a weekend project
⚠️ **Unclear trauma graph integration** → This is technically complex, need clarity

---

## Your Advantage

✅ You've seen the 61-page survey (they said they'd send it - you already have it!)
✅ You understand the pain point (3-week survey marathon)
✅ You can speak their language ("data intranet", "synthesizer", "warehouse")
✅ You know the data model (every survey question is a field)
✅ You understand the users (volunteers to data scientists)

**Go into Thursday with confidence. You know more than you think!**

---

## Quick Prep Checklist

Before Thursday:
- [ ] Review the survey again, note any confusing questions
- [ ] Sketch a quick database schema
- [ ] Look up Max QDA, Qualtrics, Tableau if unfamiliar
- [ ] Prepare 3-5 specific questions based on survey
- [ ] Have notepad ready to sketch screens during call
- [ ] Be ready to push back on scope ("What's absolutely essential for v1?")

During Thursday:
- [ ] Ask for walkthroughs, not descriptions
- [ ] Draw everything (screens, data flows, architecture)
- [ ] Use their language back to them
- [ ] Request real examples, not hypotheticals
- [ ] Summarize what you heard and confirm understanding
- [ ] End with clear next steps and deliverables

After Thursday:
- [ ] Send summary of what you heard
- [ ] Provide technical architecture proposal
- [ ] Give timeline estimate for MVP
- [ ] List any remaining unknowns/blockers

---

## Files You Have

1. **project_analysis_and_context.md** - Full project breakdown from call transcript
2. **questions_for_clients.md** - Detailed questions organized by priority (now includes research questions!)
3. **survey_analysis_and_data_model.md** - Deep dive on the 61-page survey with exact data model
4. **impact_framework_analysis.md** - The theoretical framework and research infrastructure insights
5. **GAP_ANALYSIS_critical_unknowns.md** - ⚠️ **READ THIS!** 20 critical gaps from call re-analysis
6. **QUICK_REFERENCE.md** - This file! Quick prep for Thursday (updated with research insights)

## The Complete Picture

You now understand:
- ✅ **The problem**: 61-page survey, 3 weeks to complete, data goes stale
- ✅ **The users**: 196 chapters ranging from 2-person volunteers to 50-person orgs
- ✅ **The data model**: Every survey question = a database field
- ✅ **The framework**: 4 impact pillars, 3 impact types, 3 violence types
- ✅ **The dual purpose**: Operational tool for chapters + research infrastructure for 10Seven
- ✅ **The challenge**: Make it simple while supporting PhD-level research

You're ready. 🚀
