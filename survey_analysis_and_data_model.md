# YWCA Impact Survey Analysis - Data Model Insights

## Critical Insight: The "Why" Behind This Platform

**The survey is 61 pages long and takes chapters 3 weeks to complete.**

This explains EVERYTHING about why they need this platform:
- Chapters spend weeks digging through files to answer questions
- Data gets "stale" after the survey is done
- Nothing is tracked continuously
- Headquarters has to survey them repeatedly to get updates
- **The platform's job: Make this survey obsolete by capturing this data continuously**

---

## Data Model Structure

Based on the survey, here's what the data warehouse needs to store:

### Entity 1: Organization/Chapter Profile

**Basic Information:**
- Local association name (dropdown of 194 chapters)
- Headquarters address
- Geographic service area (counties, cities, zip codes, neighborhoods)
- Multiple locations (yes/no, how many)
- Fiscal year start date

**Staffing:**
- Full-time workers (0-5, 6-10, 11-20, 21+)
- Part-time workers (same ranges)
- Volunteers (same ranges)

**Financial:**
- Annual revenue last fiscal year
- Annual revenue current fiscal year (projected)
- Primary funding source type
- File upload: 990 forms
- File upload: Projected budget

**Mission & Strategy:**
- Mission/vision statement (text)
- Strategic plan (yes/no)
- Strategic plan priorities (text or file upload)

**Demographics Served:**
- Race/ethnicity (multiple checkboxes):
  - White/Caucasian
  - African American/Black
  - Middle Eastern/North African/Arab/Arab American
  - American Indian/Alaska Native/Indigenous
  - Hispanic/Latinx/Latino/Chicanx/Chicana/Chicano
  - Pacific Islander/Native Hawaiian
  - Asian/Asian American

- Gender groups served:
  - Female
  - Male
  - Transgender/Non-binary/Gender non-conforming

- Income levels served (multiple select):
  - <$35k, $35-50k, $50-75k, $75-100k, $100-150k, $150-200k, $200-300k, $300k+
  - Predominant income levels (select up to 3)

- Age ranges served:
  - 0-13, 14-18, 19-29, 30-44, 45-59, 60-78, 78+

**Service Metrics:**
- Number of people served last fiscal year
- Number of people planning to serve this fiscal year
- Demographics changes in last 5 years (yes/no + explanation)

---

### Entity 2: Programs

**For each program (up to 5 per survey), they track:**

**Basic Info:**
- Program name
- Stated objectives/purpose (text)
- Languages delivered in (English, Spanish, French, Chinese, other)

**Impact Areas (multi-select):**
- Women & Girls Empowerment
- Health & Safety
- Racial Justice & Civil Rights

**Type of Violence Addressed (multi-select):**
- Racial violence
- Gender-based violence
- Economic violence

**Resources Leveraged (multi-select):**
- Funding
- Research/data collection instruments
- Media coverage
- Connections to other LAs/institutions
- Educational resources for beneficiaries
- Training for service providers
- Access to thought leaders/powerbrokers

**Likelihood of Achieving Impact:**
- 7-point scale: Highly likely → Highly unlikely → N/A

**Program Activities vary by violence type** (see below)

---

### Entity 3: Organizational Efforts (Non-Program Activities)

**Types of efforts (multi-select):**
- Public awareness campaigns
- Publish policy briefs
- Publish original research
- Consultative/advisory services to governments/institutions
- Fundraising initiatives
- Community outreach (events, workshops)
- Partnership/coalition building
- Voter education and registration

**Intended Impact (multi-select):**
- Shift communication about social problems
- Reduce/eliminate denial about social problems
- Change/adopt public policy
- Position as leader in solution development
- Increase access to basic needs for beneficiaries
- Increase sense of belonging/safety for beneficiaries
- Engage institutions in inequity
- Compel institutions to recognize their role in harm

**Likelihood of achieving impact:** (same 7-point scale)

**Tools/Supports:**
Matrix of: Have & utilize | Have but rarely utilize | Wish I had | Don't have | Not sure I need

- Lawyers/policy experts
- Research software
- CRM to track beneficiaries
- Grant writer
- Data analytics software
- Legal/compliance support
- Marketing/outreach technology
- Additional funding sources
- Internal collaboration platform
- Training and development

---

### Entity 4: Impact Evaluation (3 types, same structure for each)

**Structure repeats for:**
1. Racial Violence Programs
2. Gender-Based Violence Programs
3. Economic Violence Programs

#### For Each Violence Type:

**Program Activities (multi-select, varies by type)**

Examples for Racial Violence:
- Curriculum delivery to communities affected by racism
- Training for professionals
- Essential assistance distribution
- Skills/workforce development
- Navigation assistance for support services
- Implicit bias trainings
- Cultural competency trainings
- Refugee/immigrant assistance
- Voting rights programming

**How Programs Address This Violence (multi-select)**

Examples for Economic Violence:
- Implementing guaranteed income programs
- Expanding access to financial institutions
- Bank account setup support
- Asset-building expansion
- Financial education to undo financial trauma
- Environmental justice work

**Societal Impacts Achieved (multi-select):**
- Shift in local communication about social problem
- Reduction/elimination of social denial
- Policy/rule/regulation changed or adopted
- Organization positioned as leader
- None of the above
- Not applicable

**Beneficiary Impacts Achieved (multi-select):**
- Increased access to basic needs
- Increased confidence/skills
- Increased sense of belonging/safety
- None of the above
- Not applicable

**Institutional Impacts Achieved (multi-select):**
- Institutions exhibit more meaningful engagement
- Institutions recognize their role in harm
- Institutions assume responsibility and take steps to undo harm
- None of the above
- Not applicable

**Evidence of Impact (multi-select):**
- Policy adoption decree
- Pre/post-survey results
- Earned media coverage
- Peer-reviewed journal submission accepted
- Initial funding
- Funding renewal
- Copycat program
- Requests for advisory services/board appointments
- Increase in beneficiaries served
- Repeat participation by beneficiaries
- Testimonials/personal stories
- Prefer to describe

**File Uploads:**
- Documents, reports, materials demonstrating impact

---

### Entity 5: Aspirations (Future Plans)

**Future Programs/Efforts (select up to 3):**
- Train more institutions/policymakers
- Reach more people harmed by social problems
- Develop more public awareness campaigns
- Train more beneficiaries on skills/workforce
- Train more professionals
- Develop/deliver curriculum
- Provide essential assistance
- Assist with accessing support services
- Develop/distribute data and research
- Build coalitions/partnerships
- None of the above

**Future Impacts Hoped For (select up to 3):**
- Shift in local communication
- Reduction of social denial
- Policy change/adoption
- Position as leader
- Increase beneficiary access to needs
- Increase beneficiary confidence/skills
- Increase beneficiary belonging/safety
- More institutional engagement
- Institutional recognition of harm
- Institutional responsibility for undoing harm
- None of the above

**Plans:**
- Design a program
- Initiate organizational effort
- Both
- Neither

**Focus:**
- Specific social problem
- Specific community/group
- Both
- Not sure yet
- Not applicable

---

## Key Technical Observations

### 1. Conditional Logic
The survey has extensive conditional logic:
- "Display this question IF..." appears throughout
- Questions show/hide based on previous answers
- File upload fields appear when user selects "prefer to upload"
- Follow-up questions appear based on likelihood ratings

**Platform Implication:** Need flexible form builder with conditional logic

### 2. File Uploads
Chapters can upload:
- 990 tax forms
- Projected budgets
- Strategic plans
- Geographic service area lists
- Staff/volunteer information
- Impact documentation (reports, materials)

**Platform Implication:** Need robust file storage and management

### 3. Matrix Questions
Many questions use matrix format where rows are items and columns are options:
- Programs × Impact Areas
- Programs × Resources
- Programs × Likelihood ratings
- Tools × Have/Want/Use status

**Platform Implication:** Need good UI for complex multi-dimensional data entry

### 4. Multi-Select Questions
Most questions allow multiple selections, not single choice

**Platform Implication:** Many-to-many relationships in database

### 5. Open-Ended Text
Significant amount of qualitative data:
- Mission statements
- Program objectives
- Why/how questions
- Additional comments

**Platform Implication:** Need good text field handling and possible qualitative analysis tools

---

## What the Platform Replaces

### Current State (Survey-Based):
1. Chapter receives survey link (61 pages)
2. Spends 3 weeks finding documents, consulting colleagues
3. Fills out survey all at once
4. Submits
5. Data goes to Impact Department
6. Never sees it again until next survey
7. Can't access their own data
8. Can't see other chapters' data
9. Can't generate reports when needed

### Future State (Platform-Based):
1. Chapter logs in anytime
2. Updates data as things happen (continuous)
3. Uploads documents as they're created
4. Can see their own data dashboard anytime
5. Can generate reports instantly for grant applications
6. Can see aggregated data from other chapters
7. National HQ can see everything in real-time
8. No more 3-week survey marathon
9. Data is always current, not stale

---

## Data Warehouse Core Entities Summary

```
ORGANIZATION (Chapter)
├── Basic Info (name, address, locations, fiscal year)
├── Staffing (FT, PT, volunteers)
├── Financials (revenue, funding sources)
├── Mission/Strategy (statements, plans)
├── Demographics Served (race, gender, income, age)
└── Service Metrics (numbers served, changes)

PROGRAMS (1-to-many with Organization)
├── Basic Info (name, objectives, languages)
├── Impact Areas (W&G Empowerment, Health/Safety, Racial Justice)
├── Violence Types (Racial, Gender-Based, Economic)
├── Resources Leveraged
├── Activities (specific to violence type)
├── How They Address Violence
├── Likelihood of Achieving Impact
└── Evidence of Impact

IMPACT EVALUATIONS (by Violence Type, linked to Programs)
├── Societal Impacts
├── Beneficiary Impacts
├── Institutional Impacts
└── Evidence & Documentation

ORGANIZATIONAL EFFORTS (1-to-many with Organization)
├── Types of Efforts
├── Intended Impact
├── Likelihood of Achieving
└── Tools/Supports (have vs. wish)

ASPIRATIONS (1-to-one with Organization)
├── Future Programs/Efforts Planned
├── Future Impacts Hoped For
└── Focus Areas

FILES/DOCUMENTS (many-to-many with multiple entities)
├── 990 Forms
├── Budgets
├── Strategic Plans
├── Impact Documentation
└── Other Supporting Materials
```

---

## Reports That Need to Be Generated

Based on the survey questions, chapters need reports that answer:

### For Grant Writing:
1. **Demographics Report**
   - "Who we serve: 67% of our clients are women of color earning less than $35k/year in these zip codes..."

2. **Impact Summary Report**
   - "Our programs reached X people and achieved these outcomes..."
   - Evidence of impact (policy changes, funding secured, media coverage)

3. **Program Overview Report**
   - List of active programs
   - Objectives and outcomes for each
   - Resources leveraged

4. **Comparison Report** (Cross-Chapter)
   - "20 YWCA chapters in New York serve similar demographics..."
   - "70% of our programs deal with women who are SNAP eligible..."

### For National HQ:
5. **Network Aggregation Report**
   - Total people served across all chapters
   - Geographic coverage map
   - Program type distribution
   - Impact areas breakdown

6. **Chapter Health Report**
   - Revenue trends
   - Staffing levels
   - Service capacity
   - Impact likelihood scores

### For Chapters Themselves:
7. **Year-Over-Year Comparison**
   - How demographics have changed
   - Service growth/decline
   - New programs launched
   - Impact improvements

8. **Gap Analysis Report**
   - Tools we have vs. wish we had
   - Resources needed
   - Future aspirations vs. current capacity

---

## Auto-Calculations Needed

Based on survey data, platform should automatically calculate:

1. **Percentages**
   - "X% of clients are from Y demographic"
   - "X% of programs achieved likely/highly likely impact"
   - "X% of funding comes from grants vs. events"

2. **Trends**
   - Year-over-year growth in people served
   - Revenue changes
   - Demographic shifts

3. **Aggregations**
   - Total programs by impact area
   - Total beneficiaries across all programs
   - Geographic coverage (unique zip codes served)

4. **Comparisons**
   - Chapter performance vs. network average
   - Resource gaps (what most chapters wish they had)

5. **Scores/Ratings**
   - Overall impact likelihood score (average across programs)
   - Evidence strength (how many types of evidence they have)

---

## Questions This Survey Helps Answer

### For Chris's Thursday Meeting:

✅ **What data goes IN?**
- Everything in this 61-page survey
- Plus ongoing updates (new programs, beneficiaries served, funding received)
- Plus file uploads (990s, strategic plans, impact docs)

✅ **What data comes OUT?**
- Grant-ready reports with demographics, impact, and evidence
- Cross-chapter comparison insights
- Network-wide aggregations for national HQ
- Year-over-year trends

✅ **Who are the users?**
- **Chapter staff**: Entering data, generating reports for grants
- **National HQ**: Viewing aggregated data, monitoring chapter health
- **Data-sophisticated chapters**: Using advanced analytics
- **Basic chapters**: Just want simple dashboards and reports

✅ **What does "user-friendly" mean?**
- NOT a 61-page survey marathon
- Enter data as you go (monthly updates)
- Click a button, get a report
- Visual dashboards, not just numbers
- File uploads, not manual data entry

✅ **What's the core value?**
- **Continuous data tracking** instead of survey snapshots
- **Instant report generation** instead of 3-week data hunts
- **Cross-chapter insights** instead of isolation
- **Always-current data** instead of stale survey results

---

## Platform Features Implied by Survey

### Data Entry:
- Form builder with conditional logic
- Multi-select checkboxes
- Matrix/grid inputs
- File upload management
- Auto-save/draft functionality
- "Start and stop as you go" capability

### Data Storage:
- Structured data (demographics, metrics)
- Unstructured data (text fields, documents)
- Time-series data (track changes over years)
- Relational data (programs → impacts → evidence)
- File storage (documents, 990s, plans)

### Data Output:
- Report templates based on common grant questions
- Export formats (PDF, Word, Excel)
- Visualization (charts, graphs, maps)
- Comparison views (chapter vs. network average)
- Cross-chapter discovery/browsing

### User Management:
- Chapter-level access control
- National HQ elevated permissions
- Multiple users per chapter
- Role-based features (admin, data entry, viewer)

### Integration:
- Survey data import (Qualtrics)
- File system for uploads
- Possibly export to other analytics tools

---

## Next Steps for Chris

With this survey in hand, you can now:

1. **Map out the database schema** precisely
   - You know all the entities and fields
   - You know the relationships
   - You know the data types

2. **Design specific user flows**
   - Chapter adds a new program → fills out these specific fields
   - Chapter generates grant report → includes these sections
   - HQ views network data → sees these aggregations

3. **Create wireframes/mockups**
   - Show them a mockup of what "Program entry" looks like
   - Show them a mockup of a "Grant Report" output
   - Show them a dashboard view

4. **Estimate complexity accurately**
   - You can see the conditional logic requirements
   - You can see the file handling needs
   - You can see the reporting complexity

5. **Ask smarter questions Thursday**
   - "I see Q31 asks about impact areas. Is this how you categorize programs everywhere, or just for this survey?"
   - "Q25 asks about tools you 'have and utilize' vs 'wish I had'. Should the platform track this for inventory management?"
   - "The survey allows uploading strategic plans. Should the platform also allow linking programs to strategic plan goals?"

---

## Critical Questions to Ask Thursday

Now that you've seen the survey:

1. **Data continuity**: "Should chapters be able to see their historical survey responses in the platform, or is this a fresh start?"

2. **Survey elimination**: "Is the goal to completely replace this survey, or will some questions still need to be asked annually?"

3. **Real-time updates**: "How often should chapters update different types of data? (e.g., demographics quarterly, but program adds as they launch)"

4. **Report customization**: "Should chapters be able to customize reports, or are you providing fixed templates?"

5. **Audit trail**: "Do you need to track who entered what data and when for accountability?"

6. **Data validation**: "Should the platform enforce required fields, or allow partial/draft entries?"

7. **Survey migration**: "You have existing survey data from October 2024. Should we import this as baseline data?"

8. **Qualitative data**: "There's a lot of open-ended text in the survey. Do you need tools to analyze this (like Max QDA does)?"

---

## The "Aha!" Moment

**This survey IS the data model for the warehouse.**

Every question in this survey represents:
- A field in the database
- A section on a dashboard
- A data point in a report
- An input in the platform

The platform's job is to make filling out this survey an ongoing, continuous, painless process rather than a 3-week marathon once a year.

**The platform transforms:**
- 61-page survey → Intuitive dashboard with progressive disclosure
- 3-week burden → 30-minute monthly updates
- Stale annual data → Real-time living database
- No visibility → Rich insights and cross-chapter learning
- Grant writing panic → One-click report generation
