# Project Gutenberg - Front-End Redesign

A modern, responsive redesign of Project Gutenberg's user interface, bringing contemporary web standards to the world's oldest digital library while preserving its core mission of providing free access to public domain literature.

## Table of Contents

- [Overview](#overview)
- [Preview](#preview)
- [Tech Stack](#tech-stack)
- [Repository Structure](#repository-structure)
- [Features](#features)
- [Installation Guide](#installation-guide)
- [Usage](#usage)
- [Constraints & Future Improvements](#constraints--future-improvements)
- [License](#license)

## Overview

Project Gutenberg is a dedicated effort to digitize and archive cultural works in the public domain. This redesign project focuses on modernizing the user experience and accessibility of the original platform through contemporary front-end web technologies.

The objective is to demonstrate professional UI/UX design principles while respecting the mission of providing free access to literature without barriers. This project was developed as part of a comprehensive web programming course focused on front-end development mastery.

## Preview

![Project Gutenberg Landing Page](images/landing-page.png)

The redesigned interface features a clean, professional layout with:
- Fixed navigation bar with responsive menu toggle and prominent logo
- Integrated search functionality for book discovery
- Featured sections for latest and popular public domain books with cover images
- Donation prompt banner encouraging user contributions
- Mobile-first responsive design with hamburger menu for smaller screens

## Tech Stack

| Technology               | Purpose                                                                                                                                 |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| **HTML5**                | Semantic markup structure for accessible, standards-compliant web pages. Supports accessibility features and SEO optimization.          |
| **CSS3**                 | Modern styling with flexbox layouts, responsive media queries, and smooth transitions. Ensures visual consistency across pages.         |
| **JavaScript (Vanilla)** | Lightweight, dependency-free interactivity for menu toggles, search functionality, and responsive behavior without external frameworks. |
| **SVG Icons**            | Scalable vector graphics for interface elements (search, close buttons, menu icons) ensuring crisp display at all resolutions.          |

## Repository Structure

```
project-gutenberg/
├── Home.html              # Main landing page with featured books and search
├── catalog.html           # Book catalog with filtering and pagination
├── about.html             # Project information and mission statement
├── help.html              # User support and FAQ documentation
├── donate.html            # Donation information and contribution options
├── home.css               # Primary stylesheet with responsive layouts
├── script.js              # Core interactivity (menu toggle, responsive behavior)
├── images/
│   ├── pglogo/            # Project Gutenberg logos (light/dark variants)
│   ├── books/             # Book cover images and thumbnails
│   └── socials/           # Social media icons and links
├── README.md              # Project documentation
└── LICENSE                # MIT License
```

**Key Design Decisions:**

- Centralized CSS for consistent styling across all pages
- Vanilla JavaScript to eliminate dependencies and reduce bundle size
- SVG icons for crisp, scalable interface elements
- Fixed navigation for persistent access to site features
- Semantic HTML structure for improved accessibility

## Features

### Core Functionality

- **Responsive Navigation** — Fixed header with collapsible menu for mobile devices, toggle logic handles window resize events
- **Search Interface** — Multiple search entry points (header and main search bar) supporting title, author, publisher, and ISBN queries
- **Book Catalog Display** — Grid-based layout showcasing featured books with cover images, titles, and clickable links
- **Donation Prompt** — Modal-style donation banner with close functionality to encourage user contributions
- **Mobile-First Responsive Design** — Hamburger menu automatically shows/hides based on viewport width with threshold at 1100px

### Visual Design

- **Modern Aesthetic** — Clean white/light gray backgrounds with dark navigation bar for strong visual hierarchy
- **Logo Redesign** — Custom Project Gutenberg logos optimized for both dark and light backgrounds
- **Book Cover Grid** — Professional presentation of literature with consistent image dimensions and spacing
- **Accessibility** — Proper alt text, semantic HTML, keyboard-navigable interface elements

## Installation Guide

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- A local web server (for development)

### Setup Steps

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/project-gutenberg.git
   cd project-gutenberg
   ```

2. **Start a local web server:**

   Using Python 3:

   ```bash
   python -m http.server 8000
   ```

   Using Python 2:

   ```bash
   python -m SimpleHTTPServer 8000
   ```

   Using Node.js (install http-server globally):

   ```bash
   npm install -g http-server
   http-server
   ```

3. **Access the application:**

   ```
   http://localhost:8000
   ```

4. **Navigate through pages:**
   - Click "Home" in the navigation menu
   - Use the hamburger icon on mobile devices to toggle the menu
   - Click book covers to view details (placeholder pages available)

### Why a Local Server?

HTML files use relative paths for stylesheets and scripts. Opening files directly with `file://` protocol can cause CORS issues and prevent proper loading of resources. A local web server ensures all assets load correctly.

## Usage

### For Users

1. **Browsing Books:**
   - Start at the home page to view latest and popular books
   - Click on any book cover to view detailed information
   - Use the search bar to find books by title, author, publisher, or ISBN

2. **Navigation:**
   - Use the top navigation menu to access different sections
   - On mobile devices, click the hamburger icon to reveal the menu
   - The menu automatically collapses on screens narrower than 1100px

3. **Search:**
   - Enter search terms in the dedicated search field
   - Results update based on your query
   - Filter by author or genre for more refined results

### For Developers

**Customizing Styling:**

- Edit `home.css` to modify colors, fonts, and layouts
- All CSS follows a single-file architecture for maintainability
- Uses flexbox for layout (no float-based or grid-based layouts)

**Adding Interactive Features:**

- Extend `script.js` with additional event listeners
- Current implementation includes menu toggle and responsive resize handler
- Consider extracting features into separate files for larger projects

**Modifying Content:**

- Update HTML files to change page structure
- Replace book images in `images/books/` directory
- Update book metadata in carousel/grid sections

## Constraints & Future Improvements

### Current Limitations

1. **Static Book Data** — Book information is hardcoded in HTML rather than dynamically loaded from an API or database
2. **Limited Interactivity** — Search functionality is not connected to actual data filtering; results must be wired to backend
3. **Placeholder Pages** — About, Help, and Donate pages are template files without full implementation
4. **No Backend Integration** — No server-side functionality; all features are front-end only
5. **Browser Compatibility** — Modern CSS features may not support older browsers (IE11 and below)

### Planned Enhancements

**Short-term:**

- Implement functional search filtering with JavaScript
- Complete About, Help, and Donate page content
- Add book detail modal/page with full descriptions
- Implement donation form with payment gateway integration

**Medium-term:**

- Connect to Project Gutenberg API or similar book database
- Add user authentication and reading history
- Implement wishlist/favorites functionality
- Add book recommendations based on user history

**Long-term:**

- Migrate to React/Vue.js for component reusability and state management
- Implement PWA functionality for offline reading
- Add dark mode toggle with persistent user preferences
- Build backend API with Node.js/Python for user data and book metadata
- Integrate e-reader functionality for browser-based book reading

### Technical Debt

- CSS could be modularized using BEM methodology for larger-scale projects
- JavaScript should be refactored into ES6 modules as functionality grows
- Consider build tooling (Webpack, Vite) as the project scales

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

The MIT License is a permissive open-source license that allows free use, modification, and distribution of this code for both commercial and non-commercial purposes, provided the license and copyright notice are included.

---

**Educational Purpose:** This redesign was created as part of a comprehensive web programming course focused on mastering front-end development. It demonstrates proficiency in HTML5, CSS3, vanilla JavaScript, and responsive design principles without relying on frameworks or preprocessors.

**Original Project:** This is a redesign of [Project Gutenberg](https://www.gutenberg.org), a remarkable volunteer-driven initiative digitizing public domain books since 1971.
