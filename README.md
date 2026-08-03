# RohrFix24 Website

A modern, production-ready corporate website for a German plumbing and heating service company.

## Project Goal

Build a high-quality commercial website that meets modern frontend development standards and is suitable for real-world production.

The project should look and feel like it was created by a professional digital agency rather than generated automatically.

## Target Audience

- Homeowners
- Apartment owners
- Property managers
- Small businesses
- Customers looking for plumbing, heating, emergency, and maintenance services

## Core Services

- Plumbing Installation
- Plumbing Repair
- Heating Installation
- Heating Repair
- Emergency Service (24/7)
- Pipe Repair
- Leak Detection
- Bathroom Renovation
- Maintenance

## Tech Stack

- HTML5
- CSS3
- Vanilla JavaScript

No frameworks.

## Development Principles

- Desktop First
- Pixel Perfect implementation
- Component-based architecture
- Strict BEM methodology
- Semantic HTML
- Responsive design
- Accessibility (WCAG)
- Performance-first approach

Detailed coding standards are defined in **AGENTS.md**.

## Project Structure

```
/
├── AGENTS.md
├── README.md
├── index.html
├── css/
│   ├── base/
│   ├── layout/
│   ├── components/
│   ├── sections/
│   └── main.css
├── js/
├── assets/
│   ├── images/
│   ├── icons/
│   └── fonts/
```

## Development Workflow

Development is performed in the following order:

1. Desktop
2. Tablet
3. Mobile

Each stage must be completed and approved before moving to the next one.

## Design Requirements

The provided design mockup is the single source of truth.

Implementation must reproduce the design as accurately as possible.

Do not modify:

- layout
- spacing
- typography
- component positions
- visual hierarchy
- proportions

If something does not fit, fix the implementation instead of changing the design.

## Quality Requirements

The final website must provide:

- clean architecture
- reusable components
- scalable codebase
- maintainable CSS
- high readability
- modern UX/UI
- excellent Core Web Vitals
- accessibility compliance

## Browser Support

- Chrome
- Edge
- Firefox
- Safari

Latest stable versions.

## Project Status

The Desktop, Tablet, and Mobile layouts are implemented. Desktop starts at `1024px` and keeps the complete horizontal navigation. Tablet covers `768px` through `1023px` and uses an accessible burger menu, a reduced content flow without Reviews, and the repeated Final CTA. Its Contact section keeps the written request form while omitting repeated contact details. Mobile covers widths below `768px`, follows the approved `390px` composition, and omits repeated Reviews, Contact, and Final CTA sections. Contact-form validation, responsive navigation, and the scroll-to-top control use minimal JavaScript.

The portfolio contact form sends a non-personal demo payload to `https://jsonplaceholder.typicode.com/posts`. Name, phone number, email, and message content remain in the browser and are not included in that test request. Replace the endpoint and payload mapping before production use.

## Component Reuse Check

The following fragment can be inserted into a separate test page without changing Header or Hero styles:

```html
<section class="section section--light">
  <div class="container">
    <div class="section-header">
      <p class="section-header__eyebrow">Test</p>
      <h2 class="section-header__title">Neue Sektion</h2>
      <p class="section-header__description">Testbeschreibung</p>
    </div>

    <a class="button button--primary" href="#">Mehr erfahren</a>
  </div>
</section>
```

This verifies that the shared layout and UI blocks do not depend on `.site-header` or `.hero` parent selectors.
