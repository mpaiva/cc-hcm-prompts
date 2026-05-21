# AI-First HCM Product Design Library

A comprehensive, production-ready design specification library for a modern AI-first Human Resource Information System (HRIS). This library contains detailed screen prompts for 48 screens across 7 core modules, with mandatory WCAG 2.2 AA accessibility standards and explainable AI integration throughout.

## 📋 Project Overview

This design library serves as a single source of truth for building a next-generation HRM platform that combines powerful HR functionality with AI-powered insights and automation. Every screen is documented with wireframes, workflows, data models, and accessibility requirements suitable for design teams, developers, and product managers.

**Total Screens**: 48  
**Total Modules**: 7  
**Accessibility Standard**: WCAG 2.2 AA (Mandatory)  
**AI Integration**: Throughout all modules with explainability focus

---

## 📁 Module Structure

### 1. Recruiting & Applicant Tracking (8 screens)
End-to-end recruitment workflow from job posting to offer management with AI-powered resume screening and candidate matching.

**Screens:**
- 1.1: Job Posting Creation/Management
- 1.2: Job Posting View (Candidate)
- 1.3: Applications Dashboard (Recruiter)
- 1.4: Application Details & Resume Review
- 1.5: Candidate Evaluation & Scoring
- 1.6: Interview Scheduling
- 1.7: Interview Feedback Form
- 1.8: Offer Management

**Key AI Features**: Resume parsing, skill extraction, candidate ranking, bias detection, competitive offer suggestions

**File**: `RECRUITING_SCREEN_PROMPTS.md` (previously completed)

---

### 2. Onboarding & Offboarding (8 screens)
Streamlined onboarding and offboarding processes with task management, document collection, background checks, and access provisioning.

**Screens:**
- 2.1: New Hire Checklist
- 2.2: Document Collection & E-Signature
- 2.3: Background Check Status
- 2.4: IT & Systems Access Setup
- 2.5: Equipment & Supply Request
- 2.6: Onboarding Progress Dashboard
- 2.7: Offboarding Checklist
- 2.8: Exit Interview & Feedback

**Key Features**: Task automation, progress tracking, document workflow, system integration

**File**: `ONBOARDING_SCREEN_PROMPTS.md` (previously completed)

---

### 3. Performance Management (8 screens)
Goal setting, performance reviews, feedback, and career development planning with AI-driven insights.

**Screens:**
- 3.1: Goal Setting & OKR Management
- 3.2: Goal Progress Tracking
- 3.3: Continuous Feedback & Recognition
- 3.4: Performance Review Form
- 3.5: One-on-One Meeting Notes
- 3.6: Career Development Plan
- 3.7: Calibration Session
- 3.8: Performance Analytics Dashboard

**Key AI Features**: Goal recommendations, performance predictions, bias mitigation in reviews, calibration insights

**File**: `PERFORMANCE_SCREEN_PROMPTS.md` + `PERFORMANCE_SCREEN_PROMPTS_PART2_COMPLETE.md` (previously completed)

---

### 4. Employee Self-Service (8 screens)
Complete self-service portal for employee profile management, benefits, time off, expenses, payroll, and documents.

**Screens:**
- 4.1: Employee Profile & Directory
- 4.2: Benefits Enrollment
- 4.3: Time Off Request
- 4.4: Time Off Calendar
- 4.5: Expense Report
- 4.6: Pay Stub & Payroll Information
- 4.7: Tax Documents (W2, 1099, etc.)
- 4.8: Documents & Records

**Key Features**: Self-service automation, OCR receipt processing, cost calculators, document management

**Files**: 
- `SELF_SERVICE_SCREEN_PROMPTS.md` (screens 4.1-4.3)
- `SELF_SERVICE_SCREEN_PROMPTS_PART2.md` (screens 4.4-4.8)

(Previously completed)

---

### 5. Learning & Development (5 screens)
Personalized learning platform with AI-powered course recommendations, skill tracking, and learning paths.

**Screens:**
- 5.1: Learning Catalog
- 5.2: Course Enrollment & Progress
- 5.3: Learning Path
- 5.4: Skills & Certifications
- 5.5: Learning Recommendations

**Key AI Features**: Personalized recommendations based on skill gaps, role, and goals; adaptive learning pacing; skill validation

**File**: `LEARNING_DEVELOPMENT_SCREEN_PROMPTS.md`

---

### 6. Compensation Management (5 screens)
Total compensation transparency, salary management, bonus structures, equity tracking, and market benchmarking.

**Screens:**
- 6.1: Compensation Statement
- 6.2: Salary Review & Adjustment
- 6.3: Bonus & Variable Pay Management
- 6.4: Equity & Stock Options
- 6.5: Market Data & Benchmarking

**Key AI Features**: Market analysis, equity gap detection, salary recommendations, compensation optimization

**File**: `COMPENSATION_MANAGEMENT_SCREEN_PROMPTS.md`

---

### 7. AI-First Features (8 screens)
Cross-module AI capabilities including conversational assistant, advanced analytics, and optimization tools.

**Screens:**
- 7.1: AI Resume Screening Assistant
- 7.2: AI Job Matching Engine
- 7.3: AI Interview Insights
- 7.4: AI Performance Insights
- 7.5: AI Learning Recommendations
- 7.6: AI Career Pathing
- 7.7: AI Compensation Optimization
- 7.8: AI Assistant (Conversational)

**Key Features**: Explainable AI, human-in-the-loop workflows, predictive analytics, natural language processing

**Files**:
- `AI_FIRST_FEATURES_SCREEN_PROMPTS_PART1.md` (screens 7.1-7.4)
- `AI_FIRST_FEATURES_SCREEN_PROMPTS_PART2.md` (screens 7.5-7.8)

---

## 🎯 What's Included in Each Screen Prompt

### 1. **Wireframe Layout**
ASCII-art wireframes showing the complete screen layout, component positioning, and data display hierarchy.

### 2. **Key Features & Workflows**
Detailed descriptions of all features, user interactions, and process flows. Includes:
- Feature descriptions
- Step-by-step workflows
- User interaction patterns
- Data validation rules
- Error handling scenarios

### 3. **Data Model**
Complete JavaScript-style data structures defining:
- All fields with types and constraints
- Relationships between entities
- Enums for standardized values
- Optional vs. required fields
- Nested objects and arrays

### 4. **UI Components Required**
Specification of all UI components needed:
- Form elements (inputs, dropdowns, date pickers)
- Data display components (tables, cards, charts)
- Navigation components
- Modal and overlay patterns
- Button and action components

### 5. **WCAG 2.2 AA Accessibility Requirements**

#### Color Contrast
- Text on background: 4.5:1 minimum ratio
- Specific color values for different states
- Focus indicators: 3:1 minimum contrast

#### Keyboard Navigation
- Complete Tab order through all interactive elements
- Arrow key support for lists and dropdowns
- Enter/Space for activation
- Escape for closing modals
- Keyboard shortcuts where applicable

#### Screen Reader Support
- ARIA labels for all interactive elements
- aria-live regions for dynamic content
- aria-label and aria-describedby for clarity
- Semantic HTML structure
- Proper heading hierarchy
- Table headers with scope attributes

#### Focus Management
- Visible focus indicators on all interactive elements
- Skip links for navigation
- Focus traps in modals
- Focus return after modal close
- Initial focus placement strategy

#### Touch Targets
- All interactive elements: 44×44 pixels minimum
- Action buttons: 48×56 pixels
- Adequate spacing between targets
- Mobile-friendly sizing

#### Motion & Animation
- Respect `prefers-reduced-motion: reduce` media query
- No auto-playing animations
- Smooth transitions (if animations exist)
- Instant display as fallback

#### Error Handling
- All errors announced with `role="alert"`
- Clear, actionable error messages
- Form validation with field-level feedback
- Status updates with `role="status"` and aria-live

### 6. **AI Integration Points**
Where applicable, screens include:
- AI recommendation triggers
- Machine learning models involved
- Explainability approach
- Confidence/uncertainty communication
- Human review workflows
- Bias detection and mitigation

### 7. **Dependencies & Integrations**
External systems and screens that interact:
- Data flow between modules
- Third-party integrations (payroll, benefits, etc.)
- API requirements
- Authentication/authorization considerations

### 8. **Edge Cases & Error Scenarios**
Special situations and how to handle them:
- Data validation edge cases
- Permission/access restrictions
- Empty states
- Error recovery
- Conflicting data scenarios

### 9. **Success Metrics**
How to measure if the screen is working well:
- User engagement metrics
- Task completion rates
- Performance benchmarks
- Accessibility compliance verification

---

## 🎨 Design System Alignment

All screens follow consistent patterns for:

### Forms
- Standard input field styling
- Consistent label positioning
- Error message display
- Required field indicators
- Clear submit/cancel buttons

### Data Display
- Sortable/filterable tables with sticky headers
- Card-based layouts for grouped data
- Progress bars with percentage labels
- Color-coded status indicators
- Pagination or infinite scroll patterns

### Navigation
- Breadcrumb trails
- Consistent tab patterns
- Sidebar navigation where applicable
- Modal overlay patterns
- Action button styling

### Interactive Elements
- Consistent button styles (primary/secondary/tertiary)
- Hover and active states
- Loading indicators
- Success/error notifications
- Confirmation dialogs for destructive actions

---

## ♿ Accessibility Commitment

**Every screen in this library meets WCAG 2.2 AA standards.** This is not optional—accessibility requirements are embedded in each screen specification.

### Why WCAG 2.2 AA?
- **AA Level**: Ensures usability for 95%+ of users, including those with disabilities
- **WCAG 2.2**: Latest accessibility guidance (2023)
- **Inclusive by Design**: Not an afterthought, but built into every feature

### What's Covered
- ✅ Visual accessibility (contrast, focus indicators, text sizing)
- ✅ Motor accessibility (keyboard navigation, touch targets)
- ✅ Cognitive accessibility (clear language, predictable patterns)
- ✅ Hearing accessibility (captions, transcripts, visual indicators)
- ✅ Temporal accessibility (no time-based restrictions, animation control)

---

## 🤖 AI-First Philosophy

This library emphasizes AI as an augmentation tool, not a replacement:

### Explainability
Every AI recommendation includes:
- Clear reasoning for the suggestion
- Confidence/uncertainty levels
- Supporting evidence from data
- Links to review underlying data

### Human-in-the-Loop
- AI recommends, humans decide
- Easy override capability
- Audit trails for decisions
- Escalation paths for complex cases

### Bias Mitigation
- Bias detection in resume screening
- Equity analysis in compensation
- Demographic parity checks
- Fairness-aware algorithms

### Transparency
- "Why was I recommended this?" answers
- "What data informed this?" explanations
- Clear model limitations
- Regular model performance reviews

---

## 🚀 How to Use This Library

### For Design Teams
1. Pick a screen from the relevant module
2. Review the wireframe for layout and components
3. Note all interactive states and transitions
4. Check accessibility requirements for color/contrast
5. Use UI components list as component spec
6. Create high-fidelity mockups in design tool (Figma, etc.)
7. Link screens together showing complete user flows

### For Developers
1. Review screen data model for database schema
2. Identify API endpoints needed
3. Check dependencies for data flow between screens
4. Implement components based on UI components list
5. Add accessibility attributes (ARIA, semantic HTML)
6. Test keyboard navigation and screen readers
7. Verify color contrast and focus indicators

### For Product Managers
1. Review module overview for scope
2. Check workflows and user interactions
3. Note edge cases and error scenarios
4. Review success metrics for validation
5. Identify integration requirements
6. Plan phased rollout by module
7. Define acceptance criteria based on features listed

### For QA/Testing Teams
1. Extract test cases from workflows
2. Create accessibility checklist using requirements
3. Test all keyboard navigation patterns
4. Verify all error messages display correctly
5. Check color contrast with tools
6. Test with screen readers (NVDA, JAWS, etc.)
7. Validate touch target sizes on mobile

### For Accessibility Specialists
1. Review WCAG 2.2 AA requirements per screen
2. Audit design mockups against requirements
3. Test implemented features with assistive technologies
4. Verify keyboard navigation completeness
5. Check form labeling and error announcements
6. Validate focus management in modals
7. Test motion preferences handling

---

## 📊 By The Numbers

| Metric | Count |
|--------|-------|
| **Total Screens** | 48 |
| **Modules** | 7 |
| **Data Models** | 48 |
| **UI Components** | 400+ |
| **Accessibility Checkpoints** | 48+ per screen |
| **AI Integration Points** | 25+ |
| **Lines of Documentation** | 10,000+ |

---

## 🔄 Design Evolution

This library is a living document. Screens can evolve based on:
- User research and feedback
- Accessibility testing results
- AI model improvements
- Integration requirements
- Market and competitive changes

### Versioning
Document versions should track in commit history. Major updates:
- Breaking changes to workflows
- New accessibility features
- Significant AI model updates
- Integration changes

---

## 🛠️ Getting Started

### Prerequisites
- Familiarity with modern web applications
- Understanding of WCAG 2.2 AA standards
- Design tools (Figma recommended) or development frameworks
- For AI features: understanding of ML concepts

### Next Steps
1. **Review Module Overview**: Start with the module most relevant to your team
2. **Study a Complete Screen**: Pick one screen and review all sections
3. **Extract Requirements**: Identify what your team needs to implement
4. **Create Implementation Plan**: Break down the work into sprints
5. **Use as Source of Truth**: Reference this library throughout development
6. **Validate Against Checklist**: Ensure all accessibility requirements are met

---

## 📖 Files in This Repository

```
cc-hcm-prompts/
├── README.md (this file)
├── HCM_SCREEN_INVENTORY.md (overview of all 48 screens)
├── RECRUITING_SCREEN_PROMPTS.md (8 screens)
├── ONBOARDING_SCREEN_PROMPTS.md (8 screens)
├── PERFORMANCE_SCREEN_PROMPTS.md (screens 3.1-3.4)
├── PERFORMANCE_SCREEN_PROMPTS_PART2_COMPLETE.md (screens 3.5-3.8)
├── SELF_SERVICE_SCREEN_PROMPTS.md (screens 4.1-4.3)
├── SELF_SERVICE_SCREEN_PROMPTS_PART2.md (screens 4.4-4.8)
├── LEARNING_DEVELOPMENT_SCREEN_PROMPTS.md (5 screens)
├── COMPENSATION_MANAGEMENT_SCREEN_PROMPTS.md (5 screens)
├── AI_FIRST_FEATURES_SCREEN_PROMPTS_PART1.md (screens 7.1-7.4)
└── AI_FIRST_FEATURES_SCREEN_PROMPTS_PART2.md (screens 7.5-7.8)
```

---

## 🤝 Contributing

This library is designed to evolve. When making changes:
1. Update the relevant screen prompt file
2. Maintain the established format and structure
3. Ensure all accessibility requirements are included
4. Test any new workflows or data models
5. Document the change with clear commit message
6. Link related screens if dependencies changed

---

## 📝 License

This design library is proprietary. All screens, wireframes, data models, and documentation are the intellectual property of the organization.

---

## ❓ Questions?

Refer to:
- **Screen Details**: Individual prompt files for specific screen questions
- **Data Models**: Check the data model section of relevant screen
- **Accessibility**: Search WCAG 2.2 AA requirements in any screen
- **Workflows**: Key Features & Workflows section describes user interactions
- **AI Integration**: Check AI-First Features module for advanced capabilities

---

## 🎯 Summary

This library provides everything needed to design, develop, test, and launch a world-class, accessible, AI-augmented HRIS platform. Every screen has been thoughtfully designed with accessibility as a first-class requirement and AI integration as a core philosophy.

**Ready to build something great!**
