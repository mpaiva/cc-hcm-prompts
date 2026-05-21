# Recruiting & Applicant Tracking Screen Prompts

> **Design Principle**: Each screen prioritizes WCAG 2.2 AA accessibility. All prompts include specific accessibility guidance inline with feature descriptions.

---

## SCREEN 1: Job Posting Creation/Management

### Purpose & User Context
Enable recruiters and hiring managers to create, edit, publish, and manage job postings across multiple job boards with AI-assisted job descriptions and market-rate salary suggestions.

**Primary Users:**
- Recruiters (creating postings, publishing to boards)
- Hiring Managers (approving postings, setting requirements)

**Secondary Users:**
- HR Managers (managing job board integrations)
- Finance (budget approval for positions)

### Key User Workflows

#### Workflow A: Create New Job Posting
1. Recruiter clicks "Create Job"
2. Fills basic info (title, department, location, salary range)
3. Uses AI to generate/enhance job description
4. Adds requirements (skills, experience, education)
5. Configures publishing (which job boards, internal career site)
6. Sets application deadline and hiring manager
7. Submits for approval (if required)
8. Publishes when approved

#### Workflow B: Edit Existing Posting
1. Recruiter views active posting
2. Updates job description, requirements, or salary
3. AI suggests optimal changes for candidate matching
4. Republishes or schedules update
5. Tracks what changed and when

#### Workflow C: Job Posting Analytics
1. Recruiter/hiring manager views posting performance
2. Sees: views, applications, application rate, time-to-fill
3. AI suggests improvements: "Salary range too low for market"
4. Can A/B test different descriptions

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  JOB POSTING MANAGER                                   [Help]     │
├─────────────────────────────────────────────────────────────────┤
│  [Create New Job] [View Analytics] [Draft Postings] [Published] │
│                                                                   │
│  ACTIVE POSTINGS (5)                                             │
│  ─────────────────────────────────────────────────────────────   │
│  Senior Software Engineer - Remote                               │
│  Posted: 8 days ago | Views: 342 | Apps: 47 | Rate: 13.7%       │
│  Status: Active (Closes in 22 days)                              │
│  [View Details] [Edit] [Analytics] [Close Early]                 │
│                                                                   │
│  Product Manager - NYC Office                                    │
│  Posted: 3 days ago | Views: 156 | Apps: 12 | Rate: 7.7%        │
│  Status: Active | AI Insight: Low app rate - consider salary ↑  │
│  [View Details] [Edit] [Analytics] [Boost]                       │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  CREATE NEW JOB POSTING                                          │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Step 1 of 4: Basic Information                                  │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Job Title *                [Senior Software Engineer________]   │
│  Department *               [Engineering ▼]                      │
│  Location *                 [Remote / NYC / San Francisco ▼]     │
│  Job Type *                 [Full-Time ▼]                        │
│  Hiring Manager *           [Start typing...] (autocomplete)      │
│  Salary Range (optional)    From: [$______] To: [$______]        │
│  Application Deadline *     [________] (date picker)             │
│                                                                   │
│  [Next: Job Description] [Cancel]                                │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  Step 2 of 4: Job Description                                    │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  [✨ AI Generate Description]  [Import from Template]             │
│                                                                   │
│  Job Description *          [Rich Text Editor________________]   │
│                             [B I U Link Insert Table]             │
│                             [_________________________________]   │
│                             [_________________________________]   │
│                                                                   │
│  AI Suggestions:                                                  │
│  ├─ "Add 'Remote flexibility' - top candidates expect this"      │
│  ├─ "Highlight learning culture - common attractor"              │
│  └─ "Add specific tools: React, Python, AWS - improves matching" │
│                                                                   │
│  [Accept Suggestions] [Skip]                                     │
│                                                                   │
│  [Previous] [Next: Requirements] [Save Draft]                    │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  Step 3 of 4: Requirements & Skills                              │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Required Skills *          [+ Add Skill]                        │
│                             □ Python (5+ years)  [Remove]        │
│                             □ React (3+ years)   [Remove]        │
│                             □ AWS (2+ years)     [Remove]        │
│                                                                   │
│  Nice-to-Have Skills        [+ Add Skill]                        │
│                             □ Kubernetes        [Remove]         │
│                             □ TypeScript        [Remove]         │
│                                                                   │
│  Education                  [Bachelor's Degree ▼]                │
│  Experience Level *         [Senior (5+ years) ▼]                │
│  Travel Required            [No ▼]                               │
│  Security Clearance         [None ▼]                             │
│                                                                   │
│  [Previous] [Next: Publishing] [Save Draft]                      │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  Step 4 of 4: Publishing Settings                                │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Publishing Channels        [✓] Careers Site                     │
│                             [✓] LinkedIn (costs $200/30 days)    │
│                             [✓] Indeed                           │
│                             [ ] Glassdoor                        │
│                             [ ] GitHub Jobs                      │
│                                                                   │
│  Publishing Date            [Publish Immediately ▼]             │
│  Application Method         [Online Form ▼]                      │
│  Show Salary in Posting     [Yes ▼]                              │
│                                                                   │
│  Review & Submit:                                                │
│  Job Title: Senior Software Engineer                             │
│  Location: Remote | Salary: $150K-$200K                         │
│  Posted to: 3 boards | Deadline: Feb 15, 2024                   │
│  Hiring Manager: Sarah Chen                                      │
│                                                                   │
│  [Require Approval] [Publish Now] [Save Draft] [Cancel]          │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Job Posting List
**For Each Posting:**
- Title, department, location, job type
- Posted date, deadline
- Performance metrics: views, applications, application rate
- Status (draft, active, closed, filled, expired)
- AI insights (if underperforming)
- Quick action buttons

#### 2. Multi-Step Form
**Step 1: Basic Info**
- Title, department, location, type, hiring manager
- Salary range (optional but recommended)
- Application deadline

**Step 2: Job Description**
- Rich text editor with formatting
- AI generation: "Optimize this description for candidates"
- AI suggestions for improvement (inline)
- Template library import

**Step 3: Requirements**
- Required skills (searchable dropdown, add custom)
- Nice-to-have skills
- Education level, experience years
- Special requirements (travel, clearance, etc.)

**Step 4: Publishing**
- Select job boards to post to (multi-select)
- Publish immediately or schedule
- Show/hide salary
- Approval routing if required

#### 3. AI Features

**Description Generation:**
- "Optimize job description for [role]"
- Suggests must-have content (responsibilities, benefits, culture)
- Auto-extracts skills from description

**Market Analysis:**
- Suggests salary range based on location, experience, skills
- Flags if salary too low: "Below market for Senior Eng in SF (+$30K)"
- Compares to competitor postings (anonymized)

**Performance Insights:**
- "This posting has 40% lower app rate than similar roles"
- Suggests improvements: "Add remote flexibility", "Highlight learning culture"
- Predicts time-to-fill: "This posting typically takes 35 days to fill"

**Duplicate Detection:**
- Warns if similar role already posted
- Suggests reusing description or combining into one posting

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Form Steps**: Clear step indicator (1 of 4) with heading
- **Rich Text Editor**: Accessible toolbar with keyboard shortcuts (Ctrl+B for bold, etc.)
- **Skill Tags**: Use text labels, not color alone
- **Performance Metrics**: Numbers clearly readable (not tiny)
- **AI Suggestions**: Use text labels, not icon alone
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Tab Order**: Title → Department → Location → ... → Submit
- **Rich Editor**: Tab enters editor, then tabs through formatting buttons, Escape to exit
- **Skill Addition**: Tab to "Add Skill" button, Enter to add, Tab through list
- **Radio/Select**: Arrow keys to navigate options, Enter to select
- **Focus**: Clear 2px border on all focused elements

#### Screen Reader Compatibility
- **Form Steps**: `<fieldset>` with `<legend>` for each step
- **Labels**: Explicit `<label for="job_title">` for all fields
- **Rich Editor**: `role="region" aria-label="Job Description Editor"`
- **AI Suggestions**: `role="status" aria-live="polite"` for suggestions appearing
- **Skill List**: `<ul>` with `aria-label="Required Skills: 3 items"`

#### Focus Management
- **Step 1 Load**: Focus on Job Title field
- **Step Submission**: Focus moves to first field of next step
- **Error**: Focus on first field with error + announce error message
- **Modal**: Focus trap in modal, focus returns to trigger on close

#### Error States
- **Required Fields**: Marked with asterisk AND `aria-required="true"`
- **Invalid Salary**: "Minimum must be less than maximum"
- **Missing Deadline**: "Application deadline is required"
- **Form Validation**: Inline feedback as user types

#### Motion & Animation
- **Step Transitions**: Instant or simple fade (honor `prefers-reduced-motion`)
- **AI Suggestions**: No animated loading bars, use text status
- **Rich Editor**: No animations in toolbar

#### Touch Accessibility
- **Buttons**: 44x44px minimum ([Next], [Previous], [Publish])
- **Form Fields**: 44px height, width sufficient for content
- **Skill Tags**: 48x48px minimum tap targets
- **Select Dropdowns**: Large hit area (44x44px)

### Data Model & Inputs

**Job Posting:**
- Job ID, title, department, location
- Job type (full-time, contract, etc.)
- Description (rich text)
- Salary min/max, salary currency
- Required/nice-to-have skills (list)
- Education, experience level
- Hiring manager ID
- Application deadline, posted date
- Status (draft, active, closed, filled)
- Publishing channels (LinkedIn, Indeed, etc.)
- Board-specific URLs

**Posting Metrics:**
- Views count, application count
- Application rate, time-to-fill
- Source tracking (which board generated best candidates?)

### Data Outputs & Integrations

**Job Board Integrations:**
- LinkedIn API: Post and sync applications
- Indeed XML feed: Automated posting
- Glassdoor: Job sync
- Internal careers site: Auto-populated

**Recruiter Dashboard:**
- Active postings, performance metrics, aging

**Candidate-Facing:**
- Job listing (read-only) on careers site and job boards

### Edge Cases & Error Handling

1. **Job Board Integration Fails**
   - Status: "⚠️ Failed to post to LinkedIn - will retry in 1 hour"
   - Manual fallback: "Post manually" with link to board

2. **Posting Expires Without Close**
   - Auto-close after deadline
   - Keep in "closed" state for analytics

3. **Salary Range Too Wide**
   - Alert: "Range >$100K may deter qualified candidates"
   - Suggest tightening range

### Inter-Screen Interactions

- **Triggers**: Job Posting View (candidate-facing), Applications Dashboard
- **Linked to**: Requisition management, budget tracking
- **Data feeds**: Job boards, careers site

---

## SCREEN 2: Job Posting View (Candidate)

### Purpose & User Context
Present job posting to candidates with clear information, apply button, and personalized recommendations for similar opportunities.

**Primary Users:**
- Job Seekers (anonymous and registered)

**Secondary Users:**
- Recruiters (track views, manage candidate interest)

### Key User Workflows

#### Workflow A: Browse & Apply
1. Candidate finds posting on career site or job board
2. Reviews full details (title, description, requirements, salary, benefits)
3. Sees AI match score ("You're a 92% match for this role")
4. Clicks "Apply"
5. Signs up/logs in if needed
6. Submits application

#### Workflow B: Save for Later
1. Candidate browses posting
2. Clicks "Save Job"
3. Added to saved jobs list
4. Email reminder to apply later

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  JOB POSTING: Senior Software Engineer                          │
│  [← Back to Results] [Share] [Save] [Report Job]                 │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Senior Software Engineer                                         │
│  at [Company Name] · Remote                                      │
│  $150,000 - $200,000 per year                                    │
│                                                                   │
│  [📌 Save Job] [⬈ Share] [Apply Now]                            │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  YOUR MATCH: 92% [████████░] Excellent fit for your skills!     │
│  You have 7 of 8 required skills. Missing: Kubernetes           │
│  [View Skill Analysis]                                           │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  JOB DETAILS                                                      │
│  ─────────────────────────────────────────────────────────────   │
│  Job Type: Full-Time                                             │
│  Experience Level: Senior (5+ years)                             │
│  Location: Remote (Candidates worldwide)                         │
│  Posted: 8 days ago | Deadline: Feb 15, 2024                    │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  ABOUT THE ROLE                                                   │
│  ─────────────────────────────────────────────────────────────   │
│  We're looking for a Senior Software Engineer to lead our        │
│  platform infrastructure team. You'll architect scalable         │
│  systems, mentor junior engineers, and drive technical          │
│  excellence across the organization.                             │
│                                                                   │
│  Key Responsibilities:                                           │
│  • Design and implement high-performance backend services        │
│  • Lead code reviews and mentor team members                     │
│  • Collaborate with product and design on technical feasibility  │
│  • Optimize database queries and improve system performance      │
│  • Own deployment pipelines and infrastructure-as-code           │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  ABOUT YOU                                                        │
│  ─────────────────────────────────────────────────────────────   │
│  Required Skills & Experience:                                   │
│  ✓ Python (5+ years)                                             │
│  ✓ React (3+ years)                                              │
│  ✓ AWS (2+ years)                                                │
│  ✓ System Design & Architecture                                  │
│  ✓ Leadership or mentorship experience                           │
│                                                                   │
│  Nice-to-Have:                                                   │
│  • Kubernetes experience                                         │
│  • Open source contributions                                     │
│  • Experience with distributed systems                           │
│                                                                   │
│  Education:                                                      │
│  Bachelor's degree in Computer Science or related field          │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  BENEFITS & PERKS                                                │
│  ─────────────────────────────────────────────────────────────   │
│  • Competitive salary: $150K - $200K (+ equity)                 │
│  • Health insurance (medical, dental, vision)                   │
│  • 401(k) with 4% company match                                 │
│  • Unlimited PTO (target: 20 days/year)                         │
│  • Home office setup stipend ($2,000)                           │
│  • Professional development budget ($2,500/year)                │
│  • Mental health support & wellness programs                     │
│  • Remote-first culture with optional NYC office                │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  COMPANY CULTURE                                                  │
│  ─────────────────────────────────────────────────────────────   │
│  We believe in building a diverse, inclusive team where          │
│  everyone can do their best work. Our engineering culture        │
│  emphasizes code quality, continuous learning, and supporting    │
│  career growth.                                                   │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  SIMILAR OPPORTUNITIES YOU MIGHT LIKE                            │
│  ─────────────────────────────────────────────────────────────   │
│  Staff Backend Engineer at [Company2] - Remote | $180K-$240K   │
│  Match: 89% | [View]                                             │
│                                                                   │
│  Senior Full-Stack Engineer at [Company3] - SF | $160K-$220K    │
│  Match: 85% | [View]                                             │
│                                                                   │
│  Lead Engineer at [Company4] - Remote | $170K-$230K             │
│  Match: 88% | [View]                                             │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  Ready to apply?                                                  │
│  [Apply Now] [Save Job] [Share with Friend]                     │
│                                                                   │
│  Questions? [Contact Recruiter] [FAQs]                           │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Header & Key Info
- Job title, company, location, salary
- Posted date, deadline
- Quick action buttons (Save, Share, Report)

#### 2. AI Match Score
- Percentage match (92%)
- Visual progress bar
- Summary ("Excellent fit")
- Link to skill analysis breakdown
- Missing skills listed

#### 3. Main Content Sections
- About the role (description, responsibilities)
- About you (requirements, nice-to-have, education)
- Benefits & perks
- Company culture
- Interview process (if available)

#### 4. Related Opportunities
- Similar jobs with match scores
- Quick preview on hover
- [View] links

#### 5. Call-to-Action
- Primary: [Apply Now]
- Secondary: [Save Job], [Share]

### AI Features

**Smart Matching:**
- Shows match % based on candidate profile
- "You have 7 of 8 skills"
- Highlights learning opportunity: "Master Kubernetes and you'll be perfect"

**Recommendations:**
- "Similar roles you might like based on your skills"
- Shows salary ranges for similar roles

**Application Intelligence:**
- Pre-fills application form from candidate profile (if registered)
- "Ready to apply in 1 click" (for returning candidates)

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Match Score**: Number (92%) + bar + text ("Excellent fit")
- **Skills List**: Checkmarks + text (not color alone)
- **Salary**: Clear formatting ($150,000 - $200,000, not $150k-200k)
- **Sections**: Clear headings (h2) for each section
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Tab Order**: Title → Match Score → [Apply] → [Save] → Content sections → Footer
- **All Buttons**: Keyboard accessible ([Apply Now], [Save Job], [Share], [Contact Recruiter])
- **Links**: All links keyboard accessible (Similar jobs, Company profile)
- **Focus**: Clear 2px border on focused items
- **Skip Link**: "Skip to Apply" for quick navigation

#### Screen Reader Compatibility
- **Heading Structure**: h1 for job title, h2 for sections (About Role, Requirements, etc.)
- **Match Score**: `aria-label="92% match: Excellent fit for your skills"`
- **Skills List**: `<ul role="list">` with `<li>` items
  - `<li><span aria-label="required skill">✓</span> Python</li>`
- **Salary**: `<span aria-label="$150,000 to $200,000 per year">$150K-$200K</span>`
- **Benefits**: List structure, clear text descriptions
- **Similar Jobs**: `<section aria-label="Similar opportunities">`

#### Focus Management
- **Page Load**: Focus on job title heading
- **Apply Button**: Large, prominent, easy to tab to
- **Modal/Application Form**: Focus trap in form, focus returns on close

#### Error States
- **Deadline Warning**: "This job closes in 2 days - apply soon"
- **Application Errors**: Clear messaging if form submission fails

#### Motion & Animation
- **Scroll**: Static, honor `prefers-reduced-motion`
- **Hover Effects**: No animations, use underline for links
- **Match Score**: Static (no animation of bar filling)

#### Touch Accessibility
- **Buttons**: 44x44px minimum ([Apply], [Save], [Share])
- **Match Score Bar**: Large (44px+ height)
- **Links**: 44x44px tap targets
- **Spacing**: 12px between tappable elements

### Data Model & Inputs

**Job Posting (from Screen 1):**
- All job posting data (title, description, salary, requirements, etc.)

**Candidate Profile (if logged in):**
- Skills, experience, education
- Resume data
- Preferences (location, job type, salary expectations)

**Candidate Analytics:**
- View count, conversion rate, save count
- Source (career site, LinkedIn, Indeed, etc.)

### Data Outputs & Integrations

**Candidate-Facing:**
- Job recommendations based on profile
- Similar job suggestions

**Recruiter Dashboard:**
- View tracking, save count, application source
- Candidate interest indication

**Integrations:**
- **Job Boards**: Display postings from linked boards
- **User Profile**: Match score calculation
- **Recommendations Engine**: AI matching

### Edge Cases & Error Handling

1. **Job Expired**
   - "This position is no longer accepting applications"
   - Suggest similar open roles

2. **Salary Range Removed**
   - Show "Competitive salary" instead
   - Link to benefits summary

3. **Candidate Profile Incomplete**
   - "Complete your profile for personalized match score"
   - Allow apply anyway with email signup

### Inter-Screen Interactions

- **Links from**: Job search results, job boards, recommendations
- **Triggers**: Application submission → Applications Dashboard
- **Links to**: Candidate profile, company profile, similar jobs
- **Integrates with**: Application form (Screen 3)

---

## SCREEN 3: Applications Dashboard (Recruiter)

### Purpose & User Context
Recruiter's central hub for managing all applications across job postings, with AI-powered ranking, filtering, and bulk actions.

**Primary Users:**
- Recruiters
- Hiring Managers (view-only access to applications)

### Key User Workflows

#### Workflow A: Screen Applications
1. Recruiter views all applications for a job posting
2. AI automatically ranked candidates (top matches first)
3. Filters by stage, rating, keyword
4. Reviews AI summary for each candidate
5. Moves candidates between stages (screening → interview → offer)

#### Workflow B: Bulk Actions
1. Selects multiple candidates
2. Sends bulk email ("Thanks for applying, next steps...")
3. Schedules interviews for multiple people
4. Moves batch to next stage
5. Rejects with personalized message template

#### Workflow C: Pipeline Visualization
1. Views pipeline as Kanban board (stages as columns)
2. Drags cards to move candidates between stages
3. Sees candidate aging (how long in current stage)
4. Identifies bottlenecks

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  APPLICATIONS DASHBOARD                                [Help]     │
├─────────────────────────────────────────────────────────────────┤
│  [Senior Software Engineer] [View All] [View by Stage]           │
│  Total Apps: 47 | New: 12 | Screened: 23 | Interviews: 8        │
│                                                                   │
│  [Filter] [Search] [Sort: AI Rank ▼] [View Options] [Bulk ⋮]    │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  LIST VIEW                                                        │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  [☐] Name         | Score | Stage      | Applied | Actions       │
│  ───────────────────────────────────────────────────────────     │
│  [☑] Alex Chen    | 95    | Screening  | 5 days  | [Move] [+]    │
│      ✓ 7/8 skills | 12yr exp | React, Python, AWS              │
│      Summary: Excellent match, strong backend exp, currently...  │
│      [View Full Profile] [Email] [Schedule Interview]            │
│                                                                   │
│  [☐] Jordan Lee   | 87    | Screening  | 3 days  | [Move] [+]    │
│      ✓ 6/8 skills | 8yr exp | Python, Go, Docker              │
│      Summary: Good match, strong DevOps background...            │
│      [View Full Profile] [Email] [Schedule Interview]            │
│                                                                   │
│  [☐] Sam Patel    | 82    | Applied    | 1 day   | [Move] [+]    │
│      ✓ 5/8 skills | 6yr exp | Python, JavaScript              │
│      [View Full Profile] [Email] [Screening Call]                │
│                                                                   │
│  [☐] Morgan Davis | 76    | Applied    | 2 days  | [Move] [+]    │
│      ○ 4/8 skills | 10yr exp | AWS, Kubernetes, Java           │
│      [View Full Profile] [Email] [More Info Needed]              │
│                                                                   │
│  [Show 11 more applications]                                      │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  SELECTED: 2 Candidates                                           │
│  [Move to: Interviews ▼] [Email] [Schedule] [Reject] [+]         │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

**Kanban Pipeline View:**

```
┌─────────────────────────────────────────────────────────────────┐
│  PIPELINE VIEW: Senior Software Engineer                        │
├─────────────────────────────────────────────────────────────────┤
│  [+ New Stage]                                                   │
│                                                                   │
│  APPLIED         │ SCREENING      │ INTERVIEWS     │ OFFER        │
│  (12)            │ (23)           │ (8)            │ (2)          │
│  ──────────────────────────────────────────────────────────────  │
│  📌 Alex Chen    │ 📌 Jordan Lee  │ 📌 Casey Park  │ 📌 Morgan   │
│  95% match      │ 87% match      │ Scheduled:     │ Score: 92   │
│  Click to view  │ Aging: 3 days  │ Tomorrow 2pm   │ Offer Sent  │
│  ────────────   │ ────────────   │ ────────────   │ Accepted    │
│  📌 Sam Patel   │ 📌 Morgan Davis│ 📌 Charlie F.  │             │
│  82% match      │ 76% match      │ Scheduled:     │ [+ Move]    │
│  Needs review   │ Aging: 2 days  │ Friday 10am    │             │
│  ────────────   │ [+ Move]       │                │             │
│  [+ New App]    │ [+ Assign]     │ [+ Schedule]   │             │
│                 │                │                │             │
│  [+ New Stage]  │ [+ New Stage]  │ [+ New Stage]  │             │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Application List with AI Ranking
**For Each Candidate:**
- Checkbox for bulk selection
- Name and AI match score (95, 87, 82, etc.)
- Current stage and days in stage
- Quick summary (skills match, experience, candidate strengths)
- Action buttons: [View Profile], [Email], [Schedule], [Move]

#### 2. Filtering & Search
- Filter by: stage, score range, keyword, date applied
- Search by name, email, skills
- Saved filters (e.g., "Top 25%", "No-go candidates")
- Advanced search (experience level, location preference, etc.)

#### 3. Sorting Options
- By AI rank (default)
- By application date (newest first)
- By time in stage (aging)
- By match score

#### 4. Bulk Actions
**For Multiple Selected:**
- Move to stage (Screening → Interviews → Offer → Hired)
- Send email (with template selection)
- Schedule interviews (calendar integration)
- Reject candidates (reason codes, template)
- Add to pipeline (another job posting)

#### 5. Pipeline/Kanban View
- Columns for each stage (Applied, Screening, Interviews, Offer, Hired)
- Candidate cards show score, summary
- Aging indicator (color-coded)
- Drag-to-move candidates between stages
- Stage counts at top

### AI Features

**Intelligent Ranking:**
- Scores candidates based on skill match, experience, etc.
- Top candidates bubble up automatically
- "Alex is 95% match - likely to succeed in this role"

**Resume Screening:**
- Auto-flags top performers: "⭐ Meets all requirements"
- Highlights concerns: "⚠️ Employment gap 2015-2016"
- Summarizes key points for quick review

**Duplicate Detection:**
- Identifies candidates who applied to multiple roles
- Suggests: "This candidate also applied to Product Manager role"

**Bottleneck Alerts:**
- "Screening stage has 23 candidates - consider moving to interviews"
- "No interviews scheduled for this week - behind target"

**Next-Step Recommendations:**
- "Ready for interview" for top screened candidates
- "Request more info" for borderline cases
- "Reject" suggestions for obviously unqualified candidates (with reason)

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Score**: Number (95) + bar + label ("Excellent match")
- **Status Indicators**: Stage name + visual (not position alone in Kanban)
- **Checkboxes**: Clear, large (minimum 24x24px)
- **Card Layout**: Clear hierarchy, not cramped
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Checkboxes**: Spacebar to toggle
- **Rows**: Tab through candidates, arrow keys within row, Enter to expand details
- **Bulk Actions**: Tab to dropdown, arrow keys to select action, Enter to confirm
- **Kanban**: Tab through cards, arrow keys to move between stages (drag alternative)
- **Focus**: Clear 2px border on all focused items

#### Screen Reader Compatibility
- **Table Structure**: Proper `<table>` with `<thead>` and `<tbody>`
  - Column headers: `<th scope="col">Score</th>`
  - Row structure: Name, score, stage, days, actions
- **Kanban Alternative**: List view always available
- **Candidate Cards**: 
  - `<article role="region" aria-label="Alex Chen: 95% match, Screening stage">`
  - Announce: "Candidate card 1 of 12 in Screening stage"
- **Selections**: `aria-label="2 candidates selected"`
- **Bulk Actions**: Announce action taken ("3 candidates moved to Interviews")

#### Focus Management
- **Page Load**: Focus on job posting selector or candidate list
- **Checkbox Selection**: Focus remains on checkbox, announce count
- **Bulk Action**: Focus on action button, confirm action, focus returns to list
- **Modal/Details**: Focus trap in modal, focus returns on close

#### Error States & Validation
- **Bulk Rejection**: Confirm action ("Delete 3 candidates from pipeline?")
- **Stage Move**: Show new stage, allow undo
- **Email Send**: Confirm template, recipient count

#### Motion & Animation
- **Kanban Drag**: Drag-to-move alternative available (keyboard)
- **Transitions**: Instant or simple slide (honor `prefers-reduced-motion`)
- **Filtering**: Results update without animation

#### Touch Accessibility
- **Checkboxes**: 44x44px minimum tap targets
- **Candidate Rows**: Large touch area (48px+ height)
- **Buttons**: 44x44px minimum ([Move], [Email], [Schedule])
- **Kanban Cards**: Large draggable areas for touch

### Data Model & Inputs

**Application:**
- Application ID, candidate ID, job ID
- Status (applied, screening, interview, offer, hired, rejected)
- Application date, status updated date
- AI score, match percentage
- Custom notes, ratings

**Bulk Actions:**
- Selected candidate IDs
- Action type (move, email, schedule, reject)
- Template/parameters

### Data Outputs & Integrations

**Recruiter Analytics:**
- Pipeline metrics (candidates per stage, time in stage)
- Source attribution (which boards/referrals produce best candidates)
- Time-to-hire by role

**Email/Calendar Integration:**
- Candidate email addresses for outreach
- Interview calendar availability
- Offer tracking

### Edge Cases & Error Handling

1. **Bulk Move with Missing Data**
   - "3 candidates selected: 1 missing interview time - continue?"
   - Move rest, handle exception for incomplete ones

2. **Candidate Duplicates Across Jobs**
   - Alert: "Alex Chen also applied to Product Manager role"
   - Option to consolidate or keep separate

3. **Rejection Reason Required**
   - "Please select a reason before rejecting"
   - Reasons: Unqualified, Overqualified, Bad fit, Proceeded with another candidate, etc.

### Inter-Screen Interactions

- **Links from**: Job Posting View (apply)
- **Links to**: Application Details & Resume Review (Screen 4), Interview Scheduling (Screen 6)
- **Triggers**: Candidate movement updates in pipeline

---

Continuing in next part due to length...
