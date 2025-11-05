# Questions for Thursday Meeting - YWCA Data Platform

## Your Approach

**You're here to understand their world, not spec a system.**

- Focus on "show me" not "tell me"
- Ask about current reality, not envisioned future
- Let technical details emerge from workflows
- Real examples only, no hypotheticals
- Take notes on pain points and frustrations

**Meeting Goal:** Walk away understanding what they do, how they do it, where it breaks, and what good looks like.

---

## Meeting Structure (2 hours)

### Part 1: Show Me How You Work Today (45 min)
Understand current state, tools, processes, pain points

### Part 2: Show Me the Artifacts (30 min)
See actual research, grants, trauma graph, data

### Part 3: Walk Through Integration Scenarios (30 min)
How YWCA data, 10Seven research, and Trauma Graph connect

### Part 4: Clarify Scope & Next Steps (15 min)
MVP, timeline, deliverables

---

# PART 1: Show Me How You Work Today

## Current State & Pain Points

### 1. Show Me Your Current Research Process
**"Can you show me a research paper you've published or are working on that uses YWCA network data?"**

**If they have one:**
- Walk through it together
- What data did you need from YWCA chapters?
- How did you get that data? (survey? manual collection?)
- What was hard to get?
- What took the most time?
- How did you aggregate across 196 chapters?
- How did you ensure data quality?

**If they don't have one yet:**
- "Walk me through a paper you plan to publish"
- What hypothesis are you testing?
- What data do you need?
- How would you get it today?

→ **Listen for:** Integration challenges, data quality issues, current workarounds

---

### 2. Show Me How YWCA Chapters Use Data Today
**"Walk me through how a chapter currently answers the question: 'How many women did we serve last year?'"**

- Where do they look for this data?
- Is it in one place or scattered across files?
- How long does it take to gather?
- How confident are they in the accuracy?
- What happens after they report it?

**Follow-up:** "Show me the current survey process from start to finish"
- Chapter receives survey link...
- Then what happens?
- How long does it really take?
- What's the most painful part?

→ **Listen for:** Where data lives now, what's hard to find, why it takes 3 weeks

---

### 3. Show Me How You Currently Categorize Programs
**"Walk me through how you categorize a chapter's program into your framework (Racial Violence, Gender-Based Violence, Economic Violence)"**

- Show me an example program and how you'd categorize it
- Can you show me one that was challenging to categorize?
- What did you do when a program addressed multiple violence types?
- What about programs that don't fit any category?

**Follow-up:** "How do chapters currently describe their programs?"
- Do they use your framework language or their own?
- How do you translate their language to your framework?

→ **Listen for:** Edge cases, flexibility needs, current workarounds for programs that don't fit

---

### 4. The Trauma Graph - Show Me What It Is
**"Can you show me the trauma graph? Let's look at it together."**

- What am I looking at?
- What geographic levels does it cover? (zip code? county? neighborhood?)
- What trauma indicators are shown? (financial trauma, domestic violence - what else?)
- How often is this data updated?
- Where does the underlying data come from?

**Follow-up:** "How does a chapter use this today?"
- Do they access it now?
- Have you shown it to any chapters?
- What was their reaction?
- What questions did they have?

→ **Listen for:** Geographic granularity, what data exists, how it's actually used

---

### 5. Current Tools & Frustrations
**"Show me the tools you use today for research and data analysis"**

- Max QDA - what do you use it for?
- Tableau - what do you visualize?
- Qualtrics - how does it fit in?
- Excel/SPSS/R - what analysis do you do?

**Follow-up:** "What frustrates you most about your current setup?"
- Where does data get stuck?
- What takes way longer than it should?
- What do you wish you could do but can't?

→ **Listen for:** What's working, what's broken, what they're trying to accomplish

---

# PART 2: Show Me the Artifacts

## Real Examples & Documents

### 6. Show Me Grant Applications
**"Can you show me a grant application a chapter has submitted, or one they're working on?"**

**If they have one:**
- What data did the chapter need for this grant?
- Where did they get it?
- What was missing or hard to get?
- How long did it take them to compile the data?
- What would have made this easier?

**If they don't have one:**
- "What does a typical grant application require?"
- What sections need data vs. narrative?
- What funders are they typically applying to?

→ **Listen for:** What "grant-ready report" actually means, what data is critical

---

### 7. Show Me Survey Responses
**"Can you show me actual survey responses from chapters (anonymized if needed)?"**

- How complete are the responses typically?
- What questions do chapters struggle with most?
- What data is highest quality vs. lowest?
- Do chapters provide narrative or just numbers?

→ **Listen for:** Data quality issues, what's easy vs. hard for chapters to answer

---

### 8. Show Me How You Currently Map Data
**"How do you currently connect YWCA chapter data to trauma graph data?"**

- Show me an example
- Chapter serves [geographic area], trauma graph has data at [level] - how do you match?
- What happens when a chapter serves multiple zip codes with different trauma indicators?
- Have you done this analysis before or is this aspirational?

→ **Listen for:** Actual integration patterns, geographic matching challenges

---

### 9. Show Me What "Compelling Narrative" Looks Like
**"You mentioned helping chapters 'build a compelling narrative to raise money' - can you show me an example?"**

- What does that narrative look like?
- What data supports it?
- What makes it compelling vs. just factual?
- Is it mostly narrative with some data, or mostly data with some narrative?

→ **Listen for:** Balance of story vs. statistics, what funders respond to

---

# PART 3: Walk Through Integration Scenarios

## End-to-End Workflows

### 10. Scenario: YWCA Data → 10Seven Research → Publication
**"Let's walk through a specific scenario: How does data from Buffalo chapter's housing program end up in your research on economic violence?"**

**Step by step:**
- Buffalo enters data about their housing program (where? how?)
- That data gets to 10Seven (how?)
- You aggregate it with 195 other chapters (how?)
- You analyze it (using what tools?)
- You correlate it with trauma graph data (how?)
- You publish findings (where? what does it say?)

→ **Listen for:** Every integration point, every transformation, every place data could get stuck

---

### 11. Scenario: Chapter Uses Platform for Grant
**"Walk me through: Chapter director needs to write a grant application by Friday. It's Monday morning."**

**Current state (without platform):**
- What do they do Monday?
- Where do they look for data?
- What takes the most time?
- Do they finish by Friday?

**Future state (with platform):**
- What changes?
- What do they do instead?
- How much time does it save?
- What do they still have to do manually?

→ **Listen for:** Time saved, what platform must provide, what remains manual

---

### 12. Scenario: Cross-Chapter Learning
**"Scenario: Buffalo wants to learn about childcare programs in New York. Walk me through how they'd do this with the platform."**

- What exactly are they looking for? (ideas? best practices? data?)
- What can they see about Rochester's childcare program?
- Can they see specific outcomes/data or just that Rochester has a childcare program?
- Can they contact Rochester directly?
- Is data anonymized or attributed?

→ **Listen for:** What "cross-chapter discovery" actually means, privacy boundaries

---

### 13. Scenario: Edge Case Program
**"Give me a real example of a program that didn't fit neatly into your framework"**

- What was the program?
- Why didn't it fit?
- What did you do?
- How did you categorize it in the end?
- Did this cause problems for analysis?

**Follow-up:** "Can a program address all 3 violence types?"
- If yes, how do you handle that?
- If no, how do you decide which one?

→ **Listen for:** How rigid the framework really is, how they handle edge cases

---

# PART 4: Clarify Scope & Next Steps

## MVP Definition & Priorities

### 14. What Must Be in Version 1?
**"If you had to pick the THREE most important things this platform must do on day 1, what would they be?"**

Force prioritization. Listen for what they say first.

**Follow-up:** "Can the data warehouse launch without trauma graph integration, or must they launch together?"

→ **Listen for:** What's truly essential vs. nice-to-have

---

### 15. Survey Replacement Strategy
**"After this platform launches, does the annual survey go away completely, or does it continue in some form?"**

- What happens to the survey workflow?
- Are there questions that can only be asked annually?
- Do chapters fill out the survey once to seed the platform?

**Follow-up:** "Should we import the October 2024 survey data as baseline, or start fresh?"

→ **Listen for:** Whether this replaces or supplements survey, data migration expectations

---

### 16. Timeline & Expectations
**"When do you need this? What's the timeline you've committed to YWCA or funders?"**

- What's the launch date?
- Are there milestones before full launch?
- Can we launch to a pilot group first?

→ **Listen for:** Real deadline vs. aspirational timeline

---

### 17. Success Metrics
**"How will you know this platform is successful 6 months after launch?"**

- Adoption rate by chapters?
- Grants won?
- Time saved?
- Research published?
- Data quality improved?

→ **Listen for:** What success actually looks like to them

---

## Follow-Up & Next Steps

### 18. User Testing
**"Can we test an early version with 2-3 actual chapter directors before building the full thing?"**

- Who would be good chapters to include?
- Can you introduce me to them?
- Small, medium, and large chapter?

→ **Get:** Contact info, permission to talk to real users

---

### 19. Materials & Access
**"What materials can you share with me after this meeting?"**

**Request:**
- October 2024 survey responses (anonymized)
- Example research papers using YWCA data
- Grant applications from chapters
- Access to trauma graph (if it's built)
- Any previous technical proposals or specs

→ **Get:** Artifacts to study, baseline understanding

---

### 20. Confirm Understanding & Next Steps
**"Let me summarize what I'm hearing and you tell me if I got it right..."**

Recap:
1. The core problem you're solving
2. How the three pieces integrate (YWCA data + 10Seven research + Trauma Graph)
3. What must be in v1
4. What success looks like

**Then:** "Based on this conversation, here's what I'll create next..."
- Detailed technical architecture proposal
- Data model design
- Wireframes/prototype for key workflows
- Timeline estimate

"I'll have this ready in [timeframe]. Does that work?"

→ **Confirm:** Shared understanding, clear next deliverables

---

# REFERENCE: Key Things to Observe

## During the Meeting, Watch For:

### Integration Challenges:
- How do they currently connect YWCA data → 10Seven research → Trauma Graph?
- Where does integration break down today?
- What's manual vs. automated?
- What takes the most time?

### Edge Cases:
- Programs that don't fit the framework
- Chapters that serve multiple geographies
- Data that's missing or low quality
- Exceptions to the rules

### Pain Points (Listen for These Phrases):
- "This takes forever..."
- "We have to manually..."
- "There's no good way to..."
- "Chapters struggle with..."
- "We wish we could..."

### Assumptions to Validate:
- Is data individual client records or aggregate numbers?
- Is update frequency monthly, quarterly, or as-needed?
- Do chapters actually want cross-chapter discovery?
- Is trauma graph integration the killer feature or nice-to-have?

---

# MEETING PREP CHECKLIST

## Before Thursday:
- [ ] Review this questions doc
- [ ] Review PROJECT_UNDERSTANDING.md
- [ ] Have notepad ready to sketch
- [ ] Screen sharing set up if remote
- [ ] Recording set up (with permission)

## During Thursday:
- [ ] Let them show you (screen share, documents, tools)
- [ ] Take notes on pain points and frustrations
- [ ] Sketch workflows as they describe them
- [ ] Ask "can you show me an example?" frequently
- [ ] Confirm understanding as you go

## After Thursday:
- [ ] Send summary of what you heard
- [ ] Request any materials they mentioned
- [ ] Confirm next deliverables and timeline
- [ ] Update PROJECT_UNDERSTANDING.md with new info

---

# PRO TIPS

**Best Practices for This Meeting:**

1. **"Show me" > "Tell me"**
   - Ask them to share their screen
   - Look at actual documents together
   - See their current tools in action

2. **Real examples > Hypotheticals**
   - "Show me a program that was hard to categorize"
   - Not "How would you categorize a complex program?"

3. **Current reality > Envisioned future**
   - "How do you do this today?"
   - Not "How do you want to do this?"

4. **Follow the energy**
   - When they get excited or frustrated, dig deeper
   - That's where the real requirements are

5. **Draw everything**
   - Sketch workflows, data flows, screens
   - Visual understanding > verbal description

6. **Confirm as you go**
   - "Let me make sure I understand..."
   - Repeat back what you heard
   - Catch misunderstandings early

7. **Embrace silence**
   - Let them think
   - Don't fill every pause
   - Best insights come after pauses

8. **"What else?"**
   - When they finish an answer, ask "What else?"
   - Often the most important thing comes 3rd or 4th

---

# RED FLAGS TO WATCH FOR

⚠️ **"We envision..." without showing current state** → Ask to see how they do it today first

⚠️ **Vague on actual workflows** → Keep asking for specific examples

⚠️ **Everything is "must-have"** → Force prioritization: "If you could only have ONE thing..."

⚠️ **No real examples to show** → This might be more aspirational than they let on

⚠️ **Can't show you the trauma graph** → Is it actually built? Is it just a concept?

⚠️ **Haven't talked to YWCA users** → Who validated that this is what chapters need?

⚠️ **Unrealistic timeline** → "We need this in 2 weeks" = manage expectations now

---

# YOUR GOAL

**By end of Thursday, you should be able to answer:**

✅ How do they currently do their work?
✅ Where does it break down?
✅ What does the trauma graph actually show?
✅ How do the three pieces (YWCA, 10Seven, Trauma Graph) integrate?
✅ What are real edge cases vs. theoretical ones?
✅ What must be in v1?
✅ What does success look like?

**You should NOT know yet:**
❌ Exact data model design
❌ Technical architecture specifics
❌ UI/UX designs
❌ Implementation details

**Those come after you understand their world.**

---

# OPENING LINE

> "Thanks for taking the time today. I've reviewed the survey and your framework document, and I have a lot of questions. But before I ask anything, I'd love to just see how you work today. Can you show me [a research paper / the trauma graph / how you currently use YWCA data]? Let's start there and I'll ask questions as we go."

**This sets the tone: Show me your world, I'm here to understand.**

Good luck! 🚀
