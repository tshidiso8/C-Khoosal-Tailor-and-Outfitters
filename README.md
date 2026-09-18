C Khoosal Tailor and Outfitters — Website (Part 2)

A multi-page website for C Khoosal Tailor and Outfitters, a clothing and tailoring
store based in Fordsburg, Johannesburg. Part 1 built the site's HTML structure and
content; Part 2 implements the CSS styling, responsive design, and the corrections
raised in the Part 1 feedback.

 Pages

| Page | File | Description |
|---|---|---|
| Homepage | `index.html` | Store introduction, hero image, and brand strip |
| Explore | `lists.html` | Product catalogue grouped by brand, plus payment methods |
| About | `table.html` | Store description and an embedded map/store locator |
| Enquiries | `enquiries.html` | New in Part 2. General enquiry form and direct contact details |
| Registration | `registration.html` | Customer sign-up form |

 Technologies Used

 HTML5 — semantic page structure
 CSS3 — a single external stylesheet (`style.css`), including CSS Grid, Flexbox,
  custom properties (design tokens), pseudo-classes, and media queries
Google Fonts — Archivo (headings) and Inter (body text)

 Project Structure

C Khoosal Tailor and Outfitters/
├── index.html
├── lists.html
├── table.html
├── enquiries.html
├── registration.html
├── style.css
├── README.md
├── screenshots/                 (responsive-design evidence)
├── IMAGES/                      (logos)
├── stock clothing images/       (Dickies)
├── Lacoste stock clothing/
├── Converse stock clothing/
├── Carvela stock clothing/
├── Bishop stock clothing/
├── NAVADA stock clothing/
└── LOGO for payment methods/
```

 Part 2 — What Was Added

 1. External stylesheet & base styles
- Created a single external stylesheet, `style.css`, linked from every HTML page.
- Established design tokens (`:root` custom properties) for colour, font family,
  border radius, shadow and content width, so the whole site shares one consistent
  palette and rhythm.
- Set a base font, font size, line-height and colour scheme, and a shared
  margin/padding reset (`box-sizing: border-box`).

 2. Typography
- Applied `font-family`, `font-weight`, `line-height` and `letter-spacing` rules to
  headings and body text, using a display typeface (Archivo) for headings and a
  readable body typeface (Inter) for paragraphs and form fields.
- Used a type scale (`clamp()` on headings) so heading sizes adjust smoothly between
  mobile and desktop rather than jumping at fixed breakpoints.

 3. Layout
- Built the navigation bar, product grid, brand-logo grid, payment-logo grid and the
  new Enquiries layout with CSS Grid and Flexbox (`display: grid`/`flex`,
  `grid-template-columns`, `justify-content`, `align-items`, `flex-direction`).
- Kept a consistent `max-width` content column across pages via the `--content-width`
  token, so text and grids stay readable on wide screens.

4. Visual styling
- Styled cards, buttons, form fields and the sticky navigation bar with `color`,
  `background-color`, `border`, `border-radius` and `box-shadow`.
- Added interactive states with `:hover`, `:focus-visible` and `:active` on
  navigation links, product cards, brand logos and form buttons, so the site gives
  clear visual feedback without any JavaScript.

5. Responsive design
- Defined two breakpoints (`900px` and `600px`, plus a `400px` fallback for the
  product grid) using `@media` queries.
- The product grid, brand-logo grid and Enquiries layout reflow from a multi-column
  desktop layout down to a single/two-column mobile layout.
- Used relative units (`rem`, `em`, `%`, `clamp()`) throughout for font sizes,
  spacing and widths so elements scale rather than break.
- Images use `max-width: 100%` and `object-fit` so they never overflow their
  container on smaller screens.
- Verified the layout using resized browser windows at desktop, tablet and mobile
  widths — see [Screenshots](#screenshots) below.

 6. New Enquiries section
- Added a dedicated Enquiries page (`enquiries.html`) and linked it from the
  navigation bar on every page.
- Includes a general enquiry form (name, email, phone, subject dropdown, message)
  styled consistently with the existing Registration form, plus a contact card
  with the store's phone number, email and location for anyone who prefers not to
  use the form.
- Linked from the homepage "Contact Us" band as an additional call to action.

 Screenshots

Evidence of the responsive layout across desktop, tablet and mobile widths (see the
`screenshots/` folder for the full set, including the Explore and Enquiries pages):

Homepage — Desktop
![Homepage desktop](screenshots/home-desktop.png)

Homepage — Tablet
![Homepage tablet](screenshots/home-tablet.png)

Homepage — Mobile
![Homepage mobile](screenshots/home-mobile.png)

Explore (product grid) — Tablet
![Explore tablet](screenshots/explore-tablet.png)

Enquiries — Mobile
![Enquiries mobile](screenshots/enquiries-mobile.png)

 Changelog

All notable changes to this project are recorded below, most recent first.

 Part 2: Enquiries section
- Added: New `enquiries.html` page with a general enquiry form (name, email,
  phone, subject, message) and a direct-contact card (phone, email, location).
- Added: `.enquiries-layout`, `.contact-card`, `.contact-line` and
  `.contact-label` styles in `style.css`, including a stacked single-column layout
  on screens narrower than 900px.
- Added: Shared `textarea`/`select` styling so all form controls (Registration
  and Enquiries) look and behave consistently.
- Changed: Navigation bar on every page updated to include an "Enquiries" link.
- Changed: Homepage "Contact Us" band now links through to the Enquiries page.

 Part 2: CSS styling and responsive design
- Added: External stylesheet `style.css`, linked from all four HTML pages,
  replacing any inline or unstyled markup carried over from Part 1.
- Added: Design tokens (colour palette, fonts, radius, shadow, content width)
  as CSS custom properties for consistency across pages.
- Added: Base typography rules (font family, size scale, weight, line-height,
  letter-spacing) for headings and body copy, using Archivo and Inter from
  Google Fonts.
- Added: Grid/Flexbox layouts for the navigation bar, brand-logo strip,
  product grid, payment-methods grid and registration form card.
- Added: Visual styling for cards, buttons and links (colour, background,
  border, border-radius, box-shadow) plus `:hover`/`:focus-visible`/`:active`
  states for all interactive elements.
- Added: Responsive breakpoints at 900px, 600px and 400px, switching the
  product grid and navigation spacing to suit tablet and mobile screens, and
  using relative units (`rem`, `em`, `%`, `clamp()`) throughout.
- Added: `screenshots/` folder with desktop, tablet and mobile evidence of the
  responsive layout for the Homepage, Explore and Enquiries pages.

 Corrections from Part 1 feedback
Fixed: Standardised the navigation markup and link order across all pages
  (Homepage → Explore → About → Registration, now also including Enquiries) so
  every page shares the same header structure.
- Fixed: Added descriptive `alt` text to every product, brand and payment-logo
  image so the catalogue is accessible to screen readers.
- Fixed: Added `loading="lazy"` to below-the-fold images (product photos,
  brand logos, payment logos) to improve page load performance.
- Fixed: Corrected inconsistent heading levels on the About and Explore pages
  so the document outline follows a logical `h1` → `h2` structure.
- Fixed: Added `<label for>` associations for every form field on the
  Registration page for accessibility and clicking convenience.
- Fixed: Standardised pricing and sizing text formatting across the product
  catalogue (currency, casing, and size list punctuation).

> If your Part 1 feedback included further specific comments not reflected above,
> add a dated entry here describing the exact correction made — the lecturer should
> be able to trace every feedback point to a changelog entry.

  Part 1: Initial structure and content
- Initial multi-page HTML structure: Homepage, Explore (product listings), About
  (store info and map), and Registration form.
- Product catalogue content added for Dickies, Lacoste, Converse, Carvela, Bishop
  and NAVADA, including images, names, prices and sizes.
- Payment methods section added (PayFlex, PayJustNow, Paxi) with terms.

 References

- Mozilla Developer Network (MDN). *CSS: Cascading Style Sheets.*
  https://developer.mozilla.org/en-US/docs/Web/CSS
- Mozilla Developer Network (MDN). *A guide to CSS layout — Flexbox and Grid.*
  https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_layout
- Mozilla Developer Network (MDN). *Using media queries.*
  https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries
- Google Fonts. *Archivo* and *Inter* typefaces.
  https://fonts.google.com/
- W3C. *Web Content Accessibility Guidelines (WCAG) 2.1.*
  https://www.w3.org/WAI/standards-guidelines/wcag/

 Author

C Khoosal Tailor and Outfitters website — developed as part of a module
assignment (Part 1 and Part 2).

© 2026, C Khoosal
