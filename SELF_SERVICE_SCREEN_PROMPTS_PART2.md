# Employee Self-Service Screen Prompts (Part 2)

> **Accessibility Standard**: All screens below meet WCAG 2.2 AA standards with comprehensive accessibility requirements covering color contrast, keyboard navigation, screen reader compatibility, focus management, touch targets, error handling, and motion preferences.

---

## Screen 4.4: Time Off Calendar

### Purpose
Provide employees and managers with a visual calendar view of team and company time off schedules, enabling better planning and coverage coordination. Employees see their own approvals and can view team availability; managers see full team calendar with absence types.

### User Personas
- **Primary**: All Employees, Managers
- **Secondary**: HR Partners (company-wide view)

### Layout & Wireframe

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ←  Time Off Calendar 2025        [List View]  [My Calendar]    │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  VIEW: [My Team ▼]  |  FILTER: [All Leave Types ▼]              │
│                                                                   │
│  January 2025                            [< Prev]  [Next >]      │
│  ┌─────┬─────┬─────┬─────┬─────┬─────┬─────┐                    │
│  │ Sun │ Mon │ Tue │ Wed │ Thu │ Fri │ Sat │                    │
│  ├─────┼─────┼─────┼─────┼─────┼─────┼─────┤                    │
│  │     │     │     │  1  │  2  │  3  │  4  │                    │
│  │     │  5  │  6  │  7  │  8  │  9  │ 10  │                    │
│  │     │ 12  │ 13  │ 14  │ 15  │ 16  │ 17  │ (company holiday)  │
│  │     │ 19  │ 20  │ 21  │ 22  │ 23  │ 24  │                    │
│  │ 26  │ 27  │ 28  │ 29  │ 30  │ 31  │     │                    │
│  └─────┴─────┴─────┴─────┴─────┴─────┴─────┘                    │
│                                                                   │
│  TEAM MEMBER ABSENCES (January 2025):                            │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Sarah Chen (Manager)    [V] Jan 15 (Vacation - 1 day)       ││
│  │ John Smith             [V] Jan 30-Feb 3 (Vacation)          ││
│  │ Alex Johnson           [S] Jan 24 (Sick Leave)              ││
│  │ Maria Rodriguez        [H] Jan 15 (Holiday)                 ││
│  │ Mike Davis             [P] Jan 22 (Personal Day)            ││
│  │ Jamie Lee              [V] Jan 7-9 (Vacation)               ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  LEGEND:                                                          │
│  [V] Vacation  [S] Sick Leave  [P] Personal  [H] Holiday [BL] Blackout│
│                                                                   │
│  COVERAGE STATUS:                                                 │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Jan 30-Feb 3: 2 of 8 team members away (75% coverage)       ││
│  │ Risk Level: Low [View Coverage Plan]                        ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  COMPANY HOLIDAYS 2025:                                           │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Jan 1  - New Year's Day (Wed)                               ││
│  │ Feb 17 - Presidents Day (Mon)                               ││
│  │ Mar 17 - Observed Holiday (Mon)                             ││
│  │ [Show More Holidays]                                        ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

#### 1. Calendar View Options
- **Month View** (default)
  - Full month grid showing all dates
  - Click on date to see details
  - Multiple absences on same day shown with count badge
  - Weekends shaded differently
  - Company holidays highlighted

- **List View**
  - Chronological list of all absences
  - Filterable by team member, leave type, date range
  - Each absence card shows: person, dates, type, duration
  - Click to expand details

- **Team/Individual Toggle**
  - "My Team" — shows all direct reports (manager view)
  - "Company" — shows organization-wide (limited by permissions)
  - "My Calendar" — shows only current user's approvals

#### 2. Leave Type Filtering
- **Multi-select Filters**
  - Vacation
  - Sick Leave
  - Personal Days
  - Floating Holidays
  - Unpaid Leave
  - Bereavement
  - Sabbatical
  - Company Holidays
  - Blackout Dates
  - Toggle "Show my absences" separately

#### 3. Team Absences List
- **Display Format**
  - Employee name (linked to profile)
  - Leave type with icon/badge
  - Date range (formatted: "Jan 30-Feb 3")
  - Duration ("4 business days")
  - Status indicator (Approved, Pending, Tentative)
  - Expandable for coverage details

- **Manager View Additional Info**
  - Coverage status for that absence
  - Who's covering (if handoff documented)
  - Approval status and date
  - Comments/notes (if provided)

#### 4. Coverage Planning
- **Coverage Status Indicator**
  - For dates with team absences: "X of Y team members away"
  - Coverage percentage calculation
  - Risk level color coding: Green (adequate), Yellow (monitor), Red (understaffed)
  - Suggested actions for coverage issues

- **Coverage Plan Link**
  - Click to view who's covering during absence
  - Based on handoff notes from time off request
  - Highlight gaps in coverage
  - Allow manager to reassign coverage

#### 5. Company Holiday & Blackout Display
- **Company Holidays**
  - Full list of company holidays for year
  - Observed date if different from actual date
  - Company closure dates
  - Time off not needed for these dates

- **Blackout Dates**
  - Critical project dates when time off restricted
  - Department-specific blackout dates
  - Red highlighting on calendar
  - Reason for blackout (if available)

#### 6. Calendar Navigation
- **Month/Year Selector**
  - Previous/Next month arrows
  - Month/Year dropdown for quick jump
  - Today button to return to current date
  - Date range picker for custom range

- **Print & Export**
  - Print calendar view
  - Export to iCal format
  - Export team absences as CSV

### Data Model

```
TimeOffCalendar {
  id: UUID
  calendar_type: Enum (INDIVIDUAL, TEAM, COMPANY)
  owner_id: UUID (FK to Employee) [nullable for company calendar]
  team_id: UUID (FK to Team) [nullable, for team calendar]
  year: Integer
  month: Integer (1-12)
  
  entries: Array<CalendarEntry {
    id: UUID
    date: Date
    employee_id: UUID
    leave_type: Enum (VACATION, SICK, PERSONAL, HOLIDAY, BLACKOUT, etc.)
    leave_request_id: UUID (FK to TimeOffRequest)
    is_half_day: Boolean
    status: Enum (APPROVED, PENDING, TENTATIVE, REJECTED)
    employee_name: String
    department: String
    manager_name: String
    coverage_assigned_to: Array<UUID> (employee IDs)
    notes: String
  }>
}

CalendarFilter {
  view_type: Enum (MONTH, LIST, WEEK)
  team_scope: Enum (MY_TEAM, COMPANY, DIRECT_REPORTS)
  leave_types: Array<String> (VACATION, SICK, PERSONAL, etc.)
  date_range: {
    start_date: Date
    end_date: Date
  }
  include_company_holidays: Boolean
  include_blackout_dates: Boolean
}

CoverageStatus {
  id: UUID
  date_range: {
    start_date: Date
    end_date: Date
  }
  team_id: UUID
  total_team_size: Integer
  absent_count: Integer
  coverage_percentage: Decimal (0-100)
  coverage_level: Enum (GREEN, YELLOW, RED)
  at_risk_projects: Array<String>
  coverage_assignments: Array<{
    absent_employee_id: UUID
    covering_employee_id: UUID
    coverage_type: String (full, partial, escalation)
  }>
}

CompanyHoliday {
  id: UUID
  name: String
  actual_date: Date
  observed_date: Date (nullable, if observed on different date)
  description: String
  is_paid: Boolean
  affected_departments: Array<UUID> (if department-specific)
}

BlackoutDate {
  id: UUID
  start_date: Date
  end_date: Date
  reason: String
  department_id: UUID (nullable, if department-specific)
  project_id: UUID (nullable)
  severity: Enum (ADVISORY, RESTRICTED, PROHIBITED)
  exceptions_allowed: Boolean
}
```

### UI Components Required
- Calendar grid component (month view)
- List component with grouping (by team member, by date)
- Filter menu with multi-select
- Badge: Leave type indicator
- Color-coded calendar cells
- Expandable detail panel
- Date range picker
- Export button with dropdown

### WCAG 2.2 AA Accessibility Requirements

#### Color & Contrast
- Calendar cells have 4.5:1 contrast between text and background
- Leave type badges (V, S, P, H) have text labels in addition to color coding
- Company holidays highlighted with pattern (stripe) + color (not color alone)
- Blackout dates have distinct visual indicator
- Weekends and weekdays distinguished with 3:1 contrast minimum

#### Keyboard Navigation
- Tab through calendar dates (arrow keys navigate within grid)
- Calendar grid has `role="grid"` with `aria-rowcount`, `aria-colcount`
- Arrow keys navigate date cells (up/down/left/right)
- Enter to view date details
- Filter buttons keyboard accessible
- List view items navigable with arrow keys
- Skip link to jump to calendar grid

#### Screen Reader Support
- Page title: "Time Off Calendar 2025"
- Month view marked `<section aria-label="January 2025 calendar">`
- Calendar grid uses `<table role="grid">` with proper `aria-selected` states
- Each date cell: `<div role="gridcell" aria-label="January 15, 2025, Wednesday. John Smith (Vacation, approved).">`
- Multiple absences: `aria-label="January 30, 2025. 2 absences: John Smith (Vacation), Alex Johnson (Sick Leave)."`
- Leave type icons have text equivalents: `<span aria-label="Vacation">[V]</span>`
- Filter state announced: `aria-label="Filters: Vacation, Sick Leave"`
- Coverage status: `<section aria-label="Coverage Status: 2 of 8 team members away, 75% coverage, Low risk">`
- Blackout dates: `aria-label="January 31 - February 14, 2025. Critical project deadline. Time off restricted."`

#### Focus Management
- Calendar grid receives focus on page load
- First date cell (today or month start) has focus ring
- When selecting filter, focus remains on filter button (with aria-pressed state)
- When navigating to different month, focus moves to first date of new month
- Skip to main calendar link available at top

#### Touch & Target Size
- Calendar date cells: minimum 44×44 px
- Filter buttons: 44×44 px minimum
- View toggle buttons (Month/List): 44×44 px
- Navigation arrows (Prev/Next): 44×44 px
- Leave type badges on list items: 40px height minimum

#### Error Handling & Validation
- If no absences found: "No time off scheduled for this period" (neutral message)
- If calendar data fails to load: "Calendar data couldn't load. Try refreshing." with retry button
- Permission denied for company view: "You don't have permission to view company-wide calendar."
- All error messages have `role="alert"`

#### Motion & Animation
- Calendar month transitions respect `prefers-reduced-motion` (instant switch, no animation)
- List item expansions instant (no slide-down animation)
- Hover effects have static alternatives (not animation-dependent)

#### Semantic HTML & ARIA
- Proper heading hierarchy: `<h1>` for page, `<h2>` for sections
- Calendar as `<table role="grid">` with `<thead>`, `<tbody>`
- Filter list as `<ul>` with `<li>` for each filter option
- Leave type legend as `<dl>` (definition list)
- Buttons with clear labels: `<button aria-label="View previous month (December)">Previous</button>`

### AI Integration Points

#### 1. Coverage Intelligence
- **Staffing Alerts**: "Jan 30-Feb 3: Only 2 engineers available. Risk level: High. Need 1 more engineer."
- **Smart Reassignment**: Suggest team members who can cover based on skills/availability
- **Project Impact**: "Marketing campaign launch Feb 15. Current absences shouldn't impact launch."

#### 2. Absence Pattern Detection
- **Unusual Patterns**: "Alex Johnson has 4 consecutive Mondays off in Q1. Possible pattern."
- **High-Usage Periods**: "Q2 has 18 vacation days taken by team (average 12). Monitor approval process."
- **Fairness Analysis**: Compare absence usage across team to flag inequities

#### 3. Blackout Date Recommendations
- **Automatic Blackout Suggestion**: Based on project timeline, suggest blackout dates for critical periods
- **Conflict Detection**: "3 team members have vacation approved during critical project period. Review?"

#### 4. Calendar Optimization
- **Scheduling Suggestions**: "Consider requesting Feb 17-21 (already has President's Day, reducing coverage gap)"
- **Trend Analysis**: "Your team has historically taken 40% of vacation in Q3. Proactively plan coverage."

### Integrations & Dependencies

#### Internal Integrations
- **Time Off Requests**: Pull approved time off from request module
- **HRIS Core**: Employee data, organizational structure, team membership
- **Calendar System**: Company holiday calendar, manager calendars (availability)
- **Project Management**: Project milestones for blackout date correlation
- **Notification System**: Alert managers when coverage is insufficient

#### External Integrations
- **Calendar Providers**: Export to Google Calendar, Outlook, iCal
- **Analytics**: Track absence patterns, coverage rates over time

### Edge Cases & Error States

#### 1. Overlapping/Conflicting Absences
- **Same Date, Different Types**: Show all absences (e.g., John on vacation, Sarah on sick leave)
- **Handoff Conflict**: If person covering is also absent on same date, highlight conflict

#### 2. Permission-Based View Limits
- **Non-Managers**: Can see own time off + company holidays + team members' time off (configurable)
- **Managers**: Can see direct reports' time off, not peers' time off
- **HR**: Can see all time off (for compliance)
- **Restricted Departments**: Hide absences for security/sensitive roles

#### 3. Data Inconsistencies
- **Pending Requests**: Show with "Pending" indicator (don't assume approved)
- **Cancelled Requests**: Don't display on calendar
- **Withdrawn Requests**: Remove from calendar if user searches history

#### 4. Timezone Handling
- **Remote Teams**: Display times in employee's timezone with note
- **Date Boundary Crossing**: If absence crosses timezone boundary, clarify dates in both zones

### Success Metrics & Testing Scenarios

#### Calendar Display
- [ ] Month view displays all dates correctly
- [ ] Multiple absences on same date show all entries
- [ ] Company holidays display with correct highlighting
- [ ] Weekends/weekdays visually distinct

#### Navigation & Filtering
- [ ] Previous/Next month navigation works
- [ ] Month/Year dropdown jumps to correct month
- [ ] Filter selections update calendar correctly
- [ ] Filtered results show only selected leave types

#### Team View
- [ ] Team member absences display correctly
- [ ] Coverage percentage calculated accurately
- [ ] Risk level color-coding correct
- [ ] Manager view shows only direct reports

#### Data Accuracy
- [ ] Absences match approved time off requests
- [ ] Duration calculations correct (business days vs. calendar days)
- [ ] Pending requests marked as such
- [ ] Cancelled absences removed from calendar

#### Accessibility
- [ ] Calendar grid navigable with arrow keys
- [ ] Screen reader announces all dates and absences
- [ ] Filter state changes announced
- [ ] Color not only means of differentiation

---

## Screen 4.5: Expense Report

### Purpose
Enable employees to submit expense reports for reimbursement with receipt uploads, category management, policy compliance checking, and approval workflow tracking. AI features include receipt scanning, auto-categorization, and duplicate detection.

### User Personas
- **Primary**: All Employees
- **Secondary**: Managers (approval), Finance Team (processing)

### Layout & Wireframe

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ←  Expense Report              [Recent Reports]  [Policies]     │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  CREATE NEW EXPENSE REPORT                                       │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Report Date Range: [Jan 1 - Jan 31, 2025 ▼]                 ││
│  │ Project/Cost Center: [Project X ▼]                          ││
│  │ Business Purpose: [___________________________________]      ││
│  │                   [Q1 Product Launch Meeting]                ││
│  │                                                              ││
│  │ ADD EXPENSES:                                                ││
│  │ ┌──────────────────────────────────────────────────────────┐││
│  │ │ Expense Type: [Meals ▼]                                  │││
│  │ │ Date: [Jan 15, 2025 ▼]                                   │││
│  │ │ Category: [Meals & Entertainment ▼]                      │││
│  │ │ Description: [Client lunch meeting]                      │││
│  │ │ Amount: [$________] USD                                  │││
│  │ │ Receipt: [Upload Receipt] or [Scan Receipt with Camera] │││
│  │ │                                                           │││
│  │ │ [+ Add Another Expense]                                  │││
│  │ └──────────────────────────────────────────────────────────┘││
│  │                                                              ││
│  │ EXPENSE SUMMARY:                                            ││
│  │ ┌──────────────────────────────────────────────────────────┐││
│  │ │ Meals & Entertainment:  $145.50  (3 receipts)            │││
│  │ │ Transportation:         $87.25   (2 receipts)            │││
│  │ │ Supplies:              $23.99   (1 receipt)              │││
│  │ │                                                           │││
│  │ │ TOTAL: $256.74                                           │││
│  │ │ Policy Compliance: ✓ All expenses within policy          │││
│  │ │                                                           │││
│  │ │ [Review Receipts]  [Validate]  [Cancel]                │││
│  │ └──────────────────────────────────────────────────────────┘││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  SUBMITTED REPORTS                                               │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Dec 1-31, 2024 - Product Launch Expenses                    ││
│  │ Status: Paid on Jan 10, 2025  |  Total: $523.40            ││
│  │ [View]                                                       ││
│  │                                                              ││
│  │ Nov 1-30, 2024 - Travel Reimbursement                       ││
│  │ Status: Approved, pending payment  |  Total: $1,245.99     ││
│  │ [View]                                                       ││
│  │                                                              ││
│  │ Oct 15-31, 2024 - Client Entertainment                      ││
│  │ Status: Pending Manager Approval  |  Total: $89.50         ││
│  │ [View]  [Edit]  [Withdraw]                                  ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

#### 1. Expense Report Header
- **Report Details**
  - Date range (start/end date picker)
  - Project or cost center assignment
  - Business purpose/description (required)
  - Report status (Draft, Submitted, Approved, Paid, Rejected)

- **Report Metadata**
  - Report ID/number for reference
  - Submission date
  - Approval manager
  - Approval/rejection date and comments

#### 2. Add Expenses
- **Expense Form**
  - Date picker (expense date)
  - Expense type dropdown (Meals, Travel, Supplies, Equipment, etc.)
  - Category auto-suggestion (based on type)
  - Description field (required, 200 char max)
  - Amount in USD (decimal input)
  - Currency selection (if multi-currency support)
  - Merchant name (optional, extracted from receipt)
  - Receipt upload

- **Receipt Handling**
  - File upload button for receipt image (JPG, PNG, PDF)
  - Drag-drop receipt upload
  - Camera icon to scan receipt with phone camera
  - OCR extraction of amount and merchant (AI)
  - Preview receipt image before saving
  - Max file size: 10MB per receipt
  - Validation: amount matches receipt

- **Bulk Upload Option**
  - Upload ZIP of multiple receipts
  - Auto-parse receipt data
  - Match receipts to expense amounts

#### 3. Expense List & Management
- **Expense Item Cards**
  - Date, category, description
  - Amount (highlighted)
  - Receipt thumbnail (if image)
  - Policy compliance indicator (✓ or ⚠)
  - Edit/delete buttons
  - Reorder/prioritize option

- **Expense Categorization**
  - Auto-suggest category based on merchant name
  - Manual override available
  - Policy guidelines per category (max amount, approval requirement)
  - Tooltip: "Meals max $75/person, Group meals max $200"

- **Duplicate Detection**
  - AI alerts if same amount/merchant submitted twice
  - Option to merge duplicates
  - Manual confirmation if flagged as duplicate

#### 4. Expense Summary & Totals
- **Summary View**
  - Total by category (breakdown)
  - Grand total
  - Number of receipts attached
  - Days covered
  - Average daily expense

- **Policy Compliance Checker**
  - Green checkmark: "All expenses comply with policy"
  - Yellow warning: "Meal expense $95 exceeds policy limit of $75. Manager approval required."
  - Red error: "Business travel without pre-approval required."

#### 5. Review & Submission
- **Receipt Gallery**
  - Modal to view all attached receipts
  - Zoom/pan receipt images
  - Download individual receipt
  - Receipt list with related expense amount

- **Validation Before Submit**
  - All expenses have receipts (required)
  - All required fields complete
  - Policy compliance checks
  - Business purpose provided
  - Confirmation: "Ready to submit for approval"

- **Submit Report**
  - Send for manager approval
  - Notification to manager
  - Report locked for editing after submission
  - Confirmation screen with reference number

#### 6. Report History & Status Tracking
- **Report List**
  - Date range
  - Report total
  - Status badge (Draft, Submitted, Approved, Paid, Rejected)
  - Submission date
  - Last updated date

- **Report Status Details**
  - Current status
  - Timeline of status changes (submitted, approved, paid)
  - Approval manager
  - Approval comments/notes
  - Payment date (if paid)
  - Payment method

- **Report Actions**
  - View full report details
  - Edit (if draft or rejected)
  - Re-submit (if rejected with feedback)
  - Download as PDF
  - Email receipts to accountant

### Data Model

```
ExpenseReport {
  id: UUID
  report_number: String (format: "EXP-2025-001")
  employee_id: UUID (FK to Employee)
  
  date_range: {
    start_date: Date
    end_date: Date
  }
  
  business_purpose: String (required, max 500 chars)
  project_id: UUID (FK to Project) (nullable)
  cost_center_id: UUID (FK to CostCenter) (nullable)
  
  expenses: Array<Expense {
    id: UUID
    date: Date
    type: Enum (MEALS, TRAVEL, SUPPLIES, EQUIPMENT, ACCOMMODATION, ENTERTAINMENT, OTHER)
    category: String
    description: String (required)
    amount: Decimal (USD)
    currency: String (default: USD)
    merchant_name: String (nullable, extracted from receipt)
    receipt_id: UUID (FK to Receipt)
    receipt_url: String
    receipt_ocr_data: {
      amount: Decimal (extracted from receipt)
      merchant: String
      date: Date
      confidence: Float (0-1)
    }
    policy_compliant: Boolean
    policy_violation_reason: String (nullable)
    created_at: Timestamp
    updated_at: Timestamp
  }>
  
  total_amount: Decimal (sum of all expenses)
  currency: String (report currency)
  
  status: Enum (DRAFT, SUBMITTED, APPROVED, PAID, REJECTED, WITHDRAWN)
  
  manager_id: UUID (FK to Employee) [auto-set to employee's manager]
  manager_approval_date: Timestamp (nullable)
  manager_comments: Text (nullable)
  
  finance_reviewer_id: UUID (FK to Employee) (nullable)
  finance_review_date: Timestamp (nullable)
  finance_comments: Text (nullable)
  
  payment_status: Enum (NOT_PAID, PENDING, PAID, FAILED)
  payment_date: Date (nullable)
  payment_method: Enum (DIRECT_DEPOSIT, COMPANY_CARD_CREDIT, CHECK)
  
  policy_compliance_status: Enum (COMPLIANT, WARNINGS, VIOLATIONS)
  policy_violation_count: Integer
  policy_violations: Array<{
    expense_id: UUID
    violation_type: String
    description: String
    required_approval: Boolean
  }>
  
  duplicate_flags: Array<{
    flagged_expense_id: UUID
    potential_duplicate_id: UUID
    confidence: Float (0-1)
    resolution: Enum (MERGED, REJECTED, CONFIRMED_DIFFERENT)
  }>
  
  submitted_at: Timestamp (nullable)
  created_at: Timestamp
  updated_at: Timestamp
}

Expense {
  id: UUID
  report_id: UUID (FK to ExpenseReport)
  date: Date
  type: Enum (MEALS, TRAVEL, SUPPLIES, EQUIPMENT, ACCOMMODATION, ENTERTAINMENT, OTHER)
  category: String
  description: String
  amount: Decimal
  currency: String
  merchant_name: String (nullable)
  receipt_id: UUID (FK to Receipt)
  
  created_at: Timestamp
  updated_at: Timestamp
}

Receipt {
  id: UUID
  report_id: UUID (FK to ExpenseReport)
  expense_id: UUID (FK to Expense)
  file_name: String
  file_url: String (cloud storage URL)
  file_type: Enum (JPEG, PNG, PDF)
  file_size: Integer (bytes)
  
  ocr_extracted_data: {
    amount: Decimal
    merchant: String
    date: Date
    vendor_address: String
    ocr_confidence: Float (0-1)
  }
  
  uploaded_at: Timestamp
}

ExpensePolicy {
  id: UUID
  company_id: UUID
  category: Enum (MEALS, TRAVEL, SUPPLIES, ENTERTAINMENT)
  max_per_day: Decimal (nullable)
  max_per_transaction: Decimal
  max_per_month: Decimal (nullable)
  requires_pre_approval_above: Decimal (nullable)
  requires_manager_approval_above: Decimal
  description: Text
  exceptions: Array<{
    role: String
    limit_override: Decimal
  }>
  
  created_at: Timestamp
  updated_at: Timestamp
}
```

### UI Components Required
- Card component: Expense item
- Modal: Receipt gallery/preview
- File upload: Receipt upload with drag-drop
- Camera capture: Mobile receipt scanning
- Input: Amount decimal field
- Dropdown: Expense type, category, project
- Badge: Policy compliance indicator
- Timeline: Report status history
- Table: Expense summary by category

### WCAG 2.2 AA Accessibility Requirements

#### Color & Contrast
- Policy compliance indicators (✓/⚠) have text label + color
- Amount values have 4.5:1 contrast with background
- Status badges have text label (not color alone)
- Receipt upload area has clear visual boundary (4.5:1 border contrast)
- Category labels have 4.5:1 contrast

#### Keyboard Navigation
- Tab through all form fields: date → type → category → description → amount → receipt → add another
- File upload button keyboard accessible
- All dropdowns keyboard operable (arrow keys, Enter to select)
- Receipt gallery navigable with arrow keys (previous/next image)
- Report list items keyboard navigable
- Expense items can be deleted/edited with keyboard

#### Screen Reader Support
- Page title: "Expense Report"
- Expense form marked `<fieldset><legend>Add Expense</legend>...</fieldset>`
- Expense type label: `<label for="expense-type">Expense Type (required)</label>`
- Amount input: `<label for="amount">Amount in USD (required)</label><input id="amount" type="number" aria-describedby="amount-help"><div id="amount-help">Enter amount with cents, e.g., 45.99</div>`
- Receipt upload: `<label for="receipt-upload">Receipt (required)</label><input id="receipt-upload" type="file" aria-label="Upload receipt image, JPG or PNG">`
- Policy compliance: `<div aria-live="polite" aria-label="Policy Compliance: All expenses within policy."></div>`
- Duplicate flag: `<div aria-live="alert">Duplicate detected: Amount matches transaction from Jan 10. Confirm this is a different expense.</div>`
- Report list marked `<section aria-label="Expense Reports (4 reports)">`
- Status live region: `<div aria-live="polite" aria-label="Report status updated to Approved.">`

#### Focus Management
- Expense type dropdown receives focus on form load
- When adding expense, new empty form section receives focus
- After uploading receipt, focus returns to amount field
- When submitting report, focus moves to success message
- Edit/delete buttons focus retained on same item after action

#### Touch & Target Size
- Receipt upload area: 120×120 px minimum hit target (larger drop zone recommended)
- Receipt upload button: 44×44 px
- File delete button: 44×44 px
- Camera capture button: 44×44 px
- Expense item action buttons (edit/delete): 44×44 px each
- Amount input field: 40px min height, 100px min width
- "Add Another Expense" button: 44×44 px

#### Error Handling & Validation
- Missing receipt: "Receipt required for all expenses" (clear requirement)
- File too large: "Receipt file is 12MB. Maximum size is 10MB." (specific)
- Amount exceeds policy: "This meal expense ($95) exceeds the per-transaction limit of $75. Manager approval required." (explains policy)
- Duplicate detected: "This $67.50 transaction on Jan 15 matches a transaction on Jan 10. Is this a duplicate?" (actionable)
- Missing business purpose: "Business purpose is required. Please explain the business reason for these expenses." (explains why)
- All errors have `role="alert"` and high contrast color

#### Motion & Animation
- Receipt image transitions respect `prefers-reduced-motion`
- Form expansion/collapse animations respect preference
- Status changes announced immediately (not animated)
- Dropdown open/close instant or respecting preference

#### Semantic HTML & ARIA
- Form inputs have associated `<label>` tags
- Expense items in `<ul>` with `<li>` for each item
- Category list uses `<dl>` format
- Receipt gallery uses `<figure>` with `<figcaption>`
- Report summary in `<table>` with proper `<thead>`, `<tbody>`
- Status timeline uses `<ol>` (ordered list)

### AI Integration Points

#### 1. Receipt Scanning & OCR
- **Automatic Data Extraction**: Scan receipt image, extract amount, merchant, date
  - "Receipt scanned: $45.99 from Starbucks on Jan 15"
- **Amount Verification**: Compare extracted amount with user-entered amount
  - "Extracted amount ($45.99) matches entered amount. ✓"
- **Missing Data Detection**: "Receipt image unclear. Please re-scan merchant name section."

#### 2. Expense Categorization
- **Auto-Category Suggestion**: Based on merchant name, suggest category
  - "Starbucks → Meals & Entertainment"
  - "Uber → Transportation"
  - "Best Buy → Supplies/Equipment"
- **Correction Learning**: If user corrects auto-suggested category, learn for future

#### 3. Policy Compliance Checking
- **Real-time Compliance**: Check each expense against company policy
  - "This meal expense exceeds $75 limit. Manager approval required."
- **Cross-policy Alerts**: "You've spent $200 on meals this month. Remaining budget: $50."
- **Missing Pre-Approval**: "This equipment purchase ($500) requires pre-approval. Request approval first?"

#### 4. Duplicate Detection
- **Same Merchant, Same Amount**: Flag as possible duplicate
  - "This $45.99 Starbucks charge matches Jan 10 transaction. Duplicate?"
- **Multiple Submissions**: Detect if expense submitted in multiple reports
- **Card Reconciliation**: Compare to corporate card transactions

#### 5. Expense Optimization
- **Tax Category Tagging**: Suggest tax-deductible categories
  - "Meals with clients may be tax-deductible. Category: Business Entertainment"
- **Travel Expense Bundling**: Group hotel + meals + transport under travel project
- **Reimbursement Speed**: Predict payment timeline based on policy and manager workload

### Integrations & Dependencies

#### Internal Integrations
- **HRIS Core**: Employee data, manager relationships
- **Payroll System**: Deposit direct reimbursements to payroll
- **Finance/Accounting**: Expense reports feed to GL, cost center tracking
- **Project Management**: Cost center/project assignment, budget tracking
- **Notification System**: Email notifications for submissions, approvals, payments
- **Manager Dashboard**: Expense approval queue

#### External Integrations
- **OCR Service**: Cloud vision API for receipt scanning (Google Cloud Vision, AWS Textract)
- **File Storage**: Cloud storage for receipt images (S3, Azure Blob, Google Cloud Storage)
- **Accounting Software**: Export approved expenses to QuickBooks, NetSuite
- **Payment System**: Direct deposit processing via payroll provider

### Edge Cases & Error States

#### 1. Multi-Currency Expenses
- **Foreign Travel**: Allow currency selection (EUR, GBP, JPY, etc.)
- **Conversion Rate**: Auto-apply daily exchange rate or allow manual entry
- **Report Total**: Sum in employee's home currency

#### 2. Missing Receipts
- **Policy Exception**: For expenses < $25, receipt may be waived (configurable)
- **Lost Receipt Affidavit**: Option to submit statement instead of receipt (requires manager approval)
- **Merchant Verification**: If no receipt, allow manager to verify with corporate card statement

#### 3. Report Rejection & Resubmission
- **Manager Rejection**: Provide detailed feedback
  - "Receipt illegible - cannot verify amount. Please re-submit with clearer image."
- **Edit & Resubmit**: Return to draft mode, allow corrections, resubmit
- **History**: Track resubmission attempts and changes

#### 4. Payment Processing
- **Payment Delay**: Notify if payment delayed > 5 business days
- **Failed Deposit**: If ACH fails, fallback to check payment
- **Negative Balance**: If employee owes company (overpayment from prior report), apply offset

#### 5. Manager Escalation
- **Threshold Exceeded**: Reports > $500 automatically route to finance review (configurable)
- **Policy Violation**: Expenses violating policy require exception approval
- **Suspicious Patterns**: Flag if employee submitting expenses daily (possible scam)

### Success Metrics & Testing Scenarios

#### Expense Submission
- [ ] Expense report submits without errors
- [ ] All fields required for submission are enforced
- [ ] Receipt file uploads successfully
- [ ] Amount extracted from receipt matches entered amount

#### Receipt Processing
- [ ] Receipt OCR extracts merchant name correctly
- [ ] Receipt OCR extracts amount correctly
- [ ] Receipt image displays in preview
- [ ] Receipt can be viewed at full resolution

#### Policy Compliance
- [ ] Policy violations detected and flagged
- [ ] Compliant expenses pass validation
- [ ] Warnings display for borderline expenses
- [ ] Report cannot submit with unresolved violations

#### Duplicate Detection
- [ ] Duplicate expenses flagged correctly
- [ ] False positives minimal
- [ ] User can confirm as different if not duplicate
- [ ] Merged duplicates removed from report

#### Manager Approval
- [ ] Manager receives notification
- [ ] Manager can approve/reject via email or portal
- [ ] Employee notified of decision immediately
- [ ] Approved reports proceed to payment

#### Accessibility
- [ ] Form keyboard navigable
- [ ] Receipt upload works with keyboard
- [ ] Screen reader announces all form fields
- [ ] Error messages clear and actionable

---

## Screen 4.6: Pay Stub & Payroll Information

### Purpose
Enable employees to access and download current and historical pay stubs, review earnings breakdown (gross, deductions, taxes, benefits), verify direct deposit, and understand payroll calendar and tax withholding.

### User Personas
- **Primary**: All Employees
- **Secondary**: Finance/Payroll Team (for compliance)

### Layout & Wireframe

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ←  Pay Stub & Payroll          [View Current]  [W4 Settings]   │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  CURRENT PAY PERIOD (Most Recent)                               │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Pay Period: Jan 1-15, 2025                                   ││
│  │ Pay Date: Jan 20, 2025                                       ││
│  │ [Download PDF]  [Email]  [View Full Details]                ││
│  │                                                              ││
│  │ EARNINGS                          DEDUCTIONS                 ││
│  │ ├─ Salary:         $3,000.00     ├─ Federal Tax:  $450.00   ││
│  │ ├─ Bonus:          $500.00       ├─ Social Security: $186.00││
│  │ ├─ Overtime:       $150.00       ├─ Medicare:      $43.50   ││
│  │ └─ Other:          $0.00         ├─ 401k Contrib:  $200.00  ││
│  │                                    ├─ Health Ins:   $250.00  ││
│  │ GROSS PAY: $3,650.00              └─ Other:        $0.00    ││
│  │                                                              ││
│  │ TAXES: $679.50  |  BENEFITS: $450.00  |  DEDUCTIONS: $0.00 ││
│  │                                                              ││
│  │ NET PAY (Direct Deposit): $2,520.50                         ││
│  │ Last 4 of Account: ****0123  |  Deposit Confirmed           ││
│  │                                                              ││
│  │ YEAR-TO-DATE TOTALS (as of Jan 15, 2025)                   ││
│  │ ├─ Gross Pay:          $3,650.00                            ││
│  │ ├─ Federal Taxes:      $450.00                              ││
│  │ ├─ Social Security:    $186.00                              ││
│  │ ├─ Medicare:           $43.50                               ││
│  │ └─ Net Pay:            $2,970.50                            ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  PAY HISTORY                                                     │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Period           Pay Date    Gross     Taxes   Deductions Net││
│  │ Dec 16-31, 2024 | Jan 5      $3,200   $650     $450    $2,100││
│  │ Dec 1-15, 2024  | Dec 20     $3,200   $650     $450    $2,100││
│  │ Nov 16-30, 2024 | Dec 5      $3,100   $640     $400    $2,060││
│  │ [Show More]                                                  ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  PAYROLL CALENDAR 2025                                           │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Pay Frequency: Bi-weekly (every other Friday)                ││
│  │ Next Pay Date: Jan 20, 2025                                  ││
│  │ Next Period: Jan 16-31, 2025                                 ││
│  │                                                              ││
│  │ Upcoming Pay Dates:                                          ││
│  │ ├─ Jan 20 (current period ends Jan 15)                      ││
│  │ ├─ Feb 3 (Jan 16-31)                                        ││
│  │ ├─ Feb 17 (Feb 1-14, includes Presidents Day)               ││
│  │ └─ Mar 3 (Feb 15-28)                                        ││
│  │ [View Full Year Calendar]                                   ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  DIRECT DEPOSIT                                                  │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Account: Checking  |  Bank: Capital One 360                 ││
│  │ Account Number: ****0123  |  Routing: 011103093              ││
│  │ Status: Verified & Active                                    ││
│  │ [Change Direct Deposit]                                      ││
│  │                                                              ││
│  │ Secondary Account (optional):                               ││
│  │ None configured. [Add Secondary Account]                    ││
│  │                                                              ││
│  │ Direct Deposit Authorization (eSignature): ✓ Signed Jan 2025││
│  │ [Download Authorization]                                    ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

#### 1. Current Pay Stub Display
- **Pay Period Information**
  - Pay period start/end dates
  - Pay date
  - Pay frequency indicator (bi-weekly, monthly, etc.)
  - Status (paid, pending, draft)

- **Earnings Section**
  - Base salary
  - Bonus, overtime, commissions
  - Other pay types (shift differentials, etc.)
  - Gross pay total (highlighted)

- **Deductions Section**
  - Federal income tax
  - Social Security tax
  - Medicare tax
  - 401(k) contributions
  - Health insurance deductions
  - FSA/HSA deductions
  - Other deductions
  - Total deductions

- **Net Pay**
  - Net pay amount (most prominent)
  - Deposit method (direct deposit, check)
  - Account last 4 digits
  - Deposit confirmation status

- **Year-to-Date Totals**
  - YTD gross pay
  - YTD taxes by type
  - YTD benefits contributions
  - YTD net pay

#### 2. Pay Stub Actions
- **Download PDF**
  - Full pay stub PDF with all details
  - Formatted for printing
  - Secure download link
  - File naming convention: "Paystub_2025_01_20.pdf"

- **Email Pay Stub**
  - Send to employee email
  - Send to alternate email (if configured)
  - Include direct deposit confirmation in email

- **View Full Details**
  - Modal with complete breakdown
  - Itemized list of all deductions
  - Tax withholding details
  - Benefit elections impact on pay

#### 3. Pay History
- **Historical Pay Stubs**
  - List of past pay stubs
  - Date range filter (month, quarter, year)
  - Table with: period, pay date, gross, taxes, deductions, net
  - Sortable columns (by date, by amount)
  - Pagination (20 stubs per page)

- **Download Options**
  - Download individual pay stub
  - Bulk download (e.g., all 2024 pay stubs as ZIP)
  - Export to CSV (for spreadsheet analysis)

- **Stub Details Link**
  - Click any row to view full stub details
  - Comparison view (compare two periods)
  - Trend analysis (over time)

#### 4. Payroll Calendar
- **Calendar View**
  - Full year pay dates
  - Pay period dates (start/end)
  - Holiday considerations (paid holidays don't extend period)
  - Calendar format showing all pay dates

- **Pay Frequency Information**
  - Current pay frequency (weekly, bi-weekly, monthly, semi-monthly)
  - Next pay date
  - Current pay period end date
  - Days until next payment

- **Holiday & Closure Impact**
  - Note if upcoming pay date affected by holiday
  - Advance payment notifications (if paid early before holiday)
  - Holiday pay implications

#### 5. Direct Deposit Management
- **Current Account Information**
  - Account type (checking, savings)
  - Bank/financial institution
  - Last 4 digits of account (masked)
  - Routing number (last 4 digits, masked)
  - Account verification status
  - Active/inactive status

- **Change Direct Deposit**
  - Guided form to update account
  - Bank name/ABA routing number lookup
  - Account number (requires re-entry for verification)
  - Account type selector
  - Percentage allocation (for split deposits)
  - eSignature requirement

- **Split Deposits** (if enabled)
  - Primary account with percentage
  - Secondary account with percentage
  - Verification: percentages total 100%
  - Add/remove secondary account

- **Direct Deposit Authorization**
  - eSignature form for ACH authorization
  - Download signed authorization
  - Authorization effective date
  - Revoke authorization option

#### 6. Tax Withholding & W4
- **Current W4 Information**
  - Link to update W4
  - Filing status
  - Allowances/adjustments
  - Additional withholding amount
  - Effective date

- **Withholding Calculator**
  - Estimate taxes withheld
  - Adjust withholding scenario
  - Calculate impact on pay
  - Link to IRS withholding calculator

#### 7. Benefits Impact on Payroll
- **401(k) Contributions**
  - Current contribution percentage
  - Contribution amount per paycheck
  - YTD contributions
  - Employer match information
  - Link to 401(k) plan details

- **Health Insurance Deductions**
  - Monthly premium
  - Deduction per paycheck
  - Coverage type (self, self+family, etc.)
  - Link to benefits enrollment

- **FSA/HSA Contributions**
  - Election amount per year
  - Deduction per paycheck
  - YTD contributions
  - Remaining balance

### Data Model

```
PayStub {
  id: UUID
  employee_id: UUID (FK to Employee)
  pay_period_id: UUID (FK to PayPeriod)
  
  pay_period: {
    start_date: Date
    end_date: Date
    pay_date: Date
    pay_frequency: Enum (WEEKLY, BI_WEEKLY, SEMI_MONTHLY, MONTHLY)
  }
  
  earnings: {
    base_salary: Decimal
    bonus: Decimal (0 if none)
    overtime: Decimal (0 if none)
    shift_differential: Decimal (0 if none)
    other_pay: Decimal (0 if none)
    gross_pay: Decimal (sum of all earnings)
  }
  
  taxes: {
    federal_income_tax: Decimal
    social_security_tax: Decimal
    medicare_tax: Decimal
    state_income_tax: Decimal (0 if not applicable)
    local_income_tax: Decimal (0 if not applicable)
    total_taxes: Decimal
  }
  
  deductions: {
    pre_tax_401k: Decimal
    post_tax_401k: Decimal (roth)
    health_insurance: Decimal
    dental_insurance: Decimal
    vision_insurance: Decimal
    life_insurance: Decimal
    fsa: Decimal
    hsa: Decimal
    other_deductions: Decimal
    total_deductions: Decimal
  }
  
  net_pay: {
    amount: Decimal (gross - all deductions)
    payment_method: Enum (DIRECT_DEPOSIT, CHECK, CASH)
    account_last_4: String (masked)
    deposit_confirmation: Boolean
  }
  
  year_to_date: {
    gross_pay: Decimal
    total_taxes: Decimal
    total_deductions: Decimal
    net_pay: Decimal
    as_of_date: Date
  }
  
  status: Enum (DRAFT, PENDING, PAID, VOID, AMENDED)
  created_at: Timestamp
  updated_at: Timestamp
}

PayPeriod {
  id: UUID
  company_id: UUID
  start_date: Date
  end_date: Date
  pay_date: Date
  pay_frequency: Enum (WEEKLY, BI_WEEKLY, SEMI_MONTHLY, MONTHLY)
  period_number: Integer (1-52 for annual)
  fiscal_year: Integer
}

DirectDeposit {
  id: UUID
  employee_id: UUID (FK to Employee)
  account_type: Enum (CHECKING, SAVINGS)
  bank_name: String
  routing_number: String (encrypted)
  account_number: String (encrypted)
  account_last_4: String (visible)
  is_primary: Boolean
  allocation_percentage: Decimal (for split deposits)
  is_active: Boolean
  verified: Boolean
  verification_date: Date (nullable)
  authorization_signature: String (eSignature)
  authorization_date: Date
  created_at: Timestamp
  updated_at: Timestamp
}

W4Form {
  id: UUID
  employee_id: UUID (FK to Employee)
  filing_status: Enum (SINGLE, MARRIED_FILING_JOINTLY, MARRIED_FILING_SEPARATELY, HEAD_OF_HOUSEHOLD)
  allowances: Integer (0-14, deprecated in 2020+ but may still display)
  extra_withholding: Decimal (additional per-paycheck withholding)
  dependent_info: {
    number_of_dependents: Integer
    other_income: Decimal
  }
  effective_date: Date
  form_w4_version: String (2020, 2021, etc.)
  signed_date: Date
  created_at: Timestamp
  updated_at: Timestamp
}
```

### UI Components Required
- Card component: Pay stub summary
- Modal: Full pay stub details
- Table: Pay history list
- Download button with dropdown
- Email button
- Direct deposit form with bank lookup
- eSignature component
- Calendar: Payroll calendar
- Chart: YTD trends (bar chart of earnings over time)

### WCAG 2.2 AA Accessibility Requirements

#### Color & Contrast
- Net pay amount highlighted with 4.5:1 contrast
- Gross pay, taxes, deductions have 4.5:1 text contrast
- Table headers have 4.5:1 contrast
- Pay date/status information readable at 4.5:1
- Section headers (Earnings, Deductions) have 4.5:1 contrast

#### Keyboard Navigation
- Tab through all sections: current stub → history → calendar → direct deposit
- Pay history table keyboard navigable (arrow keys within table)
- Download buttons keyboard accessible
- Direct deposit form fields all keyboard operable
- Links to edit W4 keyboard accessible
- Skip links for jumping to sections

#### Screen Reader Support
- Page title: "Pay Stub & Payroll Information"
- Current pay stub section: `<section aria-label="Current Pay Stub for Jan 1-15, 2025">`
- Earnings section: `<table role="table" aria-label="Earnings breakdown"><thead><tr><th>Type</th><th>Amount</th></tr></thead>...`
- Gross pay prominent: `<div aria-label="Gross Pay: $3,650.00">`
- Net pay (main): `<div aria-label="Net Pay (Direct Deposit): $2,520.50" role="region">`
- Direct deposit account: `<div aria-label="Checking account ending in 0123 at Capital One 360, verified and active">`
- YTD totals: `<section aria-label="Year-to-Date Totals as of Jan 15, 2025">`
- Pay history table: `<table aria-label="Pay History (most recent 6 months)">`
- Payroll calendar: `<section aria-label="Payroll Calendar 2025, bi-weekly pay frequency">`
- All list items marked with proper hierarchy

#### Focus Management
- Current pay stub receives focus on page load
- When modal opens (full details), focus trapped in modal
- Escape key closes modal, focus returns to trigger
- Skip to content link available
- Tax withholding section easily reachable with skip link

#### Touch & Target Size
- Download button: 44×44 px minimum
- Email button: 44×44 px minimum
- View full details button: 44×44 px minimum
- Edit direct deposit button: 44×44 px
- Pay history row height: 50px minimum for touch
- Calendar date cells: 44×44 px minimum
- Form input fields: 40px min height

#### Error Handling & Validation
- Changing direct deposit: "This change will be effective with your next paycheck on [date]." (explains timing)
- Invalid routing number: "Routing number must be 9 digits. Yours is 6 digits." (specific)
- Unverified account: "Your account requires verification before deposits process. Check your account for micro-deposits." (explains next step)
- All errors have `role="alert"` and clear action items

#### Motion & Animation
- Expanding sections respect `prefers-reduced-motion` (instant open, no slide animation)
- Chart animations respect preference (display immediately)
- Modal open/close animations respect preference
- Smooth scrolling to sections respects preference

#### Semantic HTML & ARIA
- Pay stub section marked with `<section>`
- Earnings/Deductions/Taxes in `<table>` with proper `<thead>`, `<tbody>`
- YTD totals in `<dl>` (definition list)
- Pay history in `<table>` with sortable column headers
- Calendar as `<table>` with `role="grid"` for dates
- Form labels connected to inputs

### AI Integration Points

#### 1. Payroll Insights
- **Budget Planning**: Based on historical pay, forecast net pay for budget planning
  - "Based on last 6 months, your average net pay is $2,600/month"
- **Tax Optimization**: Suggest W4 adjustments to optimize withholding
  - "Your last 3 paychecks have $800+ refunded. Consider increasing allowances to get more take-home now."
- **Deduction Analysis**: Highlight deduction opportunities
  - "You're contributing $200/month to 401(k). With company match, that's $300 growing."

#### 2. Benefits Impact Modeling
- **Cost-Benefit Analysis**: Model impact of benefits changes
  - "Switching to PPO Gold will cost $150/month more but reduces your copays by $400/year."
- **Savings Goals**: Based on paycheck, suggest retirement contribution increase
  - "Increasing 401(k) by 1% ($37/check) won't significantly impact take-home."

#### 3. Direct Deposit Verification
- **Bank Lookup**: Auto-complete bank name from routing number
  - Enter routing "011103093" → auto-populate "Capital One 360"
- **Fraud Detection**: Flag suspicious account changes
  - "Direct deposit account changed from Bank A to Bank B. Confirm this change?"

#### 4. Tax Withholding Optimization
- **W4 Suggestions**: Based on filing status and dependents, suggest optimal withholding
  - "You claimed 1 allowance and withheld an extra $50/check. Based on income, recommend 2 allowances instead."
- **Estimated Tax**: Project year-end tax liability
  - "Based on YTD earnings, estimated annual tax liability is $5,600. Current withholding on track."

### Integrations & Dependencies

#### Internal Integrations
- **Payroll System**: Real-time pay stub data, direct deposit information
- **HRIS Core**: Employee data, tax withholding information
- **Benefits System**: Deduction amounts, benefits election data
- **401(k) Provider**: 401(k) contribution data and plan information
- **Finance/Accounting**: GL posting, cost center tracking
- **Notification System**: Email delivery of pay stubs, deposit notifications

#### External Integrations
- **Bank APIs**: Direct deposit verification (optional, via Plaid or similar)
- **Tax Software**: W4 form templates (IRS forms)
- **PDF Generation**: Pay stub PDF creation and formatting
- **eSignature Service**: eSignature for direct deposit authorization

### Edge Cases & Error States

#### 1. Pay Stub Variations
- **Off-Cycle Payroll**: Bonus or severance pay outside normal schedule
- **Void Pay Stubs**: Corrected paychecks (original voided, new issued)
- **Amended Pay Stubs**: Corrections after original pay (e.g., tax adjustment)

#### 2. Direct Deposit Issues
- **Pending Verification**: New account requires 1-2 micro-deposits for verification
  - Show message: "Your account is pending verification. Check your account for deposits of $0.XX"
- **Failed Deposit**: If ACH fails, notify employee and provide fallback (check payment)
- **Account Closure**: If employee closes account without updating, flag and prevent deposits

#### 3. Tax Withholding Issues
- **No Federal Tax**: Self-employed or contractor may have 0 federal withholding
- **Married w/ Multiple Jobs**: May need extra withholding to avoid underwithholding
- **Non-Resident Alien**: Different tax treatment and withholding rules

#### 4. Benefits Timing
- **Benefits Effective Date**: If benefits change mid-period, show pro-rated amounts
- **Open Enrollment Change**: If employee changes health plan, show partial period old/new
- **Life Event**: Births, deaths, marriages may affect benefits retroactively

#### 5. Data Privacy & Security
- **Masked Account Numbers**: Always show only last 4 digits
- **Encrypted Storage**: Routing and account numbers encrypted
- **Secure Download**: Pay stub PDFs require login, not accessible via direct link
- **Timeout**: Downloads expire after 1 hour

### Success Metrics & Testing Scenarios

#### Pay Stub Accuracy
- [ ] Current pay stub displays correctly
- [ ] All earnings calculated correctly
- [ ] All deductions calculated correctly
- [ ] Net pay = Gross - Deductions
- [ ] YTD totals match payroll system

#### Historical Data
- [ ] Previous pay stubs display correctly
- [ ] Pagination works (20 per page)
- [ ] Sort by date ascending/descending works
- [ ] Download individual stub creates correct PDF

#### Direct Deposit
- [ ] Current direct deposit account displays correctly
- [ ] Account verification status correct
- [ ] Change direct deposit form accepts valid input
- [ ] eSignature requirement enforced

#### Payroll Calendar
- [ ] All pay dates for year display correctly
- [ ] Current pay period highlighted
- [ ] Next pay date correct
- [ ] Holiday considerations reflected

#### Accessibility
- [ ] All form inputs keyboard navigable
- [ ] Screen reader announces pay amounts
- [ ] Direct deposit changes announced
- [ ] Error messages clear and actionable

---

## Screen 4.7: Tax Documents (W2, 1099, etc.)

### Purpose
Enable employees to access, download, and manage tax documents (W2, 1099, 1098-T) with integration to tax software, eSignature capabilities, and support contact options for tax questions.

### User Personas
- **Primary**: All Employees
- **Secondary**: Finance/Tax Department (for audit trails)

### Layout & Wireframe

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ←  Tax Documents                  [Tax Center]  [Support]       │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  2024 TAX DOCUMENTS                                              │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Available Documents:                                         ││
│  │                                                              ││
│  │ ☐ W2 (Wage & Tax Statement)                                ││
│  │   Issued: January 28, 2025  |  Employer: Acme Corp         ││
│  │   [View]  [Download PDF]  [Download to Tax Software]       ││
│  │   [Print]  [Email]        [Verify (eSignature)]            ││
│  │                                                              ││
│  │ ○ 1099 (Miscellaneous Income)                              ││
│  │   Status: Not Applicable (W2 only income)                   ││
│  │                                                              ││
│  │ ○ 1098-T (Qualified Education Expenses)                    ││
│  │   Status: Not Applicable                                    ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  PRIOR YEARS                                                     │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ 2023 Tax Documents                                           ││
│  │ └─ W2: Issued Jan 30, 2024  [View]  [Download]             ││
│  │                                                              ││
│  │ 2022 Tax Documents                                           ││
│  │ └─ W2: Issued Jan 28, 2023  [View]  [Download]             ││
│  │                                                              ││
│  │ 2021 Tax Documents                                           ││
│  │ └─ W2: Issued Jan 31, 2022  [View]  [Download]             ││
│  │                                                              ││
│  │ [Show More Years]                                            ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  DOWNLOAD TO TAX SOFTWARE                                        │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Supported Software:                                          ││
│  │ [TurboTax]  [H&R Block]  [TaxAct]  [Other Software]        ││
│  │                                                              ││
│  │ Select year: [2024 ▼]                                       ││
│  │ Choose software: [TurboTax ▼]                               ││
│  │                                                              ││
│  │ [Download IIF or XML file for import]                       ││
│  │ Or continue to [Link to TurboTax] (auto-import)             ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  TAX INFORMATION SUMMARY (2024)                                  │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Box 1 (Wages, tips, other compensation):  $85,450          ││
│  │ Box 2 (Federal income tax withheld):       $10,250          ││
│  │ Box 3 (Social Security wages):             $85,450          ││
│  │ Box 4 (Social Security tax withheld):      $5,298           ││
│  │ Box 5 (Medicare wages and tips):           $85,450          ││
│  │ Box 6 (Medicare tax withheld):             $1,239           ││
│  │                                                              ││
│  │ [View Full Box-by-Box Details]                              ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  DOCUMENT VERIFICATION                                           │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Need to verify your documents for a loan or other purpose? ││
│  │ [Request Verification Letter]                               ││
│  │ (Requires eSignature and ID verification)                   ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  QUESTIONS ABOUT YOUR TAX DOCUMENTS?                             │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Contact Payroll/Tax Department: [payroll@company.com]       ││
│  │ [Email Question]  [Schedule Callback]  [FAQ]                ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

#### 1. Current Year Tax Documents
- **W2 (Wage & Tax Statement)**
  - Issued date and employer name
  - Status: Available, Pending, Not Applicable
  - Quick actions: View, Download PDF, Download to Tax Software, Print, Email
  - Verification capability for loans

- **1099 Forms** (if applicable)
  - 1099-NEC: Non-employee compensation (contractors)
  - 1099-MISC: Miscellaneous income
  - Status indicator: Issued, Pending, Not Applicable
  - Quick actions for each form

- **1098-T** (if applicable)
  - Qualified education expense statement
  - Status: Issued, Pending, Not Applicable
  - Educational institution details

#### 2. Document Viewer
- **W2 View**
  - Full W2 form display (simulated)
  - All required boxes (1-20)
  - Employer EIN and address
  - Employee SSN (partially masked except last 4)
  - Zoom/pan functionality for reading
  - Print-friendly formatting

- **Box Details**
  - Box-by-box breakdown of W2 fields
  - Explanations of key boxes (wages, taxes, SSN withholding)
  - Link to IRS box explanations

- **Form Comparison**
  - Compare W2 from current year vs. prior years
  - Show changes in income, taxes, deductions

#### 3. Download & Export Options
- **PDF Download**
  - Full W2/1099 form as PDF
  - Multiple copies downloadable
  - Formatted for printing or filing

- **Tax Software Integration**
  - TurboTax direct link (OAuth)
  - H&R Block direct link
  - TaxAct direct link
  - Download IIF or XML for import
  - Step-by-step import instructions for each software

- **Email Delivery**
  - Send tax document to employee email
  - Send to alternate email if needed
  - Resend option

#### 4. Prior Year Documents
- **Historical Access**
  - List of prior years (2023, 2022, 2021, etc.)
  - Expandable for each year showing available documents
  - Download options for each prior year

- **Archive Access**
  - Documents from 7+ years ago may require archival request
  - Submit request for historical document (processed in 5-10 business days)

#### 5. Tax Software Download
- **Software Selection**
  - Dropdown to select tax software
  - Supported software list
  - Instructions for each software
  - Link to software provider if need to purchase

- **File Format Options**
  - IIF format (for QuickBooks, TurboTax)
  - XML format (for some tax software)
  - PDF format (for filing/record keeping)

- **Auto-Import Option**
  - Direct link to TurboTax/H&R Block auto-import
  - OAuth authentication
  - Pre-fills forms automatically

#### 6. Tax Information Summary
- **Key W2 Fields Display**
  - Box 1: Wages, tips, other compensation
  - Box 2: Federal income tax withheld
  - Box 3: Social Security wages
  - Box 4: Social Security tax withheld
  - Box 5: Medicare wages
  - Box 6: Medicare tax withheld
  - Box 12a-d: Other deductions/benefits (if any)

- **Year-over-Year Comparison**
  - Current year vs. prior year totals
  - Income growth/change
  - Tax withholding comparison

#### 7. Document Verification
- **Verification Letter Request**
  - For mortgage, loan, or other verification
  - eSignature requirement (identity verification)
  - Processing timeline (1-2 business days)
  - Download verification letter as PDF

- **Verification Letter Details**
  - Employee name, ID, employment status
  - Income verification (Box 1 amount)
  - Employment dates
  - Employer letterhead and signature

#### 8. Support & Help
- **FAQ Section**
  - Common tax document questions
  - W2 vs 1099 explanation
  - How to use tax software integration
  - Document retention recommendations
  - IRS links and resources

- **Contact Payroll/Tax Department**
  - Email contact form
  - Email address to contact directly
  - Callback request option
  - Expected response time (24-48 hours)

### Data Model

```
TaxDocument {
  id: UUID
  employee_id: UUID (FK to Employee)
  document_type: Enum (W2, 1099_NEC, 1099_MISC, 1098_T, 1098_Q, OTHER)
  tax_year: Integer
  issued_date: Date
  status: Enum (DRAFT, ISSUED, AVAILABLE, PENDING, ARCHIVED)
  
  # W2-specific fields
  w2_data: {
    employer_ein: String (masked)
    employer_name: String
    employer_address: String
    employee_ssn: String (masked, show only last 4)
    
    box_1_wages: Decimal
    box_2_federal_tax_withheld: Decimal
    box_3_ss_wages: Decimal
    box_4_ss_tax_withheld: Decimal
    box_5_medicare_wages: Decimal
    box_6_medicare_tax_withheld: Decimal
    box_7_ss_tips: Decimal (nullable)
    box_8_allocated_tips: Decimal (nullable)
    box_12: Array<{ code: String, amount: Decimal }>
    box_14: Array<{ description: String, amount: Decimal }>
    
    is_corrected_w2: Boolean
    original_w2_id: UUID (if corrected, reference to original)
  }
  
  # 1099-specific fields
  form_1099_data: {
    payer_ein: String (masked)
    payer_name: String
    box_1_miscellaneous_income: Decimal (nullable)
    box_2_federal_income_tax: Decimal (nullable)
    # Additional 1099 boxes as applicable
  }
  
  document_url: String (cloud storage URL)
  document_file_size: Integer (bytes)
  checksum: String (for security/verification)
  
  verification_status: Enum (NOT_VERIFIED, VERIFIED, VERIFICATION_REQUESTED)
  verification_signatures: Array<{
    signer_name: String
    signature_date: Date
    verification_type: String (bank_statement, passport, etc.)
  }>
  
  created_at: Timestamp
  updated_at: Timestamp
}

VerificationLetter {
  id: UUID
  employee_id: UUID (FK to Employee)
  requested_date: Date
  requested_by_employee: Boolean
  purpose: String (mortgage, loan, visa, other)
  
  letter_content: {
    verification_type: String
    employee_name: String
    employment_status: String
    income_amount: Decimal (from W2 Box 1)
    employment_dates: { start_date: Date, end_date: Date (nullable) }
    company_name: String
    company_address: String
    letter_date: Date
  }
  
  status: Enum (DRAFT, SIGNED, ISSUED, ARCHIVED)
  esignature: {
    signer_name: String
    signature_date: Date
    digital_signature: String
  }
  
  document_url: String
  issued_date: Date (nullable)
  
  created_at: Timestamp
  updated_at: Timestamp
}

TaxSoftwareIntegration {
  id: UUID
  employee_id: UUID (FK to Employee)
  software_name: Enum (TURBOTAX, HR_BLOCK, TAXACT, OTHER)
  authorization_token: String (encrypted, OAuth token)
  auth_expiration_date: Date (nullable)
  last_sync_date: Date (nullable)
  sync_status: Enum (CONNECTED, EXPIRED, FAILED)
}
```

### UI Components Required
- Card component: Document summary card
- Modal: Document viewer (W2 form simulation)
- Modal: Verification letter request form
- Button group: Download options (PDF, Software, Email)
- Table: Prior years list
- Expandable section: Prior year documents
- Dropdown: Software selection
- eSignature component
- FAQ accordion

### WCAG 2.2 AA Accessibility Requirements

#### Color & Contrast
- Document status badges have text labels + color (not color alone)
- W2 form numbers (Box 1, Box 2, etc.) have 4.5:1 contrast
- Dollar amounts in summary have 4.5:1 contrast with background
- Links to tax software have distinct color
- Status indicators (Available, Pending, Not Applicable) readable

#### Keyboard Navigation
- Tab through document list
- Arrow keys navigate between documents
- Enter to view/download document
- Download options (PDF, Software, Email) keyboard accessible
- Prior years expandable with keyboard (Enter/Space)
- Form inputs in verification letter all keyboard operable
- Skip links for jumping to sections

#### Screen Reader Support
- Page title: "Tax Documents"
- Current year section: `<section aria-label="2024 Tax Documents">`
- Each document card: `<div role="region" aria-label="W2, Wage and Tax Statement, issued January 28, 2025">`
- Document status: `<span aria-label="Available">✓</span> W2` (not color alone)
- Summary amounts: `<div aria-label="Box 1 Wages, tips, other compensation: $85,450">`
- Prior years list: `<details aria-label="2023 Tax Documents"><summary>2023...</summary>...</details>`
- Software selection: `<label for="software">Choose tax software:</label><select id="software">...`
- Download buttons: `<a href="..." aria-label="Download 2024 W2 as PDF">Download PDF</a>`
- Verification letter form: `<fieldset><legend>Request Verification Letter</legend>...`

#### Focus Management
- W2 document receives focus on page load
- Document viewer modal traps focus (Escape to close)
- Download menu opens with focus on first option
- Verification letter form focused when modal opens
- Skip to main content link available

#### Touch & Target Size
- Document cards: 60px minimum height for touch
- Download button: 44×44 px minimum
- View/Download/Email buttons: 44×44 px each
- Prior years expand button: 44×44 px
- Verification request button: 44×44 px
- Contact button: 44×44 px

#### Error Handling & Validation
- Document not available: "Your 2024 W2 is being processed. Check back after Jan 30." (explains timeline)
- Verification letter request form missing purpose: "Please select the purpose for this verification letter." (clear requirement)
- eSignature verification failed: "Signature verification failed. Please try again." (explain next step)
- All errors have `role="alert"` and clear instructions

#### Motion & Animation
- Document viewer opening respects `prefers-reduced-motion` (instant display)
- Prior year expansion respects preference (no animation)
- Download progress respects preference
- Form transitions instant

#### Semantic HTML & ARIA
- Proper heading hierarchy: `<h1>` for page, `<h2>` for sections
- Document list as `<ul>` with `<li>` for each document
- Prior years as `<details>`/`<summary>` structure
- Tax summary in `<table>` with `<thead>`, `<tbody>`
- Form inputs with associated `<label>` tags
- Verification letter as `<form>`

### AI Integration Points

#### 1. Document Summarization
- **Key Takeaways**: "Your 2024 W2 shows income of $85,450 and federal tax withheld of $10,250. Tax refund estimate: $1,500-2,000."
- **Tax Efficiency**: "Your total tax withholding ($17,000) is slightly higher than historical average ($16,500). Consider adjusting W4 for higher take-home."

#### 2. Tax Planning Insights
- **Income Trends**: "Your income increased 8% from 2023 to 2024. At this rate, 2025 income likely ~$92,000."
- **Withholding Analysis**: "Based on W2 trends, recommended federal withholding adjustment to save $50/paycheck."

#### 3. Verification Letter Automation
- **Quick Generation**: Auto-populate verification letter with W2 data
- **Purpose-Specific Templates**: Customize letter based on stated purpose (mortgage, visa, etc.)

#### 4. Tax Resource Recommendations
- **Software Recommendation**: Based on income complexity, recommend TurboTax vs. H&R Block
  - "Simple W2-only income? H&R Block Free. Complex? TurboTax Premier."
- **Deduction Reminders**: Suggest common deductions based on income level
  - "With $85K income, consider estimated tax deductions, IRA contributions, HSA."

### Integrations & Dependencies

#### Internal Integrations
- **Payroll System**: Pull W2 data directly from payroll
- **HRIS Core**: Employee data for verification letters
- **Document Management**: Store and version tax documents
- **Notification System**: Email delivery of documents, notifications of availability
- **eSignature Service**: Signature capture for verification letters

#### External Integrations
- **Tax Software APIs**: TurboTax, H&R Block, TaxAct integrations (OAuth)
- **IRS Resources**: Links to IRS W2 box explanations, tax publications
- **Document Storage**: Cloud storage (S3, Azure Blob) for PDF files

### Edge Cases & Error States

#### 1. Corrected Tax Documents
- **Amended W2**: If W2 is corrected, show "Corrected W2-c" with reference to original
- **Multiple Corrections**: Show timeline of corrections and which is most current

#### 2. Non-US Employees
- **Non-Resident Alien**: Different tax form (Form 8288, Form 8840)
- **Visa Status**: Display appropriate tax documents for visa type
- **ITIN vs. SSN**: Some employees may have ITIN instead of SSN

#### 3. Missing Documents
- **Pending W2**: "Your 2024 W2 is being processed. Expected availability: January 30, 2025."
- **Not Applicable**: "You did not receive a 1099 for 2024 (W2 employee only)."

#### 4. Multi-State Employment
- **State Tax Documents**: If worked in multiple states, separate state tax forms
- **State W2 Copies**: Show Box 19 (state wages) and corresponding state documents

#### 5. Security & Privacy
- **Masked Information**: SSN shown only as last 4 digits
- **Secure Download**: Links expire after 30 days or 5 downloads
- **Audit Trail**: Log all document downloads, views, email sends
- **Encryption**: Documents encrypted at rest and in transit

### Success Metrics & Testing Scenarios

#### Document Availability
- [ ] Current year W2 displays when issued
- [ ] Prior year documents accessible and organized
- [ ] Status (Issued, Pending, Not Applicable) correct
- [ ] Multiple copies of same document available

#### Download & Export
- [ ] PDF download creates correct file
- [ ] Download to TurboTax/H&R Block works (OAuth flow)
- [ ] IIF/XML export format correct for tax software
- [ ] Email delivery sends to correct address

#### Document Viewer
- [ ] W2 form displays all boxes correctly
- [ ] Box values match payroll data
- [ ] Prior years display with historical values
- [ ] Form readable and printable

#### Verification Letter
- [ ] Request form accepts all required fields
- [ ] Letter generates with correct data
- [ ] eSignature capture works
- [ ] Letter delivers as PDF within SLA

#### Accessibility
- [ ] All document links keyboard accessible
- [ ] Download menu keyboard navigable
- [ ] Screen reader announces document status
- [ ] Form labels connected to inputs
- [ ] Prior year expansion works with keyboard

---

## Screen 4.8: Documents & Records

### Purpose
Provide centralized repository for employee employment records and documents including offer letters, contracts, certifications, policy acknowledgments, I-9 verification, direct deposit authorization, emergency contacts, and personal document uploads with signature workflow support.

### User Personas
- **Primary**: All Employees
- **Secondary**: HR Team (record management), Managers (access to reports' documents if allowed)

### Layout & Wireframe

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ←  Documents & Records           [Upload]  [My Signed]  [Help]  │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  DOCUMENT LIBRARY (24 documents)                                 │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ EMPLOYMENT DOCUMENTS (7)                                     ││
│  │ ├─ ✓ Job Offer Letter                                       ││
│  │ │  Signed: Jan 5, 2024  |  Status: Signed                   ││
│  │ │  [View]  [Download]  [Email]  [Request New Signature]     ││
│  │ │                                                           ││
│  │ ├─ ✓ Employment Contract (At-Will Statement)                ││
│  │ │  Signed: Jan 5, 2024  |  Status: Signed                   ││
│  │ │  [View]  [Download]  [Email]                              ││
│  │ │                                                           ││
│  │ ├─ ○ Non-Compete/NDA Agreement                              ││
│  │ │  Status: Pending Your Signature (expires Jan 25)          ││
│  │ │  [Sign Now]  [View]  [Download]  [Decline]               ││
│  │ │                                                           ││
│  │ ├─ ✓ Employment Agreement (Startup Options)                 ││
│  │ │  Signed: Jan 5, 2024  |  Status: Signed                   ││
│  │ │  [View]  [Download]                                       ││
│  │ │                                                           ││
│  │ ├─ ✓ Confidentiality Agreement                              ││
│  │ │  Signed: Jan 10, 2024  |  Status: Signed                  ││
│  │ │  [View]  [Download]                                       ││
│  │ │                                                           ││
│  │ ├─ ○ I-9 Verification (Employment Eligibility)              ││
│  │ │  Status: Action Needed (Document expires May 1, 2025)     ││
│  │ │  [Complete Now]  [View]  [Documents Status]               ││
│  │ │  Missing: Copy of passport/green card                     ││
│  │ │                                                           ││
│  │ ├─ ✓ Direct Deposit Authorization                           ││
│  │ │  Signed: Jan 3, 2024  |  Status: Signed                   ││
│  │ │  [View]  [Download]                                       ││
│  │ └─                                                           ││
│  │                                                              ││
│  │ POLICY & COMPLIANCE (8)                                      ││
│  │ ├─ ✓ Company Handbook Acknowledgment                        ││
│  │ │  Signed: Jan 5, 2024  |  Status: Signed                   ││
│  │ │  [View]  [Download]                                       ││
│  │ │                                                           ││
│  │ ├─ ✓ Anti-Harassment & Discrimination Policy                ││
│  │ │  Signed: Jan 5, 2024  |  Status: Signed                   ││
│  │ │  [View]  [Download]                                       ││
│  │ │                                                           ││
│  │ ├─ ✓ Code of Conduct                                        ││
│  │ │  Signed: Jan 5, 2024  |  Status: Signed                   ││
│  │ │  [View]  [Download]                                       ││
│  │ │                                                           ││
│  │ ├─ ✓ Remote Work Policy                                     ││
│  │ │  Signed: Jan 5, 2024  |  Status: Signed                   ││
│  │ │  [View]  [Download]                                       ││
│  │ │                                                           ││
│  │ ├─ ✓ Information Security Policy                            ││
│  │ │  Signed: Jul 15, 2024  |  Status: Signed                  ││
│  │ │  [View]  [Download]  [Renew Signature]                    ││
│  │ │                                                           ││
│  │ ├─ ○ Arbitration Agreement                                  ││
│  │ │  Status: Pending Your Signature (expires Jan 31)          ││
│  │ │  [Sign Now]  [View]  [Download]  [Decline]               ││
│  │ │                                                           ││
│  │ ├─ ✓ Data Privacy (GDPR) Acknowledgment                     ││
│  │ │  Signed: Jan 5, 2024  |  Status: Signed                   ││
│  │ │  [View]  [Download]                                       ││
│  │ │                                                           ││
│  │ └─ Training Acknowledgments (3 trainings completed)         ││
│  │                                                              ││
│  │ CERTIFICATIONS & LICENSES (5)                                ││
│  │ ├─ ✓ PMP Certification (Project Management Professional)   ││
│  │ │  Issue Date: Mar 15, 2022  |  Expires: Mar 14, 2025       ││
│  │ │  License #: PMC-12345  |  Issuer: PMI                     ││
│  │ │  [View]  [Download]  [Set Expiration Reminder]            ││
│  │ │                                                           ││
│  │ ├─ ✓ AWS Certified Solutions Architect                      ││
│  │ │  Issue Date: Jul 8, 2023  |  Expires: Jul 8, 2026         ││
│  │ │  [View]  [Download]  [Set Expiration Reminder]            ││
│  │ │                                                           ││
│  │ ├─ ⚠ First Aid/CPR Certification                            ││
│  │ │  Issue Date: Jan 15, 2022  |  EXPIRES SOON: Feb 1, 2025   ││
│  │ │  [View]  [Download]  [Renew]                              ││
│  │ │                                                           ││
│  │ ├─ ✓ Driver's License (Commercial)                          ││
│  │ │  Issue Date: Apr 1, 2018  |  Expires: Mar 31, 2026        ││
│  │ │  License #: C123456  |  State: CA                         ││
│  │ │  [View]  [Download]                                       ││
│  │ │                                                           ││
│  │ └─ ✓ CPA License                                            ││
│  │    Issue Date: Jun 1, 2019  |  Expires: May 31, 2025        ││
│  │    License #: CA-CPA-789  |  State: CA                      ││
│  │    [View]  [Download]  [Renew]                              ││
│  │                                                              ││
│  │ EMERGENCY CONTACTS (1)                                       ││
│  │ ├─ ✓ Emergency Contact Form                                 ││
│  │ │  Last Updated: Jan 10, 2024                               ││
│  │ │  [View]  [Update]  [Download]                             ││
│  │ │  Contact 1: Jane Doe (Spouse) - (555) 123-4567            ││
│  │ │  Contact 2: John Doe (Father) - (555) 234-5678            ││
│  │ │                                                           ││
│  │ │ [+ Add Personal Document]                                 ││
│  │ │                                                           ││
│  │ └─                                                           ││
│  │                                                              ││
│  │ PERSONAL DOCUMENTS (3)                                       ││
│  │ ├─ ○ 2024 Performance Review                                ││
│  │ │  Uploaded: Jan 10, 2024  |  Status: Archived              ││
│  │ │  [View]  [Download]  [Delete]                             ││
│  │ │                                                           ││
│  │ ├─ ○ Development Plan                                       ││
│  │ │  Uploaded: Jan 8, 2024  |  Status: Active                 ││
│  │ │  [View]  [Download]  [Update]  [Archive]                  ││
│  │ │                                                           ││
│  │ └─ ○ Resume (Internal Use Only)                             ││
│  │    Uploaded: Mar 15, 2023  |  Status: Active                ││
│  │    [View]  [Download]  [Update]  [Archive]                  ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  BULK ACTIONS                                                    │
│  [Download All Documents]  [Request New Signature]  [Export]     │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

#### 1. Employment Documents Section
- **Job Offer Letter**
  - Date issued, offer details
  - Signed date and signature status
  - View full offer document
  - Download and email capabilities

- **Employment Agreements**
  - At-will employment statement
  - Equity/option agreements
  - Stock purchase agreements
  - Consultation/referral agreements
  - Signed date, signature status

- **Confidentiality/IP Agreements**
  - Non-disclosure agreements (NDA)
  - Non-compete agreements
  - IP assignment agreements
  - Signed status and dates

- **I-9 Employment Eligibility**
  - Current verification status
  - Document requirements checklist
  - Expiration date tracking
  - Action needed notifications
  - Link to upload supporting documents (passport, green card, etc.)

- **Direct Deposit Authorization**
  - ACH authorization form
  - Signed date and status
  - Revoke option if needed

#### 2. Policy & Compliance Section
- **Company Handbook Acknowledgment**
  - Acknowledgment of receipt
  - Signed date
  - Update when handbook revised (requires new signature)

- **Anti-Harassment/Discrimination Policy**
  - Acknowledgment of policy
  - Annual renewal requirement
  - Signed date

- **Code of Conduct**
  - Company values and ethical standards
  - Signed acknowledgment
  - Refresh annually

- **Remote Work Policy** (if applicable)
  - Work-from-home agreement
  - Equipment/security requirements
  - Signed acknowledgment

- **Information Security Policy**
  - Password requirements, device security, data handling
  - Annual training completion + acknowledgment
  - Due for renewal after 1 year

- **Arbitration Agreement**
  - Dispute resolution terms
  - Signature pending with deadline
  - Option to decline (with HR notification)

- **Privacy & Data Protection**
  - GDPR acknowledgment (for EU employees)
  - Data privacy policy acknowledgment
  - Signed date

- **Training Acknowledgments**
  - List of completed trainings (Harassment training, Mandatory training, etc.)
  - Completion date
  - Expiration/renewal date

#### 3. Certifications & Licenses Section
- **Professional Certifications**
  - PMP, AWS, Google Cloud, etc.
  - Issue date, expiration date
  - License/certificate number
  - Issuing organization
  - Status: Valid, Expiring Soon, Expired
  - Renewal reminders

- **Required Licenses**
  - Driver's license (for driving jobs)
  - Nursing licenses, legal licenses, etc.
  - Status and expiration tracking
  - Renewal notifications

- **Expiration Tracking**
  - Visual indicator: Valid (green), Expiring Soon (yellow), Expired (red)
  - Automatic reminders 30/60 days before expiration
  - Renewal request workflow

#### 4. Emergency Contacts
- **Emergency Contact Form**
  - Primary contact name, relationship, phone
  - Secondary contact name, relationship, phone
  - Additional contacts (optional)
  - Last updated date
  - Update workflow

- **Contact Usage Policy**
  - Explanation of when contacts are used
  - Privacy statement
  - Permission to share with other employees (for team identification)

#### 5. Personal Documents Section
- **Employee Upload Area**
  - Drag-drop upload interface
  - Supported formats: PDF, Word, Excel, image
  - Max file size: 25MB
  - Version history (upload date, file size)

- **Document Management**
  - Archive vs. Active document status
  - Delete old documents
  - Add descriptions/tags
  - Share with manager (optional)

- **Common Personal Documents**
  - Performance reviews (historical)
  - Development plans
  - Resume (internal use)
  - Certifications/diplomas
  - References/testimonials

#### 6. Document Signature Workflow
- **Pending Signatures**
  - List of documents awaiting signature
  - Expiration date for signing
  - One-click "Sign Now" button
  - Email reminders

- **eSignature Process**
  - Document preview
  - Signature capture (draw, type, or upload image)
  - Identity verification (if required)
  - Confirmation after signing
  - Download signed copy

- **Signature History**
  - List of all signed documents
  - Sign date, signer name, IP address
  - Audit trail for compliance

- **Signature Renewal**
  - For policies requiring annual renewal
  - Quick re-signature workflow
  - Historical record of all signatures

#### 7. Expiration Tracking & Alerts
- **Upcoming Expirations**
  - I-9 document expiration
  - Certification/license expiration
  - Policy signature renewal due
  - Proactive notifications 30/60 days before

- **Expired Documents**
  - Visual indicators (red badge)
  - Action required notification
  - Renewal instructions

#### 8. Bulk Operations
- **Download All Documents**
  - ZIP of all documents
  - Organized by category
  - Encrypted/secure download link

- **Request New Signature**
  - Batch request signatures on all policies
  - Useful for policy updates
  - Multi-document signing workflow

- **Export & Archive**
  - Export document list as CSV
  - Archive old documents
  - Retention policy compliance

### Data Model

```
EmploymentDocument {
  id: UUID
  employee_id: UUID (FK to Employee)
  document_type: Enum (OFFER_LETTER, EMPLOYMENT_AGREEMENT, NDA, EMPLOYMENT_CONTRACT, I9, DIRECT_DEPOSIT, HANDBOOK_ACK, POLICY_ACK, CODE_OF_CONDUCT, ARBITRATION_AGREEMENT, PRIVACY_POLICY, CERTIFICATION, LICENSE, EMERGENCY_CONTACT, PERSONAL_UPLOAD)
  
  title: String
  description: String (optional)
  category: Enum (EMPLOYMENT, POLICY_COMPLIANCE, CERTIFICATIONS, EMERGENCY_CONTACTS, PERSONAL)
  
  document_url: String (cloud storage URL)
  file_name: String
  file_size: Integer (bytes)
  file_type: String (pdf, docx, jpg, etc.)
  
  issue_date: Date (nullable)
  expiration_date: Date (nullable)
  
  signature_required: Boolean
  signature_status: Enum (UNSIGNED, PENDING, SIGNED, DECLINED, EXPIRED)
  signature_deadline: Date (nullable)
  
  signatures: Array<Signature {
    id: UUID
    signer_id: UUID
    signer_name: String
    signature_image: String (base64)
    signed_date: Timestamp
    signature_method: Enum (DRAW, TYPE, UPLOAD_IMAGE)
    ip_address: String (for audit trail)
  }>
  
  license_number: String (nullable, for certifications/licenses)
  issuing_organization: String (nullable)
  issuing_state: String (nullable)
  
  renewal_required: Boolean (nullable)
  renewal_date: Date (nullable)
  renewal_frequency_months: Integer (nullable)
  
  tags: Array<String> (searchable tags)
  status: Enum (ACTIVE, ARCHIVED, DELETED)
  visibility: Enum (PRIVATE_EMPLOYEE_ONLY, MANAGER_VISIBLE, HR_ONLY, COMPANY_WIDE)
  
  version: Integer (for document versioning)
  previous_version_id: UUID (nullable, references prior version)
  
  created_at: Timestamp
  updated_at: Timestamp
}

Signature {
  id: UUID
  document_id: UUID (FK to EmploymentDocument)
  signer_id: UUID (FK to Employee)
  signer_name: String
  signature_image: String (base64 encoded image)
  signature_date: Timestamp
  signature_method: Enum (DRAW, TYPE, UPLOAD_IMAGE)
  ip_address: String
  user_agent: String
  
  created_at: Timestamp
}

EmergencyContact {
  id: UUID
  employee_id: UUID (FK to Employee)
  
  contacts: Array<Contact {
    id: UUID
    name: String (required)
    relationship: Enum (SPOUSE, CHILD, PARENT, SIBLING, FRIEND, COWORKER, OTHER)
    phone_number: String (required)
    email: String (optional)
    address: String (optional)
    priority: Integer (1 = primary, 2 = secondary, etc.)
  }>
  
  last_updated: Date
  updated_by_employee_id: UUID
  
  created_at: Timestamp
  updated_at: Timestamp
}

I9Document {
  id: UUID
  employee_id: UUID (FK to Employee)
  
  employment_eligibility: {
    status: Enum (NOT_STARTED, IN_PROGRESS, VERIFIED, EXPIRED, RE_VERIFICATION_REQUIRED)
    form_completion_date: Date (nullable)
    verification_date: Date (nullable)
    reverification_date: Date (nullable)
    
    document_list_a: Array<{
      document_type: String
      document_number: String
      expiration_date: Date (nullable)
      status: Enum (SUBMITTED, VERIFIED, PENDING, EXPIRED)
    }>
    
    document_list_bc: Array<{
      document_type: String
      document_number: String
      expiration_date: Date (nullable)
      status: Enum (SUBMITTED, VERIFIED, PENDING, EXPIRED)
    }>
  }
  
  supporting_documents: Array<{
    id: UUID
    document_type: String (Passport, Green Card, Driver's License, Birth Certificate, etc.)
    file_url: String
    file_name: String
    uploaded_date: Date
    status: Enum (PENDING_REVIEW, APPROVED, REJECTED, PENDING_RESUBMISSION)
  }>
  
  i9_form_url: String
  form_completion_date: Date (nullable)
  reverification_required_date: Date (nullable)
  
  status: Enum (NOT_STARTED, IN_PROGRESS, COMPLETED, PENDING_EMPLOYEE_ACTION, EXPIRED)
  
  created_at: Timestamp
  updated_at: Timestamp
}

CertificationLicense {
  id: UUID
  employee_id: UUID (FK to Employee)
  
  certification_name: String
  issuing_organization: String
  license_number: String (nullable)
  issue_date: Date
  expiration_date: Date (nullable)
  
  credential_url: String (nullable, link to online verification)
  document_url: String (copy of certificate)
  
  renewal_date: Date (nullable)
  renewal_frequency_months: Integer (nullable)
  is_required_for_role: Boolean
  
  status: Enum (VALID, EXPIRING_SOON, EXPIRED, RENEWAL_REQUIRED)
  
  created_at: Timestamp
  updated_at: Timestamp
}
```

### UI Components Required
- Expandable section/accordion: Document categories
- Card component: Document card with actions
- Modal: Document viewer (PDF, image, etc.)
- Modal: Signature capture
- Modal: Emergency contact form
- File upload: Drag-drop personal document upload
- Badge: Status indicator (Signed, Pending, Expired, etc.)
- Checkbox: Bulk selection
- Button group: Actions (View, Download, Sign, Delete, etc.)
- Notification banner: Action needed alerts
- Calendar/date picker: Expiration date
- List: Emergency contacts

### WCAG 2.2 AA Accessibility Requirements

#### Color & Contrast
- Status badges (Signed, Pending, Expired) have text labels + color
- Expiration warnings (yellow, red) have text labels
- Links to documents have distinct color
- All text has 4.5:1 contrast minimum
- Section headers readable at 4.5:1

#### Keyboard Navigation
- Tab through all documents and actions
- Arrow keys navigate document list
- Enter to view/download document
- Expandable sections toggle with Enter/Space
- Signature capture field keyboard accessible
- Emergency contact form all keyboard operable
- Bulk checkbox selection keyboard accessible
- Skip links for major sections

#### Screen Reader Support
- Page title: "Documents & Records"
- Each category section: `<section aria-label="Employment Documents (7 documents)">`
- Document card: `<div role="region" aria-label="Job Offer Letter, signed Jan 5, 2024">`
- Status badge: `<span aria-label="Signed">✓</span>` (text + visual)
- Expiration warning: `<span aria-label="Expires soon: Feb 1, 2025">⚠</span>`
- Action needed: `<div aria-live="assertive" aria-label="I-9 document requires action. Passport copy needed. Expires May 1, 2025.">`
- Document list: `<ul aria-label="7 employment documents">`
- Certification expiration: `<div aria-label="First Aid/CPR Certification, expires Feb 1, 2025 (expires soon)">`
- Emergency contacts: `<section aria-label="Emergency Contacts (2 contacts)">`
- Signature pending: `<div aria-live="polite" aria-label="Pending your signature: Non-Compete Agreement. Sign by Jan 25.">`

#### Focus Management
- Employment documents section receives focus on page load
- When document is signed, focus returns to document card
- Modal for signature capture traps focus (Escape closes)
- After uploading personal document, focus returns to upload area
- Skip to main content link available

#### Touch & Target Size
- Expandable section buttons: 44×44 px minimum
- Document action buttons (View, Download, Sign, Delete): 44×44 px
- Checkbox for bulk selection: 44×44 px
- Signature field: min 200×100 px for drawing
- File upload area: 120×120 px minimum
- Emergency contact action buttons: 44×44 px
- Expiration date button: 44×44 px

#### Error Handling & Validation
- Required field missing: "Certificate number is required for certifications." (specific)
- Expiration date invalid: "Expiration date cannot be in the past. Please enter a future date." (explains issue)
- Signature declined: "You declined the Non-Compete Agreement. Contact HR to discuss." (action required)
- File upload too large: "Document file is 30MB. Maximum size is 25MB." (specific limit)
- All errors have `role="alert"` with clear guidance

#### Motion & Animation
- Expandable sections open/close respecting `prefers-reduced-motion` (instant, no animation)
- Signature capture drawing smooth but respects preference for no animation
- Document viewer transitions respect preference
- Status badge updates instant (not animated)

#### Semantic HTML & ARIA
- Proper heading hierarchy: `<h1>` page, `<h2>` sections, `<h3>` subsections
- Document list as `<ul>` with `<li>` for each document
- Categories as `<section>` elements with aria-labels
- Emergency contacts as `<ul>` or `<dl>`
- Forms with associated `<label>` tags
- Signatures as `<article>` with signed details
- Expandable sections as `<details>`/`<summary>` or custom with proper ARIA

### AI Integration Points

#### 1. Document Organization & Tagging
- **Auto-tagging**: Based on document content, auto-assign categories
  - "This looks like a confidentiality agreement → add NDA tag"
- **Duplicate Detection**: Flag if same document uploaded twice
  - "This appears to be a duplicate of your 2024 performance review. Delete old copy?"

#### 2. Expiration & Renewal Alerts
- **Proactive Reminders**: Notify 60/30 days before expiration
  - "Your PMP certification expires in 30 days. Start renewal process?"
- **Renewal Guidance**: Provide links to renewal resources
  - "Renew your AWS certification here: [link]. Takes ~2 hours and costs $150."

#### 3. Signature Automation
- **Missing Signature Detection**: Identify required signatures not yet signed
  - "You're missing 2 signatures: I-9 and Arbitration Agreement. Both due by Jan 31."
- **Batch Signature Requests**: When policies update, batch request signatures
  - "3 policies were updated. Please sign by Feb 15."

#### 4. Compliance Monitoring
- **Compliance Status**: Check if employee has all required documents
  - "You're missing: Driver's License copy (required for drivers), I-9 Form"
- **Audit Trail**: Auto-generate audit reports of all documents and signatures
  - Generate compliance report for external audits

#### 5. Search & Retrieval
- **Smart Search**: Natural language search of documents
  - "Find my non-compete agreement" → fetches NDA and Non-Compete documents
- **Document Insights**: Summarize key terms from documents
  - "Your equity vesting: 4-year schedule with 1-year cliff. $500K RSU grant."

### Integrations & Dependencies

#### Internal Integrations
- **HRIS Core**: Employee data, job titles, departments
- **eSignature Service**: Digital signature capture and verification
- **Document Management**: Version control, storage, retention
- **Notification System**: Email reminders for signatures/expirations
- **HR Workflows**: I-9 verification process, onboarding checklist
- **Compliance System**: Document retention policies, audit trails

#### External Integrations
- **Cloud Storage**: Document storage (S3, Azure Blob, Google Drive)
- **eSignature Providers**: DocuSign, Adobe Sign (for advanced workflows)
- **Certification Verifiers**: LinkedIn, PMI, AWS (for credential verification)
- **Background Check Services**: Trigger verification upon I-9 completion

### Edge Cases & Error States

#### 1. I-9 Compliance
- **Employment Authorization**: Track when I-9 expires and requires reverification
- **Remote I-9**: Support remote I-9 completion with video verification
- **Status Changes**: If employment status changes (e.g., visa expires), flag for re-verification

#### 2. Policy Changes & Signature Renewal
- **Policy Updates**: Track policy version and require signature on updated version
- **Exemptions**: Allow HR to exempt employees from certain policies
- **Batch Signature Requests**: When 10+ policies updated, batch request signatures

#### 3. Departed Employees
- **Archive Documents**: Archive all documents when employee departs
- **Retention Period**: Maintain documents for compliance period (typically 3-7 years)
- **Access Restrictions**: Restrict access after departure (except for HR/legal)

#### 4. Legal Holds
- **Litigation**: Flag documents that may be subject to legal hold
- **Prevent Deletion**: Prevent deletion of documents under legal hold
- **Audit Trail**: Track all access to legal-hold documents

#### 5. Multi-State Compliance
- **State-Specific Documents**: Some states require specific policies/forms
- **Variable Policies**: Customize documents based on employee location
- **Legal Review**: Ensure all policies compliant with state law

### Success Metrics & Testing Scenarios

#### Document Organization
- [ ] Documents organized by category correctly
- [ ] Expandable sections work and display correct count
- [ ] Document status badges show correct status (Signed, Pending, Expired)
- [ ] Expiration dates display and calculate correctly

#### Signature Workflow
- [ ] Pending signature documents appear in "Action Needed"
- [ ] Signature capture modal opens and allows drawing/typing
- [ ] Signed documents update status to "Signed"
- [ ] Email reminder sent for signatures expiring soon
- [ ] Declined signatures noted and HR notified

#### Expiration Tracking
- [ ] Certifications with expiration dates tracked
- [ ] Expiring soon (30 days) flagged in yellow
- [ ] Expired documents flagged in red
- [ ] Renewal notifications sent at appropriate times

#### I-9 Verification
- [ ] I-9 form status displays correctly
- [ ] Missing documents clearly listed
- [ ] Supporting documents can be uploaded
- [ ] Reverification date tracked and alerts sent

#### Personal Document Upload
- [ ] Files upload successfully (PDF, Word, Excel, images)
- [ ] File size validation works (max 25MB)
- [ ] Documents tagged and searchable
- [ ] Version history maintained

#### Accessibility
- [ ] All expandable sections keyboard navigable
- [ ] Signature capture field keyboard accessible
- [ ] Screen reader announces document status
- [ ] Error messages clear and actionable
- [ ] Emergency contact form accessible

---

## Summary: Employee Self-Service Module (Complete)

The Employee Self-Service module provides 8 comprehensive screens enabling employee autonomy in managing personal information, benefits, time off, expenses, compensation, tax documents, and employment records:

1. **Employee Profile & Directory** (4.1) — Personal info management with org chart, colleague discovery
2. **Benefits Enrollment** (4.2) — Benefits selection, plan comparison, dependent management
3. **Time Off Request** (4.3) — Request vacation/sick leave with balance tracking and manager workflow
4. **Time Off Calendar** (4.4) — Visual team and company calendar with coverage status
5. **Expense Report** (4.5) — Submit expenses with receipt scanning, policy compliance, approval workflow
6. **Pay Stub & Payroll** (4.6) — Access pay stubs, direct deposit, payroll calendar, W4 management
7. **Tax Documents** (4.7) — W2/1099 access, verification letters, tax software integration
8. **Documents & Records** (4.8) — Centralized document library with signature workflow, expiration tracking

**All screens maintain WCAG 2.2 AA accessibility standards with comprehensive color contrast, keyboard navigation, screen reader support, focus management, touch-friendly targets, clear error handling, and motion/animation preferences. AI integration points include intelligent recommendations, compliance checking, document automation, and predictive analytics. Complete data models, integrations, edge cases, and success metrics provided for implementation.**
