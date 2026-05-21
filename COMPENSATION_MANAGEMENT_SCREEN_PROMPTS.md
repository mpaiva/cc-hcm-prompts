# Compensation Management Screen Prompts

> **Accessibility Note**: All screens below meet WCAG 2.2 AA standards with specific requirements for color contrast (4.5:1 for text), keyboard navigation, screen reader compatibility, focus management with visible indicators (3:1 minimum), 44×44 pixel touch targets, role="alert" for error handling, and prefers-reduced-motion support.

---

## Screen 6.1: Compensation Statement

### Overview
The Compensation Statement provides employees with a comprehensive view of their total compensation package, including base salary, bonuses, equity, benefits valuation, and year-over-year comparisons. This screen emphasizes transparency and helps employees understand the full value of their compensation.

### Wireframe Layout

```
┌─────────────────────────────────────────────────────┐
│ Compensation Statement                          [✕] │
├─────────────────────────────────────────────────────┤
│                                                     │
│ Compensation Year: [2025 ▼]  [Download PDF]       │
│                                                     │
├─────────────────────────────────────────────────────┤
│ TOTAL COMPENSATION: $250,000                        │
│ (↑ 8% from 2024)                                   │
├─────────────────────────────────────────────────────┤
│                                                     │
│ BASE SALARY                      BONUS             │
│ ┌────────────────────────────┐ ┌──────────────┐    │
│ │ $150,000                   │ │ $30,000      │    │
│ │ Monthly: $12,500           │ │ Target: 20%  │    │
│ │ (↑ 3% from last year)      │ │ (↑ from 15%) │    │
│ └────────────────────────────┘ └──────────────┘    │
│                                                     │
│ EQUITY                           BENEFITS VALUE    │
│ ┌────────────────────────────┐ ┌──────────────┐    │
│ │ Stock Options: 10,000      │ │ $40,000      │    │
│ │ Vested: 4,000 (40%)        │ │ Health Ins.  │    │
│ │ Current Value: $50,000     │ │ 401(k): $15k │    │
│ │ [View Details]             │ │ Other: $25k  │    │
│ └────────────────────────────┘ └──────────────┘    │
│                                                     │
│ RETIREMENT CONTRIBUTIONS         PTO VALUATION     │
│ ┌────────────────────────────┐ ┌──────────────┐    │
│ │ 401(k): $15,000            │ │ 20 Days PTO  │    │
│ │ Employer Match: $7,500     │ │ Value: $8,0  │    │
│ │ (6% match)                 │ │ Used: 5 days │    │
│ └────────────────────────────┘ └──────────────┘    │
│                                                     │
├─────────────────────────────────────────────────────┤
│ 📊 YEAR-OVER-YEAR COMPARISON                       │
│                                                     │
│ Category        2023      2024      2025   Change  │
│ ────────────────────────────────────────────────── │
│ Base Salary    $145,000  $149,500  $150,000 +0.3% │
│ Bonus         $25,000   $28,000   $30,000  +7.1%  │
│ Equity Value  $35,000   $40,000   $50,000  +25%   │
│ Benefits      $35,000   $38,000   $40,000  +5.3%  │
│ Total Comp    $240,000  $255,500  $270,000 +5.7%  │
│                                                     │
├─────────────────────────────────────────────────────┤
│ [Request Review]  [Contact HR]  [Print/Share]     │
└─────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Total Compensation Display**
   - Large, prominent display of total compensation figure
   - Year-over-year comparison with percentage change
   - Comparison to peer average (anonymized) - "You're in the 75th percentile"
   - Inflation-adjusted historical comparison

2. **Compensation Breakdown**
   - Base salary with monthly breakdown and recent changes
   - Bonus structure, target percentage, and actual/estimated amounts
   - Equity holdings with vesting information
   - Benefits valuation by category
   - Retirement contributions and employer match
   - PTO and other time-off valuation

3. **Historical Comparison**
   - Year-over-year table showing 3-5 years of history
   - Absolute and percentage changes highlighted
   - Trend indicators (up/down arrows with color coding)
   - Ability to filter by compensation category

4. **Equity Details**
   - Stock options/RSUs vesting schedule
   - Current market value and gain/loss
   - Exercise/sale options
   - Tax implications (defer to detailed view)

5. **Download & Share**
   - PDF download of compensation statement
   - Share with financial advisor (encrypted link)
   - Print-friendly format
   - Email to self

### Data Model

```javascript
{
  CompensationStatement: {
    employee_id: String (UUID),
    year: Number,
    effective_date: Date,
    currency: String ("USD", "EUR", etc.),
    total_compensation: Decimal,
    
    base_salary: {
      amount: Decimal,
      monthly: Decimal,
      last_adjustment_date: Date,
      adjustment_reason: String,
      adjustment_amount: Decimal,
      adjustment_percentage: Decimal
    },
    
    bonus: {
      plan_id: String,
      target_amount: Decimal,
      target_percentage: Decimal,
      actual_amount: Decimal,
      status: Enum ("pending", "earned", "paid"),
      payment_date: Date,
      metrics: [{
        metric_name: String,
        target: Decimal,
        actual: Decimal,
        achievement: Decimal,
        weight: Decimal
      }]
    },
    
    equity: {
      type: Enum ("stock_options", "rsu", "restricted_stock"),
      total_granted: Number,
      total_vested: Number,
      vesting_schedule: [{
        vesting_date: Date,
        shares_vesting: Number,
        cumulative_vested: Number,
        cumulative_percentage: Decimal
      }],
      current_value: Decimal,
      cost_basis: Decimal,
      gain_loss: Decimal,
      strike_price: Decimal (for options),
      exercise_window_end: Date
    },
    
    benefits: {
      health_insurance: {
        plan_name: String,
        coverage_type: Enum ("individual", "family"),
        employer_contribution: Decimal,
        employee_contribution: Decimal,
        total_value: Decimal
      },
      dental_vision: {
        coverage_type: String,
        employer_contribution: Decimal,
        total_value: Decimal
      },
      retirement: {
        plan_type: Enum ("401k", "pension", "other"),
        employer_contribution: Decimal,
        match_percentage: Decimal,
        employee_contribution: Decimal,
        total_value: Decimal
      },
      other_benefits: [{
        name: String,
        value: Decimal,
        type: Enum ("wellness", "education", "financial", "other")
      }],
      total_benefits_value: Decimal
    },
    
    pto_valuation: {
      days_allocated: Number,
      days_used: Number,
      days_remaining: Number,
      daily_rate: Decimal,
      total_value: Decimal,
      carryover_allowed: Boolean,
      carryover_max_days: Number
    },
    
    historical_comparisons: [{
      year: Number,
      base_salary: Decimal,
      bonus: Decimal,
      equity_value: Decimal,
      benefits_value: Decimal,
      total_compensation: Decimal
    }],
    
    peer_percentile: {
      role: String,
      company_size: String,
      location: String,
      percentile: Number (0-100),
      peer_median: Decimal,
      peer_25th: Decimal,
      peer_75th: Decimal
    }
  }
}
```

### UI Components Required

1. **Header Section**
   - Page title "Compensation Statement"
   - Year selector dropdown
   - Download/Print/Share buttons
   - Navigation breadcrumbs

2. **Total Compensation Card**
   - Large number display (use font size 32-48px minimum)
   - Year-over-year change indicator with color-coded arrow
   - Percentile badge
   - "View Details" collapsible section

3. **Compensation Cards**
   - Four-card grid layout
   - Card title with icon
   - Large amount display (24px minimum)
   - Description or metadata
   - Optional "View Details" links

4. **Historical Comparison Table**
   - Responsive table with sticky header
   - Clear row/column labels
   - Data cells with currency formatting
   - Trend indicators (↑↓)
   - Color-coded positive/negative changes

5. **Action Buttons**
   - Primary: "Request Review" (meeting with HR)
   - Secondary: "Contact HR" (chat/email)
   - Tertiary: "Print/Share"

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text on white background: 4.5:1 ratio (use #333333 for body text, #000000 for headers)
- Card backgrounds: Use light gray (#F5F5F5) with sufficient contrast
- Positive trend (+): Green (#2E7D32) with min 4.5:1 contrast against white
- Negative trend (-): Orange (#E65100) with min 4.5:1 contrast against white
- Focus indicators: Blue (#0066CC) with 3:1 minimum against background
- Icons: Use solid colors that meet 4.5:1 contrast with adjacent text

**Keyboard Navigation**
- Tab order: Year selector → Download button → Compensation cards → Historical table → Action buttons
- Arrow keys navigate within dropdown year selector
- Enter to activate download/print/share buttons
- Tab to focus on table cells for detailed content review
- Escape to close any overlays or details panels

**Screen Reader Support**
- Page heading: `<h1>Compensation Statement for [Year]</h1>`
- Section headings: `<h2>Base Salary</h2>`, `<h2>Year-Over-Year Comparison</h2>`
- Compensations cards: `<div role="region" aria-labelledby="bonus-heading">`
  - Aria-label for amounts: "Total Compensation: $250,000, up 8% from last year"
  - Trend announcements: "Equity Value increased $10,000 or 25%"
- Table with `<table aria-label="Historical Compensation Comparison">` 
  - Table headers: `<th scope="col">Year</th>` and `<th scope="row">[year]</th>`
  - Data cells announce amount and trend: "$150,000, up 0.3 percent"
- Year selector: `<select aria-label="Select compensation year">`
- Buttons: Clear text labels without relying on icons alone
  - `<button aria-label="Download compensation statement as PDF">Download PDF</button>`

**Focus Management**
- Focus indicator on all interactive elements (buttons, select, links): 3px solid blue outline with min 3:1 contrast
- Initial focus on page load: Year selector
- Focus retained when opening overlays
- Tab order visible and logical

**Touch Targets**
- All buttons minimum 44×44 pixels (year selector dropdown: 44px height, 200px width minimum)
- Card content areas clickable (48×48 minimum)
- "View Details" links: minimum 44×44 interactive area

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce` - remove fade-in animations
- Trend arrows: No animation unless user hasn't set prefers-reduced-motion
- Number transitions: Instant display or slow fade (>2 seconds) if animated

**Error & Status Messages**
- Status updates announced via `role="status"` (non-intrusive changes like trend recalculation)
- Critical messages via `role="alert"` (if document requires signature, if equity vesting date passed)

---

## Screen 6.2: Salary Review & Adjustment

### Overview
Salary Review & Adjustment screen enables managers and HR professionals to recommend and process salary adjustments based on performance, market data, promotions, and equity analyses. This screen includes workflow management, approval routing, and communication templates.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ Salary Review & Adjustment                            [✕] │
├───────────────────────────────────────────────────────────┤
│ Review Cycle: Q1 2025 [▼] | Status: In Progress          │
│                                                           │
│ [Filters: All ▼] [Search employee ___________] [Reset]   │
├───────────────────────────────────────────────────────────┤
│                                                           │
│ Employee List                                             │
│ ┌────────────────────────────────────────────────────┐   │
│ │ ☑ Employee Name | Role | Current | Recommended │   │   │
│ ├────────────────────────────────────────────────────┤   │
│ │ ☐ Sarah Chen    | PM   | $150k  | $157.5k (+5%) │   │   │
│ │ ☐ Marcus Liu    | Eng  | $145k  | $149.3k (+3%) │   │   │
│ │ ☐ Jennifer Park | Eng  | $160k  | $160k    (0%) │   │   │
│ └────────────────────────────────────────────────────┘   │
│                                                           │
│ [Add Employee]                                            │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ SALARY ADJUSTMENT FORM                                    │
│                                                           │
│ Selected Employee: Sarah Chen [Change]                   │
│                                                           │
│ ┌─────────────────────────────────────────────────────┐ │
│ │ Current Salary:        $150,000                      │ │
│ │ Proposed Salary:       [150000 ___________]         │ │
│ │ Adjustment Amount:     $7,500                        │ │
│ │ Adjustment %:          5.0%                          │ │
│ │ Effective Date:        [05/21/2025 ▼]              │ │
│ └─────────────────────────────────────────────────────┘ │
│                                                           │
│ JUSTIFICATION & ANALYSIS                                  │
│                                                           │
│ Justification Type:                                       │
│ ◉ Performance (Performance Rating: 4.2/5)                │
│ ◯ Market Adjustment (Below market by 5%)                 │
│ ◯ Promotion                                              │
│ ◯ Retention                                              │
│ ◯ Other                                                  │
│                                                           │
│ Details: [Large text area]                               │
│ "Sarah has demonstrated strong leadership and technical  │
│  expertise. Current role scope expanded to include team  │
│  mentoring."                                             │
│                                                           │
│ ┌─────────────────────────────────────────────────────┐ │
│ │ MARKET DATA COMPARISON                              │ │
│ │ Role: Product Manager (San Francisco)               │ │
│ │ Peer 25th:    $145,000                              │ │
│ │ Peer Median:  $160,000  [↑ Sarah is below]         │ │
│ │ Peer 75th:    $175,000                              │ │
│ │ Company avg:  $158,000                              │ │
│ └─────────────────────────────────────────────────────┘ │
│                                                           │
│ EQUITY ANALYSIS                                           │
│ ◐ This adjustment does not create equity concerns        │ │
│   [View Equity Report]                                   │ │
│                                                           │
│ APPROVAL WORKFLOW                                         │
│ [Budget Approval] → [Executive Review] → [HR Approval]  │ │
│                                                           │
│ [Submit for Approval] [Save as Draft] [Cancel]          │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Employee List View**
   - Table showing current and recommended adjustments
   - Bulk selection with checkboxes
   - Filters: department, team, adjustment reason, status
   - Search by name/employee ID
   - Sortable columns
   - Show/hide market data columns

2. **Salary Adjustment Form**
   - Input fields for proposed salary
   - Auto-calculation of adjustment amount and percentage
   - Effective date picker with scheduling options
   - Predefined justification types with custom details
   - Market data display alongside form
   - Equity impact analysis

3. **Market Data Comparison**
   - Show peer salary bands for role/location
   - Competitor benchmarking data
   - Internal company average
   - Historical trends
   - Link to full market data report

4. **Equity Analysis**
   - Automatic check for salary equity (similar roles, demographics)
   - Flag any inequities or concerns
   - Summary of gender/race/tenure-based equity
   - Compliance with equity requirements

5. **Approval Workflow**
   - Multi-level approvals (budget → executive → HR)
   - Auto-routing based on adjustment amount
   - Comments at each approval level
   - Estimated approval timeline
   - Notification when approved

6. **Communication**
   - Pre-written communication templates
   - Customization options
   - Schedule notification date
   - One-click employee notification

### Data Model

```javascript
{
  SalaryAdjustment: {
    adjustment_id: String (UUID),
    review_cycle_id: String,
    employee_id: String (UUID),
    current_salary: Decimal,
    proposed_salary: Decimal,
    adjustment_amount: Decimal,
    adjustment_percentage: Decimal,
    effective_date: Date,
    created_by_manager_id: String (UUID),
    created_date: Date,
    status: Enum ("draft", "submitted", "in_review", "approved", "rejected", "implemented"),
    
    justification: {
      type: Enum ("performance", "market_adjustment", "promotion", "retention", "other"),
      details: String,
      performance_rating: Decimal (0-5) (optional),
      promotion_details: String (optional),
      retention_reason: String (optional),
      other_reason: String (optional)
    },
    
    market_data: {
      role: String,
      location: String,
      peer_25th_percentile: Decimal,
      peer_median: Decimal,
      peer_75th_percentile: Decimal,
      competitor_average: Decimal,
      internal_company_average: Decimal,
      adjustment_vs_market: Decimal,
      data_source: String
    },
    
    equity_analysis: {
      similar_roles_count: Number,
      gender_pay_ratio: Decimal,
      race_pay_ratio: Decimal,
      tenure_pay_ratio: Decimal,
      flag_high_risk: Boolean,
      flag_moderate_risk: Boolean,
      recommendations: [String]
    },
    
    approvals: [{
      approval_level: Enum ("budget", "executive", "hr"),
      approver_id: String (UUID),
      approval_date: Date,
      status: Enum ("pending", "approved", "rejected"),
      comments: String,
      required_approval: Boolean,
      auto_approved: Boolean
    }],
    
    communication: {
      template_id: String,
      employee_notification_date: Date,
      notification_method: Enum ("email", "meeting", "both"),
      custom_message: String,
      notification_sent: Boolean,
      notification_sent_date: Date
    }
  }
}
```

### UI Components Required

1. **Employee List Table**
   - Selectable rows with checkboxes
   - Sortable headers (name, current salary, proposed, adjustment %)
   - Sticky header on scroll
   - Row highlighting on hover
   - Quick-action buttons per row (Edit, View Details, Delete)

2. **Salary Input Form**
   - Input field for proposed salary (currency formatted)
   - Read-only fields for current salary and calculations
   - Dropdown for adjustment justification type
   - Large text area for details (min 100px height)
   - Date picker for effective date

3. **Market Data Card**
   - Horizontal bar chart showing peer percentiles
   - Current employee position highlighted
   - Legend with data source
   - "View Full Report" link

4. **Equity Analysis Panel**
   - Checkmark or warning icon
   - Summary text
   - Risk level indicator (green/yellow/red)
   - "View Equity Report" button

5. **Approval Workflow Indicator**
   - Horizontal stepper showing approval stages
   - Current stage highlighted
   - Checkmarks for completed approvals
   - Pending count display

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text on white: 4.5:1 (use #333333 for body, #000000 for headers)
- Table rows: Alternate #FFFFFF and #F5F5F5 backgrounds
- Market data bar chart: Green (#2E7D32, 4.5:1), Yellow (#F57C00, 4.5:1), Red (#C62828, 4.5:1)
- Equity risk: Green (#2E7D32), Yellow (#F57C00), Red (#C62828)
- Focus indicators: 3px blue (#0066CC) outline with 3:1 contrast

**Keyboard Navigation**
- Tab: Review cycle selector → Filters → Search → Table rows → Add button → Form fields → Submit button
- Arrow keys: Navigate table rows (Up/Down), manage dropdowns (Arrow keys open/close)
- Enter/Space: Toggle row selection, open row details
- Escape: Close any open modals or dropdown filters
- Ctrl+A: Select all employees in table

**Screen Reader Support**
- Page heading: `<h1>Salary Review & Adjustment - Q1 2025</h1>`
- Table: `<table aria-label="Employee salary adjustments">` with proper `<thead>`, `<tbody>`, `<th scope="col">` and `<th scope="row">`
- Table announcement: "X of Y employees reviewed, X pending approval"
- Form sections: `<fieldset><legend>Justification Details</legend>` for radio button groups
- Checkboxes: `<input type="checkbox" aria-label="Select Sarah Chen for adjustment">`
- Adjustment calculation announcement via `role="status"`: "Proposed salary: $157,500. Adjustment: $7,500 or 5%"
- Equity analysis: `<div role="status" aria-live="polite">No equity concerns detected</div>`
- Approval workflow: `<div aria-label="Approval workflow: Budget approval pending, Executive review, HR approval">`

**Focus Management**
- All interactive elements have visible focus indicator (3px solid blue, 3:1 contrast)
- Initial focus on review cycle selector
- Focus moves to first form field when employee is selected
- Modal focus trap when viewing equity/market details
- Skip link at top: "Skip to adjustment form"

**Touch Targets**
- All buttons: 44×44 minimum (action buttons 48×56px)
- Checkboxes: 44×44 interactive area (visual 24×24 with padding)
- Table rows: Minimum 44px height
- Date picker trigger: 44×44 minimum

**Motion & Animation**
- Remove animations for `prefers-reduced-motion: reduce`
- Table sorting: No animated re-ordering, instant display
- Approval status changes: Instant visual update with `role="status"` announcement

**Error & Status Messages**
- Form validation: `role="alert"` for required fields
  - "Proposed salary is required"
  - "Proposed salary cannot exceed market 75th percentile by more than 5%"
- Status updates: `role="status"` aria-live="polite"
  - "Adjustment submitted for approval"
  - "3 out of 10 approvals completed"

---

## Screen 6.3: Bonus & Variable Pay Management

### Overview
Bonus & Variable Pay Management enables managers and HR to define bonus structures, calculate payouts based on performance metrics, manage approvals, and communicate results to employees. This screen supports complex bonus calculations and equity considerations.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ Bonus & Variable Pay Management                      [✕] │
├───────────────────────────────────────────────────────────┤
│ Bonus Cycle: 2025 Annual [▼]  Status: Metrics Review     │
│                                                           │
│ [View Plans] [Create New Plan] [Reports]                │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ ACTIVE BONUS PLANS                                        │
│                                                           │
│ Plan: Annual Performance Bonus                            │
│ Type: Performance-Based | Period: 2025 | Status: Active   │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Target Payout: 20% of salary for all employees       │ │
│ │ Budget Cap: $500,000                                  │ │
│ │ Current Accrual: $485,000 (97%)                       │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ BONUS CALCULATION SETUP                                   │
│                                                           │
│ Formula: Base (60%) + Individual (30%) + Company (10%)   │
│                                                           │
│ ┌──────────────────┐ ┌──────────────────┐                │
│ │ Base Component   │ │ Individual Comp.  │                │
│ │ Target: 12% saly │ │ Target: 6% salary │                │
│ │ Weight: 60%      │ │ Weight: 30%       │                │
│ │                  │ │                   │                │
│ │ [Edit] [View]    │ │ [Edit] [View]     │                │
│ └──────────────────┘ └──────────────────┘                │
│                                                           │
│ ┌──────────────────┐                                      │
│ │ Company Comp.    │                                      │
│ │ Target: 2% salary│                                      │
│ │ Weight: 10%      │                                      │
│ │                  │                                      │
│ │ [Edit] [View]    │                                      │
│ └──────────────────┘                                      │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ PERFORMANCE METRICS                                       │
│                                                           │
│ Metric Name          | Target | Actual | Achievement %   │
│ ────────────────────────────────────────────────────────  │
│ Revenue Growth       | $10M   | $9.8M  | 98%            │
│ [Edit metric] [Add more metrics]                         │
│                                                           │
│ Product Quality      | 95%    | 92%    | 97%            │
│ [Edit metric]                                            │
│                                                           │
│ Customer Retention   | 92%    | 95%    | 103%           │
│ [Edit metric]                                            │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ PAYOUT CALCULATION                                        │
│                                                           │
│ [Calculate Payouts]                                       │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Calculation Method: Actual Achievement based         │ │
│ │ Salary Reference Date: 12/31/2024                    │ │
│ │                                                      │ │
│ │ [Run Calculation] [Preview Results] [Save Draft]    │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ PAYOUT RESULTS PREVIEW                                    │
│                                                           │
│ Employee Name | Salary | Target | Achievement | Payout  │
│ ───────────────────────────────────────────────────────  │
│ Sarah Chen    | 150k   | 30k    | 100%        | 30k    │
│ Marcus Liu    | 145k   | 29k    | 95%         | 27.6k  │
│ Jennifer P    | 160k   | 32k    | 98%         | 31.4k  │
│                                                           │
│ Total Payout: $89,000                                    │
│                                                           │
│ [Approve Payouts] [Export] [Cancel]                      │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Bonus Plan Management**
   - Create multiple bonus plans (annual, quarterly, special)
   - Define plan structure (target payout %, components, weights)
   - Budget cap and tracking
   - Status tracking (draft, setup, metrics, calculation, approval, active)

2. **Bonus Component Setup**
   - Base component (performance floor)
   - Individual performance component
   - Company/team performance component
   - Custom weightings
   - Edit templates for future use

3. **Performance Metrics**
   - Define company-wide metrics (revenue, customer satisfaction, etc.)
   - Individual team metrics (quality, velocity, etc.)
   - Achievement tracking (actual vs. target)
   - Support for multiple metric types (currency, percentage, count)

4. **Bonus Calculation**
   - Automated calculation based on formula and metrics
   - Support for modifiers (location, role, tenure)
   - Overpayment controls (no individual exceeds cap)
   - Budget tracking and alerts
   - Equity check (flag unusual distributions)

5. **Approval Workflow**
   - Multi-level approvals (budget review, executive sign-off)
   - Comments and adjustments at each level
   - Rollback capability
   - Audit trail

6. **Payout Processing**
   - Export payout data
   - Schedule payment date
   - Employee communication template
   - Integration with payroll system

### Data Model

```javascript
{
  BonusPlan: {
    plan_id: String (UUID),
    plan_name: String,
    plan_type: Enum ("annual", "quarterly", "special", "retention"),
    fiscal_year: Number,
    period_start_date: Date,
    period_end_date: Date,
    status: Enum ("draft", "setup", "metrics", "calculation", "approval", "active", "closed"),
    created_by_id: String (UUID),
    created_date: Date,
    
    target_payout: {
      default_percentage: Decimal (0-1),  // e.g., 0.20 for 20%
      by_role: [{
        role: String,
        percentage: Decimal
      }],
      by_location: [{
        location: String,
        percentage_modifier: Decimal  // e.g., 1.1 for 110%
      }]
    },
    
    budget: {
      total_budget: Decimal,
      current_accrual: Decimal,
      budget_by_department: [{
        department: String,
        budget: Decimal,
        current_spend: Decimal
      }]
    },
    
    components: [{
      component_id: String (UUID),
      component_name: String,
      component_type: Enum ("base", "individual", "company", "team"),
      target_percentage: Decimal,
      weight: Decimal,
      metrics: [String] (references to Performance Metric IDs)
    }],
    
    performance_metrics: [{
      metric_id: String (UUID),
      metric_name: String,
      metric_type: Enum ("revenue", "customer", "quality", "people", "innovation", "other"),
      unit: String ("USD", "percent", "count", etc.),
      target_value: Decimal,
      actual_value: Decimal,
      achievement_percentage: Decimal,
      weight: Decimal,
      scope: Enum ("company", "department", "team", "individual"),
      owner_id: String (UUID),
      last_updated: Date
    }],
    
    payout_calculations: [{
      calculation_id: String (UUID),
      calculation_date: Date,
      calculation_method: Enum ("target_based", "actual_achievement", "hybrid"),
      salary_reference_date: Date,
      total_payouts: Decimal,
      number_of_employees: Number,
      average_payout: Decimal,
      status: Enum ("draft", "calculated", "approved", "processed")
    }],
    
    payouts: [{
      payout_id: String (UUID),
      employee_id: String (UUID),
      salary_at_reference_date: Decimal,
      target_payout: Decimal,
      achievement_percentage: Decimal,
      calculated_payout: Decimal,
      final_approved_payout: Decimal,
      payment_date: Date,
      status: Enum ("calculated", "approved", "processed", "paid")
    }],
    
    approvals: [{
      approval_level: Enum ("finance", "executive", "board", "payroll"),
      approver_id: String (UUID),
      approval_date: Date,
      status: Enum ("pending", "approved", "rejected"),
      comments: String
    }]
  }
}
```

### UI Components Required

1. **Plan Cards**
   - Plan name and type badge
   - Status indicator (color-coded)
   - Key metrics (target %, budget, accrual)
   - Action buttons (Edit, View, Calculate)

2. **Component Cards**
   - Title with percentage/weight display
   - Target value
   - Associated metrics list
   - Edit/View buttons

3. **Metrics Management**
   - Editable metric table
   - Input fields for target and actual values
   - Achievement % calculated field
   - Add/delete metric rows

4. **Calculation Controls**
   - Method selector (radio buttons)
   - Reference date picker
   - Calculate button (prominent)
   - Status indicator

5. **Payout Results Table**
   - Sortable columns (employee, salary, payout, achievement %)
   - Detailed row expansion
   - Summary totals row
   - Export button

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text on white: 4.5:1 (use #333333 for body, #000000 for headers)
- Status badges: Active (green #2E7D32, 4.5:1), Draft (gray #757575, 4.5:1), Closed (gray #9E9E9E, 4.5:1)
- Achievement bars: Green (#2E7D32) for 100%+, Yellow (#F57C00) for 80-99%, Red (#C62828) for <80%
- Focus indicators: 3px blue (#0066CC), 3:1 minimum contrast

**Keyboard Navigation**
- Tab: Bonus cycle selector → Buttons (View Plans, Create) → Plan cards → Component cards → Metrics table → Calculation button → Approval section
- Arrow keys: Navigate table rows, open/close plan details
- Enter: Activate buttons, edit metrics
- Escape: Close modal dialogs, cancel edits

**Screen Reader Support**
- Page heading: `<h1>Bonus & Variable Pay Management - 2025 Cycle</h1>`
- Plan section: `<section aria-labelledby="active-plans-heading">`
  - `<h2 id="active-plans-heading">Active Bonus Plans</h2>`
- Component cards: `<div role="region" aria-label="[Component Name] - Target [percentage]%, Weight [weight]%">`
- Metrics table: `<table aria-label="Performance Metrics">` with proper headers
  - Column announcement: "Revenue Growth: Target $10,000,000, Actual $9,800,000, Achievement 98%"
- Calculation status: `<div role="status" aria-live="polite">Calculation in progress...</div>`
- Results table: `<table aria-label="Payout Calculation Results">`
  - Row summary: "[Employee Name]: Salary $150,000, Target Payout $30,000, Achievement 100%, Final Payout $30,000"
- Achievement % badges: 
  - `<span aria-label="Achievement 98 percent, target exceeded">98%</span>`

**Focus Management**
- Visible focus indicator (3px blue) on all interactive elements
- Initial focus on bonus cycle selector
- Focus trap in modal dialogs (Create Plan, View Details)
- Skip link: "Skip to bonus calculation section"
- Tab order: All form inputs in logical order (plan → components → metrics → calculate)

**Touch Targets**
- All buttons: 44×44 minimum (action buttons 48×56px)
- Component cards: 48×48 minimum for "Edit"/"View" buttons
- Metric row delete: 44×44 minimum
- Calculation button: 56×48px (prominent)
- Metric table rows: 44px height minimum

**Motion & Animation**
- Remove animations if `prefers-reduced-motion: reduce`
- No animated transitions during metric updates
- Achievement % display instantly, not animated

**Error & Status Messages**
- Validation errors: `role="alert"`
  - "Total component weights must equal 100%"
  - "Actual values required for all metrics before calculation"
- Calculation updates: `role="status"` aria-live="polite"
  - "Calculation complete: Total payouts $89,000"
  - "X out of Y approvals received"
- Warnings: `role="alert"` aria-live="assertive"
  - "Budget will be exceeded by $5,000 with current calculations"

---

## Screen 6.4: Equity & Stock Options

### Overview
Equity & Stock Options screen allows employees to view their equity grants, track vesting schedules, understand valuations, and exercise options. This screen emphasizes clarity on complex financial concepts and provides tools for financial planning.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ Equity & Stock Options                              [✕] │
├───────────────────────────────────────────────────────────┤
│                                                           │
│ TOTAL EQUITY VALUE: $125,000                             │
│ 250 shares held | Current Price: $50/share               │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ ACTIVE GRANTS                                             │
│                                                           │
│ Grant 1: Stock Options (ISO)                             │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Grant Date: 01/15/2023      Type: ISO Stock Options  │ │
│ │ Total Shares: 10,000         Strike Price: $20/share  │ │
│ │                                                       │ │
│ │ Vested: 2,500 (25%)          [Show Schedule]         │ │
│ │ Unvested: 7,500 (75%)                                 │ │
│ │                                                       │ │
│ │ Current Value: $125,000                               │ │
│ │ Intrinsic Value: $75,000 (10,000 × $50 - 10,000 × $20)
│ │ Gain: $75,000 (unrealized)                            │ │
│ │                                                       │ │
│ │ Exercise Window Expires: 01/15/2033                   │ │
│ │ Next Vesting: 03/15/2025 (625 shares)               │ │
│ │                                                       │ │
│ │ [View Vesting Schedule] [Tax Implications] [Exercise]│ │
│ │ [View Details] [Export Grant] [Edit Contact Info]    │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ Grant 2: Restricted Stock Units (RSU)                    │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Grant Date: 06/01/2024      Type: RSU                │ │
│ │ Total Units: 150             Price at Grant: $45/unit │ │
│ │                                                       │ │
│ │ Vested: 0 (0%)               [Show Schedule]         │ │
│ │ Unvested: 150 (100%)         Vesting: 4-year schedule│ │
│ │                                                       │ │
│ │ Current Value: $7,500                                │ │
│ │ Grant Value: $6,750                                  │ │
│ │ Gain: $750 (unrealized)                              │ │
│ │                                                       │ │
│ │ Next Vesting: 09/01/2024 (37.5 units)               │ │
│ │                                                       │ │
│ │ [View Vesting Schedule] [Tax Implications] [Details]  │ │
│ │ [Export Grant] [Edit Contact Info]                   │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ VESTING SCHEDULE VIEWER                                   │
│                                                           │
│ Selected: Stock Options Grant 1                          │
│                                                           │
│ ╔════════════════════════════════════════════════════╗ │
│ ║                                                    ║ │
│ ║ 10,000 shares total                              ║ │
│ ║                                                    ║ │
│ ║ Year 1  ████░░░░░░  2,500 vested (25%)           ║ │
│ ║ Year 2  ████████░░  5,000 vested (50%)           ║ │
│ ║ Year 3  ██████████  7,500 vested (75%)           ║ │
│ ║ Year 4  ██████████  10,000 vested (100%)         ║ │
│ ║         (Complete)                                ║ │
│ ║                                                    ║ │
│ ║ Next vesting: March 15, 2025 (+625 shares)       ║ │
│ ║                                                    ║ │
│ ╚════════════════════════════════════════════════════╝ │
│                                                           │
│ Detailed Schedule:                                        │
│ Vesting Date  | Shares | Cumulative | Vesting %          │
│ ────────────────────────────────────────────────────────  │
│ 01/15/2024    | 2,500  | 2,500      | 25%               │
│ 03/15/2025    | 625    | 3,125      | 31%               │
│ 06/15/2025    | 625    | 3,750      | 38%               │
│ 09/15/2025    | 625    | 4,375      | 44%               │
│ ... (8 more rows)                                        │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ EXERCISE & ACTIONS                                        │
│                                                           │
│ [Exercise Options] [Request Early Exercis] [Sell Shares]  │
│                                                           │
│ [Download Tax Report] [Contact HR/Legal] [Help]          │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Grant Overview**
   - Summary of all active equity grants
   - Grant type (ISO options, NSO options, RSU, restricted stock)
   - Total shares/units with vesting status
   - Current market value and cost basis

2. **Vesting Schedule**
   - Visual representation (progress bar with years)
   - Detailed table with dates and share counts
   - Next vesting date highlighted
   - Acceleration information (if applicable)

3. **Valuation Information**
   - Current market price (real-time or daily updated)
   - Current total value of holdings
   - Intrinsic value (for options)
   - Unrealized gains/losses
   - Cost basis tracking

4. **Tax Implications**
   - Estimated tax liability (ISO vs NSO)
   - Alternative Minimum Tax (AMT) implications
   - Withholding information
   - ISO exercise timing considerations
   - Link to tax form requirements

5. **Exercise Options**
   - Exercise vested options
   - Stock purchase methods (cash, cashless exercise, broker-assisted)
   - Early exercise option (if available)
   - Option expiration countdown

6. **Document Downloads**
   - Grant agreement PDF
   - Award notice
   - Vesting schedule
   - Tax forms (Form 3921, Form 3922)
   - Historical statements

### Data Model

```javascript
{
  EquityGrant: {
    grant_id: String (UUID),
    employee_id: String (UUID),
    grant_date: Date,
    grant_type: Enum ("iso_stock_option", "nso_stock_option", "rsu", "restricted_stock"),
    grant_status: Enum ("active", "exercised", "expired", "cancelled"),
    
    grant_details: {
      total_shares: Number,
      strike_price: Decimal (for options),
      price_at_grant: Decimal (for RSU/restricted stock),
      vesting_schedule_type: Enum ("4_year_monthly", "4_year_quarterly", "cliff_then_monthly", "custom"),
      cliff_months: Number (if applicable),
      vesting_start_date: Date,
      vesting_end_date: Date,
      acceleration_clauses: [String] // e.g., "Change of control", "Termination without cause"
    },
    
    vesting_schedule: [{
      vesting_date: Date,
      shares_vesting: Number,
      cumulative_shares: Number,
      cumulative_percentage: Decimal,
      is_vest_date: Boolean,
      is_acceleration_triggered: Boolean
    }],
    
    current_status: {
      vested_shares: Number,
      unvested_shares: Number,
      vested_percentage: Decimal,
      current_market_price: Decimal,
      price_as_of_date: Date,
      current_total_value: Decimal,
      cost_basis: Decimal,
      unrealized_gain_loss: Decimal,
      unrealized_gain_loss_percentage: Decimal
    },
    
    option_details: {  // Only for options
      option_type: Enum ("iso", "nso"),
      exercise_window_expiration_date: Date,
      shares_outstanding: Number,
      intrinsic_value: Decimal,  // (market_price - strike) × shares
      exercise_methods_available: [Enum("cash", "cashless", "broker_assisted")],
      early_exercise_allowed: Boolean,
      post_termination_exercise_window_days: Number
    },
    
    tax_information: {
      estimated_iso_tax_liability: Decimal,
      estimated_nso_tax_liability: Decimal,
      amt_exposure: Decimal (for ISOs),
      withholding_required: Boolean,
      withholding_amount: Decimal,
      related_forms: [String]  // "Form 3921", "Form 3922", etc.
    },
    
    exercise_history: [{
      exercise_id: String (UUID),
      exercise_date: Date,
      shares_exercised: Number,
      exercise_price: Decimal,
      exercise_method: Enum ("cash", "cashless", "broker_assisted"),
      total_cost: Decimal,
      net_proceeds: Decimal,
      status: Enum ("pending", "completed")
    }],
    
    documents: [{
      document_id: String (UUID),
      document_type: String ("Grant Agreement", "Vesting Schedule", "Tax Form", "Award Notice"),
      document_url: String,
      download_date: Date
    }]
  }
}
```

### UI Components Required

1. **Grant Cards**
   - Grant type badge with icon
   - Grant date and key terms
   - Vesting progress bar (visual + percentage)
   - Valuation summary (current value, gain/loss)
   - Next vesting date
   - Action buttons

2. **Vesting Schedule Visualizer**
   - Year-by-year progress bar
   - Animated fill based on time progression
   - Next vesting date callout
   - Detailed table below

3. **Vesting Table**
   - Sortable/filterable columns
   - Date, shares, cumulative count
   - Sticky header on scroll
   - Highlight next vesting date

4. **Value Display Cards**
   - Large number for total value
   - Current market price (prominently displayed)
   - Cost basis and gain/loss
   - Color-coded gain/loss (green/red)

5. **Exercise Modal/Form**
   - Grant selection dropdown
   - Vested shares available
   - Exercise method selector (radio buttons)
   - Price and cost calculations
   - Confirmation button

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text on white: 4.5:1 (use #333333 for body, #000000 for headers)
- Grant cards background: #F5F5F5 with #333333 text
- Vesting progress: Green (#2E7D32) filled, Gray (#CCCCCC) unfilled, 4.5:1 against white
- Gain (positive): Green (#2E7D32, 4.5:1)
- Loss (negative): Red (#C62828, 4.5:1)
- Alert: Orange (#F57C00, 4.5:1)
- Focus indicators: 3px blue (#0066CC), 3:1 minimum contrast

**Keyboard Navigation**
- Tab: Total value card → Grant cards → Vesting schedule selector → Exercise button → Document downloads
- Arrow keys: Navigate grant list, select vesting schedule
- Enter: Open grant details, initiate exercise
- Escape: Close modals, cancel exercises

**Screen Reader Support**
- Page heading: `<h1>Equity & Stock Options</h1>`
- Total value section: `<div role="region" aria-labelledby="total-value-heading">`
  - `<h2 id="total-value-heading">Total Equity Value: $125,000</h2>`
  - Detailed summary: "Aria-label='250 shares at $50 per share, current market value $125,000'"
- Grant cards: `<article aria-labelledby="grant-[id]-title">`
  - `<h3 id="grant-[id]-title">[Grant Type] - [Grant Date]</h3>`
  - Vesting announcement: "Vested: 2,500 of 10,000 shares (25%). Next vesting: March 15, 2025 - 625 shares"
  - Value announcement: "Current Value: $125,000. Unrealized Gain: $75,000 or 150%"
- Vesting progress bar: `<div role="progressbar" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100" aria-label="25 percent vested">`
- Vesting table: `<table aria-label="Detailed vesting schedule for Stock Options Grant 1">`
  - Row announcement: "Vesting Date: January 15, 2024. Shares: 2,500. Cumulative: 2,500. Vesting Percentage: 25%"
- Exercise modal: `<dialog aria-labelledby="exercise-title">`
  - `<h2 id="exercise-title">Exercise Stock Options</h2>`

**Focus Management**
- Visible focus indicator (3px blue) on all interactive elements
- Initial focus on total value summary
- Focus trap in exercise modal
- Skip link: "Skip to vesting schedule"
- Tab order: Overview → Grants → Details → Actions

**Touch Targets**
- All buttons: 44×44 minimum (action buttons 48×56px)
- Grant cards: 48×48 minimum for action buttons
- Table rows: 44px height
- Document download links: 44×44 minimum

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce`
- Vesting progress bars: No animation, instant display
- Number transitions: Instant or static

**Error & Status Messages**
- Exercise errors: `role="alert"`
  - "Cannot exercise unvested options"
  - "Insufficient funds for cash exercise. Minimum required: $200,000"
- Status updates: `role="status"` aria-live="polite"
  - "Exercise request submitted for approval"
  - "Shares will be available in 2-3 business days"
- Warnings: `role="alert"` aria-live="assertive"
  - "Stock option expires in 60 days"
  - "Exercise window expires soon"

---

## Screen 6.5: Market Data & Benchmarking

### Overview
Market Data & Benchmarking provides HR and Finance professionals with access to market compensation data for salary benchmarking, competitiveness analysis, and informed decision-making on compensation adjustments.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ Market Data & Benchmarking                          [✕] │
├───────────────────────────────────────────────────────────┤
│                                                           │
│ FILTERS & PARAMETERS                                      │
│                                                           │
│ Job Role: [Product Manager ▼]                            │
│ Location: [San Francisco, CA ▼] [+ Add Location]        │
│ Company Size: [250-1000 employees ▼]                     │
│ Industry: [Technology ▼]                                  │
│ Experience Level: [Senior (5+ years) ▼]                 │
│                                                           │
│ Data Source: [Salary.com, Glassdoor, Levels.fyi ▼]     │
│ Last Updated: April 2025                                  │
│                                                           │
│ [Apply Filters] [Reset] [Export Report] [Save View]     │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ SALARY BENCHMARKS                                         │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │        Salary Distribution for PM (San Francisco)    │ │
│ │                                                      │ │
│ │ 10th %ile    25th %ile    Median    75th %ile 90th % │
│ │   $130k        $145k     $160k      $175k    $190k  │ │
│ │                                                      │ │
│ │ [Your Company Average: $158k ↓]                      │ │
│ │                                                      │ │
│ │ Percentile Distribution (Visual):                   │ │
│ │                                                      │ │
│ │ ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  │ │
│ │ ↑10%    ↑25%    ↑50%    ↑75%    ↑90%                │ │
│ │ $130k   $145k   $160k   $175k   $190k               │ │
│ │                    ▲ Our Company ($158k)             │ │
│ │                                                      │ │
│ │ Your company is 1.3% below market median            │ │
│ │                                                      │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ DETAILED COMPENSATION BREAKDOWN                           │
│                                                           │
│ Component    | 10th   | 25th  | Median | 75th  | 90th   │
│ ──────────────────────────────────────────────────────── │
│ Base Salary  | 130k   | 145k  | 160k   | 175k  | 190k   │
│ Bonus        | 8%     | 12%   | 20%    | 25%   | 30%    │
│ Stock/Equity | 2%     | 5%    | 15%    | 25%   | 35%    │
│ Benefits*    | 8k     | 12k   | 15k    | 20k   | 25k    │
│ Total Comp   | 148k   | 167k  | 195k   | 225k  | 260k   │
│                                                           │
│ * Health, retirement, PTO valuation                      │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ COMPANY COMPETITIVENESS                                   │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Your Company Distribution (10 PMs in San Francisco)  │ │
│ │                                                      │ │
│ │ Below 25th: 1 person  (10%)   [↓]                   │ │
│ │ 25th-50th:  3 people  (30%)   [→]                   │ │
│ │ 50th-75th:  4 people  (40%)   [↑]                   │ │
│ │ Above 75th: 2 people  (20%)   [↑]                   │ │
│ │                                                      │ │
│ │ Average: 51st percentile (in line with market)      │ │
│ │ Recommendation: Competitive positioning is good.    │ │
│ │ Consider adjustment for 1 below-market employee.    │ │
│ │                                                      │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ INTERNAL SALARY BANDS                                     │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Role: Product Manager                                │ │
│ │ Min:  $140,000    (20th percentile of market)        │ │
│ │ Mid:  $160,000    (50th percentile of market)        │ │
│ │ Max:  $180,000    (80th percentile of market)        │ │
│ │                                                      │ │
│ │ Penetration Rates:                                   │ │
│ │ Min: 3 employees (30%)      [→]                      │ │
│ │ Mid: 5 employees (50%)      [↑] Target: 60%          │ │
│ │ Max: 2 employees (20%)      [↓] Target: 20%          │ │
│ │                                                      │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ MARKET TRENDS                                             │
│                                                           │
│ Year   | Market Median | YoY Growth | Your Company Avg   │
│ ────────────────────────────────────────────────────────  │
│ 2023   | $145,000      |    —       | $142,000           │
│ 2024   | $152,500      | +5.2%      | $149,000           │
│ 2025   | $160,000      | +4.9%      | $158,000           │
│ 2026E  | $166,400      | +3.9%      | $163,000 (est.)    │
│                                                           │
│ Your company has kept pace with market growth            │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ SALARY BAND ADJUSTMENT TOOL                               │
│                                                           │
│ [Recalculate Bands] [Update Min/Mid/Max] [Save Bands]   │
│                                                           │
│ [Create Custom Report] [Email to Finance] [Help & Info]  │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Market Data Filters**
   - Job role/title selection
   - Location filtering (single or multiple)
   - Company size range
   - Industry selection
   - Experience level filtering
   - Data source selection

2. **Salary Benchmarks**
   - Percentile display (10th, 25th, 50th, 75th, 90th)
   - Visual distribution chart
   - Company average overlay
   - Comparison analysis (above/below market)
   - Compensation component breakdown

3. **Competitiveness Analysis**
   - Company salary distribution vs. market
   - Percentile positioning for current employees
   - Identify outliers (too high/low)
   - Recommendations for adjustments

4. **Internal Salary Bands**
   - Min/Mid/Max salary bands based on market data
   - Employee penetration by band
   - Targets for distribution
   - Adjustment recommendations

5. **Market Trends**
   - Historical salary trends (3+ years)
   - Year-over-year growth rates
   - Comparison of company growth to market
   - Forecast for next year

6. **Reporting Tools**
   - Export reports as PDF/Excel
   - Custom report builder
   - Email reports to stakeholders
   - Save favorite views

### Data Model

```javascript
{
  MarketBenchmarkData: {
    benchmark_id: String (UUID),
    query_date: Date,
    data_source: Enum ("salary.com", "glassdoor", "levels.fyi", "payscale", "linkedin", "internal_survey"),
    
    filters: {
      job_role: String,
      locations: [String],
      company_size_min: Number,
      company_size_max: Number,
      industry: String,
      experience_level: String,
      education_level: String (optional)
    },
    
    market_data: {
      sample_size: Number (number of data points),
      percentile_10: Decimal,
      percentile_25: Decimal,
      median: Decimal,
      percentile_75: Decimal,
      percentile_90: Decimal,
      mean: Decimal,
      standard_deviation: Decimal,
      
      confidence_interval_lower: Decimal,
      confidence_interval_upper: Decimal
    },
    
    compensation_breakdown: {
      base_salary: {
        percentile_10: Decimal,
        percentile_25: Decimal,
        median: Decimal,
        percentile_75: Decimal,
        percentile_90: Decimal
      },
      bonus_percentage: {  // as % of salary
        percentile_10: Decimal,
        percentile_25: Decimal,
        median: Decimal,
        percentile_75: Decimal,
        percentile_90: Decimal
      },
      equity_percentage: {  // as % of total comp
        percentile_10: Decimal,
        percentile_25: Decimal,
        median: Decimal,
        percentile_75: Decimal,
        percentile_90: Decimal
      },
      benefits_value: {
        percentile_10: Decimal,
        percentile_25: Decimal,
        median: Decimal,
        percentile_75: Decimal,
        percentile_90: Decimal
      },
      total_compensation: {
        percentile_10: Decimal,
        percentile_25: Decimal,
        median: Decimal,
        percentile_75: Decimal,
        percentile_90: Decimal
      }
    },
    
    company_comparison: {
      your_company_average_salary: Decimal,
      your_company_percentile_position: Decimal,
      number_of_employees_benchmarked: Number,
      employees_by_percentile_band: {
        below_25th: Number,
        percentile_25_to_50: Number,
        percentile_50_to_75: Number,
        above_75th: Number
      }
    },
    
    salary_bands: {
      role: String,
      minimum_salary: Decimal,  // e.g., 20th percentile
      midpoint_salary: Decimal,  // e.g., 50th percentile
      maximum_salary: Decimal,   // e.g., 80th percentile
      
      penetration_analysis: {
        at_minimum_count: Number,
        at_minimum_percentage: Decimal,
        at_midpoint_count: Number,
        at_midpoint_percentage: Decimal,
        at_maximum_count: Number,
        at_maximum_percentage: Decimal,
        above_maximum_count: Number,
        above_maximum_percentage: Decimal
      },
      
      target_distribution: {
        at_minimum_target: Decimal,  // e.g., 0.10
        at_midpoint_target: Decimal,  // e.g., 0.60
        at_maximum_target: Decimal    // e.g., 0.20
      }
    },
    
    historical_trends: [{
      year: Number,
      market_median: Decimal,
      market_growth_percentage: Decimal,
      your_company_average: Decimal,
      your_company_growth_percentage: Decimal,
      market_vs_company_delta: Decimal
    }],
    
    recommendations: [String]  // e.g., "Increase salary band for role X by 3%"
  }
}
```

### UI Components Required

1. **Filter Panel**
   - Dropdown selectors for each filter
   - Multi-select for locations
   - Apply/Reset buttons
   - Filter summary display
   - Save filter view option

2. **Salary Distribution Chart**
   - Horizontal percentile chart
   - Visual bars for each percentile
   - Company average overlay
   - Legend with actual values
   - Interactive tooltips

3. **Benchmark Cards**
   - Large percentile value display
   - Range values (low-high)
   - Comparison indicator
   - Insight text

4. **Competitiveness Gauge**
   - Horizontal gauge showing percentile position
   - Color-coded zones (red/yellow/green)
   - Recommendation callout

5. **Salary Band Cards**
   - Min/Mid/Max values prominently displayed
   - Penetration chart (stacked bar)
   - Target vs. actual comparison

6. **Trends Chart**
   - Multi-line chart (market vs. company over time)
   - Year labels and growth rates
   - Legend and data labels

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text on white: 4.5:1 (use #333333 for body, #000000 for headers)
- Chart percentile bars: Blue (#0066CC, 4.5:1)
- Company average line: Red (#C62828, 4.5:1)
- Positive trend (above market): Green (#2E7D32, 4.5:1)
- Negative trend (below market): Orange (#F57C00, 4.5:1)
- Focus indicators: 3px blue (#0066CC), 3:1 minimum contrast

**Keyboard Navigation**
- Tab: Filter selectors → Apply button → Chart section → Data table → Report buttons
- Arrow keys: Navigate dropdowns, select filter values
- Enter: Apply filters, access detailed breakdowns
- Escape: Close filter dropdowns, cancel operations

**Screen Reader Support**
- Page heading: `<h1>Market Data & Benchmarking</h1>`
- Filter section: `<section aria-labelledby="filters-heading">`
  - `<h2 id="filters-heading">Filters & Parameters</h2>`
  - Each filter: `<label>Job Role:</label> <select aria-label="Select job role for benchmarking">`
- Salary distribution chart: `<div role="img" aria-labelledby="chart-description">`
  - Detailed description: "Salary distribution for Product Manager in San Francisco: 10th percentile $130,000, 25th percentile $145,000, median $160,000, 75th percentile $175,000, 90th percentile $190,000. Your company average: $158,000, positioned 1.3% below market median"
- Benchmark values: `<div aria-label="Market median salary: $160,000. Your company average: $158,000. Difference: $2,000 or 1.3% below median">`
- Salary band section: `<section aria-labelledby="bands-heading">`
  - `<h2 id="bands-heading">Internal Salary Bands</h2>`
  - Band summary: "Minimum: $140,000 (20th percentile). Midpoint: $160,000 (50th percentile). Maximum: $180,000 (80th percentile)"
- Market trends table: `<table aria-label="Salary trends 2023-2026">`
  - Row: "[Year]: Market Median $[amount], [Growth]% growth. Your Company Average $[amount], [Growth]% growth"

**Focus Management**
- Visible focus indicator (3px blue) on all interactive elements
- Initial focus on first filter (Job Role dropdown)
- Tab order: Filters → Apply → Charts → Tables → Reports
- Focus should not trap; users can tab away from any element
- Skip link: "Skip to salary benchmark charts"

**Touch Targets**
- All buttons: 44×44 minimum (action buttons 48×56px)
- Filter dropdowns: 44px height minimum
- Chart interactive areas: 44×44 minimum touch target
- Table rows: 44px height minimum
- Report links: 44×44 minimum

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce`
- No animated chart transitions
- Instant display of filter results (no fade-in)

**Error & Status Messages**
- Insufficient data: `role="alert"`
  - "Not enough data for selected filters. Try broadening your search parameters."
- Update notifications: `role="status"` aria-live="polite"
  - "Data updated. Showing benchmarks for [Role] in [Location]"
  - "Report exported successfully"
- Data freshness: `role="status"`
  - "Data last updated: April 15, 2025"

---

## Summary of Compensation Management Module

All 5 screens in the Compensation Management module prioritize:

1. **Transparency**: Clear display of complex financial information (compensation components, equity valuations, market data)
2. **Compliance**: Support for equity analysis, tax implications, and regulatory requirements
3. **Decision Support**: Data-driven tools for HR and managers to make informed compensation decisions
4. **Employee Understanding**: Simple explanations of complex concepts (vesting, equity types, market positioning)
5. **Accessibility**: WCAG 2.2 AA compliance across all screens with specific attention to:
   - Financial number formatting and clarity
   - Complex data visualization accessibility (charts with text descriptions)
   - Keyboard navigation through forms and data
   - Screen reader support for calculations and comparisons
   - Focus management in modal/detailed views
   - 44×44 pixel touch targets for all interactive elements

All screens maintain consistent design patterns, data models, and accessibility standards as established in previous modules.
