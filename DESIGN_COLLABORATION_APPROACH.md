# Design Collaboration Approach for Thursday

## The Real Situation

**What I initially thought**: They have a design in mind, I need to extract requirements and build it.

**What's actually happening**: They know the PROBLEM (survey fatigue, need data platform) but **don't know what the solution looks like yet**. They want me to help design it, then build it.

**My role**: Product Designer + Developer

---

## How This Changes Thursday's Meeting

### OLD APPROACH ❌
- "Show me the screens you want"
- "Walk me through the UX you envision"
- "What should this look like?"
→ **Problem**: They don't know yet! That's why they hired me.

### NEW APPROACH ✅
- "Here are 3 ways we could approach this - which feels right?"
- "I sketched some concepts based on your survey - react to these"
- "Let's figure out together what makes sense for your users"
→ **Better**: Collaborative design, I'm leading with proposals

---

## What I Should Bring to Thursday

### 1. Understanding of Constraints (Ask Questions About)
- **User sophistication**: 2-person volunteer orgs vs. 50-person data teams
- **Usage frequency**: Daily? Monthly? Only when writing grants?
- **Technical comfort**: Can they handle complexity or need dead simple?
- **Primary use case**: What will they do 80% of the time?
- **Device context**: Desktop? Tablet? Phone?

### 2. UX Concept Options (Show Them Options)

Present 2-3 different approaches and let them react:

#### Option A: "Simple Form-Based"
**Best for**: Less sophisticated users, clarity over power
```
Chapter Dashboard
├── "Add New Program" button
├── List of their programs
└── "Generate Report" button

Add Program = Multi-step form
Update Data = Edit forms
Reports = Pick template, click generate
```
**Pros**: Familiar, can't get lost
**Cons**: More clicking, feels like data entry

#### Option B: "Spreadsheet-Like"
**Best for**: Power users, bulk data entry
```
Chapter Dashboard
├── Programs (table view)
│   ├── Inline editing
│   ├── Add row
│   └── Bulk import
└── Reports (sidebar)

Add Program = Add row to table
Update Data = Click cell, edit inline
Reports = Select data, export
```
**Pros**: Fast for bulk entry, familiar to Excel users
**Cons**: Can be overwhelming, easy to make mistakes

#### Option C: "Dashboard + Wizard Hybrid"
**Best for**: Mixed sophistication, balance power and simplicity
```
Chapter Dashboard
├── Key Metrics Cards (people served, programs active, etc.)
├── "Quick Actions" (Add Program wizard, Generate Report)
└── Data tables below (Programs, Impact, etc.)

Add Program = Guided wizard with progress bar
Update Data = Dashboard cards with "update" links
Reports = Report builder wizard
```
**Pros**: Clear for beginners, efficient for power users
**Cons**: More complex to build

### 3. Information Architecture Options

**Critical Question**: How do they mentally organize their data?

**Option 1: Organization-Centric**
```
Chapter (Buffalo)
├── Profile (address, staff, fiscal info)
├── Programs (all programs live here)
├── Impact (results across all programs)
└── Reports (generate from all data)
```

**Option 2: Program-Centric**
```
Chapter (Buffalo)
├── Program 1: Domestic Violence Housing
│   ├── Details
│   ├── Impact Evaluation
│   ├── Demographics Served
│   └── Evidence
├── Program 2: Financial Literacy
└── Chapter Profile (org-level data)
```

**Option 3: Activity-Centric**
```
Chapter (Buffalo)
├── Data Entry (forms for all data types)
├── My Impact (view all impact data)
├── Reports (generate from all data)
└── Learn (see other chapters)
```

Which mental model matches how they think about their work?

---

## Questions to Frame as Design Constraints

### Instead of: "What should the UI look like?"
### Ask: "Help me understand the constraints so I can design the right solution"

### User Context Questions:
1. **"Walk me through a typical chapter director's week. When would they open this platform?"**
   - Daily check-in?
   - Monthly data update?
   - Only when grant deadline looming?
   → This tells me: Dashboard needs vs. task-oriented design

2. **"Which is harder for chapters: gathering the data, or entering it into systems?"**
   - If gathering is hard → Focus on "save draft, come back later"
   - If entering is hard → Focus on "bulk import, templates, autofill"

3. **"When they generate a grant report, is this something they do alone or with their team?"**
   - Alone → Simple "click to generate"
   - With team → Need collaboration features, comments, review workflow

4. **"Show me how a chapter currently stores this data (if at all)"**
   - Excel? → Maybe spreadsheet-like interface
   - Nothing? → Need extreme simplicity
   - Salesforce? → They can handle complexity

### Cross-Chapter Learning Questions:
5. **"If Buffalo wants inspiration from Rochester, what are they hoping to find?"**
   - "I want to copy their program" → Need program templates, full details
   - "I want to see if anyone else does X" → Need search/browse by category
   - "I want to know what's working" → Need success metrics, evidence
   → This determines the "network view" UX

6. **"Are chapters competitive or collaborative?"**
   - Collaborative → Show chapter names, encourage direct contact
   - Competitive → Anonymize data, aggregate only
   - Mixed → Let chapters opt-in to sharing

### Report Generation Questions:
7. **"Show me a grant application you want to fill out with this platform's data"**
   - Look at actual form structure
   - See what sections they need
   → Design report templates to match real grant applications

8. **"Do you write one grant application and send to multiple funders, or custom for each?"**
   - One template → Need one flexible report
   - Custom each time → Need modular report builder
   → Determines report customization needs

---

## Proposed Thursday Agenda

### Part 1: Understand Usage Context (30 min)
**Goal**: Understand constraints to inform design decisions

- Walk through typical chapter user's workflow
- See examples of their current tools/processes
- Understand frequency and context of use
- Identify primary vs. secondary use cases

### Part 2: React to UX Concepts (45 min)
**Goal**: Get directional feedback on approach

- Show 2-3 UX approach options (form-based vs. dashboard vs. spreadsheet)
- Present information architecture options
- Sketch main screens together
- Identify what feels right vs. wrong

### Part 3: Prioritize & Scope (30 min)
**Goal**: Agree on MVP features and approach

- Based on their reactions, propose MVP scope
- Identify "must have day 1" vs. "can add later"
- Agree on timeline given chosen approach
- Set expectations for next deliverable (mockups? prototype?)

### Part 4: Next Steps (15 min)
- I'll create detailed mockups based on today's direction
- Schedule follow-up to review mockups
- Identify any users from YWCA we can talk to for validation

---

## What to Sketch Before Thursday

Create quick wireframes (hand-drawn or Figma/Excalidraw) for:

1. **Chapter Dashboard** (3 variations: simple, power user, hybrid)
2. **Add Program Flow** (form vs. wizard vs. inline)
3. **Report Generation** (template picker vs. builder)
4. **Cross-Chapter Discovery** (search vs. browse vs. feed)
5. **National HQ Dashboard** (aggregated view)

**Keep them rough** - you want reactions, not approval of final designs.

---

## Key Insights to Validate

From all the analysis, I think these are true but need to confirm:

### Hypothesis 1: Simple > Powerful
**Assumption**: Most chapters are 2-10 people, not sophisticated, need simple.
**Validate**: Show simple vs. complex options, see which they gravitate toward.

### Hypothesis 2: Program is the Core Entity
**Assumption**: Everything revolves around programs (not organization, not individuals).
**Validate**: Show program-centric vs. org-centric IA, see which makes sense.

### Hypothesis 3: Monthly Update Cadence
**Assumption**: They'll update data monthly, not daily.
**Validate**: Ask about usage frequency, design accordingly.

### Hypothesis 4: Grant Reports are the Killer Feature
**Assumption**: Report generation is why chapters will love this.
**Validate**: Confirm this is #1 value prop vs. other features.

### Hypothesis 5: Cross-Chapter Learning is Secondary
**Assumption**: Nice to have, but not why they'll use it daily.
**Validate**: Ask "If you could only have ONE feature, what would it be?"

---

## Design Principles to Propose

Based on everything I know, suggest these principles and see if they agree:

1. **Simple by Default, Powerful When Needed**
   - Start with minimal fields, progressive disclosure for advanced
   - "80% of users need 20% of features"

2. **Progress > Perfection**
   - Autosave everything
   - Draft mode always available
   - "Better to have incomplete data than no data"

3. **Reduce Duplication**
   - Auto-calculate everything possible
   - Pre-fill from previous entries
   - "Type it once, use it everywhere"

4. **Context-Aware Help**
   - Tooltips for framework terms
   - Examples for every field
   - "Never leave users guessing"

5. **Mobile-Friendly (But Desktop-First)**
   - Most data entry happens at desk
   - But should be viewable on phone
   - "Enter on desktop, review on mobile"

---

## Red Flags to Watch For

### 🚩 "We want it to look like [complex enterprise software]"
**Response**: "Let's start simple. We can always add complexity, but can't remove it once users learn it."

### 🚩 "Every field is important!"
**Response**: "Help me prioritize. If a chapter only has 10 minutes, what's the minimum they should enter?"

### 🚩 "Can we make it work like Max QDA/Qualtrics/Tableau?"
**Response**: "Those are research tools for PhD analysts. Your chapters are program directors. Different tools for different users."

### 🚩 They can't articulate the primary use case
**Response**: "Let's talk to a real chapter director. We need to understand their actual workflow."

---

## Deliverables After Thursday

Based on direction from meeting, you'll create:

1. **Wireframes** (next week)
   - Main screens based on chosen UX approach
   - 3-5 key user flows
   - Mobile and desktop views

2. **Information Architecture** (next week)
   - Sitemap
   - Navigation structure
   - Data model refinement

3. **Interactive Prototype** (following week)
   - Clickable mockups in Figma
   - Test with 2-3 YWCA chapter users
   - Iterate based on feedback

4. **Technical Architecture Proposal** (following week)
   - Stack recommendations
   - Database schema
   - Integration plan for trauma graph
   - Timeline estimate

**Then**: Build phase starts

---

## The Real Questions for Thursday

1. **"What's the ONE thing that, if this platform did it well, would make chapters actually use it?"**

2. **"Show me a chapter director's current process for answering 'How many women did you serve?' - walk me through where they find that data."**

3. **"If I showed this platform to a chapter director and they looked confused - what would that tell us we did wrong?"**

4. **"When chapters use your trauma graph, what do they love about it? What frustrates them?"**
   → Use this to inform data warehouse UX

5. **"Should this feel like a research tool or an operations tool?"**
   → Determines visual design, terminology, complexity level

---

## Confidence Heading Into Thursday

### You Have ✅
- Deep understanding of the problem
- Complete data model from survey
- Understanding of research framework
- Working trauma graph to reference

### You Need ✅
- Direction on UX approach (simple vs. powerful)
- Validation of primary use case (reports? data entry? learning?)
- Examples of current workflows
- Reactions to design concepts

### You'll Create After Thursday ✅
- Wireframes
- Prototype
- Technical architecture
- Timeline

---

## Bottom Line

**Thursday is NOT a requirements meeting.**
**Thursday IS a collaborative design workshop.**

You're not there to take notes on what they want.
You're there to propose options and figure out together what's right.

Come with concepts. Leave with direction. Build with confidence.

🚀
