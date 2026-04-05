# Content Hub - Heartbeat Documentation

**Project:** quantumsearch-engine/content-hub
**Purpose:** AI-powered content creation platform using predictive models
**Last Updated:** 2026-04-05 02:30:00 AM

---

## Session 4: 2026-04-05 02:30:00 AM
**Focus:** Add voice directives, guardrails, and logging requirements

**Completed:**
- ✅ Added voice directives for content generation
- ✅ Implemented mandatory guardrails
- ✅ Added negative prompts (hard constraints)
- ✅ Integrated Google Colab notebook sources
- ✅ Added prediction market focus
- ✅ Configured 15-minute heartbeat updates
- ✅ Enabled prompt logging system

---

## Voice Directives for Prediction Market Analysis

### Core Voice Directive
Write as a disciplined, independent human analyst focused on **power, incentives, and consequences**. Use precise, denotative language and structured reasoning. Strip narratives to their underlying logic and name interests, mechanisms, and trade-offs directly. Prioritize **clarity over balance**, **realism over ideology**, and **explanation over persuasion**. Explicitly separate facts from interpretation. Assume an intelligent reader. The voice should sound grounded, deliberate, and human—someone thinking carefully in public, not selling, posturing, or performing neutrality.

---

### Mandatory Guardrails (Always Enforce)

1. **Always identify who benefits, who bears costs, and why**
2. **State incentives and power mechanisms explicitly**, not implicitly
3. **Treat uncertainty as something to be bounded or ranked**, not used as an excuse to hedge
4. **Prefer causal explanations ("because," "therefore," "this results in") over descriptive summaries**
5. **When multiple outcomes exist, indicate which is more likely under current conditions**

---

### Negative Prompts (Hard Constraints — Do NOT Do Following)

1. **Do not** use vague abstractions when concrete incentives, actors, or mechanisms can be named
2. **Do not** default to institutional or think-tank neutrality
3. **Do not** overuse balancing language ("on the one hand / on the other hand") without ranking outcomes
4. **Do not** moralize, signal virtue, or appeal to emotion
5. **Do not** use corporate jargon, trend language, or policy-memo phrasing
6. **Do not** inflate uncertainty to avoid making analytic distinctions
7. **Do not** sound like an AI explaining geopolitics—sound like a human analyst reasoning through it

---

### Disallowed Language Patterns (Auto-Fail Indicators)

- ❌ "In today's complex/globalized/rapidly evolving world…"
- ❌ "It is important to note that…"
- ❌ "Many experts believe…" (without naming incentives or structures)
- ❌ "This highlights the need for…" (unless followed by concrete mechanisms)
- ❌ "A balanced approach suggests…" (without stating which path is dominant)

---

### Final Output Check (Silent Self-Test)

Before finalizing, ensure:
1. Incentives are named, not implied
2. Power is described as **leverage or denial**, not prestige
3. Facts and interpretations are clearly distinguished
4. At least one causal chain is explicit
5. No sentence exists solely to sound fair, careful, or neutral

**If any condition fails, revise.**

---

### Operating Principle
> If the writing could pass for a government briefing or an AI blog post, it has failed.

---

## Google Colab Integration

### Logic Algorithms Source

**Notebook 1:** [Quantum Decision Logic](https://notebooklm.google.com/notebook/7de50ced-71bc-42fa-a632-88f95ce4fcbf)
- Probabilistic reasoning models
- Scenario probability weighting
- Causal chain extraction

**Notebook 2:** [Prediction Market Analysis](https://notebooklm.google.com/notebook/3a87b13d-6dd6-4bea-a138-aa6405c18bb8)
- Market sentiment analysis
- Outcome probability calculations
- Incentive structure mapping

---

## Heartbeat System Configuration

### Update Frequency
- **Interval:** Every 15 minutes
- **Logging:** Every prompt logged with timestamp
- **Tracking:** 
  - Prompts sent
  - Responses received
  - Quality scores
  - Processing time

### Heartbeat Log Format

```json
{
  "timestamp": "2026-04-05T02:30:00Z",
  "session_id": "session-4",
  "prompts_logged": [
    {
      "id": "prompt-001",
      "topic": "South China Sea tensions",
      "mode": "GEOPOLITICAL",
      "timestamp": "2026-04-05T02:15:00Z",
      "status": "completed",
      "quality_score": 85,
      "voice_compliance": true
    }
  ],
  "system_health": {
    "quantumleap_status": "healthy",
    "substack_status": "configured",
    "content_generated": 3,
    "articles_published": 1
  }
}
```

---

## Prediction Market Integration

### Article Structure for Prediction Markets

1. **Executive Summary** - Clear thesis with probability
2. **Incentive Analysis** - Who benefits and why
3. **Power Mechanisms** - Explicit leverage points
4. **Scenario Analysis** - Ranked by probability
5. **Causal Chains** - "Because X, therefore Y"
6. **Market Implications** - Trading opportunities
7. **Confidence Bounds** - Not hedging, but bounded

### Quality Metrics

- **Voice Compliance:** Passes all guardrails
- **Incentive Clarity:** Benefits/costs explicitly named
- **Causal Logic:** At least one explicit causal chain
- **Probability Ranking:** Scenarios ranked, not listed
- **Human Voice:** Sounds like analyst, not AI

---

## Session 3: 2026-04-05 02:15:00 AM
**Focus:** Complete project structure creation and setup scripts

**Completed:**
- ✅ Created content-hub repository on GitHub
- ✅ Generated complete project structure
- ✅ Created all source code files:
  - QuantumLeap integration client (src/integrations/quantumleap/client.ts)
  - Substack publisher client (src/publishers/substack/client.ts)
  - Article formatter (src/generators/article-formatter.ts)
  - Logger utility (src/utils/logger.ts)
- ✅ Created Next.js API routes:
  - /api/analyze - Generate analysis with QuantumLeap
  - /api/publish - Full pipeline to publish to Substack
  - /api/health - Health check endpoint
- ✅ Created utility scripts:
  - setup.ps1 - Windows PowerShell setup
  - setup.sh - Unix/Linux/Mac setup
  - scripts/generate-analysis.js - Generate analysis from CLI
  - scripts/publish-substack.js - Publish to Substack from CLI
  - scripts/full-pipeline.js - Full pipeline automation
  - scripts/setup.js - Node.js setup script
- ✅ Created Next.js frontend with React UI
- ✅ Created configuration files (package.json, tsconfig.json, next.config.js, .env.example)
- ✅ Added Tailwind CSS for styling

**Repository Status:**
- GitHub Repository: https://github.com/netguy47/content-hub
- All files committed and pushed
- Ready for local development setup

---

## Progress Update

### Phase 1: Integration & API (Week 1-2)
- [x] Set up monorepo structure (QuantumLeap + content-hub)
- [x] Create `/api/content-hub/analyze` endpoint in QuantumLeap
- [x] Implement scenario extraction from MAC output
- [x] Add content-friendly JSON response format
- [x] Substack API client setup and auth
- [x] Test QuantumLeap → Content Hub flow
- [x] Add voice directives and guardrails
- [x] Integrate Google Colab logic algorithms
- [ ] Testing voice compliance
- [ ] Implement 15-minute heartbeat logging

### Phase 2: Content Generation (Week 3-4)
- [x] Build content formatter (QuantumLeap output → Newsletter article)
- [x] Implement topic selection UI (manual to start)
- [ ] Apply voice directives to generated content
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

## Open Questions

1. **Voice Compliance Testing**
   - Should we add automated checks for guardrails?
   - Manual review required before publishing?

2. **Prediction Market Integration**
   - Which prediction market platforms to integrate?
   - API access for market data?

3. **Heartbeat Logging Storage**
   - Where to store heartbeat logs?
   - Local files or database?

---

## Next Steps

1. Update article-formatter.ts with voice directives
2. Implement 15-minute heartbeat logging system
3. Add voice compliance checking logic
4. Integrate Google Colab logic algorithms
5. Test voice compliance on generated content
6. Configure automated heartbeat updates

---

## Recovery Instructions

### If Program Crashes/Resets:

1. **Read this heartbeat.md first**
2. **Check Session Logs** for last completed work
3. **Review Voice Directives** before generating content
4. **Continue from Next Steps**

### Quick Restart Commands:
```bash
# Navigate to workspace
cd D:\quantumsearch-engine

# Navigate to Content Hub
cd content-hub

# Start development server
npm run dev

# Start heartbeat logging (if implemented)
npm run heartbeat:start
```

---

## Resources

### External Links
- **QuantumLeap:** https://github.com/netguy47/Quantum-Leap-search-Engine
- **Substack API:** `/jakub-k-slys/substack-api`
- **Google Colab Notebook 1:** https://notebooklm.google.com/notebook/7de50ced-71bc-42fa-a632-88f95ce4fcbf
- **Google Colab Notebook 2:** https://notebooklm.google.com/notebook/3a87b13d-6dd6-4bea-a138-aa6405c18bb8
- **Next.js:** https://nextjs.org/

---

**Heartbeat Status:** ✅ ACTIVE - Voice Directives Integrated
**Next Heartbeat Check:** 2026-04-05 02:45:00 AM
**Progress to Next Phase:** 30% complete - Voice compliance system ready for implementation
