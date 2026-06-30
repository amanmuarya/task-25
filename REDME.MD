# FlowApp Landing Page

A single-page SaaS landing page built with Tailwind CSS (CDN build) —  only built-in Tailwind utility classes.

## Structure
1. **Navigation** — fixed glassmorphism navbar (`backdrop-blur`, `bg-white/5`, `border-white/10`)
2. **Hero** — headline, subhead, CTA buttons, dashboard preview card
3. **Features** — bento-style grid (`md:col-span-2 md:row-span-2` for the large card)
4. **Testimonials** — 3-column glass card grid, middle card offset with `md:-translate-y-8`
5. **Call to action** — gradient background section with two buttons
6. **Footer** — link columns + social icons

**Continuous/ambient** — `animate-bounce`, `animate-pulse`, `animate-spin` (Tailwind's four built-in keyframe animations are `spin`, `ping`, `pulse`, `bounce`; nothing else is used).

**Entrance/stagger** — elements tagged `.reveal` start at `opacity-0 translate-y-8`. A short inline script removes those classes and adds `opacity-100 translate-y-0` once on `DOMContentLoaded`. The actual stagger comes from each element's own `transition-all duration-700 delay-{100|150|200|300|500}` classes — the script just triggers all of them at once, it doesn't control timing itself.

**Hover** — `hover:scale-105` / `hover:scale-110`, `hover:-translate-y-1`, `hover:rotate-2` / `hover:-rotate-2`, combined with `transition` / `transition-all` / `transition-transform`.

## Known limitations of the "stock utilities only" constraint

- `animate-spin` only runs at Tailwind's default ~1s speed. There's no built-in slower variant without an arbitrary-value override (`duration-[Nms]`), which was avoided here since arbitrary values blur the line with "custom CSS." A large decorative ring at full spin speed looked bad, so it was dropped rather than forced.
- There's no built-in equivalent to a smooth vertical "float" loop — `animate-bounce` is the closest stock option, but it's a sharper motion than a true float.
- 3D transforms (`rotate-x`, `rotate-y`, `perspective`) aren't part of stock Tailwind utilities, so any "tilt on hover" effect is limited to 2D `scale`/`translate`/`rotate`.

## Files

- `flowapp-fixed.html` — the page  

## how to run 
   - live service = chorem , eadg .. 