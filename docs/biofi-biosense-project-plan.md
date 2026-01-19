# BioFi / BioSense Project Plan

**Client**: Jay @ bio.xyz  
**Developer**: Matthew Berryhill  
**Date**: January 19, 2025  
**Rate**: $125/hour  

---

## Executive Summary

BioFi is a Web3 e-commerce platform that enables DAOs to sell direct-to-consumer biohacking and supplementation products. The first client is **DERMA DAO**, a Korean skincare DAO launching their beauty brand.

Jay wants to build **BioSense** - an AI-powered content marketing system that acts as a "virtual sales rep" for brands. The system creates AI personas that generate and distribute short-form video content (primarily TikTok).

### The Two Pillars

| Pillar | Goal | System Responsibility |
|--------|------|----------------------|
| 🎯 **ATTENTION** | Get eyeballs on content | AI generates & distributes viral content |
| 💰 **CONVERSION** | Turn viewers into buyers | Track the funnel; product story does the selling |

**Key Insight**: Attention is primary (~70% of effort). Conversion is tracked but the product's unique ingredients and story handle the actual selling.

**Priority**: Speed over perfection. Get content distributing immediately and refine the system in parallel.

**Timeline**: First 5+ videos live on TikTok by end of January 2025.

---

## What The Client Wants

### The Core Concept

An AI agent system that:
1. **Researches** what content is working in the biohacking/skincare space
2. **Generates** video content through multiple AI "personas" (virtual influencers)
3. **Distributes** content to TikTok (and potentially other platforms)
4. **Analyzes** performance and optimizes strategies

### The Multi-Persona Strategy

Jay wants to test multiple strategies simultaneously:
- Create ~10 TikTok accounts, each with a different AI persona
- Example personas mentioned:
  - Fitness persona
  - Female model persona
  - Skincare mom persona
- Test which strategies gain traction
- Fold failing strategies, double down on winners
- Continuously iterate with new personas

### How Jay Described It

> "BioFi will become, it will be like a sales rep, in a way... meaning that it should create attention"

> "The conversion should happen from the ingredients, or a story of DERMA DAO... the skincare has a chemical compound called ABC. ABC has been using by Jennifer Lopez... and then the conversion and the checkout should be leading directly to BioFi"

---

## The Attention → Conversion Model

Jay clearly distinguished between two separate goals with different responsibilities:

### 1. ATTENTION (Primary Goal - What BioSense Does)

The AI system's **primary job is to generate attention** - getting eyeballs on content.

- Create viral/engaging short-form video content
- Optimize for views, watch time, engagement
- Test multiple personas and strategies to find what gets traction
- The content doesn't need to hard-sell; it needs to **capture interest**

> "It should create attention, I think that's probably is the most important thing"

**KPIs for Attention**:
- Views
- Watch time / completion rate
- Likes, comments, shares
- Follower growth
- Reach / impressions

### 2. CONVERSION (Secondary Goal - Product Does the Selling)

Conversion is handled by the **product story and unique value proposition**, not the AI content.

Jay's insight: The AI content creates curiosity, but the **product's unique ingredients and story** close the sale.

> "The conversion should happen from the ingredients, or a story of DERMA DAO... it should be good at converting, it doesn't have to be the greatest, but it should be good at converting, but attention is the most important thing"

**The Conversion Flow**:
```
AI Content (Attention) → User Curiosity → Product Page (Story/Ingredients) → Purchase
```

**Example from Jay**:
> "The skincare has a chemical compound called ABC. You know, ABC has been using by Jennifer Lopez... and then the conversion and the checkout should be leading directly to... DERMA DAO. You can sort of shop it at BioFi"

**KPIs for Conversion**:
- Click-through rate to BioFi
- Add to cart rate
- Purchase conversion rate
- Revenue per video/persona

### Why This Distinction Matters

This changes how we build and measure the system:

| Aspect | Attention Focus | Conversion Focus |
|--------|-----------------|------------------|
| Content Style | Entertaining, hook-driven, viral | Educational, trust-building |
| Optimization Target | Views, engagement | CTR, purchases |
| Iteration Speed | Fast - test many strategies | Slower - refine messaging |
| Success Metric | Did people watch? | Did people buy? |

**For MVP**: Focus heavily on attention. Track conversion, but don't over-optimize for it yet. Prove the attention model works first, then refine the conversion funnel.

---

## System Architecture Overview

Organized by the two pillars:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         BioSense Platform                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ╔═══════════════════════════════════════════════════════════════════════╗  │
│  ║                    🎯 ATTENTION PILLAR                                ║  │
│  ╠═══════════════════════════════════════════════════════════════════════╣  │
│  ║                                                                       ║  │
│  ║  1. LISTENING LAYER                                                   ║  │
│  ║     - Scrape TikTok for trending biohacking/skincare content         ║  │
│  ║     - Identify winning content patterns and hooks                     ║  │
│  ║     - Track competitor/influencer strategies                          ║  │
│  ║                                                                       ║  │
│  ║  2. PERSONA/STRATEGY LAYER                                            ║  │
│  ║     - AI agents for each brand persona (fitness, skincare mom, etc.) ║  │
│  ║     - Knowledge base with strategy rules (MD/PDF)                     ║  │
│  ║     - Multiple strategies running in parallel                         ║  │
│  ║                                                                       ║  │
│  ║  3. CONTENT GENERATION LAYER                                          ║  │
│  ║     - AI generates video scripts/content per persona                  ║  │
│  ║     - Integration with video tools (HeyGen, D-ID, etc.)              ║  │
│  ║     - "Turn trending content into our version"                        ║  │
│  ║                                                                       ║  │
│  ║  4. DISTRIBUTION LAYER                                                ║  │
│  ║     - Post to TikTok (primary)                                        ║  │
│  ║     - Manage multiple accounts (~10 personas)                         ║  │
│  ║     - Scheduling and automation                                       ║  │
│  ║                                                                       ║  │
│  ║  5. ATTENTION ANALYTICS                                               ║  │
│  ║     - Track: views, watch time, engagement, follower growth          ║  │
│  ║     - A/B test personas and strategies                                ║  │
│  ║     - Identify winners, fold losers, iterate                          ║  │
│  ║                                                                       ║  │
│  ╚═══════════════════════════════════════════════════════════════════════╝  │
│                                    │                                        │
│                                    ▼                                        │
│  ╔═══════════════════════════════════════════════════════════════════════╗  │
│  ║                    💰 CONVERSION PILLAR                               ║  │
│  ╠═══════════════════════════════════════════════════════════════════════╣  │
│  ║                                                                       ║  │
│  ║  6. CONVERSION TRACKING                                               ║  │
│  ║     - Track clicks from TikTok → BioFi                               ║  │
│  ║     - UTM parameters per persona/video                                ║  │
│  ║     - Attribution: which content drives purchases                     ║  │
│  ║                                                                       ║  │
│  ║  7. CONVERSION ANALYTICS                                              ║  │
│  ║     - Track: CTR, add-to-cart, purchases, revenue                    ║  │
│  ║     - Revenue per persona/strategy                                    ║  │
│  ║     - Funnel analysis: where do users drop off?                       ║  │
│  ║                                                                       ║  │
│  ║  Note: Actual conversion happens on BioFi via product story          ║  │
│  ║  and unique ingredients - not optimized by this system               ║  │
│  ║                                                                       ║  │
│  ╚═══════════════════════════════════════════════════════════════════════╝  │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## MVP vs Full System

### Option A: MVP (Recommended to Start)

**Scope**:
- Backend only - no front-end dashboard
- Strategy defined via MD/PDF knowledge documents
- 10 TikTok accounts with different AI personas
- Manual/semi-automated content generation
- Basic analytics tracking

**Goal**: First 5 strategy videos distributed by **end of January 2025**

**Approach**: 
> "Even though it's a bad strategy, at least we will put in something... if it do very well in the next three to four weeks and it has some hits, that it's sort of proven strategy that this is working"

### Option B: Full System (Future Phase)

**Additional Scope**:
- Front-end platform for DAO owners
- Self-service persona creation and management
- Automated strategy optimization
- Multi-tenant support for different DAOs/products
- Advanced analytics dashboard

---

## Division of Responsibilities

### Matt (Software Development)

| Component | Description |
|-----------|-------------|
| Social Listening System | Scraping/monitoring for trending content |
| AI Persona Agents | Building the agents that represent brand personas |
| Content Generation Pipeline | Integration with video generation tools |
| Distribution Automation | TikTok API integration, scheduling |
| Analytics Infrastructure | Tracking, conversion monitoring, performance analysis |
| Strategy Optimization AI | System that analyzes what's working |
| System Architecture | Overall design and implementation |

### Hyke (Supporting Role)

| Component | Description |
|-----------|-------------|
| Video Production Expertise | Advising on video generation approaches |
| Bandwidth Support | Available to help in the 2-4 week window |
| Tool Integration | Potentially helping with video tool integrations |

Jay stated:
> "Hike could come in and help us in this project with the video part of things, so it just not just be, like, you and your efforts. I think Hike will also have bandwidth in the upcoming two to four weeks to help support this."

---

## Task Breakdown: Organized by Pillars

All work is organized around the two core pillars: **ATTENTION** and **CONVERSION**.

### 🎯 PILLAR 1: ATTENTION (Primary Focus)

Everything that drives eyeballs to content.

#### Phase A1: Attention Infrastructure (Week 1)

| Task | Estimated Hours | Purpose |
|------|-----------------|---------|
| Research trending content patterns in biohacking/skincare | 3-4 hrs | Understand what gets attention |
| Research video generation tools (HeyGen, D-ID, etc.) | 3-4 hrs | How we create attention-grabbing content |
| Research TikTok API / distribution options | 2-3 hrs | How we distribute content at scale |
| Define persona templates (fitness, skincare mom, etc.) | 3-4 hrs | Multiple angles to capture attention |
| Create strategy knowledge base (MD/PDF docs) | 2-3 hrs | Document what works |

**Deliverable**: Clear understanding of attention landscape and tool decisions

#### Phase A2: Attention Engine Build (Weeks 1-2)

| Task | Estimated Hours | Purpose |
|------|-----------------|---------|
| Build AI persona agent system | 8-12 hrs | Core engine that creates persona-based content |
| Integrate video generation tool(s) | 6-10 hrs | Produce actual video content |
| Build TikTok distribution pipeline | 6-8 hrs | Get content in front of eyeballs |
| Create first 3-5 persona configurations | 4-6 hrs | Multiple strategies running in parallel |
| Set up content scheduling/automation | 3-4 hrs | Consistent posting cadence |

**Deliverable**: Working pipeline: Persona → Content → TikTok

#### Phase A3: Attention Deployment (Weeks 2-3)

| Task | Estimated Hours | Purpose |
|------|-----------------|---------|
| Generate first batch of content (5+ videos) | 4-6 hrs | Initial content library |
| Deploy to TikTok accounts | 2-4 hrs | Go live |
| Monitor posting and debug issues | 4-6 hrs | Ensure content is reaching audience |
| Iterate on content hooks/formats | 6-10 hrs | Improve attention capture |

**Deliverable**: First 5+ videos live, generating views

#### Phase A4: Attention Optimization (Weeks 3-4+)

| Task | Estimated Hours | Purpose |
|------|-----------------|---------|
| Build attention analytics dashboard | 4-6 hrs | Track views, watch time, engagement |
| Implement A/B testing for personas | 4-6 hrs | Find winning strategies |
| Scale to 10 personas/accounts | 6-8 hrs | More experiments = more learning |
| Build strategy iteration logic | 4-6 hrs | Auto-identify what's working |

**Deliverable**: Data-driven attention optimization loop

---

### 💰 PILLAR 2: CONVERSION (Secondary Focus)

Everything that turns attention into purchases.

#### Phase C1: Conversion Tracking Setup (Week 2)

| Task | Estimated Hours | Purpose |
|------|-----------------|---------|
| Research conversion tracking options (Segment, etc.) | 2-3 hrs | Understand tracking landscape |
| Implement click tracking (TikTok → BioFi) | 3-4 hrs | Know where traffic comes from |
| Set up UTM parameters per persona/video | 2-3 hrs | Attribution by content |
| Integrate with BioFi analytics (if exists) | 2-4 hrs | End-to-end funnel visibility |

**Deliverable**: Basic conversion tracking in place

#### Phase C2: Conversion Analysis (Weeks 3-4)

| Task | Estimated Hours | Purpose |
|------|-----------------|---------|
| Build conversion analytics views | 3-4 hrs | CTR, add-to-cart, purchases by source |
| Analyze attention → conversion correlation | 2-3 hrs | Which attention strategies convert? |
| Identify conversion optimization opportunities | 2-3 hrs | Where is the funnel leaking? |
| Document product story/ingredient hooks | 2-3 hrs | What messaging drives conversion |

**Deliverable**: Understanding of what converts and why

#### Phase C3: Conversion Optimization (Week 4+)

| Task | Estimated Hours | Purpose |
|------|-----------------|---------|
| Optimize CTA placement in content | 3-4 hrs | Better handoff to product page |
| Test different conversion hooks | 3-4 hrs | Ingredient stories, social proof, etc. |
| Implement revenue-per-persona tracking | 2-3 hrs | True ROI by strategy |
| Recommend landing page improvements | 2-3 hrs | Improve BioFi conversion rate |

**Deliverable**: Conversion rate improvements and ROI visibility

---

## Time Estimates Summary

### By Pillar

| Pillar | Phase | Estimated Hours | Target |
|--------|-------|-----------------|--------|
| **ATTENTION** | A1: Infrastructure | 13-18 hrs | End of Week 1 |
| **ATTENTION** | A2: Engine Build | 27-40 hrs | End of Week 2 |
| **ATTENTION** | A3: Deployment | 16-26 hrs | End of Week 3 |
| **ATTENTION** | A4: Optimization | 18-26 hrs | Week 4+ |
| **CONVERSION** | C1: Tracking Setup | 9-14 hrs | Week 2 |
| **CONVERSION** | C2: Analysis | 9-13 hrs | Weeks 3-4 |
| **CONVERSION** | C3: Optimization | 10-14 hrs | Week 4+ |

### Totals

| Focus Area | Total Hours | % of Effort |
|------------|-------------|-------------|
| **ATTENTION** | 74-110 hrs | ~70% |
| **CONVERSION** | 28-41 hrs | ~30% |
| **TOTAL** | **102-151 hours** | 100% |

**MVP Target**: Weeks 1-3 (~75-90 hours) = Content live + basic tracking

**Note**: Attention is the primary focus because:
1. Jay explicitly said attention is "the most important thing"
2. Can't optimize conversion without traffic first
3. Product story/ingredients handle much of the conversion work

---

## Weekly Milestones

| Week | Focus | Key Deliverable | Success Metric |
|------|-------|-----------------|----------------|
| **Week 1** | Attention Infrastructure | Tools selected, personas defined | Ready to build |
| **Week 2** | Attention Engine + Conversion Tracking | Pipeline working, tracking in place | Can generate & post content |
| **Week 3** | Deployment | 5+ videos live on TikTok | Content getting views |
| **Week 4** | Optimization | Data-driven iteration | Know what's working |

---

## Risk Assessment (by Pillar)

### Attention Risks

| Risk | Impact | Likelihood | Mitigation |
|------|--------|------------|------------|
| TikTok API restrictions | High | Medium | Research alternatives, manual posting fallback |
| Video generation quality | High | Medium | Test multiple tools early, Hyke advises |
| Account bans (multi-account) | High | Medium | Stagger creation, follow TOS |
| Content not gaining traction | Medium | Medium | Expected - system designed to iterate |
| Algorithm changes | Medium | Low | Diversify personas and strategies |

### Conversion Risks

| Risk | Impact | Likelihood | Mitigation |
|------|--------|------------|------------|
| Can't track attribution properly | Medium | Medium | Use UTM params, Segment fallback |
| Low conversion despite attention | Medium | High | Product story handles conversion, not content |
| BioFi site issues | Medium | Low | Flag to Jay, outside our scope |
| Scope creep into full e-commerce | Low | Medium | Stay focused on content → click tracking |

---

## Key Questions to Clarify (by Pillar)

### 🎯 Attention Questions

1. **Platform scope**: Is TikTok the only platform for MVP, or should we plan for Instagram Reels/YouTube Shorts from the start?

2. **Video generation**: Any preferred tools already in use or researched? (e.g., HeyGen, Synthesia, D-ID, custom)

3. **Content type**: Full AI-generated videos, or AI scripts with stock footage, or talking head avatars?

4. **DERMA DAO assets**: What product info, images, branding assets are available?

5. **Account management**: Who creates/owns the TikTok accounts? How do we handle credentials?

### 💰 Conversion Questions

6. **Conversion tracking**: Is there existing analytics on BioFi, or do we need to set this up?

7. **Product page**: Is the DERMA DAO product page ready with the ingredient story and conversion messaging?

8. **Success metrics**: What conversion rate would be considered successful for this MVP?

---

## Recommended Next Steps

### Immediate (Before Starting)
1. Confirm MVP scope and answer key questions above
2. Get DERMA DAO product assets and messaging

### Week 1: Attention Foundation
3. Set up project infrastructure
4. Research and select video generation tools
5. Define first 3-5 persona strategies
6. Begin building persona agent system

### Week 2: Build + Track
7. Complete attention engine (content generation + distribution)
8. Set up conversion tracking (UTMs, click tracking)
9. Generate first batch of content

### Week 3: Go Live
10. Deploy first 5+ videos to TikTok
11. Monitor attention metrics (views, engagement)
12. Begin tracking conversion funnel

### Week 4+: Optimize Both Pillars
13. Analyze what's working (attention) and what converts (conversion)
14. Scale winning strategies, fold losers
15. Iterate and improve

---

## Engagement Terms

- **Rate**: $125/hour
- **Billing**: Time and materials (not fixed scope)
- **Approach**: Agile/iterative with weekly check-ins
- **Communication**: Regular updates on progress vs. goals
- **Flexibility**: Scope can adjust as we learn what works

### Weekly KPI Check-ins

| Week | Attention KPIs | Conversion KPIs |
|------|----------------|-----------------|
| Week 1 | Tools selected, personas defined | Tracking plan ready |
| Week 2 | Pipeline working | Tracking implemented |
| Week 3 | Videos live, views coming in | Click-throughs tracked |
| Week 4 | Winning strategies identified | ROI per persona visible |

Per the call:
> "I would prefer to not waste a lot of time on like scope and philosophy and just get going... I like to eliminate any speed bumps or friction, but make sure we have, let's say, ongoing KPI, another indicator that says, hey, we're moving the right direction"

---

## Appendix: Potential Tech Stack (To Be Validated)

### 🎯 Attention Stack

| Component | Options to Explore |
|-----------|-------------------|
| AI Persona Agents | Custom (leverage existing platform agent), LangChain, CrewAI |
| Video Generation | HeyGen, Synthesia, D-ID, Runway, custom pipelines |
| Content Scheduling | Buffer, Later, custom automation |
| Distribution | TikTok API, third-party schedulers, manual posting |
| Attention Analytics | TikTok native analytics, custom dashboard |
| Knowledge Base | Markdown files, vector DB for retrieval |

### 💰 Conversion Stack

| Component | Options to Explore |
|-----------|-------------------|
| Click Tracking | UTM parameters, link shorteners with tracking |
| Attribution | Segment, Mixpanel, custom tracking |
| Conversion Analytics | BioFi native analytics, custom dashboard |
| Funnel Analysis | Segment, Amplitude, custom |

### Infrastructure

| Component | Options to Explore |
|-----------|-------------------|
| Compute | Cloud functions, containerized services |
| Storage | S3/GCS for video assets |
| Database | PostgreSQL, MongoDB for analytics data |

---

*Document created: January 19, 2025*
*Next update: After kickoff alignment call*
