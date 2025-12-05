# PROJECT 3: BINDING
**Typography &amp; Interaction I, Fall 2025**

# Rethinking Graphic Design History - A Digital Mini-Book

For the third project for Typography & Interaction, I created a multi-page "binding" of digital articles exploring three perspectives on design history education.

## Overview

This project consists of three texts that challenge traditional approaches to graphic design history, including my chosen reading from Project 1:

1. **"Knowing Your Design History Is Crucial to Aesthetic Innovation"** by Kristen Coogan: Explores how understanding historical style cycles informs contemporary design innovation.
2. **"We Need Graphic Design Histories That Look Beyond the Profession"** by Aggie Toppins: Advocates for expanding design history beyond the profession to include cultural and social contexts.
3. **"Can We Teach Graphic Design History Without the Cult of Hero Worship?"** by Aggie Toppins: Questions the traditional focus on individual "design heroes" in favor of contextual understanding.

## Design Inspiration

The visual design is inspired by *[Geronimo Stilton](https://embed.cdn.pais.scholastic.com/v1/channels/tso/products/identifiers/isbn/9780545307710/alternate/0/renditions/500)* children's books, which use playful typography and engaging visual hierarchies to make reading more dynamic and entertaining.

## Concept

### Typography
- **Instrument Sans** (variable font): Primary body text
- **Instrument Serif**: Headings and emphasis
- Font faces loaded via `@font-face` in CSS files

### Responsive Design
- Mobile-first approach with main breakpoints at 500px and 850px, few at 415px
- Responsive typography scaling across devices, checking for legibility
- Adaptive + experimental grid layouts for optimal reading experience (I saw a good amount of mobile articles laid out in single-column, so I wanted to try switching it to multi-column layouts. And for desktop dimensions, I wanted to introduce single-column layouts rather than various multi-column ones, essentially reversing what I typically expect from today's online articles and their responsive forms.)


### Visual Elements

#### Color System
Three distinct cool color palettes for each article:
- **Style Cycles**: Green palette (`#c6e3c7`, `#87BBA1`, `#47928b`, `#1c6364`, `#162E30`)
- **People's Design**: Teal palette (`#D4F6F5`, `#87AFBB`, `#3A7485`, `#0C4655`, `#132228`)
- **De-heroizing**: Blue palette (`#D4E9F6`, `#879ABB`, `#3A4F85`, `#012B62`, `#161328`)


#### Decorative Patterns
CSS-generated geometric patterns for visual interest:
- **Circular CSS background patterns**: [CSS Pattern Generator](https://css-pattern.com/)




#### SVG Animation

- **Rotating book stack SVG on homepage**: [SVGRepo - Books Stack Icon](https://www.svgrepo.com/svg/94674/books-stack-of-three)
- Infinite **rotating animation** with responsive scaling - tutorial from [SVG Tutorial](https://svg-tutorial.com/svg/css-animation)

### Interactive Typography

Inspired by Geronimo Stilton's expressive text treatments:

- **`.slant` / `.slant2`**: Slightly rotated text for emphasis
- **`.stroke`**: Text with thin stroke outline
- **`.shadow`**: Drop shadow effect
- **`.space`**: Letter-spaced italic text
- **`.shimmer`**: Animated gradient text effect - inspiration from [Julien Thibeaut](https://ibelick.com/blog/create-animated-text-gradient-with-css)
- **`.geronimo`**: Orange serif text format - dedicated to Geronimo Stilton

### Navigation
- Home page navigation banners with color-coded sections
- Top navigation bar with theme titles for each respective article
- Active state indicators
- Clean hover states
- Simpler footer navigation bar for easy navigation to the top of the article or the home page

### Layout Features
- Sticky numbered/lettered labels for paragraph navigation
- Highlighted (`<mark>`) for key concepts
- Italicized (`<em>`) for emphasis on certain key terms/words
- Pull quotes with custom styling + alignment changes based on device dimensions
- Grid-based layouts, with multi-column layout on smaller screens and single-column layout on larger screens



## DOM Elements
### Structural Elements
- `<header>`
    - Contains site hero and article titles
    - Houses SVG graphic on home page and primary headings, like author and published date

- `<main>`
    - Contains navigation, articles, and figures

- `<article>`
    - Semantic wrapper for essay content

- `<section>`
    - Groups related content thematically
    - `.para` sections create reading rhythm
    - `.intro` and `.colophon` provide framing content on home page

- `<nav>`
    - Primary navigation in header
    - Footer navigation for article traversal
    - Unordered lists for semantic navigation menu structure

- `<footer>`
    - Copyright information
    - Secondary navigation
    - Consistent across all pages

### Content Elements
- `<h1>`: Page/article title (one per page)
- `<h2>`: Not used (intentional flat hierarchy)
- `<h3>`: Section subheadings on homepage
- Nested `<span>` elements for color differentiation

### Typography Elements

- `<p>`: Paragraphs with various classes (`.pg`, `.context`, `.label`)
- `<em>`: Semantic emphasis in italics
- `<mark>`: Highlighted phrases for visual + semantic importance
- `<blockquote>`: Pull quotes from article text
- Custom `<span>` classes for decorative typography

### Links
- `<a>`
    - Navigation between pages and file directory
    - External attribution links in `<figcaption>`
### External Media

- `<svg>`: Inline animated book stack icon for home page decoration
- `<img>`: Cover image with lazy loading that speaks to all three article themes
- `<figure>` + `<figcaption>`: Semantic image structure

### Class Naming Conventions

- `.dark-line`, `.line`: Decorative banner separators
- `.title-sec`: Title section container
- `.og-text`: Original publication info
- `.context`: Article introduction quote
- `.para`: Paragraph container with grid layout
- `.pg`: Paragraph text content
- `.bq`: Blockquote
- `.label`: Sticky numbered/lettered labels
- `.intro`, `.colophon`: Homepage sections


## CSS

### Reset.css
*Based on [The New CSS Reset](https://github.com/elad2412/the-new-css-reset) by Elad Shechter*

### Modern CSS Features
- CSS Grid for complex layouts
- CSS Custom Properties (variables) for theming
- Container queries with `@media`
- CSS animations and transforms
- Logical properties (`margin-block`, `padding-inline`)
- `text-wrap: balance` and `text-wrap: pretty` for optimal text breaks

### Accessibility Considerations
- Semantic HTML structure
- Sufficient color contrast ratios
- Responsive font sizing
- CSS document with heading hierarchy

## Image Credits

### Image: 
*"What is Design?" Poster of Elena Pacenti's Work*
- **Source**: Instagram [@thecharliefund](https://www.instagram.com/thecharliefund)
- Exploring multiple definitions of design


## Credits

### Original Essay Authors:
- Kristen Coogan: ["Knowing Your Design History is Crucial to Aesthetic Innovation"](https://eyeondesign.aiga.org/knowing-your-design-history-is-crucial-to-aesthetic-innovation/)
- Aggie Toppins: ["We Need Graphic Design Histories That Look Beyond the Profession"](https://eyeondesign.aiga.org/we-need-graphic-design-histories-that-look-beyond-the-profession/)
- Aggie Toppins: ["Can We Teach Graphic Design History Without the Cult of Hero Worship?"](https://eyeondesign.aiga.org/can-we-teach-graphic-design-history-without-the-cult-of-hero-worship/)
