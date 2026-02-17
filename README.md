# CVMake - Tailored Resume & Cover Letter Generator

A system for generating customized CVs and cover letters based on a comprehensive professional experience database.

## Structure

```
cvmake/
├── config/                    # Personal information and preferences
├── experience/                # Detailed professional history
├── templates/                 # LaTeX templates for CVs and cover letters
└── generated/                 # Generated application materials
    └── [role-company-YYYY-MM-DD]/
        ├── cv.tex
        ├── cv.pdf
        ├── cover-letter.tex
        ├── cover-letter.pdf
        └── metadata.yaml
```

## Workflow

1. **Populate Experience Database**: Work with Claude to build out your professional history in the `experience/` folder
2. **Generate Tailored Materials**: Request a CV for a specific role/company
3. **Review & Edit**: Claude generates LaTeX files that you can review and edit
4. **Compile**: Generate PDF from LaTeX
5. **Store**: All materials saved in `generated/` for future reference

## Getting Started

1. Fill in `config/personal-info.yaml` with your contact details
2. Start populating your professional history by chatting with Claude
3. Generate your first CV for a target role

## Templates

- **modern.tex**: Contemporary design with accent colors
- **traditional.tex**: Conservative format for traditional industries
- **technical.tex**: Optimized for tech roles with skills-first layout

## Compiling LaTeX

```bash
cd generated/[application-folder]
pdflatex cv.tex
pdflatex cover-letter.tex
```

Or use your preferred LaTeX editor (Overleaf, TeXShop, VS Code with LaTeX Workshop, etc.)
