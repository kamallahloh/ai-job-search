---
framework_version: 1.0.0
---

# Job Evaluation Framework

<!-- SETUP: Skill match areas and career goals are personalized by running /setup -->

## Scoring Dimensions

Evaluate each job posting against these five dimensions:

### 1. Technical Skills Match (0-100)
How well do the required/preferred skills align with the candidate's capabilities?

| Score | Meaning |
|-------|---------|
| 80-100 | Core requirements are primary skills |
| 60-79 | Most requirements match, 1-2 gaps that are learnable |
| 40-59 | Partial match, significant upskilling needed |
| 0-39 | Fundamental mismatch |

**Strong match areas:** C#/.NET (Core, MVC, Web API, Web Forms, Razor Pages, EF), JavaScript/TypeScript (React, Next.js, Vue.js, Node.js, Express.js, Nest.js), SQL Server/PostgreSQL/Oracle/MongoDB, REST API integration, AWS (Cloud Practitioner + Solutions Architect Associate)
**Moderate match areas:** Real-time/integration tooling (SignalR, Socket.io, OAuth2), IIS deployment, GIS domain knowledge, Delphi/Object Pascal, Agile/Scrum project delivery
**Weak match areas:** Deep ML/data science, large-scale distributed systems, DevOps/CI-CD ownership, mobile development

### 2. Experience Match (0-100)
Does work history align with what they're looking for?

| Score | Meaning |
|-------|---------|
| 80-100 | Direct experience in the same domain and role type |
| 60-79 | Related experience, transferable skills clear |
| 40-59 | Adjacent experience, would need to make the case |
| 0-39 | Unrelated experience |

**Strong:** Enterprise .NET integration development (Marshal Travel); full-stack ownership across .NET/JS ecosystems
**Moderate:** Legacy-to-modern stack maintenance and GIS domain work (GCE); desktop ERP/PoS development (SmartSoft); cloud/solutions architecture (AWS-certified, not yet applied on the job)
**Entry-level:** Pure cloud/DevOps engineering roles (certified but no hands-on production experience yet)

### 3. Behavioral/Culture Fit (0-100)
Does the role and company culture match the behavioral profile?

| Score | Meaning |
|-------|---------|
| 80-100 | Culture strongly matches behavioral preferences |
| 60-79 | Mixed signals but mostly compatible |
| 40-59 | Some friction areas |
| 0-39 | Significant culture mismatch |

**Red flags to research:** Department disorganization, work dominated by maintenance over development, poor chemistry with leadership, culture mismatches. Check reviews, media coverage, LinkedIn connections, and network contacts for insider perspective.

### 4. Location & Logistics (Pass/Fail + Notes)
- Within commute range: PASS
- Remote with occasional office: PASS
- Requires relocation: FAIL (deal-breaker)
- Frequent international travel: FLAG (discuss with user)

### 5. Career Alignment & Motivation (0-100)
Does this role advance career goals and contain tasks that energize?

| Score | Meaning |
|-------|---------|
| 80-100 | Strongly aligned with career direction, clear growth path |
| 60-79 | Good role but only partially aligned with long-term goals |
| 40-59 | Decent job but doesn't build toward career goals |
| 0-39 | Dead end or backwards step |

**Career goals:**
- Apply AWS certifications (Cloud Practitioner, Solutions Architect - Associate) toward cloud/solutions architecture work
- Own full-stack features end-to-end, from database to UI
- Keep learning new stacks and technologies, ideally at an international company with well-established workflows

**Motivation filter:** Evaluate not just whether you *can* do the tasks, but whether the tasks will *energize* you. Consider:
- Tasks that energize: cloud/architecture work, full-stack ownership, learning new stacks and technologies
- Tasks that drain: purely maintenance work with no exposure to new tech/skills
- Non-task factors: leadership style, department culture, company values, degree of autonomy

**Life situation alignment:** Consider personal constraints:
- **Security**: Currently employed (Software Developer, Marshal Travel) - passively open, not job-search-urgent, can be selective
- **Flexibility**: Open to relocation; no hard commute constraint
- **Professional development**: Actively pursuing AWS certifications; prioritizes roles with a genuine learning/growth path over stable-but-static ones

### 6. Salary Benchmark (Optional)

If the salary lookup tool is configured (`salary_data.json` exists), look up the company:
```
python salary_lookup.py "<Company Name>" --json
```

If a city is known from the posting, add `--city "<City>"` to narrow results.

Present findings as:
```
### Salary Benchmark
| Metric | Value |
|--------|-------|
| [Category] index | XX.X (+/-X.X% vs baseline) |
| Overall index | XX.X (+/-X.X% vs baseline) |
```

Interpret results relative to the baseline defined in the data file's metadata. For index-based data, higher typically means above-market compensation.

If the salary tool is not configured, skip this section.

## Output Format

Present the evaluation as:

```
## Job Fit Evaluation: [Role] at [Company]

| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Skills | XX/100 | [brief note] |
| Experience Match | XX/100 | [brief note] |
| Behavioral Fit | XX/100 | [brief note] |
| Location | PASS/FAIL | [brief note] |
| Career Alignment | XX/100 | [brief note] |

**Overall Score: XX/100** (weighted average of scored dimensions)

### Verdict: [Strong Fit / Good Fit / Moderate Fit / Weak Fit / Poor Fit]

### Key Strengths for This Role
- [bullet points]

### Gaps to Address
- [bullet points]

### Recommendation
[1-2 sentences: apply/skip/apply with caveats]

### Company Research Checklist
- [ ] Checked company website (mission, values, recent news)
- [ ] Checked review sites (Glassdoor, Jobindex, etc.)
- [ ] Checked LinkedIn for team size, recent hires, connections
- [ ] Checked media for restructuring, growth, or workplace issues
- [ ] Identified network contacts who may know the team/manager
```

## Calibration from Past Applications
- Marshal Travel's "Full Stack .NET Developer - Integration-Heavy" posting (C#/ASP.NET, Vue.js, SignalR, IIS, SQL Server/EF, payment gateway integrations) led to a hire (Jan 2026) - confirmed strong-fit signal for similarly-scoped .NET integration roles.
- SmartSoft (Software Developer, Delphi/Object Pascal + Oracle DB) and GCE (Software Developer, GIS/legacy-and-modern-stack) both led to hires in 2024 - confirms generalist "Software Developer" postings convert well even when the stack is unfamiliar going in (Delphi, legacy ASP.NET Web Forms), as long as the role offers genuine skill growth.
- MENAFN (Full Stack Developer) and UBA (Backend Developer) both reached full offer stage in May 2024 - confirmed strong-fit signal for full-stack/backend developer postings specifically. Both were declined for reasons unrelated to fit (compensation, and the role's project being postponed), not skill gaps.
- GoldenTik (Software Developer, 2026) reached offer stage while already employed - confirms the current .NET/full-stack profile remains competitive in the market well past the bootcamp era, not just as a fresh graduate.
- Earlier 2024 applications covering a very wide spread of unrelated junior roles (Java Developer, Junior Laravel Developer, Front-End Angular, Research Analyst, Junior Project Coordinator, Associate Product Operations) still have no recorded outcomes and remain excluded from calibration. The wide-net phase produced real signal specifically in Full Stack/Backend/Software Developer postings (5 of 6 tracked outcomes above), not in the scattered adjacent-role applications.

## Weighting
- Technical Skills: 30%
- Experience Match: 25%
- Behavioral Fit: 15%
- Career Alignment: 30%

(Location is pass/fail, not weighted)

## Thresholds
- **Strong Fit** (75+): Definitely apply, tailor everything
- **Good Fit** (60-74): Apply, address gaps in cover letter
- **Moderate Fit** (45-59): Consider carefully, discuss with user
- **Weak Fit** (30-44): Probably skip unless strategic reasons
- **Poor Fit** (<30): Skip

## Pre-Application: Call the Employer (Best Practice)

Before writing the application, consider whether the candidate should call the contact person listed in the posting. **Only call if there are substantive questions** - never call just to "be remembered."

### When to Suggest Calling
- The posting has unclear or ambiguous requirements
- It's unclear which competencies are essential vs. nice-to-have
- The role description is vague about day-to-day tasks
- There's a named contact person who invites questions

### Good Questions to Ask
- "What are the primary challenges in this role?"
- "How is time typically divided across the listed responsibilities?"
- "Which competencies are most critical for success in this position?"
- "What does success look like in the first 6-12 months?"

### Rules for the Call
- Prepare a 30-second "elevator pitch" about your background in case they ask
- The call's purpose is **gathering information**, not delivering a pitch
- Take notes - use what you learn to tailor the application
- Reference the conversation naturally in the cover letter ("After speaking with [name], I was especially drawn to...")
