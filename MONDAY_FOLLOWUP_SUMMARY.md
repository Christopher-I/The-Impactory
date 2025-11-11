# Monday Follow-Up Call - Key Changes Summary

**Date**: Monday follow-up call after Thursday's project pivot
**Status**: Major scope expansion confirmed

---

## 🔥 Critical New Requirements

### 1. Survey Builder Platform (COMPLETELY NEW)
- **Replace Qualtrics entirely**
- Build custom survey creation tool
- Skip logic (conditional questions)
- Data collection + export
- Goal: "All in one place" - stop using multiple platforms

### 2. Enhanced Quantitative Analysis (MUCH MORE IMPORTANT)
- Stats IQ-level analysis (correlations, p-values, significance testing)
- Cross-tabulation (demographics + geography)
- Correlation matrices
- **90% of visualizations are TABLES** (not fancy charts)
- Comparable to SPSS/R for advanced analysis

### 3. Target Audiences Clarified
- **B2B**: Think tanks, government bodies, nonprofits
- **B2C**: Researchers, financial advisors
- **PARENTS = HUGE NEW MARKET** ⭐
  - Most common inquiry
  - Started in K-12 financial education
  - Massive untapped potential

### 4. Map Technology & Features Finalized
- **Mapbox confirmed** (Chloe loves it)
- **Event-based filters (NEW)**: Time periods, policy events, historical periods
- **Two-tier premium model**:
  - Vector 1: Static vs Dynamic maps
  - Vector 2: Basic vs Multidimensional overlays
- **Granularity = premium feature**

### 5. Marketing Strategy
- **DON'T market white label** publicly (except Ed Hub)
- **DO market trauma graph licensing** (primary product)
- White label only when client requests it

### 6. Trial Licensing (NEW)
- 14-day access codes at conferences
- Lead generation from speaking engagements
- Discount for post-trial licenses

### 7. Mobile Apps Confirmed
- All products likely need mobile versions
- Impacts tech stack significantly
- Firebase stronger for mobile OR hybrid approach

---

## Impact on Project

### Complexity:
- **Was**: 7/10
- **Now**: 8/10 (survey builder + enhanced quant + mobile)

### Risk:
- **Was**: 4/10
- **Now**: 4.5/10 (slightly higher due to expanded scope)

### Tech Stack Recommendation:
- **Supabase** for internal warehouse (PostgreSQL for geo + stats + version history + CLI workflow)
- **Mapbox** for maps (confirmed)
- **Mobile**: Hybrid (Supabase internal, Firebase mobile) OR Supabase + React Native

---

## What's Being Built

**Before Monday**: Research platform with qual coding + maps

**After Monday**: **Complete replacement of their entire tool stack**

Replace:
- ❌ Qualtrics → ✅ Custom survey builder
- ❌ Max QDA → ✅ Collaborative qual coding
- ❌ SPSS/R → ✅ Integrated quant analysis
- ❌ Adobe Illustrator → ✅ Automated Mapbox maps
- ❌ Siloed tools → ✅ ONE integrated platform

---

## Key Quotes

**Chloe on Integration**:
> "If all of that was in one place for us, that would be a huge game changer, huge."

**Chloe on Survey Builder**:
> "I would honestly love to get away from another platform. It is literally a survey where people are inputting their answers."

**Chloe on White Label Marketing**:
> "Do I think we're going to get a lot of YWCA clients? No... people are going to stop at the trauma graph, like, that's really what they want."

**Chris on Granularity**:
> "The further down you can go in detail, sounds like that's of high value?"

**Chloe**: "Big time."

---

## Next Steps

1. **Explore Qualtrics** (Nina sending login)
2. **Finalize tech stack** decision
3. **Create alignment doc** for client
4. **Prepare proposal** (cost, timeline, roadmap)
5. **Travel**: Nov 28 - Dec 9 (email only)

---

## Bottom Line

**What changed**: Project scope expanded significantly. Not just qual coding + maps anymore. Now building complete end-to-end research platform: surveys → qual → quant → maps → licensing.

**Why it matters**: This positions 10Seven to completely replace their tool stack and own their entire workflow. Much larger opportunity, but also more complex build.

**Feasibility**: Still very feasible (8/10 complexity), nothing exotic, but more time required.

**Business case**: Even stronger - solving more pain points, replacing more expensive subscriptions, "game changer" for their workflow.
