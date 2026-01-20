# BioFi / BioSense Project Plan

**Client**: Jay @ bio.xyz  
**Developer**: Matthew Berryhill  
**Date**: January 19, 2025  
**Rate**: $125/hour  

---

## Executive Summary

**This MVP is a Proof of Value (POV)** - the beginning of a larger initiative, not the end product. The goal is to validate the approach quickly and learn what works before investing in a full-scale system.

BioFi is a Web3 e-commerce platform that enables DAOs to sell direct-to-consumer biohacking and supplementation products. The first client is **DERMA DAO**, a Korean skincare DAO launching their beauty brand.

Jay wants to build **BioSense** - a content marketing system where AI personas act as both **sales reps** and **brand ambassadors** through short-form video content (primarily TikTok).

### The AI Persona: Sales Rep + Brand Ambassador

| Role | Focus | Content Style |
|------|-------|---------------|
| **Brand Ambassador** | Build awareness & trust | Educational, entertaining, story-driven |
| **Sales Rep** | Drive conversions | Product highlights, CTAs, links to BioFi |

Most content is brand ambassador style (80%) with sales moments woven in naturally (20%).

### The Two Pillars

| Pillar | Goal | System Responsibility |
|--------|------|----------------------|
| 🎯 **ATTENTION** | Get eyeballs on content | Research trends, distribute content, track engagement |
| 💰 **CONVERSION** | Turn viewers into buyers | Track the funnel; product story does the selling |

### Division of Labor

| Person | Role | Focus |
|--------|------|-------|
| **Hyke** | Video Production | Creates the actual video content for each persona |
| **Matt** | Systems & Automation | Builds tools to support Hyke: research, distribution, analytics |

**Matt's Value**: Connect systems together to speed up Hyke's work via low-hanging fruit automation - NOT building full AI video generation.

**MVP Focus**: 1 persona/strategy first. Scale to multiple personas after MVP proves out.

**MVP Includes**: Backend automation only. **No front-end dashboard**. Integrating with upstream AI/automation services.

**Priority**: Speed over perfection. Get content distributing and iterate.

**Timeline**: ~5 weeks to MVP complete (first videos live + learnings)

**Estimated Hours**: 90-130 hours (Matt's systems work)

---

## What The Client Wants

### The Core Concept

A content marketing system that:
1. **Researches** what content is working in the biohacking/skincare space (Matt automates)
2. **Produces** video content through multiple "personas" (Hyke creates)
3. **Distributes** content to TikTok and potentially other platforms (Matt automates)
4. **Analyzes** performance and optimizes strategies (Matt builds analytics)

### The Multi-Persona Strategy (Future Vision)

Jay's long-term vision is to test multiple strategies simultaneously:
- Create multiple TikTok accounts, each with a different persona
- Example personas mentioned:
  - Fitness persona
  - Female model persona
  - Skincare mom persona
- Test which strategies gain traction
- Fold failing strategies, double down on winners
- Continuously iterate with new personas

**Note**: This is the future vision. MVP starts with **1 persona** to prove the system works.

Each persona embodies both roles:

| Persona | Brand Ambassador Content | Sales Rep Content |
|---------|-------------------------|-------------------|
| Fitness persona | Workout tips, wellness advice, biohacking education | "This ingredient helped my recovery..." |
| Female model persona | Skincare routines, beauty tips, lifestyle | "The secret ingredient in my routine..." |
| Skincare mom persona | Family wellness, natural products, ingredient education | "Why I switched to DERMA DAO for my family..." |

### The AI Persona Concept: Sales Rep + Brand Ambassador

Jay described the personas as acting like both a **sales rep** and a **brand ambassador**:

> "BioFi will become, it will be like a sales rep, in a way... meaning that it should create attention"

#### Sales Rep Role
- **Goal**: Drive traffic and conversions to BioFi
- **Behavior**: Highlights product benefits, includes CTAs, links to product pages
- **Metric**: Conversion rate, revenue generated

#### Brand Ambassador Role
- **Goal**: Build awareness and trust for DERMA DAO
- **Behavior**: Shares the brand story, educates about unique ingredients, builds community
- **Metric**: Follower growth, engagement, brand sentiment

#### How They Work Together

The persona is NOT just a hard-sell salesperson. It's a trusted voice that:
1. **Educates** about biohacking/skincare (Brand Ambassador)
2. **Entertains** with engaging content (Brand Ambassador)
3. **Builds curiosity** about unique ingredients (Brand Ambassador → Sales Rep)
4. **Guides to purchase** when the viewer is ready (Sales Rep)

> "The conversion should happen from the ingredients, or a story of DERMA DAO... the skincare has a chemical compound called ABC. ABC has been using by Jennifer Lopez... and then the conversion and the checkout should be leading directly to BioFi"

**Key Insight**: The "brand ambassador" content creates the attention and trust. The "sales rep" role converts that attention into purchases. Most content should be brand ambassador style (entertaining, educational) with sales rep moments woven in naturally.

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

Organized by the two pillars, with clear separation of Hyke's work (video production) and Matt's work (systems/automation):

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         BioSense Platform                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ╔═══════════════════════════════════════════════════════════════════════╗  │
│  ║                    🎯 ATTENTION PILLAR                                ║  │
│  ╠═══════════════════════════════════════════════════════════════════════╣  │
│  ║                                                                       ║  │
│  ║  1. RESEARCH/LISTENING [MATT]                                         ║  │
│  ║     - Scrape TikTok for trending biohacking/skincare content         ║  │
│  ║     - Surface winning content patterns to inform Hyke                 ║  │
│  ║     - Track competitor/influencer strategies                          ║  │
│  ║                                                                       ║  │
│  ║  2. PERSONA/STRATEGY [MATT + HYKE]                                    ║  │
│  ║     - Define persona templates and strategy docs                      ║  │
│  ║     - Knowledge base with strategy rules (MD/PDF)                     ║  │
│  ║     - Multiple strategies to test in parallel                         ║  │
│  ║                                                                       ║  │
│  ║  3. VIDEO PRODUCTION [HYKE - PRIMARY]                                 ║  │
│  ║     - Hyke creates the actual video content                           ║  │
│  ║     - NOT fully AI-generated - human creative work                    ║  │
│  ║     - Matt provides supporting automation where helpful               ║  │
│  ║                                                                       ║  │
│  ║  4. DISTRIBUTION [MATT]                                               ║  │
│  ║     - Automate posting to TikTok                                      ║  │
│  ║     - MVP: 1 account only                                             ║  │
│  ║     - Scheduling and content queue management                         ║  │
│  ║                                                                       ║  │
│  ║  5. ATTENTION ANALYTICS [MATT]                                        ║  │
│  ║     - Track: views, watch time, engagement, follower growth          ║  │
│  ║     - Surface insights to guide Hyke's content strategy               ║  │
│  ║     - Identify winners, fold losers, iterate                          ║  │
│  ║                                                                       ║  │
│  ╚═══════════════════════════════════════════════════════════════════════╝  │
│                                    │                                        │
│                                    ▼                                        │
│  ╔═══════════════════════════════════════════════════════════════════════╗  │
│  ║                    💰 CONVERSION PILLAR                               ║  │
│  ╠═══════════════════════════════════════════════════════════════════════╣  │
│  ║                                                                       ║  │
│  ║  6. CONVERSION TRACKING [MATT]                                        ║  │
│  ║     - Track clicks from TikTok → BioFi                               ║  │
│  ║     - UTM parameters per persona/video                                ║  │
│  ║     - Attribution: which content drives purchases                     ║  │
│  ║                                                                       ║  │
│  ║  7. CONVERSION ANALYTICS [MATT]                                       ║  │
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

### Matt's Focus: Automation & Systems to Support Hyke

The goal is to **remove friction from Hyke's workflow** through:

1. **Automated Research**: Hyke shouldn't have to manually hunt for trending content
2. **Automated Distribution**: Hyke shouldn't have to manually post content
3. **Automated Analytics**: Easy visibility into what's working
4. **Content Pipeline**: Smooth handoff from Hyke's videos → scheduled posting

---

## Scope: MVP (1 Persona)

This engagement covers the **MVP phase only**. Future phases will require separate scoping.

### MVP Scope (This Engagement)

- **1 TikTok account** with 1 persona strategy
- **No front-end** - backend/automation only
- **Integration-based** - leveraging upstream AI/automation services (not building custom AI infrastructure)
- Strategy defined via MD/PDF knowledge documents
- Automated distribution pipeline
- Basic analytics tracking

### Technical Approach

Matt will integrate with existing upstream services for AI agent infrastructure rather than building custom AI systems from scratch. This includes:
- Third-party social listening/scraping tools (e.g., Apify)
- Existing scheduling/distribution platforms
- Analytics platforms (Segment, etc.)
- Matt's existing agent platform for research automation

**This keeps scope focused on integration and orchestration, not building AI from scratch.**

**Goal**: First videos from 1 persona distributed by **end of January 2025**

**Why 1 Strategy First**:
1. Faster to launch - less complexity
2. Learn what works before scaling
3. Prove the pipeline works end-to-end
4. Reduce Hyke's initial workload
5. Get data to inform which strategies to add next

**Approach**:
> "Even though it's a bad strategy, at least we will put in something... if it do very well in the next three to four weeks and it has some hits, that it's sort of proven strategy that this is working"

---

### Future Phases (Not Scoped - Requires Separate Engagement)

**Scale Phase**: Expand to additional personas/accounts, multi-account automation, strategy comparison

**Full System**: Front-end dashboard, self-service persona management, multi-tenant support

---

## Division of Responsibilities

### Hyke (Video Production - Primary Content Creator)

| Component | Description |
|-----------|-------------|
| **Video Production** | Creates the actual video content |
| **Persona Visuals** | Designs how each persona looks/sounds |
| **Content Creation** | Produces videos for each persona strategy |
| **Creative Direction** | Determines what content will capture attention |

**Key Point**: Hyke handles video generation. The videos are NOT expected to be fully AI-generated - Hyke creates the actual content.

### Matt (Software Development - Systems & Automation)

Your role is to **connect systems together to speed up Hyke's work** via low-hanging fruit automation.

| Component | Description |
|-----------|-------------|
| **Social Listening/Research** | Scrape/monitor TikTok for trending content patterns to inform Hyke's content strategy |
| **Distribution Automation** | TikTok API integration, scheduling, multi-account posting |
| **Analytics Infrastructure** | Tracking views, engagement, conversions |
| **Strategy Analysis** | AI that analyzes what's working vs. not |
| **Workflow Automation** | Connect tools to speed up Hyke's production pipeline |
| **Content Pipeline** | Manage content queue, scheduling, posting workflow |

**Low-Hanging Fruit Focus**:
- Automate the research → Hyke doesn't have to manually find trending content
- Automate distribution → Hyke doesn't have to manually post content
- Automate analytics → Easy visibility into what's working
- Automate scheduling → Content goes out consistently

Jay stated:
> "Hike could come in and help us in this project with the video part of things, so it just not just be, like, you and your efforts. I think Hike will also have bandwidth in the upcoming two to four weeks to help support this."

---

## Task Breakdown: Organized by Pillars

All work is organized around the two core pillars: **ATTENTION** and **CONVERSION**.

**Key**: Matt builds systems/automation. Hyke creates video content.

**MVP Focus**: 1 persona/strategy first. Scale to multiple personas after MVP proves out.

### 🎯 PILLAR 1: ATTENTION (Primary Focus)

Everything that drives eyeballs to content.

#### Phase A1: Research & Strategy Setup (Week 1)

| Task | Estimated Hours | Owner | Purpose |
|------|-----------------|-------|---------|
| Research TikTok API / distribution options | 2-3 hrs | Matt | How to automate posting |
| Build trending content scraper/monitor | 4-6 hrs | Matt | Surface trends for Hyke |
| **Define 1 MVP persona with Hyke** | 2-3 hrs | Matt + Hyke | Pick the best starting strategy |
| Create strategy knowledge base (MD/PDF docs) | 2-3 hrs | Matt | Document the MVP persona rules |
| Set up project infrastructure | 2-3 hrs | Matt | Dev environment, repos |

**Deliverable**: MVP persona defined, research tools working, ready to build distribution

#### Phase A2: Distribution & Pipeline Build (Weeks 1-2)

| Task | Estimated Hours | Owner | Purpose |
|------|-----------------|-------|---------|
| Build TikTok distribution automation | 4-6 hrs | Matt | Post to 1 account automatically |
| Build content queue/scheduling system | 3-4 hrs | Matt | Manage when content goes out |
| Create upload workflow for Hyke | 3-4 hrs | Matt | Easy handoff: Hyke's videos → system |
| Test distribution pipeline | 2-3 hrs | Matt | Ensure posting works reliably |

**Deliverable**: Working pipeline for 1 account: Hyke uploads → scheduled → posted to TikTok

#### Phase A3: MVP Content Launch (Weeks 2-3)

| Task | Estimated Hours | Owner | Purpose |
|------|-----------------|-------|---------|
| Support Hyke's content production | 2-4 hrs | Matt | Automation assists as needed |
| Deploy first 5+ videos via pipeline | 2-3 hrs | Matt | Go live with MVP persona |
| Monitor posting and debug issues | 3-4 hrs | Matt | Ensure content reaches audience |
| Refine workflow based on Hyke feedback | 2-3 hrs | Matt | Improve handoff process |

**Deliverable**: First 5+ videos live on TikTok from 1 persona

#### Phase A4: MVP Analytics & Learning (Weeks 3-4)

| Task | Estimated Hours | Owner | Purpose |
|------|-----------------|-------|---------|
| Build attention analytics dashboard | 4-6 hrs | Matt | Track views, watch time, engagement |
| Surface insights for Hyke | 2-3 hrs | Matt | What's working? What should Hyke do more of? |
| Analyze MVP performance | 2-3 hrs | Matt | Is this strategy worth scaling? |
| **Decide: iterate or pivot** | 1-2 hrs | Team | Based on data, what's next? |

**Deliverable**: Data-driven decision on whether to scale this strategy or try another

*Note: Scale phase (multi-account, additional personas) would be a separate engagement.*

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

## Time Estimates (MVP Only)

Note: These estimates are for **Matt's systems/automation work only**. Hyke's video production time is separate.

Estimates include buffer for:
- Debugging and troubleshooting
- API limitations or unexpected blockers
- Iteration based on feedback
- Coordination overhead

### MVP Scope (This Engagement)

| Pillar | Phase | Estimated Hours | Target |
|--------|-------|-----------------|--------|
| **ATTENTION** | A1: Research & Strategy | 18-26 hrs | End of Week 1 |
| **ATTENTION** | A2: Distribution Build (1 account) | 18-26 hrs | End of Week 2-3 |
| **ATTENTION** | A3: MVP Content Launch | 14-20 hrs | Weeks 3-4 |
| **ATTENTION** | A4: MVP Analytics & Learning | 14-20 hrs | Weeks 4-5 |
| **CONVERSION** | C1: Tracking Setup | 14-20 hrs | Weeks 2-3 |
| **CONVERSION** | C2: Analysis | 12-18 hrs | Weeks 4-5 |

### MVP Totals

| Focus Area | Total Hours | % of Effort |
|------------|-------------|-------------|
| **ATTENTION** (Matt) | 64-92 hrs | ~70% |
| **CONVERSION** (Matt) | 26-38 hrs | ~30% |
| **MVP TOTAL** (Matt) | **90-130 hours** | 100% |

**MVP Target**: Weeks 1-5 (~90-130 hours) = 1 persona live + basic tracking + learnings

### Timeline Note

This is a realistic timeline assuming:
- Part-time availability (not full-time dedicated)
- Coordination with Hyke's schedule
- Normal troubleshooting and iteration cycles
- Some buffer for unknowns (API issues, platform changes, etc.)

*Future phases (scale, full system) would require separate scoping and engagement.*

---

## Weekly Milestones (MVP)

| Week | Focus | Key Deliverable | Success Metric |
|------|-------|-----------------|----------------|
| **Week 1** | Research & Strategy | 1 MVP persona defined, tools researched | Ready to build pipeline |
| **Week 2** | Build Pipeline | Distribution pipeline in progress | Core automation working |
| **Week 3** | Pipeline + Tracking | Distribution complete, tracking setup | Can post content automatically |
| **Week 4** | Launch | First videos live from 1 persona | Content reaching audience |
| **Week 5** | Learn & Analyze | Analytics, insights, decision | Know if strategy is working |

*Post-MVP phases would be scoped separately.*

---

## Risk Assessment (by Pillar)

### Attention Risks

| Risk | Impact | Likelihood | Mitigation |
|------|--------|------------|------------|
| TikTok API restrictions | High | Medium | Research alternatives, manual posting fallback |
| Account bans (multi-account) | High | Medium | Stagger creation, follow TOS |
| Content not gaining traction | Medium | Medium | Expected - system designed to iterate |
| Algorithm changes | Medium | Low | Diversify personas and strategies |
| Hyke bandwidth constraints | Medium | Medium | Matt's automation reduces Hyke's manual work |

### Collaboration Risks

| Risk | Impact | Likelihood | Mitigation |
|------|--------|------------|------------|
| Misaligned workflow | Medium | Medium | Sync with Hyke early, iterate on handoff process |
| Content bottleneck (waiting on Hyke) | Medium | Medium | Build pipeline so it's ready when Hyke delivers |
| Communication gaps | Low | Medium | Regular check-ins between Matt and Hyke |

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

2. **Hyke's workflow**: What tools does Hyke use to create videos? How should the handoff work (upload location, format, etc.)?

3. **Trend research**: What specific types of trending content should we surface for Hyke? Any sources he already follows?

4. **DERMA DAO assets**: What product info, images, branding assets are available for Hyke to use?

5. **Account management**: Who creates/owns the TikTok accounts? How do we handle credentials for automated posting?

6. **Posting frequency**: How many videos per account per day/week? What's the target content volume?

### 💰 Conversion Questions

7. **Conversion tracking**: Is there existing analytics on BioFi, or do we need to set this up?

8. **Product page**: Is the DERMA DAO product page ready with the ingredient story and conversion messaging?

9. **Success metrics**: What conversion rate would be considered successful for this MVP?

### 🤝 Collaboration Questions

10. **Communication with Hyke**: How should Matt and Hyke coordinate? Shared tools, check-ins?

11. **Content approval**: Does content need approval before posting, or is it automated once Hyke uploads?

12. **Feedback loop**: How quickly does Hyke need analytics feedback to adjust content strategy?

---

## Recommended Next Steps

### Immediate (Before Starting)
1. Confirm MVP scope and answer key questions above
2. **Pick 1 MVP persona** with Hyke (e.g., fitness, skincare mom, or model)
3. Sync with Hyke on workflow and collaboration approach
4. Get DERMA DAO product assets and messaging

### Week 1: Research & Strategy (Matt + Hyke)
5. Set up project infrastructure
6. Build trending content scraper to surface ideas for Hyke
7. **Document the 1 MVP persona strategy** (voice, style, content themes)
8. Begin building TikTok distribution pipeline

### Week 2: Pipeline Complete + Hyke Starts Creating
9. Complete distribution automation for 1 account (Matt)
10. Create content upload workflow for Hyke (Matt)
11. Set up conversion tracking (Matt)
12. **Hyke begins producing first batch of content for MVP persona**

### Week 3: MVP Launch
13. Deploy first 5+ videos via automated pipeline
14. Monitor posting, fix any distribution issues
15. Track attention metrics (views, engagement)

### Week 4: Learn & Decide
16. Surface analytics insights for Hyke
17. Analyze what's working (attention) and what converts (conversion)
18. **Decision point**: Is this strategy worth scaling, or try a different persona?

*Post-MVP phases would require separate scoping and engagement.*

---

## Engagement Terms

- **Rate**: $125/hour
- **Billing**: Time and materials (not fixed scope)
- **Approach**: Agile/iterative with weekly check-ins
- **Communication**: Regular updates on progress vs. goals
- **Flexibility**: Scope can adjust as we learn what works

### Weekly KPI Check-ins (MVP = 1 Persona)

| Week | Attention KPIs | Conversion KPIs |
|------|----------------|-----------------|
| Week 1 | 1 MVP persona defined, tools researched | Tracking plan ready |
| Week 2 | Pipeline build in progress | Tracking implementation started |
| Week 3 | Pipeline complete, ready to post | Tracking implemented |
| Week 4 | First videos live, views coming in | Click-throughs tracked |
| Week 5 | Data on MVP strategy performance | ROI visibility for 1 persona |

Per the call:
> "I would prefer to not waste a lot of time on like scope and philosophy and just get going... I like to eliminate any speed bumps or friction, but make sure we have, let's say, ongoing KPI, another indicator that says, hey, we're moving the right direction"

---

## Appendix: Potential Tech Stack (To Be Validated)

### 🎯 Attention Stack (Matt's Systems)

| Component | Options to Explore | Purpose |
|-----------|-------------------|---------|
| **Trend Scraping** | Apify, custom scrapers, social listening APIs | Surface trending content for Hyke |
| **Content Queue** | Custom system, Airtable, Notion API | Manage Hyke's videos through pipeline |
| **Distribution** | TikTok API, third-party schedulers, manual posting | Automate posting (MVP: 1 account) |
| **Scheduling** | Custom automation, cron jobs, task queues | Consistent posting cadence |
| **Attention Analytics** | TikTok native analytics, custom dashboard | Track views, engagement |
| **Knowledge Base** | Markdown files, Notion | Persona strategy docs |

**Note**: Video generation tools (HeyGen, D-ID, etc.) are Hyke's domain, not Matt's focus.

### 💰 Conversion Stack (Matt's Systems)

| Component | Options to Explore | Purpose |
|-----------|-------------------|---------|
| **Click Tracking** | UTM parameters, link shorteners with tracking | Attribution by video/persona |
| **Attribution** | Segment, Mixpanel, custom tracking | End-to-end funnel visibility |
| **Conversion Analytics** | BioFi native analytics, custom dashboard | CTR, purchases, revenue |
| **Funnel Analysis** | Segment, Amplitude, custom | Where users drop off |

### Infrastructure

| Component | Options to Explore | Purpose |
|-----------|-------------------|---------|
| **Compute** | Cloud functions, containerized services | Run automation jobs |
| **Storage** | S3/GCS for video assets | Store Hyke's videos for distribution |
| **Database** | PostgreSQL, MongoDB | Analytics data, content queue |
| **Existing Platform** | Matt's agent platform (shown in call) | Potential backend for research agents |

---

*Document created: January 19, 2025*
*Next update: After kickoff alignment call*
