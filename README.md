# AI-Powered Lead Intelligence Hub
## Job Application Showcase

### What This Workflow Does

This is an **end-to-end lead automation system** that captures leads from webhooks, enriches them with data from multiple sources, uses AI to score their quality, and intelligently routes them to your sales team.

**In simple terms:** Lead comes in → Gets smarter with data → AI rates it → Goes to the right place

### The Complete Flow

```
1. Lead Webhook Arrives
   ↓
2. Validate & Check for Duplicates
   ↓
3. Enrich with External Data (Clearbit, LinkedIn, Website)
   ↓
4. Score with AI (Demographics, Engagement, Intent)
   ↓
5. Route to Sales (Hot/Warm/Cold leads)
   ↓
6. Store Everything (Google Sheets, HubSpot)
```

### Key Capabilities

✅ **Data Validation**
- Webhook signature verification
- Required fields check
- Email validation
- Duplicate detection

✅ **Multi-Source Enrichment**
- Clearbit (company data)
- LinkedIn (contact profiles)
- Website analysis (content parsing)
- Historical CRM data

✅ **AI-Powered Scoring**
- Demographics fit (25%)
- Engagement signals (35%)
- Buying intent (40%)
- Multi-model AI (Gemini, GPT-4o, Claude)

✅ **Smart Routing**
- Hot leads → Slack alert + HubSpot
- Warm leads → HubSpot
- Cold leads → Google Sheets nurture list

✅ **Reliability**
- Error tracking with Dead Letter Queue
- Graceful fallbacks
- Comprehensive logging
- Cost tracking per lead

---

## The Refactoring: From Monolith to Modular

### Before (Original Single Workflow)
```
One massive workflow with 35+ nodes
├─ Enrichment logic (9 nodes)
├─ Scoring logic (5 nodes)
└─ Storage logic (6 nodes)

❌ Hard to maintain
❌ Hard to test individual pieces
❌ Can't reuse components
❌ Confusing to navigate
```

### After (Refactored with Sub-Workflows)
```
Clean main workflow (12 nodes)
├─ Call Enrichment Service
├─ Call Scoring Service
└─ Call Persistence Service

✅ Easy to maintain
✅ Test each service independently
✅ Reuse services in other workflows
✅ Clear separation of concerns
```

### Architecture

**Main Workflow** (12 nodes)
- Webhook intake
- Data validation
- Orchestrates 3 sub-workflows
- Response handling

**Sub-Workflow 1: Enrichment Service**
- Pulls data from 4 sources in parallel
- Returns enriched lead object
- Reusable for other automation

**Sub-Workflow 2: Scoring Service**
- Uses multiple AI models
- Calculates demographics/engagement/intent scores
- Returns scored lead with recommendations
- Independent and testable

**Sub-Workflow 3: Persistence Service**
- Updates 4 Google Sheets tables
- Logs to HubSpot
- Records analytics
- Modular for scaling

### Why This Matters

This refactoring demonstrates:
- **Professional software architecture** (separation of concerns)
- **Production-ready patterns** (modular, testable, maintainable)
- **Scalability thinking** (each service can be versioned/updated independently)
- **Best practices** (follows microservices principles in n8n)

---

## Technical Highlights

### What I Built

**Integration Points**
- Webhook (input)
- Clearbit API (company data)
- LinkedIn/Proxycurl (profiles)
- Google Sheets (storage & analytics)
- HubSpot (CRM sync)
- Slack (alerts)

**Data Handling**
- Phone normalization (E.164)
- Domain extraction
- Company size categorization
- UUID generation
- Email validation with regex

**AI/ML**
- Multi-model orchestration (4 different AI services)
- Weighted scoring algorithm
- Fallback logic for failures
- Cost tracking

**Error Handling**
- Dead Letter Queue for failed leads
- Graceful degradation
- Partial data handling
- Comprehensive logging

---

## Results

- **Main workflow**: 16 operational nodes (down from 35+)
- **Sub-workflows**: 3 independent, reusable services
- **Enrichment**: 4 data sources in parallel
- **Scoring**: Multi-model AI analysis
- **Reliability**: Zero data loss with error tracking
- **Performance**: 15-30 seconds end-to-end
- **Cost**: ~$0.01-0.03 per lead

---

## Skills Demonstrated

This workflow shows I can:

✅ **API Integration** - Clearbit, LinkedIn, HubSpot, Google Sheets, Slack
✅ **Data Transformation** - Normalization, validation, mapping
✅ **Error Handling** - Graceful failures, retries, logging
✅ **Workflow Architecture** - Modular design, separation of concerns
✅ **AI/ML** - Multi-model orchestration, scoring algorithms
✅ **Google Sheets** - Complex operations, batching, upserts
✅ **Webhook Management** - Input validation, signature verification
✅ **Refactoring** - Converting monolith to modular system
✅ **Documentation** - Clear, comprehensive guides
✅ **Production Thinking** - Monitoring, cost tracking, reliability

---

## Relevant to Your Job Requirements

Your posting asked for someone who can:

| Your Need | My Demonstration |
|-----------|-----------------|
| Build & maintain n8n workflows | ✅ Full end-to-end workflow system |
| API integration & webhooks | ✅ 5 API integrations + webhook validation |
| Google Sheets mastery | ✅ Complex sheets operations with batching |
| Split, loop, branch flows | ✅ Parallel enrichment + conditional routing |
| Error handling & retries | ✅ Dead Letter Queue + graceful fallbacks |
| Custom JS logic | ✅ Data transformation nodes with helpers |
| Data transformation | ✅ Normalization, validation, mapping |
| Modular design | ✅ Sub-workflows for reusability |

---

**Want to learn more?** You can contact me anytime https://dominicgs.com/
