# CVMake - Tailored Resume & Cover Letter Generator

A system for generating customized CVs and cover letters using AI. Maintain a comprehensive professional history database, then generate role-specific CVs tailored to different positions, companies, and industries.

## How It Works

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

## Basic Workflow

1. **Build your experience database** - Use Claude Code to interview you about your professional history. Claude populates detailed markdown files covering every role, achievement, and skill.

2. **Generate tailored CVs** - Ask Claude to create CVs for specific roles:
   ```
   "Generate a CV for a Senior Product Manager role at an early-stage AI startup"
   "Create a Head of Data CV targeting Series B+ companies"
   ```

3. **Compile to PDF** - Run `pdflatex cv.tex` to generate the final PDF.

The key insight: your experience database contains *more* detail than any single CV would include. Claude selects and emphasizes the most relevant content for each target role.

## Project Structure

```
cvmake/
├── CLAUDE.md                    # Instructions for Claude Code
├── templates/                   # Reusable LaTeX templates
│
└── private/                     # Git submodule (your private repo)
    ├── CLAUDE.md                # Your personal CV style preferences
    ├── experience/              # Professional history database
    │   └── professional-history.md
    ├── generated/               # Generated CVs and cover letters
    │   ├── baseline/            # Reusable baseline CVs by role type
    │   └── applications/        # Job-specific CVs
    └── seed/                    # Original pre-project resume (optional)
```

The `private/` folder is a git submodule pointing to a separate private repository. This keeps your personal data private while the project framework remains public.

## Getting Started

### Prerequisites

- **Git** - For version control
- **Claude Code** - For AI-assisted CV generation ([claude.ai/claude-code](https://claude.ai/claude-code))
- **LaTeX** - For compiling `.tex` files to PDF (see installation below)

### 1. Fork and clone

```bash
git clone git@github.com:yourname/cvmake.git
cd cvmake
```

### 2. Set up your private content repo

Create a **private** repo on GitHub (e.g., `yourname/cvmake-private`), then link it:

```bash
# Remove the existing submodule reference
git submodule deinit -f private
git rm -f private
rm -rf .git/modules/private

# Add your own private repo as a submodule
git submodule add git@github.com:yourname/cvmake-private.git private

# Set up the folder structure
cd private
mkdir -p experience generated/baseline generated/applications seed
touch experience/professional-history.md
git add . && git commit -m "Initial structure" && git push

cd ..
git add . && git commit -m "Link to my private repo" && git push
```

### 3. Populate your professional history

Start Claude Code and ask it to interview you:

```bash
claude
```

Then: *"Interview me about my professional history and populate the experience database."*

Claude will guide you through each role, extracting achievements, metrics, skills, and context.

### 4. Generate your first CV

Once your experience database is populated:

```
"Generate a 2-page CV for [target role] at [company type]"
```

Then compile:

```bash
cd private/generated/[your-cv-folder]
pdflatex cv.tex
pdflatex cv.tex  # Run twice for proper formatting
```

## Installation

### LaTeX (macOS)

```bash
# Option 1: BasicTeX (smaller, ~100MB)
brew install --cask basictex

# Option 2: Full MacTeX (larger, ~4GB, includes GUI apps)
brew install --cask mactex

# After installation, restart terminal or run:
eval "$(/usr/libexec/path_helper)"

# Install required packages
sudo tlmgr update --self
sudo tlmgr install fontawesome5 enumitem titlesec parskip lmodern
```

### Alternative: Overleaf (no local install)

1. Go to [overleaf.com](https://overleaf.com)
2. Create new project → Upload the `.tex` file
3. Click "Recompile"

## Tips

### For Better CV Generation
- Keep your experience database detailed - include more than you'd ever put on one CV
- Note specific metrics (percentages, team sizes, revenue impact)
- Include context about company stage, team size, reporting structure
- Document challenges overcome and skills developed

### For Specific Applications
- Tell Claude the exact role title and company
- Mention industry or company culture if relevant
- Specify which aspects of your background to emphasize
- Request specific length (1 page, 2 pages) if needed

## Troubleshooting

### Missing LaTeX packages
```bash
sudo tlmgr install [package-name]
```

### PDF not updating
Run `pdflatex` twice - some elements need two passes to render correctly.

## License

MIT License - Feel free to fork and adapt for your own use.
