# HR Operating Framework

A static HTML reference site covering 11 HR practice areas with 89 individual modules — structured for execution across multi-site, multi-country operations.

## Structure

```
hr_system/
├── index.html                          # Master index (entry point)
├── [dept]_[module].html                # 89 individual module pages
└── README.md
```

### The 11 Practice Areas

| # | Area | Tier | Modules |
|---|------|------|---------|
| 01 | HR Operations | Operational | 9 |
| 02 | Talent Acquisition | Operational | 9 |
| 03 | Compensation & Benefits | Operational / Strategic | 8 |
| 04 | Performance Management | Operational | 7 |
| 05 | Learning & Development | Strategic | 7 |
| 06 | People Analytics | Strategic | 9 |
| 07 | HR Business Partnering | Strategic | 10 |
| 08 | Employee Experience & Culture | Enterprise | 8 |
| 09 | Organisation Design | Enterprise | 9 |
| 10 | HR Technology | Enterprise | 9 |
| 11 | Centre of Excellence | Enterprise | 7 |

## Usage

Open `index.html` in any browser — no build step or server required.

- **Search**: Press `/` to focus the search bar and filter modules by name or description. Press `Escape` to clear.
- **Navigate by department**: Use the nav chips below the hero to jump to a specific practice area.

## File Naming Convention

```
[number]_[dept]_[topic].html
  │        │       └── module topic (snake_case)
  │        └── department code: ta, cb, pm, ld, pa, hrbp, ex, od, hrtech, coe, hr-ops
  └── module number within the department (1–10)
```

Example: `3_hrbp_stakeholder.html` → HRBP module #3, Stakeholder Management

## Tech Stack

- Pure HTML + CSS (no build tools, no frameworks)
- Google Fonts: Fraunces, Epilogue, JetBrains Mono, IBM Plex Sans, IBM Plex Mono, Playfair Display
- Vanilla JavaScript (tab switching, search/filter on index)
- Responsive via CSS media queries

## Known Limitations & Improvement Areas

- **CSS duplication**: Each HTML file embeds its own full stylesheet. A shared `shared.css` would reduce the repo size significantly.
- **No CMS**: Content is hardcoded in HTML. Any update requires manual editing.
- **No build pipeline**: No minification or optimisation.
- **Accessibility**: ARIA labels and keyboard navigation are partial.

## Contributing

All module files follow the same pattern:
1. CSS variables in `:root` for the colour scheme
2. A sticky header with department logo and status badges
3. Navigation tabs switching between content panels via the `sw()` JS function
4. Stat cards, data tables, and supporting components

To add a new module, copy the closest existing file in the same department and update the content and `<title>` tag.
