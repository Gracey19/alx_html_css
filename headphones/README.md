code README.md
# Headphones Landing Page

This project is a pixel-perfect implementation of a designer’s vision using only HTML and CSS. It was built as part of the ALX Front-End Software Engineering program.

## Figma Reference
Design file duplicated from [Headphones UI by Nicolas Philippot](https://www.figma.com/design/AEp29lQqvuLLai2ITY5cer/a5366bbd595c643993665e2a28909370a7e12c66?node-id=0-2&t=ccYdS1QmrMAXRqgm-0)

## Tools Used
- VS Code
- Git Bash
- Figma (Inspect mode)
- Fonts: Source Sans Pro, Spin-Cycle-OT

## Responsive Design
- Mobile layout activates at screen width ≤ 480px
- Max content width: 1000px, centered
- Hover/active styles:
  - Links: `#FF6565`
  - Buttons: `opacity: 0.9`

## Validation
- HTML and CSS validated using [W3C Validator](https://validator.w3.org/)
- Accessibility checked with semantic tags and label usage

## Screenshots
_Add screenshots of desktop and mobile views once you finish the build._

## Notes
- Some Figma values were rounded for cleaner CSS
- No external frameworks or libraries used
- All assets sourced from ALX-provided archives

## TROUBLESHOOTING JOURNAL

### Font Weight Override Due to Semantic Tag Mismatch

**Issue:**  
Both paragraphs inside the `.hero` section were rendering with the same font weight—either both bold or both regular—despite having distinct classes (`.hero-lead` and `.hero-description`) and separate font-weight declarations.

**Cause:**  
The container was opened with `<div class="hero">` but closed with `</section>`, creating a semantic mismatch. This disrupted the cascade and caused unexpected inheritance behavior, making class-specific styles ineffective.

**Fix:**  
- Replaced `<div>` with `<section>` to match semantic intent and closing tag.
- Applied unique classes to each paragraph:
  ```html
  <p class="hero-lead">High-quality headphones for your everyday life.</p>
  <p class="hero-description">Lorem ipsum dolor sit amet...</p>

Scoped font weights explicitly in CSS:
.hero-lead {
  font-family: 'Source Sans Pro', sans-serif;
  font-weight: 700;
}

.hero-description {
  font-family: 'Source Sans Pro', sans-serif;
  font-weight: 400;
}

Validation:

Verified font rendering in DevTools → Computed styles.

Confirmed correct font files loaded in Network tab.

Ensured spacing and layout matched Figma spec.

Lesson Learned:

Even with perfect CSS, a mismatched semantic tag can hijack your cascade. Always validate your opening and closing tags—especially when using semantic containers like <section>, <article>, or <main>.

## Author
Grace Wesonga – Junior Developer, ALX FE SE Program

### Task 0: Header and Hero Section

### Task 1: Navigation and Hero Text

### Task 2: What We Do Section

### Task 3: Our Results Section

- Implemented red pentagon layout with +2% and caption text
- Applied Source Sans Pro Regular 14px for caption
- Added background image (`headphones_hero_2.jpg`) for visual depth
- Increased spacing between pentagons and heading for clarity

### Task 4: Contact Us Section

Implemented a clean, responsive contact form based on the Figma design:

-Added labeled fields for **Name**, **Email**, and **Message**
-Styled inputs and textarea using Source Sans Pro, 14px
-Designed a bold red **“CALL TO ACTION”** button with hover effect
-Ensured mobile responsiveness at screen width ≤ 480px
-Applied semantic HTML tags and `required` attributes for basic validation

This section balances clarity, accessibility, and editorial polish—ready for real-world client use.

### Task 6: Replace Background Image with Code

Replaced the image-based layout in the “Our results” section with pure HTML and CSS pentagons:

-Drew each pentagon using `clip-path: polygon(...)`—no image files used
-Styled percentage values (`+2%`) and caption text (`Lorem ipsum dolor`) inside each shape
-Applied `Source Sans Pro` with SemiBold for headings and Regular 14px for labels
-Used Flexbox for responsive layout and spacing
-Removed `headphones_hero_2.jpg` and replaced with solid background color `#071629`

This implementation meets ALX’s requirement for semantic structure and image-free geometry, while preserving editorial clarity and visual impact.

### Task 8: Hamburger Menu Implementation

Enhanced mobile responsiveness by adding a hamburger menu using pure JavaScript:

- Replaced navigation links with a hamburger icon on screens ≤ 480px
- Toggled menu visibility with smooth transitions using `classList.toggle('active')`
- Styled the icon using three stacked `<span>` bars with Flexbox and transitions
- Ensured accessibility and responsiveness across screen sizes
- No frameworks used—pure HTML, CSS, and JavaScript

This final task completes the ALX Front-End HTML & CSS block, demonstrating mastery of layout, animation, and responsive design.

