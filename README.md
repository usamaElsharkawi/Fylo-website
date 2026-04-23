# Project 5: Fylo Landing Page (Tailwind CSS v4 Oxide)

A high-fidelity landing page implementation focusing on modern CSS-in-CSS workflows, design token centralization, and professional theme management.

## 🧠 Deep-Dive Learnings (Product Engineering)

### 1. Tailwind CSS v4 Architecture
- **CSS-First Design**: Moved from JS-based configuration to centralized `@theme` blocks in CSS.
- **Custom Variants**: Implemented `@variant dark (&:where(.dark, .dark *))` to enable the Selector Strategy for theme toggling.
- **Asset Registration**: Integrated logos and background SVGs directly into the CSS theme layer as custom variables.

### 2. Modern Dark Mode Architecture
- **The "Zero-Flash" Problem**: Learned that `useEffect` in React or deferred scripts in Plain JS cause a white flash before the theme applies.
- **The Solution**: Used a **Blocking Synchronous Script** in the `<head>` (`theme-detect.js`) to apply the `.dark` class before the first paint.
- **Persistence**: Managed state with `localStorage` while ensuring the UI stays in sync with system preferences using `matchMedia`.

### 3. Browser Internals: Script Loading
- **Blocking (Standard)**: Use for critical path logic (like theme detection).
- **`defer`**: Use for non-critical interaction logic. It downloads in parallel and executes after parsing.
- **`async`**: Use for independent scripts (Analytics) that don't depend on the DOM.

### 4. Full-Stack Context (React & Next.js)
- Discussed the difference between Client-Side Hydration and **Server-Side Rendering (SSR)**.
- Explored why **Cookies** are the gold standard for Next.js dark mode to achieve zero-flash on the server.

---

*This repo serves as a living knowledge base for advanced frontend engineering patterns.*
