# GAP ANALYSIS - Critical Unknowns from Client Call

## ⚠️ RED FLAGS & CRITICAL GAPS

### 🚨 HIGHEST PRIORITY GAPS (Must Resolve Thursday)

---

## Gap 1: MVP Scope is Completely Undefined

**What we know:**
- They need a data warehouse
- They need trauma graph integration
- They want it for 196 chapters

**What we DON'T know:**
- What MUST be in version 1 vs. version 2?
- Can data warehouse launch without trauma graph?
- Can trauma graph launch without data warehouse?
- What's the absolute minimum YWCA will accept?
- What's the timeline? (NEVER mentioned in call - huge red flag)

**Why this is critical:**
This could be a 6-month project or a 2-year project. Without clear MVP scope, you'll be building forever or disappointing the client.

**Questions to ask:**
1. "What's the launch date you promised YWCA?"
2. "If you had to pick ONE thing for v1, data warehouse or trauma graph?"
3. "What features can we defer to v2 without breaking the deal?"

---

## Gap 2: The Trauma Graph is a Black Box

**What we know:**
- It shows financial trauma, domestic violence by geography
- It's "fixed" data from 10Seven's research
- It allows "drill down to neighborhood level"
- Users can see "what percentage of our data set is experiencing something"

**What we DON'T know:**
- Does it currently exist or are you building it from scratch?
- Chloe says Chris has "already started to mock up" - what's the current state?
- What's the data source? How often is it updated?
- How does geographic matching work? (manual? automatic by zip code?)
- What does "overlay" mean technically? API calls? Pre-loaded datasets?
- What's the UX? Can you show an example?

**Why this is critical:**
Everyone talks about trauma graph but nobody explains what it IS. This could be 50% of the technical effort.

**Questions to ask:**
1. "Can you show me the trauma graph right now? Even if incomplete?"
2. "What data is in it? What are the actual fields/metrics?"
3. "How does a user interact with it? Walk me through the UX."
4. "Is the data refreshed real-time or monthly?"

---

## Gap 3: The Previous Proposal - What Was Already Promised?

**What we know:**
- Someone before Chris wrote a proposal
- It was sent to YWCA, then to their funders
- It's a "low key roadmap"
- Chloe says "a lot of the steps, I think, still apply"

**What we DON'T know:**
- What features were promised in that proposal?
- What timeline was committed to?
- What budget was quoted?
- What technical decisions were already made?
- Does YWCA think those commitments still stand?

**Why this is critical:**
You might be inheriting commitments you don't know about. YWCA might expect features that were promised but never communicated to you.

**Questions to ask:**
1. "Walk me through what was in the previous proposal line by line"
2. "What did YWCA agree to based on that proposal?"
3. "What technical approach did the previous developer recommend?"
4. "Are there any promises in there that are unrealistic?"

---

## Gap 4: Survey Replacement Strategy is Vague

**What we know:**
- Current survey: 61 pages, 45-50 questions, takes 3 weeks
- Previous survey: 800 questions (!)
- Platform should "take all this stuff we collected from you in this survey and put it in this dashboard"
- October 2024 survey data exists

**What we DON'T know:**
- Does the platform REPLACE the survey or COMPLEMENT it?
- Do chapters fill out survey once to seed the platform, then update ongoing?
- Does the survey go away completely after platform launches?
- What happens to October 2024 survey data? Import it?
- Are some questions annual-only vs. ongoing tracking?

**Why this is critical:**
This determines your entire data model and onboarding flow. If you're importing existing data, you need a migration plan. If survey continues, you need integration.

**Questions to ask:**
1. "After platform launches, do you still send out the annual survey?"
2. "Should we import the October 2024 survey responses as baseline data?"
3. "Which survey questions become ongoing data entry vs. one-time setup?"

---

## Gap 5: Cross-Chapter Visibility Rules Undefined

**What we know:**
- Chapters want to see "what other organizations are up to"
- Example: Buffalo wants to see what New York chapters are doing
- Andrea says: "they could just go into this platform and say, oh, in Buffalo, they're doing X, Y, Z"

**What we DON'T know:**
- Can Buffalo see Rochester's RAW data or only aggregated?
- Can they see specific program details or just categories?
- Can they see individual chapter identities or anonymous?
- What if chapters are competing for same grants? (competitive sensitivity)
- Is this opt-in per chapter or forced visibility?
- What about client-level data? (HIPAA concerns)

**Why this is critical:**
This determines your entire permissions/security architecture. Get it wrong and you violate HIPAA or create competitive problems.

**Questions to ask:**
1. "Give me 3 examples of what Buffalo chapter CAN see about Rochester"
2. "Give me 3 examples of what they CANNOT see"
3. "Can chapters opt out of sharing their data with the network?"

---

## Gap 6: Research vs. Operations Priority is Unclear

**What was said:**
- Chloe: "We did run correlational analyzes. We did run multivariate regressions"
- Chloe: "I don't think that functionality needs to be on their stuff"
- Chloe: "But the capability will be there. Because if we ever did get a client that's like, yeah, I want to be able to do multivariate regressions...we could turn that on"

**The confusion:**
- Is this primarily a research tool for 10Seven?
- Or primarily an operational tool for YWCA chapters?
- Do you build advanced statistics now or later?
- Who's the primary user?

**Why this is critical:**
Research tools and operational tools have different architectures. Research needs data exports, statistical packages, flexible schemas. Operations needs simple UIs, templates, guardrails.

**Questions to ask:**
1. "Is the primary purpose to help chapters write grants? Or to help 10Seven publish research?"
2. "Should chapters see the impact framework or should we hide it?"
3. "Do we build statistical analysis in v1 or can that wait?"

---

## Gap 7: Technical Architecture - Completely Unspecified

**What we know:**
- Nothing. Zero technical details in the entire call.

**What we DON'T know:**
- What's the tech stack?
- Where does this deploy? (cloud? on-prem?)
- Who hosts it? (10Seven? YWCA? vendor?)
- What about data residency for HIPAA compliance?
- What about backups, disaster recovery?
- What about performance? (196 chapters × thousands of records each)
- What's the database approach? (one DB with 196 tenants? 196 separate DBs?)

**Why this is critical:**
You can't estimate effort or cost without knowing the technical foundation. HIPAA compliance alone could double your effort.

**Questions to ask:**
1. "Where will this be hosted?"
2. "Do you have technical infrastructure already or start from scratch?"
3. "What's your preference for tech stack?"
4. "Who handles DevOps, monitoring, backups?"

---

## Gap 8: Budget and Resources - Never Mentioned

**What was said:**
- "They received grant dollars that we co-wrote with them to build this"
- "We want to give you enough information for, frankly, us to defer to you"

**What was NOT said:**
- How much money is available?
- What's the budget for this project?
- Are there budget constraints?
- Is this fixed-bid or hourly?

**Why this is critical:**
Budget determines scope. If they expect a $500K platform but have $50K budget, that's a problem you need to know NOW.

**Questions to ask:**
1. "What's the total budget for this project?"
2. "Is this funded by YWCA's grant or 10Seven's budget or both?"
3. "Are there milestone payments or one lump sum?"

---

## Gap 9: Chris's Role and Capacity Unclear

**What the call implies:**
- Chris is building the Smith education platform (already underway)
- Chris is now being asked to build the YWCA data platform
- These are being discussed as if Chris is solo developer

**What's unclear:**
- Is Chris expected to build both simultaneously?
- Is there a team or is Chris solo?
- What's Chris's actual capacity?
- Who handles design? Testing? DevOps?
- Is this realistic?

**Why this is critical:**
This could be 6-12 months of full-time work for a team. If Chris is expected to do this alone while also working on Smith, that's a recipe for burnout or failure.

**Questions to ask:**
1. "What's the team structure? Is there a team or am I solo?"
2. "What's my expected allocation? 100% on this or splitting time with Smith?"
3. "Who handles design? QA? DevOps?"

---

## Gap 10: Report Generation is Vague "Pretty and Comprehensive"

**What was said:**
- "They're gonna type in. We had 168 people. 108 of them ate breakfast this morning, it needs to spit out a report that's like, pretty and comprehensive"
- "They really want to be able to write a grant and say, Hey, in the state of New York...70% of our programs are dealing with women who are SNAP eligible"

**What's unclear:**
- What format? PDF? Word? Excel? All three?
- What sections does a report have?
- Is it templated or customizable per chapter?
- Can they add their own narrative text?
- What audience? (foundations? government? individual donors?)
- Do different grant types need different reports?

**Why this is critical:**
Report generation could be 25% of the development effort. Need specifics.

**Questions to ask:**
1. "Show me an example grant report you wish you could generate"
2. "What format do funders require?"
3. "Can chapters customize reports or must they use fixed templates?"

---

## Gap 11: The "Diagnostic Tools" Mystery

**What was said:**
- "We also have a different other tools, like surveys and diagnostic things and whatever that they can leverage from the platform"
- "They were able to pull a diagnostic tool from the platform that they give to the women who come in"
- "We don't sell that outright, like I'm not going to send you a PDF of that. You have to have a license in order to access those tools"

**What's unclear:**
- What ARE these diagnostic tools?
- Do they already exist or need to be built?
- Are these 10Seven's research instruments?
- How do chapters use them? Download PDFs? Online forms?
- How do results flow back into the platform?

**Why this is critical:**
If you're building a library of assessment tools, that's a whole additional feature set not discussed.

**Questions to ask:**
1. "What diagnostic tools do you have already built?"
2. "Do chapters administer these online or on paper?"
3. "Do results automatically populate the platform?"

---

## Gap 12: The Data Flow is Fuzzy

**What was said:**
- "How do you envision that they upload their information. How often? What does that flow look like?"
- Chloe: "That's such a good question...they should be doing the same, considering how many women they serve...at a minimum monthly"

**What's unclear:**
- Do chapters manually enter data or import from files?
- If importing, what format? (CSV? Excel? API from other systems?)
- What if they already have a platform they're using?
- How do you prevent duplicate entries?
- Who ensures data quality?

**Why this is critical:**
Data entry UX makes or breaks adoption. If it's too hard, they won't use it.

**Questions to ask:**
1. "Do chapters enter data manually or import from other systems?"
2. "What systems are some chapters currently using that we need to integrate with?"
3. "Who ensures data quality? Can HQ edit chapter data?"

---

## Gap 13: Qualtrics Integration - Required or Optional?

**What was said:**
- "I largely use Qualtrics...I'm fine if there was a way...if we can just embed it cool"
- "I don't know if Qualtrics what their API situation looks like"
- "If I don't have to, like, log on constantly, and it's something that we can just use, that'd be great"

**What's unclear:**
- Is Qualtrics integration required for MVP?
- Is this for 10Seven's internal use or YWCA's use?
- Does YWCA have Qualtrics accounts?
- Do you need Qualtrics Enterprise for API access?
- Or can this be deferred to v2?

**Why this is critical:**
Third-party integrations can be complex and expensive. Need to know if this is must-have or nice-to-have.

**Questions to ask:**
1. "Is Qualtrics integration required for YWCA launch?"
2. "Who pays for Qualtrics licenses?"
3. "Can we defer this to v2?"

---

## Gap 14: National HQ vs. Chapter Permissions

**What was said:**
- "USA kind of gets its own version where it kind of collates all of the data"
- "Individual chapters get, like their own much better, more functional data warehouse"

**What's unclear:**
- What can HQ do that chapters can't?
- Can HQ edit chapter data or only view?
- Can HQ delete chapters? Archive them?
- Can HQ force chapters to use certain fields?
- Do chapters see the same interface or different UI?

**Why this is critical:**
Multi-level permissions are complex. Need clear rules.

**Questions to ask:**
1. "What permissions does national HQ have that chapters don't?"
2. "Can HQ edit chapter data?"
3. "Do they see the same UI or a different admin interface?"

---

## Gap 15: Historical Data and Migration

**What was said:**
- October 2024 survey data exists
- "Some people actually have, like, a data platform that they're using, but they like, hate it"

**What's unclear:**
- Should you import October 2024 survey data?
- If chapters have existing platforms, migrate their data?
- How many years of historical data do they want?
- Is historical comparison important? (year-over-year)
- Or start fresh?

**Why this is critical:**
Data migration is risky and time-consuming. Need to know if required.

**Questions to ask:**
1. "Do you want to import existing survey data or start fresh?"
2. "How important is historical comparison?"
3. "What's the migration strategy for chapters already on other platforms?"

---

## Gap 16: Training and Change Management

**What was said:**
- 196 chapters with varying sophistication
- "Some are in LA, but some are in a very rural town in Illinois and or like Alaska"
- "Some organizations, it's literally two full time employees, and everyone else is volunteer"

**What's unclear:**
- Who trains 196 chapters?
- Is there onboarding materials? Videos? Live training?
- What's the rollout strategy? (all at once? phased?)
- Who provides ongoing support?
- What if chapters refuse to use it?

**Why this is critical:**
Best platform in the world fails without adoption. 196 chapters = huge change management challenge.

**Questions to ask:**
1. "What's the rollout plan? All chapters at once or phased?"
2. "Who handles training?"
3. "What support resources do we need to provide?"

---

## Gap 17: The "White Label" Ambiguity

**What was said:**
- "Bespoke, but really white label data warehouse"
- They want to license to other clients beyond YWCA

**What's unclear:**
- Is this YWCA-branded or 10Seven-branded?
- How configurable must it be for other clients?
- What's hardcoded vs. configurable?
- Can other clients have different data models?
- Or must they fit 10Seven's framework?

**Why this is critical:**
Building true multi-tenant SaaS is much harder than building one custom solution.

**Questions to ask:**
1. "Is this YWCA-specific or a product you'll sell to others?"
2. "How much customization will future clients need?"
3. "Should we build for one client now and generalize later?"

---

## Gap 18: The Impact Framework Enforcement

**What we know from the survey doc:**
- 4 impact measurement pillars
- 3 types of impact
- 3 types of violence
- Specific intervention types for each

**What's unclear:**
- Must chapters fit into this framework?
- Or can they define their own categories?
- Is the framework visible to end users?
- Or abstracted in the UI?
- What if a program doesn't fit?

**Why this is critical:**
Rigid frameworks frustrate users. Flexible frameworks create data quality problems. Need right balance.

**Questions to ask:**
1. "Must ALL programs fit into your violence type taxonomy?"
2. "Can chapters add their own categories?"
3. "Do chapters see this framework or is it hidden?"

---

## Gap 19: File Uploads and Document Management

**What we know from survey:**
- Chapters can upload 990s, budgets, strategic plans, impact documentation

**What's unclear:**
- Is this just file storage or do you extract data from files?
- Version control? (upload 2023 990, then 2024 990 - how handled?)
- File size limits? Security scanning?
- Who can see uploaded files?
- Can files be shared across chapters?

**Why this is critical:**
Document management can be complex, especially with HIPAA considerations.

**Questions to ask:**
1. "Is file storage just for reference or do we extract data?"
2. "What's the workflow for version control?"
3. "What security is required for uploaded files?"

---

## Gap 20: The "They're Disorganized" Warning

**What Chloe said:**
- "Another client to put it nicely, very quirky. They're highly disorganized in a hot mess"

**The implication:**
- Requirements will be unclear
- Decision-making will be slow
- Expectations may be unrealistic
- Adoption may be challenging

**Why this is critical:**
Difficult clients require more explicit contracts, more documentation, more change order processes.

**Questions to ask:**
1. "Who's the decision-maker at YWCA?"
2. "How do we handle scope changes?"
3. "What's the escalation process for issues?"

---

## SUMMARY: What MUST Be Clarified Thursday

### Can't Proceed Without:
1. **MVP Definition** - What's in v1?
2. **Timeline** - When do they need it?
3. **Budget** - How much money is available?
4. **Trauma Graph** - Show me what exists
5. **Previous Proposal** - What was promised?

### Critical for Accurate Estimate:
6. **Technical Architecture** - Where deployed? What stack?
7. **Chris's Role** - Solo or team? Capacity?
8. **Survey Replacement** - Import existing data?
9. **Report Generation** - Show example output
10. **Cross-Chapter Visibility** - What's public vs. private?

### Important for Good UX:
11. **User Personas** - Who exactly uses what features?
12. **Data Entry Flow** - Manual or import?
13. **Permission Levels** - HQ vs. chapter roles
14. **Diagnostic Tools** - What exists vs. needs building?
15. **Qualtrics Integration** - Required or optional?

---

## RISKS IF GAPS NOT ADDRESSED

### Risk 1: Massive Scope Creep
Without clear MVP, this becomes a never-ending project.

### Risk 2: Technical Debt
Building without architectural planning = rewrite later.

### Risk 3: Failed Adoption
If YWCA doesn't use it, project fails regardless of technical quality.

### Risk 4: Budget Overrun
No budget discussion = high risk of Chris undercharging or client sticker shock.

### Risk 5: Missed Expectations
Previous proposal may have set expectations Chris doesn't know about.

### Risk 6: Burnout
If Chris is expected to solo-build two major platforms simultaneously, unsustainable.

---

## RECOMMENDED APPROACH FOR THURSDAY

### Part 1: Start with Constraints (30 min)
1. "What's the deadline YWCA expects?"
2. "What's the total budget?"
3. "Show me the previous proposal - what was promised?"
4. "What MUST be in v1 vs. what can wait?"

### Part 2: Show Don't Tell (45 min)
1. "Show me the trauma graph"
2. "Show me your current tools (Max QDA, Qualtrics, etc.)"
3. "Show me an example grant report you want to generate"
4. "Show me the October 2024 survey data"

### Part 3: Walk Through Scenarios (45 min)
1. "Walk me through: Buffalo chapter logs in to enter a new domestic violence program. What happens?"
2. "Walk me through: Buffalo chapter needs to write a grant by Friday. What do they do?"
3. "Walk me through: National HQ wants to see network-wide childcare statistics. What do they do?"

### Part 4: Make Decisions (30 min)
1. Data warehouse first or trauma graph first?
2. Survey import or start fresh?
3. Qualtrics integration in v1 or v2?
4. Statistical analysis in v1 or v2?
5. What's the rollout plan?

---

## CONFIDENCE LEVEL ASSESSMENT

### High Confidence (80%+):
✅ Who the client is (YWCA)
✅ The core problem (no data system)
✅ The desired outcome (grant-ready reports)
✅ User sophistication range
✅ Two main components exist conceptually

### Medium Confidence (50-80%):
⚠️ The survey structure (we have the doc)
⚠️ The impact framework (we have the doc)
⚠️ Cross-chapter visibility (some discussion)
⚠️ Basic feature list (mentioned but vague)

### Low Confidence (20-50%):
❌ MVP scope
❌ Timeline
❌ Budget
❌ Technical requirements
❌ Report generation specifics
❌ Trauma graph details

### No Confidence (<20%):
🚫 What was in previous proposal
🚫 Deployment architecture
🚫 Chris's role and capacity
🚫 Data migration strategy
🚫 Training and rollout plan
🚫 Change management approach

---

## BOTTOM LINE

**The call was excellent for CONTEXT but terrible for SPECIFICS.**

You understand:
- Why YWCA needs this
- What pain they're experiencing
- What outcome they want
- Who will use it

You don't understand:
- What to actually build
- When they need it
- How much they can pay
- Where it deploys
- Who builds it

**Thursday's meeting must get specific or you'll be building blindly.**

The fact that budget was never mentioned is the biggest red flag.
