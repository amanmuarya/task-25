
# FlowApp - Modern SaaS Platform Landing Page 🚀

A sleek, high-conversion landing page template designed for modern SaaS products. Built entirely with HTML5 and Tailwind CSS, this template features cutting-edge UI/UX patterns including 3D transforms, glassmorphism, glowing ambient backgrounds, and bento-grid layouts.

## Features

*   **Modern Hero Section**: Animated background gradients and ambient light blobs.
*   **3D Dashboard Preview**: A perspective-tilted UI mockup with floating, animated metric cards (Tasks, Project Status, Team Activity).
*   **Glassmorphism Effects**: Frosted glass navigation bars and floating cards using Tailwind's `backdrop-blur`.
*   **Bento Grid Layout**: A highly visual, responsive asymmetric grid for showcasing product features.
*   **Custom Animations**: Custom Tailwind keyframes for floating elements, morphing shapes, and smooth scroll reveals.
*   **Fully Responsive**: Flawless display across mobile, tablet, and desktop viewports.
*   **Zero Build Step**: Runs directly in the browser via Tailwind CSS CDN.

##  Tech Stack

*   **HTML**: Semantic markup for structure.
*   **Tailwind CSS**: Utility-first CSS framework (loaded via CDN for instant prototyping).
##  Quick Start

Because this project uses the Tailwind CSS CDN, there is no build process, `npm install`, or complex setup required.




##  Customization

The Tailwind configuration is embedded directly in the `<head>` of the HTML file. You can easily tweak the theme colors, animations, and keyframes by modifying the `tailwind.config` script:

```html
<script>
    tailwind.config = {
        darkMode: 'class',
        theme: {
            extend: {
                colors: {
                    slate: { 950: '#020617' }
                },
                animation: {
                    'float': 'float 6s ease-in-out infinite',
                    // Add your custom animations here
                }
            }
        }
    }
</script>