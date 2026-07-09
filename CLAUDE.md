# Job Application Assistant for Kamal Lahloh

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for Kamal Lahloh, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

<!-- This section is auto-populated by /setup. You can also fill it in manually. -->

### Identity
- **Name:** Kamal Lahloh (legal name: Kamal Mahmoud Abdel Fattah Lahloh)
- **Location:** Amman, Jordan (open to relocation)
- **Languages:** Arabic (Native), English (Professional Working), Japanese (Elementary)
- **Status:** Employed (Software Developer, Marshal Travel) - passively open to new opportunities
- **LinkedIn headline:** "Software Developer at Marshal || MERAKI || AWS SAA-C03"

### Education
<!-- List your degrees, most recent first -->
- **Full-Stack Web Development Bootcamp** (Oct 2023-Mar 2024) - MERAKI Academy
  - 22-week immersive program, 400+ hours; MERN/PERN stacks, Agile/Scrum
- **Bachelor of Engineering (BE) in Civil Engineering** (Sep 2009-Jan 2014) - The Hashemite University

### Professional Experience
<!-- List your roles, most recent first -->
- **Software Developer** (Jan 2026 - Present) - **Marshal Travel** (Amman, Jordan)
  - Full Stack .NET Developer on an integration-heavy enterprise platform (Portal, API, Backoffice)
  - C#, ASP.NET MVC/Web API, Vue.js in Razor views, SignalR, IIS, SQL Server + Entity Framework
  - Third-party API and payment gateway integrations
- **Software Developer** (Oct 2024 - Dec 2025) - **General Computers and Electronics Co. (GCE)** (Amman, Jordan)
  - (GIS) Geographical Information Systems Department (renamed Innovation, AI and DTS Department)
  - TypeScript, Next.js, .NET 8; maintained legacy ASP.NET Web Forms/MVC/Razor Pages
- **Software Developer** (Jun 2024 - Oct 2024) - **SmartSoft Technologies** (Amman, Jordan)
  - Delphi/Object Pascal and Oracle Database for desktop ERP/PoS solutions
- **Project Manager, Sr. Civil Engineer** (Aug 2014 - Mar 2024) - **Construction Industry** (Jordan & Saudi Arabia)
  - ~9.5 years of project management and civil engineering prior to transitioning into software development

### Technical Skills
- **Primary:** C#/.NET (Core, MVC, Web API, Web Forms, Razor Pages, EF), JavaScript/TypeScript (React, Next.js, Vue.js, Node.js, Express.js, Nest.js)
- **Secondary:** SignalR, Socket.io, OAuth2, IIS deployment, Delphi/Object Pascal, Agile/Scrum
- **Domain:** Full-stack web development, GIS, enterprise .NET integrations, cloud/solutions architecture (AWS)
- **Software:** MongoDB, PostgreSQL, Oracle DB, SQL Server, Git/GitHub, Postman, Trello, Cloudinary

### Certifications
<!-- List relevant certifications with dates -->
- **AWS Certified Cloud Practitioner (CLF-C02)** - completed Feb 14, 2026 (expires Feb 14, 2029)
- **AWS Certified Solutions Architect - Associate (SAA-C03)** - completed May 31, 2026 (expires May 31, 2029)
- **Full-Stack Web Development Bootcamp** - 400h+ - completed Mar 7, 2024 (MERAKI Academy)
- **GCE Security Awareness Training**

### Publications
<!-- None on record -->

### Awards
<!-- None on record -->

### Behavioral Profile
<!-- No formal assessment on record yet; inferred signals below, see 02-behavioral-profile.md -->
- **Eager learner** - repeatedly picks up new stacks quickly (civil engineering -> MERN/PERN -> Delphi/Oracle -> .NET/GIS -> .NET integrations)
- **Organized and detail-focused** - self-described as highly organized and deeply focused
- **Strengths:** Comfortable both leading (SCRUM master) and working solo end-to-end
- **Growth areas:** [YOUR_GROWTH_AREAS]
- **Thrives in:** International companies with well-established workflows

### What Excites You
<!-- What motivates you professionally -->
- Cloud/architecture work - applying AWS certifications toward solutions architecture
- Full-stack ownership - owning features end-to-end from database to UI
- Learning new stacks and technologies
- Working with an international company that has well-established workflows

### Target Sectors
<!-- Industries and companies you're targeting -->
- Big Tech / Cloud: Amazon, AWS, Google, Microsoft
- Jordan/MENA Tech: Estarta, ProgressSoft, Integrated Technology Group (ITG), ESKADENIA
- Tech-enabled consumer platforms: Careem, TaxiF, Talabat

### Deal-breakers
<!-- Hard constraints on job search -->
- No growth or learning path (purely maintenance work with no exposure to new tech/skills)
- Unstable or very early-stage companies (high layoff/instability risk)

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - a job/education title must never sit at the bottom of a page with its bullets spilling to the next page. Use `\needspace{5\baselineskip}` before each `\cventry` to prevent this, and `\enlargethispage{2-3\baselineskip}` to rescue a trailing section that just barely spills
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`

### ATS & keyword verification (CV)
ATS parsers read the PDF's embedded text layer, not the rendered page. Extract it with `pdftotext -layout` and verify what a parser sees. `pdftotext` (poppler) is optional - if missing, skip the parseability items with a warning and check keyword coverage from the visual PDF read instead.
- [ ] CV text layer extracts cleanly - no `(cid:*)` markers, `�` replacement characters, or text visible in the PDF but absent from the extraction
- [ ] Email and phone appear as **literal text** in the extraction (icon-glyph noise like `MOBILE-ALT`/`Envelope` is harmless, but a contact detail carried only by an icon or hyperlink is invisible to ATS)
- [ ] Reading order of the extracted text matches the visual order (single-column stock template is safe; multi-column custom templates are where this breaks)
- [ ] Posting keywords covered or honestly absent - synonym-only matches tightened to the posting's exact term where truthfully applicable, keywords the profile genuinely supports added to experience bullets, genuine gaps left visible and **never stuffed**
