# Performance Management Screen Prompts - Part 2 (Complete: Screens 5-8)

---

## SCREEN 5: Performance Review Form

### Purpose & User Context
Formal mid-year and annual performance review capturing goal progress, competency assessments, 360 feedback synthesis, and overall performance rating with calibration.

**Primary Users:**
- Managers (completing reviews for direct reports)
- HR (monitoring completion, managing review cycles)

**Secondary Users:**
- Employees (reviewing own assessments, manager feedback)
- Executives (reviewing high-potential/at-risk employees)

### Key User Workflows

#### Workflow A: Manager Completing Review
1. Manager opens review template for each direct report
2. Imports goal progress from Goal Tracking screen
3. Views 360 feedback summary
4. Completes competency assessments
5. Provides overall rating and narrative summary
6. Submits for employee review and acknowledgment
7. Files final review

#### Workflow B: Employee Review Process
1. Employee receives notification: "Your review is ready"
2. Reviews manager's assessment
3. Adds self-assessment and comments
4. Acknowledges review (required for legal compliance)
5. Can request follow-up discussion
6. Archived in personnel file

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  PERFORMANCE REVIEW FORM (ANNUAL)                     [Help]     │
├─────────────────────────────────────────────────────────────────┤
│  Employee: Alex Chen (Senior Software Engineer)                  │
│  Review Period: January 1 - December 31, 2023                    │
│  Manager: Sarah Kim                                              │
│  Review Date: January 15, 2024                                   │
│  Status: Draft (Manager) | Employee Sign-off: Pending            │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  GOAL ACHIEVEMENT SUMMARY                                        │
│  ─────────────────────────────────────────────────────────────   │
│  Goals Set: 5 | Completed: 4 (80%) | At Risk: 1 | Abandoned: 0  │
│                                                                   │
│  Goal 1: Ship Feature X                                  ✓ 100%  │
│  Goal 2: Code Quality Initiative                        ✓ 90%   │
│  Goal 3: Professional Development                      ✓ 100%  │
│  Goal 4: Database Optimization                         ✓ 85%   │
│  Goal 5: Mentorship Program                            ⚠ 60%   │
│                                                                   │
│  Overall Goal Achievement: 87% (Exceeds typical 85%)             │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  COMPETENCY ASSESSMENT                                           │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Technical Competency           [████████░] 4.5/5 | Exceeds      │
│  Communication                  [████████░] 4.4/5 | Exceeds      │
│  Leadership & Mentoring         [███████░░] 4.2/5 | Exceeds      │
│  Collaboration                  [█████████] 4.7/5 | Exceeds      │
│  Initiative & Problem-Solving   [████████░] 4.5/5 | Exceeds      │
│  Customer Focus                 [███████░░] 4.0/5 | Meets        │
│  Adaptability                   [███████░░] 3.9/5 | Meets        │
│                                                                   │
│  Overall Competency Score:      4.3/5 (Exceeds Expectations)    │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  360-DEGREE FEEDBACK SUMMARY                                     │
│  ─────────────────────────────────────────────────────────────   │
│  Feedback Received From: 7 raters (Manager, 3 peers, 3 reports) │
│  Average Rating: 4.3/5 (Very Strong)                             │
│                                                                   │
│  Key Strengths (from 360):                                       │
│  • Excellent communicator and collaborator                       │
│  • Strong technical expertise and problem-solving                │
│  • Positive influence on team culture                            │
│  • Willingness to help others and mentor                         │
│                                                                   │
│  Development Opportunities (from 360):                           │
│  • Delegation - can trust team more, empower others              │
│  • Strategic thinking - consider longer-term business impact     │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  MANAGER ASSESSMENT & NARRATIVE                                  │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Overall Performance Rating *   [Needs Improvement]              │
│                                 [Below Expectations]             │
│                                 [Meets Expectations ▼]           │
│                                 [Exceeds Expectations]            │
│                                 [Far Exceeds Expectations]        │
│  Selected: Exceeds Expectations (4 of 5)                         │
│                                                                   │
│  Performance Summary (Required):                                 │
│  [Alex has had an exceptional year. Delivered on all major      │
│   goals, maintained high code quality, and been a valuable      │
│   mentor to junior team members. Strong contributor to team     │
│   success. Ready for increased responsibility.]                 │
│                                                                   │
│  Key Accomplishments This Year:                                  │
│  [________________________]                                       │
│  [________________________]                                       │
│                                                                   │
│  Areas for Development / Improvement Needed:                     │
│  [Delegation skills would benefit from coaching. Consider       │
│   involving Alex in strategic planning to broaden perspective.] │
│                                                                   │
│  Performance Trend:                                              │
│  Last Year: Meets Expectations | This Year: Exceeds             │
│  Trajectory: Upward ↗ | Recommendation: Promotion Potential     │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  COMPENSATION & CAREER DECISIONS                                 │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Salary Recommendation:  [Based on performance + calibration]    │
│  Current Salary:         $175,000                                │
│  Recommended Increase:   4.5% ($188,000 total)                  │
│  [AI Market Check: Competitive for role/level in SF]            │
│                                                                   │
│  Bonus Recommendation:   [Eligible - 20% of base (typical)]     │
│  Promotion Consideration: [Yes - Ready for Senior/Lead role]    │
│  Recommended Next Role:   [Staff Engineer or Tech Lead]          │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  CALIBRATION STATUS                                              │
│  ─────────────────────────────────────────────────────────────   │
│  Calibration Round:     [Not Yet Calibrated]                     │
│  Manager Peers:         [View Comparable Ratings]                │
│  [Ready for Calibration] [View Calibration Session]              │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  EMPLOYEE ACKNOWLEDGMENT                                         │
│  ─────────────────────────────────────────────────────────────   │
│  Status: Awaiting Employee Response                              │
│                                                                   │
│  [Send to Employee for Review] [Save Draft]                      │
│  [Submit & Archive] [Cancel]                                     │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Goal Achievement Summary
- Goals completed vs. total
- Visual progress for each goal
- Overall achievement percentage with benchmark comparison

#### 2. Competency Assessment
- Role-specific competencies rated 1-5
- Color-coded performance levels (Below, Meets, Exceeds, Far Exceeds)
- Overall competency score

#### 3. 360 Feedback Integration
- Summary of feedback themes
- Key strengths and development areas
- Average rating

#### 4. Manager Assessment
- Overall performance rating (dropdown or radio buttons)
- Performance narrative (required, minimum length)
- Key accomplishments and development areas
- Performance trend (improved, stable, declining)

#### 5. Compensation Decisions
- Salary adjustment recommendation with AI market check
- Bonus eligibility and amount
- Promotion consideration and recommended next role

#### 6. Calibration Integration
- Status indicator (ready for calibration, calibrated, etc.)
- Link to calibration session
- Peer comparison tool

#### 7. Employee Acknowledgment
- Required signature/acknowledgment
- Ability to add comments or dispute
- Legal compliance tracking

### AI Features

**Rating Consistency:**
- Flags inconsistencies: "Rated 5/5 technical but 2/5 for goal achievement?"
- Suggests adjustment: "Your rating pattern suggests lower overall rating is warranted"

**Compensation Analysis:**
- Market benchmarking: "4.5% increase is 75th percentile for this role/location"
- Equity checking: "This employee is 10% below market - consider adjustment"

**Promotion Readiness:**
- "Performance metrics suggest ready for promotion to Staff Engineer"
- "Consider 360 feedback on delegation before promoting to manager"

**Calibration Preparation:**
- Identifies outliers: "You rated 5/5, peer managers rated 3.5/5 - discuss in calibration"
- Predicts calibration outcome: "Likely to be calibrated to Meets Expectations"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Rating Scales**: Text labels + numbers (Meets, Exceeds, etc.)
- **Progress Bars**: Number % + visual bar
- **Competency Grid**: Table with clear row/column headers
- **360 Summary**: Text list (not visual shapes)
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Rating Dropdown**: Arrow keys to select, Enter to confirm
- **Text Areas**: Tab to enter, Shift+Tab to exit
- **Checkboxes**: Spacebar to toggle
- **Buttons**: All keyboard accessible
- **Links**: All links keyboard accessible (peer comparison, calibration)
- **Focus**: Clear 2px border

#### Screen Reader Compatibility
- **Overall Rating**: `aria-label="Overall Performance Rating: Exceeds Expectations (4 of 5)"`
- **Competency Table**: Proper `<table>` with `<thead>`, headers with `scope="col"`
- **360 Summary**: `<section aria-label="360-Degree Feedback Summary">`
- **Compensation**: Clear text for salary amount ($188,000 vs. $175,000)

#### Focus Management
- **Page Load**: Focus on overall rating or performance summary
- **Form Entry**: Focus on next required field
- **Submission**: Focus on confirmation message

#### Error States & Validation
- **Required Fields**: Performance narrative required, minimum 50 characters
- **Rating Missing**: "Overall rating required before submit"
- **Inconsistent Data**: "Rating doesn't align with goal achievement - clarify?"

#### Motion & Animation
- **Loading**: No spinner, text status: "Calculating market benchmarks..."
- **Submit**: Instant confirmation (no animation)

#### Touch Accessibility
- **Rating Dropdown**: 44px height, large tap area
- **Text Areas**: 44px height, full-width
- **Buttons**: 44x44px minimum
- **Table Navigation**: Large row heights (48px+)

### Data Model & Inputs

**Performance Review:**
- Review ID, employee ID, manager ID, period
- Goal achievement data (imported from goal tracking)
- 360 feedback summary (linked)
- Competency ratings (1-5 for each)
- Overall rating (1-5)
- Performance narrative text
- Compensation recommendations
- Promotion consideration
- Employee acknowledgment

### Data Outputs & Integrations

**Personnel File:**
- Archived review for legal/HR records
- Performance history for future reviews

**Compensation System:**
- Salary adjustment, bonus, equity recommendations
- Feed into payroll processing

**Career Development:**
- Review results input to career development planning (Screen 7)
- Promotion recommendations tracked

**Analytics:**
- Performance rating distribution by role, level, department
- Compensation allocation trends
- Promotion pipeline

### Edge Cases & Error Handling

1. **Poor Performance Rating**
   - Ensure proper documentation
   - Require specific performance incidents/evidence
   - Flag for HR review

2. **Promotion But Low 360 Feedback**
   - Alert manager: "360 feedback shows development opportunities for this role"
   - Suggest: "Consider coaching before promotion"

3. **Very High Rating But Below Average Compensation**
   - Alert: "Equity concern - high performer paid below market"
   - Recommend adjustment

### Inter-Screen Interactions

- **Linked from**: Goal Progress (Screen 2), 360 Feedback (Screen 3)
- **Triggers**: Compensation adjustments, Promotion process
- **Links to**: Career Development Plan (Screen 7), Calibration (Screen 8)
- **Used in**: Personnel records, promotion decisions

---

## SCREEN 6: One-on-One Meeting Notes

### Purpose & User Context
Document conversations between managers and direct reports, capturing discussion topics, action items, progress updates, and career development planning.

**Primary Users:**
- Managers (documenting meetings, tracking action items)
- Employees (reviewing discussion, confirming action items)

### Key User Workflows

#### Workflow A: Before 1-on-1
1. Manager opens 1-on-1 template
2. Reviews previous meeting notes
3. Adds agenda items (goal progress, blockers, feedback)
4. Prepares talking points based on performance data

#### Workflow B: During 1-on-1
1. Manager and employee discuss agenda
2. Manager takes notes on discussion
3. Identifies action items with owners and dates
4. Updates goal progress if needed

#### Workflow C: After 1-on-1
1. Manager finalizes notes
2. Sends to employee for review/confirmation
3. Action items become tasks
4. Used for future check-ins and performance review

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  ONE-ON-ONE MEETING NOTES                              [Help]     │
├─────────────────────────────────────────────────────────────────┤
│  Employee: Alex Chen | Manager: Sarah Kim                        │
│  Meeting Date: January 15, 2024 | Duration: 45 minutes          │
│  Status: [Draft] [In Progress] [Completed] [Awaiting Review]    │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  AGENDA ITEMS                                                     │
│  ─────────────────────────────────────────────────────────────   │
│  [x] Goal Progress Check-In                                      │
│  [x] Feedback on Recent Project                                  │
│  [x] Career Development Discussion                               │
│  [x] Team Dynamics / Blockers                                    │
│  [ ] [+ Add Agenda Item]                                         │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  DISCUSSION NOTES                                                │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  GOAL PROGRESS                                                    │
│  Alex is on track with most goals. Feature X shipping next week. │
│  Code quality initiative at 90% - great progress. Discussed      │
│  mentorship program - Alex willing to take lead on training      │
│  plan. Timeline adjusted to Q2 start.                            │
│                                                                   │
│  FEEDBACK ON RECENT PROJECT                                      │
│  Excellent work on database optimization. 40% performance        │
│  improvement is significant. Great leadership on the team.       │
│  Suggestion: delegate some tasks to junior engineers to build    │
│  their experience.                                               │
│                                                                   │
│  CAREER DEVELOPMENT                                              │
│  Alex is interested in Staff Engineer or Tech Lead role.         │
│  Discussed skill gaps: delegation and strategic thinking.        │
│  Recommend: leadership coaching (Q2), strategic planning project │
│  (Q2/Q3). Promotion timeline: possible late 2024 if development  │
│  goals met.                                                       │
│                                                                   │
│  FEEDBACK & RECOGNITION                                          │
│  Recognized strong mentoring of junior team member Mike.         │
│  360 feedback highlighted excellent communication and            │
│  collaboration. One note: could delegate more.                  │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  ACTION ITEMS                                                     │
│  ─────────────────────────────────────────────────────────────   │
│  [x] ✓ Complete Feature X                    Owner: Alex         │
│      Due: January 22, 2024 | Status: On Track                   │
│                                                                   │
│  [ ] Enroll in Leadership Coaching           Owner: Sarah        │
│      Due: February 15, 2024 | Status: Not Started               │
│      (Action: Research and enroll Alex in coaching program)      │
│                                                                   │
│  [ ] Define Mentorship Training Plan         Owner: Alex         │
│      Due: January 31, 2024 | Status: In Progress                │
│      (Action: Create draft training curriculum with Mike)        │
│                                                                   │
│  [ ] Strategic Planning Project Assignment   Owner: Both         │
│      Due: February 28, 2024 | Status: Pending                   │
│      (Action: Sarah to identify stretch project for Q2)          │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  NEXT MEETING                                                     │
│  Scheduled: February 19, 2024 @ 2:00 PM                          │
│  Topics to Revisit: Coaching progress, mentorship plan          │
│  [Confirm Date] [Reschedule]                                     │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  MANAGER NOTES / SENTIMENT                                       │
│  Alex continues to be a strong performer. Growth trajectory is  │
│  positive. Delegation coaching will help prepare for leadership  │
│  role. On track for promotion consideration.                     │
│                                                                   │
│  Performance Assessment: ⭐⭐⭐⭐⭐ (Exceptional)                 │
│  Engagement Level:        ⭐⭐⭐⭐⭐ (Highly Engaged)               │
│  Promotion Readiness:     ⭐⭐⭐⭐  (Very Ready)                   │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  [Mark Complete] [Send to Employee] [Share] [Export]             │
│  [Schedule Next Meeting] [Add to Performance Review]             │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Agenda Setting
- Pre-meeting agenda items with checkboxes
- Topics auto-populated based on goals, feedback, timing
- Can add custom agenda items

#### 2. Discussion Notes
- Structured sections: Goals, Feedback, Career Development, Team Dynamics, Recognition
- Free-text notes capture conversation
- Auto-timestamps for references

#### 3. Action Items
- Each item has: owner, due date, status
- Linked to goals/OKRs where applicable
- Can be converted to tasks/calendar items

#### 4. Next Meeting
- Auto-scheduled or manual scheduling
- Topics to revisit
- Calendar link

#### 5. Manager Assessment
- Performance/engagement rating quick capture
- Sentiment/tone notes
- Used for review period accumulation

#### 6. Distribution & Follow-up
- Send to employee for review/confirmation
- Export to PDF
- Add to performance review
- Create tasks from action items

### AI Features

**Meeting Insights:**
- Summarizes discussion into action items automatically
- Flags important items: "Promotion candidate, document development plan"

**Action Item Tracking:**
- Reminds when due dates approaching
- Escalates overdue items

**Pattern Recognition:**
- "Alex consistently mentions delegation - recommend coaching"
- "Recurring blocker: waiting on other team - escalate?"

**Review Integration:**
- Auto-includes important discussion points in performance review
- Flags development discussions for career planning

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Checkboxes**: Clear, large (24x24px minimum)
- **Rating Stars**: Text labels (Exceptional, Highly Engaged, Very Ready)
- **Action Items**: Text status (Not Started, In Progress, On Track, Completed)
- **Sections**: Clear headings (h2)
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Checkboxes**: Spacebar to toggle
- **Text Areas**: Tab to enter notes, Shift+Tab to exit
- **Action Item Management**: Tab through items, arrow keys to navigate
- **Buttons**: All keyboard accessible
- **Links**: Schedule meeting, export links keyboard accessible
- **Focus**: Clear 2px border

#### Screen Reader Compatibility
- **Agenda**: `<ul>` with checkbox items
  - `<li><input type="checkbox"> Goal Progress Check-In</li>`
- **Action Items**: `<ol>` with clear structure
  - `<li aria-label="Action: Complete Feature X, Owner: Alex, Due: January 22, Status: On Track">`
- **Ratings**: `aria-label="Performance Assessment: 5 of 5 stars, Exceptional"`

#### Focus Management
- **Page Load**: Focus on agenda or first text area
- **Note Completion**: Focus confirmation button
- **Action Item Entry**: Tab through fields (owner, due date, status)

#### Error States & Validation
- **Missing Next Meeting**: "Schedule next meeting before completing notes?"
- **No Action Items**: Optional, but suggested: "Consider action items from discussion?"

#### Motion & Animation
- **Auto-summarization**: Text status, no animation
- **Section Transitions**: Instant

#### Touch Accessibility
- **Checkboxes**: 44x44px minimum
- **Text Areas**: 44px height, full-width
- **Buttons**: 44x44px minimum
- **Rating Stars**: 44x44px per star
- **Action Item Rows**: 48px+ height

### Data Model & Inputs

**1-on-1 Meeting:**
- Meeting ID, employee ID, manager ID
- Meeting date, duration
- Status (draft, completed, reviewed)
- Agenda items (list)
- Discussion notes (text)
- Action items (list with owners, due dates)
- Next meeting date
- Manager assessment (ratings, sentiment)

### Data Outputs & Integrations

**Task/Calendar:**
- Action items converted to tasks
- Next meeting added to calendar

**Performance Review:**
- Discussion points and assessment fed to formal review
- Development conversations documented

**Career Development:**
- Career discussion notes inform career planning (Screen 7)
- Development goals tracked

**Analytics:**
- Meeting frequency by manager
- Common discussion topics
- Action item completion tracking

### Edge Cases & Error Handling

1. **Employee Disputes Action Item**
   - Allow employee comments
   - Flag for manager review/discussion

2. **Action Item Not Completed by Due Date**
   - Alert manager and employee
   - Option to reschedule or escalate

3. **High Performer But Low Engagement Scores**
   - Alert: "High performer showing lower engagement - check in?"
   - Suggest: "Consider workload, growth opportunities"

### Inter-Screen Interactions

- **Links from**: Goal Progress (Screen 2), 360 Feedback (Screen 3)
- **Links to**: Career Development Plan (Screen 7)
- **Feeds into**: Performance Review (Screen 5)
- **Triggers**: Task creation, calendar events

---

## SCREEN 7: Career Development Plan

### Purpose & User Context
Create personalized career development plans with learning goals, skill building, mentorship, and trajectory toward desired future roles.

**Primary Users:**
- Employees (defining career goals and development path)
- Managers (supporting and approving development plans)

**Secondary Users:**
- HR (talent development strategy, succession planning)
- Learning team (recommend courses)

### Key User Workflows

#### Workflow A: Employee Career Planning
1. Employee defines career goal (Staff Engineer, Tech Lead, Manager, etc.)
2. Identifies skills needed for target role
3. Assesses current proficiency in each skill
4. Creates development plan (courses, projects, mentorship)
5. Proposes timeline (6 months, 1 year, 18 months)
6. Submits to manager for approval

#### Workflow B: Manager Collaboration
1. Manager reviews employee's career goals
2. Provides feedback (realistic timeline, additional skill gaps)
3. Approves plan with resources/support
4. Checks progress quarterly

#### Workflow C: Development Tracking
1. Employee completes learning (courses, projects)
2. Updates skill proficiency
3. Seeks feedback from mentor
4. Assess readiness for target role

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  CAREER DEVELOPMENT PLAN                               [Help]     │
├─────────────────────────────────────────────────────────────────┤
│  Employee: Alex Chen | Manager: Sarah Kim                        │
│  Career Goal: Staff Engineer or Engineering Manager              │
│  Target Timeframe: 18 months (by Q3 2025)                        │
│  Status: [In Progress] | Last Updated: January 15, 2024          │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  CAREER GOAL & CONTEXT                                           │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Target Role(s):                                                  │
│  1. Staff Engineer (preferred) - Deep technical expertise        │
│  2. Engineering Manager - Leadership + team growth               │
│                                                                   │
│  Why This Role:                                                  │
│  [Interested in architectural decisions and technical strategy.  │
│   Want to have broader impact on company technology direction.   │
│   Currently strong IC, exploring both IC and management tracks.] │
│                                                                   │
│  Readiness Assessment:                                            │
│  Currently: Senior Engineer (L4)                                  │
│  Target: Staff Engineer (L5) or Engineering Manager               │
│  Gap Analysis: [View Details]                                    │
│  Timeline: Realistic (18 months with focused effort)             │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  SKILL DEVELOPMENT PLAN                                          │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  REQUIRED SKILLS (Staff Engineer Track)                          │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  1. Technical Architecture & System Design                       │
│     Current Level: 4/5 (Strong) | Target: 5/5 (Expert)          │
│     Development Plan:                                             │
│     • Lead 1-2 major architecture projects (Q2-Q4 2024)          │
│     • Take advanced system design course (Educative)             │
│     • Present technical talks at engineering all-hands           │
│     Timeline: Ongoing, major project by Q4 2024                  │
│                                                                   │
│  2. Strategic Thinking & Business Acumen                         │
│     Current Level: 2/5 (Developing) | Target: 4/5 (Strong)      │
│     Development Plan:                                             │
│     • Attend leadership coaching (Q2 2024)                       │
│     • Participate in strategic planning meetings                 │
│     • Read business strategy books (CEO recommendations)         │
│     • Mentor from VP Engineering on business context             │
│     Timeline: Coaching Q2, mentoring ongoing                     │
│                                                                   │
│  3. Delegation & Mentoring                                       │
│     Current Level: 3/5 (Adequate) | Target: 4.5/5 (Strong)      │
│     Development Plan:                                             │
│     • Lead mentorship program (already started)                  │
│     • Mentoring coaching sessions                                │
│     • Lead team on code review process                           │
│     Timeline: Ongoing                                             │
│                                                                   │
│  4. Communication for Influence                                  │
│     Current Level: 4/5 (Strong) | Target: 5/5 (Expert)          │
│     Development Plan:                                             │
│     • Present at external conferences (Q3/Q4 2024)              │
│     • Write technical blog posts                                 │
│     Timeline: Conference talk by Q3 2024                         │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  LEARNING OPPORTUNITIES                                          │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Courses & Training:                                              │
│  ✓ Advanced System Design (Educative) - [Start Q2 2024]         │
│  ✓ Leadership Coaching Program - [Start Q2 2024]                │
│  [ ] Executive presence workshop - [Q3 2024]                    │
│  [+ Recommend More Learning]                                     │
│                                                                   │
│  Projects & Stretch Assignments:                                 │
│  [ ] Lead major architecture decision (Q2-Q4 2024)              │
│  [ ] Strategic initiative participation (ongoing)                │
│  [ ] Cross-functional collaboration (product, sales)             │
│                                                                   │
│  Mentoring & Relationships:                                      │
│  ✓ Mentor: VP Engineering (business strategy mentor)             │
│  ✓ Mentor: Director of Engineering (technical mentor)            │
│  ✓ Mentees: Mike & Sarah (junior engineers)                      │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  DEVELOPMENT PROGRESS TRACKER                                    │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  System Design Skills:      [██████░░░░] 60% progress           │
│  Strategic Thinking:        [███░░░░░░░] 30% progress           │
│  Delegation/Mentoring:      [██████░░░░] 60% progress           │
│  Communication Impact:      [███████░░░] 70% progress           │
│                                                                   │
│  Overall Career Readiness:  [█████░░░░░] 50% (on track)         │
│                                                                   │
│  Estimated Promotion Readiness: Q2 2025 (Staff Engineer)         │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  MANAGER SUPPORT & ALIGNMENT                                     │
│  ─────────────────────────────────────────────────────────────   │
│  Status: Approved by Manager                                     │
│  Manager: Sarah Kim approved on January 15, 2024                 │
│  Support Provided:                                                │
│  • Mentorship from VP Eng, Director Eng                          │
│  • Budget: $2,500 for courses/coaching                           │
│  • Time: ~10 hours/month for learning + mentorship               │
│  • Project assignment: Major architecture project Q2 2024        │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  NEXT REVIEW CHECKPOINT                                          │
│  Scheduled: April 15, 2024 (Q2)                                  │
│  Topics: Progress on coaching, architecture project status       │
│                                                                   │
│  [Save & Share] [Export PDF] [Schedule Review] [Update Progress] │
│  [Share with Mentor] [Get Recommendations]                       │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Career Goal Definition
- Target role(s)
- Rationale/motivation
- Realistic timeline assessment
- Current level vs. target

#### 2. Skill Gap Analysis
- Current proficiency for each skill
- Target proficiency
- Development plan per skill
- Timeline for each skill

#### 3. Learning Opportunities
- Recommended courses (from Learning module)
- Stretch projects
- Mentoring relationships
- External activities (speaking, writing, etc.)

#### 4. Progress Tracking
- Overall readiness % to target
- Skill-by-skill progress
- Milestone tracking
- Promotion timeline prediction

#### 5. Manager Support
- Resources allocated (budget, time, mentors)
- Approved assignments/projects
- Regular review checkpoints

#### 6. Mentoring Integration
- Assigned mentors (by skill)
- Mentor relationships
- Feedback from mentors

### AI Features

**Career Path Recommendations:**
- "Based on your skills, Staff Engineer is strong fit, Management may take longer"
- Suggests alternative paths: "Tech Lead hybrid role available"

**Skill Gap Analysis:**
- Identifies critical gaps: "Strategic thinking is biggest gap for Staff Engineer"
- Predicts learning time: "2-3 months for system design mastery based on current pace"

**Learning Recommendations:**
- Suggests courses based on gaps and role
- Estimates ROI: "This coaching has 85% success rate for promotions in 18 months"

**Timeline Optimization:**
- "With current resources, Staff Engineer by Q2 2025 is achievable"
- "Manager track requires longer (24 months) due to additional skill gaps"

**Mentor Matching:**
- "VP Eng is excellent choice for strategy mentoring"
- Suggests peer mentors: "Jane promoted to Staff Engineer last year - consider pairing"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Progress Bars**: Number % + visual bar
- **Skill Levels**: Text labels (1-5: Novice to Expert)
- **Checkboxes**: Clear, large (24x24px)
- **Timeline**: Text dates (Q2 2024) with visual if used
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Tabs/Sections**: Tab to expand, arrow keys within
- **Form Fields**: Tab through all inputs
- **Checkboxes**: Spacebar to toggle
- **Buttons**: All keyboard accessible
- **Links**: Recommend, share, export links keyboard accessible

#### Screen Reader Compatibility
- **Heading Structure**: h1 for goal, h2 for sections (Skills, Learning, etc.)
- **Skill List**: `<ol>` with clear labels
  - `<li aria-label="Skill: System Design, Current: 4/5 Strong, Target: 5/5 Expert">`
- **Progress**: `aria-label="System Design Skills: 60% progress"`
- **Checkboxes**: `<input type="checkbox" aria-label="Completed: Advanced System Design course">`

#### Focus Management
- **Page Load**: Focus on career goal section
- **Form Entry**: Tab through fields in order
- **Update**: Focus on confirmation message

#### Error States & Validation
- **Unrealistic Timeline**: "18 months for 5-level jump in 2 skills is very aggressive"
- **No Manager Approval**: "Plan should be reviewed/approved by manager"
- **No Learning**: "Plan has no development activities - add courses or projects?"

#### Motion & Animation
- **Progress Update**: Instant (no animation)
- **Section Expansion**: Instant or simple slide

#### Touch Accessibility
- **Checkboxes**: 44x44px minimum
- **Form Fields**: 44px height, full-width
- **Buttons**: 44x44px minimum
- **Section Headers**: Large (48px+) for easy tapping

### Data Model & Inputs

**Career Development Plan:**
- Plan ID, employee ID, manager ID
- Target role(s), timeline
- Goal/rationale text
- Skills with current/target levels
- Development activities (courses, projects, mentorship)
- Progress data (% complete per skill, overall %)
- Manager approval status
- Next review date

### Data Outputs & Integrations

**Learning Integration:**
- Recommended courses → Learning Catalog (Screen 5)
- Learning progress tracked against plan

**Performance Review:**
- Career development plan included in formal review context
- Progress toward development goals evaluated

**Succession Planning:**
- High-potential employees with promotion timeline tracked
- Development readiness for future roles

**Analytics:**
- Time-to-promotion by development path
- Most common skill gaps for each target role
- Learning effectiveness for promotions

### Edge Cases & Error Handling

1. **Mentor Unavailable**
   - Flag: "Assigned mentor not responding"
   - Suggest: "Request different mentor" or "Manager can substitute"

2. **Development Path Blocked**
   - Example: "Can't get architecture project assignment"
   - Solutions: Alternative stretch project, consulting work

3. **Promotion Timeline Misaligned**
   - Employee wants Staff role in 6 months (unrealistic)
   - Alert: "Based on skill gaps and typical pace, 12-18 months is realistic"

### Inter-Screen Interactions

- **Links from**: Performance Review (Screen 5), One-on-One Notes (Screen 6)
- **Linked to**: Learning Catalog (learning recommendations)
- **Feeds**: Succession planning data
- **Used in**: Talent review decisions

---

## SCREEN 8: Calibration Session (Manager View)

### Purpose & User Context
Manager calibration meetings ensure consistent performance ratings, identify high performers and at-risk employees, and make fair compensation/promotion decisions.

**Primary Users:**
- Managers (participating in calibration discussions)
- HR/Executives (leading calibration, managing fairness)

**Secondary Users:**
- Finance (approving compensation pools)

### Key User Workflows

#### Workflow A: Pre-Calibration Preparation
1. HR prepares calibration session with manager submissions
2. Shows distribution of ratings and recommendations
3. Managers review their ratings before meeting
4. System flags outliers and inconsistencies

#### Workflow B: Calibration Discussion
1. Group of peer managers reviews ratings across similar roles
2. Discusses outlier ratings (very high or very low)
3. Reaches consensus on rating adjustments
4. Ensures consistent standards across teams

#### Workflow C: Post-Calibration
1. HR updates compensation decisions
2. Communicates final ratings to employees
3. Archives calibration notes for compliance

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  CALIBRATION SESSION - ENGINEERING MANAGERS               [Help]  │
├─────────────────────────────────────────────────────────────────┤
│  Session: Annual Calibration 2024 - Engineering                  │
│  Scope: All Senior+ Engineers (L4+)                              │
│  Facilitator: VP Engineering                                     │
│  Managers: Sarah, Mike, Jennifer (3 teams)                       │
│  Employees Under Review: 24 people                               │
│  Status: In Progress (Day 2 of 2)                                │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  RATING DISTRIBUTION                                             │
│  ─────────────────────────────────────────────────────────────   │
│  Before Calibration:         After Calibration (projected):      │
│  Far Exceeds: 2 (8%)         Far Exceeds: 2 (8%)                 │
│  Exceeds:     8 (33%)        Exceeds:     8 (33%)                │
│  Meets:       10 (42%)       Meets:       10 (42%)               │
│  Below:       4 (17%)        Below:       4 (17%)                │
│  Improvement: Consistent bell curve distribution                  │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  HIGH PERFORMER / PROMOTION CANDIDATES                           │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Alex Chen (Sarah's team)                                        │
│  Rating: Exceeds Expectations (4/5)                              │
│  Manager Recommendation: Promote to Staff Engineer               │
│  Feedback: "Strong technical skills, good leadership, ready for  │
│   broader responsibility. Delegation coaching in progress."      │
│  Calibration Consensus: ✓ Agree - Promote                        │
│  Promotion Timeline: Q2 2025 (18 months)                         │
│  Compensation Increase: 12% + equity refresh                     │
│  [View Full Profile] [Discuss] [Notes]                           │
│                                                                   │
│  Jordan Lee (Mike's team)                                        │
│  Rating: Exceeds Expectations (4/5)                              │
│  Manager Recommendation: Identify for Manager Track              │
│  Feedback: "Natural leader, strong people skills. Maybe better   │
│   fit for management than IC track."                             │
│  Calibration Discussion: Consider both tracks, get feedback      │
│  Current Consensus: [Pending Discussion]                         │
│  [View Full Profile] [Discuss] [Notes]                           │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  AT-RISK / PERFORMANCE CONCERNS                                  │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Casey Park (Jennifer's team)                                    │
│  Rating: Below Expectations (2/5)                                │
│  Manager Recommendation: Performance Improvement Plan            │
│  Concern: "Struggling with recent tech transitions. Needs support │
│   and skill development. No attitude/behavior issues."           │
│  Calibration Notes: Discussed - not a fit issue, skill gap      │
│  Support Plan: Mentoring + technical training (3 months)         │
│  Review Checkpoint: April 2024                                   │
│  [View Full Profile] [Discuss] [Notes]                           │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  OUTLIERS & DISCUSSION ITEMS                                     │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  ⚠️  Sarah's "Meets" Ratings Are 15% Higher Than Peer Avg       │
│      Sarah's Meets avg: 44% vs. Company avg: 38%                │
│      Possible causes: Stronger team, lower standards, or bias?   │
│      Discussion needed: Let's align on Meets expectations        │
│                                                                   │
│  🔴 Mike's "Below" Ratings Are 25% Higher Than Peer Avg        │
│      Mike's Below avg: 25% vs. Company avg: 17%                │
│      Discussion: Is there a team dynamic issue? Support needed?  │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  CALIBRATION NOTES & DECISIONS                                   │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Overall Observations:                                           │
│  [✓] Distribution is aligned to expectations (bell curve)        │
│  [⚠] Some variation in standards across managers - addressed     │
│  [✓] High performers identified for succession planning          │
│  [✓] At-risk employees have support plans in place               │
│  [✓] No significant fairness/equity concerns                     │
│                                                                   │
│  Agreed Actions:                                                 │
│  • Alex Chen: Promotion to Staff Engineer path confirmed         │
│  • Jordan Lee: Explore both IC and management tracks             │
│  • Casey Park: 3-month support plan, April review checkpoint     │
│  • Sarah: Calibrate "Meets" expectations to company standard     │
│  • Mike: 1-on-1 with VP to discuss team dynamics                 │
│                                                                   │
│  Fairness Review:                                                │
│  Compensation increase distribution:                             │
│  • Average increase: 4.2%                                        │
│  • By rating: Below 1.0% | Meets 3.5% | Exceeds 5.8% | Far 7%  │
│  • By gender/race: [Check equity analysis]                       │
│  ✓ No significant equity concerns identified                     │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  NEXT STEPS                                                       │
│  • HR: Finalize compensation decisions                           │
│  • Managers: Prepare to communicate ratings to teams             │
│  • HR: Schedule individual conversations for promotions/concerns  │
│  • Finance: Process merit increase approvals                     │
│                                                                   │
│  [Close Calibration] [Export Report] [Archive Session]           │
│  [Schedule Communication Prep] [Send to Finance]                 │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Rating Distribution
- Visual comparison of before/after calibration
- Bell curve analysis
- Department/peer group comparisons

#### 2. High Performers & Promotions
- Flagged candidates for promotion or high potential
- Discussion notes and consensus
- Timeline and compensation recommendations

#### 3. At-Risk Employees
- Below-expectations ratings with context
- Support plans and improvement timelines
- Checkpoints for progress monitoring

#### 4. Outlier Analysis
- Managers whose ratings deviate from peers
- Potential bias detection
- Discussion items for fairness

#### 5. Fairness Review
- Compensation increase distribution analysis
- Demographic parity checks
- Equity flagging

#### 6. Consensus & Decision Tracking
- Notes of calibration discussion
- Final agreed ratings/recommendations
- Actions and owners

### AI Features

**Fairness Monitoring:**
- Detects rating patterns by demographic (if available)
- Flags: "Women rated 8% lower on average"
- Suggests: "Review for potential gender bias in evaluations"

**Manager Calibration:**
- "Sarah rates 15% higher than peer managers"
- "Mike has outlier low ratings - discuss team concerns"

**High Performer Identification:**
- "Based on ratings and performance, 5 ready for promotion"
- "Estimated time-to-promotion: 12-24 months"

**Risk Scoring:**
- "3 employees below expectations - recommend support plans"
- "Casey Park trending down - intervention recommended"

**Compensation Optimization:**
- Calculates merit increase distribution
- "Distribution aligns to performance ratings"
- "Budget utilization: 87% of allocated pool"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Distribution Charts**: Pie/bar charts with text summary
  - Table alternative: list format
- **Outlier Flagging**: Text + visual (⚠️) indicator
- **Rating Labels**: Text labels (Below, Meets, Exceeds, etc.)
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Tabs/Sections**: Tab to expand sections, arrow keys within
- **Employee List**: Tab through candidates, arrow to navigate
- **Discussion Notes**: Tab to text field
- **Buttons**: All buttons keyboard accessible
- **Focus**: Clear 2px border

#### Screen Reader Compatibility
- **Chart Summary**: Text description of distribution
  - `aria-label="Rating Distribution: 8% Far Exceeds, 33% Exceeds, 42% Meets, 17% Below"`
- **High Performers**: `<section aria-label="High Performer: Alex Chen, Exceeds rating, recommended for promotion">`
- **Outlier Alert**: `role="alert" aria-live="assertive"` for warnings
- **Compensation**: Text explanation of increase distribution

#### Focus Management
- **Page Load**: Focus on rating distribution or high performers section
- **Discussion**: Focus on text area for notes
- **Actions**: Focus on confirmation after decisions

#### Error States & Validation
- **Unresolved Outliers**: "Sarah's ratings are 15% higher - discuss before finalizing?"
- **Missing Support Plans**: At-risk employees without plans
- **Incomplete Notes**: "Document decision for audit trail"

#### Motion & Animation
- **Chart Transitions**: Static or simple fade
- **Distribution Update**: Instant

#### Touch Accessibility
- **Employee Cards**: Large (48px+) for easy tapping
- **Buttons**: 44x44px minimum
- **Discussion Text Area**: 44px height, full-width
- **Chart Interaction**: Large tap areas if interactive

### Data Model & Inputs

**Calibration Session:**
- Session ID, period, scope
- Managers participating
- Employees under review
- Pre-calibration ratings from managers
- Calibration discussions and notes
- Final calibrated ratings
- Consensus decisions
- Actions and owners

### Data Outputs & Integrations

**Compensation System:**
- Final calibrated ratings → merit increases
- Promotion recommendations → promotion process
- Budget allocation tracking

**Performance Reviews:**
- Calibrated ratings finalize reviews
- Communicated to employees

**Talent Management:**
- High performer tracking for succession planning
- At-risk employee support programs
- Development recommendations

**Analytics & Compliance:**
- Rating distribution analysis
- Demographic equity review
- Fairness audit trail

### Edge Cases & Error Handling

1. **Manager Strongly Disagrees with Calibration**
   - Document reason for override
   - Require VP/HR approval
   - Audit trail for compliance

2. **Equity Concern Detected**
   - Flag for HR/Legal review
   - May require rating adjustment
   - Documentation for defensibility

3. **Very High Turnover in One Manager's Team**
   - Investigate: management quality or external factors?
   - May need support/coaching for manager

### Inter-Screen Interactions

- **Input from**: Individual Performance Reviews (Screen 5)
- **Uses**: 360 Feedback (Screen 3), Goal Achievement (Screen 2)
- **Outputs to**: Compensation decisions, Promotion process, Talent planning
- **Integration**: Fair process documentation for legal compliance

---

## Summary: All 8 Performance Management Screens Complete

The Performance Management module provides comprehensive tools for:
- **Goal-setting & alignment** (Screens 1-2)
- **Multi-source feedback** (Screens 3-4)
- **Formal reviews** (Screen 5)
- **Ongoing conversations** (Screen 6)
- **Career development** (Screen 7)
- **Fair calibration** (Screen 8)

Each screen is designed with accessibility (WCAG 2.2 AA), AI intelligence, and integration across the performance lifecycle.

**Total Deliverables to Date:**
- ✅ Screen Inventory (48 screens)
- ✅ Onboarding & Offboarding (8 screens, 2,694 lines)
- ✅ Recruiting & Applicant Tracking (8 screens, 2,448 lines)
- ✅ Performance Management (8 screens, ~2,800 lines)

**Remaining Modules Ready to Build:**
- Employee Self-Service (8 screens)
- Learning & Development (5 screens)
- Compensation Management (5 screens)
- AI-First Features (8 screens)
