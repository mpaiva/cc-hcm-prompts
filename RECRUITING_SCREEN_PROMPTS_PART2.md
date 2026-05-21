# Recruiting & Applicant Tracking Screen Prompts - Part 2

---

## SCREEN 4: Application Details & Resume Review

### Purpose & User Context
Deep-dive view of individual applications with embedded resume viewer, AI-extracted data, skill analysis, and collaboration tools for interview coordination.

**Primary Users:**
- Recruiters (reviewing applications, making screening decisions)
- Hiring Managers (reviewing top candidates)

### Key User Workflows

#### Workflow A: Screen Individual Application
1. Recruiter clicks candidate from Applications Dashboard
2. Views full resume with AI annotations
3. Sees extracted data (skills, experience, education)
4. Reviews gap analysis (vs job requirements)
5. Adds notes/rating
6. Moves to next stage or rejects

#### Workflow B: Team Collaboration
1. Recruiter adds hiring manager as reviewer
2. Manager reviews application and leaves feedback
3. Recruiter sees manager's notes
4. Discusses in comments thread
5. Makes joint decision

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  APPLICATION REVIEW: Alex Chen - Senior Software Engineer        │
│  [← Back] [Print] [Share] [More ⋮]                              │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  CANDIDATE SUMMARY                                               │
│  ─────────────────────────────────────────────────────────────   │
│  Alex Chen | alex.chen@email.com | (555) 123-4567               │
│  San Francisco, CA · Open to Remote                              │
│  LinkedIn: /in/alexchen | GitHub: github.com/alexchen          │
│                                                                   │
│  AI ANALYSIS                                                      │
│  ─────────────────────────────────────────────────────────────   │
│  Match Score: 95/100 | Recommendation: ⭐⭐⭐⭐⭐ STRONG YES       │
│  All Required Skills Present: ✓ Python ✓ React ✓ AWS            │
│  Missing Skills: Kubernetes (learns quickly, has DevOps exp)    │
│  Verification Score: 100% (all claims verified)                 │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  RESUME (click to annotate)                                      │
│  [Embedded PDF Viewer]                                           │
│  ─────────────────────────────────────────────────────────────   │
│  [PDF Preview Area: Full resume displayed with annotations]     │
│  [Pages: 1 of 2]  [Zoom: 100%] [Full Screen]                   │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  EXTRACTED EXPERIENCE                                            │
│  ─────────────────────────────────────────────────────────────   │
│  ✓ Current Role:  Senior Software Engineer at TechCorp          │
│    Company: TechCorp · Location: SF · Duration: 3 years         │
│    Responsibilities: Backend services, team leadership, DevOps   │
│                                                                   │
│  ✓ Previous:      Software Engineer II at StartupX              │
│    Company: StartupX · Duration: 4 years                         │
│    Key Tech: Python, AWS, Microservices                         │
│                                                                   │
│  ✓ Previous:      Junior Developer at WebAgency                │
│    Company: WebAgency · Duration: 2 years                       │
│    Key Tech: JavaScript, React, REST APIs                       │
│                                                                   │
│  EDUCATION                                                       │
│  ─────────────────────────────────────────────────────────────   │
│  ✓ Bachelor of Science in Computer Science                      │
│    University of California, Berkeley · Graduated: 2015         │
│                                                                   │
│  EXTRACTED SKILLS                                                │
│  ─────────────────────────────────────────────────────────────   │
│  Technical:  ✓ Python (12 yrs) | ✓ React (8 yrs) | ✓ AWS (7)   │
│             ✓ SQL | ✓ Git | ✓ CI/CD | Java (5 yrs)            │
│                                                                   │
│  Soft Skills: Leadership | Mentoring | Code Reviews            │
│                                                                   │
│  SKILL-TO-JOB MATCH                                              │
│  ─────────────────────────────────────────────────────────────   │
│  Required:                         Candidate Has:               │
│  ✓ Python (5+ yrs)       →         12 years ✓ Excellent       │
│  ✓ React (3+ yrs)        →         8 years ✓ Excellent        │
│  ✓ AWS (2+ yrs)          →         7 years ✓ Excellent        │
│  ✓ System Design         →         Multiple roles ✓ Strong     │
│  ✓ Leadership            →         Mentoring exp ✓ Strong      │
│                                                                   │
│  Nice-to-Have:                                                   │
│  • Kubernetes            →         No experience ○ Concern      │
│  • Open Source           →         GitHub projects ✓ Yes        │
│  • Distributed Systems   →         Microservices ✓ Yes         │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  VERIFICATION & RED FLAGS                                        │
│  ─────────────────────────────────────────────────────────────   │
│  ✓ Employment verified: TechCorp confirms 3 years               │
│  ✓ Education verified: UC Berkeley degree confirmed             │
│  ✓ No major red flags detected                                  │
│  ℹ️  Small gap: 2 months between StartupX and current (likely) │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  TEAM FEEDBACK                                                    │
│  ─────────────────────────────────────────────────────────────   │
│  Sarah Kim (Hiring Manager) - Reviewed 2 days ago               │
│  "Strong candidate. Excellent Python skills and leadership      │
│   background. Only concern is Kubernetes gap, but learnable.    │
│   I'd move to interviews. 5/5 stars"                            │
│   [Reply] [Edit] [Delete]                                       │
│                                                                   │
│  Mike Johnson (Senior Engineer) - Added to review               │
│  "Looks good from tech perspective. Want to schedule a          │
│   technical interview to assess system design depth."           │
│  [Reply]                                                         │
│                                                                   │
│  [+ Add Reviewer] [+ Add Comment]                                │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  YOUR DECISION                                                    │
│  ─────────────────────────────────────────────────────────────   │
│  Rating: [1⭐ 2⭐ 3⭐ 4⭐ 5⭐] (4 Stars selected)                 │
│  My Notes:  [_________________________________]                │
│                                                                   │
│  Action:  [Move to: Interviews ▼] [Schedule Interview]          │
│           [Request More Info] [Reject] [Hold in Pipeline]       │
│                                                                   │
│  [Save & Next Candidate] [Back to List]                         │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Candidate Summary
- Name, contact info, location
- Links to LinkedIn, GitHub, portfolio
- Job applied for, application date

#### 2. AI Analysis
- Match score (0-100)
- Recommendation (Strong Yes, Yes, Maybe, Weak No, Reject)
- Required skills present/missing
- Verification score
- Major red flags or concerns

#### 3. Resume Viewer
- Embedded PDF/document viewer
- Annotation tools (highlight, comment on resume)
- Multi-page navigation
- Zoom and full-screen options
- Print option

#### 4. Extracted Data
- Work history (extracted automatically)
- Education
- Skills (parsed from resume)
- Key achievements

#### 5. Skill-to-Job Matching
**Matrix showing:**
- Required skill → Candidate has (with years)
- Gap analysis (missing skills)
- Nice-to-have match

#### 6. Verification & Red Flags
- Employment verification status
- Education verification
- Red flags (employment gaps, inconsistencies, etc.)
- Notes on any concerns

#### 7. Team Collaboration
- Reviewers and their feedback
- Rating stars (5-star system)
- Comments thread
- Ability to add/tag other reviewers

#### 8. Decision & Next Steps
- Rating selector
- Personal notes
- Action button (Move to stage, Schedule, Reject, Hold)
- Quick navigation to next candidate

### AI Features

**Smart Data Extraction:**
- Parses resume to extract experience, education, skills
- Matches candidate timeline (employment dates, gaps)
- Verifies claims where possible

**Gap Analysis:**
- "Missing Kubernetes but has DevOps experience - learnable"
- Flags unexpected gaps: "2-month gap between roles"

**Recommendation Engine:**
- "95% match - move to interviews"
- Confidence score based on skill match, experience level

**Collaboration Insights:**
- Surfaces team consensus: "All reviewers agree: move to interviews"
- Flags disagreement: "Mike rates 4/5, Sarah rates 3/5 - discuss?"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Resume Viewer**: Accessible PDF (not image-only)
  - Text must be selectable/copyable
  - Provide alternative: transcript or structured data
- **Match Score**: Number (95) + label ("Strong Yes") + color (not alone)
- **Skills List**: Checkmark + text (not color alone)
- **Red Flags**: Icon + text label
- **Ratings**: Star labels (1-5) with text ("5 Stars")
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **PDF Viewer**: All controls keyboard accessible
  - Arrow keys: navigate pages
  - Ctrl+F: search within PDF
  - Alt+Plus/Minus: zoom
- **Tabs/Sections**: Tab to expand sections, arrow keys within
- **Rating**: Arrow keys to select stars, Enter to confirm
- **Comments**: Tab to text area, type comment, Tab to [Reply], Enter to submit
- **Buttons**: All buttons keyboard accessible
- **Focus**: Clear 2px border on focused items

#### Screen Reader Compatibility
- **PDF Alternative**: If PDF not accessible, provide structured data
  - `<section aria-label="Work Experience">`
  - List employment chronologically with dates, titles
- **Match Score**: `aria-label="Match score: 95 out of 100. Recommendation: Strong Yes"`
- **Skills**:
  - `<ul aria-label="Extracted Skills">`
  - `<li><span aria-label="required">✓</span> Python</li>`
- **Red Flags**: `role="alert" aria-live="assertive"`
- **Ratings**: 
  - `<fieldset><legend>Your Rating</legend>`
  - Radio buttons labeled "1 Star", "2 Stars", etc.
- **Comments**: Each comment is `<article role="comment">`
  - Author, timestamp, content announced

#### Focus Management
- **Page Load**: Focus on candidate name heading
- **Rating Selection**: Focus on selected star, arrow keys to change
- **Comment Focus**: Focus moves to comment text area when adding
- **Modal/Details**: Not typically modal, but if so: focus trap

#### Error States & Validation
- **Missing Rating**: "Please select a rating before moving to interviews"
- **Reject Reason**: "Rejection reason required - select from dropdown"
- **Comment Too Long**: "Comment must be under 500 characters"

#### Motion & Animation
- **PDF Transitions**: Instant page change (no animation)
- **Skill List**: Instant expand/collapse
- **Rating Selection**: Instant star fill (no animation)
- **Honor `prefers-reduced-motion`**: No animations

#### Touch Accessibility
- **PDF Viewer**: Large gesture controls (pinch-to-zoom, swipe for pages)
- **Rating Stars**: 44x44px minimum tap targets
- **Comment Buttons**: 44x44px minimum ([Reply], [Edit], [Delete])
- **Action Buttons**: 44x44px minimum
- **Spacing**: 12px between tappable elements

### Data Model & Inputs

**Application Data (from Screen 3):**
- Candidate info, application date, job applied for
- AI score, recommendation

**Resume Data:**
- Resume file (PDF, Word, plain text)
- Extracted: experience, education, skills
- Formatted text version (alternative to PDF)

**Reviews/Feedback:**
- Reviewer ID, rating (1-5 stars)
- Comments, timestamp
- Verification status

### Data Outputs & Integrations

**Decision Tracking:**
- Rating, notes, decision (move/reject/hold)
- Used for pipeline analytics

**Reference Data:**
- Skills extracted used for skill analytics
- Verification results archived

**Integrations:**
- **Resume Parser**: Extract structured data from resume
- **Background Check**: Link to verification results
- **Calendar**: Schedule interview from this screen
- **Email**: Send candidate communication

### Edge Cases & Error Handling

1. **Resume Not Accessible (Image-Only)**
   - Provide alternative: transcript view with extracted data
   - Suggest candidate upload text-based version

2. **Employment Verification Fails**
   - Flag but don't block: "Unable to verify - candidate may clarify in interview"

3. **PDF Rendering Issues**
   - Fall back to text version: "Resume can't display - view as text"

4. **Multiple Reviewers, Conflicting Ratings**
   - Show all ratings: "Sarah: 4/5, Mike: 3/5 - discuss?"

### Inter-Screen Interactions

- **Links from**: Applications Dashboard (Screen 3)
- **Links to**: Interview Scheduling (Screen 6)
- **Triggers**: Rating/decision updates pipeline
- **Provides Data to**: Interview Feedback (Screen 7)

---

## SCREEN 5: Candidate Evaluation & Scoring

### Purpose & User Context
Structured evaluation form for assessing candidates against job criteria, with AI-powered recommendations and comparison views.

**Primary Users:**
- Hiring Managers (evaluating during screening or interviews)
- Interviewers (after technical/behavioral interviews)

### Key User Workflows

#### Workflow A: Screening Evaluation
1. Hiring manager opens candidate evaluation form
2. Sees criteria for the job (technical skills, experience, cultural fit, etc.)
3. Rates each criterion (1-5 scale)
4. Adds comments explaining ratings
5. Gets overall score recommendation
6. Sees how candidate compares to other applicants
7. Submits evaluation

#### Workflow B: Interview Feedback Integration
1. Multiple interviewers complete evaluations
2. System aggregates scores
3. Shows consensus areas and disagreements
4. Recommends next step (advance, hold, reject)

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  CANDIDATE EVALUATION: Alex Chen - Senior Software Engineer      │
├─────────────────────────────────────────────────────────────────┤
│  Evaluator: Sarah Kim (Hiring Manager)                          │
│  Date: Today | Interview: Technical Interview (2 hours)         │
│                                                                   │
│  Evaluation Type: [Technical Interview ▼]                        │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  TECHNICAL SKILLS ASSESSMENT                                     │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  1. Python Proficiency                                           │
│     [1] [2] [3] [4] [5⭐] Selected: 5/5 (Expert)               │
│     Evidence/Comments:                                           │
│     [Wrote complex algorithms, handled edge cases perfectly]    │
│                                                                   │
│  2. System Design & Architecture                                 │
│     [1] [2] [3] [4⭐] [5] Selected: 4/5 (Strong)               │
│     Evidence/Comments:                                           │
│     [Good understanding of trade-offs, missed scalability point] │
│                                                                   │
│  3. Problem Solving & Approach                                   │
│     [1] [2] [3] [4⭐] [5] Selected: 4/5 (Strong)               │
│     Evidence/Comments:                                           │
│     [Methodical approach, good communication of thinking]        │
│                                                                   │
│  EXPERIENCE & BACKGROUND                                         │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  4. Relevant Experience (5+ years backend)                        │
│     [1] [2] [3] [4] [5⭐] Selected: 5/5 (Exceeds)              │
│     Evidence/Comments:                                           │
│     [12 years total, 7 years backend, multiple large systems]   │
│                                                                   │
│  5. Leadership & Mentoring                                       │
│     [1] [2] [3] [4⭐] [5] Selected: 4/5 (Strong)               │
│     Evidence/Comments:                                           │
│     [Described mentoring 2 junior engineers, good leadership]    │
│                                                                   │
│  SOFT SKILLS & FIT                                               │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  6. Communication & Collaboration                                │
│     [1] [2] [3] [4] [5⭐] Selected: 5/5 (Excellent)            │
│     Evidence/Comments:                                           │
│     [Clear communicator, articulate, asks clarifying questions]  │
│                                                                   │
│  7. Cultural Fit & Values Alignment                              │
│     [1] [2] [3] [4⭐] [5] Selected: 4/5 (Good)                │
│     Evidence/Comments:                                           │
│     [Values continuous learning, collaborative, growth mindset]  │
│                                                                   │
│  OVERALL ASSESSMENT                                              │
│  ─────────────────────────────────────────────────────────────   │
│  Average Score: 4.4 / 5.0  →  Recommendation: ⭐⭐⭐⭐ ADVANCE   │
│                                                                   │
│  Additional Notes:                                               │
│  [________________________________________]                    │
│  [________________________________________]                    │
│                                                                   │
│  COMPARISON TO OTHER CANDIDATES                                  │
│  ─────────────────────────────────────────────────────────────   │
│  Technical Skills:  Alex: 4.4/5  |  Position: #1 of 8 evaluated │
│  Experience:        Alex: 4.8/5  |  Position: #1 of 8 evaluated │
│  Soft Skills:       Alex: 4.5/5  |  Position: #2 of 8 evaluated │
│  Overall:          Alex: 4.4/5  |  Position: #1 of 8 evaluated │
│                                                                   │
│  Other candidates with 4+/5 overall: Jordan (4.2), Sam (4.1)   │
│                                                                   │
│  RECOMMENDATION                                                   │
│  ─────────────────────────────────────────────────────────────   │
│  AI Recommendation: ADVANCE TO NEXT ROUND                        │
│  Reasoning: Alex scores highly across all dimensions, with       │
│  particular strength in technical skills and communication.      │
│  No significant concerns identified. Strong candidate.           │
│                                                                   │
│  [Submit Evaluation] [Save Draft] [Cancel]                       │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Structured Criteria
**By Category:**
- Technical Skills (role-specific: coding, design, domain knowledge)
- Experience & Background (years, relevant roles, scope)
- Soft Skills (communication, collaboration, problem-solving)
- Cultural Fit & Values

**For Each Criterion:**
- 1-5 rating scale with descriptors (Novice, Competent, Strong, Expert, Exceeds)
- Text field for evidence/comments
- Reference to job requirements for context

#### 2. Rating Scale with Descriptions
- 1: Novice/Weak - Significant concerns
- 2: Developing/Below - Some concerns
- 3: Competent/Adequate - Meets baseline
- 4: Strong/Advanced - Exceeds in some areas
- 5: Expert/Exceptional - Excellent fit

#### 3. Evidence/Comments
- Text input for each rating
- Prompts: "What specific examples support this rating?"
- AI suggestions: "Common reasons for this rating..."

#### 4. Overall Score
- Calculated from individual ratings
- AI recommendation (Advance, Hold, Reject, Request More Info)
- Reasoning explanation

#### 5. Comparison View
- How candidate ranks vs other candidates evaluated
- Shows positioning (1st of 8, 3rd of 12, etc.)
- Highlights if they're outlier (top, bottom, significantly different)

#### 6. Team Evaluations
- If multiple people evaluated, show all scores
- Highlight agreement/disagreement areas
- Consensus score if applicable

### AI Features

**Smart Rating Suggestions:**
- "Based on performance, typically rates 4/5 in System Design"
- Learns from historical ratings in your organization

**Recommendation Engine:**
- "With these scores, candidate should advance"
- Identifies "must-ask" follow-up questions if scores are mixed

**Comparison Insights:**
- "Alex is in top 20% for Python proficiency"
- "This is strongest pool of candidates for this role in 12 months"

**Flagging:**
- Highlights disagreement between interviewers: "Technical score: 4/5 vs 2/5 - discuss?"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Rating Scale**: Numbers (1-5) + text labels (Novice, Expert)
  - Not color alone (use text)
  - Selected indicator clear (bold, asterisk, or radio button)
- **Categories**: Clear headings (h2) for each section
- **Comparison Chart**: Use text labels with numbers
  - Bar chart alternative: provide table
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Radio Buttons**: Arrow keys to select rating (1-5), Enter to confirm
- **Text Fields**: Tab through comments, Shift+Tab back
- **Tabs/Sections**: Arrow keys to navigate categories
- **Buttons**: [Submit], [Save Draft], [Cancel] all keyboard accessible
- **Focus**: Clear 2px border on focused items

#### Screen Reader Compatibility
- **Form Structure**: `<fieldset>` and `<legend>` for each criterion
  - `<legend>1. Python Proficiency</legend>`
  - Radio buttons: `<input type="radio" aria-label="5 Stars: Expert">`
- **Rating Feedback**: 
  - `<span role="status" aria-live="assertive">Selected: 5/5 (Expert)</span>`
- **Overall Score**: `aria-label="Overall Score: 4.4 out of 5.0"`
- **Comparison Table**: Proper `<table>` with headers
- **Recommendation**: `role="region" aria-label="AI Recommendation: Advance to Next Round"`

#### Focus Management
- **Page Load**: Focus on first criterion heading or rating scale
- **Rating Selection**: Focus remains on scale, arrow keys navigate
- **Tab to Text Field**: Focus moves to evidence text field after rating
- **Submission**: Focus on success message or next step

#### Error States & Validation
- **Incomplete Evaluation**: "Please complete all criteria before submitting"
- **Missing Evidence**: Optional but flagged if missing for low/high ratings
  - "A rating of 1/5 should include evidence. Continue?"

#### Motion & Animation
- **Rating Selection**: Instant (no animation of bar filling)
- **Score Calculation**: Instant update (no spinning calculator)
- **Comparison Bars**: Static or simple fade

#### Touch Accessibility
- **Radio Buttons**: 44x44px minimum tap targets
- **Text Fields**: 44px height, full-width input
- **Buttons**: 44x44px minimum
- **Criterion Cards**: Large touch area (48px+ height)

### Data Model & Inputs

**Evaluation Criteria:**
- Criterion ID, name, category
- Description, expected rating distribution
- Scoring rubric (1-5 descriptors)

**Evaluation Response:**
- Evaluation ID, candidate ID, evaluator ID
- Criterion ID, rating (1-5)
- Evidence/comments text
- Timestamp, evaluation type (screening, technical, etc.)

### Data Outputs & Integrations

**Aggregated Score:**
- Overall average score
- Recommendation (advance/hold/reject)
- Evaluation history per candidate

**Analytics:**
- Rating distribution per criterion
- Evaluator consistency (do your ratings align with others?)
- Prediction accuracy (do highly-rated candidates succeed?)

**Integrations:**
- **Interview Scheduling**: Link from interview feedback form
- **Pipeline**: Scoring influences candidate stage progression
- **Reference Checks**: Prepare reference questions based on ratings

### Edge Cases & Error Handling

1. **Multiple Evaluators, Different Scales**
   - Normalize scores across evaluators
   - Show individual + average ratings

2. **Outlier Rating (e.g., 1/5 when others rated 4/5)**
   - Alert: "Your rating differs significantly - note any specific concerns?"

3. **Missing Criteria**
   - "Some criteria not rated - complete before submitting?"
   - Allow optional fields if job allows

### Inter-Screen Interactions

- **Links from**: Interview Feedback (Screen 7), Applications Dashboard
- **Links to**: Offer Management (Screen 8)
- **Provides Data to**: Pipeline stage progression, reference checks
- **Triggers**: AI recommendations in Applications Dashboard

---

## SCREEN 6: Interview Scheduling

### Purpose & User Context
Coordinate interviews with candidates, interviewers, and meeting logistics. Sync with calendars, send invites, and manage rescheduling.

**Primary Users:**
- Recruiters (scheduling interviews)
- Candidates (receiving and confirming interviews)
- Interviewers (adding availability, joining meetings)

### Key User Workflows

#### Workflow A: Schedule Interview
1. Recruiter selects candidate and interview type (phone, technical, final)
2. Views candidate's and interviewer's availability
3. Picks optimal time slot
4. Generates meeting link (Zoom, Teams, etc.)
5. Sends invite to all parties
6. Candidate confirms attendance

#### Workflow B: Candidate Self-Schedule
1. Candidate gets email with link: "Schedule your interview"
2. Clicks link, sees available slots
3. Selects preferred time
4. Receives confirmation with meeting link

#### Workflow C: Interviewer Perspective
1. Interviewer sees scheduled interviews on their calendar
2. Can reject/propose alternatives if conflict
3. Joins meeting at scheduled time
4. Takes notes during interview

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  INTERVIEW SCHEDULING: Alex Chen - Senior Software Engineer      │
├─────────────────────────────────────────────────────────────────┤
│  [Schedule Interview] [Reschedule] [Cancel]                     │
│                                                                   │
│  INTERVIEW CALENDAR                                              │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Step 1: Interview Type                                          │
│  [Phone Screen (30 min)] [Technical Interview (120 min)]         │
│  [Behavioral Interview (60 min)] [Final Round (90 min)]         │
│  Selected: Technical Interview                                   │
│                                                                   │
│  Step 2: Select Interviewer(s)                                   │
│  Suggested: Sarah Kim (Hiring Manager - available most times)   │
│           Mike Johnson (Senior Engineer - limited availability)  │
│           [Add Custom Interviewer]                               │
│                                                                   │
│  Selected Interviewers:                                          │
│  [x] Sarah Kim          [View Availability] [Remove]             │
│  [x] Mike Johnson       [View Availability] [Remove]             │
│  [ ] [+ Add Interviewer]                                         │
│                                                                   │
│  Step 3: Find Best Time Slot                                     │
│                                                                   │
│  Candidate Timezone: PT (Pacific Time)                           │
│  Candidate Notes: "Available weekdays 5-8pm, weekends anytime"  │
│                                                                   │
│  CALENDAR VIEW                                                    │
│  ─────────────────────────────────────────────────────────────   │
│  [« Mon Jan 15] [Tue Jan 16] [Wed Jan 17] [Thu Jan 18] [Fri»]  │
│                                                                   │
│  Monday (Jan 15)       [Column shows times 9am-6pm]              │
│  9am:  (Sarah: free) (Mike: free)                                │
│  10am: (Sarah: free) (Mike: BUSY)                                │
│  11am: (Sarah: BUSY)  (Mike: free)                               │
│  12pm: (Sarah: BUSY)  (Mike: free)                               │
│  1pm:  (Sarah: free) (Mike: free)                                │
│  2pm:  (Sarah: BUSY)  (Mike: free)                               │
│  3pm:  (Sarah: free) (Mike: free)  ← ⭐ AI Suggests            │
│  4pm:  (Sarah: BUSY)  (Mike: BUSY)                               │
│  5pm:  (Sarah: free) (Mike: free)  ← ✓ Candidate Available     │
│                                                                   │
│  [Best Options: 3pm, 5pm Today]                                  │
│                                                                   │
│  Tuesday (Jan 16)                                                │
│  [Similar view...]                                               │
│                                                                   │
│  Step 4: Confirm Details                                         │
│  ─────────────────────────────────────────────────────────────   │
│  Interview Type:   Technical Interview (2 hours)                │
│  Date/Time:        Monday, January 15, 2024 at 3:00 PM PT      │
│  Duration:         2 hours                                       │
│  Interviewers:     Sarah Kim, Mike Johnson                       │
│  Meeting Link:     Zoom link (auto-generated)                    │
│  Interview Format: [Live Video ▼]                                │
│  Location:         [Zoom / In-Person / Phone ▼]                 │
│                                                                   │
│  Confirmation Email Preview:                                     │
│  Subject: "Interview Scheduled: Senior Software Engineer"        │
│  Body: [Show draft email to candidate]                           │
│  [Edit Template]                                                 │
│                                                                   │
│  [Schedule Interview] [Continue Searching] [Cancel]              │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  SCHEDULED INTERVIEWS                                            │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  ✓ Phone Screen                                                  │
│    Date: Jan 13, 2024 | Time: 10:00 AM PT                       │
│    Interviewer: Sarah Kim                                        │
│    Status: Completed | Notes: [Read Notes]                      │
│    Feedback: [View Feedback]                                     │
│    [Reschedule] [Add Notes] [Request Feedback]                   │
│                                                                   │
│  ⊙ Technical Interview                                           │
│    Date: Jan 15, 2024 | Time: 3:00 PM PT                        │
│    Interviewers: Sarah Kim, Mike Johnson                         │
│    Status: Scheduled (Tomorrow)                                  │
│    Meeting Link: [Join Zoom] (available 15 min before)          │
│    [Reschedule] [Cancel] [Edit Details] [Message Candidate]    │
│                                                                   │
│  [+ Schedule Next Interview] [View All]                          │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Interview Type Selection
- Phone screen, technical interview, behavioral, final round
- Duration displayed for each type
- Custom interview types allowed

#### 2. Interviewer Selection
- Suggest best-fit interviewers based on role
- Show availability (color-coded: free, busy, unavailable)
- Add custom interviewers (outside system)

#### 3. Calendar View
- Shows availability for all selected interviewers
- Respects timezones (candidate's timezone)
- AI highlights optimal slots (everyone free + candidate available)
- Color-coded: ✓ (available), ⚠ (one person busy), ✗ (everyone busy)

#### 4. Confirmation Details
- Interview type, date, time, duration
- Interviewers
- Meeting link (auto-generated)
- Email preview to candidate
- Format selection (video, in-person, phone)

#### 5. Scheduled Interviews List
- Past interviews (completed, with feedback)
- Upcoming interviews (with meeting link)
- Reschedule/cancel options
- Interviewer feedback link

### AI Features

**Optimal Slot Suggestions:**
- "3pm is best - everyone available + candidate prefers evenings"
- Learns from past successful interview times

**Availability Prediction:**
- "Mike rarely responds to adds - propose to him first?"
- Suggests pre-confirming busy interviewers

**Timezone Awareness:**
- Auto-converts times for candidate's timezone
- Avoids unreasonable times (avoid 6am calls)

**Follow-up Automation:**
- "Schedule feedback form 24 hours after interview"
- "Candidate hasn't confirmed - send reminder"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Calendar**: Table alternative available (text list of slots)
  - Row: Date | Time | Sarah Status | Mike Status | Candidate Availability
- **Availability Icons**: Text + color (✓ free, ⚠ busy, ✗ unavailable)
- **Interview Steps**: Clear numbering (Step 1 of 4)
- **Meeting Link**: Text link, not just button
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Interview Type**: Tab through options, arrow keys, Enter to select
- **Interviewer Selection**: Checkboxes with Tab/Spacebar to toggle
- **Calendar**: 
  - Tab through date columns (Mon, Tue, Wed, etc.)
  - Arrow keys navigate time slots
  - Enter/Spacebar to select time slot
- **Buttons**: All buttons keyboard accessible
- **Focus**: Clear 2px border

#### Screen Reader Compatibility
- **Calendar Alternative**: Provide sortable list view of available times
  - "Monday 3pm: Sarah available, Mike available, Candidate available"
- **Availability Status**: 
  - `aria-label="Sarah Kim: Available for 3pm slot"`
  - `aria-label="Mike Johnson: Busy (conflict with team meeting)"`
- **Selected Interview**:
  - `role="region" aria-label="Interview scheduled for Monday January 15, 3:00 PM PT"`
- **Email Preview**: Read as continuous text (not visual layout)

#### Focus Management
- **Page Load**: Focus on Step 1 (Interview Type selection)
- **Step Submission**: Focus moves to first input of next step
- **Calendar Focus**: Announce selected time slot
- **Confirmation**: Focus on [Schedule Interview] button

#### Error States & Validation
- **No Time Available**: "No slots available with all interviewers - add another date range?"
- **Candidate Unavailable**: "Candidate marked unavailable at this time - proceed?"
- **Timezone Conflict**: "This time is 6am for candidate - too early?"

#### Motion & Animation
- **Calendar Transitions**: Instant date change (no animation)
- **Status Updates**: Real-time, no animation
- **Scrolling**: Static, honor `prefers-reduced-motion`

#### Touch Accessibility
- **Calendar Slots**: Large touch targets (48x48px minimum)
- **Checkboxes**: 44x44px minimum
- **Buttons**: 44x44px minimum
- **Date Navigation**: Large < > buttons (44x44px)

### Data Model & Inputs

**Interview Type:**
- Type ID, name, duration
- Default interviewers, questions (if applicable)

**Interview Slot:**
- Interview ID, candidate ID, job ID
- Interview type, date, time, duration
- Interviewer IDs, meeting link URL
- Status (scheduled, completed, cancelled, rescheduled)
- Notes, feedback link

**Availability Data:**
- User ID, free/busy calendar feed
- Timezone preferences
- Candidate availability notes

### Data Outputs & Integrations

**Calendar Invites:**
- Sent to all parties (candidates, interviewers)
- Meeting link included
- Timezone-aware

**Reminders:**
- 24 hours before: "Reminder: Interview tomorrow at 3pm"
- 15 minutes before: "Interview starting soon - join Zoom"

**Integrations:**
- **Calendar APIs**: Google Cal, Outlook sync
- **Video Conferencing**: Zoom, Teams, Google Meet (auto-link generation)
- **Email**: Send invites, reminders, confirmations
- **Interview Feedback**: Trigger feedback form post-interview

### Edge Cases & Error Handling

1. **Candidate Timezone Ambiguous**
   - "Confirm your timezone: [Pacific Time ▼]"
   - Show converted times for clarity

2. **Interviewer Declines/No Response**
   - Auto-remove from availability after 48 hours
   - Suggest alternate interviewers

3. **Double-Booking**
   - "Sarah has conflict at 3pm - this will show as tentative on her calendar"
   - Option to propose alternative time

4. **Meeting Link Generation Fails**
   - Fallback: "Send meeting details manually - here's the info to share"
   - Candidate still receives invite with time/location

### Inter-Screen Interactions

- **Links from**: Applications Dashboard, Interview Feedback
- **Links to**: Interview Feedback Form (Screen 7)
- **Creates**: Calendar events, sends invitations
- **Provides Data to**: Offer Management (interview completion status)

---

Continuing with Screens 7-8 in next part...
