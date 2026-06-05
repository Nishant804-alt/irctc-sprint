# IRCTC Design Engineering Sprint

![Status](https://img.shields.io/badge/Status-Part%20A%20Complete-success)
![Version](https://img.shields.io/badge/Version-1.0.0-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 📋 Table of Contents

- [Overview](#overview)
- [Project Background](#project-background)
- [Repository Structure](#repository-structure)
- [Part A Deliverables](#part-a-deliverables)
- [Part B Deliverables](#part-b-deliverables)
- [Methodology](#methodology)
- [Tools Used](#tools-used)
- [How to Run](#how-to-run)
- [Git Workflow](#git-workflow)
- [Contribution Guidelines](#contribution-guidelines)
- [Submission Requirements](#submission-requirements)
- [License](#license)

## 🎯 Overview

This repository contains the deliverables for the **IRCTC Design Engineering Sprint**, a comprehensive product management and UX research project focused on identifying and documenting critical user experience issues in the Indian Railway Catering and Tourism Corporation (IRCTC) online ticketing platform.

### Sprint Structure

- **Part A:** Problem Discovery - Detailed documentation of 6 high-impact user experience issues
- **Part B:** Solution Specifications - Technical specifications, AI feature proposals, and prioritization matrices

### Project Goal

Provide actionable insights for improving the IRCTC platform's usability, reliability, and overall user experience through systematic problem identification and solution planning.

## 📚 Project Background

IRCTC (Indian Railway Catering and Tourism Corporation) is the official online ticketing platform for Indian Railways, serving millions of users daily. Despite its critical importance, the platform suffers from numerous user experience issues that impact booking efficiency, user satisfaction, and system reliability.

This sprint adopts a structured approach to:
- Identify and document critical UX problems through systematic research
- Analyze user flows and break points
- Propose technical solutions with implementation specifications
- Leverage AI capabilities to enhance platform functionality
- Prioritize improvements based on impact and effort

## Repository Structure

```
irctc-sprint/
├── README.md                          # Project overview and documentation
├── part-a/
│   └── PROBLEMS.md                    # Problem discovery documentation
├── part-b/
│   ├── SPECS.md                       # Technical solution specifications
│   ├── AI-FEATURE.md                  # AI-powered feature proposals
│   └── MATRIX.md                      # Prioritization and impact analysis
└── assets/
    └── screenshots/                   # Screenshots supporting problem documentation
```

## Part A Deliverables

### PROBLEMS.md
A comprehensive problem discovery document containing:

- **Summary:** Overview of 6 documented problems across IRCTC platform
- **Problem 1:** Tatkal Booking Crashes at 10:00 AM
  - System failure during critical booking windows
  - 12-step user flow with break point analysis
  - Technical failure identification (API, database, load balancer)
  
- **Problem 2:** Search Filters Do Not Work Reliably
  - Inconsistent filter application across train search
  - 15-step user flow with multiple break points
  - Session state and cache failure analysis
  
- **Problem 3:** Seat Selection Resets Randomly
  - Seat selection state persistence issues
  - 17-step user flow demonstrating reset behavior
  - Frontend state management and concurrency issues
  
- **Problem 4:** Payment Gateway Timeout During High Traffic
  - Payment integration failures during peak hours
  - 15-step user flow with timeout analysis
  - Gateway API and transaction lock failures
  
- **Problem 5:** PNR Status Not Updating in Real-Time
  - Delayed PNR status updates causing misinformed decisions
  - 15-step user flow showing cache invalidation issues
  - Database sync and cache TTL problems
  
- **Problem 6:** Mobile Layout Breaks on Smaller Screens
  - Responsive design failures on budget smartphones
  - 17-step user flow demonstrating layout issues
  - CSS media query and touch target failures

Each problem includes:
- What is broken
- How I found it (for self-discovered problems)
- Affected users
- Frequency analysis
- Current flow step by step (minimum 6 steps)
- Where exactly it breaks
- Screenshot description

## Part B Deliverables

### SPECS.md
Technical solution specifications for addressing the documented problems:
- Detailed technical requirements for each fix
- Implementation approaches and architecture recommendations
- API specifications and database schema changes
- Frontend component redesign specifications
- Testing and validation criteria

### AI-FEATURE.md
Proposed AI-powered features to enhance IRCTC platform:
- Intelligent recommendation engine for train selection
- Predictive waitlist confirmation system
- Natural language query interface
- Automated customer support chatbot
- Dynamic pricing optimization
- Fraud detection and prevention

### MATRIX.md
Prioritization and impact analysis:
- Problem prioritization matrix (severity vs. effort)
- ROI analysis for proposed solutions
- Risk assessment for implementation
- Timeline and resource allocation recommendations
- Success metrics and KPIs

## Tools Used

### Research & Documentation
- **Markdown:** Documentation formatting
- **Git:** Version control and collaboration
- **Chrome DevTools:** Browser inspection and debugging
- **Mobile Device Testing:** Cross-device compatibility testing

### Platforms Tested
- **Desktop Chrome:** Primary desktop browser testing
- **Mobile Chrome:** Mobile browser testing on various screen sizes
- **Budget Smartphones:** Testing on devices < 360px screen width

### Documentation Tools
- **VS Code:** Code and markdown editing
- **Git:** Version control
- **GitHub:** Repository hosting and collaboration

## How to Run

### Prerequisites
- Git installed on local machine
- Basic understanding of markdown syntax
- Text editor or IDE (VS Code recommended)

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd irctc-sprint
   ```

2. **Review Part A deliverables**
   ```bash
   # Open problem documentation
   cat part-a/PROBLEMS.md
   # Or open in your preferred markdown viewer
   ```

3. **Review Part B deliverables** (when available)
   ```bash
   # View solution specifications
   cat part-b/SPECS.md
   # View AI feature proposals
   cat part-b/AI-FEATURE.md
   # View prioritization matrix
   cat part-b/MATRIX.md
   ```

4. **View screenshots** (when available)
   ```bash
   # Navigate to screenshots directory
   cd assets/screenshots
   # View supporting screenshots
   ```

### Viewing Markdown Files
- **VS Code:** Built-in markdown preview (Ctrl+Shift+V)
- **GitHub:** Automatic markdown rendering in repository view
- **Markdown editors:** Typora, MarkText, or any markdown viewer
- **Command line:** `cat` or `less` for basic viewing

## Git Workflow

### Branching Strategy
- `master` branch: Main production branch
- Feature branches: Created for each major deliverable (e.g., `part-a-problems`, `part-b-specs`)

### Commit Convention
Use descriptive commit messages following conventional commit format:
```
<type>: <subject>

<body>

<footer>
```

**Types:**
- `feat`: New feature or deliverable
- `docs`: Documentation changes
- `fix`: Bug fixes or corrections
- `refactor`: Code restructuring
- `style`: Formatting changes
- `test`: Test additions or modifications

**Examples:**
```
docs: add comprehensive problem documentation for Part A
feat: complete AI feature proposals for Part B
fix: correct formatting in SPECS.md
```

### Workflow Steps

1. **Create feature branch**
   ```bash
   git checkout -b feature/<branch-name>
   ```

2. **Make changes and commit**
   ```bash
   git add .
   git commit -m "feat: add problem documentation"
   ```

3. **Push to remote**
   ```bash
   git push origin feature/<branch-name>
   ```

4. **Create pull request** (if using GitHub/GitLab)
   - Describe changes in PR description
   - Reference related issues
   - Request review from team members

5. **Merge after approval**
   - Squash commits for clean history
   - Delete feature branch after merge

### Pull Request Guidelines
- Keep PRs focused and small
- Include descriptive title and description
- Link to related issues or deliverables
- Ensure all documentation is updated
- Request review before merging

## Submission Requirements

### Part A Submission Checklist
- [x] PROBLEMS.md completed with 6 documented problems
- [x] Each problem includes affected users section
- [x] Each problem includes frequency analysis
- [x] Each problem includes minimum 6-step current flow
- [x] Each problem clearly identifies exact failure points
- [x] Professional markdown formatting throughout
- [x] Screenshots documented in description sections
- [ ] Actual screenshot files added to assets/screenshots/ (optional)

### Part B Submission Checklist (To Be Completed)
- [ ] SPECS.md with technical solution specifications
- [ ] AI-FEATURE.md with AI-powered feature proposals
- [ ] MATRIX.md with prioritization and impact analysis
- [ ] All deliverables follow professional markdown formatting
- [ ] Cross-references between Part A problems and Part B solutions
- [ ] Implementation timeline and resource allocation

### Quality Standards
- **Clarity:** All documentation must be clear and concise
- **Completeness:** All sections must be thoroughly filled
- **Accuracy:** Technical details must be accurate and realistic
- **Professionalism:** Maintain professional tone throughout
- **Consistency:** Use consistent formatting and terminology
- **Actionability:** Solutions must be implementable and specific

### Final Submission
1. Ensure all deliverables are complete
2. Verify markdown formatting renders correctly
3. Check all links and references work
4. Commit all changes with descriptive message
5. Push to main branch
6. Create release tag (if applicable)
7. Submit repository link or zip file as required

## Contact & Support

For questions or clarifications regarding this sprint:
- Review the documentation in each deliverable
- Check git commit history for change rationale
- Refer to project guidelines provided by instructors/mentors

---

**Last Updated:** June 5, 2026
**Version:** 1.0.0
**Status:** Part A Complete, Part B In Progress
