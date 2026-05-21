# Performance Management Screen Prompts - Part 2

---

## SCREEN 3: 360-Degree Feedback Request

### Purpose & User Context
Coordinate collection of multi-source feedback from managers, peers, direct reports, and sometimes external stakeholders for holistic performance perspective.

**Primary Users:**
- HR/Managers (creating feedback rounds, managing logistics)
- Employees (receiving feedback requests, optionally requesting feedback)

**Secondary Users:**
- Peers, direct reports, managers (feedback providers)
- Executives (review 360 summary for high performers)

### Key User Workflows

#### Workflow A: Create Feedback Round
1. HR initiates 360 feedback round (typically annual or mid-cycle)
2. Selects feedback participants (managers, peers, direct reports)
3. Customizes feedback questions or uses template
4. Sets deadline (usually 2-3 weeks)
5. Sends invitations to raters
6. Tracks completion status
7. Closes round and shares results with employee

#### Workflow B: Employee Perspective
1. Employee sees "360 feedback round open"
2. Optionally nominates additional raters (trusted peers, stakeholders)
3. Receives results when round closes
4. Reviews feedback themes and suggestions
5. Can request follow-up conversations to understand feedback

#### Workflow C: Feedback Provider Experience
1. Rater receives email: "Provide feedback on [Employee]"
2. Opens feedback form (anonymous or attributed)
3. Answers structured questions (competencies, strengths, development areas)
4. Optionally adds open-ended comments
5. Submits (can be anonymous)
6. HR tracks completion

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  360-DEGREE FEEDBACK ROUNDS                            [Help]     │
├─────────────────────────────────────────────────────────────────┤
│  [Create New Round] [Active Rounds] [Archive] [My Feedback]      │
│                                                                   │
│  ACTIVE 360 FEEDBACK ROUNDS (2)                                   │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Annual 360 Review - Cycle 2024                                  │
│  Period: Jan - Mar 2024                                          │
│  Status: In Progress (50% Complete) | Deadline: Feb 28           │
│  Participants: 245 total, 120 completed (49%)                    │
│  [Manage Round] [View Results] [Send Reminders]                  │
│                                                                   │
│  Mid-Cycle 360 Review (Engineering Department)                   │
│  Period: Jan 2024                                                │
│  Status: In Progress (75% Complete) | Deadline: Feb 15           │
│  Participants: 42 total, 31 completed (74%)                      │
│  [Manage Round] [View Results] [Send Reminders]                  │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  CREATE NEW 360 FEEDBACK ROUND                                    │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Round Name *               [Annual 360 Review 2024________]     │
│  Description                [Feedback for performance reviews]   │
│  Department/Level *         [All Staff ▼]                        │
│  Feedback Template *        [Standard 360 Questions ▼]           │
│  Rater Types (select all)   [x] Manager  [x] Peers               │
│                             [x] Direct Reports  [ ] External     │
│  Anonymous Feedback         [x] Yes - anonymous by default       │
│  Employee Can Nominate      [x] Yes - suggest raters             │
│  Raters Per Employee        [5-7 minimum recommended]            │
│                                                                   │
│  Round Dates                                                      │
│  Open Date *                [________] (opens day of send)       │
│  Close Date *               [________] (typically 2-3 weeks)     │
│                                                                   │
│  Notification Template      [Standard Email ▼]                   │
│  [Customize Email]                                               │
│                                                                   │
│  [Preview] [Schedule] [Cancel]                                   │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  MANAGE ROUND: Annual 360 Review - Cycle 2024                    │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Round Details:                                                  │
│  Total Participants: 245 | Completed: 120 (49%) | Pending: 125  │
│  Estimated Completion: Feb 25 (based on current pace)            │
│                                                                   │
│  COMPLETION STATUS BY DEPARTMENT                                 │
│  Engineering: 58/85 (68%)  [████████░░] [Send Reminder]         │
│  Sales:       42/75 (56%)  [██████░░░░] [Send Reminder]         │
│  Marketing:   20/45 (44%)  [████░░░░░░] [Send Reminder]         │
│  Operations:  0/40  (0%)   [░░░░░░░░░░] [Send Reminders]        │
│                                                                   │
│  PARTICIPANTS PENDING FEEDBACK (125 people)                      │
│  [Filter by: All Status] [Department] [Days Pending]             │
│                                                                   │
│  Name              | Status    | Sent | Days Pending | Action    │
│  ─────────────────────────────────────────────────────────────   │
│  Sarah Kim         | Assigned  | 1d  | 1 day        | [Remind]   │
│  Mike Johnson      | Not Sent  | -   | -            | [Send]     │
│  Alex Chen         | Assigned  | 3d  | 3 days       | [Remind]   │
│  Jordan Lee        | Assigned  | 5d  | 5 days       | [Escalate] │
│  [Show 121 more pending...]                                      │
│                                                                   │
│  BULK ACTIONS                                                     │
│  [Send to All Pending] [Send Reminder to 5+ Days] [Extend Deadline] │
│                                                                   │
│  [Close Round Early] [Extend Deadline] [View Results] [Archive] │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

**Feedback Request View (Rater's Perspective):**

```
┌─────────────────────────────────────────────────────────────────┐
│  360 FEEDBACK REQUEST                                  [Help]     │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  You're invited to provide feedback on: Alex Chen                │
│  Due by: February 28, 2024                                        │
│  Time to Complete: 10 minutes                                     │
│  Feedback Type: Annual 360 Review                                │
│  Your Relationship: Peer (reporting to same manager)             │
│                                                                   │
│  Your feedback will be used for Alex's development and           │
│  performance review. Your responses are confidential.            │
│                                                                   │
│  [Start Feedback] [Save for Later] [Not Applicable - Skip]       │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  FEEDBACK QUESTIONS                                              │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Communication & Clarity                                         │
│  How effective is Alex at communicating ideas and information?  │
│  [1] [2] [3] [4⭐] [5] | Very Effective                          │
│                                                                   │
│  Comments (optional):                                            │
│  [Alex communicates clearly in meetings and written updates.]   │
│                                                                   │
│ ──────────────────────────────────────────────────────────────  │
│                                                                   │
│  Collaboration & Teamwork                                        │
│  How well does Alex collaborate with team members?               │
│  [1] [2] [3] [4] [5⭐] | Excellent                               │
│                                                                   │
│  Comments (optional):                                            │
│  [One of the best team players on the team. Always willing to  │
│   help others and contribute to team success.]                  │
│                                                                   │
│ ──────────────────────────────────────────────────────────────  │
│                                                                   │
│  [Next Question] [Previous] [Save Progress] [Submit]             │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

**Feedback Summary Results:**

```
┌─────────────────────────────────────────────────────────────────┐
│  YOUR 360 FEEDBACK RESULTS                                       │
├─────────────────────────────────────────────────────────────────┤
│  Annual 360 Review - Cycle 2024                                  │
│  Feedback Summary | Strengths | Development Areas | Action Plan  │
│                                                                   │
│  FEEDBACK OVERVIEW                                               │
│  Feedback Received From: 7 raters (1 Manager, 3 Peers, 3 Reports)│
│  Average Rating (1-5 scale): 4.3/5.0  (Very Strong)              │
│  Consistent Theme: Strong communicator, good collaborator        │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  TOP STRENGTHS (mentioned in 6+ of 7 responses)                  │
│  ─────────────────────────────────────────────────────────────   │
│  ⭐ Communication & Clarity      (Avg: 4.6/5)                    │
│  ⭐ Collaboration & Teamwork     (Avg: 4.7/5)                    │
│  ⭐ Problem-Solving               (Avg: 4.4/5)                    │
│  ⭐ Initiative & Proactiveness    (Avg: 4.3/5)                    │
│  ⭐ Technical Expertise          (Avg: 4.4/5)                    │
│                                                                   │
│  DEVELOPMENT AREAS (mentioned in 3-5 responses)                  │
│  Development Opportunity: Delegation & Empowering Others        │
│  └─ "Alex could trust the team more and delegate responsibility" │
│  └─ "Sometimes takes on too much personally"                    │
│                                                                   │
│  Development Opportunity: Strategic Thinking                     │
│  └─ "Good at tactical problems, could think more long-term"     │
│  └─ "Could benefit from understanding business context better"  │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  GROWTH OPPORTUNITIES & RECOMMENDATIONS                          │
│  ─────────────────────────────────────────────────────────────   │
│  Based on feedback themes:                                       │
│  • Consider delegation and mentoring goal in Q2                  │
│  • Explore strategic thinking course or project                  │
│  • Schedule feedback conversations with peers                    │
│  • Discuss strengths and growth with your manager                │
│                                                                   │
│  [Schedule Feedback Conversation] [Download Report] [Share w/Manager] │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Round Creation
- Round name, description, scope (department, level)
- Select feedback template (standard questions)
- Rater types: Manager, Peers, Direct Reports, External
- Anonymous option (recommended for honesty)
- Employee can nominate additional raters
- Open/close dates
- Customize notification email

#### 2. Round Management
- Status overview (% complete, pending count)
- Completion tracking by department/person
- Reminders (auto or manual send)
- Deadline extension options
- Close round early option

#### 3. Rater Experience
- Invitation with context (employee role, relationship to rater)
- Timed (10 min average)
- Structured questions with rating scales
- Optional comments for each question
- Progress saving
- Submit with confirmation

#### 4. Feedback Summary Results
**For Each Participant:**
- Average ratings by competency
- Key themes (strengths, development areas)
- Quotes from raters (anonymized)
- Consistency indicators ("6 of 7 mentioned X")
- Recommendations for growth

#### 5. Conversation Prompts
- Suggestions for 1-on-1 discussions
- Download report option
- Share with manager option
- Action plan for development

### AI Features

**Rater Matching:**
- Suggests optimal raters: "Peers who work closely with you 40+ hours/month"
- Identifies bias: "3 raters are close friends - balance with objective peers"

**Feedback Synthesis:**
- Automatically identifies common themes
- "6 of 7 mentioned strong communication"
- Surfaces nuance: "Strengths as individual contributor, consider management readiness"

**Development Recommendations:**
- Suggests learning based on feedback gaps
- "Feedback shows delegation gap - recommend leadership coaching"
- Identifies peer mentors: "Sarah has strength here, consider pairing"

**Consistency Checking:**
- Flags outlier feedback: "One rater rated 2/5 when others rated 4.5/5"
- Suggests follow-up: "One manager rated significantly lower - discuss?"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Rating Scales**: Numbers (1-5) + text labels (Poor, Excellent)
  - Selected clearly marked (bold, checked radio button)
- **Completion Bar**: % number + visual bar
- **Results Themes**: Text list (not visual shapes/colors alone)
- **Average Scores**: Clear number (4.3/5.0) + context
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Rating Scale**: Arrow keys to select (1-5), Enter to confirm
- **Comments**: Tab to text field, type, Tab to next question
- **Buttons**: [Start], [Submit], [Next], [Previous] all keyboard accessible
- **Results**: Tab through sections, arrow keys within theme lists
- **Focus**: Clear 2px border

#### Screen Reader Compatibility
- **Questions**: `<fieldset>` and `<legend>` for each question
  - `<legend>Communication & Clarity</legend>`
  - Radio buttons: `<input type="radio" aria-label="5 Stars: Very Effective">`
- **Comments**: `<textarea aria-label="Comments for communication clarity question">`
- **Results Summary**:
  - Themes as `<ul>` with `<li>` items
  - `<li>Communication & Clarity (Average: 4.6/5)</li>`
- **Quotes**: Announced as supporting evidence (not visual callouts)

#### Focus Management
- **Start**: Focus on first question
- **Question Navigation**: Focus on rating scale or text field
- **Submission**: Focus on confirmation message
- **Results Page**: Focus on summary heading

#### Error States & Validation
- **Incomplete Feedback**: "Some questions not answered - complete before submitting?"
  - Allow save as draft
- **Rating Missing**: "Rating required for Communication & Clarity"

#### Motion & Animation
- **Progress Through Questions**: Instant page change
- **Results Appearance**: Static or simple fade
- **Theme Loading**: No spinning loader, text: "Synthesizing feedback..."

#### Touch Accessibility
- **Radio Buttons**: 44x44px minimum tap targets
- **Comment Fields**: 44px height, full-width
- **Buttons**: 44x44px minimum
- **Question Cards**: Large scrollable layout (48px+ height)

### Data Model & Inputs

**360 Round:**
- Round ID, name, period
- Template ID (set of questions)
- Department/scope
- Open date, close date
- Rater types included
- Anonymous toggle
- Employee nomination option
- Status (draft, active, closed, archived)

**Feedback Response:**
- Response ID, round ID, recipient ID, rater ID
- Question ID, rating (1-5)
- Comments text
- Rater type (manager, peer, direct report, external)
- Anonymous toggle
- Timestamp

**Feedback Summary:**
- Recipient ID, round ID
- Average ratings by competency
- Themes (extracted or manually curated)
- Recommendation text

### Data Outputs & Integrations

**Employee View:**
- Results summary, themes, recommendations
- Download report

**Performance Review:**
- 360 feedback integrated into formal review (Screen 5)

**Development Planning:**
- Results feed into career development plan (Screen 7)
- Learning recommendations based on feedback

**Analytics:**
- Average ratings by role, level, department
- Consistency in feedback across raters
- Which feedback themes are most actionable

### Edge Cases & Error Handling

1. **Insufficient Raters**
   - "Only 2 responses received - results may not be representative"
   - Option to keep round open longer or proceed with limited data

2. **Rater Bias Detected**
   - "One rater consistently rates lower - data may be subjective"
   - Offer option to flag or exclude outlier

3. **Employee Receives Harsh Feedback**
   - Ensure results framed constructively
   - Offer manager/coach support for processing feedback

4. **Rater Declines**
   - Track non-completion
   - Offer alternative raters

### Inter-Screen Interactions

- **Linked to**: Feedback Submission (Screen 4)
- **Triggers**: Performance Review (Screen 5) with 360 summary
- **Links to**: One-on-One Meeting Notes (Screen 6) for discussing feedback
- **Provides Data to**: Career Development Plan (Screen 7)

---

Continuing with Screens 4-8 in next section...

## SCREEN 4: Feedback Submission Form

### Purpose & User Context
Enable structured feedback submission from managers, peers, or during interviews. Can be used for 360 feedback, interview feedback, or manager feedback on direct reports.

**Primary Users:**
- Managers (submitting feedback on direct reports)
- Interviewers (interview feedback)
- Peers (360 feedback, peer reviews)

### Key User Workflows

#### Workflow A: Manager Submitting Direct Report Feedback
1. Manager opens feedback form for direct report
2. Answers structured questions (communication, collaboration, performance, etc.)
3. Provides ratings and written comments
4. Saves draft or submits immediately
5. Feedback appears in employee's record

#### Workflow B: 360 Feedback Submission
1. Peer receives 360 feedback request
2. Opens form with 5-7 questions
3. Rates on scale, adds optional comments
4. Submits (anonymous)
5. Aggregated with other feedback

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  FEEDBACK SUBMISSION FORM                              [Help]     │
├─────────────────────────────────────────────────────────────────┤
│  Feedback for: Alex Chen (Senior Engineer)                       │
│  Feedback Type: Manager Feedback (Quarterly)                     │
│  Submission Deadline: February 28, 2024                          │
│  Time to Complete: ~10 minutes                                   │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  PERFORMANCE & IMPACT                                            │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  1. Overall Performance                                          │
│     How would you rate their overall performance this period?   │
│     [1] [2] [3] [4⭐] [5]                                       │
│     Selected: 4/5 (Strong Performance)                          │
│                                                                   │
│     Comments:                                                    │
│     [Alex has delivered strong results. Completed feature       │
│      work on time, mentored 2 junior engineers effectively.]   │
│                                                                   │
│  2. Quality of Work                                              │
│     How would you rate the quality of their work?                │
│     [1] [2] [3] [4] [5⭐]                                       │
│     Selected: 5/5 (Excellent)                                   │
│                                                                   │
│     Comments:                                                    │
│     [Code is clean, well-tested, and maintainable. No rework    │
│      needed. Exceeds standards.]                                │
│                                                                   │
│  3. Growth & Development                                         │
│     How much have they grown in their role this period?          │
│     [1] [2] [3] [4⭐] [5]                                       │
│     Selected: 4/5 (Significant Growth)                          │
│                                                                   │
│     Evidence:                                                    │
│     [Now leading code review process for team. Taking on more   │
│      complex architecture decisions. Mentoring others.]         │
│                                                                   │
│  COMPETENCIES & SKILLS                                          │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  4. Technical Competency                                         │
│     [1] [2] [3] [4] [5⭐] | Exceptional                          │
│     Context: Role requires advanced Python & system design      │
│     Assessment: Exceeds requirements                             │
│                                                                   │
│  5. Communication                                                │
│     [1] [2] [3] [4⭐] [5] | Strong                              │
│     Context: Key for leadership potential                        │
│     Assessment: Meets expectations                               │
│                                                                   │
│  6. Collaboration & Teamwork                                     │
│     [1] [2] [3] [4] [5⭐] | Excellent                            │
│     Context: Critical for engineering team                       │
│     Assessment: Exceeds expectations                             │
│                                                                   │
│  STRENGTHS & AREAS TO DEVELOP                                    │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Key Strengths (select all that apply):                          │
│  [✓] Problem-solving ability        [✓] Technical depth         │
│  [✓] Collaboration                  [ ] Leadership              │
│  [✓] Initiative/Proactiveness       [ ] Communication clarity   │
│  [ ] Customer focus                 [ ] Adaptability            │
│  [+] Add Custom Strength                                         │
│                                                                   │
│  Areas for Development (select all that apply):                  │
│  [ ] Time management               [✓] Delegation               │
│  [ ] Public speaking               [ ] Strategic thinking       │
│  [ ] Conflict resolution           [ ] Technical depth         │
│  [+] Add Custom Development Area                                 │
│                                                                   │
│  Overall Comments / Feedback:                                    │
│  [________________________________]                             │
│  [________________________________]                             │
│  [________________________________]                             │
│                                                                   │
│  RECOMMENDATION / NEXT STEPS                                     │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  What is your overall recommendation?                            │
│  [Promote / High Potential] [Perform Well] [Meet Expectations]  │
│  [Below Expectations] [Needs Improvement]                        │
│  Selected: Perform Well / High Potential                         │
│                                                                   │
│  Suggested Development Opportunities:                            │
│  □ Leadership/Management training                               │
│  □ Expand to new technical area (e.g., system design)           │
│  □ Stretch project/assignment                                   │
│  □ Executive coaching for communication                         │
│  □ Mentorship/sponsorship opportunities                         │
│  [✓] Continue current role with growth                          │
│                                                                   │
│  [Submit Feedback] [Save Draft] [Cancel]                         │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Structured Questions
- Organized by category (Performance, Competencies, Strengths)
- Rating scales with text descriptors
- Optional comments for each rating
- Context provided (what's important for this role)

#### 2. Competency Assessment
- Role-specific competencies (technical, leadership, etc.)
- Scale with performance levels (Below, Meets, Exceeds)
- Evidence field for specific examples

#### 3. Strengths & Development Areas
- Checkbox lists of common items
- Custom items allowed
- Used for pattern analysis and development planning

#### 4. Recommendation
- Overall assessment (Promote, Perform Well, Meet, Below, Needs Improvement)
- Suggested next steps
- Development opportunities

#### 5. Draft Saving
- Auto-save progress
- Resume later option
- Timestamp tracking

### AI Features

**Feedback Quality Checking:**
- Flags inconsistent feedback: "Rating 5/5 quality but commented on rework needed?"
- Suggests clarification: "Quantify impact - how many people mentored?"

**Bias Detection:**
- "Your feedback focuses heavily on technical skills - consider soft skills too?"
- Compares to your historical patterns: "You usually rate 4/5, this is 3/5 - elaborate?"

**Recommendation Matching:**
- "Rating 4.5 average typically aligns with 'Perform Well' recommendation"
- "Your recommendation conflicts with ratings - confirm?"

**Development Suggestions:**
- "With this rating pattern, suggest: leadership coaching, stretch project"
- Learns from successful employees: "High performers with similar gaps typically benefit from X"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Rating Scales**: Numbers (1-5) + text descriptors (Poor, Excellent)
  - Selected option clearly marked
- **Checkboxes**: Clear, large (24x24px minimum)
- **Sections**: Clear headings (h2) for each section
- **Comments**: Text input area, not visual annotation
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Rating Scales**: Arrow keys to select (1-5), Enter to confirm
- **Checkboxes**: Tab and Spacebar to toggle
- **Text Fields**: Tab to enter, type, Tab to next field
- **Buttons**: [Submit], [Save Draft], [Cancel] keyboard accessible
- **Focus**: Clear 2px border

#### Screen Reader Compatibility
- **Form Structure**: `<fieldset>` and `<legend>` for each section
- **Questions**: `<label>` with question text, radio buttons for ratings
  - `<input type="radio" aria-label="5 Stars: Exceptional">`
- **Comments**: `<textarea aria-label="Comments for technical competency"`
- **Checkboxes**: `<input type="checkbox" aria-label="Strength: Problem-solving ability">`
- **Recommendation**: Radio buttons with options
  - `<input type="radio" aria-label="Perform Well - demonstrates strong capability">`

#### Focus Management
- **Page Load**: Focus on first question
- **Section Changes**: Focus moves to first question in new section
- **Submission**: Focus on confirmation or success message
- **Draft Saved**: Focus on success message, allow resume from same point

#### Error States & Validation
- **Missing Required Ratings**: "Overall Performance rating is required"
- **Inconsistent Data**: "You rated 5/5 quality but mentioned rework - clarify?"
- **Incomplete Form**: Allow save as draft, warn on exit unsaved

#### Motion & Animation
- **Section Transitions**: Instant (no scrolling animation)
- **Auto-save**: Silent, no notification needed
- **Submit**: Text feedback ("Feedback submitted") not animation

#### Touch Accessibility
- **Radio Buttons**: 44x44px minimum tap targets
- **Checkboxes**: 44x44px minimum
- **Text Fields**: 44px height, full-width input
- **Buttons**: 44x44px minimum
- **Spacing**: 12px between form elements

### Data Model & Inputs

**Feedback Template:**
- Template ID, name
- Questions (ordered list)
- Question type (rating scale, text, checkboxes)
- Competency mappings

**Feedback Submission:**
- Submission ID, form ID, rater ID, recipient ID
- Question ID, rating/response
- Comments text
- Timestamp
- Draft status

### Data Outputs & Integrations

**Employee Record:**
- Feedback stored for review/performance assessment
- Aggregated for 360 summary
- Searchable by date, rater type, competency

**Performance Review:**
- Manager feedback inputs to formal review (Screen 5)

**Development Planning:**
- Feedback themes inform career development plan (Screen 7)

### Edge Cases & Error Handling

1. **Feedback Too Vague**
   - "Provide specific examples for ratings"
   - AI suggests: "You wrote 'good work' - specific impact?"

2. **Extremely High or Low Rating Without Comment**
   - "5/5 rating requires explanation - what did they do exceptionally?"
   - "1/5 rating requires documentation - what are specific concerns?"

3. **Biased Language Detected**
   - AI alert: "This word is biased - consider different phrasing"
   - Flag for HR review if needed

### Inter-Screen Interactions

- **Linked from**: 360 Feedback Request (Screen 3)
- **Triggers**: 360 Summary (Screen 3)
- **Used in**: Performance Review (Screen 5)
- **Provides Data to**: One-on-One Notes (Screen 6), Career Planning (Screen 7)

---

**Continuing with Screens 5-8 in final section...**

Due to length, the complete Part 2 with Screens 4-8 has been truncated. The complete Performance Management module would include:

**SCREEN 5: Performance Review Form** - Formal review with goal assessment, 360 feedback integration, overall rating, calibration
**SCREEN 6: One-on-One Meeting Notes** - Meeting documentation with agenda, discussion topics, action items, goal tracking  
**SCREEN 7: Career Development Plan** - Career goals, skill development, mentor relationships, succession planning
**SCREEN 8: Calibration Session** - Manager calibration to ensure consistent ratings, identify high performers/at-risk employees

Each screen would follow the same comprehensive structure with:
- Detailed workflows and use cases
- Visual layouts and wireframes
- Feature specifications
- AI integration points
- Full WCAG 2.2 AA accessibility requirements
- Data models and integrations
- Edge cases and error handling
- Inter-screen interactions

**Ready to proceed with the complete Part 2 file or move to next module?**
