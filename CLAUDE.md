# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

PDFe is a simple web application that displays a church's Statement of Faith (Declaración de Fe) for Iglesia Bautista Filadelfia Curicó. The project consists of a single HTML file that presents 18 articles of faith with interactive features.

## Project Structure

```
PDFe/
├── index.html          # Main HTML file with embedded CSS and JavaScript
└── pdf/               # Directory containing PDF documents
    └── Declaracion_de_Fe_Iglesia_Bautista_Filadelfia ver 2.pdf
```

## Development Environment

This is a static web project with no build process, package manager, or dependencies. The project uses vanilla HTML, CSS, and JavaScript.

### Running the Project

Since this is a static HTML file, you can:
- Open `index.html` directly in a web browser
- Use a local web server: `python -m http.server 8000` (Python 3) or `python -m SimpleHTTPServer 8000` (Python 2)
- Use VS Code Live Server extension

### No Build/Test/Lint Commands

This project has no:
- Package.json or build configuration
- Testing framework
- Linting tools
- Package manager dependencies

## Technical Architecture

### Single Page Application Structure

The application is built as a single HTML file with:

1. **Embedded CSS**: All styling is contained within `<style>` tags in the HTML head
   - Uses CSS Grid for responsive layout (`beliefs-grid`)
   - Custom CSS animations and transitions
   - Mobile-first responsive design with multiple breakpoints
   - Dark color scheme with gradients

2. **Interactive JavaScript Features**:
   - Tooltip system for Bible verse references (`verse-reference` elements)
   - Intersection Observer for scroll animations
   - Keyboard accessibility support
   - Smooth scrolling behavior

3. **Content Structure**:
   - Header with church name and title
   - 18 belief cards in a responsive grid layout
   - Each belief card contains:
     - Numbered badge
     - Title and content
     - Bible verse references with hover tooltips

### Key CSS Classes and Components

- `.belief-card`: Individual faith statement cards
- `.verse-reference`: Interactive Bible verse tags with tooltips
- `.tooltip`: Dynamically positioned tooltip for verse content
- `.beliefs-grid`: CSS Grid container for responsive layout

### JavaScript Functionality

- **Tooltip System**: Shows Bible verse text when hovering over references
- **Scroll Animations**: Cards animate in when scrolled into view
- **Accessibility**: Keyboard navigation support for tooltips
- **Responsive Positioning**: Smart tooltip positioning that avoids screen edges

## Content Management

The 18 articles of faith are hardcoded in HTML. To modify content:
1. Edit the HTML directly in `index.html`
2. Each belief is in a `.belief-card` div with numbered structure
3. Bible verses are in `data-verse` attributes of `.verse-reference` spans

## Language and Styling

- Content is in Spanish
- Uses Times New Roman font family for traditional appearance
- Color scheme: Dark grays (#111827, #374151) with white backgrounds
- Responsive design supports mobile, tablet, and desktop viewports