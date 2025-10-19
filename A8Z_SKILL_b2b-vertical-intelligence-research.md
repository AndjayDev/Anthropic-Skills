---
name: b2b-vertical-intelligence-research
description: Analyzes prospect website content to generate comprehensive market intelligence briefs and pre-call presentations. Extracts business profile, vertical classification, pain points, disruptions, and leverage opportunities. Uses explicit research planning with NLP-driven keyword extraction. Integrates with 3X Sales Accelerator methodology for B2B sales preparation. Use when analyzing prospect websites for pre-call intelligence, market positioning, or strategic brief generation.
---

# B2B Vertical Intelligence Research

Advanced prospect intelligence system for 3X Sales Accelerator methodology. Transforms scraped website content into actionable market intelligence briefs and pre-call presentations.

## Quick Start

**Command:** `/analyze-prospect [company_website_content]`

**Process:**
1. Website content analysis and UVP extraction
2. NLP-driven research planning (you approve scope)
3. Multi-source intelligence gathering
4. Tiered brief generation (Tier 1/2/3)
5. Pre-call presentation creation

## Core Capabilities

### Intelligence Modules
- **Business Profile Analysis** - Company classification, offerings, positioning
- **Vertical Intelligence** - Industry trends, disruptions, regulations
- **Pain Detection** - Hiring signals, technology gaps, growth indicators
- **Competitive Landscape** - Similar companies, market positioning
- **Recent Events** - News, funding, M&A, launches
- **Decision-Maker Mapping** - Key stakeholders, buying patterns

### Output Formats
- **Tier 1 Brief** (5-8 pages): High-value prospects ($5M+ revenue, C-suite)
- **Tier 2 Brief** (3-5 pages): Mid-market ($2M-$5M, Director/Manager)
- **Tier 3 Brief** (2-3 pages): Time-sensitive/High-authority
- **Pre-Call Deck** (Markdown or JSON for PandaDoc/Google Templates)

## Commands

### Primary Analysis Command
```
/analyze-prospect [website_content] --tier=[1|2|3] --depth=[0-5] --format=[markdown|json]
```

**Parameters:**
- `website_content`: Scraped text or parsed HTML
- `tier`: Brief complexity (1=comprehensive, 2=balanced, 3=executive)
- `depth`: Verbosity level (0=minimal, 5=exhaustive)
- `format`: Output format (markdown for docs, json for automation)

### Research Planning Command
```
/plan-research [company_name] --focus=[all|fundamentals|competitive|pain-signals]
```

Generates NLP-driven research plan based on extracted UVP and strategic keywords. Presents comprehensive research scope for your approval before execution.

### Brief Generation Command
```
/generate-brief [company_name] --tier=[1|2|3] --template=[digital-footprint|strategic|executive]
```

Creates market intelligence brief using approved research data and selected template.

### Presentation Command
```
/create-precall-deck [company_name] --format=[markdown|json] --slides=[5|10|15]
```

Generates pre-call presentation with pain points, leverage opportunities, and 3X Sales Accelerator positioning.

## Workflow

### Step 1: Content Analysis
```
/analyze-prospect [scraped_website_content]
```

**Claude extracts:**
- Company name, industry, business model
- Core offerings and unique value propositions
- Target market and customer segments
- Technology stack indicators
- Strategic keywords and positioning signals

### Step 2: Research Planning (EXPLICIT APPROVAL REQUIRED)

**Claude presents research plan:**
```
📋 RESEARCH PLAN FOR [COMPANY NAME]

**Company Fundamentals Research:**
- Recent news articles (last 90 days)
- Funding rounds and investor information (Crunchbase)
- Leadership changes and key hires
- Financial performance indicators

**Industry/Vertical Intelligence:**
- [Industry] market trends and growth projections
- Regulatory changes affecting [vertical]
- Technology disruptions in [sector]
- Competitive dynamics analysis

**Competitive Landscape:**
- Top 5 similar companies by NAICS code
- Market positioning and differentiation
- Pricing strategies and business models
- Strategic partnerships and alliances

**Pain Signal Detection:**
- Job postings indicating growth challenges
- Technology adoption gaps from stack analysis
- Customer review analysis (G2, TrustRadius)
- Support ticket patterns and service gaps

**Recent Events (Last 6-12 Months):**
- Product launches and feature releases
- Market expansion announcements
- M&A activity and strategic investments
- Partnership announcements

**Estimated Research Time:** 15-20 web searches
**Confidence Level:** High (based on extracted UVP clarity)

✅ Approve this research plan?
🔧 Modify research scope?
❌ Skip research and use website data only?
```

### Step 3: Intelligence Gathering

After approval, Claude executes:
- Web searches for approved categories
- Data extraction and synthesis
- Cross-reference validation (3+ sources)
- Confidence scoring per finding

### Step 4: Brief Generation

Choose tier and generate:
```
/generate-brief [company_name] --tier=2 --depth=3
```

**Output includes:**
- Executive snapshot with pain points
- Competitive landscape analysis
- Market opportunity assessment
- Leverage points for 3X Sales Accelerator
- Pre-call preparation checklist
- Strategic discussion framework

### Step 5: Pre-Call Deck Creation
```
/create-precall-deck [company_name] --format=markdown --slides=10
```

**Deck structure:**
1. Company intelligence snapshot
2. Pain points identified
3. Market positioning opportunity
4. Competitive advantages analysis
5. 3X Sales Accelerator fit assessment
6. 30-day implementation preview
7. Success metrics framework
8. Strategic questions for discovery
9. Objection handling preparation
10. Next steps and engagement framework

## Integration with 3X Sales Accelerator

### Pain Detection Methodology
Applies systematic pain signal detection from job postings, technology gaps, and market indicators. Avoids "pain sniffing" terminology - uses "Pain Detection" framework.

### 30-Day Fulfillment Timeline
All briefs reference 30-day implementation milestone with scaling to 20-30 meetings in months 2-3 based on prospect capacity.

### Value-Based Positioning
NO pricing tiers mentioned. Focus on outcome value, ROI potential, and revenue impact. Rev-share remains an option based on prospect situation.

### Sales Call Strategy Integration
Incorporates frameworks from attached sales training:
- Assumed Commonality Psychology
- Strategic Problem Inversion
- Solution-as-Evolution positioning
- Two-Option Choice Architecture (without specific pricing)

## Advanced Features

### Depth Control System

**Level 0-1:** Bottom-line essentials (50-100 words per section)
**Level 2-3:** Balanced analysis (100-300 words per section) [DEFAULT]
**Level 4-5:** Comprehensive deep-dive (300-800+ words per section)

### Multi-Format Output

**Markdown:**
- Direct document generation
- Compatible with Pandoc conversion
- Ready for PDF/DOCX export

**JSON:**
```json
{
  "company_profile": {...},
  "pain_points": [...],
  "competitive_analysis": {...},
  "leverage_opportunities": [...],
  "pre_call_strategy": {...}
}
```

Structured for PandaDoc API or Google Templates integration.

### Template Selection

**Digital Footprint Strategy Template:**
- 19+ page comprehensive analysis
- All modules active, depth=5
- Full competitive analysis
- Multi-scenario disruption modeling

**Strategic Growth Brief:**
- 3-5 page balanced analysis
- Key intelligence focus
- Tactical recommendations
- Session preparation framework

**Executive Assessment:**
- 2-3 page snapshot
- Critical insights only
- Immediate actionability
- Decision-focused content

## Quality Assurance

**Confidence Scoring:**
- All findings scored 0.0-1.0
- Multi-source validation required (3+ sources for statistics)
- Explicit uncertainty flagging when confidence <0.75
- Source attribution for all claims

**Human-in-the-Loop Triggers:**
- Low confidence analyses (<0.70) require review
- Conflicting data sources flagged for verification
- Missing critical information highlighted

## Best Practices

1. **Always start with research planning** - Don't execute searches without approval
2. **Match tier to prospect profile** - Tier 1 for enterprise, Tier 3 for time-sensitive
3. **Adjust depth based on complexity** - Simple businesses = Depth 2, Complex = Depth 4-5
4. **Use markdown for docs, JSON for automation** - Choose format based on downstream use
5. **Review research plan carefully** - Modify scope to focus on most relevant intelligence
6. **Validate pain signals** - Ensure detected pain points align with 3X Sales Accelerator capabilities

## Examples

See `/modules/examples.md` for complete usage scenarios.

## Module Documentation

- `/modules/business_profile.md` - Company classification and positioning
- `/modules/vertical_intelligence.md` - Industry analysis framework
- `/modules/pain_detection.md` - Signal detection methodology
- `/modules/competitive_landscape.md` - Market positioning analysis
- `/modules/recent_events.md` - News and activity tracking
- `/modules/decision_makers.md` - Stakeholder mapping

## Templates

- `/templates/tier1_brief.md` - Executive Intelligence Brief (5-8 pages)
- `/templates/tier2_brief.md` - Strategic Market Brief (3-5 pages)
- `/templates/tier3_brief.md` - Executive Assessment (2-3 pages)
- `/templates/precall_deck_markdown.md` - Pre-call presentation template
- `/templates/precall_deck_json.json` - Structured presentation data

## Scripts

- `/scripts/extract_uvp.py` - UVP and keyword extraction
- `/scripts/classify_vertical.py` - Industry classification
- `/scripts/score_pain_signals.py` - Pain signal quantification
- `/scripts/research_planner.py` - NLP-driven research planning
