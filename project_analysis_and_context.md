# YWCA Data Platform Project - Analysis and Context

## Conversation Context

**Date**: 2025-11-05
**Your Role**: Chris (Developer/Technical Lead)
**Clients**: Nina, Andrea, and Chloe (10Seven team)
**Situation**: You had a call with clients about a new project and left feeling unclear about what they need. You requested help analyzing the call transcript to better understand the project requirements.

---

## Project Overview

Your clients are building a platform called **"The Impactory"** - a dual-purpose data system with two main components that can be licensed separately or together.

### The Client: YWCA

- **Organization**: YWCA (Young Women's Christian Association)
- **Structure**: 196 local chapters nationwide with headquarters in DC
- **Programs**: Domestic violence housing, childcare, gyms, leadership programs for teen girls, economic empowerment
- **Current State**: No centralized data system ever, highly disorganized, chapters use spreadsheets/manual tracking or nothing at all

---

## Core Problems They're Solving

1. **No data infrastructure**: Chapters have nowhere to store their program data systematically
2. **Survey fatigue**: Headquarters constantly surveys chapters (used to be 800 questions, now 45-50) that take weeks to complete
3. **No reporting back**: After collecting survey data, nothing gets shared back to chapters
4. **Can't fundraise effectively**: Without compelling data narratives, they can't write strong grant applications
5. **Wide capability gap**: Some chapters have 2 employees, others have 50 - vast differences in data sophistication
6. **No cross-learning**: Chapters can't see what other chapters are doing

---

## What You Need to Build: Two Components

### Component 1: Data Warehouse/Dashboard

**Think of it as a "data intranet"** - a centralized repository that:

- Allows all 196 chapters to upload and store their program data
- **Must be extremely user-friendly** (their previous data person "didn't know what a correlation was")
- Automatically synthesizes data (e.g., user enters "168 people, 108 ate breakfast" → platform calculates and displays "64% ate breakfast")
- Generates "pretty and comprehensive" reports for grant writing
- Lets chapters see what other chapters are doing (discovery/collaboration)
- Provides off-the-shelf diagnostic survey tools they can use with clients
- HIPAA compliant (they use this as their standard even though not required)
- USA headquarters gets aggregated view of all chapter data
- Best practice: monthly data updates

**Key Technical Requirements:**
- Multi-tenant architecture (196 separate chapters + 1 national view)
- Role-based access control
- Data aggregation and automatic calculations
- Report generation
- Survey tool integration
- Cross-chapter visibility features

---

### Component 2: Trauma Graph Integration

**10Seven's proprietary research tool** that:

- Contains fixed datasets about financial trauma, domestic violence severity, etc. by geographic area
- Visualizes as interactive maps (can drill down to neighborhood level)
- Shows **side-by-side/split-screen view**: chapter's own data alongside 10Seven's trauma research
- **Example use case**: Chapter sees "67% of our clients experience financial shame" → compares with 10Seven's shame indicators for their neighborhood → identifies hotspots → targets case managers to specific areas
- **Never shares raw data** - only aggregated visualizations/percentages
- Separate license from the data warehouse

**Key Technical Requirements:**
- Geographic visualization (maps)
- Drill-down capability (state → neighborhood level)
- Split-screen/side-by-side comparison view
- Integration with the data warehouse for comparison features
- Usage tracking (for usage-based licensing)

---

## Key Technical Considerations

### User Experience

- Target users range from 2-person volunteer operations to sophisticated data teams
- Must be "as simple as logging into company intranet"
- Platform does the analysis work for them (automatic percentages, correlations)
- Advanced features (multivariate regressions) available but hidden from basic users
- Focus on accessibility over complexity

### Data Flow

1. Chapters upload their data regularly (ideally monthly)
2. Platform stores and synthesizes it
3. Creates exportable reports for grant writing
4. Allows cross-chapter visibility for learning
5. Headquarters gets consolidated national view

### Security & Compliance

- HIPAA compliance standard (even though not technically required)
- Data privacy - chapters own their data
- 10Seven's research data never exposed as raw data, only visualizations
- Secure multi-tenant data isolation

### Licensing Model (Affects Architecture)

- **License 1**: Data warehouse only
- **License 2**: Trauma graph only
- **Most common**: Both licenses together
- Usage-based pricing being considered for trauma graph
- Need to discuss how this affects data fetching/architecture

---

## Current Tools They Want to Consolidate

They currently use multiple platforms that this should potentially replace/integrate:

- **Qualtrics**: Surveys and statistical analysis (might embed via API)
- **Max QDA**: Qualitative data coding
- **Tableau**: Data visualization
- **Atlas**: Another data platform

---

## Business Context

- This is white-label/replicable for other clients beyond YWCA
- Only targets clients interested in their specific research areas (financial trauma, wealth justice, domestic violence, etc.) - not a generic data platform
- Other potential clients mentioned:
  - **Smith**: Education platform (separate project you're already working on with CMS)
  - **Urban Institute**: Research organization (would likely license trauma graph only)
- They're positioning as "not becoming a software company" but building proprietary tools that integrate with their research

---

## Parallel Project: Smith (For Context)

You're also working on an education platform for another client called Smith:
- Built a CMS (Content Management System) that was well-received
- Platform is for educational content delivery to students
- Has modules, units, and pages with navigation
- Integration with podcast features being discussed
- This represents the "education hub" version of The Impactory

---

## What's Coming Next

### Materials They're Sending You:

1. Previous proposal written for YWCA (technical roadmap)
2. Impact survey they created for YWCA (shows what data they collect)
3. Deck explaining survey questions and rationale
4. Information about current platforms they use (Max QDA, Qualtrics, Tableau, Atlas)

### Next Meeting:

- **When**: Thursday (moved up 1 hour - now 10am PST / 1pm EST)
- **Purpose**: Walk through all materials, discuss trauma graph in detail, expand scope to cover entire Impactory platform
- **Agenda**:
  - Review existing tools they use
  - Understand data collection methods
  - Discuss licensing structure and technical requirements
  - Clarify exact data types and platform specifications

### Additional Near-Term:

- Meeting with Renee on the 11th to discuss licensing pricing for Smith project
- Chloe will send proposal and survey materials before Thursday meeting

---

## Key Questions Still Outstanding

1. **Licensing architecture**: How does the licensing model affect how you build data fetching/access?
2. **Platform integration**: Should Qualtrics be embedded or replaced?
3. **Data types**: Exact specifications of what data goes where
4. **Split-screen mechanics**: Technical implementation of side-by-side data comparison
5. **Statistical tools**: What level of analysis capability to expose to different user types?
6. **Multi-tenancy**: How to handle 196 separate chapters plus national aggregation?
7. **Data import**: How do chapters get their existing data (spreadsheets, etc.) into the system?
8. **API requirements**: For third-party integrations (Qualtrics, potential future tools)

---

## What Makes This Confusing

The project is complex because it's actually **three things in one**:

1. **A data management system** (warehouse for YWCA's data)
2. **A research tool** (trauma graph visualization)
3. **A white-label platform** (replicable for multiple clients)

Plus it needs to serve users with vastly different technical sophistication levels while maintaining HIPAA-level security.

---

## Key Insights from the Call

### User Quotes That Reveal Requirements:

**On simplicity:**
> "Their data person was like a former elementary maths teacher who, like, didn't know what a correlation was" - Chloe

**On user experience:**
> "I want to log in and just like, see a reminder of how many programs were in California last year under child care. Like, I don't think it's like this, like, super sophisticated thing." - Andrea

**On the data intranet concept:**
> "It really is. It has that kind of vibe, you know, when you log on to your like, company internet and like, there's, like, pretty basic announcements and things, but it also is just like a repository for everything you kind of need to know about the organization" - Chris (your analogy was spot-on!)

**On their disorganization:**
> "They are a client that will also be using the impactory, but instead of for the education side, they need a data platform. I'm not sure how they are, as large as they are, and they literally have had no data system ever like to track their impact" - Chloe

**On data synthesizing:**
> "They're gonna type in. We had 168 people. 108 of them ate breakfast this morning, it needs to spit out a report that's like, pretty and comprehensive." - Chloe

**On the actual use case:**
> "All they could say right now is, will you serve 100 girls? It's like, that's not compelling." - Chloe (This is why they need the platform - to tell compelling data stories for fundraising)

---

## Technical Architecture Considerations

Based on the requirements, you'll likely need:

### Frontend:
- User-friendly dashboard interface
- Interactive data visualizations
- Map-based visualization for trauma graph
- Split-screen/comparison view
- Report generation interface
- Cross-chapter discovery/browsing

### Backend:
- Multi-tenant data architecture
- User authentication & authorization (chapter-level, national-level)
- Data aggregation engine
- Statistical calculation engine (percentages, correlations, regressions)
- Report generation engine
- API layer for integrations
- Usage tracking (for licensing)

### Data Storage:
- Relational database for structured data
- Separation between client data and 10Seven research data
- Geographic data for trauma graph
- Time-series data (for tracking over time)

### Integration Points:
- Qualtrics (surveys) - possibly via API
- Existing data import (CSV, Excel uploads)
- Export capabilities (PDF reports, data exports)

---

## Action Items for You (Chris)

- [ ] Review materials when they arrive (proposal, survey, platform info)
- [ ] Research the existing platforms they use (Max QDA, Qualtrics, Tableau, Atlas)
- [ ] Prepare questions about licensing architecture for Thursday meeting
- [ ] Think about multi-tenant architecture approach
- [ ] Consider how to handle the split-screen trauma graph comparison feature
- [ ] Prepare technical recommendations for the Thursday discussion

---

## Notes

- The call transcript was 13 pages long and very conversational, which is why the requirements felt scattered
- Your clients (Nina, Andrea, Chloe) clearly know what they want but explained it in business terms rather than technical specifications
- The project is actually well-thought-out from their perspective - they've done a year and a half of research with YWCA
- The confusion likely came from the dual nature of the product (data warehouse + research tool) and the wide range of user sophistication levels it needs to serve
- This is a significant project with potential for multiple clients beyond YWCA

---

## Summary for Quick Reference

**What it is**: A user-friendly data platform that lets YWCA chapters store their program data and compare it with 10Seven's trauma research to tell compelling stories for fundraising.

**Core challenge**: Make it simple enough for volunteers with no data experience, but powerful enough to be useful.

**Two products in one**:
1. Data warehouse (their data)
2. Trauma graph (10Seven's research data)

**Scale**: 196 chapters + 1 national headquarters view

**Key differentiator**: Integration of client's operational data with 10Seven's proprietary research data for contextual insights.
