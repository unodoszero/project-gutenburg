# Project Gutenberg Front-End Redesign

![HTML5](https://img.shields.io/badge/HTML5-MARKUP-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-STYLING-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JAVASCRIPT-VANILLA-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Static Site](https://img.shields.io/badge/STATIC-SITE-2E3440?style=for-the-badge)
![License](https://img.shields.io/badge/LICENSE-MIT-00A86B?style=for-the-badge)

A responsive static redesign concept for Project Gutenberg, focused on presenting the digital library with a cleaner home page, stronger navigation, visible search entry points, and a curated book-browsing layout.

This project is a front-end practice build rather than an official Project Gutenberg product. It recreates the feel of a public-domain ebook catalog using semantic HTML, custom CSS, vanilla JavaScript, local image assets, and a lightweight multi-page structure.

## Table of Contents

- [Preview](#preview)
- [Tech Stack](#tech-stack)
- [Repository Overview](#repository-overview)
- [Features](#features)
- [Installation Guide](#installation-guide)
- [Usage](#usage)
- [Design Notes](#design-notes)
- [Constraints & Future Improvements](#constraints--future-improvements)
- [License](#license)

## Preview

| Preview | Description |
| --- | --- |
| ![Project Gutenberg redesigned landing page](images/landing-page.png) | Home page redesign with fixed navigation, Project Gutenberg branding, donation prompt, primary search field, featured ebook sections, book covers, and footer links. |

## Tech Stack

| Technology | Role |
| --- | --- |
| HTML5 | Defines the page structure for the home page, catalog page, and placeholder supporting pages. |
| CSS3 | Handles layout, spacing, responsive behavior, visual hierarchy, book grids, footer styling, and hover states. |
| Vanilla JavaScript | Adds the responsive menu toggle behavior and resets the navigation display on larger viewports. |
| Local image assets | Provides book covers, social icons, Project Gutenberg logo treatments, favicon, and the README preview image. |

## Repository Overview

```text
.
├── Home.html              # Main redesigned Project Gutenberg landing page
├── catalog.html           # Simple catalog page with sample public-domain ebook links
├── about.html             # Placeholder supporting page
├── donate.html            # Placeholder supporting page
├── help.html              # Placeholder supporting page
├── home.css               # Shared styling for the landing page layout and responsive UI
├── script.js              # Mobile navigation toggle behavior
├── images/
│   ├── books/             # Local book cover images used in the featured grids
│   ├── pglogo/            # Logo, favicon, and menu icon assets
│   ├── socials/           # Footer social media icons
│   └── landing-page.png   # README preview screenshot
├── LICENSE
└── README.md
```

## Features

- Fixed top navigation with Project Gutenberg branding, page links, and a compact search field.
- Responsive mobile menu controlled with vanilla JavaScript.
- Donation callout section with dismiss-style close button UI.
- Large ebook search input designed as the main home page action.
- Featured book sections for latest, popular, and Project Gutenberg-published books.
- Hover states for book cards, links, search fields, and footer navigation.
- Footer layout with grouped informational links and social media icons.
- Separate catalog page linking to selected public-domain books on gutenberg.org.

## Installation Guide

1. Clone the repository:

   ```bash
   git clone https://github.com/shoichiideologies/project-gutenburg.git
   ```

2. Move into the project directory:

   ```bash
   cd project-gutenburg
   ```

3. Open the project in a browser. No package installation or build step is required because this is a static HTML/CSS/JavaScript project.

## Usage

Open `Home.html` directly in a browser:

```bash
open Home.html
```

You can also use a local static server if your environment prefers serving files over `file://` access:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/Home.html`.

## Design Notes

The redesign keeps Project Gutenberg's literary identity visible through serif typography, a restrained grayscale layout, and book-cover-forward browsing sections. The home page emphasizes the actions a visitor would expect from a digital library: searching the catalog, browsing featured books, learning about donations, and navigating to supporting sections.

The repository also includes custom Project Gutenberg logo assets for different placement contexts, including the main home page header and the compact navigation area.

## Constraints & Future Improvements

- The search fields are visual UI elements only; they do not currently query Project Gutenberg data.
- Several supporting pages are placeholders and would need complete content and shared styling.
- Some navigation links are static or placeholder links and should be normalized before deployment.
- The book lists are hardcoded instead of being generated from a catalog source or API.
- Future iterations could add accessible form behavior, active navigation states, a real search integration, reusable page templates, and stronger responsive testing across device sizes.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

This repository is an independent front-end redesign concept and is not affiliated with or endorsed by Project Gutenberg.
