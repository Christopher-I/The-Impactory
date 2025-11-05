# Questions for Thursday Meeting - YWCA Data Platform

## ⚡ YOUR ROLE: Full-Service Product Agency

**You're the complete package**:
1. **Discovery & Strategy**: Help them understand their pain points better
2. **Product Design**: Design the UX/UI collaboratively with them
3. **Development**: Build and deliver the platform

**This means Thursday is a comprehensive discovery + design session where you:**
- Ask deep questions to understand requirements
- Show concepts to guide the design direction
- Walk through workflows together
- Validate assumptions and constraints

You're not just extracting requirements OR just showing designs - you're doing both as their trusted partner.

---

## 🎯 Meeting Structure (2 hours)

### Part 1: Understanding Context & Pain Points (30 min)
- Learn about current workflows and frustrations
- Understand users and their capabilities
- Identify the ONE killer feature

### Part 2: Design Collaboration (45 min)
- Present wireframe concepts for feedback
- Sketch screens together
- Validate information architecture

### Part 3: Requirements Deep Dive (30 min)
- Data model and workflows
- Technical architecture needs
- Integration requirements

### Part 4: Scope & Next Steps (15 min)
- MVP definition
- Timeline and deliverables
- Schedule follow-up

---

# PART 1: CONTEXT & PAIN POINTS

## A. Understanding Current State

### Q1: Usage Pattern - When Do They Actually Use This?
**"Walk me through a typical chapter director's week. When would they open this platform?"**

Why this matters:
- Daily check-in → Design dashboard with key metrics
- Monthly data entry → Design task-based (forms/wizards)
- Only when writing grants → Design report generator + minimal data entry

What you're listening for:
- Frequency of use
- Context of use (rushed? relaxed? collaborative?)
- Competing priorities

---

### Q2: Current Workflow Pain Points
**"Show me how a chapter currently answers 'How many women did you serve last year?' Walk me through where they get that data."**

Why this matters:
- Reveals actual pain points (not hypothetical ones)
- Shows what the platform needs to improve

What you're listening for:
- Do they have the data or must they gather it?
- Is it in one place or scattered?
- Is gathering hard or entering hard?
- Do they trust their own data?

**Ask to see:**
- Their current tools/spreadsheets/files
- An example of digging through data for the survey
- Their frustration points

---

### Q3: The ONE Thing - What's the Killer Feature?
**"If this platform could only do ONE thing really well, what would make chapters actually use it and love it?"**

Why this matters:
- Identifies the core value proposition to design around
- Everything else is secondary

What you're listening for:
- Is it grant reports? (Focus on report generation UX)
- Is it seeing what others do? (Focus on cross-chapter discovery)
- Is it easier data entry? (Focus on forms/wizards)
- Is it always-current data? (Focus on dashboard/updates)

---

### Q4: User Sophistication Level
**"Show me your trauma graph. What do chapters love about it? What confuses them?"**

Why this matters:
- Tells you their capability level
- Informs complexity of data warehouse UX

What you're listening for:
- Do they rave about simplicity or power features?
- What causes confusion?
- What makes them feel successful?

**Follow-up:**
**"Do most chapters use Excel regularly? Are they comfortable with data entry?"**
- Yes → Can handle spreadsheet-like interface
- No → Need extremely simple forms

---

### Q5: Team Dynamics
**"When a chapter generates a grant report, is this something they do alone or with their team?"**

Why this matters:
- Solo → Simple "click to generate"
- Team → Need collaboration, comments, review workflow

What you're listening for:
- Who enters data? (one person? multiple?)
- Who generates reports? (same person?)
- Is there review/approval?

---

### Q6: Device Context
**"Are chapter directors at their desk when they use this, or on the go?"**

Why this matters:
- Desktop → Can use complex layouts, multiple panels
- Mobile → Must be touch-friendly, single column

What you're listening for:
- Primary device for data entry
- Primary device for viewing reports
- Need to work offline?

---

## B. User Workflow Walkthroughs

**REQUEST THESE! Have them walk you through step-by-step:**

### Walkthrough 1: Chapter First-Time User
**"Can you walk me through what happens when a chapter director logs in for the first time?"**

- What does the dashboard look like?
- What options do they see?
- What's their first action?
- What can they see immediately vs. what needs setup?

---

### Walkthrough 2: Adding a New Program
**"A chapter just launched a new domestic violence housing program. Walk me through how they add it to the platform."**

Based on the survey, they need to enter:
- Program name
- Objectives/purpose
- Languages delivered in
- Impact areas (Women & Girls Empowerment, Health & Safety, Racial Justice)
- Type of violence addressed (Racial, Gender-Based, Economic)
- Resources leveraged
- Activities (specific to violence type)
- How it addresses violence
- Evidence of impact

**Questions:**
- Do they enter all this at once or progressively?
- Can they save a draft and come back?
- How do they update program info as it evolves?
- What fields are required vs. optional?

---

### Walkthrough 3: Grant Writing Use Case
**"Take me through a real scenario: A chapter needs to write a grant application by Friday. How does this platform help them?"**

- What reports do they generate?
- What specific data points do they need?
- What format does the output need to be? (PDF? Excel? Both?)
- Can they customize reports or are they templated?
- Do they edit the report after generating it?

**Ask for:**
- 2-3 example grant applications
- Example of "grant-ready report" they want to generate

---

### Walkthrough 4: Trauma Graph Integration
**"Walk me through a real example: A chapter wants to understand financial trauma in their area and compare it to their client data."**

- Where do they click to access the trauma graph?
- How do they select their geographic area?
- What does the split-screen view actually show? (Can you sketch this?)
- What data from their side appears on the left/right?
- What trauma graph data appears on the other side?
- Can they export/save this comparison?
- What actions can they take based on what they see?

---

### Walkthrough 5: Cross-Chapter Discovery
**"Show me how a chapter in Buffalo would discover what a chapter in Rochester is doing."**

- Where do they navigate to see other chapters?
- What information can they see about other chapters? What can't they see?
- Can they filter/search? By what criteria?
- What happens if they want to "adopt" or learn from another chapter's program?

---

### Walkthrough 6: National HQ View
**"How does the national headquarters use this differently than a local chapter?"**

- What aggregated data do they see?
- Can they drill down into individual chapters?
- How do they generate reports for funders?
- Can they edit chapter data or only view?

---

### Walkthrough 7: Survey Replacement Scenario
**"Walk me through how the platform replaces the annual survey. What's different?"**

OLD WAY (Survey):
- Chapter receives survey link
- Spends 3 weeks filling it out
- Never sees data again

NEW WAY (Platform):
- Chapter does... what exactly?
- How often do they log in?
- What triggers them to update data?
- How does HQ get the data they used to get from surveys?

---

# PART 2: DESIGN COLLABORATION

## Show Wireframe Concepts & Get Reactions

**YOU LEAD THIS SECTION.** Show them wireframes, get gut reactions.

### Show Option A: Simple Form-Based Wizard
**"I sketched a simple step-by-step approach for adding programs. What do you think?"**

[Show wireframe from WIREFRAME_CONCEPTS.md - Option A]

**Ask:**
- "Does this feel too simple? Too much clicking?"
- "Would chapters feel like this is just another survey?"
- "What's good about this? What's concerning?"

---

### Show Option B: Dashboard with Inline Editing
**"Or we could do a power-user dashboard where you edit data right in tables. What do you think?"**

[Show wireframe from WIREFRAME_CONCEPTS.md - Option B]

**Ask:**
- "Would this be overwhelming for smaller chapters?"
- "Do your chapters use tools like this?"
- "What's appealing about this? What's scary?"

---

### Show Option C: Hybrid Dashboard + Wizard
**"Or a hybrid - dashboard for overview, wizard for adding new things. What do you think?"**

[Show wireframe from WIREFRAME_CONCEPTS.md - Option C]

**Ask:**
- "Which of these three feels closest to what would work for your chapters?"
- "If you could combine features from different options, what would you keep?"

---

### Cross-Chapter Discovery UX
**"For discovering what other chapters are doing, I see three approaches..."**

[Show search vs. browse vs. feed concepts]

**Ask:**
- "Which matches how chapters would actually use this?"
- "Buffalo wants to learn about childcare programs - show me how they'd find Rochester's program using this design"

---

### Report Generation UX
**"For grant reports, I see two approaches..."**

[Show template picker vs. report builder]

**Ask:**
- "Would chapters want one-click reports or ability to customize?"
- "How important is it that reports look professional vs. just having the data?"

---

### Information Architecture
**"Is a chapter's mental model 'I have programs' or 'I am an organization that runs programs'?"**

[Show program-centric vs. organization-centric navigation]

**Ask:**
- "Which structure makes more sense for how chapters think about their work?"
- "When they say 'I need to update my data,' what are they thinking of updating?"

---

### Sketch Together
**"Let's sketch the main dashboard together. What should chapters see when they first log in?"**

[Have paper/tablet ready to sketch in real-time]

- What's most important to show?
- What actions should be front and center?
- What can be hidden until needed?

---

## Validate Design Assumptions

Based on your analysis, you think these things are true. Validate them:

### Assumption 1: Simple > Powerful
**"My sense is most chapters would prefer simple and clear over powerful and flexible. True?"**

If yes → Lean toward Option A (forms) or C (hybrid)
If no → Consider Option B (dashboard)

---

### Assumption 2: Program is the Core Entity
**"It seems like everything revolves around Programs - is that right? Or is the Organization the center?"**

If programs → Design program-centric IA
If organization → Design org-centric IA

---

### Assumption 3: Monthly Update Cadence
**"I'm guessing chapters will update data monthly, not daily. Is that realistic?"**

If monthly → Design for "come back periodically" not "live dashboard"
If daily → Design for persistent presence

---

### Assumption 4: Grant Reports are the Killer Feature
**"My sense is report generation is why chapters will love this. Is that the #1 value prop?"**

If yes → Make reports EXTREMELY easy, everything else secondary
If no → What IS the #1 value prop?

---

### Assumption 5: Research Framework Should Be Abstracted
**"The impact framework is sophisticated. Should we hide it behind simple language, or do chapters need to see it?"**

If hide → Use plain language, framework in background
If show → Teach the framework, make it central

---

# PART 3: REQUIREMENTS DEEP DIVE

## A. Critical Requirements (Make-or-Break)

### Requirement 1: Data Granularity
**"When a chapter says 'we served 168 women,' is that just a number they type in, or are there 168 individual client records?"**

Why this matters: Individual records = massive privacy/security implications

**Likely answer**: Just aggregate numbers (simpler, no HIPAA concerns)

---

### Requirement 2: Cross-Chapter Visibility
**"Can Buffalo see Rochester's actual program details, or just aggregate data like '20 NY chapters do childcare'?"**

Why this matters: Determines permissions model complexity

**Show them the spectrum:**
1. Full transparency (everything public to all chapters)
2. Chapter-level summary (can see names/descriptions, not detailed data)
3. Aggregated only (can see trends, not individual chapters)
4. Opt-in sharing (chapters choose what to share)

**Which feels right?**

---

### Requirement 3: Survey Data Import
**"Should we import the October 2024 survey data as each chapter's starting point?"**

Why this matters: Affects data migration plan

Options:
- Import as baseline (chapters start with existing data)
- Start fresh (clean slate, chapters re-enter)
- Import as read-only history (reference only)

---

### Requirement 4: Survey Replacement Strategy
**"Is the platform meant to completely replace this annual survey, or transform it into continuous data entry?"**

- If replace: Do some questions still need to be asked annually?
- If transform: Which survey questions become ongoing data entry vs. one-time setup?
- What happens to the survey workflow after the platform launches?

---

### Requirement 5: Update Frequency by Data Type
**"How often should chapters update different types of data?"**

- **Organization info** (address, staff count, locations): Annually? As changes occur?
- **Demographics served**: Monthly? Quarterly? Annually?
- **Financial data**: After fiscal year? Monthly? When 990 filed?
- **Programs**: Added immediately when launched? Updated how often?
- **Impact evaluations**: Continuous assessment? Quarterly? Annually?
- **Service numbers** (people served): Real-time? Monthly? Annually?

---

## B. Data Questions

### Data Input

1. **Survey transformation:**
   **"I've reviewed the 61-page survey. Is the goal to transform this survey into the platform's data model?"**
   - Should every survey question become a field in the platform?
   - Or are some questions only for annual surveys, not continuous tracking?

2. **Conditional logic from survey:**
   - The survey has lots of "Display if..." logic (e.g., file upload if selected)
   - Should the platform replicate this conditional logic?
   - Or is the platform more flexible since data entry isn't one-time?

3. **File management:**
   - Survey allows uploading 990s, budgets, strategic plans, impact docs
   - Should platform have version control? (e.g., upload 2023 990, then 2024 990)
   - Should files be tagged/categorized?
   - Who can access uploaded files? (just the chapter, or network-wide?)

---

### Data Output

4. **What specific reports do they need?**
   - Can you show me examples of reports they wish they had?
   - What does a "compelling grant narrative" report look like?
   - What formats? (PDF, Excel, Word, presentations?)

5. **What automatic calculations are most important?**
   - You mentioned percentages - what else?
   - Averages? Trends over time? Comparisons?
   - Geographic aggregations?

---

### Trauma Graph Data

6. **What exactly is in the trauma graph dataset?**
   - What metrics/dimensions? (financial trauma, domestic violence severity - what else?)
   - What geographic levels? (state, county, city, neighborhood, zip code?)
   - How often is this data updated?
   - Where does this data come from? (10Seven's research - but what's the source?)

7. **How does trauma graph data map to chapter data?**
   - By geography only?
   - By demographic characteristics?
   - By program type?

---

## C. Research Infrastructure Questions

**Based on the "About the Impact Survey" document, this is research infrastructure, not just data storage:**

### Research vs. Operations Balance
**"I see this is research infrastructure with an impact measurement framework. What's the balance between research needs and operational needs?"**

- Is the primary purpose to support 10Seven's research and publications?
- Or is it primarily to help chapters with operations (grant writing)?
- How do we balance these potentially competing needs?

---

### Impact Framework Enforcement
**"How rigidly should the platform enforce the impact framework categories?"**

- Must all programs fit into: Racial Violence, Gender-Based Violence, or Economic Violence?
- What if a chapter's program doesn't fit the framework?
- Can chapters add their own categories or must they use your controlled vocabulary?
- The document says impact areas "may need more specificity as we learn" - how flexible should the system be?

---

### Statistical Analysis Capabilities
**"You plan to do correlation analysis across many variables. What statistical capabilities need to be in the platform?"**

- Basic only (percentages, averages, year-over-year)?
- Advanced (correlations, regressions, multivariate analysis)?
- Or will you export to Qualtrics/SPSS/R for analysis?
- Do you need cross-tabulations? Filtering by multiple variables?
- Should the platform generate the correlation tables mentioned in your doc?

---

### Data Quality for Research
**"What validation is needed to ensure research-quality data?"**

- Which fields are required for research vs. optional for operations?
- Should there be coherence checks? (e.g., evidence type must match claimed impact type)
- Review/approval process before data is used in research publications?
- How do you handle data quality issues from less sophisticated chapters?

---

### Built-In Definitions and Help
**"The survey toolkit includes a glossary with precise definitions. Should these be built into the platform?"**

- Tooltip/help text on every field with official definitions?
- Searchable glossary within platform?
- Contextual help that explains the framework as users enter data?
- Links to examples of good data entry?

---

## D. Technical Architecture Questions

### Multi-Tenancy

8. **What data can chapters see across the system?**
   - Can Buffalo see Rochester's raw client data? (I assume NO)
   - Can they see aggregated/anonymized data?
   - What's public within the network vs. private to each chapter?

9. **What can national headquarters see vs. chapters?**
   - Full access to all chapter data?
   - Separate permission levels?
   - Can they edit chapter data or only view?

---

### Licensing & Access

10. **How does licensing affect features?**
    - If a chapter only licenses the data warehouse (not trauma graph), what features are hidden?
    - If someone only licenses trauma graph (like Urban Institute), what do they see?
    - Do individual chapters control their own license or does national HQ?

11. **User accounts: How does authentication work?**
    - Individual users or shared chapter accounts?
    - How many users per chapter?
    - Role types? (admin, viewer, data entry, etc.)

---

### Integration with Existing Tools

12. **Qualtrics integration: What's the priority here?**
    - Do you want to keep using Qualtrics for surveys?
    - Should survey data automatically flow into this platform?
    - API integration or manual export/import?

13. **What about Max QDA, Tableau, Atlas?**
    - Should this platform replace them entirely?
    - Or integrate with them?
    - What features from those tools do you want to replicate?

---

## E. Process & Workflow Questions

### Data Governance

14. **Who owns what data?**
    - Chapters own their data - what does that mean technically?
    - Can they delete their data?
    - Can they export everything and leave?
    - What happens if a chapter closes?

15. **Data quality: Who ensures accuracy?**
    - Is there data validation?
    - Who reviews/approves data entries?
    - What happens if national HQ sees bad data from a chapter?

---

### Support & Maintenance

16. **Who will support end users?**
    - 10Seven team?
    - National YWCA staff?
    - Each chapter self-supports?

17. **How tech-savvy are the actual users?**
    - Can you describe the least technical person who will use this?
    - What's their comfort level with technology?
    - What devices will they use? (Desktop, tablet, phone?)

---

# PART 4: SCOPE & NEXT STEPS

## A. MVP Definition & Prioritization

### MVP Scope
**"Based on what we've discussed, here's what I think makes sense for v1..."**

[Present your MVP recommendation based on their reactions]

**Recommended v1 Components:**
- ✅ Chapter dashboard with key metrics
- ✅ Add/edit programs (wizard or form approach based on feedback)
- ✅ One standard grant report template
- ✅ Basic cross-chapter browsing (by category)
- ✅ Trauma graph integration (side-by-side view)
- ✅ National HQ aggregated dashboard

**Defer to v2:**
- ⏸ Statistical analysis tools
- ⏸ Multiple report templates
- ⏸ Advanced permissions/privacy controls
- ⏸ Qualtrics integration
- ⏸ Data export to SPSS/R
- ⏸ Mobile apps (responsive web in v1)

**"Does this feel like the right scope for v1?"**

---

### Feature Prioritization
**"If you had to rank these features by importance, what's the order?"**

- Data entry/storage
- Automatic calculations/synthesis
- Report generation
- Cross-chapter discovery
- Trauma graph visualization
- Split-screen comparison
- Survey tools
- Mobile access

---

### Timeline & Phasing

18. **What's the minimum viable product for YWCA launch?**
    - What must be in version 1?
    - What can wait for version 2?
    - What's the timeline expectation?

19. **Which component is more urgent?**
    - Data warehouse or trauma graph?
    - Can we build/launch them separately?

---

## B. Success Criteria

### Measuring Success

20. **How will you know this platform is successful?**
    - Adoption rate by chapters?
    - Grants won?
    - Time saved?
    - Data quality improvement?

21. **What would cause this project to fail?**
    - Too complex?
    - Too slow?
    - Missing key features?
    - Poor adoption?

---

## C. Close & Next Steps

### Recap What You Heard
**"Let me summarize what I'm taking away..."**

1. UX approach: [Which option they preferred]
2. Killer feature: [What they said is most important]
3. User level: [Simple vs. powerful]
4. MVP scope: [What's in v1]
5. Critical requirements: [Data granularity, visibility rules, import strategy]

**"Does that match what you were thinking?"**

---

### What You'll Create Next
**"Based on today's conversation, here's what I'll create for our next meeting..."**

1. **Detailed wireframes** (full screens for main flows)
2. **Interactive prototype** (clickable mockups in Figma)
3. **Data model** (database schema based on survey)
4. **Technical architecture proposal** (stack, integration plan)
5. **Timeline estimate** (realistic delivery for v1)

**"I'll aim to have this ready in [1-2 weeks]. Does that work?"**

---

### User Testing Request
**"Can we test the prototype with 2-3 actual chapter directors before building?"**

Why this matters: Validate design with real users

**Ask for:**
- Contact info for 3 chapters (small, medium, large)
- 30-minute sessions to walk through prototype
- Permission to iterate based on feedback

---

### Schedule Follow-Up
**"Let's schedule a follow-up to review the mockups. What's your availability in [timeframe]?"**

---

# REFERENCE MATERIALS

## Key Artifacts to Request

**Please share these before or during the meeting:**

- ✅ YWCA impact survey (full version) - YOU HAVE THIS
- ✅ Previous technical proposal (if it exists)
- ✅ Sample data from chapters (anonymized)
- ✅ Example reports they want to generate
- ✅ Screenshots/demos of Max QDA, Tableau, Atlas showing what features they use
- ✅ Current trauma graph (you built it - reference it)
- ✅ Sketches/wireframes of what they envision (if any exist)
- ✅ List of all data fields/metrics they want to track

---

## Design Principles to Propose

If they ask "what's your approach?" or "how would you design this?", share these principles:

### 1. Simple by Default, Powerful When Needed
"Most chapters are 2-10 people, not data scientists. Let's start simple. We can always add power features for sophisticated users later."

**Example**: Start with basic forms, add bulk import for power users in v2

---

### 2. Progress Over Perfection
"Better to have incomplete data than no data. Let's autosave everything, allow drafts, and never make perfection the enemy of progress."

**Example**: Can save program with just name + objective, add details later

---

### 3. Reduce Duplication
"If we can auto-calculate it, we should. If they entered it once, we should remember it. Never make users type the same thing twice."

**Example**: Calculate percentages automatically, pre-fill similar programs

---

### 4. Context-Aware Help
"The impact framework is complex. Let's put help exactly where it's needed, with examples and definitions right in context."

**Example**: Tooltip on every field explaining framework terms

---

### 5. Mobile-Friendly (But Desktop-First)
"Most data entry happens at a desk, but chapters should be able to view reports and check data on their phone."

**Example**: Desktop for entry, responsive for viewing

---

## Red Flags to Watch For

### 🚩 "We want it to look like [complex enterprise software]"
**Response**: "Let's start simple. Those tools serve research teams, but your chapters are program directors. Different users, different needs."

### 🚩 "Every field is important!"
**Response**: "Help me prioritize. If a chapter only has 10 minutes, what's the absolute minimum they should enter?"

### 🚩 "It should work like Max QDA/Qualtrics/Tableau"
**Response**: "Those are analysis tools for PhD researchers. Let's design for the chapter directors, not the analysts."

### 🚩 They can't articulate the primary use case
**Response**: "We really need to talk to a chapter director. Can we set up a 30-minute call with Buffalo or Rochester?"

### 🚩 No reaction to your wireframes
**Response**: "I'm sensing these aren't landing. Let me try a different approach. What if..."

### 🚩 "Make it flexible so users can do anything"
**Response**: "Flexibility adds complexity. Let's solve the 80% use case beautifully first, then add flexibility in v2."

### 🚩 Vague requirements
**Response**: If they can't describe specific workflows, ask for real examples

### 🚩 Scope creep
**Response**: If everything is "must have," push back and prioritize

### 🚩 Unrealistic expectations
**Response**: If they expect this built in 2 weeks, manage expectations

### 🚩 Missing stakeholders
**Response**: If YWCA users aren't involved, that's a risk

---

## What to Bring to the Meeting

### 1. Wireframe Sketches
- [ ] Chapter dashboard (2-3 variations)
- [ ] Add program wizard flow
- [ ] Report generation interface
- [ ] Cross-chapter discovery view
- [ ] National HQ dashboard
- [ ] Mobile view

**Keep them ROUGH** - pen and paper is fine. You want reactions, not pixel-perfect approval.

### 2. Your Understanding (Show You've Done Homework)
- [ ] Reference the survey structure
- [ ] Reference the impact framework
- [ ] Show you understand their pain (3-week survey marathon)
- [ ] Demonstrate you built the trauma graph

### 3. Examples to Reference
- [ ] Screenshot of trauma graph (your work)
- [ ] Example grant application (if you can find one)
- [ ] Survey questions that map to platform features

### 4. Tools for Sketching Together
- [ ] Paper + markers (or digital tablet)
- [ ] Ready to draw in real-time
- [ ] Screen sharing set up if remote

---

## Opening Line for Thursday

**Start with confidence:**

> "I've spent time with the survey and call notes. I have some concepts to show you based on what I've learned about your chapters and their needs. My goal today is to understand your pain points deeply, show you some design directions, and figure out together what's right for your users. I'll ask questions, show you options, and we'll sketch together. By the end, we should have clarity on what we're building and how. Sound good?"

**This sets the tone: Collaborative partnership, not just requirements handoff or just design showcase.**

---

## Questions You Should Be Able to Answer After Thursday

By the end of the meeting, you should clearly understand:

1. ✅ **Who are the users** and what do they need to do?
2. ✅ **What data goes in** and what data comes out?
3. ✅ **How do the two components** (warehouse + trauma graph) work together?
4. ✅ **What does success look like** for a chapter using this?
5. ✅ **What's the MVP** vs. future enhancements?
6. ✅ **What are the technical constraints** (performance, security, compliance)?
7. ✅ **What's the UX approach** (simple forms, dashboard, or hybrid)?
8. ✅ **What's the timeline** and realistic delivery schedule?

---

## Your Goal for Thursday

**Walk away with enough clarity to create:**
1. Detailed wireframes and interactive prototype
2. Technical architecture proposal
3. Database schema and data model
4. Feature prioritization (MVP vs. v2)
5. Realistic timeline estimate
6. List of any remaining unknowns

**You should be able to answer: "What am I building, for whom, and what does it look like?"**

---

## Pro Tips

- **Lead with concepts, not just questions**: Show wireframes early
- **Draw everything**: Sketch screens, data flows, architecture diagrams during the call
- **Use their language back**: When they say "data intranet," use that term in your proposals
- **Show, don't tell**: Ask them to share their screen and show you their current tools
- **Real examples only**: Every time they describe a feature, ask "can you show me a real example?"
- **Repeat back**: After each section, summarize what you heard and confirm understanding
- **Take notes on pain points**: When they say "this frustrates us," write it down - that's a key requirement
- **Sketch together**: Don't just present - co-create with them in real-time
- **Balance listening and leading**: Ask deep questions AND propose solutions

---

## Bottom Line

**You're their full-service partner**: Discovery + Design + Development

**Thursday's approach:**
1. Understand their world deeply (ask questions)
2. Show them possibilities (present concepts)
3. Co-create the solution (sketch together)
4. Define the roadmap (scope and timeline)

Come prepared. Lead with confidence. Leave with clarity. 🚀
