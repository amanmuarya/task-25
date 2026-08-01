
# FlowApp — Animated SaaS Landing Page
 
A single-file, animation-rich landing page for **FlowApp**, a fictional SaaS platform for AI-powered automation, real-time collaboration, and analytics. Built with plain HTML and Tailwind CSS (via CDN) — no build step, no external CSS frameworks, no dependencies to install.
 
There is nothing to install — Tailwind CSS and the Google Fonts (`Outfit`, `Inter`) load from CDN at runtime, so an internet connection is required the first time the page loads.
 
## File structure

index.html   →  everything: markup, Tailwind config, custom CSS, and JS all in one file
 
Keeping it single-file makes the page trivially portable — drop it on any static host (Netlify, Vercel, GitHub Pages, S3) with zero configuration.
 
 
## Custom animation system
 
All keyframes and animation utilities are declared in the inline `tailwind.config` `theme.extend` block at the top of `index.html`
 
Stagger timing (e.g. the hero headline lines appearing in sequence) is done with Tailwind's arbitrary-value syntax directly in the markup, e.g.:
 
<span class="animate-slide-up [animation-delay:220ms]">...</span>
 
Scroll-triggered reveals for the features, testimonials, and CTA sections are handled by a small `IntersectionObserver` script near the end of the file — elements start with the `.reveal` class (`opacity: 0`, translated down) and get `.in-view` added once they enter the viewport.

## Customization guide
 
**Colors / gradients** — the core palette (violet → fuchsia → cyan) is applied directly via Tailwind gradient utilities (`from-violet-500 via-fuchsia-500 to-cyan-400`, etc.) rather than custom color tokens, so you can restyle by swapping those class names throughout. The dark background scale (`space-950` → `space-700`) is defined in `tailwind.config.theme.extend.colors`.
 
**Fonts** — `Outfit` (display/headings) and `Inter` (body) are loaded from Google Fonts in the `<head>` and mapped to `font-display` / `font-body`(default) via `tailwind.config.theme.extend.fontFamily`.
 
**Copy** — all headline, body, and testimonial text is plain fictional placeholder content; search-and-replace directly in the markup.
 
**Sections** — each section is a clearly commented ` so you can reorder, duplicate, or remove sections independently.
 
**Pricing section** — a "Pricing" nav link is included but currently points to an empty `#pricing` anchor, since no pricing section content was part of the original spec. Add a `<section id="pricing">` block following the same pattern as the others to wire it up.
 
## Accessibility & performance notes
 
- Respects `prefers-reduced-motion`: animation and transition durations collapse to near-zero for users who have that OS/browser setting enabled.
- Visible focus rings (`:focus-visible`) on interactive elements for keyboard navigation.
- Semantic landmarks (`<header>`, `<nav>`, `<section>`, `<footer>`) throughout.
- No images are loaded from external sources — the dashboard mockup and avatars are built with CSS/SVG, keeping the page fast and license-free.
 
## Browser support
 
Uses modern CSS (`backdrop-filter`, CSS `mask-image`, CSS `perspective`) — best viewed in a recent version of Chrome, Edge, Safari, or Firefox. `backdrop-filter` (used for the glassmorphism effect) require.
 
