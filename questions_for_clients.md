# Questions for Thursday Meeting - YWCA Data Platform

## ⚡ YOUR ROLE: Design Partner + Developer

**CRITICAL REFRAME**: They don't have a design in mind. They hired you to:
1. Help them **figure out** what the UX/UI should look like
2. Build it

**This means Thursday is a collaborative design session, not requirements gathering.**

You're not there to ask "What do you want?"
You're there to say "Here are some options based on what I've learned - which feels right?"

---

## 🎯 Meeting Structure

### Part 1: Understand Context (30 min)
**Goal**: Learn constraints to inform your design decisions

### Part 2: Present Concepts (45 min)
**Goal**: Show wireframe options, get reactions, sketch together

### Part 3: Scope & Next Steps (30 min)
**Goal**: Agree on MVP approach and timeline

### Part 4: Clarify Critical Requirements (15 min)
**Goal**: Answer only the make-or-break questions

---

## Part 1: Context Questions (Inform Design Decisions)

These aren't "what do you want" questions - they're "help me understand your world" questions that inform design choices.

### Q1: Usage Pattern - Dashboard vs. Task-Based?
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

### Q2: The ONE Thing - What's the Killer Feature?
**"If this platform could only do ONE thing really well, what would make chapters actually use it?"**

Why this matters:
- Identifies the core value proposition to design around
- Everything else is secondary

What you're listening for:
- Is it grant reports? (Focus on report generation UX)
- Is it seeing what others do? (Focus on cross-chapter discovery)
- Is it easier data entry? (Focus on forms/wizards)
- Is it always-current data? (Focus on dashboard/updates)

---

### Q3: Current Workflow - Where's the Pain?
**"Show me how a chapter currently answers 'How many women did you serve last year?' Walk me through where they get that data."**

Why this matters:
- Reveals actual pain points (not hypothetical ones)
- Shows what the platform needs to improve

What you're listening for:
- Do they have the data or must they gather it?
- Is it in one place or scattered?
- Is gathering hard or entering hard?
- Do they trust their own data?

Ask to see:
- Their current tools/spreadsheets/files
- An example of digging through data for the survey

---

### Q4: User Sophistication - Simple or Powerful?
**"Show me your trauma graph. What do chapters love about it? What confuses them?"**

Why this matters:
- Tells you their capability level
- Informs complexity of data warehouse UX

What you're listening for:
- Do they rave about simplicity or power features?
- What causes confusion?
- What makes them feel successful?

Follow-up:
**"Do most chapters use Excel regularly? Are they comfortable with data entry?"**
- Yes → Can handle spreadsheet-like interface
- No → Need extremely simple forms

---

### Q5: Report Reality Check - What Do They Actually Need?
**"Show me a grant application you want chapters to fill out with this platform's data. Let's look at it together."**

Why this matters:
- Shows what report generation must actually produce
- Reveals what data is really important

What you're listening for:
- What sections are in grant applications?
- What level of detail do funders want?
- Is it narrative or data-heavy?
- Can one report work for multiple funders?

Ask for:
- 2-3 example grant applications
- Example of "grant-ready report" they want to generate

---

### Q6: Cross-Chapter Learning - What's the Real Use Case?
**"Tell me about a time when a chapter wished they could see what another chapter was doing."**

Why this matters:
- Reveals actual cross-chapter learning patterns
- Informs whether design should be search, browse, or feed

What you're listening for:
- Do they know which chapter to look for? (→ Search)
- Are they exploring by category? (→ Browse)
- Do they want inspiration/updates? (→ Feed)
- Are chapters collaborative or competitive?

---

### Q7: Team Dynamics - Solo or Collaborative?
**"When a chapter generates a grant report, is this something they do alone or with their team?"**

Why this matters:
- Solo → Simple "click to generate"
- Team → Need collaboration, comments, review workflow

What you're listening for:
- Who enters data? (one person? multiple?)
- Who generates reports? (same person?)
- Is there review/approval?

---

### Q8: Device Context - Desktop or Mobile?
**"Are chapter directors at their desk when they use this, or on the go?"**

Why this matters:
- Desktop → Can use complex layouts, multiple panels
- Mobile → Must be touch-friendly, single column

What you're listening for:
- Primary device for data entry
- Primary device for viewing reports
- Need to work offline?

---

## Part 2: Present Design Concepts (Get Reactions)

**YOU LEAD THIS SECTION.** Show them wireframes, get gut reactions.

### Show Option A: Simple Form-Based Wizard
"I sketched a simple step-by-step approach for adding programs. What do you think?"

[Show wireframe from WIREFRAME_CONCEPTS.md - Option A]

**Ask:**
- "Does this feel too simple? Too much clicking?"
- "Would chapters feel like this is just another survey?"
- "What's good about this? What's concerning?"

---

### Show Option B: Dashboard with Inline Editing
"Or we could do a power-user dashboard where you edit data right in tables. What do you think?"

[Show wireframe from WIREFRAME_CONCEPTS.md - Option B]

**Ask:**
- "Would this be overwhelming for smaller chapters?"
- "Do your chapters use tools like this?"
- "What's appealing about this? What's scary?"

---

### Show Option C: Hybrid Dashboard + Wizard
"Or a hybrid - dashboard for overview, wizard for adding new things. What do you think?"

[Show wireframe from WIREFRAME_CONCEPTS.md - Option C]

**Ask:**
- "Which of these three feels closest to what would work for your chapters?"
- "If you could combine features from different options, what would you keep?"

---

### Show Cross-Chapter Discovery Options
"For discovering what other chapters are doing, I see three approaches..."

[Show search vs. browse vs. feed concepts]

**Ask:**
- "Which matches how chapters would actually use this?"
- "Buffalo wants to learn about childcare programs - show me how they'd find Rochester's program using this design"

---

### Show Report Generation Options
"For grant reports, I see two approaches..."

[Show template picker vs. report builder]

**Ask:**
- "Would chapters want one-click reports or ability to customize?"
- "How important is it that reports look professional vs. just having the data?"

---

### Information Architecture - How Do They Think?
"Is a chapter's mental model 'I have programs' or 'I am an organization that runs programs'?"

[Show program-centric vs. organization-centric navigation]

**Ask:**
- "Which structure makes more sense for how chapters think about their work?"
- "When they say 'I need to update my data,' what are they thinking of updating?"

---

### Sketch Together
**"Let's sketch the dashboard together. What should chapters see when they first log in?"**

[Have paper/tablet ready to sketch in real-time]

- What's most important to show?
- What actions should be front and center?
- What can be hidden until needed?

---

## Part 3: Validate Assumptions

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

### Assumption 5: Research Framework Should Be Invisible
**"The impact framework is sophisticated. Should we hide it behind simple language, or do chapters need to see it?"**

If hide → Use plain language, framework in background
If show → Teach the framework, make it central

---

## Part 4: Critical Requirements (Only What's Make-or-Break)

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

### Requirement 4: Update Frequency Expectations
**"Realistically, how often will chapters update their data?"**

Why this matters: Informs notification/reminder strategy

- Real-time as things happen?
- Monthly during a "data day"?
- Quarterly for reports?
- Annually (defeats the purpose)?

---

### Requirement 5: MVP Scope
**"Based on what we've discussed, here's what I think makes sense for v1..."**

[Present your MVP recommendation based on reactions]

**Components:**
- ✅ Chapter dashboard with key metrics
- ✅ Add/edit programs (wizard approach)
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

**"Does this feel like the right scope for v1?"**

---

## Part 5: Close & Next Steps

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

> "I've spent time with the survey and call notes. I have some concepts to show you based on what I've learned about your chapters and their needs. My goal today is to figure out together what feels right for your users. I'll show you a few options, and I want your honest reactions - what feels right, what feels wrong. Then we can sketch together and get to something that works. Sound good?"

**This sets the tone: Collaborative design, not requirements handoff.**

---

## The Key Questions (If You Only Ask 5 Things)

1. **"What's the ONE thing that would make chapters actually use this?"** (Identifies killer feature)

2. **"Walk me through a chapter director's typical week. When would they open this?"** (Informs dashboard vs. task-based design)

3. **"Show me how chapters currently find the data they need."** (Reveals pain points)

4. **"Which of these UX approaches feels closest to what would work?"** (Gets reaction to wireframes)

5. **"Can we test a prototype with 2-3 chapter directors before building?"** (Validates design with users)

---

## Bottom Line

**You're not there to extract requirements.**
**You're there to collaborate on design.**

- Come with concepts ✅
- Get reactions ✅
- Sketch together ✅
- Leave with direction ✅

Then build with confidence. 🚀
