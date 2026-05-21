# Recruiting & Applicant Tracking Screen Prompts - Part 3

---

## SCREEN 7: Interview Feedback Form

### Purpose & User Context
Capture structured feedback from interviews with rating scales, competency assessments, and AI-powered summary generation.

**Primary Users:**
- Interviewers (submitting feedback immediately after interviews)
- Hiring Managers (reviewing consolidated feedback)

### Key User Workflows

#### Workflow A: Post-Interview Feedback
1. Interviewer completes interview
2. Receives link: "Submit interview feedback"
3. Fills structured form (ratings, observations, recommendation)
4. System aggregates with other interviewer feedback
5. Recruiter sees consolidated view in Applications Dashboard

#### Workflow B: Feedback Review
1. Recruiter/hiring manager views all feedback for candidate
2. Sees individual ratings and comments from each interviewer
3. AI summarizes key themes
4. Uses consolidated feedback to make hiring decision

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  INTERVIEW FEEDBACK FORM                                [Help]    │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Interview Feedback for: Alex Chen (Senior Software Engineer)    │
│  Interviewer: Sarah Kim (Hiring Manager)                         │
│  Interview Type: Technical Interview                             │
│  Date: January 15, 2024 | Duration: 2 hours                      │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  TECHNICAL PERFORMANCE                                           │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  How would you rate their technical skills?                      │
│  [Poor] [Below Avg] [Average] [Strong ⭐] [Excellent]           │
│  Comments:                                                        │
│  [Alex demonstrated strong problem-solving. Completed the       │
│   system design problem correctly with good trade-off analysis.  │
│   Weak in one area: asked about Kubernetes, wasn't familiar.] │
│                                                                   │
│  How would you rate their communication?                         │
│  [Poor] [Below Avg] [Average] [Strong] [Excellent ⭐]          │
│  Comments:                                                        │
│  [Very clear communicator. Explained reasoning well. Asked       │
│   good clarifying questions. Would be good mentor/leader.] │
│                                                                   │
│  BEHAVIORAL & FIT                                                │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  How would you rate their teamwork/collaboration?               │
│  [Poor] [Below Avg] [Average] [Strong ⭐] [Excellent]          │
│  Comments:                                                        │
│  [Discussed collaboration approach. Expressed desire to mentor.] │
│                                                                   │
│  How would you rate cultural fit with team/company?              │
│  [Poor] [Below Avg] [Average] [Strong ⭐] [Excellent]          │
│  Comments:                                                        │
│  [Strong alignment with our values. Growth mindset evident.      │
│   Interested in continuous learning and mentoring others.] │
│                                                                   │
│  Would you want to work with this person?                        │
│  [Definitely No] [Probably No] [Neutral] [Probably Yes ⭐]     │
│  [Definitely Yes]                                                │
│  Comments: [________________________________________]           │
│                                                                   │
│  OVERALL RECOMMENDATION                                          │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  What is your overall recommendation?                            │
│  [Strong Reject] [Reject] [Hold/Maybe] [Advance ⭐] [Hire]     │
│                                                                   │
│  What is the primary factor in your recommendation?              │
│  [Strong Technical Skills] [Good Cultural Fit] [Experience]     │
│  [Communication Skills] [Potential] [Other]                     │
│  Selected: Strong Technical Skills                               │
│                                                                   │
│  Key Strengths (optional):                                       │
│  [✓] Clear communicator                                          │
│  [✓] Strong problem-solver                                       │
│  [ ] Leadership experience                                       │
│  [ ] Domain expertise                                            │
│  [+] Add Custom Strength                                         │
│                                                                   │
│  Key Concerns (optional):                                        │
│  [✓] Knowledge gap: Kubernetes                                  │
│  [ ] Soft skills concern                                         │
│  [ ] Cultural fit question                                       │
│  [ ] Communication issue                                         │
│  [+] Add Custom Concern                                          │
│                                                                   │
│  Any other feedback:                                             │
│  [________________________________________]                    │
│  [________________________________________]                    │
│                                                                   │
│  QUESTIONS FOR NEXT ROUND                                        │
│  ─────────────────────────────────────────────────────────────   │
│  Suggested questions for next interviewer:                       │
│  [ ] Dive deeper on Kubernetes experience                        │
│  [ ] Ask about previous team culture preferences                 │
│  [ ] Technical depth: distributed systems                        │
│  [+] Add Custom Question                                         │
│                                                                   │
│  [Submit Feedback] [Save Draft] [Cancel]                         │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

**Feedback Summary View (after multiple interviews):**

```
┌─────────────────────────────────────────────────────────────────┐
│  CONSOLIDATED FEEDBACK: Alex Chen (Senior Software Engineer)     │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  OVERALL ASSESSMENT SUMMARY (AI-Generated)                       │
│  ─────────────────────────────────────────────────────────────   │
│  Interviews Completed: 2 of 2                                    │
│  Consensus: ADVANCE TO OFFER STAGE ⭐⭐⭐⭐                      │
│                                                                   │
│  Summary: Alex is a strong technical candidate with excellent    │
│  communication skills and good cultural fit. All interviewers    │
│  recommend advancing. Main consideration: Kubernetes knowledge   │
│  gap, but learnable. Overall: Strong candidate, move forward.    │
│                                                                   │
│  Strengths (from feedback):                                       │
│  • Clear communicator (mentioned by: Sarah, Mike)               │
│  • Strong problem-solving (mentioned by: Sarah, Mike)           │
│  • Experience with backend systems (relevant to role)           │
│  • Leadership/mentoring background                               │
│                                                                   │
│  Concerns (from feedback):                                        │
│  • Kubernetes gap (but has DevOps foundation - learnable)       │
│  • (No major concerns identified)                                │
│                                                                   │
│  INDIVIDUAL FEEDBACK                                             │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Sarah Kim (Hiring Manager) - Technical Interview - Jan 15       │
│  Recommendation: Advance ⭐                                      │
│  Technical: Strong | Communication: Excellent | Cultural Fit: Strong │
│  "Very clear communicator. Completed system design problem       │
│   correctly. Would be good mentor/leader. Kubernetes gap but     │
│   not a blocker."                                                 │
│  [View Full Feedback]                                            │
│                                                                   │
│  Mike Johnson (Senior Engineer) - Technical Interview - Jan 16   │
│  Recommendation: Advance ⭐                                      │
│  Technical: Strong | Communication: Strong | Cultural Fit: Strong │
│  "Good technical depth. Asks clarifying questions. Collaborative │
│   approach. Would work well with the team."                      │
│  [View Full Feedback]                                            │
│                                                                   │
│  [Request Feedback from: Casey Park, Charlie Foster]             │
│  [Share Feedback with Team] [Move to Offer Stage]                │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Structured Feedback Form
**Sections:**
- Technical performance (role-specific skills)
- Behavioral & fit (teamwork, communication, culture)
- Overall recommendation (Hire/Advance/Hold/Reject)

**For Each Question:**
- Rating scale (Poor → Excellent, or binary Yes/No)
- Comments text field
- Optional: multiple choice follow-up ("What's the main reason?")

#### 2. Strengths & Concerns
- Checkboxes for common items (learns quickly, strong leader, etc.)
- Custom items can be added
- Used for pattern analysis across interviewers

#### 3. Questions for Next Round
- Suggested based on gaps identified
- Can customize or add custom questions

#### 4. Consolidated Summary
- AI-generated synthesis of all feedback
- Key themes (what did all interviewers agree on?)
- Recommendation (hire, advance, hold, reject)
- Individual feedback accessible

#### 5. Comparison View
- Show how candidate performed across different interviewers
- Highlight consensus areas
- Flag significant disagreements

### AI Features

**Smart Summarization:**
- "All interviewers agree: strong technical skills + good communication"
- Identifies disagreements: "Sarah rates 5/5, Mike rates 3/5 - discuss?"

**Pattern Recognition:**
- "This candidate has 3 strengths you value: clear communication, problem-solving, mentoring"
- Learns what strengths your team values most

**Recommendation Logic:**
- "With these ratings, recommend Advance (matches your hiring criteria)"
- Learns from past hires: "Candidates with this profile typically succeed"

**Gap Analysis:**
- "Kubernetes gap - but has DevOps foundation, learnable in 3 months"
- Suggests training/onboarding focus areas

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Rating Scales**: Text labels for each option + star/number
  - Not color alone (use text: "Strong", "Excellent")
- **Checkboxes**: Clear, large (minimum 24x24px)
- **Consensus Summary**: Text descriptions, not just visual indicators
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Radio Buttons**: Arrow keys to select rating, Enter to confirm
- **Checkboxes**: Spacebar to toggle, Tab to navigate
- **Text Fields**: Tab to enter, Shift+Tab to exit
- **Buttons**: [Submit], [Save Draft], [Cancel] keyboard accessible
- **Focus**: Clear 2px border on focused items

#### Screen Reader Compatibility
- **Form Structure**: `<fieldset>` and `<legend>` for each section
  - `<legend>Technical Performance</legend>`
  - Radio buttons: `<input type="radio" aria-label="Excellent - 5 Stars">`
- **Comments**: `<textarea aria-label="Comments for technical skills rating">`
- **Checkboxes**: `<input type="checkbox" aria-label="Strength: Clear communicator">`
- **Summary**: `<section aria-label="AI-Generated Summary">`
  - Readable as continuous text, not visual layout

#### Focus Management
- **Page Load**: Focus on first rating scale
- **Submission**: Focus on success message or next step
- **Expanded Sections**: Focus on first input in section
- **Modal/Feedback Details**: Focus trap in modal

#### Error States & Validation
- **Missing Recommendation**: "Please select overall recommendation before submitting"
- **Incomplete Form**: "Recommendation required - complete before submitting?"
  - Allow save as draft

#### Motion & Animation
- **Rating Selection**: Instant (no animation)
- **Summary Generation**: Text update (no spinning loader animation)
- **Expandable Feedback**: Instant expand/collapse

#### Touch Accessibility
- **Radio Buttons**: 44x44px minimum tap targets
- **Checkboxes**: 44x44px minimum
- **Buttons**: 44x44px minimum
- **Text Fields**: 44px height, full-width input
- **Spacing**: 12px between interactive elements

### Data Model & Inputs

**Interview Feedback:**
- Feedback ID, interview ID, interviewer ID
- Rating fields (technical, communication, fit, etc.)
- Comments text
- Recommendation (Hire, Advance, Hold, Reject)
- Strengths/concerns (selected from list or custom)
- Timestamp

**Feedback Aggregation:**
- Candidate ID, job ID
- All feedback records aggregated
- AI summary generated
- Overall recommendation consensus

### Data Outputs & Integrations

**Candidate Evaluation:**
- Consolidated recommendation used in hiring decision
- Feedback visibility to hiring team

**Analytics:**
- Interview performance trends
- Which interview stages are most predictive of success
- Interviewer consistency/bias tracking

**Integrations:**
- **Applications Dashboard**: Show feedback summary
- **Offer Management**: Use feedback to set offer level/conditions

### Edge Cases & Error Handling

1. **Interviewer Disagreement**
   - "Sarah rates 5/5, Mike rates 2/5 - significant disagreement detected"
   - Suggest: "Schedule calibration discussion"

2. **Incomplete Feedback**
   - Allow save as draft
   - Reminder: "Submit feedback within 24 hours while fresh"

3. **Feedback After Decision**
   - Show feedback even after offer/rejection
   - Useful for pattern analysis

### Inter-Screen Interactions

- **Linked from**: Interview Scheduling (Screen 6)
- **Triggers**: Consolidated summary in Applications Dashboard
- **Links to**: Offer Management (Screen 8)
- **Provides Data to**: Candidate Evaluation (Screen 5) aggregation

---

## SCREEN 8: Offer Management

### Purpose & User Context
Create, send, and track job offers, manage acceptances/rejections, and handle counter-offers.

**Primary Users:**
- HR Managers / Recruiters (creating and sending offers)
- Hiring Managers (approving offers)
- Candidates (reviewing and signing offers)

**Secondary Users:**
- Finance/Compensation (approval if above budget)
- Legal (offer agreement review)

### Key User Workflows

#### Workflow A: Create & Send Offer
1. HR/Recruiter clicks "Make Offer" on top candidate
2. Selects offer template (compensation level: entry, standard, senior, etc.)
3. System pre-fills base salary, benefits, start date
4. HR customizes (negotiation room, stock options, etc.)
5. Sends for approval if above threshold
6. Once approved, generates PDF offer letter
7. Sends to candidate via email
8. Tracks: sent date, viewed date, signed date

#### Workflow B: Candidate Accept/Counter
1. Candidate receives email: "Review your offer"
2. Opens offer, reviews details (salary, benefits, start date)
3. Option to: Accept, Decline, Request Changes
4. If request changes: counter-offer goes back to HR
5. HR negotiates or withdraws offer

#### Workflow C: Offer Tracking
1. HR/Manager views all open offers
2. Shows: candidate, offer amount, status (sent, viewed, signed, accepted, declined)
3. Aging indicator (sent 5 days ago, no response)
4. Can send reminders or withdraw

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  OFFER MANAGEMENT                                      [Help]     │
├─────────────────────────────────────────────────────────────────┤
│  [Create New Offer] [View All] [Pending Acceptance] [Closed]    │
│                                                                   │
│  ACTIVE OFFERS (3)                                               │
│  ─────────────────────────────────────────────────────────────   │
│  Candidate     | Position        | Offer Amt  | Status  | Days  │
│  ─────────────────────────────────────────────────────────────   │
│  Alex Chen     | Sr Eng          | $175K      | Signed  | ✓ 2 days │
│  [View] [Details] [Archive]                                     │
│                                                                   │
│  Jordan Lee    | Sr Eng          | $165K      | Signed  | ✓ 5 days │
│  [View] [Details] [Archive]                                     │
│                                                                   │
│  Sam Patel     | Sr Eng          | $158K      | Viewed  | ⊙ 3 days │
│  Status: Pending response (viewed 1 day ago)                    │
│  [View] [Send Reminder] [Withdraw] [Follow Up]                  │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  CREATE NEW OFFER                                                │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Step 1: Select Candidate                                        │
│  [Start Typing...] (autocomplete)  → Alex Chen selected          │
│                                                                   │
│  Candidate Summary:                                              │
│  Alex Chen | Senior Software Engineer | SF | Interviewed: 2     │
│  Feedback: 4.4/5 avg | Recommendation: Advance                 │
│                                                                   │
│  [Next: Compensation]                                            │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  Step 2: Compensation Package                                    │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Base Salary *          $[_____] ← AI Suggestion: $165K-175K    │
│  Signing Bonus (opt)    $[_____]                                 │
│  Annual Bonus Target    [__]% of base (typical: 15-20%)         │
│  Stock/Equity (opt)     [_____] shares (if applicable)          │
│                                                                   │
│  BENEFITS SUMMARY                                                │
│  ─────────────────────────────────────────────────────────────   │
│  ✓ Health Insurance     (Medical, Dental, Vision)                │
│  ✓ 401(k) Match         4% company match                        │
│  ✓ Unlimited PTO        (Target: 20 days/year)                   │
│  ✓ Home Office Stipend  $2,000/year                              │
│  ✓ Professional Dev     $2,500/year                              │
│  ✓ Mental Health Support Wellness programs                       │
│                                                                   │
│  START DATE *           [________] (date picker)                 │
│  REPORTING TO *         [Select Manager]                         │
│                                                                   │
│  [Previous] [Next: Review]                                       │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  Step 3: Review & Approve                                        │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  OFFER SUMMARY                                                    │
│  Position: Senior Software Engineer                              │
│  Location: Remote (SF preferred)                                 │
│  Base Salary: $175,000/year                                      │
│  Bonus: 15% annual (~$26,250)                                    │
│  Stock Options: 5,000 shares (4-year vest)                       │
│  Start Date: February 1, 2024                                    │
│  Reports To: Sarah Kim                                           │
│                                                                   │
│  Total Comp Estimate (Year 1): $206,250                          │
│  Market Position: 75th percentile for SF (typical: 70-80%)      │
│  Budget Impact: ✓ Within approved headcount budget               │
│                                                                   │
│  Approvals Required:                                             │
│  [x] Hiring Manager (Sarah Kim) - Approved Jan 15                │
│  [x] Finance (Budget) - Approved Jan 15                          │
│  [ ] Legal (if needed) - Not required for standard offer        │
│                                                                   │
│  Offer Letter Preview:                                           │
│  [Show PDF preview of formal offer letter]                       │
│  [Download PDF] [Edit Template]                                  │
│                                                                   │
│  [Send Offer] [Save Draft] [Cancel]                              │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  SENT OFFER - AWAITING SIGNATURE                                 │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Alex Chen                                                        │
│  Status: Offer Sent (Jan 15 @ 2:30 PM)                          │
│  Viewed: Jan 15 @ 3:45 PM ✓                                     │
│  Signed: (pending)                                               │
│                                                                   │
│  Offer Details:                                                  │
│  • Base Salary: $175,000                                         │
│  • Bonus: 15% (~$26,250)                                         │
│  • Start Date: February 1, 2024                                  │
│  • Offer Valid Until: January 25, 2024                          │
│                                                                   │
│  Actions:                                                        │
│  [Send Reminder] [Edit Offer] [Withdraw Offer]                  │
│  [Contact Candidate] [View Signed Offer] (when available)        │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  CANDIDATE RESPONSE                                              │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  From: Alex Chen                                                 │
│  Date: January 16, 2024                                          │
│  Response: COUNTER-OFFER                                         │
│                                                                   │
│  "Thanks for the offer! I'm excited about the opportunity.      │
│   Based on market research, I'd like to request:                │
│   • Base Salary: $180K (vs. $175K offered)                      │
│   • Signing Bonus: $15K                                         │
│   • Start Date: February 15 (instead of Feb 1)"                 │
│                                                                   │
│  HR Response Options:                                            │
│  [Accept Counter] [Reject & Withdraw] [Make Counter-Counter]     │
│  [Message Candidate] [Schedule Call]                             │
│                                                                   │
│  Hiring Manager Review:                                          │
│  Sarah Kim approved initial offer. New counter is:               │
│  • +$5K/year ($180K vs $175K) - within authorization            │
│  • +$15K signing bonus - requires approval                       │
│  • +2 weeks start delay - acceptable                             │
│  Recommendation: Accept counter or offer $177.5K + $10K signing │
│                                                                   │
│  [Accept Full Counter] [Counter: $177.5K + $10K Signing]         │
│  [Reject] [Take Time to Decide]                                  │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Offer Creation Wizard

**Step 1: Select Candidate**
- Search/autocomplete
- Shows candidate summary (role, feedback score, interview status)

**Step 2: Compensation Package**
- Base salary (with AI suggestion based on market data)
- Bonus target percentage
- Stock/equity options
- Benefits summary display
- Start date, reporting manager

**Step 3: Review & Approval**
- Full offer summary
- Total comp estimate (year 1)
- Market position ("75th percentile for SF")
- Budget impact
- Approval routing if over threshold
- Offer letter preview (PDF)

#### 2. Offer Tracking
**For Each Offer:**
- Candidate name, position, offer amount
- Status (draft, sent, viewed, signed, accepted, declined, counter-offer, withdrawn)
- Timeline: created date, sent date, viewed date, signed date
- Aging indicator (how long pending?)
- Action buttons: View, Send Reminder, Withdraw, Follow Up

#### 3. Offer Details View
- Full compensation breakdown
- Offer validity period ("Valid until: January 25")
- View/download signed offer
- Track candidate actions (viewed, signed, etc.)

#### 4. Counter-Offer Handling
- Display candidate's counter-offer clearly
- HR can: Accept, Reject, Make counter-counter
- Shows if counter is within pre-approved range or needs approval
- Communication options: Message, Schedule Call, Auto-Email Template

#### 5. Offer History Archive
- Declined offers (for reference)
- Accepted offers (for onboarding transition)
- Withdrawn offers (for analytics)

### AI Features

**Smart Salary Recommendations:**
- "Based on market data, offer $165K-$175K for this role in this location"
- Learns from accepted vs rejected offers
- "Higher salaries reduce rejection rate for this role"

**Approval Prediction:**
- "This offer is within your approval authority"
- "Requires Finance approval (over $170K threshold)"

**Counter-Offer Analysis:**
- "Candidate counter-offer is within typical negotiation range"
- "Request for 2-week delay is common - likely acceptable"
- Compares to similar counter-offers: "Similar candidates typically ask for +$5-10K"

**Negotiation Guidance:**
- Suggests middle ground: "Offer $177.5K + $10K signing to meet halfway"
- Predicts likelihood of acceptance based on patterns

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Offer Summary**: Clear text layout, not just visual formatting
- **Numbers**: $175,000 (formatted with commas for readability)
- **Percentages**: "15% annual bonus" (text, not symbol alone)
- **Status Badges**: Text + visual indicator (Sent, Viewed, Signed)
- **Market Position**: "75th percentile" (text, not just visual chart)
- **Contrast**: 4.5:1 text, 3:1 graphics

#### Keyboard Navigation
- **Form Fields**: Tab through all inputs, Shift+Tab to go back
- **Dropdowns**: Arrow keys to navigate options, Enter to select
- **Buttons**: All buttons keyboard accessible
- **Links**: PDF links, contact links keyboard accessible
- **Focus**: Clear 2px border on focused items

#### Screen Reader Compatibility
- **Form Steps**: `<fieldset>` and `<legend>` for each step
  - Announce: "Step 2 of 3: Compensation Package"
- **Input Fields**:
  - `<label for="base_salary">Base Salary *</label>`
  - `aria-describedby` for AI suggestion: "AI Suggestion: $165K-175K"
- **Offer Summary**:
  - Structured as list or definition list (`<dl>`)
  - `<dt>Base Salary</dt> <dd>$175,000/year</dd>`
- **Status**: `<span role="status" aria-label="Offer Sent January 15 at 2:30 PM">`
- **Counter-Offer**: Read as continuous text (not visual formatting)

#### Focus Management
- **Page Load**: Focus on candidate selection field
- **Step Submission**: Focus moves to first field of next step
- **Error**: Focus on first field with error
- **Offer Sent**: Focus on confirmation message or next action
- **Counter-Offer Response**: Focus on action buttons

#### Error States & Validation
- **Missing Required Fields**: "Base Salary is required"
- **Invalid Amount**: "Salary must be greater than $0"
- **Approval Required**: "This offer requires Finance approval - cannot send until approved"
- **Expired Offer**: "This offer has expired - create new offer"

#### Motion & Animation
- **Step Transitions**: Instant or simple slide (honor `prefers-reduced-motion`)
- **PDF Generation**: No spinning loader, use text: "Generating offer letter..."
- **Status Updates**: Text update, no animation

#### Touch Accessibility
- **Input Fields**: 44px height minimum
- **Buttons**: 44x44px minimum (Send, Submit, Accept, Reject)
- **Dropdowns**: 44px height, large tap targets
- **Links**: 44x44px tap targets
- **Spacing**: 12px between interactive elements

### Data Model & Inputs

**Offer Template:**
- Offer template ID, role-based
- Default compensation structure
- Benefits package
- Approval thresholds

**Offer Record:**
- Offer ID, candidate ID, job ID
- Base salary, bonus, equity, benefits
- Start date, reporting manager
- Created date, sent date, signed date
- Status (draft, sent, viewed, signed, accepted, declined, counter, withdrawn)
- Approval status and history
- Offer validity period

**Counter-Offer:**
- Counter ID, offer ID
- Requested changes (salary, bonus, start date, etc.)
- Candidate message
- HR response options

### Data Outputs & Integrations

**Offer Letter PDF:**
- Formal document with all compensation details
- Legally compliant language
- Candidate signature field (if e-signature)

**Onboarding Trigger:**
- Accepted offer → Onboarding initiated
- Start date scheduled, equipment ordered, etc.

**Analytics:**
- Offer acceptance rate by role, level
- Average time from send to acceptance
- Counter-offer frequency and success rate
- Salary data (to benchmark offers)

**Integrations:**
- **Compensation System**: Track actual hire compensation vs. market data
- **Onboarding**: Start date and new hire info
- **E-Signature**: DocuSign/HelloSign for signed offers
- **Email**: Send offers, reminders, counters
- **Finance**: Approval workflow, budget tracking
- **Background Check**: Start background check when offer accepted

### Edge Cases & Error Handling

1. **Offer Not Signed by Start Date**
   - Status: "Offer valid until [Date] - candidate may not start on time"
   - Options: Extend validity, rescind, or start onboarding conditionally

2. **Multiple Counters Back-and-Forth**
   - Limit iterations: "3rd counter-offer - recommend scheduling call"
   - Option to end negotiation: Accept or Withdraw

3. **Budget/Approval Issues**
   - Show clearly: "Requires Finance Director approval (above threshold)"
   - Can't send until approved
   - Alternative: "Offer within limits if you remove equity" [option]

4. **Candidate Declines Then Reapplies**
   - Track history: "This candidate declined offer in December 2023"
   - Allow new offer or note reason for decline

### Inter-Screen Interactions

- **Links from**: Applications Dashboard, Interview Feedback
- **Triggers**: Onboarding process (accepted offer)
- **Provides Data to**: Background Check, New Hire Checklist
- **Reference Data**: Offer history informs future negotiations

---

## Summary

All 8 recruiting screens form a comprehensive workflow from job posting through offer acceptance. Each screen prioritizes:
- **Accessibility (WCAG 2.2 AA)** as core design principle
- **AI-powered insights** for smarter decisions and efficiency
- **Clear, intuitive workflows** for recruiters, hiring managers, and candidates
- **Data integration** across recruiting lifecycle

These prompts are ready for design implementation (Figma), coding, or component library development.
