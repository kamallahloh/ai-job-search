# Search Queries for Job Scraper

<!-- SETUP: Customize these queries based on your skills, target roles, and location -->

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`; Danish demos and any skill you add with `/add-portal` are included the same way. You do **not** need a matching `site:` line below for those CLIs to run.

The `site:` query templates in this file are the **WebSearch fallback** — for portals without a CLI, company career pages, or when a CLI fails.

## Search Sites

There is no built-in scraper CLI for Jordan/MENA job portals (the framework's `.agents/skills/` tools are Denmark-specific: Jobindex, Jobbank, Jobdanmark, Jobnet). Use these instead:

Primary (LinkedIn + Google site-search):
- **linkedin.com/jobs** - filter by Jordan / Amman / Remote, and by target companies
- Google `site:` searches against LinkedIn jobs and target company career pages

Secondary (MENA job boards):
- **bayt.com** - largest MENA job board
- **wuzzuf.net** - popular in Egypt/Levant, strong tech listings
- **akhtaboot.com** - Jordan-focused job board
- **tanqeeb.com** - MENA-wide job board

## Query Categories

Queries are grouped by priority. Kamal is open to relocation, so location terms are optional per query - use them to narrow to Amman/Jordan when useful, or drop them for remote/international roles.

### Priority 1: Full Stack / .NET Developer

Strongest and most desired career direction - matches current role at Marshal Travel.

```
site:linkedin.com/jobs "Full Stack Developer" ".NET" Jordan OR remote
site:linkedin.com/jobs "ASP.NET" developer Amman OR remote
site:bayt.com "Full Stack .NET Developer"
site:wuzzuf.net ".NET Developer"
```

### Priority 2: Broader Full-Stack / JavaScript Ecosystem

Kamal's skills span React/Next.js/Node.js/Vue.js as well as .NET - keep this net wide rather than narrowing to .NET only.

```
site:linkedin.com/jobs "Full Stack Developer" React OR "Next.js" OR Vue Jordan OR remote
site:linkedin.com/jobs "Software Developer" Node.js Amman OR remote
site:bayt.com "Full Stack Developer"
site:akhtaboot.com "Software Developer"
```

### Priority 3: Cloud / Solutions Architecture

Adjacent direction Kamal wants to grow into, backed by AWS Solutions Architect - Associate and Cloud Practitioner certifications.

```
site:linkedin.com/jobs "Solutions Architect" AWS Jordan OR remote
site:linkedin.com/jobs "Cloud Engineer" AWS Amman OR remote
site:tanqeeb.com "Solutions Architect"
```

### Priority 4: Target Companies (direct monitoring)

Check career pages and LinkedIn company pages directly for these:

```
site:linkedin.com/jobs "Software Developer" (Amazon OR AWS OR Google OR Microsoft)
site:linkedin.com/jobs "Software Developer" (Estarta OR ProgressSoft OR "Integrated Technology Group" OR ESKADENIA)
site:linkedin.com/jobs "Software Developer" (Careem OR TaxiF OR Talabat)
```

Target companies list:
- **Big Tech / Cloud:** Amazon, AWS, Google, Microsoft
- **Jordan/MENA Tech:** Estarta, ProgressSoft, Integrated Technology Group (ITG), ESKADENIA
- **Tech-enabled consumer platforms:** Careem, TaxiF, Talabat

## Location Filter

Kamal is **open to relocation**, so location is a soft filter, not a hard pass/fail:
- **Ideal:** Amman, Jordan (no relocation needed) or fully remote
- **Acceptable:** Other MENA/Gulf hubs with relocation support (Dubai, Riyadh, Doha, Cairo)
- **Acceptable:** International roles (US/EU) that sponsor relocation or hire fully remote
- **Borderline:** International roles requiring self-funded relocation - flag for discussion
- **Too far:** none by distance - the real filter is relocation support and company stability, not geography

## Deal-Breakers (screen out during evaluation)

- No growth or learning path - purely maintenance work with no exposure to new tech/skills
- Unstable or very early-stage companies (high layoff/instability risk)

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape [focus_area]" -> relevant category queries + custom focus-specific queries
