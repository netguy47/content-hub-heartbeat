# Content Hub - Heartbeat Documentation

**Project:** quantumsearch-engine/content-hub
**Purpose:** AI-powered content creation platform using predictive models
**Last Updated:** 2026-04-05 01:15:30 AM

---

## Project Overview

### Vision
Build a content creation application that uses QuantumLeap Defense Systems' predictive models to generate geopolitical, economic, and strategic analysis content, auto-posting to Substack (donwoods@substack.com) and future blog platforms.

### Core Capabilities
- **Predictive Content Generation**: Using QuantumLeap's Multi-Agent Chain (MAC) architecture
- **Multi-Platform Publishing**: Substack (donwoods@substack.com) + future blog
- **Content Types**: 
  - Geopolitical predictions and analysis
  - Economic scenario modeling
  - Current affairs intelligence briefs
  - Alternative story ripples (multi-scenario analysis)
  - Decision consequence mapping
- **Technical Foundation**: QuantumLeap's 3-node AI architecture (Analyst → Red Team → Synthesizer)

---

## Current State

### Phase: QuantumLeap Integration Design

**Status:** 🔶 INTEGRATION PLANNING
**Progress:** 25%

### Completed
- [x] Project vision defined
- [x] Heartbeat system initialized
- [x] Architecture research initiated
- [x] **QuantumLeap Defense Systems identified and analyzed**
- [x] **Substack API library selected** (`/jakub-k-slys/substack-api`)
- [x] QuantumLeap Multi-Agent Chain architecture documented
- [x] Monorepo integration strategy decided

### In Progress
- [x] QuantumLeap integration strategy design
- [ ] Content hub API endpoints specification
- [ ] Data flow from QuantumLeap to content generation

### Blocked
- [ ] Content-hub project structure creation
- [ ] QuantumLeap API integration implementation
- [ ] Substack API authentication setup

---

## Integration Discovery: QuantumLeap Defense Systems

### QuantumLeap Engine Analysis

**Repository:** [netguy47/Quantum-Leap-search-Engine](https://github.com/netguy47/Quantum-Leap-search-Engine)
**Version:** Beta v0.9.5
**Description:** "The Bloomberg Terminal for Geopolitical Chaos"

### Core Architecture: Multi-Agent Chain (MAC)

QuantumLeap uses a sophisticated 3-node adversarial AI architecture:

```
┌──────────────────────────────────────────────────────────┐
│              QuantumLeap Multi-Agent Chain              │
├──────────────────────────────────────────────────────────┤
│                                                          │
│  ┌────────────────┐     ┌──────────────┐             │
│  │  🟦 Node A:   │     │  🟥 Node B:  │             │
│  │  The Analyst  │────▶│  The Red     │             │
│  │              │     │  Team        │             │
│  └────────────────┘     │  (Auditor)   │             │
│         │               └──────┬───────┘             │
│         ▼                      │                      │
│         │              ┌───────▼─────────┐             │
│         │              │  🟪 Node C:     │             │
│         └─────────────▶│  The Synthesizer │             │
│                        │                 │             │
│                        └─────────────────┘             │
└──────────────────────────────────────────────────────────┘
```

**Node Roles:**

1. **Node A: The Analyst**
   - Data ingestion from web/maps
   - Domain-specific extraction
   - Grounded information gathering
   - Tools: Google Search Grounding

2. **Node B: The Red Team (Adversary)**
   - Aggressively critiques Node A's analysis
   - Detects hallucinations
   - Identifies optimism bias
   - Finds logical fallacies

3. **Node C: The Synthesizer**
   - Adjudicates between A and B
   - Discards debunked claims
   - Produces "Ground Truth JSON"
   - 3x3 tactical grid for heatmaps

### Technical Stack

**Frontend:**
- React 19
- TypeScript
- Tailwind CSS

**AI Layer:**
- Google GenAI SDK
- Gemini 2.5 Flash (speed)
- Gemini 3.0 Pro (depth)

**Simulation Modes:**
- GENERAL - Cross-domain correlations
- STRATEGY - High-level decision modeling
- ECONOMIC - Volatility & supply chain
- CRIME/POLICE - Urban risk & resource mapping
- TRAVEL - Executive protection & extraction routes
- MILITARY - OSINT & force posture
- CIVIL UNREST - Crowd dynamics & protest flashpoints

### Key Deliverables for Content Hub

1. **Intelligence Dossiers**: Red-teamed intelligence with sources
2. **Risk Heatmaps**: 3x3 grid overlays (NW, N, NE, W, C, E, SW, S, SE)
3. **Scenario Analysis**: Multiple alternative paths for events
4. **Grounded Sources**: URL-based verification of all claims
5. **PDF Export**: Classified print mode for executive briefings

---

## Content Hub Architecture (Revised)

### System Components

```
┌───────────────────────────────────────────────────────────────┐
│                   Content Hub System                          │
├───────────────────────────────────────────────────────────────┤
│                                                               │
│  ┌─────────────────────┐     ┌───────────────────┐        │
│  │  QuantumLeap API   │────▶│  Content Hub      │        │
│  │  Integration Layer  │     │  Backend          │        │
│  │                     │     │  (Next.js)        │        │
│  │  • MAC Engine      │     │                   │        │
│  │  • Mode Routing    │     │  • Orchestrator   │        │
│  │  • JSON Output     │     │  • Formatter     │        │
│  └─────────────────────┘     │  • Scheduler     │        │
│           │                 └────────┬──────────┘        │
│           ▼                          │                   │
│  ┌───────────────────────────────────▼──────────┐        │
│  │        Content Processing Pipeline          │        │
│  │                                           │        │
│  │  1. Topic Selection (auto/manual)        │        │
│  │  2. Mode Routing (ECONOMIC/MILITARY)     │        │
│  │  3. QuantumLeap Analysis Trigger          │        │
│  │  4. Multi-Scenario Extraction           │        │
│  │  5. Article Formatting                  │        │
│  │  6. Quality Scoring                   │        │
│  └───────────────────────┬───────────────────┘        │
│                        │                              │
│                        ▼                              │
│  ┌──────────────────────────────────────────────┐        │
│  │       Publishing Engine                   │        │
│  │                                          │        │
│  │  • Substack API Client                   │        │
│  │  • Draft Creation                       │        │
│  │  • Scheduled Publishing                 │        │
│  │  • Analytics Tracking                  │        │
│  └──────────────────────────────────────────────┘        │
│                                                               │
└───────────────────────────────────────────────────────────────┘
```

### Data Flow (Enhanced)

```
1. INPUT: Topic/Event
         ↓
2. Content Hub: Selects Simulation Mode (ECONOMIC/GEOPOLITICAL/ETC)
         ↓
3. QuantumLeap API: Runs Multi-Agent Chain
         ↓
4. Node A (Analyst): Gathers intelligence
         ↓
5. Node B (Red Team): Critiques and validates
         ↓
6. Node C (Synthesizer): Produces grounded dossier
         ↓
7. Content Hub: Extracts multiple scenarios
         ↓
8. Content Hub: Formats as newsletter article
         ↓
9. Human Review: Approves/edit (optional)
         ↓
10. Publishing: Auto-post to Substack
         ↓
11. Feedback: Track engagement for model improvement
```

---

## Architecture Decisions

### Decision 1: QuantumLeap Integration Strategy ✓

**Status:** DECIDED

**Selected Approach:** Direct Monorepo Integration

**Implementation:**
```
Option A: Monorepo (RECOMMENDED)
├── Quantum-Leap-search-Engine/     # Existing QuantumLeap
│   ├── src/
│   ├── api/
│   └── package.json
└── content-hub/                      # NEW
    ├── src/
    │   ├── integrations/
    │   │   └── quantumleap/     # QuantumLeap API client
    │   ├── generators/
    │   └── publishers/
    │       └── substack/        # Substack API client
    └── package.json
```

**Recommendation:** Option A (Monorepo)
- Shared types and utilities
- Easy local development
- Can reuse QuantumLeap components directly
- Simplifies deployment

**Decision Date:** 2026-04-05

---

### Decision 2: Substack Integration ✓

**Status:** DECIDED
**Library:** `/jakub-k-slys/substack-api` (TypeScript, 91.6 score)

**Implementation:**
```typescript
import { SubstackClient } from '@jakub-k-slys/substack-api';

const client = new SubstackClient({
  email: 'donwoods@substack.com',
  password: process.env.SUBSTACK_PASSWORD
});

// Create draft post
const draft = await client.createPost({
  title: analysis.headline,
  subtitle: analysis.summary,
  content: formattedArticle,
  tags: analysis.topics
});

// Schedule publish
await client.schedulePost(draft.id, {
  publishAt: new Date(Date.now() + 86400000) // 24h later
});
```

**Decision Date:** 2026-04-05

---

## Integration Points

### 1. QuantumLeap Engine Integration

**Status:** ⏳ ARCHITECTURE DEFINED

**API Endpoints to Expose:**

```typescript
// QuantumLeap API Extensions for Content Hub

interface ContentHubRequest {
  topic: string;
  mode: 'GENERAL' | 'ECONOMIC' | 'GEOPOLITICAL' | 'MILITARY' | 'CIVIL_UNREST';
  depth: 'quick' | 'deep' | 'comprehensive';
  includeScenarios?: boolean;
  includeHeatmap?: boolean;
}

interface ContentHubResponse {
  intelligence: {
    keyFindings: string[];
    confidenceScores: number[];
    groundedSources: URL[];
  };
  scenarios: Array<{
    probability: number;
    description: string;
    timeline: string;
    indicators: string[];
  }>;
  heatmap?: {
    region: string;
    riskLevel: 'LOW' | 'MEDIUM' | 'HIGH' | 'CRITICAL';
    factors: string[];
  }[];
  rawQuantumLeapOutput: any;
}
```

**Implementation Strategy:**
1. Extend existing QuantumLeap API routes (`/api/` directory)
2. Add `/api/content-hub/analyze` endpoint
3. Expose MAC chain results with content-friendly structure
4. Include scenario extraction logic

---

### 2. Substack Publishing

**Status:** ⏳ PLANNED
**Library:** `/jakub-k-slys/substack-api`
**Account:** donwoods@substack.com

**Implementation Steps:**
1. Install: `npm install @jakub-k-slys/substack-api`
2. Create `.env` with Substack credentials
3. Build formatter for QuantumLeap → Substack article
4. Implement draft creation and review workflow
5. Add scheduling system for auto-publishing
6. Monitor publishing status

---

### 3. Future Blog Platform

**Status:** ❌ NOT DEFINED
**Priority:** POST-MVP

---

## Session Logs

### Session 1: 2026-04-05 01:04:10 AM
**Focus:** Project initialization and heartbeat setup

**Completed:**
- Created GitHub repository for heartbeat tracking
- Initialized heartbeat.md documentation
- Researched Substack API integration options
- Drafted system architecture

**Decisions Made:**
- Using TypeScript for publishing (Substack API client)
- Considering Python for ML/Bayesian components
- Heartbeat system operational for crash recovery

**Next Steps:**
1. Determine quantumsearch-engine integration approach
2. Set up local development environment
3. Implement Substack API authentication
4. Create content generation prototype

**Blockers:**
- Need access to quantumsearch-engine API/docs
- Need Substack API credentials from donwoods@substack.com

---

### Session 2: 2026-04-05 01:15:30 AM
**Focus:** QuantumLeap engine discovery and integration design

**Completed:**
- ✅ Accessed QuantumLeap Defense Systems repository
- ✅ Documented Multi-Agent Chain (MAC) architecture
- ✅ Identified AI layer: Google GenAI SDK (Gemini 2.5/3.0)
- ✅ Analyzed simulation modes (7 different modes)
- ✅ Defined integration strategy with content hub
- ✅ Selected monorepo approach (Option A)
- ✅ Specified API extensions for content hub
- ✅ Updated heartbeat with quantumsearch-engine details

**Decisions Made:**
- **QuantumLeap Integration**: Direct monorepo integration, not HTTP API
- **Architecture**: Shared codebase with content-hub as sibling to QuantumLeap
- **API Extension**: New `/api/content-hub/analyze` endpoint
- **Content Output**: Extract scenarios, heatmaps, intelligence dossiers
- **Substack**: TypeScript client confirmed, implementation plan ready

**Technical Discoveries:**
- QuantumLeap uses Next.js with API routes (perfect for integration)
- Already has `/api/` directory structure
- Uses Google GenAI SDK - can leverage for content generation
- Has 7 simulation modes perfectly suited for content topics
- JSON output format ready for downstream processing

**Next Steps:**
1. Clone QuantumLeap repo locally if not already
2. Create content-hub as sibling directory in monorepo
3. Implement `/api/content-hub/analyze` endpoint in QuantumLeap
4. Test MAC chain extraction for content-friendly output
5. Set up Substack API client and authentication

**Blockers:**
- [ ] Local repository setup
- [ ] Substack API credentials (donwoods@substack.com)
- [ ] Content topic selection strategy (manual vs. automated)

---

## Features Roadmap

### Phase 1: Integration & API (Week 1-2)
- [ ] Set up monorepo structure (QuantumLeap + content-hub)
- [ ] Create `/api/content-hub/analyze` endpoint in QuantumLeap
- [ ] Implement scenario extraction from MAC output
- [ ] Add content-friendly JSON response format
- [ ] Substack API client setup and auth
- [ ] Test QuantumLeap → Content Hub flow

### Phase 2: Content Generation (Week 3-4)
- [ ] Build content formatter (QuantumLeap output → Newsletter article)
- [ ] Implement topic selection UI (manual to start)
- [ ] Create multi-scenario article templates
- [ ] Add heatmap visualization integration
- [ ] Quality scoring for generated content
- [ ] Draft review and edit workflow

### Phase 3: Publishing (Week 5-6)
- [ ] Auto-draft creation in Substack
- [ ] Scheduled publishing system
- [ ] Multi-platform formatting (Substack + future blog)
- [ ] Analytics tracking and feedback loop
- [ ] Error handling and retry logic

### Phase 4: Automation (Week 7+)
- [ ] Automated topic discovery (news APIs, trending)
- [ ] Auto-publishing based on quality score thresholds
- [ ] Blog platform integration (Ghost/WordPress/custom)
- [ ] A/B testing for content variations
- [ ] User preferences and personalization

---

## Technical Stack Recommendations

### Backend (Unified)
- **Runtime:** Node.js 20+ (both QuantumLeap and content-hub)
- **Framework:** Next.js (QuantumLeap) + Next.js (content-hub)
- **Sharing:** Shared TypeScript types, utilities
- **API:** Next.js API Routes (QuantumLeap)
- **Queue:** BullMQ (for scheduled publishing)

### Content Generation
- **QuantumLeap MAC:** Multi-Agent Chain (Analyst → Red Team → Synthesizer)
- **Google GenAI SDK:** Gemini 2.5 Flash / 3.0 Pro
- **Format:** JSON-based intelligence dossiers
- **Scenarios:** Extract from Synthesizer node

### Publishing
- **Substack:** `@jakub-k-slys/substack-api`
- **Blog:** TBD (Ghost recommended for newsletters)
- **Analytics:** Substack API + custom tracking

### DevOps
- **Version Control:** Git (monorepo)
- **CI/CD:** GitHub Actions
- **Deployment:** Vercel (Next.js hosting)
- **Monitoring:** Application logs, error tracking

---

## Risk Assessment

### High Priority
1. **QuantumLeap API Compatibility**
   - Risk: MAC output format changes break content extraction
   - Mitigation: Versioned API, fallback handling

2. **Substack API Limitations**
   - Risk: Rate limiting, feature constraints, undocumented limits
   - Mitigation: Implement queuing, test thoroughly, backup methods

### Medium Priority
1. **Content Quality Control**
   - Risk: AI-generated content accuracy
   - Mitigation: QuantumLeap's red-teaming already addresses this

2. **Platform Lock-in**
   - Risk: Substack API changes, platform policies
   - Mitigation: Abstraction layer, multiple platform support

### Low Priority
1. **Performance Scaling**
   - Risk: MAC chain slow for batch processing
   - Mitigation: Queue system, parallel processing

---

## Open Questions

1. **Repository Access**
   - Is QuantumLeap already cloned to `D:\quantumsearch-engine`?
   - Should we work from existing clone or fresh setup?

2. **Substack Authentication**
   - How do you want to handle Substack credentials?
   - Email/password? API key? OAuth?
   - Secure storage strategy (.env, secrets manager)?

3. **Content Topics**
   - Initial focus topics?
   - Manual topic selection or automated discovery?
   - Frequency of new articles (daily, weekly, on-demand)?

4. **Blog Platform**
   - Timeline for blog integration?
   - Preference: Ghost, WordPress, custom Next.js?

---

## Recovery Instructions

### If Program Crashes/Resets:

1. **Read this heartbeat.md first**
2. **Check Session Logs** for last completed work
3. **Review Open Questions** to update with new information
4. **Continue from Blockers/Next Steps**

### Quick Restart Commands:
```bash
# Navigate to workspace
cd D:\quantumsearch-engine

# If QuantumLeap not present, clone it
git clone https://github.com/netguy47/Quantum-Leap-search-Engine.git

# Create content-hub directory
mkdir content-hub

# Read heartbeat
cat ../content-hub-heartbeat/heartbeat.md

# Continue from last session
```

---

## Resources

### External Links
- **QuantumLeap:** https://github.com/netguy47/Quantum-Leap-search-Engine
- **Substack API:** `/jakub-k-slys/substack-api`
- **Google GenAI SDK:** https://cloud.google.com/ai/docs/app-builder
- **Next.js:** https://nextjs.org/

### Project Structure (Planned Monorepo)
```
D:\quantumsearch-engine\
├── Quantum-Leap-search-Engine/      # Existing QuantumLeap
│   ├── src/
│   ├── api/
│   │   └── content-hub/         # NEW: Content hub API
│   ├── public/
│   └── package.json
├── content-hub/                      # NEW: Publishing layer
│   ├── src/
│   │   ├── generators/
│   │   ├── publishers/
│   │   │   └── substack/
│   │   └── utils/
│   └── package.json
└── content-hub-heartbeat/            # This repo
    └── heartbeat.md
```

---

## QuantumLeap Content Integration Examples

### Example 1: Geopolitical Analysis

**Request:**
```json
{
  "topic": "Tensions in South China Sea",
  "mode": "GEOPOLITICAL",
  "depth": "deep",
  "includeScenarios": true,
  "includeHeatmap": true
}
```

**Response (Simplified):**
```json
{
  "intelligence": {
    "keyFindings": [
      "Recent naval exercises indicate escalation",
      "Economic stakes involve shipping routes worth $5T annually"
    ],
    "confidenceScores": [0.85, 0.72],
    "groundedSources": [
      "https://reuters.com/...",
      "https://navy.mil/..."
    ]
  },
  "scenarios": [
    {
      "probability": 0.65,
      "description": "Limited conflict with diplomatic resolution",
      "timeline": "6-12 months",
      "indicators": ["Increased diplomatic talks", "Joint military exercises"]
    },
    {
      "probability": 0.25,
      "description": "Full regional conflict with economic disruption",
      "timeline": "3-6 months",
      "indicators": ["Naval blockade", "Alliance mobilization"]
    }
  ],
  "heatmap": [
    {
      "region": "Southeast Asia",
      "riskLevel": "HIGH",
      "factors": ["Shipping disruption", "Military activity"]
    }
  ]
}
```

---

**Heartbeat Status:** ✅ ACTIVE - QuantumLeap Integration Designed
**Next Heartbeat Check:** End of current session
**Progress to Next Phase:** 25% complete - Architecture finalized, ready for implementation
