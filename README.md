# Sales Skills for Claude Code

A collection of AI agent skills focused on B2B sales tasks. Built for sales professionals, SDRs, AEs, and revenue leaders who want Claude Code (or similar AI coding assistants) to help with prospecting, discovery, deal execution, pipeline management, and closing.

Built by [Apparate](https://apparate.com.au?ref=salesskills).

**Contributions welcome!** Found a way to improve a skill or have a new one to add? [Open a PR](#contributing).

## What are Skills?

Skills are markdown files that give AI agents specialized knowledge and workflows for specific tasks. When you add these to your project, Claude Code can recognize when you're working on a sales task and apply the right frameworks, methodologies, and best practices.

## Available Skills

| Skill | Description | Triggers |
|-------|-------------|----------|
| [ab-test-setup](skills/ab-test-setup/) | Plan and run sales experiments | "sales test," "outreach experiment," "A/B test emails" |
| [analytics-tracking](skills/analytics-tracking/) | Pipeline reporting and sales metrics | "pipeline metrics," "sales dashboard," "forecast" |
| [competitor-alternatives](skills/competitor-alternatives/) | Competitive selling and positioning | "vs competitor," "battle card," "competitive deal" |
| [copy-editing](skills/copy-editing/) | Refine sales communications | "edit my email," "review my proposal," "polish outreach" |
| [copywriting](skills/copywriting/) | Sales messaging and value propositions | "value prop," "sales messaging," "pitch deck copy" |
| [email-sequence](skills/email-sequence/) | Build prospecting sequences | "outreach sequence," "cold email," "follow-up cadence" |
| [form-cro](skills/form-cro/) | Optimize lead qualification forms | "qualification form," "lead scoring," "intake form" |
| [free-tool-strategy](skills/free-tool-strategy/) | Sales enablement tools | "sales tools," "demo environment," "ROI calculator" |
| [launch-strategy](skills/launch-strategy/) | New product sales launches | "product launch," "GTM strategy," "sales rollout" |
| [marketing-ideas](skills/marketing-ideas/) | 100+ sales tactics and strategies | "sales tactics," "prospecting ideas," "pipeline generation" |
| [marketing-psychology](skills/marketing-psychology/) | Sales psychology and buyer behavior | "buyer psychology," "objection handling," "negotiation" |
| [onboarding-cro](skills/onboarding-cro/) | Customer onboarding and implementation | "customer onboarding," "implementation," "time-to-value" |
| [page-cro](skills/page-cro/) | Optimize sales pages and proposals | "proposal optimization," "sales page," "one-pager" |
| [paid-ads](skills/paid-ads/) | Paid lead generation for sales | "paid leads," "LinkedIn ads," "lead gen campaigns" |
| [paywall-upgrade-cro](skills/paywall-upgrade-cro/) | Account expansion and upselling | "upsell," "expansion," "cross-sell," "land and expand" |
| [popup-cro](skills/popup-cro/) | Lead capture and meeting conversion | "meeting booking," "demo request," "lead capture" |
| [pricing-strategy](skills/pricing-strategy/) | Pricing negotiation and value defense | "pricing objection," "discount request," "negotiation" |
| [programmatic-seo](skills/programmatic-seo/) | Sales playbook development | "sales playbook," "sales process," "methodology" |
| [referral-program](skills/referral-program/) | Customer referrals and partner sales | "referral," "partner sales," "channel sales" |
| [schema-markup](skills/schema-markup/) | Deal documentation and CRM best practices | "CRM," "deal notes," "pipeline hygiene" |
| [seo-audit](skills/seo-audit/) | Deal review and win/loss analysis | "win/loss," "deal review," "pipeline audit" |
| [signup-flow-cro](skills/signup-flow-cro/) | Sales process optimization | "sales process," "deal flow," "cycle reduction" |
| [social-content](skills/social-content/) | Social selling and LinkedIn prospecting | "LinkedIn," "social selling," "warm prospecting" |

## Installation

### Option 1: CLI Install (Recommended)

Use [add-skill](https://github.com/vercel-labs/add-skill) to install skills directly:

```bash
# Install all skills
npx add-skill louisblythe/salesskills

# Install specific skills
npx add-skill louisblythe/salesskills --skill pricing-strategy competitive-selling

# List available skills
npx add-skill louisblythe/salesskills --list
```

This automatically installs to your `.claude/skills/` directory.

### Option 2: Claude Code Plugin

Install via Claude Code's built-in plugin system:

```bash
# Add the marketplace
/plugin marketplace add louisblythe/salesskills

# Install all sales skills
/plugin install sales-skills
```

### Option 3: Clone and Copy

Clone the entire repo and copy the skills folder:

```bash
git clone https://github.com/louisblythe/salesskills.git
cp -r salesskills/skills/* .claude/skills/
```

### Option 4: Git Submodule

Add as a submodule for easy updates:

```bash
git submodule add https://github.com/louisblythe/salesskills.git .claude/salesskills
```

Then reference skills from `.claude/salesskills/skills/`.

### Option 5: Fork and Customize

1. Fork this repository
2. Customize skills for your specific sales process
3. Clone your fork into your projects

## Usage

Once installed, just ask Claude Code to help with sales tasks:

```
"Help me write a cold outreach sequence for CFOs"
→ Uses email-sequence skill

"How should I handle a pricing objection?"
→ Uses pricing-strategy skill

"Create a competitive battle card vs Salesforce"
→ Uses competitor-alternatives skill

"Review this deal and tell me what's missing"
→ Uses seo-audit (deal-review) skill

"Help me prepare for a discovery call"
→ Uses marketing-psychology (sales-psychology) skill
```

You can also invoke skills directly:

```
/pricing-strategy
/email-sequence
/competitor-alternatives
```

## Skill Categories

### Prospecting & Outreach
- `email-sequence` - Cold outreach and follow-up sequences
- `social-content` - LinkedIn prospecting and social selling
- `marketing-ideas` - 100+ sales tactics and pipeline generation
- `popup-cro` - Lead capture and meeting booking optimization

### Discovery & Qualification
- `marketing-psychology` - Sales psychology and buyer behavior
- `form-cro` - Lead qualification and scoring
- `signup-flow-cro` - Sales process optimization

### Competitive Selling
- `competitor-alternatives` - Battle cards and competitive positioning
- `copywriting` - Value propositions and differentiation

### Deal Execution
- `pricing-strategy` - Negotiation and value defense
- `page-cro` - Proposals and sales collateral
- `schema-markup` - CRM documentation and deal hygiene
- `programmatic-seo` - Sales playbooks and methodology

### Pipeline Management
- `analytics-tracking` - Pipeline metrics and forecasting
- `seo-audit` - Win/loss analysis and deal reviews
- `ab-test-setup` - Sales experimentation

### Account Growth
- `paywall-upgrade-cro` - Expansion and upselling
- `onboarding-cro` - Customer onboarding and implementation
- `referral-program` - Referrals and partner sales

### Sales Enablement
- `free-tool-strategy` - Demo environments and sales tools
- `launch-strategy` - New product GTM and sales rollout
- `paid-ads` - Paid lead generation
- `copy-editing` - Sales communication refinement

## Sales Methodologies Included

These skills incorporate proven sales frameworks:

- **BANT** - Budget, Authority, Need, Timeline
- **MEDDIC** - Metrics, Economic Buyer, Decision Criteria, Decision Process, Identify Pain, Champion
- **SPICED** - Situation, Pain, Impact, Critical Event, Decision
- **SPIN** - Situation, Problem, Implication, Need-Payoff
- **Challenger Sale** - Teach, Tailor, Take Control
- **Gap Selling** - Current State → Future State

## Contributing

Found a way to improve a skill? Have a new skill to suggest? PRs and issues welcome!

**Ideas for contributions:**
- Improve existing skill instructions or frameworks
- Add new objection handling scripts
- Add industry-specific variations
- Fix typos or clarify confusing sections
- Suggest new skills (open an issue first to discuss)
- Add examples or case studies

**How to contribute:**
1. Fork the repo
2. Edit the skill file(s)
3. Submit a PR with a clear description of what you improved

### Skill File Structure

Each skill is a directory containing a `SKILL.md` file:

```
skills/
  skill-name/
    SKILL.md
```

The `SKILL.md` file follows this format:

```markdown
---
name: skill-name
description: One-line description for skill selection
---

# Skill Name

[Full instructions for the AI agent]
```

## License

MIT - Use these however you want.
