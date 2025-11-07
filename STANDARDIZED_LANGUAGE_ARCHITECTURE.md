# Standardized Language & Architecture - The Impactory

**Purpose**: Define how the three products communicate with each other
**Created**: After Thursday call analysis
**Status**: Framework for Monday discussion

---

## Core Insight: The Relationship Between the Three Products

### **Internal Warehouse** is the **source of truth**
- This is where 10Seven does all their research work
- Creates raw data, codes, themes, insights, maps
- Everything originates here

### **Trauma Graph** is a **published artifact** created from the Warehouse
- It's not a separate product - it's a **view** of warehouse data
- Like publishing a book: the manuscript lives in the warehouse, the published book is the trauma graph
- Clients license access to see the published version

### **White Label** is **client's own data** + **optional trauma graph viewing**
- Separate data (YWCA's programs, not 10Seven's research)
- Can optionally "subscribe" to view trauma graphs
- Geographic connection: YWCA data is linked to trauma graph by location

---

## The Shared Foundation: Geography

**Everything connects through geography.** This is the common language.

All three products need to reference the **same geographic entities**:
- National level: 3,000 counties
- State/City level
- Neighborhood level
- Zip codes
- Custom boundaries (e.g., "St Paul neighborhood X")

**Why this matters**:
- Internal team codes interview: "This person lives in St Paul neighborhood X"
- Trauma graph shows: "Severity level 4 in neighborhood X"
- YWCA enters data: "We serve 500 women in neighborhood X"
- System links them: Same neighborhood X

**Key question for Monday**: Do you build your own geographic reference system, or use existing (Census data, OpenStreetMap, Google Places)?

**Challenge**: Not all neighborhoods have official boundaries. Chloe said she pulls maps from city websites. How do you standardize this?

---

## Data Flow Architecture

### **Flow 1: Internal Warehouse CREATES Trauma Graph**

```
Internal Warehouse Work:
1. Collect data (surveys, interviews)
2. Qualitative coding (highlight → code → themes)
3. Quantitative analysis (correlations, stats)
4. Map themes to geography ("housing insecurity in neighborhood X")
5. Assign severity levels (1-4)
6. Write insights ("Self-harm from bills common in neighborhood X")

When ready to share with clients:
7. "Publish" trauma graph
   - Select geography (St Paul)
   - Select date range
   - Choose which insights are "client-facing" vs "internal only"
   - Generate final severity map
   - Version it ("St Paul Financial Trauma 2024 v1.0")
   - Status: Published

Result:
→ A "Trauma Graph" becomes a licensable asset
```

**Key point**: Trauma Graph is not created separately. It's a **packaged export** from the internal warehouse, frozen at a point in time (but can be updated).

---

### **Flow 2: Clients LICENSE Trauma Graph access**

```
Client (YWCA or other) wants to see St Paul trauma data:
1. They purchase/license "St Paul Trauma Graph"
2. System records: Client X has access to Trauma Graph Y
3. When they log in, system checks licenses
4. They can VIEW:
   - Map with severity color-coding
   - Published insights for geography
   - Version history
5. They CANNOT see:
   - Raw interview transcripts
   - Survey responses
   - Internal working notes
   - Unpublished insights
```

**Key point**: It's a **read-only view** of published data. Like buying access to a research report.

---

### **Flow 3: White Label stores CLIENT'S data**

```
YWCA has their own data (separate from 10Seven's research):
- How many programs
- How many people served
- How many buildings owned
- Which neighborhoods they serve
- Impact survey responses

This lives in White Label:
1. YWCA enters: "We have a childcare program serving 500 women in St Paul neighborhood X"
2. System stores: YWCA data tied to geography (neighborhood X)
3. YWCA can query: "How many local associations have childcare?"
4. System generates reports from YWCA's own data
```

**Key point**: This is **YWCA's data**, not 10Seven's. Separate tenant, separate data.

---

### **Flow 4: Side-by-Side View (if YWCA licenses Trauma Graph)**

```
YWCA has:
- White label (their own data)
- Trauma graph license (10Seven's research)

When YWCA views neighborhood X:

Left side (their data):
- "We serve 500 women in neighborhood X"
- "Childcare program"
- "3 buildings"

Right side (trauma graph):
- "Severity level 4 in neighborhood X"
- "Financial trauma: housing insecurity is saturated theme"
- "Self-harm from unexpected bills common"

Connection: Both reference same geography (neighborhood X)
```

**Key point**: **Geographic linking** is what enables side-by-side view. Shared geographic reference system is critical.

---

## Core Shared Data Models

Here's what all three products need to understand:

### 1. **Geographic Reference System** (Foundation)

```
Geography Entity:
- Unique ID (e.g., "stpaul-neighborhoodX")
- Type (county, city, neighborhood, zip)
- Name ("Neighborhood X")
- Parent geography (neighborhood → city → county → state)
- Boundary data (polygons for mapping)
- Alternative names/aliases
```

**Used by**:
- Internal Warehouse: Tag interviews/surveys with geography
- Trauma Graph: Display severity by geography
- White Label: YWCA associates programs with geography

**Key decision**: How do you handle neighborhoods without official boundaries? Chloe manually finds maps from city websites.

---

### 2. **Trauma Graph** (Licensable Asset)

```
Trauma Graph:
- Unique ID
- Name ("St Paul Financial Trauma 2024")
- Geography covered (St Paul, MN)
- Geographic level (neighborhood, county, national)
- Version number
- Created date / last updated
- Status (draft, published, archived)
- Associated research project
```

**Created by**: Internal Warehouse
**Viewed by**: Clients with licenses
**Lives in**: Shared system (both warehouse and client view can access)

---

### 3. **Severity Assignments** (Geographic + Trauma Graph specific)

```
Severity Data:
- Trauma Graph ID (which graph this belongs to)
- Geography ID (which neighborhood/county)
- Severity level (1-4)
- Color code (for map visualization)
- Calculated from which themes/codes (internal reference)
- Last updated date
```

**Created by**: Internal Warehouse (automated from severity rules + manual judgment)
**Viewed by**: Internal team (full details) + Clients (just severity level + color)

---

### 4. **Insights** (Research findings tied to geography)

```
Insight:
- Trauma Graph ID
- Geography ID (could be state, county, neighborhood)
- Author (Chloe, Nina, Andrea)
- Date created
- Content (rich text/markdown)
- Type (theme, observation, external reference)
- Source (which codes/analysis it came from)
- Visibility (internal only vs. published to clients)
- Version history
```

**Created by**: Internal team as they work
**Viewed by**:
- Internal team: sees ALL insights (including unpublished)
- Clients: sees only insights marked "published"

**Key point**: This is the "living repository" Chloe described. Internal team can have working notes that clients never see. When ready, they mark insights as "published" and clients can view them.

---

### 5. **Client Licenses** (Who can see what)

```
License:
- Client ID (YWCA, other organizations)
- Trauma Graph ID (which graph they licensed)
- Access level (view-only)
- Start date
- End date / renewal date
- License tier (affects pricing, features)
```

**Controls**: What trauma graphs each client can view

---

### 6. **White Label Client Data** (YWCA's own data)

```
Client Program Data:
- Client ID (YWCA tenant)
- Program name
- Geography served (references shared geographic system)
- People served
- Data fields (custom per client)
- Date updated
```

**Owned by**: Client (YWCA)
**Managed by**: White Label product
**Isolated from**: Other clients (multi-tenant)

---

## Access Control: Who Sees What

This is critical for the "standardized language":

### **Internal Team (Chloe, Nina, Andrea, Allison)**
Full access to everything:
- ✅ All raw data (interviews, surveys, responses)
- ✅ All codes, themes, working notes
- ✅ All field notes
- ✅ All insights (published and unpublished)
- ✅ All trauma graphs (past, current, draft)
- ✅ All client data they collected (like YWCA impact survey)
- ✅ Can create, edit, delete everything
- ✅ Can publish trauma graphs
- ✅ Can mark insights as "client-facing"

### **Trauma Graph Client (Not YWCA, just licensing graph)**
Limited view:
- ✅ Can VIEW specific trauma graph(s) they licensed
- ✅ Can see published insights for those geographies
- ✅ Can see severity maps, color-coding
- ✅ Can see version history (what changed, when)
- ❌ Cannot see raw data (interviews, surveys, codes)
- ❌ Cannot see internal working notes
- ❌ Cannot see unpublished insights
- ❌ Cannot edit anything

### **White Label Client (YWCA)**
Own data + optional trauma graph:
- ✅ Can enter/edit their own data (programs, people served)
- ✅ Can query their own data
- ✅ Can generate reports from their data
- ❌ Cannot see other clients' data
- ❌ Cannot see 10Seven's raw research data
- **IF they license trauma graph:**
  - ✅ Can VIEW trauma graphs for their service areas
  - ✅ Side-by-side: their data + trauma graph
  - ❌ Still cannot see raw research data

---

## Key Architectural Questions (Need Team Input)

### **1. Geographic Standardization**

**Challenge**: Chloe finds maps from city websites. Not all neighborhoods have official boundaries.

**Options**:
- A) Build your own geographic reference system (maintain database of all geographies)
- B) Use existing (Census TIGER/Line, OpenStreetMap) where available, custom where needed
- C) Let each trauma graph define its own geographies (flexible but harder to link across graphs)

**Impacts**: How YWCA references geographies must match how 10Seven references them for side-by-side to work.

**Question for Monday**: How do you want to handle custom neighborhood boundaries that don't exist in official databases?

---

### **2. YWCA Impact Survey Data - Where Does It Live?**

**Situation**: 10Seven designed and collected YWCA Impact Survey from 167 local associations. That data exists now.

**Options**:
- A) **Import into YWCA white label** as baseline (YWCA owns it, so they can access it)
- B) **Keep in internal warehouse** (10Seven uses for research, YWCA re-enters into white label)
- C) **Dual storage** (lives in both, synced initially, then diverges as YWCA updates theirs)

**Impacts**:
- If A: YWCA starts with pre-populated data, easier for them
- If B: Clean separation, but YWCA has to re-enter everything
- If C: Maintains research record + gives YWCA access, but sync complexity

**Question for Monday**: Does YWCA's impact survey data get imported into their white label, or do they start fresh?

---

### **3. Trauma Graph Versioning & Updates**

**Challenge**: Chloe said they have "532 new survey responses we haven't added yet" to existing trauma graph.

**When internal team updates a published trauma graph**:
- Does it create a new version (v1.0 → v1.1)?
- Do clients with licenses automatically see updates?
- Or do they need to renew/upgrade license?

**Options**:
- A) **Living updates**: Clients always see latest version (trauma graph is continuously updated)
- B) **Versioned releases**: Each update creates new version, clients can choose when to upgrade
- C) **Time-based**: License includes updates for 1 year, then renewal required

**Impacts**: Affects licensing model and revenue structure

**Question for Monday**: Are trauma graphs "living" (clients always see latest) or "versioned" (clients get specific snapshot)?

---

### **4. Insight Visibility - Who Decides What's Published?**

**Challenge**: Internal team has working notes + published insights. How do you separate them?

**Options**:
- A) **Explicit publishing**: Chloe/team marks insights as "publish to clients" (like Medium drafts vs. published)
- B) **Automatic**: When trauma graph is published, all insights for that geography are included
- C) **Layered**: Some insights are "internal context," others are "client-facing summary"

**Current pain point from call**: Team currently texts articles to each other. They want to attach external data (NY Times articles) to geographies. Is that published to clients or internal only?

**Question for Monday**: How do you want to control which insights clients see vs. internal working notes?

---

### **5. Multi-Tenant Isolation (White Label)**

**Challenge**: Multiple clients (YWCA, future clients) each have own data. They must be isolated from each other.

**But**: They might license the same trauma graph (both serve St Paul).

**Data isolation**:
```
YWCA Tenant:
- YWCA's programs/data (isolated)
- Licensed trauma graphs (shared, read-only)

Future Client Tenant:
- Their own programs/data (isolated from YWCA)
- Licensed trauma graphs (shared, read-only - might be same St Paul graph)
```

**Architecture pattern**:
- Each white label client is a **separate tenant** (cannot see each other's data)
- Trauma graphs are **shared assets** (multiple tenants can license same graph)
- Need clear boundaries: tenant data vs. shared licensed data

**Question for Monday**: Do you expect multiple white label clients soon, or just YWCA for now? Affects how much multi-tenancy infrastructure to build upfront.

---

## Proposed Standardized Language

Based on everything above, here's the **common vocabulary** all three products should use:

### **Core Entities** (shared across all products):

1. **Geography** - Physical location (county, neighborhood, zip)
2. **Trauma Graph** - Published research asset covering specific geography
3. **Severity Level** - 1-4 scale for trauma intensity in a geography
4. **Insight** - Research finding or note attached to geography (can be published or internal)
5. **License** - Permission for client to view specific trauma graph
6. **Client/Tenant** - Organization using white label (YWCA, etc.)

### **Data Flow** (how products communicate):

1. **Internal Warehouse → Trauma Graph**: "Publish" action
   - Packages research into licensable asset
   - Marks insights as published/internal
   - Generates severity map
   - Versions it

2. **Trauma Graph → Client View**: "License" relationship
   - Client purchases access
   - Read-only view of published data
   - Geographic filtering (can only see geographies they're interested in)

3. **White Label ← → Trauma Graph**: "Geographic Link"
   - Client's data references geography
   - Trauma graph references same geography
   - System joins them for side-by-side view
   - Requires shared geographic reference system

4. **Internal Warehouse ← → White Label** (optional): "Data Import/Sync"
   - If YWCA impact survey data moves into white label
   - One-time or ongoing sync (TBD)

---

## Technical Communication Patterns

### **1. Internal Warehouse creates Trauma Graph**

When Chloe publishes St Paul trauma graph:

```
API call: publishTraumaGraph({
  geographyId: "stpaul-mn",
  geographicLevel: "neighborhood",
  dateRange: "2024-01-01 to 2024-12-31",
  includeInsights: [insightId1, insightId2, ...], // which insights are client-facing
  severityData: [
    {geographyId: "stpaul-neighborhoodX", severityLevel: 4, colorCode: "#8B0000"},
    {geographyId: "stpaul-neighborhoodY", severityLevel: 2, colorCode: "#FFA500"},
    ...
  ],
  version: "1.0",
  status: "published"
})

Result: Creates new Trauma Graph asset with ID "trauma-graph-stpaul-2024"
```

---

### **2. Client licenses Trauma Graph**

When YWCA purchases access:

```
API call: createLicense({
  clientId: "ywca-tenant",
  traumaGraphId: "trauma-graph-stpaul-2024",
  accessLevel: "view",
  startDate: "2025-01-01",
  endDate: "2025-12-31"
})

Result: Client "ywca-tenant" can now query trauma-graph-stpaul-2024 data
```

---

### **3. Client views side-by-side**

When YWCA user views neighborhood X:

```
White Label queries:
1. "Get my (YWCA) programs serving neighborhood X"
   → Returns: YWCA's own data

2. "Get trauma graph insights for neighborhood X"
   → Checks: Does this client have license to trauma graph covering neighborhood X?
   → If yes: Returns published insights + severity level
   → If no: Returns "Upgrade to view trauma graph data"

Display:
- Left: YWCA data
- Right: Trauma graph data (if licensed)
- Connected by: geographyId "stpaul-neighborhoodX"
```

---

## What Needs to Be Built (Shared Infrastructure)

For all three products to communicate, you need:

### **1. Geographic Reference Service**
- Maintains canonical list of all geographies
- API: `getGeography(id)`, `searchGeographies(query)`, `getChildGeographies(parentId)`
- Handles: counties, cities, neighborhoods, custom boundaries
- Provides: boundary data for mapping

### **2. Trauma Graph Registry**
- Maintains list of all published trauma graphs
- API: `getTraumaGraph(id)`, `publishTraumaGraph(data)`, `updateTraumaGraph(id, data)`
- Handles: versioning, status (draft/published/archived)
- Links to: geography, severity data, insights

### **3. Severity & Insights Repository**
- Stores severity assignments per geography per trauma graph
- Stores insights per geography (with published/internal flag)
- API: `getSeverity(traumaGraphId, geographyId)`, `getInsights(traumaGraphId, geographyId, visibilityLevel)`

### **4. License Management Service**
- Tracks which clients have access to which trauma graphs
- API: `checkLicense(clientId, traumaGraphId)`, `createLicense(data)`
- Used by: Client view to determine what they can see

### **5. Multi-Tenant Data Isolation**
- Each white label client is separate tenant
- Tenant data (YWCA programs) is isolated
- API: `getClientData(tenantId, dataType, filters)`
- Ensures: Client A cannot see Client B's data

---

## Summary: The Standardized Language

**All three products communicate through**:

1. **Shared Geographic Reference System**
   - Common IDs for all locations
   - Everyone uses same geography vocabulary

2. **Trauma Graph as Published Asset**
   - Created by Internal Warehouse
   - Licensed to Clients
   - Versioned and updateable

3. **Clear Access Boundaries**
   - Internal team: Full access
   - Trauma Graph clients: View published only
   - White label clients: Own data + licensed trauma graphs

4. **Geographic Linking**
   - YWCA data links to geography
   - Trauma graph links to same geography
   - System joins them for side-by-side view

5. **Visibility Flags**
   - Insights marked as "internal" or "published"
   - Controls what clients see

---

## Questions for Monday Meeting

To finalize the architecture, you need clarity on:

1. **Geographic standardization**: Census data + custom boundaries? How handle non-official neighborhoods?

2. **YWCA survey data**: Import into white label, or keep in warehouse only?

3. **Trauma graph updates**: Living (clients always see latest) or versioned (snapshot)?

4. **Insight publishing**: Explicit publish action, or automatic when graph published?

5. **Multi-tenancy priority**: Just YWCA for now, or expect multiple clients soon?

6. **White label complexity**: How simple should it really be? YWCA just needs basic queries, but do they need custom reports?

---

## Visual Summary

```
┌─────────────────────────────────────────────────────────────┐
│                    INTERNAL WAREHOUSE                        │
│  (Source of Truth - 10Seven Team Only)                      │
│                                                              │
│  • Surveys, Interviews, Raw Data                            │
│  • Qualitative Coding (highlight → code → themes)           │
│  • Quantitative Analysis (correlations, stats)              │
│  • Geographic Mapping (themes → neighborhoods)              │
│  • Severity Assignment (Level 1-4)                          │
│  • Insights Repository (published + internal)               │
│  • Field Notes, Working Notes, Version History              │
│                                                              │
│  WHEN READY: "Publish" Trauma Graph                         │
│         ↓                                                    │
└─────────┼────────────────────────────────────────────────────┘
          │
          │ Publish Action
          ↓
┌─────────────────────────────────────────────────────────────┐
│                      TRAUMA GRAPH                            │
│  (Published Asset - Clients License Access)                 │
│                                                              │
│  • Frozen snapshot of research                              │
│  • Geographic coverage (St Paul, National, etc.)            │
│  • Severity maps (color-coded 1-4)                          │
│  • Published insights only (internal notes hidden)          │
│  • Versioned (v1.0, v1.1, etc.)                            │
│  • Client access: View only, no raw data                    │
│                                                              │
│  ↙                                     ↘                     │
└─────────────────────────────────────────────────────────────┘
License to view                  License to view
    ↓                                    ↓
┌──────────────────┐            ┌──────────────────┐
│  TRAUMA GRAPH    │            │   WHITE LABEL    │
│  CLIENT          │            │   CLIENT (YWCA)  │
│                  │            │                  │
│  View only:      │            │  Two parts:      │
│  • Severity maps │            │                  │
│  • Insights      │            │  1. Own data:    │
│  • Version hist. │            │    • Programs    │
│                  │            │    • People      │
│  Cannot see:     │            │    • Buildings   │
│  • Raw data      │            │                  │
│  • Working notes │            │  2. Trauma graph │
│                  │            │     (if licensed)│
└──────────────────┘            │                  │
                                │  Side-by-side:   │
                                │  YWCA ← → Graph  │
                                │  (linked by      │
                                │   geography)     │
                                └──────────────────┘

SHARED FOUNDATION:
═══════════════════════════════════════════════════════════════
Geographic Reference System (counties, neighborhoods, zips)
- Internal Warehouse tags: "Interview from St Paul neighborhood X"
- Trauma Graph shows: "Severity 4 in neighborhood X"
- YWCA enters: "We serve 500 in neighborhood X"
- System links: Same geography ID connects all three
```

---

## Next Steps

Before Monday:
- Review this framework
- Identify questions or concerns
- Think about: Which architectural options feel right for 10Seven's needs?

During Monday:
- Get team input on 6 key questions
- Validate data flow assumptions
- Clarify YWCA white label complexity
- Confirm geographic standardization approach

After Monday:
- Finalize standardized language
- Create technical architecture diagrams
- Define API contracts between products
- Begin development planning
