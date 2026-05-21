# Performance Management Screen Prompts

> **Design Principle**: Each screen prioritizes WCAG 2.2 AA accessibility. All prompts include specific accessibility guidance inline with feature descriptions.

---

## SCREEN 1: Goal Setting & OKRs

### Purpose & User Context
Enable employees and managers to create, align, and track goals throughout the performance period using SMART goal framework and OKR methodology.

**Primary Users:**
- All Employees (setting personal goals)
- Managers (setting team/company goals, aligning cascading goals)

**Secondary Users:**
- Executives (setting company OKRs)
- HR (monitoring goal completion rates)

### Key User Workflows

#### Workflow A: Individual Goal Setting
1. Employee starts goal-setting process
2. System suggests goals based on role, previous goals, company priorities
3. Employee creates 3-5 goals for the period (quarterly or annual)
4. Uses SMART framework (Specific, Measurable, Achievable, Relevant, Time-bound)
5. Aligns goals to parent goal (manager's goal or company OKR)
6. Submits to manager for approval
7. Manager reviews, provides feedback, approves or requests changes

#### Workflow B: Goal Alignment Visualization
1. Manager views team goals to see alignment
2. Goal tree shows: Company OKR → Department Goal → Team Goal → Individual Goal
3. Identifies orphaned goals (not aligned to anything)
4. Drags goals to align with parent goal
5. Ensures no duplicate/conflicting goals

#### Workflow C: OKR Management (Executive/Manager)
1. Executive sets company OKRs for quarter/year
2. Manager cascades to team OKRs
3. Employees set personal OKs (Key Results aligned to team OKRs)
4. System shows coverage: "Company OKR: Grow revenue by 30%" is owned by 3 teams

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  GOAL SETTING & OKRs                                  [Help]     │
├─────────────────────────────────────────────────────────────────┤
│  Goal Cycle: Q1 2024 (Jan 1 - Mar 31)                           │
│  [Create Goal] [View All] [My Goals] [Team Goals] [Alignment]   │
│                                                                   │
│  MY GOALS (Q1 2024)                                              │
│  Status: 3 of 5 goals set | Submission Deadline: Dec 31, 2023   │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  GOAL 1: Ship New Feature X                                      │
│  └─ Aligns to: Team OKR - Improve Product Quality               │
│  ├─ Status: Draft                                                │
│  ├─ Progress: Not started (due: Mar 31, 2024)                   │
│  ├─ Owner: You                                                   │
│  ├─ Description: Complete feature implementation with full       │
│     test coverage by end of Q1                                   │
│  └─ Key Results:                                                 │
│      1. Complete UI design and implementation (Target: 100%)     │
│      2. Achieve 90%+ test coverage                               │
│      3. Ship to production with zero critical bugs in first week │
│  [Edit] [Align to Different Goal] [Get AI Feedback]             │
│                                                                   │
│  GOAL 2: Improve Code Quality (Team Lead Initiative)             │
│  └─ Aligns to: Company OKR - Technical Excellence                │
│  ├─ Status: Approved ✓                                           │
│  ├─ Progress: On Track (30% complete, ahead of schedule)         │
│  ├─ Owner: You + 3 teammates                                     │
│  ├─ Description: Establish and implement code review standards   │
│     across engineering team                                      │
│  └─ Key Results:                                                 │
│      1. Code review process documented (Target: Jan 31) ✓        │
│      2. 90% of PRs reviewed within 24 hours (Target: 85%) ✓      │
│      3. Average code review time < 2 hours (Target: < 2hr)       │
│  [View Progress] [Update] [Add Comment]                          │
│                                                                   │
│  GOAL 3: Professional Development - Advanced Python              │
│  └─ Aligns to: Personal Development                              │
│  ├─ Status: Approved ✓                                           │
│  ├─ Progress: In Progress (Week 4 of 8)                          │
│  ├─ Owner: You                                                   │
│  ├─ Description: Complete advanced Python course and apply       │
│     knowledge to at least 2 projects                             │
│  └─ Key Results:                                                 │
│      1. Complete DataCamp Advanced Python course (Target: Feb 15) │
│      2. Apply in 2+ projects (Target: 2 projects by Mar 31)     │
│  [View Progress] [Update]                                        │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  CREATE NEW GOAL                                                 │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Goal Title *            [________________________________]      │
│  Goal Category *         [Product ▼ | Operations | Skills | Other] │
│  Due Date *              [________] (end of quarter by default)   │
│  Description *           [________________________________]      │
│                          [________________________________]      │
│                                                                   │
│  Align to Parent Goal (optional)                                 │
│  Search: [Type to find company/team OKR...]                     │
│  Found: "Q1 OKR: Improve product quality"                       │
│  [Select] [Skip for now]                                         │
│                                                                   │
│  Key Results (optional) - Break down your goal                  │
│  ├─ Key Result 1: [________________________] (Target: __)        │
│  ├─ Key Result 2: [________________________] (Target: __)        │
│  ├─ Key Result 3: [________________________] (Target: __)        │
│  └─ [+ Add Key Result]                                           │
│                                                                   │
│  AI FEEDBACK                                                      │
│  ─────────────────────────────────────────────────────────────   │
│  [✨ Get AI Feedback on SMART Framework]                         │
│                                                                   │
│  AI Analysis:                                                     │
│  ✓ Specific: Clear and well-defined                              │
│  ✓ Measurable: Has measurable key results                        │
│  ✓ Achievable: Aligned to Q1 timeline and capabilities           │
│  ✓ Relevant: Aligns to team OKRs                                 │
│  ✓ Time-bound: Clear due date (Mar 31)                           │
│                                                                   │
│  Suggestions:                                                     │
│  • Consider adding a stretch target (90% vs typical 85%)         │
│  • How will this goal impact team/company?                       │
│  • "Learning goals typically take 20% time - manageable?"        │
│                                                                   │
│  [Accept Suggestions] [Skip]                                     │
│                                                                   │
│  [Save Draft] [Submit for Approval] [Cancel]                     │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  GOAL ALIGNMENT TREE (Manager View)                              │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Company OKR: Grow Revenue 30%                                   │
│  └─ Sales Goals (5 people)                                       │
│     ├─ Sarah: Hit $2M ARR target                                 │
│     ├─ Mike: Close 5 enterprise deals                            │
│     └─ ...                                                        │
│  └─ Product Goals (8 people)                                     │
│     ├─ Ship 3 new features                                       │
│     └─ Improve retention by 15%                                  │
│  └─ Marketing Goals (4 people)                                   │
│     └─ Launch 2 major campaigns                                  │
│                                                                   │
│  Coverage: ✓ All company OKRs have at least one owner            │
│                                                                   │
│  [View as List] [Expand/Collapse] [Print]                        │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Goal Display
**For Each Goal:**
- Title and category (product, operations, skill development, etc.)
- Description (longer context)
- Status (draft, approved, on track, at risk, completed)
- Due date
- Parent goal alignment (what company/team goal does this support?)
- Key results (break-down of goal into measurable outcomes)
- Progress tracker (% complete)
- Action buttons: Edit, Update Progress, View, Comment

#### 2. Goal Creation Form
**Multi-step or inline:**
- Title, category, description
- Parent goal selection (search and select alignment)
- Key results definition (optional but recommended)
- SMART feedback (AI validation)
- Due date and owner(s)
- Submit for manager approval

#### 3. SMART Framework Validation
- Specific: Clear and well-defined?
- Measurable: Has measurable outcomes?
- Achievable: Realistic timeline?
- Relevant: Aligns to priorities?
- Time-bound: Has deadline?
- AI provides feedback for each criterion

#### 4. Goal Alignment Tree/Visualization
- Shows company OKRs at top
- Cascades down through team/department goals
- Individual employee goals at leaf level
- Can drag-to-align goals
- Shows coverage: "All company OKRs have owners"
- Identifies orphaned goals: "This goal doesn't align to anything"

#### 5. Progress Overview
- "3 of 5 goals set" (percentage complete)
- Deadline for goal submission
- Goals by status (draft, approved, on track, at risk, completed)

#### 6. Key Results Management
- Define measurable outcomes
- Target percentages or metrics
- Update progress as work happens
- Completion percentage tracker

### AI Features

**Smart Goal Suggestions:**
- "Based on your role and past goals, consider: Improve API performance, Reduce system latency"
- Learns from successful goals: "Goals similar to this typically succeed"

**SMART Validation:**
- Feedback on each criterion
- Suggestions to improve goal quality
- "Consider making this more specific: 'Improve performance' → 'Reduce API latency by 30%'"

**Alignment Recommendations:**
- "This goal aligns well to Q1 OKR: Product Quality"
- "No one else has a goal for company OKR X - consider taking it"

**Progress Prediction:**
- "Based on current progress, you're on track to complete by Mar 31"
- "You're 30% complete at day 30 - typical pace is 33%, ahead of schedule"

**Workload Balancing:**
- "Your team has 45 goals - typical for 8 people is 24-40 goals"
- "This person has 8 goals, similar to high performers (7-9 goals typical)"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Goal Status**: Text labels (Draft, Approved, On Track, At Risk, Completed) + visual indicator
- **Progress Bars**: Number % + visual bar (not bar alone)
- **Alignment Tree**: Hierarchical structure clear with indentation + connecting lines
  - Alternative: List view option
- **Key Results**: Numbered list structure (1., 2., 3.)
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Tab Order**: Title → Category → Description → Parent Goal → Key Results → Buttons
- **Parent Goal Search**: Tab to search, type, arrow keys to select from results
- **Key Results List**: Tab through inputs, arrow keys to navigate
- **Alignment Tree**: Tab through goals, arrow keys to navigate tree, Enter to expand/collapse
  - Or provide list view as keyboard-friendly alternative
- **Buttons**: All buttons keyboard accessible
- **Focus**: Clear 2px border on focused items

#### Screen Reader Compatibility
- **Goal List**: `<ul>` with `<li>` for each goal, aria-label with full summary
  - `<li aria-label="Goal: Ship New Feature X, Draft status, Due Mar 31">`
- **Status**: `<span role="status">Approved ✓</span>`
- **Progress**: `<progress aria-label="30% complete" value="30" max="100"></progress>`
- **Alignment Tree**: Hierarchical structure with semantic markup
  - `<ol>` for goals, nested `<ol>` for child goals
  - Or use `<ul role="tree">` with `aria-expanded` for expand/collapse
- **Key Results**: `<ol>` with clear numbering

#### Focus Management
- **Page Load**: Focus on goal title or first goal in list
- **New Goal Form**: Focus on first required field (title)
- **Parent Goal Selection**: Focus on search field, arrow keys navigate results
- **Tree Navigation**: Focus indicates current node, arrow keys navigate
- **Submission**: Focus on confirmation or next step

#### Error States & Validation
- **Required Fields**: Title, category, due date marked with asterisk + aria-required="true"
- **Invalid Goal**: "Goal title is required" (specific message)
- **Validation**: Real-time or on submit:
  - "Due date must be before quarter end"
  - "Parent goal must be selected or skip for now"

#### Motion & Animation
- **Tree Expand/Collapse**: Instant or simple slide (honor `prefers-reduced-motion`)
- **Progress Update**: Instant update (no animation)
- **AI Feedback**: Text update, no animated loading

#### Touch Accessibility
- **Buttons**: 44x44px minimum ([Create Goal], [Submit], [Update])
- **Goal Cards**: Large tap area (48px+ height)
- **Input Fields**: 44px height, full-width
- **Tree Expand Icon**: 44x44px minimum
- **Spacing**: 12px between interactive elements

### Data Model & Inputs

**Goal:**
- Goal ID, owner ID, period (Q1, Q2, annual, etc.)
- Title, description, category
- Parent goal ID (for alignment)
- Due date, created date
- Status (draft, approved, in_progress, completed, abandoned)
- Progress percentage
- Key results (ordered list)

**Key Result:**
- KR ID, goal ID
- Description, target metric/percentage
- Progress (current state)
- Completed date (if applicable)

### Data Outputs & Integrations

**Manager Dashboard:**
- Team goals overview, coverage, alignment
- Goal submission deadline status

**Performance Review Integration:**
- Goals and progress used in review (Screen 5)

**Learning Integration:**
- Professional development goals linked to learning paths
- Course recommendations based on skill development goals

**Analytics:**
- Goal completion rates by role, department
- Most common goal categories
- Goal alignment patterns

### Edge Cases & Error Handling

1. **Goal Changed Mid-Period**
   - Allow goal editing with version history
   - "Goal updated Jan 15 - previous version available"

2. **Parent Goal Completed Early**
   - Notify child goal owners: "Parent goal achieved - adjust if needed?"
   - Allow goal repurposing or completion

3. **Goal Becomes Blocked**
   - Mark as "blocked" with reason
   - AI alerts: "3 goals blocked - escalate to manager?"

4. **Missed Deadline**
   - Allow extension with manager approval
   - Track: "Extended 2 weeks, original due date was Mar 31"

### Inter-Screen Interactions

- **Linked to**: Goal Progress Tracking (Screen 2)
- **Used in**: Performance Review (Screen 5)
- **Links to**: Learning Recommendations (if skill goals)
- **Provides Data to**: One-on-One Meeting Notes (Screen 6)

---

## SCREEN 2: Goal Progress Tracking

### Purpose & User Context
Monitor progress toward goals throughout the performance period with regular updates, blocker detection, and AI-powered insights.

**Primary Users:**
- All Employees (updating their own goal progress)
- Managers (tracking team member progress, identifying blockers)

**Secondary Users:**
- HR/Executives (monitoring company goal progress)

### Key User Workflows

#### Workflow A: Regular Progress Updates
1. Employee logs in, sees "Goals due for update"
2. Opens each goal for progress input
3. Updates: current progress %, blocker status, context
4. Manager receives notification: "Alex updated goals"
5. Manager reviews, provides feedback or next steps

#### Workflow B: Blocker Management
1. Employee marks goal as "blocked"
2. Provides reason: "Waiting on API from Platform team"
3. AI suggests solutions: "Timeline impact: finish by Apr 15 instead of Mar 31?"
4. Manager is alerted, can provide unblocking help
5. Once unblocked, resume progress tracking

#### Workflow C: Check-In Conversations
1. Manager schedules check-in (1-on-1)
2. Reviews employee's goal progress before meeting
3. During meeting, discusses blockers, priorities, adjustments
4. Logs check-in notes
5. Updates timelines if needed

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  GOAL PROGRESS TRACKING                               [Help]     │
├─────────────────────────────────────────────────────────────────┤
│  Q1 2024 Progress (Dec 31 is review deadline)                    │
│  [My Goals] [Team Goals] [Manager View]                         │
│                                                                   │
│  YOUR GOALS - STATUS OVERVIEW                                    │
│  ─────────────────────────────────────────────────────────────   │
│  On Track: 2 | At Risk: 1 | Blocked: 1 | Not Started: 1         │
│  [████████░░░░░░░░░] Average Progress: 65%                       │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  GOAL: Ship New Feature X                                        │
│  Status: ON TRACK ✓ | Progress: [████████░] 80% | Due: Mar 31   │
│  Last Updated: Today at 2:30 PM (2 days ago: 75%)                │
│                                                                   │
│  Progress Details:                                               │
│  ├─ KR 1: UI Design & Implementation        80% Complete ✓       │
│  │         Target: 100% | Status: On Track                      │
│  │                                                                │
│  ├─ KR 2: Test Coverage                     85% Complete ✓       │
│  │         Target: 90% | Status: Exceeding Target                │
│  │                                                                │
│  └─ KR 3: Zero Critical Bugs (First Week)   TBD (ship in progress) │
│           Target: 0 bugs | Status: Not Yet Started               │
│                                                                   │
│  Blocker Status: ✓ None                                          │
│  Confidence Level: High - "We'll ship on time"                   │
│  Context/Notes:                                                  │
│  [Design is finalized, dev team moving fast. Testing plan in     │
│   place. Should be production-ready by Mar 28.]                  │
│                                                                   │
│  [Update Progress] [Edit Notes] [Add Comment] [Mark Blocked]     │
│  [Schedule Check-in] [View History]                              │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  GOAL: Improve Code Quality (Team Lead)                          │
│  Status: AT RISK ⚠ | Progress: [██████░░░░] 60% | Due: Mar 31   │
│  Last Updated: 5 days ago (was 50%)                              │
│                                                                   │
│  Progress Details:                                               │
│  ├─ KR 1: Code Review Process Documented    100% ✓               │
│  │         Completed Jan 31 (on time)                            │
│  │                                                                │
│  ├─ KR 2: 90% of PRs Reviewed Within 24hrs  50% (Current: 75%)   │
│  │         Target: 85% average | Status: Below Target            │
│  │         Expected: Reach 85% by Feb 28                         │
│  │                                                                │
│  └─ KR 3: Avg Review Time < 2 Hours         40% Impact           │
│           Target: < 2 hrs | Status: Currently 3.5hrs avg         │
│           Concern: Team is busy with feature work                │
│                                                                   │
│  Blocker Status: ⚠ YES - Team capacity constrained               │
│  Blocker Details:                                                │
│  "Team is focused on Q1 feature work - limited capacity for      │
│   code review process enforcement. Team needs training/tooling." │
│                                                                   │
│  AI Insights:                                                     │
│  ⚠️  Timeline Risk: At current pace, you'll hit 80% target       │
│      instead of 90% by Mar 31. Options:                          │
│      1. Reduce scope (target 85% instead of 90%)                │
│      2. Add resources/tooling to improve efficiency              │
│      3. Extend timeline to Apr 30                                │
│                                                                   │
│  Confidence Level: Medium - "May miss target without intervention" │
│                                                                   │
│  Context/Notes:                                                  │
│  [Team capacity is the issue. We're using a new automated tool   │
│   starting next week that should help. I'm optimistic this will  │
│   improve the metrics.]                                          │
│                                                                   │
│  [Update Progress] [Request Help] [Adjust Timeline] [Get AI Help]│
│  [Manager Check-in Scheduled: Feb 1 @ 2pm]                       │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  GOAL: Professional Development - Advanced Python                │
│  Status: BLOCKED 🔴 | Progress: [███░░░░░░░] 30% | Due: Mar 31   │
│  Last Updated: Today                                             │
│                                                                   │
│  Progress Details:                                               │
│  ├─ KR 1: Complete DataCamp Course          30% (Week 4 of 8)    │
│  │         Target: Complete by Feb 15       | Status: Blocked    │
│  │                                                                │
│  └─ KR 2: Apply in 2+ Projects              0%                   │
│           Target: 2 projects by Mar 31      | Status: Blocked    │
│                                                                   │
│  Blocker Status: 🔴 YES - Time constraint                        │
│  Blocker Details:                                                │
│  "Feature ship is taking all my time. Can't focus on learning.   │
│   Once feature ships (Mar 28), I can dedicate time to this."     │
│                                                                   │
│  Timeline Impact: Shift to Q2?                                   │
│  Current: Blocked until Mar 28                                   │
│  Revised: Start Apr 1, complete by Jun 30 (Q2)                   │
│                                                                   │
│  [Update Progress] [Reschedule to Q2] [Get Help] [Unblock]       │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

**Manager Team View:**

```
┌─────────────────────────────────────────────────────────────────┐
│  TEAM GOAL PROGRESS (Your Team)                                  │
├─────────────────────────────────────────────────────────────────┤
│  Team Progress Summary:                                          │
│  On Track: 8 | At Risk: 2 | Blocked: 1 | Not Started: 1          │
│  Avg Progress: 72% | Team Health: ✓ Good                         │
│                                                                   │
│  TEAM MEMBER GOALS                                               │
│  ─────────────────────────────────────────────────────────────   │
│  Alex Chen                                                        │
│  │ ✓ Ship Feature X                    80% | On Track           │
│  │ ⚠ Code Quality Initiative            60% | At Risk           │
│  │ 🔴 Professional Development          30% | Blocked           │
│  └─ Last Updated: Today                                          │
│     [View Details] [Check-in Needed?]                            │
│                                                                   │
│  Jordan Lee                                                       │
│  │ ✓ Database Optimization             90% | On Track           │
│  │ ✓ Mentorship Program                70% | On Track           │
│  └─ Last Updated: 2 days ago                                     │
│     [View Details]                                               │
│                                                                   │
│  Sam Patel                                                        │
│  │ ✓ API Documentation                 100% ✓ | Completed      │
│  │ ⚠ Performance Testing Framework      40% | At Risk           │
│  └─ Last Updated: 4 days ago                                     │
│     [View Details] [Schedule Check-in]                           │
│                                                                   │
│  ALERTS & BLOCKERS                                               │
│  ─────────────────────────────────────────────────────────────   │
│  ⚠️  Alex: Code Quality goal at risk (capacity issue)             │
│  ⚠️  Alex: Learning goal blocked (shipping feature)               │
│  ⚠️  Sam: Performance Testing falling behind (2 weeks)            │
│  🔴  Mike: No progress on goals this month                       │
│                                                                   │
│  [Scheduled Check-ins This Week: 3] [Schedule More]              │
│                                                                   │
│  AI Team Insights:                                                │
│  • Team avg progress 72% at day 60: typical for this point       │
│  • 2 at-risk goals - recommend 1-on-1s this week                │
│  • Overall health: Good - continue current trajectory            │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Progress Summary
- Overall progress % (average across all goals)
- Status breakdown (On Track, At Risk, Blocked, Not Started)
- Last update timing
- Confidence level (High, Medium, Low)

#### 2. Individual Goal Progress
**For Each Goal:**
- Current progress % (visual bar + number)
- Key results breakdown with individual progress
- Status trend (was 75% yesterday, now 80%)
- Blocker status (None, Yes with reason)
- Notes/context about progress
- Timeline and deadline

#### 3. Blocker Detection & Management
- Mark goal as "blocked" with reason
- AI impact analysis: "Miss target by X if unblocked by date Y"
- Suggested solutions:
  - Reduce scope
  - Add resources
  - Extend timeline
- Request manager help/unblocking

#### 4. Confidence Level
- Manager/employee assessment: High, Medium, Low
- Reasoning: "Team moving fast, no blockers"
- Used for risk assessment

#### 5. Manager Team View
- All team member goals at a glance
- Status aggregation (how many on track, at risk, blocked)
- Alerts for goals needing attention
- Last update timing (flag if >1 week old)
- Check-in recommendations

#### 6. Update Mechanism
- Can be quick: just update % and notes
- Or detailed: update each key result individually
- Add progress comments for context
- Timestamp automatically captured

### AI Features

**Progress Prediction:**
- "At current pace (80% at day 60), you'll finish by [date]"
- "Typical goals like this take 90 days - you're on schedule"

**Blocker Detection:**
- Flags goals not updated in 1 week
- "If blocked for 2 more weeks, you'll miss target. Options..."
- Proactive: "Your team has 3 goals falling behind - schedule check-ins?"

**Timeline Optimization:**
- "If you reduce scope to 85% target instead of 90%, achievable by Mar 31"
- "Adding 1 engineer to this would accelerate by 3 weeks"

**Anomaly Detection:**
- "Usually you update goals weekly - 10 days since last update"
- "This goal historically takes 100 days, you're on 120-day path"

**Team Health Assessment:**
- "Team avg progress 72% at day 60: typical"
- "One team member has no recent updates - check in?"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Status Indicators**: Text labels (On Track, At Risk, Blocked) + color + icon
  - Not color alone (use text: "On Track ✓")
- **Progress Bars**: Number % + visual bar (78% + bar)
- **Key Result List**: Numbered structure (1., 2., 3.)
- **Blocker Box**: Clear visual distinction + text "Blocker: Yes"
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Tab Order**: Goal status → Progress % → Key Results → Blocker → Notes → Buttons
- **Progress Input**: Tab to percentage field, type number, Tab to notes
- **Buttons**: [Update], [Mark Blocked], [Get Help], all keyboard accessible
- **Team View**: Tab through team members, Enter to expand details
- **Focus**: Clear 2px border

#### Screen Reader Compatibility
- **Goal Status**: `aria-label="Ship Feature X: On Track, 80% complete, due Mar 31"`
- **Progress**: `<progress aria-label="80% complete" value="80" max="100"></progress>`
- **Key Results**: `<ol>` with clear labels
  - `<li>KR 1: Test Coverage 85% complete (target: 90%)</li>`
- **Blocker**: `role="alert" aria-live="assertive" aria-label="Blocker: Team capacity constrained"`
- **Timeline Impact**: Clear text explanation (not visual)
- **Team View**: List of team members with status

#### Focus Management
- **Page Load**: Focus on first goal or status summary
- **Update Form**: Focus on progress percentage field
- **Blocker Alert**: Focus on blocker box with alert role
- **Check-in Scheduling**: Focus on confirmation

#### Error States & Validation
- **Invalid Progress**: "Progress must be between 0-100%"
- **Missing Context**: "Blocker marked but no details provided - explain?"
- **Stale Data**: "No updates in 2 weeks - progress may be outdated"

#### Motion & Animation
- **Progress Update**: Instant or simple bar fill (honor `prefers-reduced-motion`)
- **Status Changes**: Text update (no animation)
- **Alert Appearance**: No flashing or animation

#### Touch Accessibility
- **Progress Input**: Large text field (44px height)
- **Buttons**: 44x44px minimum ([Update], [Mark Blocked], [Get Help])
- **Goal Cards**: Large tap area (48px+ height)
- **Team View**: Large member rows (48px+ height)

### Data Model & Inputs

**Goal Progress Update:**
- Update ID, goal ID, employee ID
- Progress percentage
- Progress date
- Blocker status (yes/no), blocker reason
- Notes/context
- Confidence level
- Timestamp

**Key Result Progress:**
- KR ID, current progress %, update date

### Data Outputs & Integrations

**Manager Analytics:**
- Team progress trends
- Blocker patterns (what typically blocks goals?)
- Individual progress trends

**One-on-One Prep:**
- Flags goals needing discussion in check-ins
- Historical progress for comparison

**Performance Review:**
- Goal progress data inputs to performance assessment

### Edge Cases & Error Handling

1. **No Progress Updates for 2+ Weeks**
   - Alert manager: "Schedule check-in?"
   - Prompt employee: "Update status or mark as blocked"

2. **Goal Progress Goes Backward**
   - Flag as anomaly: "Progress decreased from 80% to 60%"
   - Request explanation/new blocker

3. **Goal Becomes Irrelevant**
   - Option to "abandon" goal with reason
   - Doesn't count against completion rate
   - Documented for future reference

### Inter-Screen Interactions

- **Links from**: Goal Setting (Screen 1)
- **Links to**: One-on-One Meeting Notes (Screen 6)
- **Used in**: Performance Review (Screen 5)
- **Manager tool**: Check-in scheduling, feedback

---

Continuing with Screens 3-8 in next part due to length...
