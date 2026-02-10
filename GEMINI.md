# Project Context: AI Dev Practices Presentation

## Overview
This project contains a browser-based presentation deck titled "Mastering the AI-Assisted Development Workflow". It is a static site designed to be hosted on GitHub Pages (served from the `docs/` directory).

The presentation engine is a lightweight, custom HTML/JS viewer that renders SVG files as slides. This allows for high-quality, scalable graphics and easy editing of individual slides as code.

## Directory Structure
*   **`docs/`**: The web root for the presentation.
    *   **`index.html`**: The presentation player. Contains the viewer logic, styling, and configuration.
    *   **`slide_*.svg`**: Individual slide files. Numbered sequentially (e.g., `slide_1.svg`, `slide_2.svg`).

## Key Files
*   **`docs/index.html`**: The main entry point.
    *   **Critical Config**: Contains a JavaScript variable `const totalSlides` which **MUST** be updated manually whenever slides are added or removed.
*   **`README.md`**: Contains the link to the live presentation.

## Usage & Development

### Running Locally
To view the presentation locally, start a simple HTTP server pointing to the `docs/` directory.
```bash
# Using Python 3
python3 -m http.server 8000 --directory docs
```
Then visit `http://localhost:8000` in your browser.

### Adding or Reordering Slides
1.  **Create/Rename File**: Save the new slide as `docs/slide_N.svg`, where `N` is the slide number.
    *   Ensure all slides are numbered sequentially without gaps.
    *   If inserting a slide, you must rename all subsequent slides (e.g., `mv slide_10.svg slide_11.svg`).
2.  **Update Configuration**: Open `docs/index.html` and update the `totalSlides` constant to match the new total count.
    ```javascript
    const totalSlides = 12; // Example: Updated from 11
    ```

### Navigation Controls
*   **Next Slide**: `Right Arrow`, `Space`, `Enter`
*   **Previous Slide**: `Left Arrow`
*   **Fullscreen**: `f` or `F` (or use the "Present" button)

## Styling & Conventions
*   **Visual Theme**: Dark mode (`#1e1e2e` to `#2d2b55` gradient).
*   **Typography**: `Roboto` font family.
    *   Header: Bold, 72px-80px, `#61afef` (Blue).
    *   Headline: Regular, 48px, White.
    *   Bullets: Light, 36px, `#dcdfe4`.
    *   Accents: `#e5c07b` (Gold/Yellow) for emphasis and key visual elements.
*   **SVG Structure**: Each slide is a standalone SVG (1920x1080 viewBox). Styles are embedded within `<defs>` in each file.
