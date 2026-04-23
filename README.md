# Project Fylo - Dark Theme Landing Page

## Overview
Fylo is a secure file storage landing page. This project focuses on high-fidelity design, custom Tailwind v4 tokens, and responsive layouts.

## Technical Stack
- **HTML5**: Semantic structure.
- **Tailwind CSS v4 (Oxide)**: Modern styling with CSS variables.
- **Fonts**: Raleway (Headings), Open Sans (Body).

## Roadmap & Progress

### Sprint 1: The Foundation (Header & Hero)
- [x] Initialize Git Repository and `.gitignore`.
- [x] Configure Google Fonts (Raleway, Open Sans).
- [x] Implement responsive Header with Logo and Navigation.
- [x] Implement Hero section with Introduction Illustration.
- [x] Integrate "Curvy" background transition.
- [x] Design custom Gradient CTA button.

---

## Reflections & Deep Dives

### The "Curvy" Transition
In this sprint, we addressed the non-rectangular transition between the Hero and the Main content. Instead of complex CSS `clip-path` which can be hard to maintain, we used a dedicated `div` with:
1.  **Background SVG**: Applied the curvy desktop/mobile SVG.
2.  **Negative Margins**: Used `-mt-24` to pull the curve up into the Hero's space, creating a seamless visual flow.
3.  **Responsive Art Direction**: Leveraged Tailwind v4's breakpoint tokens (`md:bg-curvy-desktop`) to switch the curve shape based on screen width.

### Design Tokens (Tailwind v4)
We leveraged the `@theme` block in `input.css` to define our brand palette:
- `dark-blue-intro`: Lighter shade for the top hero area.
- `dark-blue-main`: Darker shade for the main content.
- `btn-gradient`: A composite class combining `from-cyan` and `to-blue`.
