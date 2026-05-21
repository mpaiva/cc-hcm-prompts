# Onboarding & Offboarding Screen Prompts

> **Design Principle**: Each screen is designed with WCAG 2.2 AA accessibility as a core requirement, not an afterthought. All prompts include specific accessibility guidance inline with feature descriptions.

---

## SCREEN 1: New Hire Checklist

### Purpose & User Context
The New Hire Checklist is the central hub for onboarding activities, providing visibility into all tasks and milestones across the new hire's first 90 days. This screen ensures nothing falls through the cracks and keeps all stakeholders (HR, manager, new hire) aligned on progress.

**Primary Users:**
- New Hires (viewing their checklist, completing assigned tasks)
- Direct Managers (assigning tasks, checking progress, coordinating with team)
- HR Managers (creating templates, monitoring all new hires, providing support)

**Secondary Users:**
- IT Administrators (viewing equipment/access tasks assigned to them)
- Team Members (if they have specific onboarding tasks assigned)

### Key User Workflows

#### Workflow A: New Hire Self-Service
1. New hire logs in first day
2. Sees personalized checklist dashboard with their name and start date
3. Reviews tasks organized by phase (Pre-boarding → Day 1 → Week 1 → Month 1 → Month 3)
4. Completes assigned "self-service" tasks (document uploads, form completion, course enrollment)
5. Checks off completed items
6. Sees progress bar moving toward 100%

#### Workflow B: Manager Oversight
1. Manager receives new team member
2. Views manager-specific onboarding checklist
3. Completes their assigned tasks (team intro, goal-setting, 1-on-1 scheduling)
4. Can see what HR and new hire have completed
5. Receives reminders for overdue tasks
6. Marks tasks complete as they happen

#### Workflow C: HR Administration
1. HR creates new hire in system (triggered by offer accepted)
2. Selects template based on role/department (engineering, sales, support, etc.)
3. Template auto-populates with standard tasks and assigns owners
4. HR can add custom tasks specific to the hire
5. HR receives daily digest of all onboarding progress
6. Can intervene if tasks are delayed

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  NEW HIRE ONBOARDING                                   [Help]    │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Welcome, [New Hire Name]! 👋                                    │
│  Start Date: [Date] | Days Remaining: [#]                        │
│                                                                   │
│  Overall Progress: [████████░░░░░░░] 60% Complete               │
│  Next Milestone: First Week Orientation (3 days away)            │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│ CHECKLISTS (Select Tab)  [Pre-Boarding] [Day 1] [Week 1] [...]  │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│ PRE-BOARDING (Due by: [Date])                                    │
│ ─────────────────────────────────────────────────────────────    │
│ ✓ Accept offer                              Completed by: You    │
│ ✓ Background check submitted                Completed by: HR     │
│ ○ I-9 verification                          Due: [Date]          │
│   └─ Assigned to: HR Manager (Sarah)        [View Details]       │
│ ○ Workspace assigned                        Due: [Date]          │
│   └─ Assigned to: IT Admin (Mike)           [View Details]       │
│ ○ Equipment order placed                    Due: [Date]          │
│   └─ Assigned to: Procurement               [View Details]       │
│                                                                   │
│ DAY 1 (Due by: [Date])                                           │
│ ─────────────────────────────────────────────────────────────    │
│ ○ Complete HR onboarding forms              Due: Today           │
│   └─ Assigned to: You                       [Complete Now]       │
│ ○ Meet your manager                         Due: Today           │
│   └─ Assigned to: Your Manager              [Calendar]           │
│ ○ Building access & badge                   Scheduled: [Time]    │
│   └─ Assigned to: Office Manager            [View Details]       │
│                                                                   │
│ [Show More Phases] [Print Checklist] [Share with Manager]        │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Header & Progress Summary
**Visual Elements:**
- Personalized greeting with new hire's name
- Start date and countdown timer (helps with timing context)
- Overall progress bar showing % completion (visual + numeric)
- Next milestone callout (sets expectation for what's coming)

**Data Displayed:**
- New hire name, role, department, manager
- Start date countdown
- Overall completion percentage
- Key upcoming milestones

#### 2. Phase-Based Task Organization
**Structure:**
- Tabs or sections for each phase: Pre-Boarding, Day 1, Week 1, Week 2-4, Month 2-3, Later
- Each phase clearly labeled with target completion date
- Color coding for status (not-started, in-progress, completed, overdue)

**Task States:**
- ○ Not started (white circle)
- ◐ In progress (half-filled circle)
- ✓ Completed (checkmark)
- ⚠ Overdue (warning icon, red border)
- ⊘ Blocked (gray, with reason shown on hover)

#### 3. Individual Task Items
**Each task shows:**
- Checkbox for quick completion (if new hire can self-check)
- Task title (action-oriented, e.g., "Complete I-9 Verification")
- Due date (in human-readable format: "Due in 2 days" or "Due: Monday")
- Assigned person/owner ("Assigned to: Sarah Chen, HR Manager")
- Status badge (Completed, On Track, Overdue, Blocked)
- Action button (varies by task type):
  - [Complete Now] - for self-service tasks
  - [View Details] - to see more info, forms, or documents
  - [Calendar] - to schedule
  - [Upload] - for document submission
- Owner avatar with initials for quick identification

#### 4. Task Details Modal/Drawer
**Opens when clicking task:**
- Full task description
- Why this task matters (context for new hire)
- Due date with calendar integration
- Owner info + contact option ("Message Sarah")
- Prerequisites ("Must be completed after: Background Check")
- Links to required documents, forms, or systems
- Progress/status tracking
- Comments section for questions or updates
- Attachment area for submissions

#### 5. AI-Powered Features

**Smart Task Recommendations:**
- AI suggests next tasks based on completion patterns
- "You're on track! Next: Complete benefits enrollment"
- Flags potential bottlenecks (e.g., "Your background check is taking longer than usual")

**Progress Analytics:**
- Comparison to typical onboarding (anonymized): "You're 10% ahead of average progress"
- Predictive alerts: "At current pace, you'll complete by [Date]"
- Risk detection: "3 critical tasks still pending with 2 days left"

**Personalized Guidance:**
- Contextual tips for each phase ("First week tip: Introduce yourself to your team on Slack")
- Role-specific task suggestions ("For engineers, we recommend completing the tech stack training by Friday")

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Color Contrast**: Status indicators (✓, ○, ⚠) use colors + text/icons (not color alone)
  - Task list text: 4.5:1 minimum contrast ratio
  - Status badges: 3:1 minimum for non-text elements
- **Font Size**: Body text minimum 16px (readable without zoom)
- **Color Blindness**: Don't rely on color alone to communicate status
  - ✓ (green) = also has checkmark icon
  - ⚠ (red) = also has exclamation icon
  - Use text labels: "Completed", "Overdue", "In Progress"

#### Keyboard Navigation
- **Tab Order**: Logical flow (header → progress bar → phase tabs → task list → buttons)
- **Tabs for Phases**: Arrow keys navigate between tabs; Enter/Space selects
- **Task Items**: Tab through each task, spacebar to expand/collapse, Enter to open modal
- **Buttons**: All action buttons keyboard accessible ([Complete Now], [View Details], [Calendar])
- **Focus Indicators**: Clear 2px border (minimum) around focused elements, high contrast color (e.g., #0066CC)

#### Screen Reader Compatibility
- **ARIA Labels**: 
  - Phase tabs: `aria-selected="true"` for active tab
  - Task status: `aria-label="Complete: Accept offer"` (action + status)
  - Progress bar: `aria-valuemin="0" aria-valuemax="100" aria-valuenow="60" aria-label="Overall Progress: 60%"`
- **Semantic HTML**: Use `<section>` for phases, `<button>` for interactive elements, proper `<form>` structure
- **Dynamic Updates**: Use `aria-live="polite"` for progress updates ("3 tasks completed")
- **Icon Alternatives**: All icons have text labels or `aria-label`
  - Avatar initials are text, not just visual
  - Status icons paired with text ("Completed ✓")

#### Focus Management
- **Modal Dialogs**: Focus trap inside modal, focus returns to trigger when closed
- **Expandable Sections**: Announce expansion state ("Details expanded" / "Details collapsed")
- **Keyboard Shortcuts**: Publish keyboard shortcuts (? key shows legend)
  - `n` = next phase
  - `p` = previous phase
  - `Enter` = expand focused task

#### Error States & Validation
- **Missing Information Alerts**: Clear, non-color-dependent indicator
  - "⚠️ 3 overdue tasks - review now"
  - Not just a red background
- **Help Text**: Inline help for complex tasks (background check, I-9 forms)
  - Accessible via `aria-describedby` attribute
  - Always visible, not just on hover

#### Motion & Animation
- **Respect Preferences**: Honor `prefers-reduced-motion`
  - Progress bar fills without animation (instant or no-frills transition)
  - Page transitions are instant or minimal
- **Animations**: If used, keep under 500ms, avoid flashing (nothing >3 times/second)

#### Touch Accessibility
- **Touch Targets**: All buttons minimum 44x44px (can be reduced to 24x24px with spacing)
- **Task Items**: Large clickable area, not just the checkbox
- **Spacing**: At least 12px between interactive elements

#### Form Accessibility (for embedded forms)
- **Labels**: Explicit `<label>` tags with `for` attribute
  - Not just placeholder text
  - E.g., `<label for="employee_id">Employee ID</label>`
- **Error Messages**: Clear, specific, linked to form fields
  - "Error: Background check form missing 'Position' field"
  - Use `aria-invalid="true"` on fields with errors
- **Required Fields**: Mark clearly with asterisk AND text
  - "Email Address *" + aria-required="true"

### Data Model & Inputs

**New Hire Data:**
- Name, role, department, manager, start date
- Employee ID, office location
- Role category (engineer, sales, support, etc.)

**Task Data:**
- Task ID, title, description, phase
- Due date, assigned to (person/department)
- Status (not_started, in_progress, completed, overdue, blocked)
- Task type (self_service, manager_action, admin_action, system_auto)
- Prerequisites (other task IDs that must complete first)
- Links to external resources (forms, documents, links)

**Progress Tracking:**
- Completion date & time
- Completed by (person)
- Comments/notes

### Data Outputs & Integrations

**HR Manager Dashboard:**
- All new hires with their overall progress
- Alerts for overdue tasks
- Bottleneck identification (most common delayed tasks)

**Manager View:**
- Only their team's onboarding status
- Quick actions for tasks assigned to them

**Reporting:**
- Onboarding completion time by role
- Task completion rates (which tasks always delay?)
- Time-to-productivity metrics

### Edge Cases & Error Handling

1. **Task Prerequisites Not Met**
   - Display task as "blocked" with reason: "Waiting for: Background Check"
   - Show dependency chain
   - Don't allow completion until prerequisite done

2. **Overdue Tasks**
   - Visual alert with countdown: "2 days overdue"
   - Escalation email sent to owner + manager + HR
   - One-click escalation button: "Mark as urgent"

3. **New Hire Changing Roles Before Start**
   - Auto-regenerate checklist with new role template
   - Show what changed: "Your checklist has been updated due to role change"
   - Preserve any already-completed tasks

4. **System Auto-Actions Not Completing**
   - E.g., email provisioning fails
   - Show error state: "⚠️ Email provisioning failed - contact IT"
   - Provide retry button with fallback contact info

5. **Manager or HR Person Changes**
   - Reassign their tasks to new owner
   - Notification sent to all parties
   - Old owner can still see history

### Inter-Screen Interactions

- **Links to**: Document Collection (for e-signature tasks), Background Check Status, IT Access Setup, Equipment Request, Training Plan
- **Triggered by**: Offer accepted (from Recruiting module)
- **Triggers**: Training enrollment (to Learning module), Manager 1-on-1 scheduling (to Calendar)

---

## SCREEN 2: Document Collection & E-Signature

### Purpose & User Context
Digital document collection for onboarding reduces manual paperwork and ensures legal compliance. New hires and employers both need to exchange critical documents (I-9, employment contracts, benefit elections, policy acknowledgments, direct deposit forms, etc.) securely and efficiently.

**Primary Users:**
- New Hires (uploading documents, signing agreements)
- HR Managers (creating document requests, collecting signatures, storing records)

**Secondary Users:**
- Managers (may need to sign off on some documents)
- Legal Team (reviewing signed documents)

### Key User Workflows

#### Workflow A: New Hire Document Completion
1. New hire logs in and sees "Documents Requiring Action" card on onboarding dashboard
2. Views list of required documents with clear status (upload pending, waiting to sign, completed)
3. Clicks on first document (e.g., "I-9 Form")
4. Pre-filled form appears with their info auto-populated
5. Fills missing fields, uploads any required supporting documents (ID photos)
6. Clicks "Review & Sign"
7. Electronic signature interface appears
8. Draws or types signature
9. Completes and document is stored
10. Next document in queue appears automatically

#### Workflow B: HR Document Management
1. HR manager goes to "Document Templates" section
2. Selects document type (I-9, W-4, Handbook Acknowledgment, Offer Letter, etc.)
3. Pre-filled fields (company name, state-specific requirements)
4. HR maps fields to employee data (first name, last name, employee ID, etc.)
5. Sets as "required" or "optional"
6. Adds to new hire document package
7. When new hire is created, documents are queued automatically
8. HR can send reminders for unsigned documents
9. Once signed, documents are automatically archived and indexed

#### Workflow C: Compliance Review
1. HR audits tab shows all completed documents
2. Filter by document type, date range, or new hire cohort
3. Each document shows:
   - Signature validity (verified, not verified, expired)
   - Timestamp and signer name
   - Document version
4. Export for compliance audits
5. Archive completed documents

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  DOCUMENTS & E-SIGNATURE                              [Help]     │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Your Onboarding Documents                                        │
│  Complete all required documents by [Date]                       │
│  Progress: [████████░░░░░░░] 4 of 7 Complete                    │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│ REQUIRED DOCUMENTS (4 remaining)                                 │
│ ─────────────────────────────────────────────────────────────    │
│                                                                   │
│ 1. ✓ Offer Letter                                               │
│    Signed: [Date] by [You]                                      │
│    [View] [Download PDF]                                         │
│                                                                   │
│ 2. ○ I-9 Employment Eligibility                      ⚠ Due Today │
│    Status: In Progress (3 of 5 fields filled)                   │
│    [Resume Form] [Preview] [Get Help]                           │
│                                                                   │
│ 3. ○ W-4 Tax Withholding                            Due: [Date] │
│    Status: Not Started                                           │
│    [Start Form]                                                  │
│                                                                   │
│ 4. ○ Direct Deposit Authorization                   Due: [Date] │
│    Status: Form Complete - Awaiting Signature                   │
│    [Sign Now] [View Form]                                       │
│                                                                   │
│ OPTIONAL DOCUMENTS (2 available)                                 │
│ ─────────────────────────────────────────────────────────────    │
│ □ Emergency Contact Form                                         │
│   [Complete Form]                                                │
│ □ Handbook Acknowledgment                                        │
│   [Review & Sign]                                                │
│                                                                   │
│ [Request Help] [Contact HR]                                      │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Document List & Status
**For Each Document:**
- Sequential number (1, 2, 3...) for guidance
- Document title ("I-9 Employment Eligibility Form")
- Status badge:
  - ✓ Completed [Signed Date]
  - ○ In Progress (X fields filled)
  - ⊙ Ready to Sign
  - ⊘ Not Started
  - ⚠ Overdue
- Due date (if applicable)
- Progress indicator for forms (3 of 5 fields)
- Action buttons contextual to status:
  - [Resume Form] - for in-progress
  - [Start Form] - for not started
  - [Sign Now] - for complete, awaiting signature
  - [View/Download] - for completed documents

#### 2. Form Builder Interface (for new hires)
**Smart Form Pre-filling:**
- Auto-fill fields from employee profile (name, DOB, address, employee ID)
- Fields shown in logical order (e.g., personal info → tax info → signature)
- Clear distinction between auto-filled (grayed out, editable if needed) and required input fields
- Inline help text for complex fields ("State of employment eligibility verification")

**Form Features:**
- Single question per screen (progressive disclosure, reduces cognitive load)
- Clear instructions for each field
- File upload for supporting documents (e.g., ID copy for I-9)
- Save progress automatically as user fills fields
- Show estimated time to completion ("~5 min remaining")
- Visual progress indicator (page X of Y)

#### 3. E-Signature Interface
**Signature Capture Methods:**
1. **Draw Signature** (tablet/touch-friendly)
   - Canvas area for stylus/finger drawing
   - "Clear & Redraw" button
   - Preview of signature

2. **Type Signature**
   - Text input field
   - Font options (cursive styles)
   - Preview of typed signature

3. **Upload Image**
   - For pre-scanned signature images
   - Image upload and positioning

**Signature Verification:**
- Timestamp of when signature was created
- Signer name (auto-filled from profile)
- Display: "Signed by [Name] on [Date] at [Time]"
- Legal text: "By signing electronically, I agree this is my signature and represents my intention to sign this document"

#### 4. Document Preview & Review
**Before Signing:**
- Full document displayed in modal/panel
- Highlight areas where signature/initials are needed
- Show all form responses before final submission
- "Review Document" button that shows final compiled version
- Option to go back and edit fields ("Back" button)

#### 5. Completed Document Management
**For Completed Documents:**
- [Download PDF] - get a copy
- [Email to Self] - send confirmation email
- [View Signature] - see the signature details
- [Request Change] - if info needs updating (goes to HR approval)

### AI-Powered Features

**Intelligent Form Recommendations:**
- AI detects common missing fields (e.g., "State tax form required for CA employees") and suggests adding to package
- Flags state-specific requirements based on hire location

**Document Prioritization:**
- AI orders documents by: legal urgency (I-9 first), complexity (simple → complex), then by deadline
- "Next: W-4 Tax Form (5 min)" helps new hires plan their time

**Bottleneck Detection:**
- Alerts HR if document completion is delayed: "Sara has 2 docs pending for 3 days"
- Suggests automated reminder (email new hire, escalate to manager)

**Compliance Validation:**
- Checks that all required fields are filled and valid
- Flags missing signatures before allowing final submission
- Warns if document versions are outdated (e.g., "2024 W-4 template required")

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Form Fields**: Clear labels above inputs, not as placeholder text
  - `<label for="first_name">First Name</label>`
  - Placeholder text for examples only ("e.g., John")
- **Status Indicators**: Use text + icons (not color alone)
  - ✓ + "Completed"
  - ⊙ + "Ready to Sign"
  - ⚠ + "Overdue"
- **Form Groups**: Fieldset + legend for grouped fields (e.g., address fields)
- **Document Preview**: Sufficient contrast for scanned/PDF content
  - If PDF embedded, ensure text is selectable (not image-only)
  - Provide text alternative for image-based forms

#### Keyboard Navigation
- **Tab Order**: Document list → form fields → buttons → signature area
- **Form Navigation**: Tab through fields, Shift+Tab to go back
- **Save Progress**: No "Save" button needed (auto-save), but provide status: "Changes saved at 3:45 PM"
- **Submit**: Clear submit button at end, Enter on last field doesn't submit (use button instead)
- **Signature Canvas**: Keyboard alternative for drawing signature
  - Option to type signature instead
  - Or upload pre-scanned signature image

#### Screen Reader Compatibility
- **Form Announcements**:
  - `<fieldset>` for grouped fields with `<legend>`
  - `aria-describedby` for help text: `<input aria-describedby="ssn_help"> <span id="ssn_help">Format: XXX-XX-XXXX</span>`
  - `aria-required="true"` for required fields
- **Status Updates**: `aria-live="polite"` for save confirmations
  - "Changes saved at 3:45 PM"
  - "Field required: Please fill in Last Name"
- **Document List**: Semantic list structure
  - `<ol>` for ordered list of documents
  - Each document in `<li>` with role="article"
- **Progress Indicators**: Announce progress
  - "Form 2 of 5: I-9 Employment Eligibility, Page 3 of 8"

#### Focus Management
- **Form Focus**: First required field focused on page load
- **Error Focus**: Focus moves to first field with error, announce error message
- **Signature**: For signature canvas, provide clear instruction: "Press Tab to skip signature, or Tab then Enter to draw signature"
- **Modal Dialogs**: Focus trap in document preview modal, focus returns to trigger when closed

#### Error States & Validation
- **Required Fields**: Clear visual + text indicator
  - "First Name *" (asterisk) + aria-required="true"
- **Error Messages**: Specific and actionable
  - Not: "Invalid input"
  - Instead: "Social Security Number must be 9 digits in format XXX-XX-XXXX"
  - Use `aria-invalid="true"` on field with error
- **Field Validation**: Inline validation feedback (not just on submit)
  - As user types: "✓ Valid email" or "✗ Invalid email format"

#### Motion & Animation
- **Form Submission**: No spinning loaders or animations
  - Use clear text: "Submitting..." then "Document signed successfully"
- **Page Transitions**: Instant or simple fade, no parallax or complex animations

#### Touch Accessibility
- **Signature Canvas**: Must be large enough for finger drawing (minimum 200x100px)
- **Form Fields**: Input height minimum 44px, width sufficient for content
- **Buttons**: All buttons 44x44px minimum touch target
- **Spacing**: At least 12px between interactive elements

### Data Model & Inputs

**Document Template Data:**
- Template ID, name, category (tax forms, legal agreements, acknowledgments)
- Required fields (name, address, title, etc.)
- Optional fields
- Supporting document types (ID scan, etc.)
- E-signature requirement (yes/no)
- Expiration (e.g., W-4 valid for 5 years)

**Employee Document Data:**
- Document ID, template ID, employee ID
- Completion status, completion date
- Signature (if required): timestamp, method (draw/type/upload)
- Form responses (key-value pairs for each field)
- Supporting document uploads (file names, hashes)

### Data Outputs & Integrations

**HR Archive:**
- All signed documents stored with full audit trail (who, when, signature verification)
- Compliance-ready PDF with signature and timestamp
- Searchable by employee, document type, date

**Integrations:**
- **DocuSign/HelloSign API**: For enterprise e-signature workflows
- **Payroll System**: Direct Deposit form data → payroll setup
- **Tax System**: W-4 data → tax withholding calculations
- **Benefits System**: Emergency contact form → benefits records

### Edge Cases & Error Handling

1. **Signature Expiration**
   - Documents signed >5 years ago flagged as "Verify Signature Recency"
   - Easy re-sign option: "Update signature" (doesn't delete original)

2. **Form Field Changes**
   - If HR updates a template after new hire started, show notification
   - Option: "New version available" with option to update/re-sign

3. **Incomplete Form Submission**
   - Browser closes mid-form: Auto-save recovers progress
   - Show: "Welcome back! You were on step 3 of 5"

4. **Duplicate Document Submission**
   - AI detects if new hire attempts to re-upload the same document
   - "This document is already complete. Upload a different file?"

5. **Rejected Signatures**
   - If manager/HR rejects signature, new hire gets notification
   - Clear reason provided: "Signature incomplete - please initial all pages"
   - Easy one-click re-sign

### Inter-Screen Interactions

- **Links from**: New Hire Checklist (task: "Complete I-9 Verification")
- **Links to**: Document archive (view completed docs)
- **Triggers**: Background Check Status screen (after I-9 completion)
- **Provides Data to**: Payroll system (from direct deposit form), Tax system (W-4), Benefits system (emergency contact)

---

## SCREEN 3: Background Check Status

### Purpose & User Context
Background checks are a critical compliance requirement for new hires. This screen provides transparency into background check status, results, and any action items while maintaining compliance with regulations like FCRA (Fair Credit Reporting Act).

**Primary Users:**
- New Hires (checking their background check status)
- HR Managers (managing background checks, receiving results, handling exceptions)
- Hiring Managers (visibility into whether new hire can start)

**Secondary Users:**
- Finance (determining start date for payroll)
- IT (determining when to provision access)
- Legal Team (reviewing issues if results are adverse)

### Key User Workflows

#### Workflow A: New Hire Self-Service Status Check
1. New hire goes to onboarding checklist
2. Clicks "Background Check" task
3. Sees status: "In Progress" with expected completion date
4. Can view what's included in the check (criminal, credit, employment history, etc.)
5. Once complete, sees results summary
6. If issues: clear explanation of what needs review
7. Can view "Clear and Fair Access" report to check their own results

#### Workflow B: HR Background Check Management
1. HR starts new hire onboarding
2. Selects background check type based on role (standard, financial, security-sensitive, etc.)
3. Initiates check with background check provider
4. System sends checks to candidate/new hire for completion
5. HR monitor dashboard shows all pending checks with aging
6. As results come in, HR gets notified
7. For clear results: automatically advances onboarding
8. For issues: flags for review, provides guidance on next steps
9. Once resolved: updates status, unblocks downstream tasks

#### Workflow C: Handling Adverse Results
1. Background check comes back with issue (conviction history, inconsistent employment)
2. System flags for HR review: "Review required: Potential adverse item"
3. HR reviews details and decision-making framework
4. If deciding to reject: HR follows FCRA notification process
   - Send "Potential Adverse Action" notice
   - New hire can dispute findings
   - Cooling-off period enforced
5. If approved despite issue: HR documents reasoning
6. New hire notified of final decision with timeline

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  BACKGROUND CHECK STATUS                              [Help]     │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Background Check Status for [New Hire Name]                     │
│  Started: [Date] | Expected Completion: [Date] (2 days)          │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  OVERALL STATUS                                                   │
│  ┌──────────────────────────────────────────────────────────┐   │
│  │ [████████░░░░░░░░░░] In Progress (70% complete)          │   │
│  │                                                            │   │
│  │ ✓ Criminal History Check         Completed [Date]        │   │
│  │ ○ Employment History Verification  In Progress            │   │
│  │ ○ Education Verification          Pending                 │   │
│  │ ✓ Reference Checks               Completed [Date]        │   │
│  │ ○ Credit Check                    Pending                 │   │
│  │                                                            │   │
│  │ Expected Completion: [Date] or sooner                     │   │
│  └──────────────────────────────────────────────────────────┘   │
│                                                                   │
│  BACKGROUND CHECK INCLUSIONS                                     │
│  ─────────────────────────────────────────────────────────────   │
│  ✓ Criminal Background (7-year history)                         │
│  ✓ Employment History Verification                              │
│  ✓ Education Verification (Degree/Diploma)                      │
│  ✓ Reference Checks (3 professional references)                 │
│  ○ Credit Check (Financial Verification)  [Why this?]           │
│                                                                   │
│  WHAT HAPPENS NEXT?                                              │
│  ─────────────────────────────────────────────────────────────   │
│  Once your background check is complete, we'll:                 │
│  1. Review results for compliance                                │
│  2. Notify you of any follow-up items needed                     │
│  3. Proceed with final onboarding steps                          │
│                                                                   │
│  Questions? [Contact HR] [View FCRA Info] [Clear & Fair Access] │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Overall Status Overview
**Visual Components:**
- Large progress bar showing % complete
- Status label (In Progress, Completed, Pending Response, Issue Detected, Approved, Rejected)
- Timeline: "Started [Date] | Expected Completion [Date] (in 2 days)"
- Overall recommendation (if applicable): Green checkmark for "Clear" or warning icon for "Pending Review"

**Messaging:**
- Status in plain language, not jargon
- Clear timeline expectations
- Link to FAQ if delays occur

#### 2. Component Breakdown
**For Each Check Component:**
- Status icon (✓ complete, ○ in progress, ⊙ pending action from candidate)
- Component name
- Completion date (if done)
- Any issues or notes
- [View Details] link to see specifics

**Components Vary by Check Type:**
- Standard: Criminal, Employment History, Education, References
- Financial: All above + Credit Check
- Security-Sensitive: All above + Security clearance, driving history, etc.

#### 3. Actions Required Section (if applicable)
**If New Hire Action Needed:**
- Clear explanation of what's needed
- [Respond Now] button to provide info
- Deadline for response
- Example: "Employment History: Confirm dates at previous employer" with link to form

**If HR Decision Needed:**
- Visible only to HR
- Summary of issue found
- Guidance on compliance steps
- Approval/Rejection options with reasoning forms

#### 4. Clear & Fair Access Report
**FCRA Compliance:**
- Link to "View Your Background Check Report" (required by FCRA)
- New hire can see exactly what was checked and results
- Ability to dispute findings
- Dispute process instructions
- Contact info for background check provider

#### 5. Timeline & History
**Timeline View Shows:**
- When check was initiated
- When each component was started/completed
- Any delays with explanation
- Final decision date (if complete)
- All correspondence dates

### AI-Powered Features

**Predictive Delays:**
- AI flags checks that are taking longer than normal
- "Employment History verification is taking 3+ days (vs 1.5 day average)"
- Auto-escalates to provider or recommends follow-up

**Compliance Automation:**
- AI checks if adverse decision process is being followed correctly
- Ensures FCRA notices are sent appropriately
- Flags edge cases (conviction older than 7 years in CA, etc.)

**Risk Scoring:**
- For HR review: AI summarizes level of concern
- "Low risk: Minor employment date discrepancy, likely data entry error"
- "Medium risk: Two-year employment gap, recommend interview follow-up"
- Suggests decision paths

**Communication Guidance:**
- AI generates FCRA-compliant rejection letters
- Suggests tone and messaging for adverse action notices
- Provides templates for follow-up communication

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Progress Bar**: Labeled with percentage AND text status
  - aria-label="Overall progress: 70% complete, in progress"
  - Use text: "70% Complete" + visual bar (not bar alone)
- **Status Colors**: Each status has icon + text
  - ✓ (green) + "Completed"
  - ○ (gray) + "In Progress"
  - ⚠ (red) + "Issue Detected"
- **Component List**: Use semantic list (`<ul>`, `<li>`) with clear visual hierarchy
- **Font Size**: At least 16px for body text, 18px+ for status labels
- **Contrast**: 4.5:1 for text, 3:1 for graphical elements

#### Keyboard Navigation
- **Tab Order**: Overall status → component list → action buttons → timeline
- **Expand/Collapse**: Use spacebar or Enter to expand component details
- **Links**: All links keyboard accessible ([Contact HR], [View FCRA Info], [Respond Now])
- **Focus Indicators**: 2px minimum clear border around focused items
- **Skip Links**: Optional "Skip to Action Items" link if content is long

#### Screen Reader Compatibility
- **Status Announcements**:
  - Progress bar: `aria-label="Background check progress: 70% complete, in progress"`
  - Overall status: `role="status" aria-live="polite"` for updates
- **Component List**: 
  - Use `<ol>` or `<ul>` structure
  - Each item: `<li><strong>Criminal History Check</strong> <span aria-label="status: completed"> ✓ </span> Completed [Date]</li>`
- **Issues**: `aria-label="Issue detected: Employment history verification pending response. Action required by [Date]."`
- **Timeline**: Use `<time datetime="2024-01-15">January 15, 2024</time>` for semantic date markup

#### Focus Management
- **Page Load**: Focus on main status heading (h1)
- **New Updates**: If status changes while user is on page, use `aria-live="assertive"` with brief notification
  - "Background check completed - all clear"
- **Modal Dialogs**: Focus trap in "View Details" or "Clear & Fair Access" modals
- **Form Submission**: Focus moves to confirmation message on submit

#### Error States & Validation
- **Issues Detected**: Clear, specific messaging (not "Check failed")
  - "Issue detected: Employment dates don't match your resume. Please clarify."
  - Include suggested next steps
- **Required Actions**: Marked clearly with asterisk + aria-required="true"
- **Deadline Warnings**: "Action required by [Date] (5 days remaining)"
  - Use visual + text indicator, not color alone

#### Motion & Animation
- **Status Updates**: No spinning loading indicators
  - Instead: "Checking employment history... (estimated 2 days remaining)"
- **Timeline**: Static or simple linear animation, no parallax
- **Transitions**: Instant or subtle fade, respect `prefers-reduced-motion`

#### Touch Accessibility
- **Component List Items**: Large touch targets (minimum 44x44px)
- **Buttons**: [Contact HR], [Respond Now], [View Details] all 44x44px+ 
- **Spacing**: 12px minimum between interactive elements
- **Mobile View**: Stack vertically for readability on small screens

### Data Model & Inputs

**Background Check Package:**
- Package type (standard, financial, security-sensitive)
- Components included (criminal, employment, education, references, credit, driving history)
- Provider (e.g., Checkr, Sterling, GoodHire)

**Check Status Data:**
- Check ID, candidate ID, package type
- Overall status (pending, in_progress, completed, completed_with_issues, approved, rejected)
- Initiated date, completed date
- Result summary (clear, clear_with_review, issue_detected, awaiting_decision)
- Individual component statuses

**Issue/Finding Data:**
- Finding ID, finding type (conviction, employment gap, education unverified, etc.)
- Severity (minor, moderate, significant)
- Description
- Recommended action
- Resolution status (resolved, pending, appealing, under_review)

### Data Outputs & Integrations

**HR Dashboard:**
- All pending background checks with aging
- Checks completed with issues (flags for decision)
- Completed/approved checks ready to advance onboarding

**Integrations:**
- **Checkr/Sterling API**: Auto-fetch results, status updates
- **Onboarding Workflow**: Auto-advance to next step if approved, block if issue detected
- **Compliance Tracking**: Archive all decisions and FCRA notices for audit
- **Start Date Management**: Freeze start date if background check delayed

### Edge Cases & Error Handling

1. **Candidate Unresponsive**
   - After 3 days without response to action items, auto-escalate
   - Manager + HR notified
   - Can rescind offer if background check not completed by start date

2. **Background Check Discrepancies**
   - Candidate disputes finding
   - HR has dispute tracking workflow
   - System tracks "Under Appeal" status until resolved

3. **Provider Delays**
   - If check pending >7 days, alert HR with provider info
   - Option to request expedite or switch provider

4. **Adverse Decision**
   - System enforces FCRA "cooling off" period (5 business days)
   - Prevents accidental early rejection letter
   - Tracks all notification attempts

5. **New Hire Start Date Before Results**
   - HR can conditionally approve (start with reduced access)
   - System tracks as "pending results" until finalized
   - Blocks higher-risk access (admin, finance) until cleared

### Inter-Screen Interactions

- **Linked from**: New Hire Checklist
- **Blocked by**: Document Collection (I-9 must be complete before background check starts)
- **Blocks**: IT Systems Access Setup, Equipment Request (until cleared)
- **Triggers**: Manager notification if delayed >5 days

---

## SCREEN 4: IT & Systems Access Setup

### Purpose & User Context
Ensures new hires have all necessary system access on day 1, from email and laptop to department-specific tools. This prevents delays, security gaps, and improves the new hire experience by reducing "waiting for access" friction.

**Primary Users:**
- IT Administrators (provisioning accounts, managing requests)
- HR Managers (requesting access for new hires)
- New Hires (confirming access received)

**Secondary Users:**
- Managers (ensuring team member has what they need)
- Security Teams (approving sensitive access)

### Key User Workflows

#### Workflow A: IT Admin Access Provisioning
1. IT admin sees dashboard of "New Hires Pending Access" (from HR)
2. Access request shows: employee name, role, department, start date
3. Pre-populated access list based on role template (eng vs. sales vs. support)
4. IT can add/remove/modify access as needed
5. For sensitive systems (database, admin, etc.): routes to manager/security for approval
6. Once approved, IT provisions access:
   - Creates email account
   - Orders/provisions laptop
   - Sets up cloud tool licenses
   - Adds to Slack channels, etc.
7. System tracks completion status
8. Sends new hire confirmation once ready

#### Workflow B: HR Access Request
1. HR adds new hire to system
2. HR fills out basic info (name, role, department, manager, start date)
3. System auto-suggests access package based on role
4. HR reviews, can customize (add/remove access)
5. Confirms: sends request to IT with clear deadline (start date)
6. Receives regular updates on provisioning status
7. If blocked/delayed: HR escalates to IT

#### Workflow C: New Hire Self-Service Verification
1. New hire logs into system (email already provisioned)
2. "System Access" card shows: "You should have access to:" [list]
3. Each item shows status: ✓ Ready, ⊙ Being Set Up, ⊘ Not Received
4. New hire can click items to test/confirm access
5. If something's missing: 1-click "Report Missing Access"
6. IT gets alert to troubleshoot

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  SYSTEM ACCESS SETUP                                   [Help]     │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Access Provisioning for New Hires                               │
│  [IT View] [HR Request View] [New Hire Status View]              │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│  NEW HIRES AWAITING ACCESS (7 pending)                           │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  [Filter by: All] [Dept: All] [Start Date Range] [Search]        │
│                                                                   │
│  Name            | Role            | Department | Start Date | Status │
│  ─────────────────────────────────────────────────────────────   │
│  Alex Chen       | Software Eng.   | Engineering| Jan 15    | 80%    │
│  [expand]        |                 |            |           |        │
│    Email: ✓ Created              |                                │
│    Laptop: ⊙ In Order (arrives Jan 14)                           │
│    GitHub: ⊙ Account Pending IT Setup                            │
│    Slack: ○ Not Started                                          │
│    VPN: ⊙ Waiting for Security Approval [review]                │
│    Database: ⊘ Pending Manager Approval [manager: need response] │
│                                                                   │
│  Sarah Johnson   | Sales Rep       | Sales      | Jan 16    | 50%    │
│  [expand]        |                 |            |           |        │
│                                                                   │
│  [+ New Access Request] [Bulk Import from HR]                    │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

**For HR/Admin Adding New Access Request:**

```
┌─────────────────────────────────────────────────────────────────┐
│  REQUEST SYSTEM ACCESS FOR NEW HIRE                              │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Step 1 of 3: Employee Information                               │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Employee Name *            [________________________]            │
│  Role *                     [________________________]            │
│  Department *               [Sales ▼]                            │
│  Manager *                  [Start Typing...] (auto-complete)    │
│  Start Date *               [________] (date picker)             │
│  Location *                 [New York ▼]                         │
│                                                                   │
│  [Next: Choose Access]      [Cancel]                             │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  Step 2 of 3: Choose Access Requirements                         │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Role Template: Sales Representative (recommended for your role) │
│  ✓ Google Workspace (Email, Drive, Docs)                        │
│  ✓ Slack - #sales, #general                                     │
│  ✓ Salesforce - Standard User License                           │
│  ✓ Office Equipment - Laptop (MacBook), Monitor, Keyboard       │
│  □ Analytics Tools (Tableau) - optional for this role           │
│  ○ VPN Access - requires manager approval                        │
│  ○ Admin Console - requires security review                     │
│                                                                   │
│  [Customize Template] [Previous] [Review & Submit]               │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  Step 3 of 3: Review & Submit                                    │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Employee: Alex Chen (Software Engineer, Engineering)            │
│  Start Date: January 15, 2024                                    │
│                                                                   │
│  Access Summary:                                                  │
│  1. Email & Google Workspace      [auto-provisioned by IT]      │
│  2. GitHub (Engineering template) [requires IT setup]           │
│  3. VPN Access                    [pending manager approval]    │
│  4. Office Equipment              [laptop order needed]         │
│  5. Slack - #engineering, #general [auto-provisioned by IT]    │
│                                                                   │
│  Approval routing:                                                │
│  → Manager approval for: VPN Access                              │
│  → IT provisioning: All system access + equipment               │
│  → Security review: VPN, database access                        │
│                                                                   │
│  [Submit Request] [Back: Edit] [Cancel]                          │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Access Request List (IT Dashboard)
**For Each New Hire:**
- Name and role
- Department and start date
- Overall completion % (progress bar)
- Quick view of access items with status
- Expandable for full details

**Status Indicators:**
- ✓ Completed (green) - access provisioned
- ⊙ In Progress (yellow) - being set up, estimated completion date
- ○ Not Started (gray) - not yet actioned
- ⊘ Pending (orange) - waiting for approval (manager, security)
- ⚠ Blocked (red) - issue preventing provisioning
- ⛔ Denied (dark red) - manager/security rejected request

#### 2. Access Item Details
**Each Access Item Shows:**
- System/tool name (Email, Slack, GitHub, etc.)
- Access type (standard/custom)
- Current status with progress
- Assigned to (which IT person/team)
- Approval status (if applicable)
- Estimated completion date
- Action buttons: [Expedite], [Troubleshoot], [Reassign], [Mark Complete]

#### 3. Access Templates by Role
**Pre-built Access Packages:**
- Based on job role/department
- Engineering: GitHub, VPN, Database, Dev Tools
- Sales: Salesforce, HubSpot, LinkedIn Sales Navigator, etc.
- HR: HRIS, Benefits Admin, ADP/Workday, etc.
- Finance: Accounting Software, Report Access, etc.

**Template Customization:**
- Add/remove access items
- Set approval requirements per item
- Define access level (read-only, edit, admin)

#### 4. Approval Workflow Integration
**For Manager/Security Approval Items:**
- Manager gets notification: "New team member access needs your approval"
- Shows: Employee name, requested access, reason why approval needed
- Approve/Deny buttons with optional reason field
- Can request more info from IT if needed
- Escalation if not approved within 2 days

#### 5. Equipment Integration
**For Hardware Orders:**
- Links to Equipment Request screen
- Tracks: Laptop ordered, shipped, delivered
- Sends notification when equipment arrives
- Can block start date if critical equipment not arriving in time

#### 6. New Hire Self-Service Status
**New Hire Can See:**
- All access they should have by role
- Current status (ready, in progress, pending)
- Test access links (click to verify email, open Slack, etc.)
- Report missing access (gets IT ticket auto-created)
- FAQ links for common access questions

### AI-Powered Features

**Smart Role-Based Provisioning:**
- AI learns typical access patterns by role, department, location
- "Based on similar sales reps, you typically need: Salesforce, HubSpot, LinkedIn Sales Navigator"
- Can recommend additional access: "Engineering team members usually request VPN access - add it?"

**Bottleneck Detection:**
- AI flags slow approvals: "VPN access waiting 3+ days on manager approval"
- Escalates to manager's manager if no response within 2 days
- Suggests expedited paths: "This access is critical for day 1 - request security pre-approval"

**Proactive Ordering:**
- AI predicts equipment needs based on role: "Eng new hire - recommend ordering MacBook Pro to arrive by start date"
- Tracks delivery timelines: "Laptop ordered 5 days ago, arrives Jan 14 (1 day before start)"

**Access Validation:**
- Validates provisioning: "Email created and tested successfully"
- Auto-confirms when access is actually used (new hire logs into system)
- Alerts if access not used after 2 days: "GitHub account created but not accessed - verify setup"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Status Indicators**: Text + icons (not color alone)
  - ✓ (green) + "Completed"
  - ⊙ (yellow) + "In Progress"
  - ⚠ (red) + "Pending Approval"
- **Tables**: Proper header cells (`<th>`), clear row organization
- **Progress**: Text % + visual bar
- **Color Contrast**: 4.5:1 for text, 3:1 for graphical elements

#### Keyboard Navigation
- **Table Navigation**: Tab through rows, arrow keys within row details
- **Expand/Collapse**: Spacebar or Enter to expand access items
- **Form Fields**: Tab through steps (step 1 → 2 → 3), shift+tab to go back
- **Buttons**: [Next], [Submit], [Approve], all keyboard accessible
- **Focus Indicators**: Clear 2px border on focused items

#### Screen Reader Compatibility
- **Table Markup**: 
  - `<table role="grid">` for access table
  - Headers with `<th scope="col">` or `<th scope="row">`
  - Row headers: `<td role="rowheader">`
- **Status Announcements**:
  - `aria-label="Email: Completed"` on status icons
  - `role="status" aria-live="polite"` for real-time updates
- **Forms**:
  - `<fieldset>` and `<legend>` for form steps
  - `aria-required="true"` for required fields
  - `aria-describedby` for help text
- **Approval Items**: Clear structure
  - `<article role="region" aria-labelledby="approval_name">`

#### Focus Management
- **Form Page Load**: Focus on first required field
- **Step Submission**: Focus on next step heading
- **Approval Notifications**: Focus on approve/deny button area
- **Table**: First cell focused on page load, arrow keys to navigate
- **Modal Dialogs**: Focus trap within dialog, focus returns to trigger when closed

#### Error States & Validation
- **Form Validation**: Inline feedback as user enters
  - "✓ Valid start date" or "✗ Start date must be in future"
- **Required Fields**: Marked with asterisk AND aria-required="true"
- **Error Messages**: Specific and actionable
  - Not: "Error"
  - Instead: "Email format invalid - use name@company.com"
- **Form Summary**: Before submission, show all selections for review

#### Motion & Animation
- **Status Updates**: No spinning loaders
  - Instead: "Setting up Slack... (estimated 2 minutes)"
- **Expandable Items**: Instant expand/collapse or simple fade, no complex animations
- **Respect Preferences**: Honor `prefers-reduced-motion`

#### Touch Accessibility
- **Buttons**: All buttons 44x44px minimum
  - [Approve], [Deny], [Expedite], [Reassign]
- **Form Inputs**: Height 44px minimum, width sufficient for content
- **Table Rows**: Large clickable area for expansion (not just tiny icon)
- **Spacing**: 12px between interactive elements minimum

### Data Model & Inputs

**Access Request:**
- Request ID, new hire ID, date created, start date
- Role, department, location
- Manager ID (for approval chain)

**Access Item Template:**
- Template ID, name, role-based association
- System/tool name
- Access level (standard, custom)
- Approval required (yes/no, required approver)
- Auto-provisioning rules (if available)
- Estimated setup time

**Individual Access Item:**
- Item ID, request ID, template item ID
- System name, access level
- Status (not_started, in_progress, pending_approval, completed, blocked, denied)
- Assigned to (IT person), assigned date
- Approved by (person), approval date
- Completed date, notes

### Data Outputs & Integrations

**HR/Manager View:**
- All pending access requests with status
- Alerts for delayed requests
- Approval queue

**Integrations:**
- **Directory/LDAP**: Create user accounts
- **Slack API**: Create user, add to channels
- **GitHub**: Create organization account, add to teams
- **Google Workspace**: Create email, add to groups
- **Salesforce/Okta/Other SSO**: User provisioning
- **Equipment System**: Track laptop/monitor orders
- **Onboarding Workflow**: Mark access setup as complete

### Edge Cases & Error Handling

1. **New Hire Start Date Moved Up**
   - Access request deadline updated
   - AI alerts if timeline now impossible
   - Can expedite or reduce scope

2. **System Provisioning Fails**
   - Error caught and reported: "Email creation failed - IT investigating"
   - IT notified immediately with error details
   - New hire can manual workaround: send password reset link

3. **Access Over-provisioned**
   - Safeguard: request shows "This access exceeds normal for role - security review required"
   - Enforces principle of least privilege

4. **Employee Leaves Before Onboarding Complete**
   - Access requests automatically cancelled
   - Any provisioned access marked for immediate deprovisioning

### Inter-Screen Interactions

- **Linked from**: New Hire Checklist (task: "System access setup")
- **Linked to**: Equipment Request (for laptop orders)
- **Provides Data to**: Manager Onboarding Workflow, Training Plan (system logins needed)
- **Triggered by**: Background check completion (don't provision sensitive access if pending)

---

## SCREEN 5: Equipment & Supply Request

### Purpose & User Context
Ensures new hires receive physical equipment and office supplies on time, preventing day 1 friction (no laptop, no desk setup, etc.). This screen coordinates ordering, delivery, inventory, and confirmation.

**Primary Users:**
- HR Managers (submitting equipment requests for new hires)
- Procurement/Office Managers (fulfilling orders, tracking inventory)
- New Hires (confirming receipt)

**Secondary Users:**
- IT (integrating with equipment setup)
- Finance (tracking costs)

### Key User Workflows

#### Workflow A: HR Equipment Request
1. HR adds new hire to onboarding
2. Clicks "Equipment & Supplies"
3. Selects role-based template ("Software Engineer" → suggests MacBook, monitor, keyboard, etc.)
4. Customizes if needed (add items, change specs)
5. Sets delivery location and date (should arrive before start date)
6. Submits request
7. Receives tracking as items are ordered and shipped
8. Can modify/add items up to cutoff date (usually 5 days before start)

#### Workflow B: Procurement Fulfillment
1. Procurement receives requests dashboard
2. Sees all pending equipment orders with deadlines
3. Batches orders for efficiency
4. Tracks delivery dates for each item
5. Updates status as items ship
6. Coordinates with office manager for onsite setup
7. Marks as "ready for pickup" when items arrive

#### Workflow C: New Hire Equipment Confirmation
1. New hire gets notification: "Your equipment is arriving"
2. Can track package delivery
3. Upon arrival, confirms receipt: "I've received MacBook, monitor, keyboard"
4. Can report missing items: "Keyboard not in shipment - request replacement"

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  EQUIPMENT & OFFICE SUPPLIES                           [Help]     │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Request Equipment for New Hire                                   │
│  [HR Request View] [Procurement View] [New Hire Status View]     │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│  HR: NEW EQUIPMENT REQUEST                                        │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  New Hire Information:                                            │
│  Name: [_________________]    Role: [_________________]          │
│  Start Date: [_________]     Location: [New York ▼]              │
│                                                                   │
│  EQUIPMENT TEMPLATE (by role)                                    │
│  Select a template or customize below:                           │
│                                                                   │
│  [Engineering - Recommended for Software Engineer ▼]             │
│      └─ MacBook Pro 16", Monitor, Keyboard, Mouse, Stand,        │
│         USB Hub, Headphones, Desk, Office Chair                 │
│                                                                   │
│  EQUIPMENT SELECTION                                              │
│  ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  Item                        | Qty | Specs              | Status │
│  ───────────────────────────────────────────────────────────    │
│  ✓ MacBook Pro              | 1   | 16" M3 Max         | Avail. │
│  ✓ Monitor                  | 1   | LG 27" 4K          | Avail. │
│  ✓ Keyboard (Wireless)      | 1   | Logitech MX Keys   | Avail. │
│  ✓ Mouse                    | 1   | Logitech MX Master | Avail. │
│  ✓ Headphones               | 1   | Sony WH-1000XM4    | Avail. │
│  ✓ Desk                     | 1   | Standing Desk      | Avail. │
│  ✓ Office Chair             | 1   | Herman Miller       | Avail. │
│  ○ Monitor Stand            | 1   | Adjustable         | [Edit] │
│                                                                   │
│  [+ Add Custom Item] [Clear All] [Reset to Template]             │
│                                                                   │
│  DELIVERY DETAILS                                                │
│  ─────────────────────────────────────────────────────────────   │
│  Delivery Location: 450 Main St, NYC (Office)                    │
│  Preferred Delivery Date: January 15, 2024 (Start Date)          │
│  Special Instructions: [_________________________________]        │
│                                                                   │
│  COST SUMMARY                                                    │
│  ─────────────────────────────────────────────────────────────   │
│  Subtotal: $3,850.00                                             │
│  Est. Shipping: $125.00                                          │
│  **Total: $3,975.00**                                            │
│                                                                   │
│  Cost Center: [Engineering ▼]  Budget Status: ✓ Available        │
│                                                                   │
│  [Submit Request] [Save as Draft] [Cancel]                       │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

**Procurement View:**

```
┌─────────────────────────────────────────────────────────────────┐
│  EQUIPMENT FULFILLMENT DASHBOARD                                 │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  [Filter by: All Status] [Deliver by Date Range] [Department]   │
│                                                                   │
│  NEW HIRE            | START DATE | ITEMS | STATUS   | ACTIONS   │
│  ─────────────────────────────────────────────────────────────   │
│  Alex Chen          | Jan 15     | 8     | ⊙ 75%    | [View]    │
│    └─ MacBook: ✓ Ordered (Arrives Jan 14)                       │
│    └─ Monitor: ✓ Ordered (Arrives Jan 14)                       │
│    └─ Chair: ⊙ Backorder (Arrives Jan 20) [Expedite?]          │
│    └─ Desk: ✓ In Office Inventory (Set up ready)                │
│                                                                   │
│  Sarah Johnson      | Jan 16     | 6     | ○ 0%     | [View]    │
│                                                                   │
│  [+ Manual Order] [Bulk Import from HR] [Check Inventory]        │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Equipment Templates by Role
**Pre-built Packages Include:**
- Engineering: High-end laptop, 2 monitors, ergonomic setup, headphones
- Sales: Laptop, monitor, portable charger, travel bag
- Support: Laptop, monitor, headphones (for calls), additional storage
- Finance: Laptop, monitor, additional security (encrypted drive), etc.
- HR: Laptop, monitor, printers access

**Template Customization:**
- Add/remove items
- Change specs (laptop model, monitor size, etc.)
- Save custom template for future use

#### 2. Equipment Catalog
**For Each Item:**
- Name and description
- Specifications (size, color, model, etc.)
- Availability (in stock, backorder date)
- Quantity
- Estimated price
- Can search/filter: "16-inch MacBook" → shows available models with prices

#### 3. Order Status Tracking
**Procurement shows:**
- Items ordered ✓
- Shipping in progress ⊙
- Estimated arrival date
- Actual arrival date
- Delivery address confirmation
- Issues/backordered items with workarounds

#### 4. Cost Management
**Displays:**
- Item costs
- Shipping estimate
- Total cost
- Approval if over limit
- Cost center allocation
- Budget availability check

#### 5. Delivery & Setup
**Coordinates:**
- Delivery location (office, new hire home, etc.)
- Delivery date (should be before or on start date)
- Setup: On-site delivery & setup, or pick up from receiving
- Special instructions (white glove setup, hold for arrival, etc.)

### AI-Powered Features

**Smart Equipment Recommendations:**
- "Based on Software Engineer role in NYC office, typical package costs $3,500-$4,000"
- Learns from past orders by role/location: "Most engineers in this location request dual monitors"
- Suggests ergonomic items: "Consider adding monitor stand and keyboard tray for comfort"

**Availability Optimization:**
- Balances cost with delivery speed
- "MacBook Pro in stock (arrives Jan 14) vs Premium option (arrives Jan 20) - recommend in-stock option"
- Auto-suggests alternatives if item is backordered: "LG Monitor unavailable, Dell U2720Q available at same price with faster delivery"

**Inventory Tracking:**
- Predicts shortages: "Surge in laptop requests next month - recommend pre-ordering"
- Identifies obsolete items: "This monitor model EOL - switch to newer model at same cost?"

**Cost Optimization:**
- Batch orders for savings: "Combining orders for 3 new hires, saving $200 on shipping"
- Negotiates supplier timing: "Push delivery of 2 items to Jan 20 to avoid overnight shipping premium ($60 saved)"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Tables**: Proper semantic `<table>` with `<thead>`, `<tbody>`, header rows
- **Status Indicators**: Text + icons (✓, ⊙, ○)
- **Color**: Don't use color alone for status (use icons + text)
- **Font Size**: 16px+ for body text
- **Contrast**: 4.5:1 for text, 3:1 for graphical elements
- **Equipment Photos**: If showing product images, include alt-text: "alt='MacBook Pro 16-inch silver'"

#### Keyboard Navigation
- **Form Steps**: Tab through role selection → equipment items → delivery details → review
- **Equipment List**: Tab through items, spacebar to select, Enter to view details
- **Quantity**: Arrow keys to adjust quantity (or +/- buttons)
- **All Buttons**: Keyboard accessible ([Submit], [Add Item], [View Details])
- **Focus Indicators**: Clear 2px border on focused items

#### Screen Reader Compatibility
- **Form Structure**:
  - `<fieldset>` and `<legend>` for form sections
  - `<label for="start_date">Start Date</label>` for fields
  - `aria-required="true"` for required fields
- **Equipment Table**:
  - `<table role="grid">` 
  - Headers: `<th scope="col">Item</th>` or `<th scope="row">`
- **Status Announcements**:
  - `aria-label="MacBook: Ordered, arrives January 14"`
  - `role="status" aria-live="polite"` for order updates
- **Costs**: Announce as "$3,975.00" (not "$3975" which might read as thousands)

#### Focus Management
- **Form Load**: Focus on role selection
- **After Selection**: Focus moves to equipment list
- **Modal Details**: Focus trap within modal, focus returns to trigger
- **Cost Summary**: Focus on total when form is complete
- **Error States**: Focus moves to first field with error

#### Error States & Validation
- **Required Equipment**: Some items are required, others optional
  - Mark clearly: "MacBook *" (required) vs "Monitor Stand" (optional)
- **Delivery Date**: Must be before/on start date
  - "Delivery date cannot be after start date (Jan 15)"
- **Budget**: Show if over limit
  - "⚠️ Total exceeds allocated budget by $500. Request manager approval."
- **Backorder Items**: Clear messaging
  - "Chair: Backordered until Jan 20 (5 days after your start). OK to proceed?"

#### Motion & Animation
- **Item Selection**: No complex animations
  - Checkmark appears instantly or with simple fade
- **Cost Updates**: Instant or no animation (respect `prefers-reduced-motion`)
- **Progress**: Static or simple progress bar

#### Touch Accessibility
- **Buttons**: 44x44px minimum ([+ Add Item], [Submit], [View])
- **Quantity Controls**: +/- buttons are large (44px), not tiny
- **Checkboxes**: Large touch targets, at least 24x24px
- **Equipment List**: Long scrollable list with large row heights (48px+)

### Data Model & Inputs

**Equipment Item:**
- Item ID, name, category (laptop, monitor, peripherals, furniture)
- Specifications (model, size, color, etc.)
- Vendor, SKU
- Cost, lead time
- Availability status (in_stock, backorder_date, discontinued)

**Equipment Request:**
- Request ID, new hire ID, role, department
- Start date, delivery location
- Requested items (item ID, quantity, delivery date)
- Status (draft, submitted, ordered, shipping, delivered, completed)
- Total cost, cost center

**Delivery Tracking:**
- Shipment ID, request ID, vendor
- Tracking number
- Estimated arrival, actual arrival
- Delivery address, special instructions
- Signature confirmation

### Data Outputs & Integrations

**HR View:**
- Request status, delivery tracking
- Budget tracking

**Procurement View:**
- Orders to fulfill, vendor management, inventory
- Delivery coordination

**Finance:**
- Equipment costs by department, month, new hire cohort
- Budget consumption

**Integrations:**
- **Supplier APIs**: Order tracking, real-time inventory, shipping updates
- **Slack**: Notifications (new hire to confirm delivery, procurement updates on status)
- **Onboarding**: Equipment setup complete → unblock "ready for day 1"
- **Inventory System**: Track equipment in office for reuse

### Edge Cases & Error Handling

1. **Item Backordered**
   - Show: "Chair backordered until Jan 20 (5 days after your start)"
   - Options: Wait, substitute with similar item, or remove from order
   - Escalate if critical item delayed

2. **Delivery Address Unknown**
   - For remote hires: "Should we ship to your home address?"
   - Need to capture address before ordering

3. **Equipment Damaged in Transit**
   - New hire reports: "Monitor arrived broken"
   - Auto-create replacement order, expedite shipping
   - Arrange return of damaged item

4. **New Hire Start Date Moved**
   - Automatically adjust delivery date
   - If new delivery date is after start date, escalate
   - Can offer temporary equipment in office

5. **Budget Constraint**
   - Order exceeds allocated budget
   - Require manager approval
   - Or suggest cost-saving alternatives

### Inter-Screen Interactions

- **Linked from**: New Hire Checklist (task: "Equipment ordered")
- **Linked to**: IT Systems Access (coordinate laptop arrival with email setup)
- **Provides Data to**: Manager Onboarding (equipment setup affects day 1 readiness)
- **Triggered by**: New hire start date set (send procurement request)

---

## SCREEN 6: Orientation & Training Plan

### Purpose & User Context
Structures new hire learning during the first 30-90 days, covering company culture, role-specific training, tools, processes, and compliance requirements. A guided curriculum ensures consistency and tracks knowledge acquisition.

**Primary Users:**
- New Hires (completing training modules)
- HR Managers (creating/assigning training plans)
- Managers (monitoring team member progress, conducting role-specific training)

**Secondary Users:**
- L&D Team (maintaining training content)
- Compliance (ensuring mandatory trainings completed)

### Key User Workflows

#### Workflow A: New Hire Self-Service Training
1. New hire logs in, sees "Learning Path" on onboarding dashboard
2. Day 1 orientation module: company tour video, culture intro, meet the team video
3. Week 1 modules: roles & responsibilities, tools intro (Slack, email, calendar), key processes
4. Completes quizzes to verify learning
5. Manager check-in: "How was your first week? Questions about role?"
6. Week 2-4: Role-specific training (engineering gets tech stack, sales gets CRM training, etc.)
7. Month 1: Mid-check-in assessment
8. Month 2-3: Advanced training, projects, mentorship
9. Day 90: Full assessment and onboarding sign-off

#### Workflow B: HR Training Plan Management
1. HR creates training template by role
2. Assigns modules (company orientation, role training, mandatory compliance)
3. Sets timeline (days 1, week 1, week 2-4, month 2-3)
4. Includes videos, documents, quizzes, live sessions
5. Can customize per employee if needed
6. Monitors completion rates
7. Sends reminders for overdue training
8. Generates completion certificates

#### Workflow C: Manager Support
1. Manager sees "new team member training" card on their dashboard
2. Views what training their new hire is assigned
3. Can conduct 1-on-1 role-specific training sessions
4. Logs training sessions completed
5. Provides feedback in check-ins
6. Accelerates or extends training as needed based on progress

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  ONBOARDING TRAINING & ORIENTATION                    [Help]     │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Your Learning Path: Welcome to [Company]!                       │
│  Progress: [████████░░░░░░░] 40% Complete (14 of 35 modules)    │
│  Estimated Completion: [Date]                                    │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│  PHASE 1: FIRST DAY (Day 1)                                       │
│  Status: In Progress (1 of 3 complete)                           │
│  ─────────────────────────────────────────────────────────────   │
│  ✓ Welcome to [Company] Video                   Completed Today  │
│    Duration: 15 min  |  [Watch Again]                           │
│                                                                   │
│  ⊙ Culture & Values Orientation                  In Progress     │
│    Duration: 25 min  |  [Resume Learning]                       │
│    Your progress: Watched 12 min of 25 min                      │
│    [Continue Watching]                                           │
│                                                                   │
│  ○ Onboarding Kickoff Meeting                    Scheduled       │
│    Scheduled for: Today at 2:00 PM with Your Manager            │
│    [Join Video Call] [Reschedule]                               │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  PHASE 2: FIRST WEEK (Jan 15 - Jan 19)                          │
│  Status: Not Started (0 of 4 complete)           Due: Jan 19    │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Slack & Internal Tools Walkthrough            Not Started     │
│    Duration: 30 min  |  [Start Learning]                        │
│    Trainer: Mike Chen, IT Team Lead                             │
│                                                                   │
│  ○ Product Deep Dive                             Not Started     │
│    Duration: 45 min video + 20 min quiz         [Start]         │
│                                                                   │
│  ○ Peer Meet & Greets (4 sessions)              Not Started     │
│    Duration: 30 min each, scheduled with peers   [Schedule]     │
│                                                                   │
│  ○ Engineering Tech Stack (YOUR ROLE)            Not Started     │
│    Duration: 60 min video + Repo Setup Exercise  [Start]        │
│    Trainer: Lead Engineering Team                               │
│                                                                   │
│ ─────────────────────────────────────────────────────────────   │
│                                                                   │
│  PHASE 3: MONTH 1 DEEP DIVE (Jan 22 - Feb 16)   [Expand]       │
│                                                                   │
│  [Optional Resources] [Download Handbook] [Ask Questions] [Help] │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Learning Path Overview
**Shows:**
- Overall progress % (visual bar + count of modules)
- Estimated completion date
- Phase-based organization (Day 1, Week 1, Month 1, Month 2-3)
- Each phase shows completion status

#### 2. Modules by Phase
**Each Module Includes:**
- Status (not started, in progress, completed, overdue)
- Title and duration
- Module type icon (video, quiz, meeting, assignment, reading)
- Action button ([Start Learning], [Resume], [Complete], [Reschedule], etc.)
- Optional: Trainer/facilitator name with message/contact link

**Module Types:**
- **Video Modules**: Watch video, includes progress bar, captions, transcripts
- **Interactive Training**: Guided walkthroughs, simulations
- **Quizzes**: Knowledge checks, must pass to advance
- **Scheduled Sessions**: Live meetings with trainer or peers
- **Assignments**: Hands-on exercises, code repos, setup tasks
- **Readings**: Documents, wikis, handbooks

#### 3. Video Player (for video modules)
**Features:**
- Progress slider (can scrub)
- Full screen option
- Speed control (0.75x to 2x)
- Closed captions toggle
- Transcript view (search within transcript)
- Download option (for offline viewing)
- Bookmarks/notes feature
- Recommended next modules

#### 4. Quiz & Knowledge Check
**Features:**
- Multiple choice, true/false, matching questions
- Immediate feedback ("Correct!" or "Incorrect, here's why...")
- Retakes allowed (with different question sets)
- Pass/fail threshold (usually 80%)
- Certificate on completion
- Links to related learning if failed

#### 5. Scheduled Sessions
**Shows:**
- Date, time, duration
- Facilitator/trainer name and avatar
- Video meeting link (Zoom, Teams, etc.)
- Notes/agenda
- [Join Meeting] button
- Ability to reschedule
- Post-session recording available

#### 6. Assignments & Hands-On Tasks
**For Role-Specific Training:**
- Clear instructions and acceptance criteria
- Links to resources (repos, documentation)
- File upload for submission
- Trainer feedback
- Mark complete when approved

#### 7. Manager Check-In Integration
**Scheduled Milestones:**
- Day 1 check-in: How's your first day?
- Week 1: Any blockers from training?
- Week 4: How are you progressing in your role?
- Month 1: Review progress, adjust training if needed
- Month 3: Final onboarding assessment

**Check-in Form Includes:**
- New hire feedback (comfort level, blockers, questions)
- Training progress review
- Role-specific assessment (can do core tasks?)
- Manager feedback
- Next steps

### AI-Powered Features

**Personalized Learning Paths:**
- AI customizes curriculum based on:
  - Role-specific skills gaps
  - Prior experience (if engineer, skip basic coding topics)
  - Learning pace (adjust module order/difficulty)
- "Based on your background, we're skipping Intro to Git and starting with advanced workflows"

**Adaptive Pacing:**
- Tracks engagement (video completion times, quiz scores)
- Slows down or speeds up training based on comprehension
- "You're mastering these concepts quickly - advance to Week 2 content"

**Progress Predictions:**
- AI forecasts learning success: "On track to master role requirements by Day 60"
- Flags at-risk new hires: "Quiz score low (60%) - recommend manager 1-on-1 on this topic"

**Content Recommendations:**
- Suggests supplementary learning: "Struggling with SQL? Here's a 10-min refresher video"
- Recommends peer mentors: "Experienced engineer John has time for pairing sessions"

**Engagement Nudges:**
- Smart reminders (not spam): "You're on pace! Just 2 more modules this week"
- "Your team is waiting for you to complete Product training - scheduled a catch-up?"

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Progress Indicators**: Text % + visual bar, not bar alone
- **Module Icons**: Icon + text label (video, quiz, meeting, assignment)
- **Video Player**: Clear controls with proper contrast
- **Captions**: All videos must have captions (at least 99% accuracy)
- **Transcripts**: Full transcript for all videos, searchable
- **Color**: Status colors paired with text or icons (not color alone)
- **Font Size**: 16px+ for body text, 18px+ for headings

#### Keyboard Navigation
- **Module List**: Tab through modules, Enter to open, Spacebar to expand
- **Video Player**: All controls keyboard accessible (play, pause, volume, captions, full screen)
  - k = play/pause
  - f = full screen
  - c = captions
  - j = -10 seconds, l = +10 seconds
- **Quizzes**: Tab through questions, spacebar to select radio/checkbox, Enter to submit
- **Meeting Links**: Keyboard accessible ([Join Meeting] button)
- **Focus Indicators**: Clear 2px border on focused items

#### Screen Reader Compatibility
- **Module List**:
  - `<ol>` for ordered list of modules
  - Each: `<li role="article">` with status aria-label
  - `<button aria-label="Start Learning: Welcome to Company video, 15 minutes">`
- **Progress**: `aria-valuenow="40" aria-valuemin="0" aria-valuemax="100" aria-label="Overall Progress: 40%"`
- **Video Player**:
  - `<video>` semantic element with captions track
  - `<track kind="captions" src="..." label="English">`
  - Current time announced: "Playing 3:45 of 15:00"
- **Quiz**:
  - Questions in `<fieldset>` with `<legend>`
  - Radio buttons properly labeled
  - Error announcements: "Question 2 is required to submit"
- **Captions**: Burned-in or externally provided (CC format or WebVTT)

#### Focus Management
- **Page Load**: Focus on first module or first incomplete module
- **Video Completion**: Focus on "Next Module" or continue button when video ends
- **Quiz Submission**: Focus on results/feedback area
- **Meeting Join**: Focus on meeting link, Enter/click to open
- **Error in Quiz**: Focus on first unanswered question with error message

#### Error States & Validation
- **Incomplete Quiz**: Clear message listing unanswered questions
  - "Questions 2 and 5 are required"
  - Keyboard accessible: navigate to unanswered questions
- **Video Player**: Error states (video unavailable, network issues)
  - "Video unavailable. Try again later or contact support."
- **Scheduled Session Rescheduling**: Confirm action
  - "Are you sure you want to reschedule this meeting?"

#### Motion & Animation
- **Captions**: Static, no animated captions
- **Progress Bar**: No animation (instant or simple fade)
- **Module Transitions**: Instant or simple page reload (honor `prefers-reduced-motion`)
- **Video Playback**: Respect playback speed preferences

#### Touch Accessibility
- **Video Controls**: Large touch targets (44x44px) for play, pause, CC button
- **Module List**: Large rows (48px+ height) for easy touch
- **Quiz Radio Buttons**: 44x44px minimum (not tiny)
- **Meeting Join Button**: 44x44px minimum button
- **Spacing**: 12px between interactive elements

### Data Model & Inputs

**Training Template:**
- Template ID, role, department
- Modules (ordered list)
- Phase structure (day 1, week 1, etc.)
- Manager check-in schedule

**Module:**
- Module ID, title, type (video, quiz, assignment, meeting)
- Duration, difficulty level
- Content (video URL, quiz questions, docs, etc.)
- Prerequisites (must complete X before this)
- Passing criteria (quiz score threshold)
- Trainer/facilitator info

**Learner Progress:**
- Progress ID, new hire ID, module ID
- Status (not_started, in_progress, completed)
- Start date, completion date
- Score (for quizzes)
- Time spent
- Notes from trainer

### Data Outputs & Integrations

**HR Dashboard:**
- All new hires' training progress
- Completion rates by role
- Slow learners (early intervention)
- Modules with low scores (content quality issues)

**Manager View:**
- New team member's training schedule
- Completion status
- Check-in prompts

**Integrations:**
- **Video Platform** (Vimeo, Wistia, YouTube): Video hosting & analytics
- **Learning Management System** (Docebo, Cornerstone): Training content management
- **Slack**: Notifications (new module, check-in reminder, completion milestone)
- **Calendar**: Meeting integrations, automated scheduler
- **Certificate System**: Auto-generate completion certificates

### Edge Cases & Error Handling

1. **New Hire Behind on Training**
   - Manager and HR notified at day 3 of falling behind
   - AI suggests accelerated path or extended timeline
   - Can extend start date if critical training incomplete

2. **Failed Quiz (below passing score)**
   - Provide resources: "Here's a 10-min refresher video"
   - Allow unlimited retakes with different questions
   - After 3rd fail, flag for manager support

3. **Scheduled Meeting Cancellation**
   - Auto-reschedule with facilitator
   - Notify new hire of new time
   - Recording provided if they can't attend

4. **Video Unavailable (tech issues)**
   - Fallback to transcript
   - Alternative: Download PDF or attend live walkthrough
   - Auto-escalate to L&D if not resolved

5. **New Hire Leaves Before Completion**
   - Archive their training record
   - Cessation of module reminders
   - Final record for offboarding

### Inter-Screen Interactions

- **Linked from**: New Hire Checklist (task: "Complete Onboarding Training")
- **Manager Check-in**: Links to Manager Onboarding Workflow
- **Learning Path**: Connects to full Learning & Development module
- **Triggers**: Completion certificate, training badges

---

## SCREEN 7: Manager Onboarding Workflow

### Purpose & User Context
Equips managers with structure, templates, and reminders to effectively onboard their new team members. This ensures consistent management practices, team integration, and successful ramp-up for both the new hire and the team.

**Primary Users:**
- Managers (conducting onboarding for direct reports)

**Secondary Users:**
- HR (monitoring manager completion, supporting onboarding)
- New Hires (can see what manager is planning)

### Key User Workflows

#### Workflow A: Manager Day 1 Preparation
1. Manager receives notification: "Alex Chen starts Monday"
2. Manager views onboarding dashboard: What to do on day 1?
3. Pre-boarding to-do list:
   - Prepare workspace (desk, chair, welcome package)
   - Send intro email to team
   - Prep for first 1-on-1
4. Manager completes pre-boarding checklist
5. Marks tasks done as he completes them

#### Workflow B: Day 1 & Week 1 Onboarding
1. Manager conducts day 1 activities:
   - Office tour
   - Meet the team
   - First 1-on-1 meeting (uses template for talking points)
2. Manager logs meeting notes
3. Manager schedules week 1 check-ins with peers
4. Sends action items to new hire (onboarding training, goals, etc.)

#### Workflow C: Month 1-3 Check-ins
1. Manager has scheduled check-ins: day 7, day 30, day 60, day 90
2. Each check-in includes:
   - Conversation starter guide (questions about progress, blockers)
   - Role-specific assessment (can do X task yet?)
   - Feedback (how's culture fit, communication, pace?)
   - Goals/expectation setting
3. Manager logs notes and outcomes
4. HR gets visibility (progress alerts if issues)

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  MANAGER ONBOARDING WORKFLOW                          [Help]     │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  New Team Member: Alex Chen (Software Engineer)                  │
│  Start Date: January 15, 2024 (2 days away)                      │
│  Manager: You (Sarah Kim)                                        │
│                                                                   │
│  PRE-BOARDING (Due: January 12)                                  │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Workspace Setup                                               │
│    └─ Desk & Equipment Ready     [✓ Mark Complete]              │
│    └─ Welcome Package Prepared   [View Checklist]                │
│    └─ Introduce to Team (Email) [Draft Email]                   │
│    └─ Peer Mentors Assigned      [Assign Mentor]                │
│                                                                   │
│  ○ First 1-on-1 Meeting Preparation                             │
│    └─ Schedule Meeting           [Schedule: Jan 15 2PM]          │
│    └─ Review New Hire Profile    [View Profile]                 │
│    └─ Prepare Talking Points     [Open Template]                │
│                                                                   │
│  DAY 1 (January 15)                                              │
│  ─────────────────────────────────────────────────────────────   │
│  ⊙ Welcome & Office Tour                                        │
│    [Completed at 10:30 AM]                                       │
│    Notes: [___________________________________] [Save]          │
│                                                                   │
│  ⊙ Team Introductions                                           │
│    Attended: Alex, Mike (peer), Sarah, James                    │
│    [Add Notes] [Mark Complete]                                  │
│                                                                   │
│  ○ Lunch with Team                                              │
│    Scheduled: 12:00 PM - [View Attendees]                       │
│                                                                   │
│  ○ First 1-on-1                                                │
│    Scheduled: 2:00 PM - [Join Meeting]                          │
│    [1-on-1 Talking Points Template]                             │
│                                                                   │
│  WEEK 1 CHECK-IN (January 19, 2:00 PM)                          │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Schedule Meeting [Schedule 1:1]                              │
│  ○ Prepare Questions [View Check-in Guide]                      │
│  ○ Log Feedback [Open Form]                                     │
│                                                                   │
│  MONTH 1 & BEYOND (View Calendar)                                │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Day 30 Check-in Scheduled: February 14                       │
│  ○ Day 60 Check-in Scheduled: February 26                       │
│  ○ Day 90 Assessment: March 16                                  │
│                                                                   │
│  [Support & FAQ] [Contact HR] [View New Hire's Progress]        │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

**1-on-1 Meeting Template:**

```
┌─────────────────────────────────────────────────────────────────┐
│  1-ON-1 MEETING: Alex Chen (Day 1)                              │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  BEFORE THE MEETING                                              │
│  ─────────────────────────────────────────────────────────────   │
│  Prepare: 5 min                                                  │
│  □ Review new hire's background and goals                        │
│  □ Have calendar open (for scheduling next check-ins)            │
│  □ Have department info ready (team structure, key contacts)     │
│                                                                   │
│  WELCOME & SETTLING IN (5 min)                                   │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Welcome warmly, thank them for joining                        │
│  ○ Ask how their first hours have been ("How's your day going?") │
│  ○ Make sure they're comfortable, have what they need            │
│                                                                   │
│  ROLE & EXPECTATIONS (10 min)                                    │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Explain their core responsibilities and success metrics       │
│  ○ Clarify: "In the first month, we expect you to..."           │
│    Example: "Learn the codebase, set up dev environment,        │
│    ship your first small PR"                                     │
│  ○ Ask: "What's your understanding of the role?"                 │
│  ○ Address any questions                                         │
│                                                                   │
│  TEAM & RELATIONSHIPS (5 min)                                    │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Introduce key team members and stakeholders                   │
│  ○ Explain team structure and how you work together              │
│  ○ Share upcoming team events/meetings                           │
│                                                                   │
│  NEXT STEPS (5 min)                                              │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Outline this week's schedule                                  │
│  ○ Share onboarding training (they'll see full schedule)         │
│  ○ Schedule check-ins: Week 1 (day 7), Month 1 (day 30)         │
│  ○ Open door policy: "My calendar is [link], reach out anytime"  │
│                                                                   │
│  MEETING NOTES                                                    │
│  ─────────────────────────────────────────────────────────────   │
│  Notes from meeting:                                             │
│  [_________________________________________]                    │
│                                                                   │
│  Key Takeaways:                                                  │
│  □ New hire understands core role  □ Yes  □ Somewhat  □ No      │
│  □ New hire has questions answered □ Yes  □ No                 │
│  □ Check-ins scheduled for month?  □ Yes  □ No                 │
│                                                                   │
│  [Save Notes] [Schedule Next Check-in] [Send Summary Email]      │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Manager Onboarding Dashboard
**Shows:**
- New hire name, role, start date, countdown timer
- Pre-boarding checklist (before day 1)
- Day 1 activities
- Week 1 & beyond check-in schedule
- Quick action buttons

#### 2. Pre-Boarding Checklist
**Manager Tasks:**
- Prepare workspace (desk setup, welcome materials)
- Send intro email to team
- Assign peer mentor/buddy
- Prepare first 1-on-1 talking points
- Ensure equipment ordered (coordination with IT/procurement)

#### 3. Meeting Templates
**Pre-built Conversation Guides for:**
- First 1-on-1 (day 1)
- Week 1 check-in
- Month 1 assessment
- Month 3 assessment

**Each Template Includes:**
- Conversation flow/talking points
- Questions to ask new hire
- Topics to cover (role expectations, team, blockers, feedback)
- Space for notes
- Time estimates (meeting duration)
- Prompts for scheduling next check-in

#### 4. Check-in Scheduling
**Features:**
- Calendar integration (sync with manager & new hire calendars)
- Suggested times based on availability
- Video call link generation
- Automatic reminders to both parties
- Pre-meeting prep checklists

#### 5. Feedback Logging
**After Each Check-in:**
- Form to capture meeting outcomes
- New hire progress assessment (on track, ahead, behind)
- Role-specific competency checks ("Can do X task?")
- Manager observations (communication, engagement, culture fit)
- Any blockers or support needed
- Goals for next period

#### 6. Integration with New Hire Progress
**Manager Can See:**
- New hire's training progress (which modules complete)
- Onboarding checklist status (HR side)
- Documents completed (I-9, etc.)
- Equipment status
- If new hire has blockers or questions

### AI-Powered Features

**Smart Conversation Prompts:**
- AI generates personalized talking points based on new hire's background
- "Alex has 5 years of Java experience - discuss if we should have them mentor junior engineers"
- Suggests discussion topics based on typical first-week blockers

**Progress Alerts:**
- Flags if new hire is falling behind: "Alex hasn't completed Week 1 training by Thursday"
- Suggests manager intervention: "Schedule 1-on-1 to see if there are blockers"

**Peer Matching:**
- Recommends best peer mentor/buddy based on role, experience, personality
- "John would be great - he joined 6 months ago in similar role"

**Meeting Optimization:**
- Suggests optimal check-in timing (not too frequent, not too sparse)
- Reminds manager of upcoming check-in 24 hours before
- Flags if manager missed scheduled check-in

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Checklists**: Checkboxes with clear labels (text, not icon alone)
- **Templates**: Clear structure with headings and sections
- **Dates/Times**: Human-readable format (not just ISO 8601)
- **Progress**: Visual + text indicator (not bar alone)
- **Color Contrast**: 4.5:1 for text, 3:1 for graphical elements
- **Font Size**: 16px+ for body text

#### Keyboard Navigation
- **Checklist**: Tab through items, spacebar to toggle checkbox
- **Templates**: Tab through sections, Enter to view or edit
- **Buttons**: All buttons keyboard accessible ([Schedule Meeting], [Save Notes], [View Profile])
- **Links**: Calendar links, profile links all keyboard accessible
- **Focus Indicators**: Clear 2px border on focused items

#### Screen Reader Compatibility
- **Checklists**:
  - `<fieldset>` with `<legend>` for checklist sections
  - Checkboxes: `<input type="checkbox" aria-label="Workspace Setup: Desk and Equipment Ready">`
- **Templates**:
  - `<section>` elements with clear headings
  - Form fields: `<label for="manager_notes">Notes from Meeting</label>`
- **Dates**: `<time datetime="2024-01-15">January 15, 2024</time>`
- **Status**: `role="status" aria-live="polite"` for updates
  - "Check-in scheduled for January 19 at 2:00 PM"

#### Focus Management
- **Page Load**: Focus on new hire name/intro section
- **Expanded Sections**: Focus moves to first item in section
- **Saved Content**: Focus on success message or next action
- **Modal Templates**: Focus trap in template, focus returns when closed

#### Error States & Validation
- **Missing Tasks**: Clear alert
  - "⚠️ First 1-on-1 not scheduled. Schedule by end of day."
- **Meeting Scheduling**: Confirm action
  - "Schedule meeting for January 19, 2:00 PM with Alex Chen?"
- **Form Submission**: Required fields marked
  - "Meeting Notes *" + aria-required="true"

#### Motion & Animation
- **Template Expansion**: Instant or simple fade (honor `prefers-reduced-motion`)
- **Checklist Completion**: Checkmark appears instantly
- **Notifications**: No flashing or distracting animations

#### Touch Accessibility
- **Checkboxes**: 44x44px minimum touch targets
- **Buttons**: 44x44px minimum ([Schedule], [Save], [View])
- **Template Sections**: Large expandable areas (48px+ height)
- **Spacing**: 12px between interactive elements

### Data Model & Inputs

**Manager Onboarding Task:**
- Task ID, type (checklist item, meeting template, feedback form)
- Due date, priority
- Completed date, notes
- Assigned manager

**Meeting/Check-in:**
- Check-in ID, new hire ID, manager ID
- Date/time, meeting type (day 1, week 1, month 1, month 3)
- Status (scheduled, completed, missed, rescheduled)
- Notes from meeting
- Feedback/assessment

### Data Outputs & Integrations

**HR Dashboard:**
- Manager completion rates (are managers doing onboarding?)
- Check-in status (are check-ins happening on schedule?)
- New hire feedback (manager perception of progress)

**New Hire View:**
- Can see what manager has planned
- Check-in meeting invites and links

**Integrations:**
- **Calendar API**: Schedule & sync meetings (Google Cal, Outlook, etc.)
- **Slack**: Notifications to manager & new hire for check-ins
- **Onboarding Dashboard**: Visibility into new hire's progress across all onboarding streams
- **Email**: Send meeting invites, templates, reminders

### Edge Cases & Error Handling

1. **Manager Misses Scheduled Check-in**
   - System escalates to HR: "Manager missed week 1 check-in"
   - Suggests rescheduling or manager discussion
   - Can assign backup person to cover

2. **New Hire Cancelled Meeting**
   - Manager can reschedule, mark as "new hire initiated cancellation"
   - Optional: capture reason (sick, urgent work, etc.)

3. **Feedback Indicates Struggling New Hire**
   - HR gets alerted: "New hire behind on training, manager notes issues"
   - Recommended interventions appear (pair programming, extended training, etc.)

4. **Manager doesn't provide notes**
   - Optional fields, but reminders if all check-ins are note-free
   - HR may follow up with manager directly

### Inter-Screen Interactions

- **Linked from**: New Hire Checklist
- **Linked to**: Training Plan (view new hire's progress), Meeting scheduling (Calendar)
- **Provides visibility to**: HR Dashboard (manager compliance)
- **Receives input from**: New Hire's training/checklist completion

---

## SCREEN 8: Offboarding Checklist

### Purpose & User Context
Manages the employee exit process systematically, from final paycheck and benefits information through asset returns, access revocation, knowledge transfer, and exit interviews. Ensures legal compliance, security, and preserves institutional knowledge.

**Primary Users:**
- HR Managers (initiating offboarding, collecting documents)
- Managers (coordinating final projects, knowledge transfer)
- IT Administrators (revoking access, data backup)
- Finance (final payroll, expense reimbursement)

**Secondary Users:**
- Departing Employees (completing exit process, optional alumni network)
- Finance (COBRA info, final compensation)

### Key User Workflows

#### Workflow A: Offboarding Initiation (by HR)
1. HR gets notice of resignation/termination
2. HR adds employee to offboarding system
3. System generates offboarding checklist based on role/tenure/dept
4. Assigns tasks to various departments (IT, Finance, Legal, Manager)
5. Sets offboarding timeline (usually 2 weeks, can be longer)
6. Notifies all stakeholders: "John is leaving on [Date]"
7. Receives regular progress updates
8. Coordinates final exit interview

#### Workflow B: Manager Coordination
1. Manager gets notification of team member departure
2. Manager views offboarding checklist:
   - Knowledge transfer tasks
   - Project handoff responsibilities
   - Team coverage planning
3. Manager schedules knowledge transfer sessions
4. Documents critical processes/contacts the employee knows
5. Marks tasks complete as they happen

#### Workflow C: IT & Access Revocation
1. IT gets offboarding request on day 1 of offboarding period
2. IT schedules access revocation for last day
3. Revokes email, Slack, GitHub, database access on final day
4. Backs up email, docs, repos per policy
5. Collects hardware (laptop, monitor, badge, etc.)
6. Verifies all access removed

#### Workflow D: Departing Employee Final Steps
1. Employee completes offboarding forms (update address for mail, W4, etc.)
2. Downloads COBRA information
3. Completes exit interview (optional)
4. Collects final paycheck confirmation
5. Signs separation agreement
6. Transfers knowledge as needed
7. Returns equipment
8. Optional: joins alumni network

### Screen Layout & Structure

```
┌─────────────────────────────────────────────────────────────────┐
│  EMPLOYEE OFFBOARDING                                  [Help]     │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Offboarding for: John Smith (Senior Engineer)                   │
│  Last Day: January 31, 2024 (8 days remaining)                   │
│  Reason: Resignation                                             │
│  Manager: Sarah Chen                                             │
│                                                                   │
│  Overall Progress: [██████░░░░░░░░░░░] 35% Complete             │
│  Status: In Progress                                             │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  FINAL COMPENSATION & ADMIN                                      │
│  ─────────────────────────────────────────────────────────────   │
│  ✓ Final Paycheck Calculated      Due: January 31                │
│    Amount: $[X] (includes PTO payout)                            │
│    [View Pay Stub]                                               │
│                                                                   │
│  ✓ Benefits Termination Processed Date: Jan 31                   │
│    COBRA Info Sent: Jan 24                                       │
│    [View COBRA Details]                                          │
│                                                                   │
│  ○ Final Expense Reimbursements    Due: January 28               │
│    Pending: $450 in receipts awaiting approval                   │
│    [Submit Expenses] [Approve All]                               │
│                                                                   │
│  ○ Tax Documents (W2)              Due: Feb 1                    │
│    Status: Will be available Jan 31 or later                     │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  KNOWLEDGE TRANSFER                                               │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Hand off Current Projects                                     │
│    Assigned to: Manager (Sarah)                                  │
│    Due: January 29                                               │
│    [View Instructions] [Mark Complete]                           │
│                                                                   │
│  ○ Document Critical Processes                                   │
│    Assigned to: John Smith                                       │
│    Due: January 30                                               │
│    [Start Documentation] [Template]                              │
│                                                                   │
│  ○ Knowledge Transfer Sessions (3 scheduled)                     │
│    Session 1: Jan 25, 2:00 PM - Database Architecture           │
│    Session 2: Jan 27, 10:00 AM - Deployment Process             │
│    Session 3: Jan 29, 2:00 PM - Team Protocols                  │
│    [View Schedule] [Add Session] [Meeting Links]                 │
│                                                                   │
│  ○ Key Contacts & Relationships Documented                       │
│    Due: Jan 30                                                   │
│    [Open Contact Map]                                            │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  ASSET RETURN & ACCESS REVOCATION                                │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Return Equipment                                              │
│    Items to return: Laptop, Monitor, Badge, Headphones           │
│    [View Checklist] [Confirm Receipt]                            │
│    Return Location: Office Receiving (3rd floor)                 │
│    Due: January 31                                               │
│                                                                   │
│  ○ Email & Documents Backup                 Scheduled: Jan 31    │
│    Status: Will be initiated on last day                         │
│    [View Policy]                                                 │
│                                                                   │
│  ⊙ IT Access Revocation                     Scheduled: Jan 31    │
│    Will be revoked on last day at 5:00 PM                       │
│    Systems affected: Slack, GitHub, VPN, Email, Analytics       │
│    [View Details] [Change Schedule]                              │
│                                                                   │
│ ─────────────────────────────────────────────────────────────────│
│                                                                   │
│  EXIT INTERVIEW & FINAL STEPS                                    │
│  ─────────────────────────────────────────────────────────────   │
│  ○ Exit Interview                                                │
│    Scheduled: January 30, 10:00 AM with HR                       │
│    [Join Meeting] [Reschedule]                                   │
│                                                                   │
│  ○ Employee Information Update                                   │
│    For Final Mailings: [Update Address]                          │
│                                                                   │
│  ○ Separation Agreement Signature                                │
│    Status: Sent Jan 20, pending signature                        │
│    [View Document] [Sign Now]                                    │
│                                                                   │
│  ○ Alumni Network Invite (Optional)                              │
│    [Join Alumni Network] [Decline]                               │
│                                                                   │
│  [Support & FAQ] [Contact HR] [View Full Checklist]              │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Detailed Features

#### 1. Offboarding Status Overview
**Shows:**
- Employee name, role, department, manager
- Last day countdown timer
- Offboarding reason (resignation, termination, retirement, etc.)
- Overall completion % (progress bar)
- Timeline view of key dates

#### 2. Final Compensation & Admin
**Displays:**
- Final paycheck amount (including PTO payout)
- Paycheck date
- Benefits termination date
- COBRA information + download
- Expense reimbursement status
- Tax documents (W2) expected date
- Separation agreement status

**Actions:**
- View pay stub
- Approve final expenses
- Sign separation agreement
- Update address for final mailings

#### 3. Knowledge Transfer
**Includes:**
- Project handoff tasks and owners
- Documentation of critical processes
- Knowledge transfer session schedule (meetings with new owner)
- Key contacts and relationships
- Mentoring commitments (if applicable)

**Features:**
- Template for process documentation
- Calendar integration for transfer sessions
- Recording/notes from sessions
- Sign-off that knowledge was transferred

#### 4. Asset Return & Access Revocation
**Asset Inventory:**
- Laptop, monitor, peripherals, badge, headphones
- Special assets (keys, credit cards, etc.)
- Checklist with "returned" confirmation
- Alternative: Shipping label if remote

**Access Revocation:**
- List of systems (Slack, GitHub, Email, VPN, etc.)
- Revocation scheduled for last day at specified time
- Email backup scheduled
- IT confirms revocation completed

#### 5. Exit Interview
**Structured Interview Including:**
- Why they're leaving
- Experience with role and company
- Feedback on manager and team
- Feedback on company culture and processes
- Suggestions for improvement
- Optional: LinkedIn reference

#### 6. Optional Alumni Network
**Post-Employment Options:**
- Join company alumni network
- Stay in touch with colleagues
- Access to company events/updates
- Optional LinkedIn group

### AI-Powered Features

**Smart Offboarding Planning:**
- AI suggests risk level: "Critical role - 6 knowledge transfer sessions recommended"
- "High-risk projects - prioritize handoff and documentation"
- "New team member just started - pair with departing employee for knowledge transfer"

**Critical Knowledge Identification:**
- AI flags: "Only John knows database architecture - schedule immediate documentation"
- "John is primary on 3 critical projects - manager approval required before release"

**Retention Opportunities:**
- If resignation: AI flags key roles at-risk: "John is mentoring 2 junior engineers - transition mentor"
- Exit interview insights: "Pattern: 3 engineers left due to limited career growth - escalate to leadership"

**Compliance Automation:**
- Ensures all required tasks completed before system access revoked
- Reminds of WARN act notices if mass layoffs
- Tracks COBRA deadline compliance

### WCAG 2.2 AA Accessibility Requirements

#### Visual Accessibility
- **Checklist Items**: Checkboxes with text labels (not icon alone)
- **Status Indicators**: Text + icons
  - ✓ (green) + "Completed"
  - ○ (gray) + "Not Started"
  - ⊙ (yellow) + "In Progress"
- **Countdown Timer**: Clear number of days (not just visual)
- **Color**: Text paired with visual indicators
- **Font Size**: 16px+ for body text
- **Contrast**: 4.5:1 for text, 3:1 for graphical elements

#### Keyboard Navigation
- **Checklist**: Tab through items, spacebar to expand, Enter to action
- **Dates**: Keyboard accessible date pickers
- **Links**: All links keyboard accessible ([View Details], [Sign Now], [Update Address])
- **Buttons**: All buttons keyboard accessible ([Mark Complete], [Reschedule], [Join Meeting])
- **Focus Indicators**: Clear 2px border on focused items

#### Screen Reader Compatibility
- **Checklist Structure**:
  - `<fieldset>` and `<legend>` for grouping (Final Compensation, Knowledge Transfer, etc.)
  - Each item: `<li><input type="checkbox" aria-label="Return Equipment"> Return Equipment (Due: Jan 31)</li>`
- **Status Announcements**:
  - Progress bar: `aria-label="Offboarding progress: 35% complete, 8 days remaining"`
  - Overdue items: `role="alert" aria-live="assertive"` for important deadlines
- **Dates**: `<time datetime="2024-01-31">January 31, 2024</time>`
- **Links to Documents**: Clear aria-labels
  - `<a href="..." aria-label="View COBRA details for final benefits">View COBRA Details</a>`

#### Focus Management
- **Page Load**: Focus on offboarding status heading
- **Expanded Sections**: Focus on first item in expanded section
- **Saved/Completed**: Focus on success message or next action
- **Modal/Dialog**: Focus trap in modal, focus returns to trigger when closed

#### Error States & Validation
- **Missing Critical Tasks**: Clear, urgent messaging
  - "⚠️ Equipment return not confirmed - must be completed by Jan 31"
- **Signature/Form Submission**: Required fields marked
  - "Separation Agreement *" + aria-required="true"
- **Deadline Warnings**: "2 days until equipment return deadline"

#### Motion & Animation
- **Checklist Items**: No animation (instant or simple fade)
- **Section Expansion**: Honor `prefers-reduced-motion`
- **Countdown Timer**: Static or simple update (no bouncing/flashing)

#### Touch Accessibility
- **Checkboxes**: 44x44px minimum touch targets
- **Buttons**: 44x44px minimum ([Mark Complete], [View Details], [Reschedule])
- **Expandable Sections**: 48px+ height for easy touch
- **Spacing**: 12px between interactive elements

### Data Model & Inputs

**Offboarding Task:**
- Task ID, category (asset return, knowledge transfer, admin, etc.)
- Title, description, due date
- Status (not_started, in_progress, completed, blocked, skipped)
- Assigned to (person/department)
- Supporting documents/forms

**Asset:**
- Asset ID, type (laptop, monitor, badge, etc.)
- Serial number, condition
- Checked out to (employee)
- Return status, return date
- Condition on return

**Knowledge Transfer Session:**
- Session ID, date/time, topic
- Attendees (departing employee, new owner, others)
- Recording/notes
- Sign-off status

### Data Outputs & Integrations

**HR Records:**
- Complete offboarding checklist (audit trail)
- Exit interview feedback
- Final compensation paid
- Archive of employee record

**IT/Security:**
- Access revocation confirmation
- Email archive/backup status
- Data handling per policy
- Asset return inventory

**Analytics/Insights:**
- Offboarding completion metrics
- Exit reasons and patterns
- Retention analysis (do certain departments/roles have higher turnover?)
- Knowledge transfer effectiveness

**Integrations:**
- **Payroll**: Final paycheck calculation, PTO payout
- **IT/LDAP**: Access revocation scheduling
- **Email System**: Archive/backup, forwarding rules
- **Finance**: Expense reimbursement, asset tracking
- **Calendar**: Meeting scheduling for exit interview, knowledge transfer sessions
- **Document System**: Separation agreements, COBRA notices
- **Alumni Network**: Optional enrollment

### Edge Cases & Error Handling

1. **Employee is on Bonus/Stock/Equity Schedule**
   - Compliance rules must be followed (document per company policy)
   - Payroll ensures all vestings, bonuses handled correctly
   - Finance team approval required

2. **Critical Knowledge Not Transferred by Last Day**
   - System escalates to manager + HR
   - May extend employment or arrange consulting
   - Documents the knowledge gap for future onboarding

3. **Equipment Not Returned**
   - System notifies IT + Finance
   - May pursue recovery or mark as asset loss
   - Possible legal action if value significant

4. **Employee Disputes Final Compensation**
   - Clear itemization provided
   - Escalation to Finance + HR
   - Documentation of calculation for audit trail

5. **Rehire Eligibility**
   - Company policy determines rehire status (eligible, not eligible, upon approval)
   - Tracked in employee record for future reference

### Inter-Screen Interactions

- **Triggered by**: Resignation/termination entered in employee record
- **Linked from**: New Hire Onboarding (inverse process)
- **Provides Data to**: HR records (departure date, reason, final compensation)
- **Integrates with**: Finance (final payroll), IT (access revocation), Payroll (COBRA)
- **Optional**: Alumni Network enrollment

---

## SUMMARY

These 8 onboarding and offboarding screens form a comprehensive workflow from offer acceptance through day 90 and beyond, with structured processes, clear accountability, and AI-powered insights. Each screen prioritizes WCAG 2.2 AA accessibility, ensuring all employees and managers can participate fully, regardless of ability.

**Key Accessibility Themes Across All Screens:**
- Color + text/icons for all status indicators
- Keyboard navigation with clear focus indicators
- Screen reader compatible with semantic HTML and ARIA labels
- Sufficient contrast (4.5:1 text, 3:1 graphics)
- 44x44px minimum touch targets
- Plain language, clear instructions
- Error states are specific and actionable
- Respect for motion preferences

Next steps: Use these prompts to design Figma wireframes, build UI components, or generate coded implementations.
