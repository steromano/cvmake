# CVMake - Tailored Resume & Cover Letter Generator

## Project Purpose
This project helps generate tailored resumes and cover letters for specific roles, companies, and industries. It maintains a comprehensive professional experience record and generates customized application materials on demand.

## Core Workflow

### 1. Professional Experience Database
- **Master Record**: `private/experience/professional-history.md` - Contains detailed work history with more information than typically appears on any single CV
- **Content Population**: Claude acts as a professional career coach, interviewing the user through conversation to build out the experience record
- **Ongoing Maintenance**: The master record is continuously updated as new experiences and achievements are discussed
- **Privacy**: All personal content lives in `private/` which is a git submodule pointing to a separate private repository

### 2. CV Generation
- **On-Demand Creation**: Generate tailored CVs for specific applications
- **Smart Selection**: Choose and emphasize the most relevant experiences for each role
- **Strategic Positioning**: Frame the profile to align with the target role/company/industry
- **Library Storage**: All generated CVs are stored in `private/generated/` for future reference and reuse

### 3. Cover Letter Generation
- Similar approach to CVs: tailored, strategic, and stored for reference

## Claude's Role
1. **Career Coach**: Interview the user to understand their professional background deeply
2. **Content Curator**: Select and emphasize relevant experiences for each application
3. **Strategic Advisor**: Position the user's profile effectively for target opportunities
4. **Claude Code Mentor**: Help the user learn Claude Code features progressively throughout the project

## Project Structure Guidelines
- Keep the master experience record detailed and comprehensive
- Store generated materials grouped by application (CV + cover letter together)
- Use clear naming conventions: `role-company-YYYY-MM-DD`
- Use LaTeX for CV and cover letter generation (professional output, flexible formatting)
- Use templates for consistency across generated documents
- Make it easy to regenerate or update previously created materials

## Claude Code Learning Goals
- Progressively introduce advanced features when appropriate
- Flag useful slash commands during natural workflow moments
- Suggest workflow improvements as opportunities arise
- Balance project work with learning new capabilities

## CV Style Preferences

### Content & Tone
- **Include all roles**: Even early career positions should appear, though they can be condensed
- **Group early career roles**: Combine early IC roles into a single "Early Career" block with brief bullet points per company
- **Plain, factual language**: Avoid hypey words like "superpower", "excellence", "cutting-edge", "best-in-class"
- **Tone down self-promotion**: Phrases like "Shipped core product features" or "hiring excellence" feel over-the-top; prefer more neutral descriptions
- **Headlines describe areas, not metrics**: Keep impact metrics (% savings, # deals) in the body text, not in bold headlines. Headlines should describe the area of work (e.g., "Data Platform" not "Data Platform Rebuild - 70% Cost Savings")

### Formatting (LaTeX)
- **Tight but readable spacing**: Reduce whitespace between job header (title + subtitle) and bullet points, but not so tight they overlap
- **No orphaned headers**: Job headers must stay on the same page as their bullet points (use `\begin{minipage}{\textwidth}...\end{minipage}`)
- **Tech/Note footers**: Include a small "Tech:" or "Note:" line after bullet points where relevant, with slight spacing above
- **Two-page target**: Aim to fill both pages without spilling to a third
- **Footer attribution**: Include a small footer linking to this GitHub repo, explaining the CV was generated with Claude Code

### Structure
- **Baseline CVs**: Store reusable templates in `private/generated/baseline/`
- **Application CVs**: Store job-specific CVs in `private/generated/applications/`
- **Naming convention**: `[target-role]-[context]` for baseline, `[company]-[role]-[date]` for applications
- **Privacy**: All personal content lives in the `private/` submodule (separate private repo)
