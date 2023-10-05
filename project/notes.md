# 7 Steps of a Web Project

1. Define
    - Who is the audience?
    - What is the purpose (business and user goals)?
2. Plan
    - What content is needed (media etc.)?
    - Sitemap (pages and hierarchy)
    - Sections in pages
    - Website personality
3. Sketch
    - Components
    - Layout patterns
    - Content guides the design
    - Sketches are quick and dirty
4. Design
    - Design the look and feel
    - Look at the sketches
    - color, typograhpy, images, icons, etc.
5. Test and optimize
    - Test with real users
    - Optimize for performance
    - Test with all browsers
    - Test with all devices
    - Accessibility
    - Lighthouse
    - SEO
6. Launch
7. Maintain
    - Analytics


## RESPONSIVE DESIGN:
- Fluid layouts
    - can adapt to any screen size
    - use relative units (vw, vh, %, em, rem [for length], etc.)
    - use max-width instead of width
- Media queries
    - @media
    - change styles depending on breakpoints
- Responsive images
    - % and max-width
- Responsive units
- Desktop-first vs. mobile-first
    - Desktop-first: start with desktop styles and then use media queries to add styles for smaller screens
    - Mobile-first: start with mobile styles and then use media queries to add styles for larger screens
    - More modern approach to do mobile-first
    
### REM and MAX-WIDHT
- REM: relative to the font-size of the root element
    - If no font-size is set, the default browser one is usually 16px (in html)
- MAX-WIDTH: max-width: 100% will make the image responsive
    - Makes no sense using it with a relative unit like rem