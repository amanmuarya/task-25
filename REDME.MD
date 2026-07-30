#  Greenwood Library Website - Student Project

##  Overview
This project is a modern, minimal, editorial-style landing page built for the fictional **Greenwood Public Library**. I created this project to practice advanced UI/UX design patterns, complex grid structures, and interactive animations using pure **HTML5** and **Tailwind CSS**.

##  Learning Process & What I Mastered

During the development of this project, I focused on moving beyond basic layouts and challenged myself with modern web design trends:

### 1. Advanced Grid Layouts (Bento Grid)
- Learned how to build an **asymmetrical Bento-style grid** using Tailwind's `col-span` and `row-span` utilities.
- Implemented responsive column shifting from 1 column on mobile to 2, 3, and 4 columns on larger screens (`grid-cols-1 md:grid-cols-2 lg:grid-cols-4`).

### 2. Custom Tailwind Configurations via CDN
- Figured out how to extend the default Tailwind theme directly in the HTML `<head>`.
- Wrote custom keyframes (`fadeUp`) and animation classes to create a **staggered entry animation** when the page loads.

### 3. Interactive Hover Effects & Pseudo-elements
- **Animated Underlines:** Used pseudo-elements (`after:absolute after:bottom-0 after:w-0 hover:after:w-full`) for smooth navbar link hovers.
- **Image Zoom:** Wrapped images in `overflow-hidden` containers and applied `group-hover:scale-105` with a long transition duration (`duration-700`) to create premium, cinematic image scaling.
- **Grayscale Transitions:** Used `grayscale hover:grayscale-0` on the testimonial avatar.

### 4. Editorial Typography & Layout
- Applied `text-balance` and tight tracking (`tracking-tighter`) to large hero headers to mimic newspaper and magazine aesthetics.
- Used Tailwind's CSS column utilities (`columns-1 sm:columns-2`) in the About section to create a multi-column reading experience without needing flexbox or grid.

##  Project Structure (Step-by-Step Build)

1. **Navigation:** Sticky top bar with backdrop blur (`backdrop-blur-md`).
2. **Hero Section:** Large typography, staggered text fade-in, and a 4-column data stats row.
3. **Collections Grid:** Interactive cards with subtle, distinct pastel background changes on hover (`hover:bg-emerald-50`, `hover:bg-amber-50`).
4. **Gallery Spaces:** Image grid with gradients and bottom-left caption tags.
5. **Values Bento Grid:** Complex spanned layout highlighting library perks.
6. **Membership Tiers:** Responsive pricing cards featuring an absolute positioned "Popular" badge and list items.
7. **Testimonial:** Centered layout emphasizing the grayscale-to-color transition.
8. **Contact Block:** A rounded, tinted CTA container for address and hours.
9. **Events:** Blog-style card grid for upcoming workshops.
10. **Footer:** Clean 4-column link structure with social SVGs.

## 🚀 How to Run

Since this project relies entirely on HTML and the Tailwind CSS CDN, there is no build step required!

1. Download or clone this repository.
2. Open the `index.html` file directly in any modern web browser.
3. Ensure you have an active internet connection so the Tailwind CDN script and Unsplash images can load.

## 🛠️ Tech Stack
- **HTML5**
- **Tailwind CSS (CDN)**
- Google Fonts (System UI fonts fallback)
- Unsplash (Placeholder imagery)