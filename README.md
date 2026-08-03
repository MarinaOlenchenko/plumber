# RohrFix24

Responsive portfolio website for a fictional German plumbing and heating service company.

I implemented the project from approved Desktop, Tablet, and Mobile design references. The main goals were accurate design reproduction, reusable component architecture, accessible interactions, and stable responsive behavior across different screen sizes.

The website content is written in German and presents emergency plumbing services, installation, repair, heating maintenance, bathroom renovation, and customer contact options.

## My Contribution

- Translated the provided layouts into semantic HTML.
- Built the interface using reusable BEM components.
- Implemented separate Desktop, Tablet, and Mobile layouts.
- Created a scalable SCSS architecture for components, sections, and layout utilities.
- Centralized all breakpoints, media queries, and responsive mixins.
- Implemented an accessible responsive navigation menu.
- Added form validation for names, phone numbers, email addresses, required fields, and privacy consent.
- Added loading, error, and success states to the contact form.
- Implemented hover, focus-visible, active, and disabled states for interactive controls.
- Added a smooth scroll-to-top control.
- Optimized images with local AVIF and WebP sources.
- Added basic SEO metadata, Open Graph data, and structured data.
- Tested the layout for horizontal overflow, element collisions, broken images, and keyboard interaction.

## Main Features

- Emergency service and appointment call-to-action elements.
- Service overview with reusable cards and custom icons.
- Company advantages and trust indicators.
- About section with responsive imagery.
- Step-by-step service process.
- Customer reviews.
- Contact form with custom client-side validation.
- Responsive Header and Footer.
- Smooth navigation and scroll behavior.
- Accessible focus management and reduced-motion support.

## Responsive Design

The project follows a Desktop-first workflow:

- **Wide Desktop:** `1280px` and above.
- **Compact Desktop:** `1024px` to `1279.98px`.
- **Tablet:** `768px` to `1023.98px`.
- **Mobile:** below `768px`.

Wide Desktop styles are defined in the component partials. All responsive overrides, breakpoint variables, and mixins are located in one file:

```text
scss/responsive/_responsive.scss
```

This makes it possible to adjust responsive boundaries without searching through individual components.

## Architecture

```text
/
|-- assets/
|   |-- icons/
|   `-- images/
|-- css/
|   `-- main.css
|-- js/
|   `-- main.js
|-- scss/
|   |-- base/
|   |-- components/
|   |-- layout/
|   |-- responsive/
|   |-- sections/
|   `-- main.scss
|-- index.html
|-- package.json
`-- README.md
```

SCSS files are the source of truth. The browser uses the compressed and generated `css/main.css` file.

Components are independent and can be added, removed, or reused without relying on parent section selectors.

## Technologies

- HTML5
- SCSS and CSS3
- CSS Grid
- Flexbox
- BEM methodology
- Vanilla JavaScript
- Dart Sass
- Prettier
- Git and GitHub

No frontend frameworks or UI libraries are used.

## Accessibility

- Semantic document structure.
- Logical heading hierarchy.
- Descriptive image alternative text.
- Visible keyboard focus states.
- Keyboard-accessible navigation.
- Accessible form labels and error messages.
- Comfortable touch targets for interactive controls.
- Reduced-motion support.
- ARIA attributes for dynamic interface states.

## Local Development

Install the development dependencies:

```bash
npm ci
```

Compile SCSS into compressed CSS:

```bash
npm run build:css
```

Watch SCSS files during development:

```bash
npm run watch:css
```

Format SCSS source files:

```bash
npm run format:scss
```

Open `index.html` through a local development server after building the styles.

## Demo Limitations

This is a portfolio project rather than a commercial website.

- The contact form uses a public test endpoint.
- Personal form values are not included in the demo request and are not stored.
- Contact details and company information are fictional.
- Some links are included to demonstrate interface states and navigation structure.
- A real production version would require a private backend, spam protection, legal review, and real business data.

## Repository

[github.com/MarinaOlenchenko/plumber](https://github.com/MarinaOlenchenko/plumber)
