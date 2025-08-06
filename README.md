# Modern Typst Resume Template

A clean, professional, and modern resume template built with [Typst](https://typst.app/), the modern alternative to LaTeX. Features a contemporary design with color-coded sections, skill badges, and project cards.

## Resume Preview
**[View PDF Preview →](resume.pdf)**

## Features

- **Modern Design**: Clean layout with professional color scheme and typography
- **Responsive Layout**: Optimized for both digital viewing and printing
- **Color-Coded Sections**: Organized skill categories with visual badges
- **Project Showcase**: Featured project cards with technology highlights
- **Professional Timeline**: Modern experience section with visual accents
- **Customizable**: Easy to modify colors, fonts, and layout elements
- **ATS-Friendly**: Clean structure that works well with Applicant Tracking Systems

## Design Highlights

- **Color Scheme**: Professional blue gradients with strategic accent colors
- **Typography**: Clean, readable fonts with proper hierarchy
- **Visual Elements**: Rounded corners, subtle borders, and strategic spacing
- **Skill Badges**: Modern pill-shaped badges for technical skills
- **Card Layout**: Project information displayed in clean, organized cards
- **Contact Icons**: Visual contact information with icons

## Prerequisites

- [Typst](https://typst.app/) installed on your system
- Typst CLI or Typst Web App access

### Installation Options

**Option 1: Typst CLI**
```bash
# Install via cargo
cargo install --git https://github.com/typst/typst --locked typst-cli

# Or download from releases
# https://github.com/typst/typst/releases
```

**Option 2: Web App**
Use the [Typst Web App](https://typst.app/) directly in your browser.

## Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/lazzerex/modern-typst-resume.git
   cd modern-typst-resume
   ```

2. **Edit the resume**
   - Open `main.typ` in your preferred editor
   - Replace placeholder content with your information
   - Customize colors and styling as needed

3. **Compile to PDF**
   ```bash
   typst compile main.typ
   ```
   
   Or for continuous compilation:
   ```bash
   typst watch main.typ
   ```

## Customization Guide

### Personal Information
Replace the placeholder content in the header section:
```typst
= Your Name
#text(size: 12pt, fill: secondary-color, style: "italic")[Your Title]
```

### Colors
Modify the color scheme at the top of the file:
```typst
#let primary-color = rgb("#2563eb")    // Main blue
#let secondary-color = rgb("#64748b")  // Gray text
#let accent-color = rgb("#0ea5e9")     // Accent blue
```

### Skills
Update skill categories and add your technologies:
```typst
("Your", "Skills", "Here").map(skill => skill-badge(skill)).join(h(4pt))
```

### Projects
Add your projects using the project card function:
```typst
project-card(
  "Project Name",
  "Project description...",
  ("Tech1", "Tech2", "Tech3"),
  link: "github.com/yourusername/project",
  featured: true  // Optional: highlights the project
)
```

### Experience
Update work experience using the experience entry function:
```typst
#experience-entry(
  "Job Title",
  "Company Name",
  "Duration",
  "Location",
  (
    "Responsibility 1",
    "Responsibility 2",
    "Achievement with metrics"
  )
)
```

## File Structure

```
├── resume.typ         # Main resume template
├── README.md          # This file
├── preview.png        # Resume preview image
└── examples/          # Example variations
    ├── single-page.typ
    ├── two-page.typ
    └── minimal.typ
```

## Sections Included

- **Header**: Name, title, and contact information
- **Professional Summary**: Brief overview with highlighted background
- **Technical Skills**: Categorized skill badges
- **Featured Projects**: Showcase of main projects with descriptions
- **Additional Projects**: Compact listing of other work
- **Professional Experience**: Timeline-style work history
- **Education & Achievements**: Academic background and key accomplishments

## Advanced Customization

### Adding New Sections
```typst
== New Section
#box(
  width: 100%,
  fill: light-gray,
  stroke: 1pt + primary-color.lighten(70%),
  radius: 8pt,
  inset: 1em
)[
  Your content here...
]
```

### Custom Skill Badge Colors
```typst
#("Skill1", "Skill2").map(skill => 
  skill-badge(skill, color: rgb("#your-color"))
).join(h(4pt))
```

### Modifying Layout
The template uses Typst's `grid` function for responsive layouts:
```typst
#grid(
  columns: (1fr, 1fr),  // Two equal columns
  gutter: 1em,
  [Column 1 content],
  [Column 2 content]
)
```

## Export Options

### PDF Generation
```bash
# Standard compilation
typst compile main.typ resume.pdf

# High-quality output
typst compile main.typ --ppi 300 resume-hq.pdf
```

### PNG/SVG Export
```bash
# Export as PNG
typst compile main.typ resume.png

# Export as SVG
typst compile main.typ resume.svg
```

## Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Make your changes** and test them
4. **Commit your changes** (`git commit -m 'Add amazing feature'`)
5. **Push to the branch** (`git push origin feature/amazing-feature`)
6. **Open a Pull Request**

### Contribution Ideas
- Additional color schemes
- New layout variations
- Industry-specific templates
- Multi-language support
- Additional helper functions

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Typst](https://typst.app/) team for creating an amazing typesetting system
- Modern CV design inspiration from contemporary resume trends
- Open source community for feedback and contributions

## Support

- **Issues**: [GitHub Issues](https://github.com/lazzerex/modern-typst-resume/issues)
- **Discussions**: [GitHub Discussions](https://github.com/lazzerex/modern-typst-resume/discussions)
- **Typst Documentation**: [Official Typst Docs](https://typst.app/docs)

---


**If this template helped you land your dream job, please consider giving it a star!**
