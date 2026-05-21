# AI-First Features Screen Prompts (Part 2: Screens 7.5-7.8)

> **Accessibility Note**: All screens below meet WCAG 2.2 AA standards with specific requirements for color contrast (4.5:1 for text), keyboard navigation, screen reader compatibility, focus management with visible indicators (3:1 minimum), 44×44 pixel touch targets, role="alert" for error handling, and prefers-reduced-motion support.

---

## Screen 7.5: AI Learning Recommendations

### Overview
AI Learning Recommendations provides personalized learning suggestions based on individual skill gaps, career goals, role requirements, and peer performance data. Employees receive a curated feed of relevant courses and learning paths.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ AI Learning Recommendations                         [✕] │
├───────────────────────────────────────────────────────────┤
│                                                           │
│ SKILL GAP ANALYSIS                                        │
│                                                           │
│ Current Role: Senior Product Manager                     │
│ Career Goal: VP Product (in 2-3 years)                   │
│                                                           │
│ Skills You Have vs. Role Requirements:                   │
│                                                           │
│ ✓ Product Strategy      (Advanced) → Target: Expert     │
│ ✓ User Research         (Advanced) → Target: Advanced   │
│ ⚠ Executive Comm.       (Intermediate) → Target: Advanced
│ ⚠ P&L Management        (Beginner) → Target: Intermediate
│ ✗ Public Speaking       (Beginner) → Target: Intermediate
│ ✗ Board Presentation    (None) → Target: Intermediate   │
│                                                           │
│ Skills to Develop: 3 recommended courses                 │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ RECOMMENDED LEARNING (Personalized Feed)                  │
│                                                           │
│ [Filters: All ▼] [Sort: Best Match ▼]                  │
│                                                           │
│ PRIORITY 1: Fill Critical Gaps (5 recommendations)       │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ 1. "Executive Communication for Leaders"            │ │
│ │    Coursera | 4 weeks | 8 hrs/week | Business      │ │
│ │                                                      │ │
│ │ Why recommended:                                     │ │
│ │ • Executive communication is critical skill gap     │ │
│ │ • Required for VP role (peer avg: 4.2/5)           │ │
│ │ • 92% of high performers complete this             │ │
│ │                                                      │ │
│ │ Estimated Time to Proficiency: 4 weeks             │ │
│ │ Success Rate for Role: 89%                          │ │
│ │                                                      │ │
│ │ [Enroll] [Add to Plan] [View Details] [Save]       │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ 2. "Financial Management for Product Leaders"       │ │
│ │    Reforge | 5 weeks | 6 hrs/week | Business      │ │
│ │                                                      │ │
│ │ Why recommended:                                     │ │
│ │ • P&L management is key gap for VP progression      │ │
│ │ • 78% of VPs rate this highly (4.7/5)             │ │
│ │ • Accelerates timeline to VP readiness by 6 months  │ │
│ │                                                      │ │
│ │ Estimated Time: 5 weeks                             │ │
│ │ Success Rate: 91%                                   │ │
│ │                                                      │ │
│ │ [Enroll] [Add to Plan] [View Details] [Save]       │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ PRIORITY 2: Accelerate Growth (3 recommendations)        │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ 3. "Advanced Product Strategy"                      │ │
│ │    Maven | 6 weeks | 5 hrs/week | Product          │ │
│ │                                                      │ │
│ │ Why recommended:                                     │ │
│ │ • Deepens your existing strength (Product Strategy) │ │
│ │ • 85% correlation with VP promotion success        │ │
│ │ • Recommended by 80% of peer high performers        │ │
│ │                                                      │ │
│ │ [Enroll] [Add to Plan] [View Details] [Save]       │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ PRIORITY 3: Explore New Skills (2 recommendations)       │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ 4. "Introduction to Data Science for Product"       │ │
│ │    Udacity | 8 weeks | 7 hrs/week | Technical      │ │
│ │                                                      │ │
│ │ Why recommended:                                     │ │
│ │ • Complements your analytical thinking              │ │
│ │ • Interesting based on browsing history             │ │
│ │ • Optional but valuable skill                        │ │
│ │                                                      │ │
│ │ [Enroll] [Add to Plan] [View Details] [Save]       │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ RECOMMENDED LEARNING PATH TO VP ROLE                      │
│                                                           │
│ Timeline: 14-16 weeks to full readiness                  │
│                                                           │
│ PHASE 1 (Weeks 1-5): Foundation                          │
│ [✗] Executive Communication ... [Start]  Weeks 1-4       │
│ [✗] Intro to Board Reporting     [Plan]  Weeks 2-5       │
│                                                           │
│ PHASE 2 (Weeks 6-10): Core Skills                        │
│ [✗] Financial Management ... [Plan] Weeks 6-10           │
│ [✗] Advanced Product Strategy ... [Plan] Weeks 7-12      │
│                                                           │
│ PHASE 3 (Weeks 11-16): Polish & Network                  │
│ [✗] Executive Presence & Leadership Weeks 12-16          │
│ [✗] Mentor with current VP (ongoing)                     │
│                                                           │
│ [Create Formal Learning Plan] [Share with Manager]       │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ PEER BENCHMARKING                                         │
│                                                           │
│ Your skills vs. peers with your role:                     │
│ Product Strategy:  ████████░░ 82% (Avg: 78%)            │
│ User Research:     █████████░ 85% (Avg: 80%)            │
│ Executive Comm:    █████░░░░░ 50% (Avg: 65%) ⚠         │
│ P&L Management:    ██░░░░░░░░ 20% (Avg: 50%) ⚠⚠        │
│                                                           │
│ ✓ You're above peers in Product Strategy & User Research │
│ ⚠ Focus on Executive Comm & P&L to match high performers │
│                                                           │
│ [View More Peer Data] [Compare with High Performers]     │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ DISMISSALS & PREFERENCES                                  │
│                                                           │
│ Dismissed recommendations (shown if interested):          │ │ • "Introduction to Agile" (dismissed: May 2025)        │
│ • "Design Thinking Workshop" (dismissed: April 2025)     │
│                                                           │
│ [Show Dismissed] [Update Preferences]                    │
│                                                           │
│ Notification Preferences:                                │
│ ◐ Email me weekly recommendations                        │
│ ◐ Notify me when new courses match my goals              │
│ [Update Settings]                                        │
│                                                           │
│ [Saved Items] [Completed Courses] [Help]                │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Skill Gap Analysis**
   - Current skills vs. role requirements
   - Target proficiency levels
   - Priority gaps for career goal
   - Visual skill comparison

2. **Personalized Recommendations**
   - Prioritized by impact and relevance
   - Why recommended explanation
   - Estimated time and success rate
   - Correlation with role/goal

3. **Learning Path Creation**
   - Sequential course recommendations
   - Phase-based approach
   - Timeline to readiness
   - Milestone tracking

4. **Peer Benchmarking**
   - Compare skills to same role peers
   - Identify skill gaps vs. peer average
   - Highlight high performer differentiators

5. **Preference Management**
   - Dismiss irrelevant recommendations
   - Save for later
   - Update learning preferences
   - Email frequency options

### Data Model

```javascript
{
  LearningRecommendation: {
    recommendation_id: String (UUID),
    employee_id: String (UUID),
    recommendation_date: Date,
    
    skill_gap_analysis: {
      current_role: String,
      target_role: String (optional),
      target_timeline_months: Number (optional),
      
      skills_analysis: [{
        skill_name: String,
        current_proficiency: Enum ("none", "beginner", "intermediate", "advanced", "expert"),
        target_proficiency: Enum ("beginner", "intermediate", "advanced", "expert"),
        gap_priority: Enum ("critical", "high", "medium", "low"),
        estimated_weeks_to_proficiency: Number
      }]
    },
    
    recommended_courses: [{
      course_id: String (UUID),
      course_name: String,
      provider: String,
      skill_focus: String,
      duration_weeks: Number,
      hours_per_week: Number,
      difficulty_level: Enum ("beginner", "intermediate", "advanced"),
      priority_tier: Enum ("critical", "high", "medium", "low"),
      
      recommendation_reason: [String],
      skill_gap_addresses: [String],
      success_rate_percentage: Decimal,
      completion_rate_percentage: Decimal,
      correlation_with_promotion: Decimal,
      peer_enrollment_percentage: Decimal,
      
      estimated_time_to_proficiency_weeks: Number,
      estimated_benefit_score: Number (0-100)
    }],
    
    learning_path: {
      goal: String,
      total_duration_weeks: Number,
      phases: [{
        phase_number: Number,
        phase_name: String,
        duration_weeks: Number,
        courses: [String],  // course IDs
        milestone: String
      }],
      timeline_to_readiness_weeks: Number
    },
    
    peer_benchmarking: {
      role: String,
      peer_count: Number,
      peer_median_scores: {
        [skill_name]: Decimal (0-1)
      },
      your_skill_scores: {
        [skill_name]: Decimal (0-1)
      },
      high_performer_skills: {
        [skill_name]: Decimal (0-1)
      }
    },
    
    user_actions: {
      recommended_courses_enrolled: Number,
      courses_completed: Number,
      dismissals: [{
        course_id: String,
        dismissal_date: Date,
        reason: String (optional)
      }],
      saved_courses: [String],
      last_interaction_date: Date
    }
  }
}
```

### UI Components Required

1. **Skill Gap Cards**
   - Skill name with current/target proficiency
   - Progress bar (current → target)
   - Gap priority badge
   - Time to proficiency estimate

2. **Course Recommendation Cards**
   - Course title and provider
   - Duration and time commitment
   - Why recommended explanation
   - Metrics (success rate, peer %,
   - Enroll/Save/Details buttons

3. **Learning Path Timeline**
   - Phase-based visual timeline
   - Course/milestone labels
   - Status indicators (completed/in progress/planned)
   - Estimated weeks for each phase

4. **Peer Comparison Chart**
   - Horizontal bar chart
   - Your score vs. peer average vs. high performer
   - Color-coded (below average/aligned/above average)
   - Legend with explanations

5. **Preferences Panel**
   - Notification frequency selector
   - Dismissed courses list
   - Update settings button

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text: 4.5:1 (#333333 body, #000000 headers)
- Skill gap bars: Green (proficient, #2E7D32), Red (gap, #C62828) with 4.5:1
- Peer benchmarks: Green (above avg, #2E7D32), Yellow (at avg, #F57C00), Red (below avg, #C62828)
- Priority badges: Red (critical), Orange (high), Yellow (medium), Green (low)
- Focus: 3px blue (#0066CC), 3:1 minimum

**Keyboard Navigation**
- Tab: Skill analysis → Course recommendations → Learning path → Peer comparison → Preferences
- Arrow keys: Navigate course list, expand recommendations
- Enter: Enroll in course, expand sections
- Escape: Close modals, dismiss overlays

**Screen Reader Support**
- Page: `<h1>AI Learning Recommendations</h1>`
- Skill gap: `<section aria-labelledby="gap-heading">`
  - Announcement: "Skill gap analysis. Current role: Senior Product Manager. Career goal: VP Product in 2-3 years. 3 critical skill gaps identified: Executive communication, P&L management, public speaking"
- Skill cards: `<div role="region" aria-label="[Skill Name]: Current [level], target [level], [weeks] weeks to proficiency">`
- Course card: `<article aria-labelledby="course-[id]-title">`
  - Summary: "[Course Name] by [Provider]. 4 weeks, 8 hours per week. Recommended because: fills executive communication gap, required for VP role, 92% of high performers complete this. Success rate: 89%."
- Learning path: `<section aria-labelledby="path-heading">`
  - Phases announced as sequential milestones
- Peer benchmark: `<div role="img" aria-label="Your skills vs peers: Product Strategy you 82%, peers 78% (above average). Executive Communication you 50%, peers 65% (below average - focus area)">`

**Focus Management**
- Visible focus (3px blue, 3:1 contrast) on all interactive
- Initial focus: Skill gap analysis section
- Skip link: "Skip to course recommendations"
- Tab through recommendations sequentially

**Touch Targets**
- Course action buttons: 44×44 minimum
- Enroll/Save/Details: 48×56 minimum
- Expand/collapse sections: 44×44 minimum
- Peer comparison labels: 44×44 minimum

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce`
- Skill bars fill instantly
- Course list loads instant, no slide animations

---

## Screen 7.6: AI Career Pathing

### Overview
AI Career Pathing provides employees and managers with AI-generated career development recommendations, including potential next roles, required skills, timeline to readiness, and success probability based on historical progression patterns.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ AI Career Pathing                                   [✕] │
├───────────────────────────────────────────────────────────┤
│ Employee: Sarah Chen | Current Role: Senior PM           │
│ Analysis Date: April 2025 | Last Updated: Weekly         │
│                                                           │
│ [View Profile] [Share with Manager] [Print Report]       │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ CAREER SUMMARY & TRAJECTORY                               │
│                                                           │
│ Current Position:  Senior Product Manager                │
│ Years in Role:     2 years                               │
│ Total Experience:  7 years (Product Management)          │
│ Promotion Likelihood (Next 12 months): 85%              │
│                                                           │
│ Career Arc:        [PM → Senior PM → Director PM →     │
│                     VP Product → C-Suite (CFO/COO)]     │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ CAREER ROADMAP (Recommended Progression)             │ │
│ │                                                      │ │
│ │ NOW: Senior Product Manager                         │ │
│ │      ✓ Performing exceptionally (4.8/5)              │ │
│ │      ✓ Ready for next level                          │ │
│ │      └─ Timeline: 0-6 months to next role           │ │
│ │                                                      │ │
│ │ ↓                                                     │ │
│ │                                                      │ │
│ │ NEXT: Director of Product (Internal Opportunity)    │ │
│ │       Skills Gap: 15%                                │ │
│ │       • Org/P&L management (need development)        │ │
│ │       • Strategic planning (already strong)          │ │
│ │       • Leadership at scale (growth area)            │ │
│ │       Timeline: 6-12 months                          │
│ │       Success Probability: 92%                       │ │
│ │       Available Roles: 1 in Product, 0 in Eng        │ │
│ │       [View Open Positions]                          │
│ │                                                      │ │
│ │ ↓                                                     │ │
│ │                                                      │ │
│ │ VP PRODUCT (Long-term goal)                          │ │
│ │       Skills Gap: 40%                                │
│ │       Timeline: 2-3 years (via Director role)        │ │
│ │       Development Path: 3 courses + mentoring        │
│ │       Success Probability: 88%                       │
│ │                                                      │ │
│ │ ↓                                                     │ │
│ │                                                      │ │
│ │ C-SUITE (CEO/COO option - alternative path)          │
│ │       Timeline: 5+ years                             │ │
│ │       Path: VP Product → Chief Strategy Officer      │
│ │                                                      │ │
│ │ [Explore Alternative Paths]                          │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ DIRECTOR OF PRODUCT - DETAILED ASSESSMENT                │
│                                                           │
│ Target Role: Director of Product                         │
│ Readiness Score: 85% (Ready with targeted development)  │
│ Timeline to Ready: 9-12 months                           │
│ Success Probability: 92%                                 │
│                                                           │
│ SKILLS REQUIRED vs. YOUR LEVEL                           │
│                                                           │
│ Essential Skills:                                         │
│ ✓ Product Strategy       [████████░░] 82% (Advanced)     │
│ ✓ Leadership             [███████░░░] 70% (Advanced)     │
│ ⚠ P&L/Financial Mgmt     [████░░░░░░] 40% (Need develop)│
│ ⚠ Org Management         [█████░░░░░] 50% (Intermediate) │
│ ✓ Stakeholder Mgmt       [██████████] 90% (Expert)       │
│                                                           │
│ Development Priorities:                                   │
│ 1. P&L & Financial Management (12-week intensive)        │
│ 2. Leading Larger Teams (mentoring + course)             │
│ 3. Strategic Planning (extend existing strength)         │
│                                                           │
│ RECOMMENDED DEVELOPMENT PLAN                              │
│                                                           │
│ Month 1-2: Financial Fundamentals                        │
│ [Course: Financial Management for Product Leaders] Q2    │
│ Manager: Schedule monthly 1:1s on financial decisions    │
│                                                           │
│ Month 3-6: Team Leadership at Scale                      │
│ [Mentoring: VP Product strategy mentoring]               │
│ [Course: Managing High-Performing Teams]                 │
│ [Stretch Assignment: Lead cross-org initiative]          │
│                                                           │
│ Month 7-9: Strategic Planning & Execution                │
│ [Mentoring: Strategic planning discussions]              │
│ [Stretch: Present to board on strategy]                  │
│                                                           │
│ Month 10-12: Director Readiness Evaluation               │
│ [Manager evaluation + AI assessment = director-ready]    │
│ [Consider internal promotions or external search]        │
│                                                           │
│ [Create Formal Development Plan] [Assign Mentor]         │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ PEER PROGRESSION BENCHMARKS (Anonymized)                 │
│                                                           │
│ Peers in your role (Senior PM):                          │
│ Average time to Director: 18-24 months                   │
│ Your timeline: 9-12 months (FASTER than average)        │
│                                                           │
│ Success rate of progression: 87% of SeniorPMs promote   │
│ Your success probability: 92% (ABOVE AVERAGE)           │
│                                                           │
│ High Performers:                                          │
│ • Often have prior P&L exp (you don't - growth area)    │
│ • Average 3 leadership courses (recommend 2-3 for you)   │
│ • Avg mentoring: 1 year from VP (recommend 1.5 yr)      │
│                                                           │
│ Attrition Risk: Very Low (1% leave in next 2 years)    │
│                                                           │
│ [View More Benchmarks]                                   │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ ALTERNATIVE CAREER PATHS                                 │
│                                                           │
│ Path 1: Product Executive (Recommended)                  │
│ Senior PM → Director PM → VP Product → C-Suite           │
│ Timeline: 5-7 years | Success Rate: 92%                 │
│                                                           │
│ Path 2: Strategy/Operations (Alternative)                │
│ Senior PM → Head of Strategy → Chief Strategy Officer    │
│ Timeline: 4-5 years | Success Rate: 78%                 │
│                                                           │
│ Path 3: Entrepreneurship (You could leave & start company)│
│ Years to readiness: 2-3 years | Market timing likely    │
│                                                           │
│ [Explore Paths] [Update Career Goal]                    │
│                                                           │
│ [Generate Career Report] [Share with Manager] [Download]│
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Career Trajectory Overview**
   - Current role and progression history
   - Recommended career path with roles and timeline
   - Promotion likelihood metrics
   - Alternative paths visualization

2. **Target Role Assessment**
   - Readiness score (0-100%)
   - Skills gap analysis
   - Timeline to readiness
   - Success probability

3. **Development Plan**
   - Prioritized skill development areas
   - Recommended courses and mentoring
   - Stretch assignments
   - Milestone timeline

4. **Peer Benchmarking**
   - Progression timeline comparison
   - Success rate vs. peer average
   - High performer differentiators
   - Attrition risk assessment

5. **Alternative Paths**
   - Multiple career trajectory options
   - Success rates and timelines
   - Skill requirements for each path

### Data Model

```javascript
{
  CareerPath: {
    career_path_id: String (UUID),
    employee_id: String (UUID),
    analysis_date: Date,
    
    current_position: {
      role: String,
      level: Enum ("entry", "mid", "senior", "lead", "director", "vp", "c_suite"),
      years_in_role: Number,
      performance_rating: Number (0-5),
      promotion_readiness: Decimal (0-1)
    },
    
    total_career_context: {
      total_years_experience: Number,
      career_history: [{
        role: String,
        company: String,
        duration_years: Number,
        achievements: [String]
      }],
      industry_focus: [String]
    },
    
    recommended_path: {
      primary_path_id: String,
      next_role: String,
      timeline_to_next_role_months: Number,
      subsequent_roles: [{
        role_sequence: Number,
        role_name: String,
        timeline_from_now_months: Number,
        timeline_from_previous_months: Number,
        success_probability: Decimal (0-1)
      }],
      long_term_ceiling: String,  // e.g., "C-Suite (CEO/COO)"
      total_years_to_ceiling: Number
    },
    
    target_role_assessment: {
      target_role: String,
      readiness_score: Decimal (0-1),  // 0-100%
      timeline_to_readiness_months: Number,
      success_probability: Decimal (0-1),
      skills_gap_percentage: Decimal (0-1),
      
      skills_required: [{
        skill: String,
        your_current_level: Enum ("none", "beginner", "intermediate", "advanced", "expert"),
        required_level: Enum ("beginner", "intermediate", "advanced", "expert"),
        gap_priority: Enum ("critical", "high", "medium", "low")
      }],
      
      development_plan: {
        focus_areas: [String],
        estimated_total_effort_hours: Number,
        recommended_courses: [String],
        recommended_mentors: [String],
        recommended_stretch_assignments: [String],
        timeline_phases: [{
          phase_number: Number,
          duration_months: Number,
          focus: String,
          activities: [String]
        }]
      }
    },
    
    alternative_paths: [{
      path_id: String (UUID),
      path_name: String,
      sequence_of_roles: [String],
      timeline_years: Number,
      success_probability: Decimal (0-1),
      skill_requirements: [String],
      differentiation_from_primary: String
    }],
    
    peer_benchmarking: {
      peer_role: String,
      peer_count: Number,
      average_time_to_promotion_months: Number,
      your_timeline_comparison: String,  // "12 months faster"
      promotion_success_rate: Decimal,
      high_performer_differentiators: [String],
      attrition_risk_next_2_years: Decimal
    }
  }
}
```

### UI Components Required

1. **Career Roadmap Visualization**
   - Vertical or horizontal timeline showing role progression
   - Current role highlighted
   - Next 2-3 roles with timelines
   - Alternative path indicators
   - Expandable for detailed view

2. **Role Assessment Cards**
   - Target role name and level
   - Readiness score prominently displayed
   - Skills gap visualization
   - Timeline and success probability
   - Development plan link

3. **Skills Comparison Chart**
   - Current level vs. required level for target role
   - Gap indicators (color-coded)
   - Skill list with current/required proficiency

4. **Development Plan Timeline**
   - Phase-based breakdown (months)
   - Activities per phase
   - Course/mentoring assignments
   - Milestone markers

5. **Benchmark Comparison**
   - Timeline comparison vs. peers (bar chart)
   - Success rate percentage
   - Differentiators text list

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text: 4.5:1 (#333333 body, #000000 headers)
- Timeline elements: Blue (#0066CC, 4.5:1)
- Skill gaps: Red (#C62828) for gaps, Green (#2E7D32) for met
- Readiness bar: Green (#2E7D32), Yellow (#F57C00), Red (#C62828) with 4.5:1
- Focus: 3px blue (#0066CC), 3:1 minimum

**Keyboard Navigation**
- Tab: Career summary → Timeline → Target role → Development plan → Alternative paths
- Arrow keys: Navigate timeline roles, expand alternative paths
- Enter: Expand role details, view development plan
- Escape: Close detailed views

**Screen Reader Support**
- Page: `<h1>AI Career Pathing</h1>`
- Career summary: `<section aria-labelledby="summary-heading">`
  - Announcement: "Sarah Chen, Senior Product Manager, 7 years total experience. Promotion likelihood next 12 months: 85%. Recommended career path: Senior PM to Director PM to VP Product to C-Suite."
- Timeline: `<nav aria-label="Career progression timeline">`
  - Roles announced sequentially with timelines
- Target role: `<article aria-labelledby="target-role-name">`
  - Summary: "Target role: Director of Product. Readiness: 85%. Timeline: 9-12 months. Success probability: 92%. Skills gap: 15%. Critical development areas: P&L Management, Team Leadership."
- Development phases: `<section aria-labelledby="dev-plan-heading">`
  - Phases announced with activities
- Peer benchmark: `<div role="region" aria-label="Progression benchmarks: Your timeline to Director 9-12 months, peer average 18-24 months. You're 12 months faster than average. Success rate: 92% for you vs. 87% peer average">`

**Focus Management**
- Visible focus (3px blue, 3:1 contrast) on all interactive
- Initial focus: Career summary section
- Skip link: "Skip to career roadmap"
- Tab through timeline and role cards sequentially

**Touch Targets**
- Timeline role click areas: 44×44 minimum
- Expand/collapse buttons: 44×44 minimum
- Alternative path selection: 48×48 minimum
- View details links: 44×44 minimum

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce`
- Timeline rendering instant
- Role expansion instant or slow fade (>2s)

---

## Screen 7.7: AI Compensation Optimization

### Overview
AI Compensation Optimization provides finance and HR leaders with AI-driven analysis and recommendations for compensation planning, including equity gap identification, salary band adjustments, and budget optimization.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ AI Compensation Optimization                        [✕] │
├───────────────────────────────────────────────────────────┤
│ Analysis Period: Q1 2025 | Department: All              │
│ Analysis Date: April 20, 2025                            │
│                                                           │
│ [By Department ▼] [Analysis Period ▼] [Export Report]   │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ COMPENSATION HEALTH SCORECARD                             │
│                                                           │
│ Market Competitiveness:   ████████░░ 78/100             │
│ Pay Equity:              ██████████ 88/100             │
│ Salary Band Distribution:  ███████░░░ 72/100             │
│ Budget Efficiency:        ████████░░ 80/100             │
│ Retention Risk:           ██████░░░░ 60/100 (Fair)      │
│                                                           │
│ Overall Score: 76/100 (Room for Optimization)            │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ KEY OPTIMIZATION OPPORTUNITIES                            │
│                                                           │
│ 1. SALARY BAND ADJUSTMENTS (High Priority)               │
│    ┌──────────────────────────────────────────────────┐ │
│    │ Role: Senior Product Manager                     │ │
│    │ Current Min/Mid/Max: $140k / $160k / $180k       │ │
│    │ Market Data (50/50th/75th): $145k / $165k / $185k│
│    │                                                  │ │
│    │ Recommendation: Adjust to $145k / $165k / $185k  │
│    │ Impact: Improve competitiveness (+5% at median)  │
│    │ Budget Cost: $45k annual (across 10 employees)   │
│    │ Expected Retention Benefit: -8% attrition risk   │
│    │ ROI: Retention value > cost                       │
│    │                                                  │ │
│    │ ✓ Recommendation: Implement immediately          │
│    │ Timeline: Q2 2025 effective                       │
│    │ [View Full Analysis] [Approve Change]             │
│    └──────────────────────────────────────────────────┘ │
│                                                           │
│ 2. EQUITY GAP REMEDIATION (Medium Priority)              │
│    ┌──────────────────────────────────────────────────┐ │
│    │ Issue: Gender pay gap detected in Engineering    │
│    │                                                  │ │
│    │ Analysis:                                        │ │
│    │ Female Engineers avg: $145k                       │
│    │ Male Engineers avg: $158k                        │
│    │ Gap: $13k (9%) - REQUIRES ATTENTION              │
│    │                                                  │
│    │ Root Cause Analysis:                              │
│    │ • Wage history anchoring (prior employer)        │
│    │ • Fewer female senior roles (role composition)   │
│    │ • Historical hiring practices                    │
│    │                                                  │
│    │ Remediation Plan:                                │
│    │ Phase 1: Equity adjustments for 5 employees      │
│    │   Cost: $60k annual                              │
│    │   Timeline: Q2 2025                              │
│    │                                                  │
│    │ Phase 2: Hiring practices audit & change         │
│    │   Timeline: Immediate                            │
│    │                                                  │
│    │ [View Detailed Gap Analysis] [Approve]            │
│    └──────────────────────────────────────────────────┘ │
│                                                           │
│ 3. BONUS STRUCTURE OPTIMIZATION (Low Priority)           │
│    ┌──────────────────────────────────────────────────┐ │
│    │ Current: Uniform 20% target across all roles     │
│    │ Recommendation: Role-based targets               │
│    │   • IC roles: 15-20% (skill/project-dependent)   │
│    │   • Manager roles: 25-35% (team performance)     │
│    │   • Executive: 40-60% (company-wide metrics)     │
│    │                                                  │
│    │ Expected Impact:                                  │
│    │ • Better alignment with responsibility           │ │ • Improved retention for high-performers         │
│    │ • Budget efficiency: 3% savings possible          │
│    │                                                  │
│    │ [View Details] [Consider Recommendation]          │
│    └──────────────────────────────────────────────────┘ │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ BUDGET ALLOCATION OPTIMIZATION                            │
│                                                           │
│ Current Budget: $5.2M | Allocation:                      │
│ • Base Salary: 78% ($4.05M)                              │
│ • Bonus: 14% ($0.73M)                                    │
│ • Equity: 6% ($0.31M)                                    │
│ • Benefits: 2% ($0.11M)                                  │
│                                                           │
│ Recommended Allocation:                                   │
│ • Base Salary: 75% ($3.9M)  (-3%)                       │
│ • Bonus: 15% ($0.78M)       (+1%)                       │
│ • Equity: 8% ($0.42M)       (+2%)  [Attract talent]      │
│ • Benefits: 2% ($0.1M)      (stable)                     │
│                                                           │
│ Impact: More competitive at totaling compensation        │
│ Same budget, improved market positioning                 │
│                                                           │
│ [View Scenario Analysis] [What-If Tool]                  │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ WHAT-IF ANALYSIS                                          │
│                                                           │
│ Scenario 1: 3% Salary Increase (Inflation Adjustment)   │
│ Budget Impact: +$156k annually                           │
│ Retention Improvement: +2%                               │
│ Market Position: Improved 5%                             │
│                                                           │
│ Scenario 2: Increase Equity for Tech Roles               │
│ Budget Impact: +$125k (reallocated)                      │
│ Attraction Impact: +15% more competitive for Sr. roles   │
│ Risk: May compress salary bands temporarily              │
│                                                           │
│ Scenario 3: New-Hire Premium Adjustment                  │
│ Budget Impact: +$85k annually                            │
│ Impact: Closes new-hire vs. tenured gap (+8%)           │
│ Risk: May create equity issues if not managed            │
│                                                           │
│ [Create Custom Scenario] [Model Budget Impact]           │
│                                                           │
│ [Generate Full Report] [Download Excel] [Share with Team]│
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Compensation Health Scorecard**
   - Overall score with component breakdown
   - Market competitiveness metric
   - Pay equity assessment
   - Salary band distribution analysis
   - Retention risk scoring

2. **Optimization Opportunities**
   - Prioritized list (high/medium/low)
   - Impact analysis (cost, retention benefit, timeline)
   - Root cause analysis for equity gaps
   - Recommended actions with approval buttons

3. **Budget Allocation Analysis**
   - Current vs. recommended allocation
   - Visual representation (stacked bar or pie chart)
   - Component percentages
   - Competitive positioning impact

4. **What-If Analysis**
   - Scenario modeling for budget changes
   - Impact on retention, attraction, market positioning
   - Custom scenario builder

5. **Reporting & Export**
   - Comprehensive report generation
   - Excel export for further analysis
   - Share with stakeholders

### Data Model

```javascript
{
  CompensationOptimization: {
    analysis_id: String (UUID),
    organization_id: String (UUID),
    analysis_date: Date,
    analysis_period: String,
    
    health_scorecard: {
      overall_score: Number (0-100),
      market_competitiveness_score: Number (0-100),
      pay_equity_score: Number (0-100),
      salary_band_distribution_score: Number (0-100),
      budget_efficiency_score: Number (0-100),
      retention_risk_score: Number (0-100),
      health_assessment: String  // "Room for Optimization"
    },
    
    optimization_opportunities: [{
      opportunity_id: String (UUID),
      title: String,
      priority: Enum ("high", "medium", "low"),
      category: Enum ("salary_bands", "equity_gap", "bonus_structure", "budget_allocation"),
      
      current_state: String,
      recommended_state: String,
      business_case: {
        implementation_cost: Decimal,
        expected_benefits: [String],
        retention_impact: String,  // e.g., "-8% attrition"
        attraction_impact: String,
        roi_assessment: String
      },
      
      timeline: String,  // "Q2 2025"
      implementation_steps: [String],
      risk_factors: [String]
    }],
    
    equity_analysis: {
      gender_wage_gap: Decimal,  // e.g., 0.09 for 9%
      race_wage_gap: Decimal,
      tenure_wage_gap: Decimal,
      issues_identified: [{
        issue: String,
        severity: Enum ("low", "medium", "high"),
        affected_employees_count: Number,
        estimated_cost_to_remediate: Decimal,
        recommended_timeline: String
      }],
      
      remediation_plan: [{
        phase: Number,
        description: String,
        cost: Decimal,
        timeline: String,
        expected_outcome: String
      }]
    },
    
    budget_allocation: {
      total_compensation_budget: Decimal,
      current_allocation: {
        base_salary_percentage: Decimal,
        bonus_percentage: Decimal,
        equity_percentage: Decimal,
        benefits_percentage: Decimal
      },
      current_allocation_amounts: {
        base_salary: Decimal,
        bonus: Decimal,
        equity: Decimal,
        benefits: Decimal
      },
      
      recommended_allocation: {
        base_salary_percentage: Decimal,
        bonus_percentage: Decimal,
        equity_percentage: Decimal,
        benefits_percentage: Decimal
      },
      
      allocation_rationale: String,
      competitive_positioning_impact: String
    },
    
    what_if_scenarios: [{
      scenario_id: String (UUID),
      scenario_name: String,
      description: String,
      
      budget_impact: Decimal,
      retention_impact: String,
      attraction_impact: String,
      market_position_impact: String,
      risks: [String],
      
      custom_parameters: {
        [param_name]: String
      }
    }]
  }
}
```

### UI Components Required

1. **Health Scorecard Cards**
   - Metric name with score (0-100)
   - Horizontal progress bar
   - Assessment label
   - Trend indicator (↑↓→)

2. **Opportunity Cards**
   - Priority badge
   - Title and category
   - Current vs. recommended state
   - Business case summary bullets
   - Action buttons (View Details, Approve)

3. **Budget Allocation Chart**
   - Stacked horizontal bar or pie chart
   - Component labels with percentages
   - Current vs. recommended side-by-side
   - Dollar amounts displayed

4. **Scenario Comparison**
   - Table showing scenarios
   - Budget impact column
   - Retention/attraction impact columns
   - Risk indicators

5. **Equity Gap Visualization**
   - Bar chart showing wage gaps
   - Affected group comparisons
   - Severity indicators
   - Remediation timeline

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text: 4.5:1 (#333333 body, #000000 headers)
- Score bars: Green (#2E7D32), Yellow (#F57C00), Red (#C62828) with 4.5:1
- Priority badges: Red (high), Orange (medium), Yellow (low)
- Equity gap: Red (#C62828) for problematic gaps
- Focus: 3px blue (#0066CC), 3:1 minimum

**Keyboard Navigation**
- Tab: Scorecard → Opportunities → Budget analysis → What-if scenarios
- Arrow keys: Navigate opportunity list, compare scenarios
- Enter: Expand opportunity details, create scenario
- Escape: Close detailed views

**Screen Reader Support**
- Page: `<h1>AI Compensation Optimization</h1>`
- Scorecard: `<section aria-labelledby="scorecard-heading">`
  - Announcement: "Compensation health scorecard. Overall score: 76 out of 100. Market competitiveness: 78. Pay equity: 88. Salary band distribution: 72. Budget efficiency: 80. Retention risk: 60."
- Opportunity: `<article aria-labelledby="opportunity-[id]-title">`
  - Summary: "Salary band adjustment for Senior PM. Priority: High. Current band: $140-180k. Recommended: $145-185k. Cost: $45k annually. Expected retention benefit: 8% reduction in attrition."
- Budget chart: `<div role="img" aria-label="Current compensation allocation: Base salary 78% ($4.05M), Bonus 14% ($0.73M), Equity 6% ($0.31M), Benefits 2% ($0.11M). Recommended: Base 75% ($3.9M), Bonus 15% ($0.78M), Equity 8% ($0.42M), Benefits 2% ($0.1M)">`
- Scenarios: `<table aria-label="What-if scenario analysis">`
  - Rows announce scenario name, budget impact, retention impact

**Focus Management**
- Visible focus (3px blue, 3:1 contrast) on all interactive
- Initial focus: Scorecard section
- Skip link: "Skip to optimization opportunities"
- Tab through cards sequentially

**Touch Targets**
- Opportunity action buttons: 44×44 minimum
- View Details/Approve: 48×56 minimum
- Scenario comparison buttons: 44×44 minimum
- Scorecard expand: 44×44 minimum

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce`
- Score bars fill instantly
- Scenario changes instant display

---

## Screen 7.8: AI Assistant (Conversational)

### Overview
The AI Assistant provides a natural language chat interface for HR-related questions, process guidance, and task assistance across the HCM system. The assistant understands company context, policies, and can escalate complex issues.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ 🤖 HR Assistant                                    [✕] │
├───────────────────────────────────────────────────────────┤
│ Chat with HR | Powered by AI                             │
│ [Clear History] [Settings]                               │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ CHAT HISTORY (Session)                                    │
│                                                           │
│ [Yesterday 3:24 PM]                                       │
│ You: How much PTO do I have left?                        │
│ HR Assistant: You have 8 days of paid time off remaining │
│              this year. Would you like to request time   │
│              off? [Request Time Off] [View Calendar]     │
│                                                           │
│ [Today 9:15 AM]                                           │
│ You: How do I enroll in 401k?                            │
│ HR Assistant: Good question! Let me help you with 401(k) │
│              enrollment. Here are the steps:              │
│              1. Go to Benefits section                   │
│              2. Select 401(k) plan from options         │
│              3. Choose contribution amount               │
│              4. Review and confirm                       │
│                                                           │
│              Your company offers:                         │
│              • Employer match: 6% (dollar-for-dollar)    │
│              • Contribution limit: $23,500/yr (2024)    │
│                                                           │
│              [Open Benefits Portal] [Quick Help Video]   │
│              [Talk to HR Specialist]                     │
│                                                           │
│ You: What's my compensation package worth?              │
│ HR Assistant: I pulled your compensation statement.      │
│              Your total comp = $250,000/year             │
│              • Base: $150,000                            │
│              • Bonus: $30,000 (target 20%)               │
│              • Equity: $50,000                           │
│              • Benefits: $20,000                         │
│                                                           │
│              Would you like details on:                  │
│              • How your salary compares to market?       │
│              • Vesting schedule for equity?              │
│              • Tax planning for equity?                  │
│              [View Full Statement] [Talk to Finance]    │
│                                                           │
│ [Today 10:45 AM - Current]                               │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ INPUT AREA                                                │
│                                                           │
│ Message Input:                                            │
│ ┌───────────────────────────────────────────────────┐    │
│ │ What performance goals should I discuss with my   │    │
│ │ manager this quarter?                             │    │
│ │                                                   │    │
│ │ [Suggestions:]                                    │    │
│ │ • How to set SMART goals                         │    │
│ │ • View goal-setting templates                    │    │
│ │ • Schedule 1:1 with manager                      │    │
│ │                                                   │    │
│ │                          [Send] [Microphone] [+] │    │
│ └───────────────────────────────────────────────────┘    │
│                                                           │
│ SUGGESTED QUESTIONS                                       │
│ [How much PTO do I have?]  [What's my salary?]          │
│ [How do I request time off?]  [How to get reimbursed?]  │
│                                                           │
│ [View Help Topics]  [Contact HR Team]  [Provide Feedback]│
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Natural Language Chat**
   - Multi-turn conversation
   - Context awareness (employee personal data, policies)
   - Questions about policies, processes, dates
   - Task assistance

2. **Intent Recognition**
   - Categorize user requests (info lookup, process help, task automation)
   - Route to knowledge base or escalation

3. **Task Assistance**
   - Guide through processes (benefits enrollment, time off request)
   - Direct links to relevant screens/documents
   - Form prefilling where possible

4. **Knowledge Base Integration**
   - Link to policy documents
   - Quick help videos
   - FAQ references
   - Document search

5. **Escalation Handling**
   - Identify when human assistance needed
   - Queue for HR team contact
   - Seamless handoff with context

6. **Conversation History**
   - Persistent chat history
   - Session management
   - Clear/archive history
   - Reference previous conversations

### Data Model

```javascript
{
  ConversationMessage: {
    message_id: String (UUID),
    conversation_id: String (UUID),
    employee_id: String (UUID),
    timestamp: Date,
    
    user_message: {
      text: String,
      original_text: String,
      intent: Enum ("info_lookup", "process_help", "task_execution", "general_question", "complaint"),
      entities_extracted: [{
        entity_type: Enum ("date", "employee_name", "policy_name", "benefit_type", "role", "location"),
        value: String
      }],
      confidence_score: Decimal (0-1)
    },
    
    assistant_response: {
      text: String,
      response_type: Enum ("information", "guidance", "action", "escalation", "clarification"),
      suggested_actions: [{
        action_label: String,
        action_type: Enum ("link_to_screen", "document_reference", "task_initiation", "contact_hr"),
        action_target: String  // URL, screen ID, etc.
      }],
      referenced_documents: [String],
      referenced_policies: [String],
      confidence_score: Decimal (0-1)
    },
    
    escalation_required: Boolean,
    escalation_reason: String (optional),
    escalation_queue_id: String (UUID) (optional),
    human_agent_assigned: Boolean,
    human_agent_id: String (UUID) (optional),
    
    user_satisfaction: {
      rating: Enum ("very_satisfied", "satisfied", "neutral", "dissatisfied", "very_dissatisfied") (optional),
      feedback: String (optional),
      rating_date: Date (optional)
    }
  },
  
  Conversation: {
    conversation_id: String (UUID),
    employee_id: String (UUID),
    start_date: Date,
    last_message_date: Date,
    status: Enum ("active", "closed", "escalated"),
    
    conversation_context: {
      employee_role: String,
      employee_department: String,
      relevant_policies: [String],
      relevant_benefits: [String],
      recent_actions: [String]  // Recent HR actions for context
    },
    
    message_count: Number,
    topics_discussed: [String],
    questions_asked: Number,
    tasks_initiated: Number,
    escalations: Number
  }
}
```

### UI Components Required

1. **Chat Message Bubbles**
   - User message right-aligned
   - Assistant message left-aligned
   - Timestamp and indicator (sending/sent)
   - Avatar indicators (user/AI)
   - Links/buttons within message

2. **Input Field**
   - Text input with autocomplete suggestions
   - Send button
   - Voice input button (optional)
   - Attachment button (optional)
   - Suggested questions/topics below

3. **Action Buttons**
   - In-message buttons (links, quick actions)
   - Color-coded by action type
   - Clear labels

4. **Suggested Questions**
   - Pre-written common questions
   - Contextual based on user role
   - Quick-select buttons

5. **Conversation Management**
   - Clear history button
   - Session indicator
   - Contact HR link
   - Help and feedback links

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text: 4.5:1 (#333333 on white, #FFFFFF on dark)
- User message bubble: Light blue (#E3F2FD) background, #000000 text
- Assistant message: White (#FFFFFF) background, #333333 text
- Buttons within messages: Blue (#0066CC), 4.5:1 contrast
- Timestamps: Gray (#757575), 4.5:1
- Focus: 3px blue (#0066CC), 3:1 minimum

**Keyboard Navigation**
- Tab: Input field → Send button → Suggested questions → Chat history → Help/Contact links
- Arrow keys: Navigate suggested questions, scroll chat history
- Enter: Send message, activate suggested question
- Escape: Clear suggestions, close modals
- Ctrl+A: Select all text in input

**Screen Reader Support**
- Page: `<h1>HR Assistant</h1>`
- Chat region: `<section role="log" aria-labelledby="chat-heading" aria-live="polite">`
  - Chat heading: "Chat history with HR Assistant"
- User message: `<div role="article" aria-label="Your message at [time]">`
  - Content announced: "[Message text]"
- Assistant message: `<div role="article" aria-label="Assistant response at [time]">`
  - Content announced with all actions/links
  - Links announced as "Open [screen/document]"
- Input field: `<textarea aria-label="Chat message input" aria-describedby="help-text">`
  - Help text: "Type your question about HR policies, benefits, or processes"
- Suggested questions: `<section aria-label="Suggested questions">`
  - Announced as buttons: "Suggested: [question text]"
- Status: `<div role="status" aria-live="polite">Message sent successfully. Waiting for response.</div>`

**Focus Management**
- Visible focus (3px blue, 3:1 contrast) on all interactive
- Initial focus: Input text area
- Skip link: "Skip to input area"
- Chat history scrolls to most recent message automatically
- Focus returns to input after message send

**Touch Targets**
- Send button: 44×44 minimum
- Suggested question buttons: 44×44 minimum
- In-message action buttons: 48×56 minimum
- Input field: 44px height minimum

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce`
- Message arrival: No animation, instant appearance
- Typing indicator (if shown): Respectfully minimal or instant

**Error & Status Messages**
- Input validation: `role="alert"`
  - "Please enter a question or select a suggested topic"
- Escalation: `role="status"` aria-live="assertive"
  - "Your question has been escalated to our HR team. A specialist will contact you within 2 hours."
- Connection issues: `role="alert"`
  - "Connection lost. Reconnecting..."

---

## Summary of AI-First Features Module

All 8 screens in the AI-First Features module prioritize:

1. **Transparency & Explainability**: All AI recommendations include clear reasoning for why specific suggestions are made
2. **Human-in-the-Loop**: AI augments but doesn't replace human decision-making
3. **Actionability**: Each screen provides clear next steps and recommended actions
4. **Accessibility**: WCAG 2.2 AA compliance with attention to:
   - Clear explanation of complex recommendations (career paths, risk scores)
   - Keyboard navigation through multi-level content (timelines, scenarios)
   - Screen reader support for AI-generated insights
   - Visual + text representation of data (charts with descriptions)
   - 44×44 pixel touch targets for all interactive elements
5. **Integration**: All screens connect to each other and existing HCM modules

These 8 screens complete the 48-screen AI-first HCM product design library.

