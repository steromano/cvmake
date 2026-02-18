# CVMake - Tailored Resume & Cover Letter Generator

A system for generating customized CVs and cover letters based on a comprehensive professional experience database. Built to work with Claude Code for intelligent CV generation tailored to specific roles, companies, and industries.

## Prerequisites

### Required
- **Git** - For version control
- **Claude Code** - For AI-assisted CV generation and professional history interviews

### For PDF Generation
- **LaTeX** - Required to compile `.tex` files to PDF

**macOS Installation:**
```bash
# Option 1: BasicTeX (smaller, ~100MB)
brew install --cask basictex

# Option 2: Full MacTeX (larger, ~4GB, includes GUI apps)
brew install --cask mactex

# After installation, restart terminal or run:
eval "$(/usr/libexec/path_helper)"

# Install additional LaTeX packages (if needed)
sudo tlmgr update --self
sudo tlmgr install fontawesome5 enumitem titlesec
```

**Alternative - No Local Install:**
- Use [Overleaf](https://overleaf.com) (free online LaTeX editor)
- Upload `.tex` files and compile in browser

## Project Structure

```
cvmake/
├── CLAUDE.md                    # Instructions for Claude Code
├── README.md                    # This file
├── .gitignore                   # Git ignore rules
├── .gitmodules                  # Submodule configuration
│
├── templates/                   # Reusable LaTeX templates (public)
│   ├── cv/
│   │   ├── modern.tex          # Contemporary design
│   │   ├── traditional.tex     # Conservative format
│   │   └── technical.tex       # Tech-focused layout
│   └── cover-letter/
│       └── standard.tex        # Cover letter template
│
└── private/                     # Git submodule (private repo)
    ├── CLAUDE.md                # Personal CV style preferences
    ├── config/                  # Personal configuration
    │   ├── personal-info.yaml  # Contact details, links
    │   └── preferences.yaml    # CV generation preferences
    │
    ├── experience/              # Professional history database
    │   ├── professional-history.md
    │   ├── education.md
    │   ├── skills.md
    │   └── achievements.md
    │
    ├── generated/               # Generated CVs and cover letters
    │   ├── baseline/            # Example CVs
    │   │   └── [target-role-name]/
    │   └── applications/        # Job-specific CVs
    │       └── [company-role-date]/
    │
    └── manual/                  # Reference materials (existing CVs, etc.)
```

**Note:** The `private/` folder is a git submodule pointing to a separate private repository. This keeps personal data (professional history, generated CVs) private while the project framework remains public.

## Getting Started

### 1. Fork this repo

Fork to get the public framework (templates, CLAUDE.md instructions).

### 2. Create your private content repo

Create a **private** repo on GitHub (e.g., `yourname/cvmake-private`) to store your personal data.

### 3. Set up the submodule

```bash
# Clone your fork
git clone git@github.com:yourname/cvmake.git
cd cvmake

# Remove the existing submodule reference (points to original author's private repo)
git submodule deinit -f private
git rm -f private
rm -rf .git/modules/private

# Add your own private repo as a submodule
git submodule add git@github.com:yourname/cvmake-private.git private

# Set up the folder structure in your private repo
cd private
mkdir -p config experience generated/baseline generated/applications manual
touch config/personal-info.yaml config/preferences.yaml
touch experience/professional-history.md experience/education.md experience/skills.md
git add . && git commit -m "Initial structure" && git push

# Commit the submodule change to your fork
cd ..
git add . && git commit -m "Link to my private repo" && git push
```

### 4. Populate your personal content

In `private/`:
- `config/personal-info.yaml` - your contact details
- `experience/professional-history.md` - your work history (use Claude to interview you!)
- `CLAUDE.md` - your personal CV style preferences (optional)
- `generated/` - where your CVs will be stored

## Usage

### 1. Configure Personal Information

Edit `private/config/personal-info.yaml` with your contact details:

```yaml
name: "Your Name"
title: "Your Professional Title"
contact:
  email: "you@example.com"
  phone: "+1 234 567 890"
  location: "City, Country"
links:
  linkedin: "linkedin.com/in/yourprofile"
  github: "github.com/yourusername"
```

### 2. Populate Professional History

The best way to populate your experience database is through a conversation with Claude Code:

```bash
claude
```

Then ask Claude to interview you about your professional history. Claude will populate the files in `private/experience/` with detailed information about each role, achievements, skills, and career narrative.

### 3. Generate Tailored CVs

Once your experience database is populated, ask Claude to generate CVs for specific roles:

```
"Generate a CV for a Senior Product Manager role at an early-stage AI startup"

"Create a Head of Data CV targeting Series B+ companies"

"Make a cover letter for the Staff Engineer role at [Company]"
```

Claude will:
- Select relevant experience for the target role
- Emphasize appropriate achievements and skills
- Generate LaTeX files in `private/generated/`
- Create metadata documenting the targeting strategy

### 4. Compile to PDF

```bash
cd private/generated/[your-cv-folder]
pdflatex cv.tex
pdflatex cv.tex  # Run twice for proper formatting

# Or compile cover letter
pdflatex cover-letter.tex
```

**Tip:** Run `pdflatex` twice to ensure cross-references and formatting are correct.

## Workflow

```
┌─────────────────────────────────────────────────────────────────┐
│                     EXPERIENCE DATABASE                          │
│  professional-history.md | education.md | skills.md | etc.      │
│         (Detailed, comprehensive, more than any single CV)       │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                    CLAUDE CODE + TEMPLATES                       │
│      Selects relevant content, emphasizes key achievements       │
│      Tailors narrative for specific role/company/industry        │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                      GENERATED CV + COVER LETTER                 │
│            LaTeX source → PDF (compiled via pdflatex)            │
│               Stored in generated/ for future reuse              │
└─────────────────────────────────────────────────────────────────┘
```

## Templates

### CV Templates

| Template | Best For |
|----------|----------|
| `modern.tex` | Startups, tech companies, modern industries |
| `traditional.tex` | Finance, consulting, traditional corporates |
| `technical.tex` | Engineering roles, technical positions |

### Customization

Templates use standard LaTeX and can be customized:
- Colors defined at top of file (`\definecolor`)
- Margins in `\geometry{...}`
- Section formatting in `\titleformat{...}`

## Tips

### For Better CV Generation
- Keep `private/experience/professional-history.md` detailed - include more than you'd ever put on one CV
- Note specific metrics and achievements (percentages, team sizes, revenue impact)
- Include context about company stage, team size, reporting structure
- Document challenges overcome and skills developed

### For Specific Applications
- Tell Claude the exact role title and company
- Mention industry or company culture if relevant
- Specify which aspects of your background to emphasize
- Request specific length (1 page, 2 pages) if needed

## Troubleshooting

### LaTeX Compilation Errors

**Missing packages:**
```bash
sudo tlmgr install [package-name]
```

**Common packages needed:**
```bash
sudo tlmgr install fontawesome5 enumitem titlesec parskip xcolor hyperref geometry
```

**Font issues:**
```bash
sudo tlmgr install lmodern
```

### PDF Not Updating
Run `pdflatex` twice - some elements need two passes to render correctly.

### Overleaf Alternative
If local LaTeX is problematic:
1. Go to [overleaf.com](https://overleaf.com)
2. Create new project → Upload Project
3. Upload the `.tex` file
4. Click "Recompile"

## License

MIT License - Feel free to fork and adapt for your own use.
