# AI-First Features Screen Prompts (Part 1: Screens 7.1-7.4)

> **Accessibility Note**: All screens below meet WCAG 2.2 AA standards with specific requirements for color contrast (4.5:1 for text), keyboard navigation, screen reader compatibility, focus management with visible indicators (3:1 minimum), 44×44 pixel touch targets, role="alert" for error handling, and prefers-reduced-motion support.

---

## Screen 7.1: AI Resume Screening Assistant

### Overview
The AI Resume Screening Assistant automates initial resume review by extracting key information, scoring candidates against job requirements, and providing explainable AI recommendations. This screen emphasizes transparency and human-in-the-loop decision-making.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ AI Resume Screening Assistant                        [✕] │
├───────────────────────────────────────────────────────────┤
│ Job Posting: Product Manager, San Francisco              │
│ Upload Resume: [Drag & Drop Area / Select File]         │
│                                                           │
│ [Clear] [Process Resume]                                 │
├───────────────────────────────────────────────────────────┤
│                                                           │
│ EXTRACTED CANDIDATE INFORMATION                           │
│                                                           │
│ Name: Sarah Chen              Phone: (555) 123-4567      │
│ Email: sarah.chen@email.com   Location: San Francisco    │
│                                                           │
│ EXPERIENCE SUMMARY                                        │
│ Current/Last Role: Senior Product Manager (2 years)       │
│ Total Experience: 7 years in Product Management          │
│ Industry Focus: SaaS, B2B                                 │
│                                                           │
│ EDUCATION                                                 │
│ • B.S. Computer Science, UC Berkeley (2016)             │
│ • Product Management Certification, Reforge (2022)       │
│                                                           │
│ KEY SKILLS EXTRACTED                                      │
│ Product Strategy [Mentioned 3x] [Verified]               │
│ User Research [Mentioned 2x] [Verified]                  │
│ Data Analysis [Mentioned 4x] [Verified]                  │
│ Agile/Scrum [Mentioned 1x] [High Confidence]            │
│ SQL [Mentioned 1x] [Low Confidence]                      │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ AI QUALIFICATION SCORING                                  │
│                                                           │
│ Overall Match Score: 82/100                              │
│ ✓ Exceeds requirements (Top 15% of applicants)          │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ REQUIREMENT ASSESSMENT                               │ │
│ │                                                      │ │
│ │ Required Skills Match:        ████████░░ 82%        │ │
│ │ Experience Level Match:       ██████████ 90%        │ │
│ │ Education Alignment:          ███████░░░ 70%        │ │
│ │ Industry Fit:                 ██████████ 95%        │ │
│ │ Cultural Fit Indicators:      ████████░░ 80%        │ │
│ │                                                      │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ RED FLAGS & GAPS                                          │
│ ⚠ Unclear employment gap (6 months in 2020)             │
│ ⚠ Limited SQL/technical skills (requirement: 2+ years)  │
│ ✓ No major concerns identified                           │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ AI REASONING & EXPLANATION                                │
│                                                           │
│ [Show Detailed Reasoning]                                │
│                                                           │
│ Score Breakdown:                                          │
│ • Product Strategy expertise: +25pts                      │
│   - 3 years as PM, led 5+ successful launches            │
│   - Led cross-functional teams of 5-8 people             │
│                                                           │
│ • User Research capability: +15pts                        │
│   - Experience with user interviews, A/B testing         │
│   - Reforge certification suggests structured training    │
│                                                           │
│ • Technical Skills Gap: -8pts                             │
│   - SQL/analytics skills mentioned minimally             │
│   - Compensated by strong data analysis experience       │
│                                                           │
│ • Culture Fit Signals: +10pts                             │
│   - Startup background suggests adaptability             │
│   - Cross-functional leadership experience               │
│                                                           │
│ • Employment Gap: -3pts                                   │
│   - 6-month gap in 2020 (likely COVID-related)           │
│   - Not considered significant concern                    │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ BIAS DETECTION ANALYSIS                                   │
│                                                           │
│ ◐ Low bias risk in scoring (Confidence: 94%)            │
│                                                           │
│ Analysis:                                                │
│ • Name-based bias check: No unusual patterns detected    │
│ • Experience weighting: Objective criteria applied       │
│ • Education consideration: Technical relevance assessed  │
│ • Gaps evaluation: Standard industry norms applied       │
│                                                           │
│ [View Full Bias Report]                                  │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ RECOMMENDATION                                            │
│                                                           │
│ ★★★★★ STRONG ADVANCE                                     │
│ Recommendation: Send to hiring manager for interview     │
│ Confidence: 89%                                          │
│                                                           │
│ Similar Candidates: 3 others with 80+ scores            │
│                                                           │
│ [✓ Move to Next Stage] [Request More Info] [Archive]    │
│                                                           │
│ [Verify Extracted Data] [Download PDF Report]            │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Resume Upload & Processing**
   - Drag-and-drop or file selection
   - Support for PDF, DOCX formats
   - Processing status indicator
   - Error handling for corrupted/unsupported files

2. **Information Extraction**
   - Candidate name, contact, location
   - Work experience timeline
   - Education and certifications
   - Skills extraction with confidence levels
   - Employment gaps flagged

3. **Requirement Matching**
   - Score against job requirements
   - Skill matching with proficiency assessment
   - Experience level evaluation
   - Education alignment
   - Industry fit assessment

4. **AI Scoring & Reasoning**
   - Overall match score (0-100)
   - Component scores visualized
   - Detailed explanation of scoring factors
   - Points added/subtracted for different criteria
   - Comparable candidate context

5. **Bias Detection**
   - Name-based bias check
   - Experience weighting analysis
   - Education consideration fairness
   - Gap evaluation consistency
   - Confidence score on bias assessment

6. **Recommendations & Next Steps**
   - Clear recommendation (advance/hold/reject)
   - Confidence level
   - Suggested next action
   - Bulk action options
   - Data export

### Data Model

```javascript
{
  ResumeScreening: {
    screening_id: String (UUID),
    job_posting_id: String (UUID),
    candidate_id: String (UUID),
    resume_file_id: String,
    processing_date: Date,
    processing_time_ms: Number,
    
    extracted_information: {
      candidate_name: String,
      contact_email: String,
      phone_number: String,
      location: String,
      current_title: String,
      years_of_experience: Number,
      
      work_experience: [{
        company: String,
        title: String,
        start_date: Date,
        end_date: Date,
        duration_months: Number,
        description: String,
        industry: String
      }],
      
      education: [{
        institution: String,
        degree: String,
        field_of_study: String,
        graduation_date: Date,
        gpa: Decimal (optional)
      }],
      
      certifications: [{
        certification_name: String,
        issuing_organization: String,
        issue_date: Date,
        expiration_date: Date (optional),
        credential_id: String (optional)
      }],
      
      skills: [{
        skill_name: String,
        proficiency_level: Enum ("beginner", "intermediate", "advanced", "expert"),
        years_of_experience: Number,
        mentions_in_resume: Number,
        confidence_score: Decimal (0-1)
      }],
      
      employment_gaps: [{
        gap_start: Date,
        gap_end: Date,
        duration_months: Number,
        likely_reason: String (optional)
      }]
    },
    
    ai_scoring: {
      overall_score: Number (0-100),
      skill_match_score: Number (0-100),
      experience_match_score: Number (0-100),
      education_score: Number (0-100),
      industry_fit_score: Number (0-100),
      cultural_fit_score: Number (0-100),
      confidence_level: Decimal (0-1),
      
      scoring_components: [{
        component_name: String,
        points_awarded: Number,
        reasoning: String,
        weight: Decimal
      }],
      
      red_flags: [{
        flag_type: String,
        description: String,
        severity: Enum ("low", "medium", "high"),
        explanation: String
      }]
    },
    
    bias_analysis: {
      bias_risk_level: Enum ("low", "medium", "high"),
      confidence_score: Decimal (0-1),
      factors_analyzed: [String],
      recommendations: [String]
    },
    
    recommendation: {
      action: Enum ("advance", "hold", "reject", "needs_review"),
      confidence: Decimal (0-1),
      next_step: String,
      alternative_roles: [String] (optional)
    },
    
    human_review_status: {
      reviewed: Boolean,
      reviewer_id: String (UUID) (optional),
      review_date: Date (optional),
      human_override_score: Number (optional),
      human_recommendation: Enum ("advance", "hold", "reject") (optional)
    }
  }
}
```

### UI Components Required

1. **Resume Upload Area**
   - Drag-and-drop zone (min 200px height)
   - File input button
   - Supported formats indicator
   - File size limit display

2. **Extracted Data Cards**
   - Candidate info card (name, contact, location)
   - Experience timeline
   - Education list
   - Skills tags with confidence badges

3. **Scoring Visualization**
   - Overall score badge (large, 48px+)
   - Horizontal bar charts for component scores
   - Color-coded scale (red/yellow/green)
   - Percentage labels

4. **Red Flags Section**
   - Warning icons with text
   - Severity indicators
   - Clear explanations
   - Link to detailed analysis

5. **Reasoning Panel**
   - Expandable/collapsible sections
   - Bullet points for clarity
   - Score adjustments with reasons
   - Highlighted key factors

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text on white: 4.5:1 (#333333 body, #000000 headers)
- Score scale: Red (#C62828), Yellow (#F57C00), Green (#2E7D32) with 4.5:1
- Red flags: Warning icon + text (no color alone)
- Focus: 3px blue (#0066CC), 3:1 minimum

**Keyboard Navigation**
- Tab: Upload area → File button → Candidate info → Scores → Red flags → Recommendation → Actions
- Enter: Upload file, expand reasoning sections
- Escape: Cancel upload, close details

**Screen Reader Support**
- Page heading: `<h1>AI Resume Screening Assistant</h1>`
- Job context: `<h2>Job: Product Manager, San Francisco</h2>`
- Extracted info: `<section aria-labelledby="extracted-heading">`
  - Candidate announcement: "Candidate: Sarah Chen, San Francisco. 7 years experience as Product Manager"
- Score announcement: `<div role="status" aria-live="polite">Overall match score: 82 out of 100. Recommendation: Strong Advance. Confidence: 89 percent"</div>`
- Red flags: `<div role="region" aria-labelledby="flags-heading">`
  - Flag announcement: "Red flag: Unclear employment gap 6 months in 2020. Severity: low"
- Reasoning: `<details><summary aria-expanded="false">Show detailed reasoning</summary>`

**Focus Management**
- Visible focus indicator on all interactive elements (3px blue, 3:1 contrast)
- Initial focus on file upload area
- Skip link: "Skip to recommendation section"
- Tab order logical: upload → review → action

**Touch Targets**
- File upload button: 44×44 minimum
- Score card: 48×48 clickable areas
- Expand/collapse buttons: 44×44 minimum
- Action buttons: 48×56 minimum

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce`
- Score bar fills instantly, no animation
- Section expansion instant or slow fade (>2s)

---

## Screen 7.2: AI Job Matching Engine

### Overview
The AI Job Matching Engine helps candidates discover relevant opportunities and helps recruiters identify top candidates by analyzing skills, experience, and career goals against job requirements.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ AI Job Matching Engine                              [✕] │
├───────────────────────────────────────────────────────────┤
│                                                           │
│ CANDIDATE PROFILE SUMMARY                                 │
│ Sarah Chen                                                │
│ Current: Senior Product Manager                          │
│ Experience: 7 years in Product Management                │
│ Location: San Francisco Bay Area                         │
│ Open to relocation: Yes                                   │
│                                                           │
│ Career Goals:                                             │
│ "Looking to transition to a VP Product role within 2-3   │
│  years. Interested in high-growth startups or scaling     │
│  companies. Passionate about B2B SaaS and fintech."       │
│                                                           │
│ [Edit Profile] [View Skills] [Add Goals]                │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ MATCHED OPPORTUNITIES (9 matches)                         │
│                                                           │
│ [Filter: All ▼] [Sort: Best Match ▼] [Save All]        │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ MATCH 1: Senior Product Manager (Stripe)             │ │
│ │ Location: San Francisco | Posted: 2 weeks ago        │ │
│ │ ▐████████████░░ 92% Match                            │ │
│ │                                                      │ │
│ │ Why this match?                                       │ │
│ │ • Your Product Strategy skills align with role req  │ │
│ │ • Experience with B2B SaaS/fintech companies        │ │
│ │ • Leadership of cross-functional teams             │ │
│ │ • Remote-friendly, supports growth goals            │ │
│ │                                                      │ │
│ │ Gaps & Development Opportunities:                    │ │
│ │ ⚠ Payment/financial systems domain (2-3 months)     │ │
│ │ ⚠ Direct reports management (you have this!)        │ │
│ │                                                      │ │
│ │ Salary Range: $170k-$200k + equity                  │ │
│ │ Company Size: 2000+ | Growth Stage: Mature          │ │
│ │                                                      │ │
│ │ [View Full Job] [Learn Domain] [Save] [Share]      │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ MATCH 2: Director of Product (Notion)                │ │
│ │ Location: San Francisco | Posted: 3 weeks ago        │ │
│ │ ▐████████░░░░░░ 84% Match                            │ │
│ │                                                      │ │
│ │ Why this match?                                       │ │
│ │ • Strong alignment with team leadership & strategy  │ │
│ │ • Enterprise B2B product experience needed          │ │
│ │ • Org alignment with career progression goal        │ │
│ │                                                      │ │
│ │ Gaps: Enterprise SaaS platform experience           │ │
│ │                                                      │ │
│ │ Salary Range: $190k-$220k + equity                  │ │
│ │ [View Full Job] [Save] [Share]                      │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ MATCH 3: VP Product, Early Stage (Figma)             │ │
│ │ Location: San Francisco | Posted: 1 week ago         │ │
│ │ ▐██████░░░░░░░░ 76% Match                            │ │
│ │                                                      │ │
│ │ Why this match?                                       │ │
│ │ • This role aligns with your 2-3 year goal!         │ │
│ │ • Strong strategic thinking needed                   │ │
│ │                                                      │ │
│ │ Gaps: VP-level experience (you're ready to grow!)   │ │
│ │       Enterprise sales experience                    │ │
│ │                                                      │ │
│ │ Recommended Path:                                     │ │
│ │ Take a Director role first (1-2 yrs) → VP ready    │ │
│ │ Suggested courses: [Executive Leadership] [Sales]  │ │
│ │                                                      │ │
│ │ [View Full Job] [Save] [Share]                      │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ [Show More Matches (6 remaining)]                        │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ SAVED OPPORTUNITIES (3)                                   │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Product Manager, Uber | 78% | Last viewed: 3 days  │ │
│ │ Engineering Lead, Dropbox | 71% | Last viewed: 1w  │ │
│ │ [Remove] [View Details]                             │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ [View All Saved] [Create Job Alert]                     │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Candidate Profile**
   - Current role and experience summary
   - Career goals and preferences
   - Skills and endorsements
   - Availability and location flexibility
   - Edit capability

2. **Opportunity Matching**
   - AI-calculated match percentage
   - Explanation of why job matches
   - Skill alignment details
   - Gap analysis with growth opportunities
   - Recommended development path

3. **Match Ranking**
   - Sort by match %, salary, company, posting date
   - Filter by experience level, role type, location
   - Saved opportunities separate from browsing

4. **Development Recommendations**
   - Skills to develop for target roles
   - Suggested courses from learning platform
   - Timeline to readiness
   - Alternative paths to goals

5. **Sharing & Alerts**
   - Save individual jobs
   - Share with mentors/peers
   - Create alerts for matching opportunities
   - Email digest of top matches

### Data Model

```javascript
{
  JobMatch: {
    match_id: String (UUID),
    candidate_id: String (UUID),
    job_posting_id: String (UUID),
    match_date: Date,
    
    candidate_profile: {
      current_role: String,
      years_of_experience: Number,
      skills: [String],
      skill_proficiency: {
        [skill_name]: Enum ("beginner", "intermediate", "advanced", "expert")
      },
      location: String,
      relocation_willing: Boolean,
      preferred_locations: [String],
      
      career_goals: String,
      target_roles: [String],
      target_timeline_years: Number,
      job_preferences: {
        company_size: [String],
        industry: [String],
        growth_stage: [String],
        remote_preference: Enum ("fully_remote", "hybrid", "onsite")
      }
    },
    
    job_profile: {
      job_title: String,
      company_name: String,
      location: String,
      required_skills: [String],
      preferred_skills: [String],
      min_years_experience: Number,
      required_education: String,
      job_level: Enum ("entry", "mid", "senior", "lead", "executive"),
      salary_range_min: Decimal,
      salary_range_max: Decimal
    },
    
    match_analysis: {
      overall_match_percentage: Number (0-100),
      skill_match_percentage: Number (0-100),
      experience_match_percentage: Number (0-100),
      location_fit: Enum ("excellent", "good", "fair", "poor"),
      salary_alignment: Enum ("excellent", "good", "fair", "poor"),
      career_goal_alignment: Enum ("excellent", "good", "fair", "poor"),
      
      matched_skills: [String],
      missing_skills: [{
        skill: String,
        importance: Enum ("critical", "important", "nice_to_have"),
        estimated_learning_time_weeks: Number
      }],
      
      strength_summary: [String],  // Why this is a good match
      gap_summary: [String]         // What needs development
    },
    
    recommendation: {
      action: Enum ("strong_apply", "apply", "develop_first", "save_for_later", "not_fit"),
      confidence: Decimal (0-1),
      reasoning: String,
      development_path: {
        skills_to_develop: [{
          skill: String,
          courses: [String],
          estimated_time_weeks: Number
        }],
        timeline_to_readiness_months: Number
      }
    },
    
    user_actions: {
      saved: Boolean,
      saved_date: Date (optional),
      applied: Boolean,
      apply_date: Date (optional),
      shared_with: [String] (user IDs),
      viewed: Boolean,
      view_count: Number
    }
  }
}
```

### UI Components Required

1. **Candidate Profile Card**
   - Summary of key info (role, experience, location)
   - Career goals display
   - Edit buttons for profile updates

2. **Job Match Card**
   - Job title and company
   - Match percentage bar (0-100)
   - "Why this match" bullets
   - Gap analysis bullets
   - Salary range
   - Action buttons (View, Save, Share)

3. **Match Percentage Bar**
   - Horizontal bar with percentage
   - Color scale (red/yellow/green)
   - Animated fill based on match

4. **Gap Analysis Section**
   - Skills to develop with learning time
   - Importance levels (critical/important/nice-to-have)
   - Links to recommended courses

5. **Saved Jobs Section**
   - Simple list of saved opportunities
   - Match percentage and last viewed date
   - Quick action buttons

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text: 4.5:1 (#333333 body, #000000 headers)
- Match percentage scale: Red (#C62828), Yellow (#F57C00), Green (#2E7D32) with 4.5:1
- Gap importance: Red for critical, Orange for important, Green for learned
- Focus: 3px blue (#0066CC), 3:1 minimum

**Keyboard Navigation**
- Tab: Profile section → Match cards → Saved section → View/Save buttons
- Arrow keys: Navigate match cards up/down
- Enter: View job details, save/share
- Escape: Close modals

**Screen Reader Support**
- Page: `<h1>AI Job Matching Engine</h1>`
- Profile: `<section aria-labelledby="profile-heading">`
  - Summary: "Sarah Chen, Senior Product Manager, 7 years experience. Open to relocation. Career goal: VP Product in 2-3 years."
- Match card: `<article aria-labelledby="job-[id]-title">`
  - Match announcement: "Job: Senior Product Manager at Stripe, San Francisco. Match: 92%. This job aligns with your B2B SaaS and fintech interests. Skill gap: Payment systems domain (2-3 months to learn)"
- Match percentage: `<div role="img" aria-label="92 percent match">`
- Action buttons: Clear labels without icons alone

**Focus Management**
- Visible focus (3px blue, 3:1 contrast) on all interactive elements
- Initial focus: Profile section
- Skip link: "Skip to matched opportunities"
- Tab through cards sequentially

**Touch Targets**
- View/Save/Share buttons: 44×44 minimum
- Match card clickable areas: 48×48
- Skill links: 44×44 minimum

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce`
- Match bar fills instantly, no animation
- Card expansion/collapse instant

---

## Screen 7.3: AI Interview Insights

### Overview
The AI Interview Insights screen analyzes interview recordings/transcripts to provide objective assessments of candidate performance, communication style, and cultural fit indicators.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ AI Interview Insights                               [✕] │
├───────────────────────────────────────────────────────────┤
│ Interview: Sarah Chen - Product Manager                  │
│ Date: April 15, 2025 | Duration: 52 minutes              │
│ Interviewer: Alex Rodriguez | Role: Hiring Manager       │
│                                                           │
│ [View Recording] [View Transcript] [Download Report]     │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ AI ANALYSIS SUMMARY                                       │
│                                                           │
│ Overall Performance: ★★★★☆ (4.2/5)                     │
│ Recommendation: STRONG ADVANCE                            │
│ Confidence: 91%                                          │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ PERFORMANCE BREAKDOWN                                     │
│                                                           │
│ ┌────────────────────┐ ┌────────────────────┐            │
│ │ Communication      │ │ Technical Depth    │            │
│ │ ★★★★★ 4.5/5      │ │ ★★★★░ 4.0/5       │            │
│ │ • Clear articulation│ │ • Strong knowledge│            │
│ │ • Good pacing      │ │ • Concrete examples│            │
│ │ • Active listening │ │ • Understanding gaps
│ │                    │ │                    │            │
│ │ [Details]          │ │ [Details]          │            │
│ └────────────────────┘ └────────────────────┘            │
│                                                           │
│ ┌────────────────────┐ ┌────────────────────┐            │
│ │ Problem Solving    │ │ Cultural Fit       │            │
│ │ ★★★★░ 4.0/5      │ │ ★★★★★ 4.5/5       │            │
│ │ • Structured approach│ │ • Team collaboration
│ │ • Creative thinking│ │ • Company values  │            │
│ │ • Trade-off analysis│ │ • Growth mindset  │            │
│ │                    │ │                    │            │
│ │ [Details]          │ │ [Details]          │            │
│ └────────────────────┘ └────────────────────┘            │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ SENTIMENT & ENGAGEMENT ANALYSIS                           │
│                                                           │
│ Emotional Tone: Positive (87% positive sentiment)        │
│ Engagement Level: High (speaking 48%, listening 52%)     │
│ Confidence Level: Confident (few filler words, clear)    │
│                                                           │
│ Sentiment Timeline:                                       │
│ [00:00] ████████░░ [10:00] ███████░░░ [20:00]          │
│ [30:00] ██████████ [40:00] █████████░ [50:00]           │
│                                                           │
│ Transcript Excerpt (Key Moment - 12:35):                │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ [Q] "Walk us through a product failure you led..."   │ │
│ │ [A] "Great question. Early in my career at Asana,    │ │
│ │      I led a feature that didn't resonate..."        │ │
│ │                                                      │ │
│ │ 🎯 KEY INSIGHT: Shows self-awareness & learning     │ │
│ │                                                      │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ [Show Key Moments] [View Full Sentiment Timeline]       │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ KEY MOMENTS IDENTIFIED                                    │
│                                                           │
│ 1. Product Vision Clarity (3:45)                         │
│    "Our vision was to empower teams..." - Shows clarity  │
│                                                           │
│ 2. Team Leadership (18:20)                               │
│    Discussion of managing cross-functional teams         │
│    Insight: Demonstrates collaborative approach         │
│                                                           │
│ 3. Learning from Failure (12:35)                         │
│    Honest reflection on product failure                  │
│    Insight: Growth mindset, accountability              │
│                                                           │
│ [View All Moments] [Compare with Other Candidates]      │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ COMPARISON TO ROLE REQUIREMENTS                           │
│                                                           │
│ Requirement          | Interview Signal | Assessment      │
│ ──────────────────────────────────────────────────────── │
│ Product Strategy     | Discussed 5 times| ✓ Strong       │
│ Analytics/Data-driven| Mentioned metrics| ✓ Capable      │
│ Leadership           | Managed 5-8 people| ✓ Exceeds    │
│ Startup Experience   | SaaS background  | ✓ Relevant     │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ RED FLAGS & CONCERNS                                      │
│                                                           │
│ ◐ No significant concerns detected (Risk: Low)           │
│ • Minor: SQL/analytics knowledge could deepen           │
│ • Note: Seemed slightly nervous about compensation      │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ AI RECOMMENDATION                                         │
│                                                           │
│ ★★★★★ STRONG ADVANCE TO OFFER STAGE                     │
│                                                           │
│ Reasoning:                                                │
│ • Exceeds requirements across all competencies          │
│ • Strong communication & cultural fit                   │
│ • Growth mindset & learning orientation                │
│ • Would be top performer in role                        │
│                                                           │
│ Next Steps:                                              │
│ 1. Schedule offer discussion with hiring team           │
│ 2. Send competitive offer package                        │
│ 3. Start background check process                        │
│                                                           │
│ [✓ Move to Offer] [Schedule Team Discussion] [Archive]  │
│ [Share with Hiring Team] [Download PDF Report]          │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Interview Metadata**
   - Candidate name and role
   - Interview date, duration, interviewer
   - Recording/transcript availability
   - Report download option

2. **Performance Scoring**
   - Overall rating (star system or numeric)
   - Component scores (communication, technical, problem-solving, cultural fit)
   - Visual indicators for each dimension

3. **Sentiment Analysis**
   - Overall sentiment percentage
   - Engagement level (talk time ratio)
   - Confidence assessment
   - Timeline visualization of sentiment shifts

4. **Key Moments**
   - Automated identification of important discussion points
   - Timestamp and transcript excerpt
   - AI-identified insight (why it matters)
   - Comparison across candidates

5. **Requirement Alignment**
   - Job requirement vs. interview evidence
   - Signal strength assessment
   - Gap identification

6. **Red Flags & Concerns**
   - Risk level assessment
   - Specific concerns flagged
   - Notes and observations

### Data Model

```javascript
{
  InterviewInsights: {
    interview_id: String (UUID),
    candidate_id: String (UUID),
    job_posting_id: String (UUID),
    interview_date: Date,
    interview_duration_minutes: Number,
    interviewer_id: String (UUID),
    
    recording_metadata: {
      recording_file_id: String,
      duration_minutes: Number,
      format: String ("mp4", "webm", etc.),
      transcript_available: Boolean,
      transcript: String (full text)
    },
    
    ai_analysis: {
      analysis_date: Date,
      overall_performance_score: Number (0-5),
      recommendation: Enum ("strong_advance", "advance", "hold", "reject"),
      confidence_level: Decimal (0-1),
      
      performance_dimensions: [{
        dimension: Enum ("communication", "technical_depth", "problem_solving", "cultural_fit"),
        score: Number (0-5),
        key_observations: [String],
        evidence_from_transcript: [String]
      }],
      
      sentiment_analysis: {
        overall_sentiment_percentage: Decimal (0-1),  // 0 = negative, 1 = positive
        engagement_percentage: Decimal (0-1),  // candidate talk time / total time
        confidence_assessment: Enum ("very_low", "low", "moderate", "high", "very_high"),
        sentiment_timeline: [{
          timestamp_minutes: Number,
          sentiment_score: Decimal (0-1)
        }]
      },
      
      key_moments: [{
        timestamp_minutes: Number,
        timestamp_seconds: Number,
        transcript_excerpt: String,
        insight_label: String,
        insight_description: String,
        importance: Enum ("critical", "high", "medium", "low")
      }],
      
      requirement_assessment: [{
        requirement: String,
        evidence_from_interview: [String],
        signal_strength: Enum ("strong", "moderate", "weak", "absent"),
        assessment: String
      }],
      
      red_flags: [{
        flag_type: String,
        severity: Enum ("low", "medium", "high"),
        description: String,
        evidence: String
      }]
    },
    
    comparative_analysis: {
      compared_to_other_candidates: Number,  // count
      percentile_rank: Number (0-100),
      similar_candidates: [String]  // candidate IDs
    },
    
    human_review: {
      reviewed: Boolean,
      reviewer_id: String (UUID) (optional),
      review_date: Date (optional),
      human_notes: String (optional),
      human_override_recommendation: Enum ("strong_advance", "advance", "hold", "reject") (optional)
    }
  }
}
```

### UI Components Required

1. **Interview Header**
   - Candidate name, role, interview date
   - Interviewer info
   - Recording/transcript links

2. **Performance Score Cards**
   - Star rating or numeric score
   - Dimension labels
   - Key observations bullets
   - Details link

3. **Sentiment Timeline**
   - Horizontal chart showing sentiment over time
   - Engagement percentage display
   - Confidence level indicator

4. **Key Moments Section**
   - Timestamp with audio player link
   - Transcript excerpt in quote format
   - Insight label and description
   - Importance indicator

5. **Recommendation Card**
   - Large recommendation text
   - Star rating
   - Reasoning bullets
   - Action buttons

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text: 4.5:1 (#333333 body, #000000 headers)
- Stars: Gold (#F57F17, 4.5:1) and gray (#BDBDBD, 4.5:1)
- Sentiment positive: Green (#2E7D32, 4.5:1)
- Sentiment negative: Red (#C62828, 4.5:1)
- Focus: 3px blue (#0066CC), 3:1 minimum

**Keyboard Navigation**
- Tab: Header → Performance cards → Sentiment chart → Key moments → Recommendation → Actions
- Arrow keys: Navigate key moments, compare candidates
- Enter: View recording/transcript, expand details
- Escape: Close modals

**Screen Reader Support**
- Page: `<h1>AI Interview Insights - [Candidate Name]</h1>`
- Performance: `<section aria-labelledby="performance-heading">`
  - Announcement: "Sarah Chen interview analysis. Overall performance: 4.2 out of 5 stars. Recommendation: Strong Advance. Confidence: 91 percent"
- Dimension cards: `<div role="region" aria-label="Communication skills: 4.5 out of 5. Clear articulation, good pacing, active listening">`
- Sentiment: `<div role="img" aria-label="Sentiment timeline over 52 minutes. Overall positive sentiment 87 percent. Engagement: speaking 48%, listening 52%">`
- Key moments: `<section aria-labelledby="moments-heading">`
  - Moment: "Key Moment at 3 minutes 45 seconds. Product Vision Clarity. Candidate stated: 'Our vision was to empower teams...' Insight: Shows clear product strategy understanding"
- Requirement table: Proper `<table>` with `<thead>`, headers

**Focus Management**
- Visible focus (3px blue, 3:1 contrast) on all interactive
- Initial focus: Performance summary
- Skip link: "Skip to recommendation"
- Tab order logical through sections

**Touch Targets**
- Recording player button: 44×44 minimum
- Performance card expand: 44×44 minimum
- Key moment timestamp links: 44×44 minimum
- Recommendation action buttons: 48×56 minimum

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce`
- Sentiment timeline animation instant or slow fade
- Score changes instant display

---

## Screen 7.4: AI Performance Insights

### Overview
AI Performance Insights analyzes employee performance data, predicts risks (attrition, underperformance), identifies high performers, and provides development recommendations for managers and executives.

### Wireframe Layout

```
┌───────────────────────────────────────────────────────────┐
│ AI Performance Insights                             [✕] │
├───────────────────────────────────────────────────────────┤
│ Department: Product Management | Team: Product            │
│ Analysis Period: Q1 2025 | Last Updated: April 20, 2025  │
│                                                           │
│ [View by: Team ▼] [Analysis Period: Q1 2025 ▼]          │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ TEAM HEALTH DASHBOARD                                     │
│                                                           │
│ Team Performance: ████████░░ 78/100 (Above Average)      │
│ Team Engagement: ████████░░ 75/100                       │
│ Retention Risk: ███░░░░░░░ 25/100 (Low Risk)            │
│                                                           │
│ Key Metrics:                                              │
│ Average Goal Achievement: 92% | Team Size: 10 | Turnover:0%│
│                                                           │
├───────────────────────────────────────────────────────────┤
│ TEAM MEMBER INSIGHTS                                      │
│                                                           │
│ [Filters: All ▼] [Sort By: Risk Level ▼] [Export]       │
│                                                           │
│ HIGH PERFORMERS (3 members)                               │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ ★ Sarah Chen - Senior Product Manager               │ │
│ │ Performance Score: 4.8/5 | Goal Achievement: 110%   │ │
│ │                                                      │ │
│ │ Strengths:                                           │ │
│ │ • Exceeds goals consistently (+10% above target)    │ │
│ │ • Strong leadership & team collaboration            │ │
│ │ • Drives innovation (3 new initiatives launched)    │ │
│ │                                                      │ │
│ │ Promotion Readiness: 95% (Ready for Director role)  │ │
│ │ Succession Plan: Yes - could backfill Sr. PM        │ │
│ │                                                      │ │
│ │ Recommended Action: Discuss promotion path          │ │
│ │                                                      │ │
│ │ [View Detailed Profile] [Create Dev Plan] [Details]│ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ ★ Marcus Liu - Product Manager                      │ │
│ │ Performance Score: 4.3/5 | Goal Achievement: 105%   │ │
│ │                                                      │ │
│ │ Promotion Readiness: 75% (2-3 months development)   │ │
│ │ Key Gap: Leadership of larger cross-functional team │ │
│ │ Dev Plan: Enroll in leadership bootcamp             │ │
│ │                                                      │ │
│ │ [View Detailed Profile] [Create Dev Plan] [Details]│ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ PERFORMERS AT RISK (2 members)                            │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ ⚠ Jennifer Park - Product Manager                   │ │
│ │ Performance Score: 2.8/5 | Goal Achievement: 65%    │ │
│ │ Attrition Risk: HIGH (78%)                           │ │
│ │ Engagement Score: 2.2/5 (Low - concerning)          │ │
│ │                                                      │ │
│ │ Risk Indicators:                                     │ │
│ │ • Performance declining trend (was 3.5 Q4 2024)     │ │
│ │ • Engagement drop following promotion that didn't   │ │
│ │   work out - likely role misalignment                │ │
│ │ • Meeting attendance down 30%                        │ │
│ │                                                      │ │
│ │ Recommended Actions:                                 │ │
│ │ 1. Schedule 1:1 conversation about role fit         │ │
│ │ 2. Discuss career interests and goals               │ │
│ │ 3. Consider role change or mentoring support        │ │
│ │                                                      │ │
│ │ [View Full Profile] [Schedule Meeting] [View Dev]  │ │
│ │ [Retention Action Plan] [Details]                   │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ DEVELOPMENT OPPORTUNITIES (5 members)                     │
│                                                           │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ ◐ Alex Rodriguez - Product Manager (3 months)       │ │
│ │ Performance Score: 3.2/5 | Goal Achievement: 80%    │ │
│ │ Dev Need: SQL/Analytics skills                       │ │
│ │ Recommended: Data Analytics for PMs course          │ │
│ │ Timeline: 6-8 weeks to proficiency                  │ │
│ │                                                      │ │
│ │ [View Profile] [Assign Course] [Details]            │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ [Show More Performance Insights (2 remaining)]           │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ PERFORMANCE TRENDS                                        │
│                                                           │
│ Team Performance Over Time                               │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Score:  Q4 2024: 75 → Q1 2025: 78 (+3 points)      │ │
│ │                                                      │ │
│ │ ███████░░ Q4: 75  ██████████ Q1: 78  ↑ +4%          │ │
│ │                                                      │ │
│ │ Trend: Improving overall (especially Sarah, Marcus) │ │
│ │ Concern: Jennifer's decline needs attention         │ │
│ └──────────────────────────────────────────────────────┘ │
│                                                           │
│ [View Detailed Trend Analysis]                           │
│                                                           │
├───────────────────────────────────────────────────────────┤
│ AI PREDICTIONS                                            │
│                                                           │
│ Attrition Risk (Next 6 months):                          │
│ • HIGH RISK: Jennifer Park (78%) - needs immediate action│
│ • MEDIUM RISK: None currently                            │
│ • LOW RISK: Rest of team                                 │
│                                                           │
│ Promotion Readiness (Next 12 months):                     │
│ • Ready Now: Sarah Chen (Director role)                  │
│ • Ready in 2-3 months: Marcus Liu, with development      │
│ • Not Ready: Rest of team (skill gaps identified)       │
│                                                           │
│ [View Full Risk Analysis] [Create Retention Plans]       │
│                                                           │
│ [Generate Department Report] [Export Data]               │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

1. **Team Health Dashboard**
   - Overall performance, engagement, and retention risk scores
   - Team size, turnover rate, average metrics
   - Quick status summary

2. **Team Member Segmentation**
   - High performers with promotion readiness
   - At-risk employees with attrition indicators
   - Development opportunities identified

3. **Detailed Performance Analysis**
   - Individual performance scores
   - Goal achievement tracking
   - Strengths and capability assessment
   - Recommended actions and development paths

4. **Risk Indicators**
   - Attrition risk scoring with confidence
   - Performance trend analysis
   - Engagement decline detection
   - Early warning signals

5. **Trend Analysis**
   - Historical performance comparison
   - Trend lines with directional indicators
   - Peer benchmark comparisons

6. **Predictive Insights**
   - Promotion readiness scoring
   - Attrition probability estimates
   - Development timeline projections
   - Succession planning indicators

### Data Model

```javascript
{
  PerformanceInsights: {
    insight_id: String (UUID),
    team_id: String (UUID),
    analysis_date: Date,
    analysis_period: Enum ("Q1", "Q2", "Q3", "Q4", "monthly"),
    fiscal_year: Number,
    
    team_health: {
      team_size: Number,
      performance_score: Number (0-100),
      engagement_score: Number (0-100),
      retention_risk_score: Number (0-100),  // lower = better
      turnover_rate_percentage: Decimal,
      average_goal_achievement_percentage: Decimal,
      average_performance_rating: Number (0-5)
    },
    
    team_member_performance: [{
      employee_id: String (UUID),
      name: String,
      role: String,
      performance_score: Number (0-5),
      goal_achievement_percentage: Decimal,
      engagement_score: Number (0-5),
      
      performance_category: Enum ("high_performer", "solid_performer", "development_needed", "at_risk"),
      
      strengths: [String],
      development_needs: [String],
      
      promotion_readiness: {
        score: Decimal (0-1),  // 0-100%
        target_role: String (optional),
        gaps_to_address: [String],
        estimated_months_to_readiness: Number
      },
      
      attrition_risk: {
        risk_level: Enum ("low", "medium", "high"),
        risk_score: Decimal (0-1),  // 0-100%
        primary_risk_factors: [String],
        confidence_level: Decimal (0-1)
      },
      
      succession_plan: {
        can_backfill_roles: [String],
        ready_to_backfill: Boolean,
        development_plan_id: String (optional)
      }
    }],
    
    performance_trends: [{
      employee_id: String (UUID),
      previous_period_score: Number (0-5),
      current_period_score: Number (0-5),
      trend_direction: Enum ("improving", "stable", "declining"),
      trend_magnitude: Number (-5 to 5),  // percentage points
      trend_confidence: Decimal (0-1)
    }],
    
    team_predictions: {
      attrition_predictions: [{
        employee_id: String (UUID),
        attrition_probability_6mo: Decimal (0-1),
        attrition_probability_12mo: Decimal (0-1),
        primary_risk_factors: [String]
      }],
      
      promotion_ready_employees: [{
        employee_id: String (UUID),
        target_role: String,
        readiness_timeline_months: Number,
        development_priorities: [String]
      }],
      
      recommended_succession_candidates: [{
        employee_id: String (UUID),
        target_role: String,
        readiness_score: Decimal (0-1),
        timeline_months: Number
      }]
    },
    
    recommended_actions: [{
      action_type: Enum ("promote", "develop", "retain", "manage_out", "mentor"),
      employee_id: String (UUID),
      action_description: String,
      urgency: Enum ("low", "medium", "high", "critical"),
      confidence: Decimal (0-1)
    }]
  }
}
```

### UI Components Required

1. **Health Dashboard Cards**
   - Large score display (numeric 0-100)
   - Label below
   - Horizontal progress bar
   - Quick metrics below each score

2. **Team Member Cards**
   - Name, role, performance score (star or numeric)
   - Goal achievement % displayed prominently
   - Strengths bullets
   - Risk/opportunity indicators
   - Action button links

3. **Risk Indicator Badge**
   - Color-coded (green/yellow/red)
   - Risk label (Low/Medium/High)
   - Score display
   - Expandable to show factors

4. **Trend Chart**
   - Line chart or bar chart comparing periods
   - Directional arrow (↑↓→)
   - Percentage change display

5. **Action Cards**
   - Recommended action text
   - Urgency indicator
   - Employee reference
   - Quick action links

### WCAG 2.2 AA Accessibility Requirements

**Color Contrast**
- Text: 4.5:1 (#333333 body, #000000 headers)
- Performance bars: Green (#2E7D32), Yellow (#F57C00), Red (#C62828) with 4.5:1
- Star ratings: Gold (#F57F17, 4.5:1) and gray (#BDBDBD, 4.5:1)
- Risk badges: Red (high), Orange (medium), Green (low) with 4.5:1
- Focus: 3px blue (#0066CC), 3:1 minimum

**Keyboard Navigation**
- Tab: Team health section → Member cards → Trends → Predictions → Actions
- Arrow keys: Navigate member list, expand details
- Enter: Expand member card, view detailed profile
- Escape: Close expanded views

**Screen Reader Support**
- Page: `<h1>AI Performance Insights - Product Management Team</h1>`
- Health section: `<section aria-labelledby="health-heading">`
  - Summary: "Team performance score: 78 out of 100, above average. Engagement: 75 out of 100. Retention risk: 25 out of 100, low risk."
- Member cards: `<article aria-labelledby="member-[id]-name">`
  - Announcement: "Sarah Chen, Senior Product Manager. Performance: 4.8 out of 5. Goal achievement: 110%. High performer. Promotion ready: 95% ready for Director role."
- Risk indicators: `<div role="status" aria-live="polite">`
  - "Jennifer Park: HIGH attrition risk 78%. Engagement declining. Needs manager attention."
- Trend chart: `<div role="img" aria-label="Team performance Q4 2024 to Q1 2025: improved from 75 to 78, trend is improving">`

**Focus Management**
- Visible focus (3px blue, 3:1 contrast) on all interactive
- Initial focus: Team health dashboard
- Skip link: "Skip to team member insights"
- Tab order logical through sections and cards

**Touch Targets**
- Member cards: Minimum 44px height
- Action buttons: 44×44 minimum
- Expand/collapse: 44×44 minimum
- Risk badge click areas: 48×48 minimum

**Motion & Animation**
- Respect `prefers-reduced-motion: reduce`
- Performance bar fills instantly
- Trend chart renders instantly

