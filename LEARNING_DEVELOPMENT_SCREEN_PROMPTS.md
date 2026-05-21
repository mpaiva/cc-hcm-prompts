# Learning & Development Screen Prompts

> **Accessibility Standard**: All screens below meet WCAG 2.2 AA standards with comprehensive accessibility requirements covering color contrast, keyboard navigation, screen reader compatibility, focus management, touch targets, error handling, and motion preferences.

---

## Screen 5.1: Learning Catalog

### Purpose
Enable employees to discover, browse, and search available learning opportunities including courses, certifications, videos, and resources with AI-powered personalized recommendations and skill-based filtering.

### User Personas
- **Primary**: All Employees
- **Secondary**: Managers (can assign courses to direct reports)

### Layout & Wireframe

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ←  Learning Catalog             [My Courses]  [Paths]  [Skills]│
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  SEARCH & FILTERS                                                │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ [Search: "Project Management" ... ⚪]                        ││
│  │                                                              ││
│  │ FILTERS:                                                     ││
│  │ Topic:     [All Topics ▼]  [Leadership] [Technical] [Sales]││
│  │ Level:     [All Levels ▼]   [Beginner] [Intermediate] [Adv]││
│  │ Format:    [All Formats ▼]  [Video] [Interactive] [Article]││
│  │ Duration:  [All Durations ▼] [< 1 hour] [1-3 hours]        ││
│  │ Provider:  [All Providers ▼] [Acme Learning] [Udemy]        ││
│  │ Status:    [All ▼]  [Not Started] [In Progress] [Completed]││
│  │                                                              ││
│  │ [Apply Filters]  [Reset]  [Save Search]                     ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  RECOMMENDED FOR YOU (Based on your role & skills)               │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ ┌──────────────┐ Advanced Product Management Strategy       ││
│  │ │ VIDEO COURSE │ Complete 4-week course on strategic...    ││
│  │ │ 12 hours     │ Provider: Acme Learning | Level: Advanced ││
│  │ │              │ ★★★★★ (487 reviews) | 2,341 enrolled      ││
│  │ │ Progress: 0% │ Your reason: Aligns with PM skills         ││
│  │ │ [Enroll]     │ [View Details]  [Save]                    ││
│  │ └──────────────┘                                             ││
│  │                                                              ││
│  │ ┌──────────────┐ Data Analysis Fundamentals                ││
│  │ │INTERACTIVE   │ Hands-on SQL, Excel, Tableau training... ││
│  │ │6 hours       │ Provider: TechSkills | Level: Beginner    ││
│  │ │              │ ★★★★☆ (234 reviews) | 1,567 enrolled      ││
│  │ │ Progress: 0% │ Your reason: Skill gap detected           ││
│  │ │ [Enroll]     │ [View Details]  [Save]                    ││
│  │ └──────────────┘                                             ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  POPULAR COURSES (This Month)                                    │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ ┌──────────────┐ Effective Communication (15,234 enrolled)  ││
│  │ │ VIDEO COURSE │ Learn to communicate with impact          ││
│  │ │ 3 hours      │ Level: Beginner | Provider: Acme          ││
│  │ │              │ ★★★★★ (2,456 reviews)                     ││
│  │ │ [Enroll]     │ [View Details]  [Save]                    ││
│  │ └──────────────┘                                             ││
│  │                                                              ││
│  │ [View More Popular Courses...]                              ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  ALL COURSES (1,247 available)                                   │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ [Grid View] [List View]                    Page 1 of 83      ││
│  │                                                              ││
│  │ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐         ││
│  │ │ PROJECT      │ │ AGILE MASTER │ │ SCRUM MASTER │         ││
│  │ │ MANAGEMENT   │ │ CLASS        │ │ CERT PREP    │         ││
│  │ │ BASICS       │ │              │ │              │         ││
│  │ │ 8 hours      │ │ 20 hours     │ │ 40 hours     │         ││
│  │ │ Beginner     │ │ Intermediate │ │ Advanced     │         ││
│  │ │ ★★★★☆       │ │ ★★★★★       │ │ ★★★★★       │         ││
│  │ │ [Enroll]     │ │ [Enroll]     │ │ [Enroll]     │         ││
│  │ │ [Details]    │ │ [Details]    │ │ [Details]    │         ││
│  │ └──────────────┘ └──────────────┘ └──────────────┘         ││
│  │                                                              ││
│  │ [Next Page →]                                               ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

#### 1. Search Functionality
- **Search Bar**
  - Real-time search across course titles, descriptions, skills
  - Autocomplete suggestions
  - Recent searches dropdown
  - Search history
  - Advanced search option

- **Search Results**
  - Results count
  - Relevant courses sorted by relevance
  - Filter suggestions based on results
  - "Did you mean?" for typos

#### 2. Filtering System
- **Topic Filter**
  - Leadership, Technical Skills, Sales, Communication, Compliance, etc.
  - Multi-select
  - Tag-based browsing
  - Show course count per topic

- **Level Filter**
  - Beginner, Intermediate, Advanced, Expert
  - Self-assessment quiz to suggest level
  - Show prerequisites per level

- **Format Filter**
  - Video courses
  - Interactive/hands-on courses
  - Readings/articles
  - Assessments/quizzes
  - Live sessions
  - Blended (mixed formats)

- **Duration Filter**
  - Less than 1 hour
  - 1-3 hours
  - 3-8 hours
  - 1-2 weeks
  - 2-4 weeks
  - Longer than 4 weeks

- **Provider Filter**
  - Internal courses
  - Acme Learning (internal provider)
  - Udemy, LinkedIn Learning, Coursera, etc.
  - Free vs. Paid courses

- **Status Filter**
  - Not started
  - In progress
  - Completed
  - Saved (bookmarked)

#### 3. Recommended Courses
- **Personalized Recommendations**
  - Based on current role: "Product Manager courses"
  - Based on skill gaps: "Data analysis skills gap detected"
  - Based on goals: "Aligned with your learning goals"
  - Based on peer activity: "Popular in your team"
  - Based on performance: "Recommended to strengthen competency X"

- **Recommendation Explanation**
  - Why is this recommended for you
  - How it relates to your role/skills
  - Estimated time to complete
  - Alignment with goals/paths

#### 4. Course Preview/Details
- **Course Card Display**
  - Course thumbnail/image
  - Title and provider
  - Brief description
  - Duration and level
  - Format icon/indicator
  - Star rating and review count
  - Enrollment count (popularity)
  - Instructor/creator name

- **Course Details Modal**
  - Full course description
  - Learning objectives (bullet list)
  - Course syllabus/modules
  - Duration breakdown
  - Requirements/prerequisites
  - Instructor biography
  - Reviews and ratings
  - Student testimonials
  - Related courses
  - Skills taught (tags)
  - Pricing/cost (if applicable)

#### 5. Popular & Trending
- **Popular This Month**
  - Top courses by enrollment
  - Top rated courses
  - Most completed courses

- **By Category/Topic**
  - Top courses in each topic area
  - Trending certifications

#### 6. Save & Enroll
- **Save Course**
  - Bookmark for later
  - Add to learning path
  - Add to calendar

- **Enroll Button**
  - One-click enrollment
  - Redirect to enrollment confirmation

### Data Model

```
Course {
  id: UUID
  title: String
  description: String
  long_description: Text
  provider_id: UUID (FK to ContentProvider)
  provider_name: String
  
  format: Enum (VIDEO, INTERACTIVE, ARTICLE, ASSESSMENT, LIVE_SESSION, BLENDED)
  level: Enum (BEGINNER, INTERMEDIATE, ADVANCED, EXPERT)
  duration_minutes: Integer
  duration_display: String (e.g., "4 hours", "2 weeks")
  
  learning_objectives: Array<String>
  topics: Array<String> (tags)
  skills_taught: Array<Skill {
    skill_id: UUID
    skill_name: String
    proficiency_level: String
  }>
  
  prerequisites: Array<UUID> (course IDs)
  
  course_image_url: String
  course_preview_url: String (if video)
  
  instructor_id: UUID (nullable)
  instructor_name: String
  instructor_bio: String (nullable)
  
  rating: Decimal (0-5)
  review_count: Integer
  enrollment_count: Integer
  completion_rate: Decimal (% of enrolled who completed)
  
  cost: Decimal (0 if free)
  currency: String (nullable)
  
  is_mandatory: Boolean
  required_for_roles: Array<UUID> (Role IDs)
  
  modules: Array<Module {
    id: UUID
    title: String
    order: Integer
    duration_minutes: Integer
    content_type: Enum (VIDEO, INTERACTIVE, ARTICLE, QUIZ)
  }>
  
  status: Enum (DRAFT, ACTIVE, ARCHIVED)
  created_at: Timestamp
  updated_at: Timestamp
}

ContentProvider {
  id: UUID
  name: String
  type: Enum (INTERNAL, EXTERNAL)
  url: String (nullable)
  logo_url: String (nullable)
  description: String (nullable)
}

CourseEnrollment {
  id: UUID
  employee_id: UUID (FK to Employee)
  course_id: UUID (FK to Course)
  enrollment_date: Date
  status: Enum (ENROLLED, IN_PROGRESS, COMPLETED, DROPPED, WAITLISTED)
  progress_percentage: Decimal (0-100)
  completion_date: Date (nullable)
  score: Decimal (nullable, for graded courses)
  time_spent_minutes: Integer
  due_date: Date (nullable)
  assigned_by_manager: Boolean (true if manager assigned)
  assigned_by_manager_id: UUID (nullable)
  required_for_compliance: Boolean
}

CourseReview {
  id: UUID
  course_id: UUID (FK to Course)
  employee_id: UUID (FK to Employee)
  rating: Integer (1-5)
  review_text: String (optional)
  created_at: Timestamp
}

CourseSave {
  id: UUID
  employee_id: UUID (FK to Employee)
  course_id: UUID (FK to Course)
  saved_at: Timestamp
}

Skill {
  id: UUID
  name: String
  category: String
  description: String
}

LearningPath {
  id: UUID
  title: String
  description: String
  courses: Array<UUID> (ordered course IDs)
  target_duration_days: Integer
  skills_covered: Array<UUID> (skill IDs)
}
```

### UI Components Required
- Search bar with autocomplete
- Filter menu (multi-select dropdowns)
- Card component: Course card
- Modal: Course details/preview
- Badge: Level indicator, format icon, rating
- Grid view and list view toggle
- Pagination
- Save button / Bookmark icon
- Enroll button
- Rating display (star rating)

### WCAG 2.2 AA Accessibility Requirements

#### Color & Contrast
- Course cards have 4.5:1 text contrast
- Level badges (Beginner, Intermediate, Advanced) have text labels + color (not color alone)
- Star ratings have text alternative ("4.5 out of 5 stars")
- Duration and provider information readable at 4.5:1
- Links to course details have distinct color
- Filter badges have clear visual distinction

#### Keyboard Navigation
- Tab through search and filter inputs
- Arrow keys navigate filter dropdowns
- Enter to apply filters
- Tab through course cards
- Arrow keys navigate course grid
- Enter to open course details modal
- Escape to close modal
- All buttons keyboard accessible

#### Screen Reader Support
- Page title: "Learning Catalog"
- Search section: `<section aria-label="Search and filter learning opportunities">`
- Search input: `<label for="course-search">Search courses, topics, skills</label><input id="course-search" aria-describedby="search-help">`
- Filter section: `<fieldset aria-label="Learning filters"><legend>Refine your search</legend>...`
- Each filter: `<label for="topic-filter">Topic</label><select id="topic-filter" aria-expanded="false">`
- Course card: `<article aria-label="Advanced Project Management, 12 hours, Advanced level, Video course, 4.5 stars out of 5, 487 reviews">`
- Course count: `<div aria-live="polite">Showing 12 of 1,247 courses</div>`
- Recommended section: `<section aria-label="Recommended for You (3 recommendations)">`
- Recommendation reason: `<span aria-label="Recommended because: Aligns with your Product Manager role">Aligns with your PM role</span>`
- Level badge announces: `<span aria-label="Advanced level">Advanced</span>`
- Format indicator: `<span aria-label="Video course">🎥</span>` with text alternative

#### Focus Management
- Search input receives focus on page load
- When modal opens (course details), focus trapped in modal
- Escape closes modal, focus returns to course card
- When filter applied, focus remains on filter button
- Pagination focus stays on current page indicator

#### Touch & Target Size
- Search input: 44px minimum height
- Filter buttons: 44×44 px minimum
- Course cards: touch-friendly size (min 60px height)
- Enroll/Save buttons on cards: 44×44 px
- Course detail button: 44×44 px
- Filter tags/badges: 40px height minimum
- Pagination buttons: 44×44 px

#### Error Handling & Validation
- No results found: "No courses found matching your search. Try different keywords or adjust filters." (clear, actionable)
- Search with no results: "Try searching for 'Project Management' or browse by topic instead." (suggestions)
- Filter error: "Unable to load courses. Please try again." with retry button
- All errors have `role="alert"`

#### Motion & Animation
- Filter application respects `prefers-reduced-motion` (instant update, no animation)
- Course card hover effects work without animation dependency
- Modal opening/closing respects preference (instant, no fade)
- Grid transitions instant (no slide animation)

#### Semantic HTML & ARIA
- Proper heading hierarchy: `<h1>` Learning Catalog, `<h2>` Recommended, Popular, All Courses
- Course list as `<section>` with course `<article>` elements
- Filters in `<fieldset>` with `<legend>`
- Form inputs with associated `<label>` tags
- Rating as `<span aria-label="4.5 out of 5 stars">`
- Prerequisites list as `<ul>`

### AI Integration Points

#### 1. Personalized Recommendations
- **Role-Based**: "As a Product Manager, you may benefit from Strategy, Data Analysis, and Leadership courses"
- **Skill Gap Analysis**: "We detected a gap in SQL skills. Recommend Data Analysis course"
- **Peer Learning**: "15 engineers in your team completed AWS Certification. Consider enrolling?"
- **Career Path**: "For advancement to Senior PM, consider Product Strategy and Executive Communication courses"

#### 2. Smart Search & Filtering
- **Natural Language Search**: "courses for managing remote teams" → finds Distributed Team Management, Remote Work, Leadership
- **Skill-to-Course Mapping**: Search by desired skill, shows courses that teach it
- **Recommendation Based on Searches**: "Searching for 'data analysis'? Also consider Statistics Fundamentals"

#### 3. Learning Path Recommendations
- **Auto-Sequencing**: Based on prerequisites and learning flow, suggest optimal course order
- **Personalized Paths**: "To develop Product Strategy skills, start with: Intro to Strategy → Market Analysis → Product Roadmapping → Strategic Planning"

#### 4. Popularity & Trending Analysis
- **Trending by Role**: "Trending in Product: AI/ML for Product, Data Literacy, Generative AI Adoption"
- **Trending by Company**: "New on platform: Agile at Scale, AI Fundamentals, Cloud Security"

### Integrations & Dependencies

#### Internal Integrations
- **HRIS Core**: Employee role, team, department for recommendations
- **Performance Management**: Recent goals and feedback for skill gap detection
- **Career Development Plans**: Current development goals
- **Learning Completion System**: Track enrollment, progress, completion
- **Notification System**: Email reminders for assigned courses

#### External Integrations
- **Content Providers**: Udemy, LinkedIn Learning, Coursera (API for catalog sync)
- **LMS**: Moodle, Canvas for internal course hosting
- **Analytics**: Track course popularity, completion rates
- **Calendar**: Calendar integration for course scheduling

### Edge Cases & Error States

#### 1. Prerequisite Management
- **Locked Courses**: If prerequisite not complete, show "Complete X course first"
- **Prerequisite Chains**: Multiple prerequisites shown in order
- **Skip Prerequisite**: Option to request skip (requires manager approval for some courses)

#### 2. Course Capacity
- **Waitlist**: When course full, option to join waitlist
- **Scheduled Sessions**: Live courses show "4 seats remaining" or "Session full"

#### 3. Cost & Approval
- **Free vs. Paid**: Clearly indicate which courses have cost
- **Budget Approval**: Expensive courses (> $500) require manager approval
- **Payment Processing**: Redirect to payment or billing department

#### 4. Inactive Courses
- **Archived Courses**: Show "This course is no longer available" but allow viewing details
- **Obsolete Content**: "This course content is outdated. We recommend X instead"

### Success Metrics & Testing Scenarios

#### Search & Filtering
- [ ] Search finds relevant courses
- [ ] Filters apply correctly and narrow results
- [ ] Multi-filter combinations work properly
- [ ] Search results update in real-time
- [ ] Filter reset clears all selections

#### Course Display
- [ ] Course cards display all required information
- [ ] Course details modal opens and shows full info
- [ ] Rating and review count display correctly
- [ ] Prerequisite information clear
- [ ] Related courses suggested

#### Enrollment
- [ ] Enroll button works from catalog and details
- [ ] Enrollment confirmation received
- [ ] Course appears in "My Courses" after enrollment
- [ ] Assigned courses visible with "Assigned by Manager" label

#### Accessibility
- [ ] Search keyboard navigable
- [ ] Filter dropdowns keyboard operable
- [ ] Course cards navigable with arrow keys
- [ ] Screen reader announces course info
- [ ] Modal focus trapped and Escape closes

---

## Screen 5.2: Course Enrollment & Progress

### Purpose
Enable employees to track their learning progress, complete course modules, take assessments, access course materials, and earn completion certificates with AI-powered adaptive pacing and progress predictions.

### User Personas
- **Primary**: All Employees
- **Secondary**: Managers (view direct reports' progress), Instructors (for live courses)

### Layout & Wireframe

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ←  Advanced Project Management Strategy     [Catalog]  [Support]│
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  COURSE HEADER                                                   │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Course: Advanced Project Management Strategy                ││
│  │ Provider: Acme Learning  |  Level: Advanced  |  12 hours    ││
│  │ Status: In Progress (started Jan 15, 2025)                  ││
│  │ Instructor: Dr. Jane Smith                                   ││
│  │ Enrollment Status: Active                                    ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  PROGRESS DASHBOARD                                              │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Overall Progress: ■■■■■■░░░░  55% Complete (6.6 of 12 hrs)  ││
│  │                                                              ││
│  │ Expected Completion: Feb 15, 2025 (18 days remaining)       ││
│  │ Pace Forecast: On Track                                      ││
│  │ Time Remaining: ~5.4 hours                                   ││
│  │                                                              ││
│  │ Predicted Time to Complete: Feb 12, 2025 (with current pace)││
│  │ Recommendation: Increase pace by 1 hour/week to finish 3    ││
│  │                 days early (or stay on current pace)        ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  LEARNING OBJECTIVES                                             │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ By completing this course, you will be able to:             ││
│  │ ✓ Define strategic project management principles            ││
│  │ ✓ Develop comprehensive project plans                       ││
│  │ ○ Manage stakeholder expectations effectively               ││
│  │ ○ Lead high-performing project teams                        ││
│  │ ○ Manage project budgets and resources                      ││
│  │ ○ Handle project risks and uncertainties                    ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  COURSE MODULES (4 of 6 completed)                               │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ ✓ Module 1: Foundations of Strategic PM (1.5 hours)         ││
│  │   Completed: Jan 20, 2025  |  Score: 88%  |  Locked: No     ││
│  │   [Review]  [View Certificate]                              ││
│  │                                                              ││
│  │ ✓ Module 2: Stakeholder Engagement (2 hours)                ││
│  │   Completed: Jan 25, 2025  |  Score: 92%  |  Locked: No     ││
│  │   [Review]  [View Certificate]                              ││
│  │                                                              ││
│  │ ✓ Module 3: Project Planning & Execution (2 hours)          ││
│  │   Completed: Feb 1, 2025  |  Score: 85%  |  Locked: No      ││
│  │   [Review]  [View Certificate]                              ││
│  │                                                              ││
│  │ ► Module 4: Team Leadership & Dynamics (1.1 of 2 hours)    ││
│  │   In Progress  |  Latest: Feb 8, 2025  |  [Resume Course]  ││
│  │   Progress: 55%  |  Time Spent: 1.1 hours                   ││
│  │   [Continue]  [Bookmark]  [Take Notes]  [Restart]          ││
│  │                                                              ││
│  │ ○ Module 5: Budget & Resource Management (2 hours)          ││
│  │   Not Started  |  Unlocks: Upon Module 4 completion         ││
│  │   [Preview]                                                  ││
│  │                                                              ││
│  │ ○ Module 6: Risk Management & Contingency (1.5 hours)       ││
│  │   Not Started  |  Unlocks: Upon Module 5 completion         ││
│  │   [Preview]                                                  ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  CURRENT MODULE: TEAM LEADERSHIP & DYNAMICS                      │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │                                                              ││
│  │ [Video Player]                                               ││
│  │ ┌──────────────────────────────────────────────────────────┐││
│  │ │ ▶ Lesson 1: Building Trust in Project Teams  [6:45]     │││
│  │ │ ━━━━━━━━━━━━━━  30%  [1:50 / 6:45]                       │││
│  │ │                                                           │││
│  │ │ [Settings] [Speed: 1x] [Captions: On] [Fullscreen]       │││
│  │ │ [Rewind 10s]  [Play]  [Skip 10s]                        │││
│  │ │                                                           │││
│  │ └──────────────────────────────────────────────────────────┘││
│  │                                                              ││
│  │ LESSON ACTIONS:                                              ││
│  │ [Bookmark This Lesson]  [Download Transcript]              ││
│  │ [Take Note]  [Mark as Complete]                            ││
│  │                                                              ││
│  │ NOTES & HIGHLIGHTS (My Notes):                              ││
│  │ ┌──────────────────────────────────────────────────────────┐││
│  │ │ [Jan 25, 1:30 PM] Trust is built through consistency... │││
│  │ │ [Jan 25, 1:45 PM] Key action: Weekly 1-1 meetings       │││
│  │ └──────────────────────────────────────────────────────────┘││
│  │                                                              ││
│  │ [+ Add Note]  [Highlight Text]  [Create Flashcard]         ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  ASSESSMENT (Module 4)                                           │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Quiz: Team Leadership Concepts (5 questions)                ││
│  │ Status: Available when videos complete                      ││
│  │ [Take Quiz]  [Review Quiz Guide]                            ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

#### 1. Course Header & Metadata
- **Course Information**
  - Course title
  - Provider, level, duration
  - Instructor name (link to instructor profile if available)
  - Enrollment date
  - Status (Enrolled, In Progress, Completed, Dropped, On Hold)

- **Quick Actions**
  - Back to catalog
  - Course completion certificate (when done)
  - Share certificate
  - Course support/help

#### 2. Progress Dashboard
- **Overall Progress**
  - Visual progress bar (% complete)
  - Hours completed and total hours
  - Status text: "X% complete (Y.Z of total hours)"

- **Timeline Information**
  - Enrollment date
  - Expected completion date
  - Time remaining
  - Time spent to date

- **Pace & Predictions**
  - Current pace (hours/week)
  - On track/behind/ahead status
  - Predicted completion date
  - Recommendation to adjust pace if needed

- **Learning Objectives Progress**
  - List of learning objectives
  - Checkmark when module/assessment related to objective completes
  - Visual progress across objectives

#### 3. Module Navigation
- **Module List**
  - Completed modules (checkmark)
  - Current module (highlight, play icon)
  - Locked modules (grayed out)
  - Module title, duration, completion status

- **Module Details Card**
  - Module number and title
  - Completion status
  - Completion date (if done)
  - Time spent / total time
  - Score (if graded assessment)
  - Prerequisite information (if module is locked)

- **Actions Per Module**
  - Completed: Review, View Certificate
  - In Progress: Continue, Bookmark, Restart
  - Not Started: Preview, Start

#### 4. Lesson / Content Player
- **Video Player**
  - Embedded video player
  - Video progress bar with scrubbing
  - Playback controls (play, pause, skip forward/backward)
  - Playback speed selector (0.5x, 1x, 1.5x, 2x)
  - Captions toggle (on/off) with caption language select
  - Fullscreen option
  - Resolution/quality selector (if applicable)
  - Volume control

- **Transcript & Captions**
  - Captions embedded in video
  - Downloadable transcript as PDF or text
  - Transcript searchable
  - Click caption to jump to time in video

- **Lesson Actions**
  - Bookmark lesson
  - Download transcript
  - Take notes (open note panel)
  - Mark as complete (manual completion)
  - Flag for review

#### 5. Note-Taking & Bookmarks
- **Note Panel**
  - Add note button
  - Note editor (text input)
  - Date/time of note
  - Link note to specific timestamp in video
  - Edit/delete notes
  - Search notes

- **Highlights**
  - Highlight text in transcripts
  - Create flashcards from highlights
  - Export highlights/flashcards

- **Bookmarks**
  - Bookmark lesson or timestamp
  - Return to bookmarked content
  - Quick access list of bookmarks

#### 6. Assessments & Quizzes
- **Quiz Access**
  - Available when prerequisite content complete
  - Quiz information (# questions, time limit, passing score)
  - "Take Quiz" button

- **Quiz Interface**
  - Questions presented one at a time (or all at once)
  - Question types: multiple choice, true/false, short answer, essay
  - Review before submit option
  - Countdown timer (if timed)
  - Flag question option

- **Quiz Results**
  - Score and percentage
  - Passing/failing status
  - Question review (which answered correctly/incorrectly)
  - Correct answers and explanations
  - Retake option (if allowed)

#### 7. Certificate & Completion
- **Completion Certificate**
  - Issued upon final module and assessment completion
  - Contains: Name, Course Title, Completion Date, Score
  - Digital certificate (downloadable PDF)
  - Shareable (social media, LinkedIn, email)
  - Verify link (external URL to verify certificate)

### Data Model

```
CourseEnrollment {
  id: UUID
  employee_id: UUID (FK to Employee)
  course_id: UUID (FK to Course)
  enrollment_date: Date
  status: Enum (ENROLLED, IN_PROGRESS, COMPLETED, DROPPED, ON_HOLD, SUSPENDED)
  progress_percentage: Decimal (0-100)
  completion_date: Date (nullable)
  final_score: Decimal (nullable)
  time_spent_minutes: Integer
  last_accessed: Timestamp
  assigned_by_manager_id: UUID (nullable)
  due_date: Date (nullable)
  is_mandatory: Boolean
  
  module_progress: Array<ModuleProgress {
    module_id: UUID
    status: Enum (NOT_STARTED, IN_PROGRESS, COMPLETED)
    completion_date: Date (nullable)
    time_spent_minutes: Integer
    score: Decimal (nullable)
    last_accessed: Timestamp
  }>
}

ModuleProgress {
  id: UUID
  enrollment_id: UUID (FK to CourseEnrollment)
  module_id: UUID (FK to CourseModule)
  status: Enum (NOT_STARTED, IN_PROGRESS, COMPLETED)
  progress_percentage: Decimal
  completion_date: Date (nullable)
  time_spent_minutes: Integer
  score: Decimal (nullable)
  last_accessed: Timestamp
}

LessonProgress {
  id: UUID
  enrollment_id: UUID (FK to CourseEnrollment)
  module_id: UUID (FK to CourseModule)
  lesson_id: UUID (FK to Lesson)
  status: Enum (NOT_STARTED, IN_PROGRESS, COMPLETED)
  completion_date: Date (nullable)
  time_watched_minutes: Integer (for videos)
  video_progress_percentage: Decimal (0-100)
  last_position_seconds: Integer (resume from this time)
  notes: Array<Note {
    id: UUID
    created_at: Timestamp
    updated_at: Timestamp
    text: String
    timestamp_seconds: Integer (nullable, for video lessons)
  }>
  bookmarked: Boolean
  bookmarked_timestamp_seconds: Integer (nullable)
}

Assessment {
  id: UUID
  module_id: UUID (FK to CourseModule)
  title: String
  description: String
  questions: Array<Question {
    id: UUID
    type: Enum (MULTIPLE_CHOICE, TRUE_FALSE, SHORT_ANSWER, ESSAY)
    question_text: String
    options: Array<String> (for multiple choice)
    correct_answer: String (for graded)
    explanation: String
  }>
  passing_score: Decimal (minimum % to pass)
  time_limit_minutes: Integer (nullable)
  is_graded: Boolean
  retake_allowed: Boolean
  retake_limit: Integer (nullable)
}

AssessmentAttempt {
  id: UUID
  enrollment_id: UUID (FK to CourseEnrollment)
  assessment_id: UUID (FK to Assessment)
  attempt_number: Integer
  started_at: Timestamp
  completed_at: Timestamp (nullable)
  score: Decimal (nullable)
  responses: Array<{
    question_id: UUID
    answer: String
    correct: Boolean (if graded)
  }>
}

CompletionCertificate {
  id: UUID
  enrollment_id: UUID (FK to CourseEnrollment)
  employee_id: UUID (FK to Employee)
  course_id: UUID (FK to Course)
  issued_date: Date
  expires_date: Date (nullable)
  certificate_number: String (unique)
  download_url: String
  share_url: String (unique, shareable link)
  verification_url: String (for verifying certificate)
}
```

### UI Components Required
- Progress bar with % indicator
- Video player (with player controls)
- Module list with collapse/expand
- Note editor / text input
- Assessment quiz component
- Quiz question renderer
- Results display
- Certificate preview/download
- Bookmark icon toggle
- Bookmark list sidebar

### WCAG 2.2 AA Accessibility Requirements

#### Color & Contrast
- Progress bar fill has 4.5:1 contrast with background
- Module status icons (completed, in progress) have text labels
- Quiz scoring colors (pass/fail) have text labels, not color alone
- Video player controls have 4.5:1 contrast
- Completion date and times readable at 4.5:1

#### Keyboard Navigation
- Tab through module list
- Arrow keys navigate modules
- Enter to select module
- Video player keyboard controls:
  - Space or Enter to play/pause
  - Arrow keys (← → ) to rewind/forward 10 seconds
  - M to mute
  - F for fullscreen
  - C for captions toggle
  - Numbers 0-9 to jump to % of video
- Tab through lesson actions
- Enter to take note, bookmark, complete lesson
- Quiz form all keyboard operable
- Skip links to jump to main content

#### Screen Reader Support
- Page title: "Advanced Project Management - Course Progress"
- Progress section: `<section aria-label="Course Progress" role="region">`
- Progress bar: `<div role="progressbar" aria-valuenow="55" aria-valuemin="0" aria-valuemax="100" aria-label="55% complete, 6.6 of 12 hours">●●●●●●○○○○</div>`
- Pace forecast: `<div aria-live="polite">On track to complete Feb 12, 2025</div>`
- Learning objectives: `<ul aria-label="Learning Objectives"><li><span aria-label="completed">✓</span> Define strategic...</li>`
- Module list: `<ol aria-label="Course Modules (4 of 6 completed)">`
- Current module: `<li aria-current="page">Module 4: Team Leadership & Dynamics</li>`
- Locked module: `<li aria-disabled="true">Module 5: Unlocks upon Module 4 completion</li>`
- Video player: `<div role="application" aria-label="Video player for Lesson 1: Building Trust. Use space to play/pause, arrow keys to seek.">`
- Video timestamp: `<div aria-live="polite" aria-label="Current time 1 minute 50 seconds out of 6 minutes 45 seconds">`
- Quiz question: `<fieldset><legend>Question 1 of 5: What is the first step?</legend><input type="radio" aria-label="Option A: ...">`
- Quiz score: `<div aria-label="Quiz complete. You scored 4 out of 5 questions correctly. Passing score: 3. Result: Passed" role="region">`

#### Focus Management
- Module list receives focus on page load
- When selecting module, focus moves to module content player
- When opening note editor, focus trapped in editor (close with Escape)
- After submitting quiz, focus moves to results summary
- Skip to main content link available

#### Touch & Target Size
- Module list items: 50px minimum height
- Play button (video): 44×44 px minimum
- Pause button: 44×44 px
- Rewind/Skip buttons: 44×44 px
- Fullscreen button: 44×44 px
- Caption toggle: 44×44 px
- Speed/Resolution buttons: 44×44 px
- Bookmark button: 44×44 px
- Complete lesson button: 44×44 px
- Quiz answer radio buttons: 44×44 px
- Take note button: 44×44 px

#### Error Handling & Validation
- Quiz answer incomplete: "Please answer all questions before submitting." (clear requirement)
- Assessment failed: "You scored 60%. Passing score is 75%. You have 2 retakes remaining." (explain next steps)
- Video loading error: "Video failed to load. Check your internet connection or try a different browser." (troubleshooting)
- Note save failed: "Your note couldn't be saved. Please try again." with retry button
- All errors have `role="alert"`

#### Motion & Animation
- Video playback smooth (respects reduced motion via browser setting)
- Progress bar animation respects `prefers-reduced-motion` (instant updates)
- Module transitions instant (no slide animation)
- Quiz results display instant (not animated)
- Module expand/collapse respects preference

#### Semantic HTML & ARIA
- Proper heading hierarchy: `<h1>` course title, `<h2>` Progress, Modules, etc.
- Module list as `<ol>` (ordered because sequence matters)
- Lesson as `<article>` within module
- Notes as `<ul>` with `<li>` for each note
- Quiz as `<form>` with `<fieldset>` for questions
- Answers as radio buttons or checkboxes with labels
- Video player as `<video>` or custom with `role="application"`

### AI Integration Points

#### 1. Adaptive Pacing
- **Recommended Pace**: "To complete on time, spend 1.5 hours/week. You're currently at 1.2 hours/week."
- **Pace Adjustment**: If falling behind, suggest acceleration options
- **Flexible Deadlines**: "Complete by Feb 28, or get notified if deadline approaches"

#### 2. Progress Predictions
- **Completion Forecast**: "At current pace, you'll complete Feb 12. Deadline is Feb 15."
- **Risk Alerts**: "You haven't accessed course in 7 days. You're 2 days behind schedule."
- **Smart Resumption**: When user returns, resume from exact point they left off

#### 3. Personalized Recommendations
- **Next Steps**: After module completion, suggest next module or complementary course
- **Quiz Preparation**: Before quiz, "You may want to review Lessons 2-3 (highest error topics)"
- **Learning Reinforcement**: "You scored 78% on this quiz. Take this 5-minute reinforcement activity?"

#### 4. Content Optimization
- **Transcript Summarization**: AI summarizes video transcripts into key takeaways
- **Note Suggestions**: AI suggests related concepts based on user notes
- **Flashcard Generation**: Auto-generate flashcards from highlighted content

#### 5. Support & Assistance
- **Chatbot for Questions**: AI chatbot answers course-specific questions
- **Performance Alerts**: If quiz performance low, suggest tutoring resources
- **Accessibility Assistance**: "Would you like extended captions, transcript downloads, or 1.5x speed permanently?"

### Integrations & Dependencies

#### Internal Integrations
- **Learning Management System**: Content hosting, progress tracking
- **Video Hosting**: Storage and streaming (YouTube, Vimeo, custom)
- **Notification System**: Progress reminders, deadline alerts
- **HRIS**: Employee data for certificate issuance
- **Career Development Plans**: Link course to career goals

#### External Integrations
- **LinkedIn**: Share certificate to LinkedIn profile
- **Calendar Systems**: Add course deadlines to calendar
- **Analytics Platforms**: Track engagement and completion

### Edge Cases & Error States

#### 1. Video Playback Issues
- **Network Issues**: "Your connection is slow. Video quality reduced to 480p. [Change Quality]"
- **Browser Incompatibility**: "Your browser doesn't support this video format. Use Chrome, Firefox, or Safari."
- **DRM/Access Issues**: "You don't have permission to access this content."

#### 2. Quiz Scenarios
- **Time Limit Expired**: "Your quiz time limit has expired. Submitting your current answers."
- **Question Failed**: Can retake if retakes allowed, else provide explanation
- **Essay Grading**: "Your essay answer will be graded by instructor. You'll be notified when graded."

#### 3. Module Prerequisites
- **Locked Module**: "Complete Module 4 first. Module 4 progress: 55% complete."
- **Skip Prerequisite Request**: Allow request to skip with manager approval

#### 4. Dropped Courses
- **Resume Dropped Course**: "This course was dropped on Jan 15. Resume course? Progress will be restored."
- **Permanent Deletion**: "Permanently delete this course from your record? This cannot be undone."

#### 5. Certificate Issues
- **Multiple Completions**: If course retaken, show latest certificate but keep prior certificates in history
- **Expired Certification**: If certification has expiration, alert when expiration approaches

### Success Metrics & Testing Scenarios

#### Progress Tracking
- [ ] Overall progress % calculates correctly
- [ ] Module progress updates when lessons complete
- [ ] Time spent tracks accurately
- [ ] Expected completion date forecasts correctly

#### Video Playback
- [ ] Video plays and pauses correctly
- [ ] Captions display (if available)
- [ ] Transcript downloads as PDF
- [ ] Resume from previous position works
- [ ] Speed adjustment works (0.5x-2x)
- [ ] Fullscreen works

#### Assessment & Scoring
- [ ] Quiz questions display correctly
- [ ] Quiz answers submit and grade
- [ ] Passing/failing status correct
- [ ] Retake functionality works (if enabled)
- [ ] Results show correct answers and explanations

#### Certificates
- [ ] Certificate issued upon course completion
- [ ] Certificate can be downloaded as PDF
- [ ] Certificate can be shared to LinkedIn
- [ ] Verification link works

#### Accessibility
- [ ] Video player keyboard controls work
- [ ] Quiz form keyboard navigable
- [ ] Screen reader announces progress
- [ ] Captions toggle works
- [ ] All content has text alternatives

---

## Screen 5.3: Learning Path

### Purpose
Enable employees to follow structured, goal-oriented learning sequences that combine multiple courses into cohesive skill development programs with milestone tracking, progress analytics, and peer benchmarking.

### User Personas
- **Primary**: All Employees (self-directed or manager-assigned)
- **Secondary**: Managers (assign paths to direct reports, track progress)

### Layout & Wireframe

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ←  Learning Path: Product Manager Master                       │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  PATH OVERVIEW                                                   │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Product Manager Master Track                                ││
│  │ Develop comprehensive PM skills from fundamentals to        ││
│  │ advanced strategy. Typical duration: 12 weeks               ││
│  │                                                              ││
│  │ Target Skills: Product Strategy, Data Analysis, Leadership,││
│  │               Communication, User Research                  ││
│  │                                                              ││
│  │ Milestones: 4                                                ││
│  │ Total Courses: 8                                              ││
│  │ Estimated Time: 48 hours                                     ││
│  │ Recommended for: Product Managers, Associate PMs             ││
│  │                                                              ││
│  │ Started: Jan 10, 2025  |  Expected Completion: Mar 28      ││
│  │ Path Status: In Progress                                     ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  PATH PROGRESS                                                   │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Overall Progress: ■■■■■■■░░░░  58% Complete (28 of 48 hrs)  ││
│  │                                                              ││
│  │ Courses Completed: 3 of 8                                    ││
│  │ Current Course: Data Analysis Fundamentals                  ││
│  │ Est. Completion: Mar 28, 2025 (49 days remaining)           ││
│  │                                                              ││
│  │ ┌──────────────────────────────────────────────────────────┐││
│  │ │ On Track to finish on time with 1.5 hr/week pace        │││
│  │ │ Peer Benchmark: You're ahead of 65% of learners in path │││
│  │ └──────────────────────────────────────────────────────────┘││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  MILESTONES & COURSES                                            │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Milestone 1: Product Management Fundamentals ✓ COMPLETED    ││
│  │ └─ ✓ Introduction to Product Management                     ││
│  │    Completed: Jan 15, 2025  |  Score: 92%                  ││
│  │ └─ ✓ User Research & Discovery                             ││
│  │    Completed: Jan 20, 2025  |  Score: 88%                  ││
│  │                                                              ││
│  │ Milestone 2: Core PM Skills (2 of 3 courses) 67% COMPLETE  ││
│  │ └─ ✓ Data Analysis for Product Managers                    ││
│  │    Completed: Feb 1, 2025  |  Score: 85%                   ││
│  │ └─ ► Data Analytics Advanced (in progress, 60% complete)   ││
│  │    Duration: 6 hours  |  Time Spent: 3.6 hours             ││
│  │    [Continue Course]                                         ││
│  │ └─ ○ A/B Testing & Experimentation                         ││
│  │    Status: Locked until Data Analytics Advanced complete   ││
│  │    Duration: 4 hours  |  [Preview]                         ││
│  │                                                              ││
│  │ Milestone 3: Advanced PM (Not Started)                      ││
│  │ └─ ○ Product Strategy & Roadmapping                         ││
│  │    Duration: 8 hours  |  Locked                            ││
│  │ └─ ○ Executive Communication for PMs                       ││
│  │    Duration: 3 hours  |  Locked                            ││
│  │                                                              ││
│  │ Milestone 4: PM Leadership (Not Started)                    ││
│  │ └─ ○ Building & Leading Product Teams                      ││
│  │    Duration: 6 hours  |  Locked                            ││
│  │ └─ ○ Stakeholder Management at Scale                       ││
│  │    Duration: 4 hours  |  Locked                            ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  PEER PROGRESS & ANALYTICS                                       │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Learners in this path: 47                                    ││
│  │ Average completion: 35% (13 completed)                       ││
│  │ Your standing: 58% complete (ahead of 65%)                  ││
│  │                                                              ││
│  │ Completion Timeline:                                         ││
│  │ Fastest: 6 weeks  |  Your pace: 8 weeks  |  Slowest: 14 wks││
│  │                                                              ││
│  │ Comparison chart showing your progress vs. peer average     ││
│  │                                                              ││
│  │ [View Leaderboard - Anonymized]                             ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  NEXT STEPS                                                      │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Your next milestone: Complete Data Analytics Advanced      ││
│  │ Recommendation: 2-3 hours/week to stay on track            ││
│  │ This unlocks: A/B Testing & Experimentation course         ││
│  │                                                              ││
│  │ [Continue Learning]  [Adjust Pace]  [Download Path Guide]  ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  ADDITIONAL RESOURCES                                            │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ [Download Learning Path Guide]                              ││
│  │ [Print Progress Certificate (Interim)]                      ││
│  │ [Share Path Achievement]                                    ││
│  │ [Related Learning Paths]                                    ││
│  │ [FAQ About this Path]                                       ││
│  │ [Instructor Office Hours] (Thurs 2-3 PM PT)                ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  FEEDBACK & SUPPORT                                              │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ [Share Feedback]  [Report Issue]  [Ask Instructor]         ││
│  │ [View Q&A Discussion]  [Join Study Group]                  ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

#### 1. Path Overview
- **Path Description**
  - Goal and learning outcomes
  - Target audience (roles, experience levels)
  - Typical duration
  - Target skills covered
  - Path difficulty level

- **Path Metadata**
  - Number of milestones
  - Total number of courses
  - Estimated total hours
  - Recommended for roles
  - Path start and expected completion dates
  - Current status (Not Started, In Progress, Completed)

#### 2. Path Progress Dashboard
- **Overall Progress Tracking**
  - Progress bar with % complete
  - Courses completed vs. total
  - Time spent vs. total
  - Expected completion date
  - Pacing assessment (On track, Behind, Ahead)

- **Milestone Breakdown**
  - Visual milestone markers (1, 2, 3, 4)
  - Milestone completion % (e.g., 67% complete)
  - Status indicators (Completed, In Progress, Locked)
  - Unlock criteria for locked milestones

#### 3. Course Sequencing
- **Milestone 1 (Fundamentals)**
  - 2-3 foundational courses
  - Build core knowledge
  - No prerequisites

- **Milestone 2 (Core Skills)**
  - Intermediate courses
  - Build on fundamentals
  - Prerequisites: Complete Milestone 1

- **Milestone 3 (Advanced)**
  - Advanced courses
  - Deep skill development
  - Prerequisites: Complete Milestone 2

- **Milestone 4 (Leadership/Specialization)**
  - Leadership or specialization courses
  - Prerequisites: Complete Milestone 3

#### 4. Course Details in Path
- **Per Course**
  - Course title and duration
  - Completion status
  - Score (if completed)
  - Time spent
  - [Continue], [Preview], or [Start] actions
  - Unlock status and criteria
  - Prerequisites shown

#### 5. Peer Benchmarking
- **Anonymized Peer Comparison**
  - Number of learners in path
  - Average completion %
  - User's percentile (e.g., "ahead of 65%")
  - Completion timeline comparison:
    - Fastest completion time
    - User's pace
    - Slowest completion time
  - Chart showing peer progress distribution

- **Leaderboard** (Optional, Anonymized)
  - Rank (1st, 2nd, 3rd, etc.)
  - Completion % only shown anonymized
  - Fastest completion time (anonymized)

#### 6. Analytics & Insights
- **Performance Metrics**
  - Average course score
  - Engagement trend (increasing/decreasing)
  - Time efficiency (hours/course)

- **Smart Recommendations**
  - "You're on track to complete by Mar 28"
  - "To stay on track, spend 2 hours/week on next course"
  - "Consider a study group (3 members in your org)"

#### 7. Certificates & Completion
- **Interim Certificates**
  - Milestone completion certificates
  - Download and share per milestone

- **Path Completion Certificate**
  - Issued upon completing all courses
  - Path title, duration, completion date
  - Skills verified
  - Shareable and verifiable

#### 8. Additional Resources
- **Path Guide Download**
  - PDF with full path details
  - Course sequence
  - Expected timeline
  - Study tips
  - Glossary of terms

- **Instructor Support**
  - Office hours schedule
  - Q&A discussion forum
  - Email instructor link

- **Study Groups**
  - Join existing study group
  - Create new study group
  - Collaboration tools

### Data Model

```
LearningPath {
  id: UUID
  title: String
  description: Text
  goal: String (learning outcome)
  
  target_roles: Array<String>
  target_audience_level: String
  difficulty_level: Enum (BEGINNER, INTERMEDIATE, ADVANCED, EXPERT)
  
  milestones: Array<Milestone {
    id: UUID
    order: Integer (1, 2, 3, 4)
    title: String
    description: String
    courses: Array<UUID> (course IDs in sequence)
    duration_hours: Integer (sum of course durations)
  }>
  
  total_courses: Integer
  total_duration_hours: Integer
  typical_duration_weeks: Integer
  
  skills_covered: Array<Skill {
    skill_id: UUID
    skill_name: String
    proficiency_level: String
  }>
  
  prerequisites: Array<UUID> (path IDs or course IDs)
  
  status: Enum (DRAFT, ACTIVE, ARCHIVED)
  created_by: UUID
  created_at: Timestamp
  updated_at: Timestamp
}

PathEnrollment {
  id: UUID
  employee_id: UUID (FK to Employee)
  path_id: UUID (FK to LearningPath)
  enrollment_date: Date
  status: Enum (ENROLLED, IN_PROGRESS, COMPLETED, DROPPED, ON_HOLD)
  progress_percentage: Decimal (0-100)
  completion_date: Date (nullable)
  
  milestone_progress: Array<MilestoneProgress {
    milestone_id: UUID
    status: Enum (NOT_STARTED, IN_PROGRESS, COMPLETED)
    progress_percentage: Decimal
    completion_date: Date (nullable)
    course_progress: Array<CourseEnrollment {
      course_id: UUID
      status: Enum (NOT_STARTED, IN_PROGRESS, COMPLETED)
      completion_date: Date (nullable)
      score: Decimal (nullable)
    }>
  }>
  
  total_time_spent_minutes: Integer
  expected_completion_date: Date
  assigned_by_manager_id: UUID (nullable)
  is_mandatory: Boolean
  
  created_at: Timestamp
  updated_at: Timestamp
}

MilestoneProgress {
  id: UUID
  path_enrollment_id: UUID (FK to PathEnrollment)
  milestone_id: UUID (FK to Milestone)
  status: Enum (NOT_STARTED, IN_PROGRESS, COMPLETED)
  progress_percentage: Decimal
  completion_date: Date (nullable)
  certificates_earned: Array<UUID>
}

PathCertificate {
  id: UUID
  path_enrollment_id: UUID (FK to PathEnrollment)
  employee_id: UUID (FK to Employee)
  path_id: UUID (FK to LearningPath)
  certification_type: Enum (MILESTONE, PATH_COMPLETION)
  milestone_id: UUID (nullable, if milestone cert)
  issued_date: Date
  download_url: String
  share_url: String
  verification_url: String
}
```

### UI Components Required
- Milestone timeline component
- Progress bar with % complete
- Course card within path (simplified)
- Peer comparison chart
- Leaderboard (anonymized)
- Certificate preview/download
- Study group finder
- Collapsible milestone sections

### WCAG 2.2 AA Accessibility Requirements

#### Color & Contrast
- Milestone status (Completed, In Progress, Locked) have text labels + color
- Progress bar fill has 4.5:1 contrast
- Percentile ranking text readable at 4.5:1
- Course status badges have text labels
- Chart data has color + pattern differentiation

#### Keyboard Navigation
- Tab through milestone sections
- Arrow keys to expand/collapse milestones (or Enter/Space)
- Tab through courses within milestone
- Enter to start course or view details
- Skip links to jump to sections
- Peer comparison chart keyboard navigable

#### Screen Reader Support
- Page title: "Learning Path: Product Manager Master"
- Path overview: `<section aria-label="Path Overview">`
- Progress section: `<section aria-label="Learning Path Progress" role="region">`
- Progress bar: `<div role="progressbar" aria-valuenow="58" aria-valuemin="0" aria-valuemax="100" aria-label="58% complete, 28 of 48 hours">`
- Pacing status: `<div aria-live="polite">On track to complete Mar 28, 2025</div>`
- Milestone list: `<ol aria-label="4 Milestones"><li><span aria-label="completed">✓</span> Milestone 1: Product Management Fundamentals</li>`
- Locked milestone: `<li aria-disabled="true">Milestone 3: Advanced PM, locked until Milestone 2 complete</li>`
- Course within milestone: `<ol aria-label="2 courses"><li>Course title, status: completed, score: 92%</li>...`
- Peer benchmarking: `<section aria-label="Peer Progress: 47 learners, you're in 65th percentile">`
- Leaderboard table: `<table aria-label="Anonymous Leaderboard"><thead><tr><th>Rank</th><th>Completion %</th></tr></thead>...`

#### Focus Management
- Milestone 1 receives focus on page load
- When expanding milestone, focus moves to first course in milestone
- When starting course, focus moves to course enrollment modal or new page
- Skip links available for navigation

#### Touch & Target Size
- Milestone expand/collapse buttons: 44×44 px minimum
- Course action buttons (Continue, Preview, Start): 44×44 px
- "Continue Learning" button: 44×44 px
- Download/Print buttons: 44×44 px
- Milestone cards: 50px minimum height

#### Error Handling & Validation
- Course not available: "This course is temporarily unavailable. Try again later." with retry option
- Path locked: "Complete Milestone 2 to unlock Milestone 3. You're 1 course away."
- Completion criteria not met: "Complete 'A/B Testing' to unlock next milestone." (clear requirement)
- All errors have `role="alert"`

#### Motion & Animation
- Milestone expand/collapse respects `prefers-reduced-motion` (instant)
- Progress bar animation respects preference (instant update)
- Chart transitions instant (no animation)
- Transitions between milestones instant

#### Semantic HTML & ARIA
- Proper heading hierarchy: `<h1>` Path, `<h2>` Milestones, `<h3>` Courses
- Milestones as `<ol>` (ordered, sequential)
- Courses within milestone as `<ol>`
- Expandable milestone as `<details>`/`<summary>`
- Progress bar as `<div role="progressbar">`
- Chart as `<table>` with headers

### AI Integration Points

#### 1. Personalized Path Recommendations
- **Role-Based**: "Based on your Product Manager role, recommend Product Manager Master path"
- **Skill Gap**: "You have strong data skills but weaker on strategy. This path fills that gap."
- **Career Progression**: "To advance to Senior PM, this path prepares you in 12 weeks"

#### 2. Adaptive Sequencing
- **Learning Style Detection**: Based on quiz performance and completion style, adjust course order
- **Difficulty Adjustment**: "You excelled in Module 1. Skip Beginner courses and jump to Intermediate?"
- **Pacing Optimization**: "Slow down—your completion rate suggests you may be rushing. Spend 3 hours on next course?"

#### 3. Progress Prediction & Alerts
- **Completion Forecast**: "At current pace (2 hrs/week), you'll finish Mar 28. Deadline is Mar 31."
- **Risk Alerts**: "You haven't logged in for 7 days. You're 3 days behind pace."
- **Catch-Up Suggestions**: "Complete 'Data Analytics Advanced' this week to stay on track"

#### 4. Peer Insights
- **Benchmarking**: "You're 65th percentile—faster than most peers. Keep it up!"
- **Study Groups**: "3 other learners in your org are on same path. Join study group?"
- **Collaboration**: "Sarah Chen from your team completed Milestone 2 yesterday. Ask her for tips?"

#### 5. Skill Validation
- **Competency Check**: Upon path completion, verify skills with assessment
- **Certification Recommendation**: "You completed Product Manager path. Ready for PMC (Product Manager Certification)?"
- **Continuous Learning**: "Post-path recommendations for deepening skills or new paths"

### Integrations & Dependencies

#### Internal Integrations
- **Learning Management System**: Course hosting, progress tracking
- **Performance Management**: Goals and development plans
- **HRIS**: Employee role for path recommendations
- **Notification System**: Progress reminders, milestone achievements
- **Study Group Platform**: Collaboration and peer connection

#### External Integrations
- **Analytics**: Track path completion rates, effectiveness
- **Calendar**: Add path milestones and deadlines to calendar

### Edge Cases & Error States

#### 1. Prerequisite Management
- **Skip Prerequisite**: Request to skip milestone with manager approval
- **Completion Verification**: Some paths require verified completion before unlocking

#### 2. Pace Adjustments
- **Acceleration**: User wants to complete faster than typical 12 weeks
- **Extended Timeline**: Extend path due date if on hold or life circumstances

#### 3. Path Updates
- **Course Changes**: If course in path updated, notify enrolled learners
- **Path Archival**: If path discontinued, notify learners and suggest alternative path

### Success Metrics & Testing Scenarios

#### Path Progress
- [ ] Overall progress % calculates correctly
- [ ] Milestone status shows accurate progress
- [ ] Expected completion date accurate
- [ ] Pacing assessment correct (on track/behind/ahead)

#### Course Sequencing
- [ ] Courses unlock in correct sequence
- [ ] Prerequisites enforced correctly
- [ ] Locked courses show unlock criteria clearly

#### Peer Benchmarking
- [ ] Peer percentile calculation correct
- [ ] Leaderboard anonymized (no names)
- [ ] Completion time comparison accurate

#### Certificates
- [ ] Milestone certificates issue correctly
- [ ] Path completion certificate issued upon finish
- [ ] Certificates downloadable and shareable

#### Accessibility
- [ ] Milestone sections keyboard navigable
- [ ] Course cards focusable
- [ ] Screen reader announces progress and status
- [ ] Chart data accessible via table alt

---

## Screen 5.4: Skills & Certifications

### Purpose
Enable employees to track, validate, and develop professional skills with self-assessments, peer endorsements, certification tracking, skill-to-role mapping, and gap analysis driving personalized learning recommendations.

### User Personas
- **Primary**: All Employees
- **Secondary**: Managers (view direct reports' skills), HR (skill mapping, gap analysis)

### Layout & Wireframe

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ←  Skills & Certifications          [Endorsements]  [Gaps]     │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  MY SKILLS PROFILE                                               │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Skills Inventory: 24 skills  |  Certifications: 5            ││
│  │ Endorsed Skills: 12          |  Pending Endorsements: 3     ││
│  │ Role-Required Skills: 8      |  Mastered: 6 (75%)          ││
│  │                                                              ││
│  │ Skill Strength: ████████████████░░░  75% (Strong)          ││
│  │ Skill Diversity: ██████████░░░░░░░░░░ 65% (Moderate)       ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  FEATURED SKILLS (Top 5 by role relevance)                       │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ 1. Product Management                                       ││
│  │    Level: Advanced  |  Endorsed by: 8 people               ││
│  │    Years of Experience: 4 years                              ││
│  │    [Endorsed by: Sarah Chen, John Smith, Mike Davis, +5]   ││
│  │    [Request Endorsement]  [Develop Further]  [Remove]       ││
│  │                                                              ││
│  │ 2. Data Analysis                                            ││
│  │    Level: Intermediate  |  Endorsed by: 5 people           ││
│  │    Years of Experience: 2 years                              ││
│  │    [Endorsed by: Jane Doe, Alex Johnson, +3]               ││
│  │    [Request Endorsement]  [Develop Further]  [Remove]       ││
│  │                                                              ││
│  │ 3. SQL & Database Management                                ││
│  │    Level: Intermediate  |  Endorsed by: 3 people           ││
│  │    [Request Endorsement]  [Develop Further]  [Remove]       ││
│  │                                                              ││
│  │ 4. User Research & Discovery                                ││
│  │    Level: Advanced  |  Endorsed by: 6 people               ││
│  │    [Request Endorsement]  [Develop Further]  [Remove]       ││
│  │                                                              ││
│  │ 5. Agile & Scrum                                            ││
│  │    Level: Intermediate  |  Endorsed by: 4 people           ││
│  │    [Request Endorsement]  [Develop Further]  [Remove]       ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  ALL SKILLS (24 total)                                           │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ [Sort: Endorsements ▼]  [Filter: Level ▼]                  ││
│  │                                                              ││
│  │ 6.  Project Management          Intermediate  Endorsed: 5  ││
│  │ 7.  Customer Communication      Advanced      Endorsed: 7  ││
│  │ 8.  Google Analytics            Beginner      Endorsed: 2  ││
│  │ 9.  Microsoft Excel             Advanced      Endorsed: 9  ││
│  │ 10. Presentations                Advanced      Endorsed: 8  ││
│  │ ...                                                          ││
│  │ [Show More Skills]                                           ││
│  │                                                              ││
│  │ [+ Add Skill]  [Import Skills from LinkedIn]                ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  CERTIFICATIONS & LICENSES (5 active)                            │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ ✓ PMP (Project Management Professional)                    ││
│  │   Issued: Mar 15, 2022  |  Expires: Mar 14, 2025           ││
│  │   License #: PMC-12345  |  Issuer: PMI                     ││
│  │   Status: Valid (expires in ~1 year)                        ││
│  │   [View Certificate]  [Verify]  [Renew]  [Share]           ││
│  │                                                              ││
│  │ ✓ AWS Certified Solutions Architect - Associate            ││
│  │   Issued: Jul 8, 2023  |  Expires: Jul 8, 2026             ││
│  │   License #: AWS-SA-789  |  Issuer: Amazon Web Services    ││
│  │   Status: Valid (2 years remaining)                         ││
│  │   [View Certificate]  [Verify]  [Renew]  [Share]           ││
│  │                                                              ││
│  │ ⚠ First Aid/CPR Certification                               ││
│  │   Issued: Jan 15, 2022  |  Expires: Feb 1, 2025            ││
│  │   Status: EXPIRING SOON (24 days remaining)                ││
│  │   [View Certificate]  [Verify]  [Renew Now]  [Share]       ││
│  │                                                              ││
│  │ ✓ SCRUM Master Certified                                   ││
│  │   Issued: Jun 10, 2023  |  Expires: Jun 10, 2026           ││
│  │   License #: CSM-456  |  Issuer: Scrum Alliance            ││
│  │   [View Certificate]  [Verify]  [Renew]  [Share]           ││
│  │                                                              ││
│  │ ○ Google Analytics 4 Certification (In Progress)            ││
│  │   Status: Exam scheduled for Feb 15, 2025                   ││
│  │   [View Details]  [Prepare]  [Reschedule]                  ││
│  │                                                              ││
│  │ [+ Add New Certification]  [Request Reimbursement]         ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  SKILL GAPS & RECOMMENDATIONS                                    │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Based on your PM role, you may benefit from:                ││
│  │                                                              ││
│  │ ▲ Data Visualization (recommended skill gap)                ││
│  │   Importance: High  |  Current Level: Beginner              ││
│  │   Career Impact: 8/10  |  Recommended Course: Tableau 101   ││
│  │   [Enroll in Tableau 101]  [Learn More]  [Dismiss]         ││
│  │                                                              ││
│  │ ▲ Executive Communication (skill gap)                       ││
│  │   Importance: High  |  Current Level: Intermediate          ││
│  │   Career Impact: 7/10  |  Recommended Course: Exec Comm...  ││
│  │   [Enroll in Course]  [Learn More]  [Dismiss]              ││
│  │                                                              ││
│  │ ▲ Advanced Statistics (optional skill gap)                  ││
│  │   Importance: Medium  |  Current Level: Beginner            ││
│  │   [Enroll in Course]  [Learn More]  [Dismiss]              ││
│  │                                                              ││
│  │ [View All Recommendations]  [Edit Profile]                  ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  REQUEST SKILL ENDORSEMENTS                                      │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Pending Endorsement Requests: 3                              ││
│  │                                                              ││
│  │ □ Product Strategy (requested from 5 people, 1 approved)   ││
│  │ □ Customer Insights (requested from 3 people, 0 approved)  ││
│  │ □ Data Modeling (requested from 4 people, 1 approved)      ││
│  │                                                              ││
│  │ [Request Endorsement from Colleague]                        ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  SKILL ASSESSMENTS (Optional)                                    │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Validate skills with assessments:                            ││
│  │                                                              ││
│  │ ○ SQL & Database Management Assessment                      ││
│  │   (10 min, intermediate level)  [Take Assessment]           ││
│  │                                                              ││
│  │ ○ Data Analysis Skills Assessment                           ││
│  │   (15 min, intermediate level)  [Take Assessment]           ││
│  │                                                              ││
│  │ ○ Product Management Competency                             ││
│  │   (20 min, advanced level)  [Take Assessment]               ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  CAREER DEVELOPMENT PLAN                                         │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Based on your skills and goals:                              ││
│  │ [View My Development Plan]                                  ││
│  │ [Create New Development Plan]                               ││
│  │ [Manager Conversation]                                      ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

#### 1. Skills Inventory
- **Skills List Display**
  - Skill name, proficiency level (Beginner, Intermediate, Advanced, Expert)
  - Years of experience (optional)
  - Number of endorsements
  - Last updated date
  - Skill category/tags

- **Add Skill**
  - Text input with autocomplete suggestions
  - Proficiency level selector
  - Years of experience input
  - Visibility settings (private, manager-only, public)
  - Category assignment

- **Edit/Update Skill**
  - Modify proficiency level
  - Update years of experience
  - Change visibility
  - Remove skill

#### 2. Endorsements
- **View Endorsements**
  - List of people who endorsed the skill
  - Their name, photo, title, department
  - Date of endorsement
  - Option to accept or hide endorsement

- **Request Endorsements**
  - Select colleagues to request endorsement from
  - Personal message (optional)
  - Track pending requests
  - Notification sent to requested colleagues

- **Endorse Others**
  - View colleagues' skills
  - One-click endorsement
  - Optional message to endorsee

- **Endorsement Privacy**
  - Option to make endorsements public or private
  - Hide negative or unwanted endorsements (removed from public view)
  - Anonymous endorsement option (if enabled)

#### 3. Certifications & Licenses
- **Certification Card**
  - Certification name
  - Issue and expiration dates
  - License number / credential ID
  - Issuing organization
  - Status: Valid, Expiring Soon, Expired, In Progress
  - Verification link (if available)

- **Certification Actions**
  - View/Download certificate
  - Share certificate
  - Verify credentials (external link)
  - Renew certification
  - Remove certification from profile
  - Set renewal reminders

- **Add Certification**
  - Certification name (autocomplete from common certs)
  - Issue date
  - Expiration date (optional)
  - License number
  - Upload certificate image/file
  - Verification URL

#### 4. Skill-to-Role Mapping
- **Role Requirements**
  - Current role listed (e.g., "Product Manager")
  - Required skills for role (8 skills)
  - Recommended skills (5-10 additional)
  - Percentage of required skills mastered

- **Skills Mastery**
  - Visual indicator of role-required skills completed
  - Missing skills flagged
  - Mastery level shown as % (e.g., 75% of required skills at Advanced level)

#### 5. Skill Gaps & Recommendations
- **Gap Analysis**
  - Skills needed for current role but missing/weak
  - Skills needed for target role (if specified)
  - Priority ranking (High, Medium, Low importance)
  - Career impact score (1-10 scale)

- **Learning Recommendations**
  - Recommended course/path to fill gap
  - Time to complete
  - [Enroll] button
  - Dismiss recommendation (option)

#### 6. Skill Assessments
- **Self-Assessment**
  - Quiz to validate claimed skill level
  - 5-10 questions per skill
  - Takes 5-15 minutes
  - Score determines proficiency level (Beginner → Expert)
  - Results can update skill profile

- **Assessment History**
  - Track assessments taken
  - Scores and dates
  - Retake after 6 months (to show progress)

#### 7. Career Development Integration
- **Link to Development Plans**
  - Skills needed for promotion/role change
  - Skills required for career goal
  - Development plan showing skill targets

### Data Model

```
SkillProfile {
  id: UUID
  employee_id: UUID (FK to Employee)
  
  skills: Array<EmployeeSkill {
    id: UUID
    skill_id: UUID (FK to Skill)
    skill_name: String
    proficiency_level: Enum (BEGINNER, INTERMEDIATE, ADVANCED, EXPERT)
    years_of_experience: Integer (nullable)
    verified: Boolean (through assessment or endorsement)
    endorsement_count: Integer
    endorsements: Array<Endorsement {
      endorser_id: UUID
      endorser_name: String
      endorsed_date: Date
      is_public: Boolean
    }>
    added_date: Date
    last_updated: Date
    visibility: Enum (PRIVATE, MANAGER_ONLY, PUBLIC)
  }>
  
  certifications: Array<Certification {
    id: UUID
    certification_name: String
    issuing_organization: String
    license_number: String (nullable)
    issue_date: Date
    expiration_date: Date (nullable)
    certificate_url: String (cloud storage URL)
    verification_url: String (nullable, external verification link)
    status: Enum (VALID, EXPIRING_SOON, EXPIRED, IN_PROGRESS)
    renewal_date: Date (nullable)
    credential_on_profile: Boolean
  }>
  
  role_id: UUID (FK to Role)
  current_role: String
  target_role_id: UUID (nullable, for aspirational roles)
  
  created_at: Timestamp
  updated_at: Timestamp
}

Skill {
  id: UUID
  name: String
  category: String (Leadership, Technical, Sales, etc.)
  description: String (nullable)
  proficiency_levels: Array<String> (BEGINNER, INTERMEDIATE, ADVANCED, EXPERT)
  role_mapping: Array<{ role_id: UUID, required: Boolean, recommended: Boolean }>
}

SkillEndorsement {
  id: UUID
  endorser_id: UUID (FK to Employee)
  endorsee_id: UUID (FK to Employee)
  skill_id: UUID (FK to Skill)
  endorsement_date: Date
  is_public: Boolean
  created_at: Timestamp
}

SkillGap {
  id: UUID
  employee_id: UUID (FK to Employee)
  skill_id: UUID (FK to Skill)
  skill_name: String
  current_level: Enum (NONE, BEGINNER, INTERMEDIATE, ADVANCED, EXPERT)
  required_level: Enum (BEGINNER, INTERMEDIATE, ADVANCED, EXPERT)
  importance: Enum (HIGH, MEDIUM, LOW)
  reason: String (for current role, for promotion, etc.)
  career_impact_score: Integer (1-10)
  recommended_course_id: UUID (nullable)
  gap_identified_date: Date
}

SkillAssessment {
  id: UUID
  skill_id: UUID (FK to Skill)
  question_count: Integer
  duration_minutes: Integer
  difficulty_level: Enum (BEGINNER, INTERMEDIATE, ADVANCED)
  passing_score: Decimal
}

SkillAssessmentAttempt {
  id: UUID
  employee_id: UUID (FK to Employee)
  assessment_id: UUID (FK to SkillAssessment)
  attempt_date: Date
  score: Decimal
  proficiency_level_awarded: Enum (BEGINNER, INTERMEDIATE, ADVANCED, EXPERT)
  results_shared: Boolean
}

Certification {
  id: UUID
  name: String
  organization: String
  description: String (nullable)
  renewal_frequency_months: Integer (nullable)
  verification_url: String (nullable)
  associated_skill_id: UUID (nullable, FK to Skill)
}
```

### UI Components Required
- Skill card (with endorsement count)
- Endorsement badge/list
- Certification card (with status indicator)
- Skill assessment quiz component
- Gap analysis card
- Skill-to-role comparison chart
- Add skill form
- Endorsement request modal
- Certificate upload/preview

### WCAG 2.2 AA Accessibility Requirements

#### Color & Contrast
- Proficiency level badges (Beginner, Intermediate, etc.) have text labels + color
- Certification status (Valid, Expiring Soon, Expired) have text + color + icon
- Gap importance (High, Medium, Low) have text labels + color
- Endorsement count numbers readable at 4.5:1
- Career impact scores readable

#### Keyboard Navigation
- Tab through skills list
- Arrow keys navigate skills
- Enter to edit skill
- Tab through certifications
- Enter to view certificate details
- Endorsement buttons keyboard accessible
- Skill assessment quiz all keyboard operable
- Skip links for major sections

#### Screen Reader Support
- Page title: "Skills & Certifications"
- Skills section: `<section aria-label="My Skills (24 skills)">`
- Skill card: `<article aria-label="Product Management, Advanced level, endorsed by 8 people">`
- Endorsement badge: `<span aria-label="Endorsed by 8 people: Sarah Chen, John Smith, ...">8</span>`
- Proficiency level: `<span aria-label="Intermediate level">Intermediate</span>`
- Certification section: `<section aria-label="Certifications (5 active, 1 in progress)">`
- Cert status: `<span aria-label="Expires Feb 1, 2025 - expiring soon">⚠ Expires Feb 1</span>`
- Gap analysis: `<section aria-label="Skill Gaps (3 gaps detected)">`
- Gap priority: `<span aria-label="High importance">High</span>`
- Assessment: `<div aria-label="SQL Assessment, 10 minutes, intermediate level">Take Assessment</div>`

#### Focus Management
- Skills list receives focus on page load
- When editing skill, focus moves to form
- Form close returns focus to skill card
- Endorsement modal traps focus (Escape closes)
- Assessment quiz focus trapped
- Skip to main content link available

#### Touch & Target Size
- Skill cards: 50px minimum height
- Edit/Remove buttons on skill: 44×44 px
- Endorsement count button: 44×44 px minimum
- Request endorsement button: 44×44 px
- Certification action buttons (View, Share, Renew): 44×44 px each
- Assessment button: 44×44 px
- Add skill button: 44×44 px

#### Error Handling & Validation
- Duplicate skill: "You already have 'Product Management' in your profile." (with option to update level instead)
- Missing certification date: "Certification date required. Please enter issue date." (clear requirement)
- Invalid expiration date: "Expiration date cannot be in the past." (explain requirement)
- Assessment error: "Assessment couldn't load. Try again in a few minutes." with retry button
- All errors have `role="alert"`

#### Motion & Animation
- Skill expand/collapse respects `prefers-reduced-motion` (instant)
- Endorsement badge updates instant (not animated)
- Gap alert animations respect preference
- Assessment transitions instant

#### Semantic HTML & ARIA
- Proper heading hierarchy: `<h1>` page, `<h2>` Skills, Certifications, Gaps, etc.
- Skills list as `<ul>` with skill `<li>`
- Certifications list as `<ul>` with cert `<li>`
- Proficiency levels as `<span>` with aria-label
- Endorsement list as `<ul>` with endorser names
- Assessment as `<form>` with `<fieldset>` per question
- Gap list as `<ul>` with gap items

### AI Integration Points

#### 1. Skill Recommendations
- **Role-Based**: "For Senior PM role, you need: Advanced Data Analysis, Executive Communication, Strategic Thinking"
- **Skill Gap Detection**: "You're strong in Product Management but weak in Data Analysis. Recommend 2 courses."
- **Peer Benchmarking**: "Other PMs in your level have: Advanced in 5 skills, you're at 3. Consider developing X skill"

#### 2. Endorsement Intelligence
- **Smart Endorsement Requests**: "Sarah Chen uses Data Analysis frequently. Ask her to endorse you?"
- **Endorsement Quality**: "You have 8 endorsements. Average is 6. Your profile is strong."
- **Reciprocal Endorsement**: "John Smith endorsed you for SQL. Consider endorsing him back?"

#### 3. Certification Tracking
- **Renewal Reminders**: "PMP expires Mar 14, 2025 (34 days). Start renewal process?"
- **Cost Optimization**: "AWS cert costs $150. Your company offers $500/year learning budget. Approve renewal?"
- **Trend Analysis**: "30% of your org has AWS cert. Consider it for career growth."

#### 4. Career Pathing
- **Skill Progression**: "Master 2 more Advanced skills to be ready for Senior PM in 6 months"
- **Learning Roadmap**: "To advance: 1) Data Visualization, 2) Strategic Communication, 3) Leadership"
- **Success Probability**: "You have 75% of skills needed for Principal PM. You're on track."

#### 5. Continuous Learning
- **Skill Decay Detection**: "You haven't updated your SQL skill in 18 months. Take refresher course?"
- **Industry Trends**: "Data Science is trending in product teams. Consider AI Fundamentals?"
- **Community Recommendations**: "Skills that are trending: Generative AI, Data Privacy, Distributed Systems"

### Integrations & Dependencies

#### Internal Integrations
- **HRIS Core**: Employee role, department, level
- **Learning Management System**: Recommended courses for gaps
- **Performance Management**: Skills related to performance goals
- **Career Development Plans**: Skills needed for target roles
- **Internal Directory**: Search colleagues for endorsements

#### External Integrations
- **LinkedIn**: Import skills from LinkedIn (if permission granted)
- **Certification Bodies**: Verify credentials (PMI, AWS, etc.)
- **Skills APIs**: Industry skill definitions and role mappings

### Edge Cases & Error States

#### 1. Duplicate Skills
- **Same Skill Multiple Entries**: Suggest merging instead of duplicates
- **Skill Name Variations**: "SQL" vs. "SQL Database" → suggest consolidation

#### 2. Endorsement Issues
- **Self-Endorsement**: Prevent self-endorsement (or mark as self-endorsed)
- **Spam Endorsements**: If person endorses many skills from different people rapidly, flag

#### 3. Expired Certifications
- **Continued Showing**: Expired certs removed from profile but kept in history
- **Renewal Failure**: If renewal attempt fails, remind user manually
- **Grace Periods**: Some certs have grace periods (e.g., 30 days after expiration)

#### 4. Skill Obsolescence
- **Deprecated Skills**: "Flash is no longer in demand. Consider removing from profile."
- **Skill Evolution**: "XML deprecated, replaced by JSON. Update skill?"

### Success Metrics & Testing Scenarios

#### Skill Management
- [ ] Skills add successfully
- [ ] Proficiency levels update correctly
- [ ] Skill edit/delete works
- [ ] Skills display in correct order (by endorsement, by role relevance)

#### Endorsements
- [ ] Endorsement requests send to correct colleagues
- [ ] Endorsement counts update immediately
- [ ] Endorser list displays correctly
- [ ] Private endorsements hidden from public profile

#### Certifications
- [ ] Certification expiration dates calculated correctly
- [ ] Expiring soon alerts trigger at right time
- [ ] Certificate verification links work
- [ ] Renewal reminders sent before expiration

#### Skill Gaps
- [ ] Gaps identified correctly based on role
- [ ] Gap recommendations accurate
- [ ] Importance ratings correct
- [ ] Career impact scores sensible

#### Accessibility
- [ ] Skills keyboard navigable
- [ ] Endorsement list screen reader accessible
- [ ] Certification status announced correctly
- [ ] Assessment quiz keyboard operable
- [ ] All status badges have text labels

---

## Screen 5.5: Learning Recommendations

### Purpose
Deliver personalized, AI-powered learning recommendations based on employee roles, skill gaps, career goals, performance feedback, and peer activity with the ability to accept, dismiss, and provide feedback on recommendation quality.

### User Personas
- **Primary**: All Employees
- **Secondary**: Managers (assign recommendations to direct reports)

### Layout & Wireframe

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                   │
│  ←  Learning Recommendations     [All]  [Dismiss]  [Preferences] │
│                                                                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  PERSONALIZED RECOMMENDATIONS FOR YOU                            │
│  Based on: Your Role (Product Manager) + Skills + Goals         │
│                                                                   │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ ① Advanced Data Analysis for Product Managers               ││
│  │   COURSE (6 hours)  |  Level: Intermediate                   ││
│  │   Provider: Acme Learning  |  ★★★★★ (234 reviews)           ││
│  │                                                              ││
│  │   Why Recommended: Fills skill gap in Data Analysis.         ││
│  │   Your current level: Beginner  |  Role req: Intermediate   ││
│  │   Career impact: +2 skill points toward Senior PM           ││
│  │                                                              ││
│  │   [Enroll]  [Save for Later]  [Not Interested]  [Details]  ││
│  │                                                              ││
│  ├─────────────────────────────────────────────────────────────┤│
│  │ ② Product Management Master Path                            ││
│  │   LEARNING PATH (8 courses, 48 hours)  |  Level: Advanced   ││
│  │   Milestones: 4  |  Typical duration: 12 weeks              ││
│  │                                                              ││
│  │   Why Recommended: Aligns with your career goal (Senior PM) ││
│  │   Skills covered: Strategy, Data, Leadership, Communication ││
│  │   Your goal timeline: 6 months  |  Path timeline: 12 weeks  ││
│  │   Completion benefit: Prepares you for promotion            ││
│  │                                                              ││
│  │   [Enroll in Path]  [Save for Later]  [Not Interested]      ││
│  │                                                              ││
│  ├─────────────────────────────────────────────────────────────┤│
│  │ ③ Executive Communication & Presence                        ││
│  │   COURSE (3 hours)  |  Level: Advanced                       ││
│  │   Provider: Executive Academy  |  ★★★★☆ (156 reviews)       ││
│  │                                                              ││
│  │   Why Recommended: Complements your PM skills. Strengthen   ││
│  │   executive communication, a key skill for senior roles.     ││
│  │   Related to goal: "Advance to Senior PM" (soft skills)     ││
│  │   15 PMs in your org completed this. Avg completion: 8 wks  ││
│  │                                                              ││
│  │   [Enroll]  [Save for Later]  [Not Interested]  [Details]  ││
│  │                                                              ││
│  ├─────────────────────────────────────────────────────────────┤│
│  │ ④ Generative AI for Product Leaders                         ││
│  │   COURSE (4 hours)  |  Level: Intermediate                   ││
│  │   Provider: Tech Institute  |  ★★★★★ (567 reviews)          ││
│  │                                                              ││
│  │   Why Recommended: Trending skill in product management.    ││
│  │   Recent update: 25% more product roles now require AI lit. ││
│  │   Trend score: High  |  Relevance to role: Strong           ││
│  │                                                              ││
│  │   [Enroll]  [Save for Later]  [Not Interested]  [Details]  ││
│  │                                                              ││
│  ├─────────────────────────────────────────────────────────────┤│
│  │ ⑤ Building and Leading Remote Teams                         ││
│  │   COURSE (6 hours)  |  Level: Advanced                       ││
│  │   Provider: Leadership Institute  |  ★★★★★ (312 reviews)    ││
│  │                                                              ││
│  │   Why Recommended: Based on feedback: "Strengthen team      ││
│  │   leadership skills" (from 360 review). This course         ││
│  │   addresses that development area directly.                 ││
│  │                                                              ││
│  │   [Enroll]  [Save for Later]  [Not Interested]  [Details]  ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  MANAGER RECOMMENDATIONS (from Sarah Chen)                       │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Sarah recommended: "SQL Fundamentals"                        ││
│  │ Reason: "Would help with data analysis for this project"   ││
│  │ Shared: Jan 15, 2025                                         ││
│  │                                                              ││
│  │ [View Course]  [Accept]  [Decline with Feedback]            ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  TRENDING IN YOUR INDUSTRY                                       │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ Growing Demand Skills:                                       ││
│  │ • Generative AI (trending +450% in 2024)                   ││
│  │ • Data Privacy & Ethics (+320%)                             ││
│  │ • Cloud Architecture (+280%)                                ││
│  │ • User Experience Design (+240%)                            ││
│  │                                                              ││
│  │ Courses trending in your company (other PMs enrolling):    ││
│  │ [See Trending Courses]                                      ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  SAVED FOR LATER (3 items)                                       │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ ☆ Mindfulness & Stress Management (5 hours)                 ││
│  │   [Enroll Now]  [View Details]  [Remove from Saved]         ││
│  │                                                              ││
│  │ ☆ Strategic Negotiation Skills (4 hours)                    ││
│  │   [Enroll Now]  [View Details]  [Remove from Saved]         ││
│  │                                                              ││
│  │ ☆ AI Fundamentals Bootcamp (20 hours)                      ││
│  │   [Enroll Now]  [View Details]  [Remove from Saved]         ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
│  DISMISSED RECOMMENDATIONS (8 hidden)  [View Dismissed]          │
│                                                                   │
│  RECOMMENDATION SETTINGS                                          │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │ [Edit Preferences]                                           ││
│  │ • Topics of Interest: [Leadership] [Technical] [Business]   ││
│  │ • Learning Styles: [Video] [Interactive] [Articles]         ││
│  │ • Frequency: Show me new recommendations [Weekly ▼]         ││
│  │ • Include trending skills: [Yes] [No]                       ││
│  │ • Include manager recommendations: [Yes] [No]               ││
│  │                                                              ││
│  └─────────────────────────────────────────────────────────────┘│
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

### Key Features & Workflows

#### 1. Personalized Recommendation Feed
- **Recommendation Cards**
  - Course/path title and type (Course, Path, Certification)
  - Duration and level
  - Provider name
  - Star rating and review count
  - Explanation of why recommended (1-2 sentences)
  - Career impact or skill improvement
  - Relevant peer statistics ("15 PMs completed", "25% of org trending toward this")

- **Recommendation Ranking**
  - Top 5-10 personalized recommendations first
  - Ranked by relevance to role, goals, and skill gaps
  - New recommendations appear at top
  - Refreshed weekly or on-demand

- **Recommendation Reasons**
  - "Fills skill gap in Data Analysis"
  - "Aligns with career goal: Senior PM"
  - "Based on 360 feedback: Strengthen team leadership"
  - "Trending skill in your industry (+450% demand)"
  - "Popular with team (4 colleagues completed)"

#### 2. Accept / Dismiss Workflow
- **Accept Recommendation**
  - "Enroll" button redirects to enrollment
  - "Save for Later" adds to saved list
  - Recommendation removed from feed

- **Dismiss Recommendation**
  - "Not Interested" hides recommendation
  - Feedback option: "Why not? [Select reason]"
  - System learns from dismissals
  - Option to undo dismissal

#### 3. Manager Recommendations
- **Manager-Assigned Courses**
  - Separate section for manager recommendations
  - Manager name and role
  - Recommendation text ("Would help with X project")
  - Date shared
  - [Accept], [Decline with Feedback] buttons

- **Optional vs. Required**
  - Indicator if required for job/compliance
  - Due date if applicable

#### 4. Trending & Popular
- **Industry Trends**
  - Trending skills in role/industry (with % growth)
  - Market data on skill demand
  - Time-sensitive opportunities

- **Company Trends**
  - Courses other employees in company are taking
  - Trending in your team
  - Trending among peer roles

#### 5. Saved for Later
- **Saved List**
  - Bookmarked recommendations
  - Quick enroll button
  - Removal option
  - Clear indication of why saved (if applicable)

#### 6. Dismissed Recommendations
- **Hidden List**
  - View dismissed recommendations
  - Reason for dismissal (shown for transparency)
  - Option to reconsider and restore

#### 7. Preferences & Settings
- **Customize Recommendations**
  - Topics of interest (Leadership, Technical, Business, etc.)
  - Learning styles (Video, Interactive, Reading)
  - Frequency (Weekly, Bi-weekly, Monthly)
  - Include trending skills? (toggle)
  - Include manager recommendations? (toggle)
  - Include peer activity? (toggle)

- **Notification Preferences**
  - Email when new recommendations added
  - Frequency of recommendation emails
  - Digest format (top 5 weekly, daily alerts, etc.)

### Data Model

```
LearningRecommendation {
  id: UUID
  employee_id: UUID (FK to Employee)
  recommended_content_id: UUID (FK to Course or LearningPath)
  content_type: Enum (COURSE, PATH, CERTIFICATION)
  
  recommendation_reason: Enum (SKILL_GAP, ROLE_REQUIRED, CAREER_GOAL, TRENDING, PEER_ACTIVITY, FEEDBACK, MANAGER_ASSIGNED)
  reason_description: String (explanation shown to user)
  
  relevance_score: Decimal (0-100, used for ranking)
  relevance_factors: {
    skill_gap_alignment: Decimal (0-100)
    role_alignment: Decimal (0-100)
    goal_alignment: Decimal (0-100)
    trending_score: Decimal (0-100)
    peer_popularity: Decimal (0-100)
    career_impact_score: Integer (1-10)
  }
  
  status: Enum (ACTIVE, SAVED, DISMISSED, ENROLLED, COMPLETED)
  
  dismissed_date: Date (nullable)
  dismissed_reason: String (nullable, why user dismissed)
  dismissed_feedback: String (nullable)
  
  manager_id: UUID (nullable, if manager-assigned)
  manager_assigned_date: Date (nullable)
  manager_reason: String (nullable)
  is_mandatory: Boolean
  due_date: Date (nullable)
  
  created_at: Timestamp
  updated_at: Timestamp
}

RecommendationPreference {
  id: UUID
  employee_id: UUID (FK to Employee)
  
  topics_of_interest: Array<String>
  learning_styles: Array<String> (VIDEO, INTERACTIVE, READING, LIVE_SESSION)
  recommendation_frequency: Enum (WEEKLY, BI_WEEKLY, MONTHLY, ON_DEMAND)
  
  include_trending_skills: Boolean
  include_manager_recommendations: Boolean
  include_peer_activity: Boolean
  include_certifications: Boolean
  
  notification_preference: Enum (EMAIL_DIGEST, DAILY_ALERT, WEEKLY_DIGEST, NONE)
  notification_frequency: String (e.g., "Thursday 9 AM PT")
  
  max_recommendations_per_week: Integer
  
  created_at: Timestamp
  updated_at: Timestamp
}

TrendingSkill {
  id: UUID
  skill_name: String
  industry: String
  yoy_growth_percentage: Decimal
  months_of_trend: Integer
  relevant_roles: Array<String>
  related_courses: Array<UUID>
}
```

### UI Components Required
- Recommendation card (with reason, rating, actions)
- Manager recommendation section
- Trending skills carousel or list
- Saved list
- Dismissed list
- Preference form (checkboxes, toggles)
- Trending skill badge
- Peer activity indicator
- Career impact visualizer

### WCAG 2.2 AA Accessibility Requirements

#### Color & Contrast
- Recommendation reason text readable at 4.5:1
- Star ratings have text equivalents
- Trending badges have text labels
- Skill growth percentages readable
- Preference toggles have text labels (not toggle alone)

#### Keyboard Navigation
- Tab through recommendation cards
- Arrow keys navigate recommendations
- Enter to enroll/save/dismiss
- Preference form fully keyboard operable
- Skip links for sections

#### Screen Reader Support
- Page title: "Learning Recommendations"
- Recommendation section: `<section aria-label="Personalized Recommendations (5 for you)">`
- Recommendation card: `<article aria-label="Advanced Data Analysis, 6-hour course, 4.5 stars, recommended because it fills your data analysis skill gap">`
- Recommendation reason: `<div aria-label="Why recommended: Fills skill gap in Data Analysis. Current: Beginner, Role requires: Intermediate">`
- Trending indicator: `<span aria-label="Trending: +450% demand growth">`
- Manager recommendation: `<section aria-label="Recommendation from Sarah Chen (Manager): SQL Fundamentals, shared Jan 15">`
- Saved list: `<section aria-label="Saved For Later (3 items)">`
- Preference: `<label><input type="checkbox" aria-label="Include trending skills in recommendations"> Include trending skills</label>`

#### Focus Management
- Recommendation feed receives focus on page load
- When dismissing, focus returns to card position (or next recommendation)
- Preference form focus trapped (close/save returns focus to trigger)
- Skip to recommendations link available

#### Touch & Target Size
- Recommendation cards: 60px minimum height
- Enroll/Save/Dismiss buttons: 44×44 px
- Trending badge: 40px height
- Preference checkboxes: 44×44 px target
- Preference form inputs: 40px min height

#### Error Handling & Validation
- No recommendations available: "No recommendations at this time. Complete more courses or update your preferences." (helpful, not error)
- Preference save failed: "Preferences couldn't be saved. Try again." with retry button
- Manager recommendation error: "Couldn't load manager recommendation. Refresh page." with retry
- All errors have `role="alert"`

#### Motion & Animation
- Card transitions respect `prefers-reduced-motion` (instant, no animation)
- Preference changes instant (no animation)
- Trending indicator pulse (if used) respects preference

#### Semantic HTML & ARIA
- Proper heading hierarchy: `<h1>` page, `<h2>` sections (Personalized, Manager, Trending, Saved, Dismissed)
- Recommendations as `<ul>` with recommendation `<li>`/`<article>`
- Trending list as `<ul>`
- Preference form as `<form>` with `<fieldset>` per section
- Checkboxes/toggles with associated `<label>` tags
- Rating as structured data: `<span aria-label="4.5 out of 5 stars">`

### AI Integration Points

#### 1. Intelligent Recommendation Engine
- **Multi-Factor Ranking**: Combine skill gaps, role requirements, goals, trends, peer activity
- **Collaborative Filtering**: "People who completed X also liked Y"
- **Content-Based Filtering**: "Courses similar to ones you completed, at next level"

#### 2. Trend Detection & Prediction
- **Emerging Skills**: "Generative AI is trending +450% in product roles. Get ahead of curve."
- **Role Evolution**: "Product roles increasingly require AI/ML knowledge. Future-proof skills."
- **Market Signals**: Track LinkedIn, job postings for skill demand shifts

#### 3. Goal-Based Recommendations
- **Career Path**: "To reach Senior PM in 12 months, complete: Data Analysis, Strategy, Leadership"
- **Promotion Readiness**: "You're missing 1 skill for promotion: Executive Communication"
- **Lateral Move**: "Interested in switching to Analytics role? Start with: Statistics, SQL, Tableau"

#### 4. Feedback Loop Learning
- **Dismissal Learning**: "You dismissed 3 sales courses. Not interested in sales skills?"
- **Engagement Learning**: "You completed 5 video courses but started 0 articles. Recommend more videos?"
- **Time Commitment Learning**: "You prefer short courses (< 4 hours). Recommend micro-courses?"

#### 5. Peer Influence & Social Learning
- **Peer Success Stories**: "15 PMs in your org completed this. Average rating: 4.8 stars."
- **Study Groups**: "3 colleagues enrolled this week. Join study group together?"
- **Manager Insights**: "Your manager mentioned you need data skills. Recommend courses?"

### Integrations & Dependencies

#### Internal Integrations
- **HRIS Core**: Employee role, level, department for recommendations
- **Performance Management**: Recent feedback and development goals
- **Learning Management System**: Completed courses, progress, assessments
- **Career Development Plans**: Target roles, career goals
- **Skills Inventory**: Current skills and gaps
- **Notification System**: Email digests, alerts

#### External Integrations
- **Trending Data APIs**: Skill demand data (LinkedIn, job posting APIs)
- **Content Providers**: Course catalogs for recommendations
- **Collaboration Tools**: Study group notifications (Slack, Teams)

### Edge Cases & Error States

#### 1. Cold Start Problem
- **New Employees**: Limited data, recommend based on role only
- **Employees with no goals**: Recommend based on role and peer activity
- **Employees with no history**: Generic role-based recommendations

#### 2. Stale Recommendations
- **Completed Content**: Don't recommend courses user completed
- **Changed Role**: Update recommendations when role changes
- **Archived Content**: Remove if recommended course archived/unavailable

#### 3. Overloaded Recommendations
- **Too Many**: If >20 recommendations, apply stricter filtering
- **User Preference**: Max recommendations setting respected
- **Fatigue**: If user dismisses many, ease up frequency

#### 4. Recommendation Conflicts
- **Conflicting Goals**: "Your goal is PM, but your skill gap is in Engineering. Which to prioritize?"
- **Time Constraints**: "This learning path takes 12 weeks, but you requested completion in 8 weeks."

### Success Metrics & Testing Scenarios

#### Recommendation Quality
- [ ] Recommendations relevant to role and skills
- [ ] Skill gap recommendations actually fill gaps
- [ ] Career goal recommendations support target role
- [ ] Trending recommendations reflect actual industry trends

#### Ranking & Personalization
- [ ] Top recommendations are most relevant
- [ ] New recommendations push less relevant down
- [ ] Dismissed items stay dismissed
- [ ] Preferences respected in recommendations

#### Manager Recommendations
- [ ] Manager recommendations appear in separate section
- [ ] Accept/decline options work
- [ ] Required recommendations flagged clearly
- [ ] Due dates respected

#### Accessibility
- [ ] Recommendation cards keyboard navigable
- [ ] Screen reader announces recommendation reason
- [ ] Preference form accessible
- [ ] All actions keyboard accessible

---

## Summary: Learning & Development Module (Complete)

The Learning & Development module provides 5 comprehensive screens enabling continuous skill development, career growth, and professional advancement:

1. **Learning Catalog** (5.1) — Discover and browse learning opportunities with AI recommendations
2. **Course Enrollment & Progress** (5.2) — Track learning progress, complete courses, assessments
3. **Learning Path** (5.3) — Follow structured skill development sequences with milestones
4. **Skills & Certifications** (5.4) — Manage skills, endorsements, certifications with gap analysis
5. **Learning Recommendations** (5.5) — Receive personalized learning recommendations

**All screens maintain WCAG 2.2 AA accessibility standards with comprehensive color contrast, keyboard navigation, screen reader support, focus management, touch-friendly targets, clear error handling, and motion/animation preferences. AI integration points include personalized recommendations, adaptive pacing, peer benchmarking, trend detection, and career path optimization. Complete data models, integrations, edge cases, and success metrics provided for implementation.**
