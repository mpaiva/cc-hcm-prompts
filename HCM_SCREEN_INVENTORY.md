# AI-First HCM Product: Screen Inventory

> **Accessibility Note**: All screens below must meet WCAG 2.2 AA standards. Each prompt will include specific accessibility requirements covering color contrast, keyboard navigation, screen reader compatibility, focus management, touch targets, and error handling.

---

## 1. RECRUITING & APPLICANT TRACKING

### 1.1 Job Posting Creation/Management
- **Module**: Recruiting & Applicant Tracking
- **Primary Users**: Recruiters, HR Managers
- **Purpose**: Enable recruiters to create, edit, and publish job postings with AI assistance for job descriptions
- **Key Features**:
  - Rich text editor for job description
  - Job title, department, location, salary range
  - Requirements/qualifications (skills, experience)
  - AI suggestion for missing job details
  - Publishing to career site and job boards
  - Status tracking (draft, active, closed)
  - Candidate matching insights
- **AI Integration Points**: Job description optimization, skill extraction, market-rate salary suggestions
- **Accessibility Focus**: Form labels, keyboard navigation through rich editor, error alerts

### 1.2 Job Posting View (Candidate)
- **Module**: Recruiting & Applicant Tracking
- **Primary Users**: Candidates (anonymous/logged-in)
- **Purpose**: Allow candidates to browse and view detailed job postings
- **Key Features**:
  - Job title, company, location, salary
  - Full job description, requirements, benefits
  - Apply button/call-to-action
  - Share functionality
  - Similar jobs sidebar
  - Bookmark/save for later
- **AI Integration Points**: Similar job recommendations, AI-powered job matching score
- **Accessibility Focus**: Readable fonts, sufficient color contrast, clear call-to-action button

### 1.3 Applications Dashboard (Recruiter)
- **Module**: Recruiting & Applicant Tracking
- **Primary Users**: Recruiters, HR Managers
- **Purpose**: Centralized view of all applications for job postings
- **Key Features**:
  - List/grid view of applications
  - Filter by job, status, date, rating
  - Search candidates by name, email, skills
  - Bulk actions (move to stage, email, reject)
  - AI-powered candidate ranking
  - Pipeline visualization
- **AI Integration Points**: Resume screening, candidate ranking, duplicate detection
- **Accessibility Focus**: Table structure, keyboard shortcuts for bulk actions, screen reader announcements for filtering

### 1.4 Application Details & Resume Review
- **Module**: Recruiting & Applicant Tracking
- **Primary Users**: Recruiters, Hiring Managers
- **Purpose**: Review individual applications and resumes with AI-powered insights
- **Key Features**:
  - Candidate info (name, contact, resume)
  - Embedded PDF viewer for resume
  - Application form responses
  - AI-extracted skills and experience
  - Rating/scoring system
  - Notes and comments
  - Move to next stage button
  - Interview scheduling link
- **AI Integration Points**: Resume parsing, skill extraction, gap analysis, candidate summary
- **Accessibility Focus**: PDF accessibility, keyboard navigation through sections, focus indicators for interactive elements

### 1.5 Candidate Evaluation & Scoring
- **Module**: Recruiting & Applicant Tracking
- **Primary Users**: Hiring Managers, Interviewers, Recruiters
- **Purpose**: Evaluate and score candidates against job criteria
- **Key Features**:
  - Evaluation criteria (technical skills, experience, culture fit, etc.)
  - Rating scale per criterion
  - Comments/feedback per section
  - Overall candidate score
  - Comparison view across candidates
  - AI-powered recommendation (qualified/not-qualified)
- **AI Integration Points**: Automated scoring based on criteria, competitive ranking, recommendations
- **Accessibility Focus**: Clear rating scales, error prevention (confirmation on low scores), text alternatives for visual indicators

### 1.6 Interview Scheduling
- **Module**: Recruiting & Applicant Tracking
- **Primary Users**: Recruiters, Hiring Managers, Candidates
- **Purpose**: Schedule interviews and send calendar invites
- **Key Features**:
  - Calendar view with interviewer availability
  - Interview type selector (phone, video, in-person)
  - Time slot selection
  - Interviewer assignment
  - Candidate notification
  - Meeting link generation (Zoom, Teams, etc.)
  - Timezone handling
- **AI Integration Points**: Optimal time slot suggestions, interviewer matching
- **Accessibility Focus**: Calendar accessibility, timezone clarity, keyboard-navigable date picker

### 1.7 Interview Feedback Form
- **Module**: Recruiting & Applicant Tracking
- **Primary Users**: Hiring Managers, Interviewers
- **Purpose**: Capture feedback from interviews with AI-powered analysis
- **Key Features**:
  - Interview details (date, interviewer, candidate)
  - Rating scales (communication, technical ability, culture fit, etc.)
  - Free-text feedback
  - Recommendation (advance, reject, maybe)
  - Comparison to job criteria
  - AI summary of feedback
- **AI Integration Points**: Feedback summarization, bias detection, recommendation insights
- **Accessibility Focus**: Form labels, clear radio button groups, error messages for incomplete forms

### 1.8 Offer Management
- **Module**: Recruiting & Applicant Tracking
- **Primary Users**: HR Managers, Hiring Managers
- **Purpose**: Create, send, and track job offers
- **Key Features**:
  - Offer template selection
  - Compensation details (salary, bonus, benefits, start date)
  - Offer letter generation
  - Send to candidate (email/portal)
  - Offer tracking (sent, viewed, signed)
  - Acceptance/rejection status
  - Counter-offer handling
- **AI Integration Points**: Competitive offer suggestions, market benchmarking
- **Accessibility Focus**: PDF accessibility, clear action buttons, status indicators

---

## 2. ONBOARDING & OFFBOARDING

### 2.1 New Hire Checklist
- **Module**: Onboarding & Offboarding
- **Primary Users**: HR Managers, Managers, New Hires
- **Purpose**: Track onboarding tasks and milestones for new employees
- **Key Features**:
  - Pre-boarding checklist (before start date)
  - Day 1 orientation tasks
  - Week 1/30/90 day checklists
  - Task assignment to different owners (HR, manager, IT, etc.)
  - Task completion tracking
  - Progress dashboard
  - Resource links (policies, systems, etc.)
- **AI Integration Points**: Checklist personalization based on role, progress analytics, task suggestions
- **Accessibility Focus**: Checkbox states, progress indicator, expandable sections

### 2.2 Document Collection & E-Signature
- **Module**: Onboarding & Offboarding
- **Primary Users**: New Hires, HR Managers
- **Purpose**: Collect required documents and obtain digital signatures
- **Key Features**:
  - Document upload interface
  - Pre-filled form fields (name, address, etc.)
  - E-signature integration (DocuSign, HelloSign, etc.)
  - Required vs. optional documents
  - Deadline tracking
  - Completion status
  - Archive signed documents
- **AI Integration Points**: Form field auto-fill, document validation, expiration reminders
- **Accessibility Focus**: File upload instructions, document preview, focus on signature areas

### 2.3 Background Check Status
- **Module**: Onboarding & Offboarding
- **Primary Users**: HR Managers, New Hires
- **Purpose**: Track background check progress and results
- **Key Features**:
  - Background check provider integration
  - Status updates (pending, in-progress, complete, issue)
  - Results summary (pass/fail/review)
  - Compliance notes
  - Clear and fair records access
  - Action items for issues
- **AI Integration Points**: Risk assessment, compliance monitoring
- **Accessibility Focus**: Clear status labels, alert announcements for critical updates

### 2.4 IT & Systems Access Setup
- **Module**: Onboarding & Offboarding
- **Primary Users**: IT Administrators, HR Managers
- **Purpose**: Request and provision system access for new hires
- **Key Features**:
  - Access request form based on role
  - Systems to provision (email, laptop, software licenses, etc.)
  - Approval workflow
  - Provisioning status tracker
  - Access confirmation email
  - Deprovisioning requests (for offboarding)
- **AI Integration Points**: Access level recommendations based on role, template suggestions
- **Accessibility Focus**: Multi-step form, clear instructions, status notifications

### 2.5 Equipment & Supply Request
- **Module**: Onboarding & Offboarding
- **Primary Users**: New Hires, HR Managers, Procurement
- **Purpose**: Request and track equipment for new employees
- **Key Features**:
  - Equipment catalog (laptop, monitor, phone, etc.)
  - Role-based default selections
  - Shipping address confirmation
  - Approval workflow
  - Delivery tracking
  - Return instructions (offboarding)
- **AI Integration Points**: Equipment recommendations by role, budget optimization
- **Accessibility Focus**: Product selection interface, clear item descriptions, order confirmation

### 2.6 Orientation & Training Plan
- **Module**: Onboarding & Offboarding
- **Primary Users**: New Hires, Managers, HR Managers
- **Purpose**: Assign and track orientation activities and training courses
- **Key Features**:
  - Training module assignments
  - Videos, documents, and interactive content
  - Progress tracking
  - Completion certificates
  - Quiz/assessment modules
  - Manager check-ins scheduled
  - First 90-day learning objectives
- **AI Integration Points**: Personalized learning paths, progress predictions, knowledge gap identification
- **Accessibility Focus**: Video captions, transcript availability, accessible course navigation

### 2.7 Manager Onboarding Workflow
- **Module**: Onboarding & Offboarding
- **Primary Users**: Managers
- **Purpose**: Guide managers through the onboarding process for their new direct reports
- **Key Features**:
  - One-on-one meeting templates
  - Team introduction checklist
  - Goal-setting guidance
  - Day 30/60/90 check-in reminders
  - Feedback requests
  - Progress notes
- **AI Integration Points**: Meeting talking points, progress recommendations, culture integration tips
- **Accessibility Focus**: Clear milestones, reminder notifications, readable text

### 2.8 Offboarding Checklist
- **Module**: Onboarding & Offboarding
- **Primary Users**: HR Managers, Managers, IT
- **Purpose**: Manage exit process and knowledge transfer
- **Key Features**:
  - Final paycheck and benefits info
  - Asset return checklist (laptop, badge, etc.)
  - Access revocation workflow
  - Knowledge transfer tasks
  - Rehire eligibility status
  - Exit survey/interview request
  - Alumni network optionality
- **AI Integration Points**: Risk assessment for critical role, knowledge capture recommendations
- **Accessibility Focus**: Clear exit information, status tracking, final document collection

---

## 3. PERFORMANCE MANAGEMENT

### 3.1 Goal Setting & OKRs
- **Module**: Performance Management
- **Primary Users**: Employees, Managers
- **Purpose**: Create and align goals for performance periods
- **Key Features**:
  - Goal creation wizard
  - Goal type (individual, team, company)
  - SMART goal guidance
  - Alignment visualization (parent-child goals)
  - Timeline and milestones
  - Key results (OKRs)
  - Progress tracking
  - AI feedback on goal quality
- **AI Integration Points**: Goal suggestions based on role, alignment checking, success prediction
- **Accessibility Focus**: Form clarity, visual alignment tree accessibility, progress indicators

### 3.2 Goal Progress Tracking
- **Module**: Performance Management
- **Primary Users**: Employees, Managers
- **Purpose**: Monitor progress toward goals throughout the period
- **Key Features**:
  - Progress input form
  - Status updates (on track, at-risk, blocked)
  - Milestone tracking
  - Key result measurements
  - Comments and context
  - AI-powered blocker detection and suggestions
  - Check-in nudges
- **AI Integration Points**: Anomaly detection (off-track goals), contextual suggestions, predictive completion dates
- **Accessibility Focus**: Status labels, form structure, notification clarity

### 3.3 360-Degree Feedback Request
- **Module**: Performance Management
- **Primary Users**: Managers, Employees, Peers
- **Purpose**: Request and collect multi-source feedback
- **Key Features**:
  - Feedback round creation
  - Recipient and rater selection
  - Anonymous feedback option
  - Custom feedback questions
  - Reminders to complete feedback
  - Response tracking
  - Rater pool management
- **AI Integration Points**: Bias detection, rater diversity checking, anonymous feedback safety
- **Accessibility Focus**: Form instructions, anonymous submission confirmation, completion reminders

### 3.4 Feedback Submission Form
- **Module**: Performance Management
- **Primary Users**: Managers, Peers, Direct Reports
- **Purpose**: Submit structured feedback on colleagues or direct reports
- **Key Features**:
  - Competency/skill-based questions
  - Rating scales
  - Open-ended comment fields
  - Guidance on constructive feedback
  - Anonymous toggle
  - Submit and confirmation
  - Follow-up actions
- **AI Integration Points**: Feedback quality scoring, bias warnings, constructive language suggestions
- **Accessibility Focus**: Clear rating scales, text area instructions, confirmation messages

### 3.5 Performance Review Form
- **Module**: Performance Management
- **Primary Users**: Managers, Employees
- **Purpose**: Complete formal performance review with rating and summary
- **Key Features**:
  - Review period details
  - Goal achievement assessment
  - Competency ratings
  - Strengths and development areas
  - Summary rating/overall performance
  - 360 feedback summary integration
  - Acknowledgment from employee
  - Career development discussion
- **AI Integration Points**: Review summarization, 360 synthesis, rating distribution checking, calibration recommendations
- **Accessibility Focus**: Multi-section form, clear rating scales, text alternative for visual summaries

### 3.6 One-on-One Meeting Notes
- **Module**: Performance Management
- **Primary Users**: Managers, Employees
- **Purpose**: Document discussions and action items from regular check-ins
- **Key Features**:
  - Meeting template
  - Date and attendee info
  - Agenda items
  - Discussion notes
  - Action items with ownership and due dates
  - Goal progress updates
  - Next meeting date
  - AI-powered summary and action extraction
- **AI Integration Points**: Automatic action item extraction, meeting summary generation, follow-up suggestions
- **Accessibility Focus**: Text input fields, checkbox lists, clear action item status

### 3.7 Career Development Plan
- **Module**: Performance Management
- **Primary Users**: Employees, Managers
- **Purpose**: Create personalized development plans for career growth
- **Key Features**:
  - Career goal definition
  - Skills to develop
  - Learning path assignment
  - Mentor/sponsor relationships
  - Timeline and milestones
  - Development resources
  - Progress tracking
  - Succession planning view
- **AI Integration Points**: Career path recommendations, skill gap analysis, learning course suggestions, mentor matching
- **Accessibility Focus**: Clear progression visualization, readable text, accessible learning resource links

### 3.8 Calibration Session (Manager View)
- **Module**: Performance Management
- **Primary Users**: Managers (group calibration)
- **Purpose**: Calibrate performance ratings across teams to ensure consistency
- **Key Features**:
  - Team member rating display
  - Distribution visualization
  - Peer comparison
  - Rating adjustment tools
  - Justification notes for changes
  - Final approval workflow
  - Consistency checking
- **AI Integration Points**: Rating consistency flagging, bias detection, outlier identification, benchmarking
- **Accessibility Focus**: Comparison table accessibility, distribution chart alternatives, clear justification inputs

---

## 4. EMPLOYEE SELF-SERVICE

### 4.1 Employee Profile & Directory
- **Module**: Employee Self-Service
- **Primary Users**: All Employees
- **Purpose**: View and edit personal employee information and access company directory
- **Key Features**:
  - Personal info (name, contact, address, etc.)
  - Profile photo
  - Department, team, manager, direct reports
  - Skills and certifications
  - Contact preferences
  - Directory search and filters
  - Manager/peer profiles
  - Org chart view
- **AI Integration Points**: Profile suggestions for skills/certifications, colleague recommendations
- **Accessibility Focus**: Photo alt-text, readable org chart, search functionality, privacy controls

### 4.2 Benefits Enrollment
- **Module**: Employee Self-Service
- **Primary Users**: All Employees
- **Purpose**: Enroll and manage benefits during open enrollment periods
- **Key Features**:
  - Benefits plan options (health, dental, vision, 401k, etc.)
  - Plan comparisons
  - Cost calculator
  - Dependent information
  - Enrollment confirmation
  - Ongoing management
  - Life event changes
  - Subsidy/contribution calculations
- **AI Integration Points**: Plan recommendations based on profile, cost-benefit analysis, optimal coverage suggestions
- **Accessibility Focus**: Comparison tables, cost calculator clarity, form labels, confirmation summaries

### 4.3 Time Off Request
- **Module**: Employee Self-Service
- **Primary Users**: All Employees
- **Purpose**: Request and track time off (vacation, sick, PTO, etc.)
- **Key Features**:
  - Time off type selector
  - Date range picker
  - Available balance display
  - Notes/reason
  - Manager approval workflow
  - Coverage/handoff notes
  - Submission confirmation
  - Request history
- **AI Integration Points**: Optimal timing suggestions, coverage recommendations, balance forecasting
- **Accessibility Focus**: Date picker accessibility, clear balance information, approval status notifications

### 4.4 Time Off Calendar
- **Module**: Employee Self-Service
- **Primary Users**: All Employees, Managers
- **Purpose**: View team and company time off calendar
- **Key Features**:
  - Team member calendar
  - Company-wide holidays
  - Time off by type/color
  - Filter by team/person
  - Coverage view (who's available)
  - Blackout dates
  - Team view for managers
- **AI Integration Points**: Coverage alerts, optimal project timing suggestions
- **Accessibility Focus**: Calendar navigation, color with text labels, list view alternative

### 4.5 Expense Report
- **Module**: Employee Self-Service
- **Primary Users**: All Employees
- **Purpose**: Submit, track, and manage reimbursement requests
- **Key Features**:
  - Expense type selector (travel, meals, supplies, etc.)
  - Date and amount
  - Receipt upload
  - Project/cost center allocation
  - Mileage tracking
  - Submission and approval workflow
  - Status tracking
  - Reimbursement method
- **AI Integration Points**: Receipt scanning, amount auto-fill, duplicate detection, category suggestions, policy compliance checking
- **Accessibility Focus**: File upload instructions, receipt image alt-text, form clarity, approval notifications

### 4.6 Pay Stub & Payroll Information
- **Module**: Employee Self-Service
- **Primary Users**: All Employees
- **Purpose**: View payroll information and access pay stubs
- **Key Features**:
  - Current pay stub download
  - Pay stub history
  - Earnings breakdown (gross, deductions, etc.)
  - Tax information
  - Direct deposit verification
  - Payroll calendar
  - Year-to-date totals
  - Tax withholding adjustments
- **AI Integration Points**: Tax optimization suggestions, net pay forecasting
- **Accessibility Focus**: PDF accessibility, table clarity, downloadable alternatives, security

### 4.7 Tax Documents (W2, 1099, etc.)
- **Module**: Employee Self-Service
- **Primary Users**: All Employees
- **Purpose**: Access and download tax documents
- **Key Features**:
  - Document type selector (W2, 1099, 1098-T, etc.)
  - Year selection
  - Digital copy access
  - Print option
  - Download to tax software
  - eSignature for verification
  - Support contact for questions
- **AI Integration Points**: Document availability notifications, tax software integration
- **Accessibility Focus**: PDF accessibility, download instructions, security measures

### 4.8 Documents & Records
- **Module**: Employee Self-Service
- **Primary Users**: All Employees
- **Purpose**: Central repository for personal employment documents
- **Key Features**:
  - Job offer
  - Employment contract
  - Certifications/training records
  - Policy acknowledgments
  - I-9 verification
  - Direct deposit authorization
  - Emergency contact forms
  - Document upload (personal docs)
  - Document signature requests
- **AI Integration Points**: Document organization, expiration tracking, missing document alerts
- **Accessibility Focus**: Document preview, searchability, signature field clarity

---

## 5. LEARNING & DEVELOPMENT

### 5.1 Learning Catalog
- **Module**: Learning
- **Primary Users**: All Employees
- **Purpose**: Browse and discover available learning opportunities
- **Key Features**:
  - Course/learning resource listings
  - Filters (topic, level, duration, format)
  - Search functionality
  - Course previews
  - Instructor/provider info
  - Enrollment/signup
  - Reviews and ratings
  - Prerequisites display
  - Completion time estimates
- **AI Integration Points**: Personalized recommendations, skill-based filtering, role-appropriate suggestions
- **Accessibility Focus**: Filter accessibility, course preview navigation, search functionality

### 5.2 Course Enrollment & Progress
- **Module**: Learning
- **Primary Users**: All Employees
- **Purpose**: Enroll in courses and track learning progress
- **Key Features**:
  - Course enrollment confirmation
  - Learning objectives display
  - Progress tracker (% complete)
  - Module/lesson navigation
  - Bookmark and note-taking
  - Assessment/quiz modules
  - Completion certificate
  - Resume integration
- **AI Integration Points**: Adaptive pacing, progress predictions, knowledge gap assessments
- **Accessibility Focus**: Video captions, transcript availability, keyboard navigation, pause/resume functionality

### 5.3 Learning Path
- **Module**: Learning
- **Primary Users**: All Employees, Managers
- **Purpose**: Follow structured sequences of courses for skill development
- **Key Features**:
  - Path goal and outcome
  - Sequential course modules
  - Recommended duration
  - Progress dashboard
  - Milestone markers
  - Completion tracking
  - Path analytics
  - Peer progress (anonymized)
- **AI Integration Points**: Personalized path recommendations, progress analytics, skill certification
- **Accessibility Focus**: Clear milestone navigation, progress visualization, course organization

### 5.4 Skills & Certifications
- **Module**: Learning
- **Primary Users**: All Employees, Managers
- **Purpose**: Track and validate skills and professional certifications
- **Key Features**:
  - Skills inventory (self-assessed and verified)
  - Certification tracking (dates, renewal, verification)
  - Endorsements from peers/managers
  - Skills assessment/testing
  - Skill development plans
  - Industry certifications directory
  - Skill-to-role mapping
- **AI Integration Points**: Skill validation, certification recommendations, skill gap analysis
- **Accessibility Focus**: Endorsement notifications, skill level clarity, assessment instructions

### 5.5 Learning Recommendations
- **Module**: Learning
- **Primary Users**: All Employees, Managers
- **Purpose**: Receive personalized learning recommendations
- **Key Features**:
  - Curated recommendation feed
  - Recommendation reasons
  - Role-based suggestions
  - Skill gap-based suggestions
  - Goal-based suggestions
  - Manager recommendations
  - Accept/dismiss recommendations
- **AI Integration Points**: ML-powered personalization, skill gap analysis, role trajectory recommendations
- **Accessibility Focus**: Clear recommendation descriptions, dismissal confirmation, notification preferences

---

## 6. COMPENSATION MANAGEMENT

### 6.1 Compensation Statement
- **Module**: Compensation Management
- **Primary Users**: All Employees
- **Purpose**: View total compensation package
- **Key Features**:
  - Salary/base pay
  - Bonus structure and estimates
  - Stock/equity information
  - Benefits value calculation
  - Retirement contributions
  - PTO valuation
  - Total compensation summary
  - Year-over-year changes
- **AI Integration Points**: Compensation breakdown, market position visualization
- **Accessibility Focus**: Table clarity, large number formatting, value breakdown hierarchy

### 6.2 Salary Review & Adjustment
- **Module**: Compensation Management
- **Primary Users**: Managers, HR Managers
- **Purpose**: Recommend and manage salary adjustments
- **Key Features**:
  - Employee list with current salaries
  - Adjustment recommendation form
  - Justification (promotion, market adjustment, etc.)
  - Market data comparison
  - Approval workflow
  - Effective date setting
  - Communication template
  - Adjustment history
- **AI Integration Points**: Salary recommendations based on market data and performance, equity analysis
- **Accessibility Focus**: Form clarity, approval notifications, market data visualization

### 6.3 Bonus & Variable Pay Management
- **Module**: Compensation Management
- **Primary Users**: Managers, HR Managers, Executives
- **Purpose**: Manage bonus structures and variable compensation
- **Key Features**:
  - Bonus plan templates
  - Target bonus levels by role
  - Performance metrics/goals
  - Payout calculations
  - Approvals workflow
  - Payout processing
  - History and actuals
  - Communication to employees
- **AI Integration Points**: Performance-based calculations, equity checking, payout optimization
- **Accessibility Focus**: Calculation explanation, approval status, payout notifications

### 6.4 Equity & Stock Options
- **Module**: Compensation Management
- **Primary Users**: Executives, Finance, Employees
- **Purpose**: Track and manage equity grants and stock options
- **Key Features**:
  - Grant details (shares, vesting schedule, strike price)
  - Vesting tracker
  - Current value calculations
  - Exercise options (for stock options)
  - Tax implications info
  - Grant history
  - Equity grant communications
- **AI Integration Points**: Valuation calculations, tax planning suggestions, vesting forecasts
- **Accessibility Focus**: Vesting schedule visualization, number formatting, financial terminology clarity

### 6.5 Market Data & Benchmarking
- **Module**: Compensation Management
- **Primary Users**: HR Managers, Finance
- **Purpose**: Access market compensation data for benchmarking
- **Key Features**:
  - Job role compensation benchmarks
  - Market data by location, industry, company size
  - Internal compensation analysis
  - Competitiveness analysis
  - Salary bands
  - Market trend reports
  - Data source information
- **AI Integration Points**: Predictive market trends, compensation gap analysis, recommendation engine
- **Accessibility Focus**: Data table accessibility, chart alternatives, legend clarity

---

## 7. AI-FIRST FEATURES (Cross-Module)

### 7.1 AI Resume Screening Assistant
- **Module**: AI-First / Recruiting
- **Primary Users**: Recruiters, Hiring Managers
- **Purpose**: AI-powered resume parsing and candidate matching
- **Key Features**:
  - Automated skill extraction
  - Experience level assessment
  - Education and certification identification
  - AI qualification scoring
  - Red flags/gaps identification
  - Comparison to job requirements
  - Bias detection feedback
  - Reasoning/explainability (why scored this way)
- **AI Integration Points**: Resume parsing (NLP), skill extraction, scoring models, bias mitigation
- **Accessibility Focus**: Clear scoring explanation, extracted data accuracy verification, human review workflow

### 7.2 AI Job Matching Engine
- **Module**: AI-First / Recruiting
- **Primary Users**: Candidates, Recruiters
- **Purpose**: AI-powered matching of candidates to opportunities
- **Key Features**:
  - Candidate skill profile
  - Job requirement matching
  - Match percentage/score
  - Reasoning for match
  - Gap analysis
  - Development recommendations
  - Similar opportunities
  - Job recommendations feed
- **AI Integration Points**: Skill matching (embeddings), job profile analysis, recommendation ranking
- **Accessibility Focus**: Match score explanation, job description clarity, recommendations list accessibility

### 7.3 AI Interview Insights
- **Module**: AI-First / Recruiting
- **Primary Users**: Hiring Managers, Recruiters
- **Purpose**: AI analysis of interview performance and candidate fit
- **Key Features**:
  - Interview recording/transcript
  - AI-powered sentiment analysis
  - Communication style assessment
  - Technical depth evaluation
  - Cultural fit indicators
  - Key moments flagging
  - Comparative insights (vs. other candidates)
  - Recommendation score
  - Interview summary
- **AI Integration Points**: Speech-to-text, sentiment analysis, cultural fit models, comparative ranking
- **Accessibility Focus**: Transcript accuracy, flagged moment clarification, summary readability

### 7.4 AI Performance Insights
- **Module**: AI-First / Performance Management
- **Primary Users**: Managers, Executives, HR
- **Purpose**: AI-driven performance analysis and predictive insights
- **Key Features**:
  - Goal achievement predictions
  - Performance trend analysis
  - Risk of attrition indicators
  - High performer identification
  - Promotion readiness scoring
  - Team health metrics
  - Outlier detection (over/underperforming)
  - Development opportunity recommendations
- **AI Integration Points**: Time series forecasting, attrition modeling, performance clustering, anomaly detection
- **Accessibility Focus**: Prediction confidence explanation, metric definitions, alert clarity

### 7.5 AI Learning Recommendations
- **Module**: AI-First / Learning
- **Primary Users**: All Employees, Managers
- **Purpose**: Personalized learning paths based on goals, role, and performance
- **Key Features**:
  - Skill gap analysis
  - Recommended courses/resources
  - Learning path creation
  - Estimated time to proficiency
  - Success rate predictions
  - Peer comparison (anonymized)
  - Manager override/customization
  - Progress predictions
- **AI Integration Points**: Collaborative filtering, skill graph analysis, learner modeling, path optimization
- **Accessibility Focus**: Recommendation clarity, learning difficulty assessment, estimated time accuracy

### 7.6 AI Career Pathing
- **Module**: AI-First / Performance + Learning
- **Primary Users**: All Employees, Managers
- **Purpose**: AI-generated career development recommendations
- **Key Features**:
  - Current role analysis
  - Potential next roles
  - Skills required for advancement
  - Timeline to readiness
  - Success probability
  - Learning path to preparation
  - Peer progression benchmarks (anonymized)
  - Internal opportunity matching
  - External market context
- **AI Integration Points**: Career progression models, skill path optimization, role requirement analysis
- **Accessibility Focus**: Career path visualization, skill requirement clarity, timeline readability

### 7.7 AI Compensation Optimization
- **Module**: AI-First / Compensation
- **Primary Users**: Finance, HR Managers
- **Purpose**: AI-driven compensation analysis and optimization
- **Key Features**:
  - Market competitiveness analysis
  - Equity gap identification
  - Promotion adjustment recommendations
  - Budget allocation optimization
  - Pay equity analysis
  - Retention risk scoring
  - Salary band recommendations
  - What-if analysis tools
- **AI Integration Points**: Market data analysis, equity modeling, budget optimization, retention prediction
- **Accessibility Focus**: Analysis result clarity, recommendation reasoning, budget visualization

### 7.8 AI Assistant (Conversational)
- **Module**: AI-First (Cross-Module)
- **Primary Users**: All Users
- **Purpose**: Natural language assistant for HR-related questions and tasks
- **Key Features**:
  - Chat interface
  - Multi-turn conversation
  - Questions about policies, processes, dates
  - Task assistance (schedule meeting, find courses, etc.)
  - Knowledge base search
  - Document references
  - Escalation to HR team
  - Conversation history
- **AI Integration Points**: LLM-based conversation, information retrieval, task automation, intent recognition
- **Accessibility Focus**: Chat interface keyboard navigation, conversation context clarity, plain language responses

---

## Summary Statistics

- **Total Screens**: 48
- **Recruiting & Applicant Tracking**: 8 screens
- **Onboarding & Offboarding**: 8 screens
- **Performance Management**: 8 screens
- **Employee Self-Service**: 8 screens
- **Learning & Development**: 5 screens
- **Compensation Management**: 5 screens
- **AI-First Features**: 8 screens

---

## Next Steps

1. **Review & Feedback**: Validate screen list and organizational structure
2. **Prioritization**: Identify which screens to tackle first for prompt creation
3. **Prompt Development**: Create comprehensive, accessibility-first prompts for each screen
4. **Figma Integration**: Move prompts into design-ready format with wireframe/component guidance

