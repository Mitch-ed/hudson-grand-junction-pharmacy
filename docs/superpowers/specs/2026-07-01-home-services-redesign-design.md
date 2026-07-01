# Home + Services Redesign — Design Spec

Date: 2026-07-01
Branch: `redesign-home-services`

## Goal
Test a new theme/layout for the Home and Services pages, modeled on the provided
`Home.png` and `Services.png` mockups, and feature the real staff/storefront photo
(`GJSTAFF.png`) on both the Home hero and the About page.

Reuses the existing design tokens in `styles.css` (navy `#1B4F8A`, red `#C52233`,
serif headings). No color/brand changes.

## Services featured (7, no prices)
1. Prescription Refills
2. B12 Injections
3. Rash Care
4. Flu & COVID Symptom Help
5. Vaccines
6. Skin Care / Anti-Aging
7. Cold Sore Treatment

## Home page (`index.html`)
- **Hero:** keep existing headline/buttons; add storefront/team photo on the right.
  Float two non-price trust chips over the photo ("No appointment necessary",
  "Most insurance accepted").
- **New "Our Services" grid:** small square icon cards, one per service. Each links
  to `services.html#svc-<slug>` and auto-scrolls to the matching detail card.
- **Dark navy feature strip:** Local & Trusted / Expert Care / Convenient / Personalized.
- **Keep** Hours table and Contact strip. **Remove** the old quick-action cards block
  (replaced by the services grid).

## Services page (`services.html`)
- Replace the vertical text list with **7 large informational cards**, each with:
  photo, title, short lead, a "We can help / What to expect" checklist, footer badges
  (No appointment necessary · Schedule ahead · Most insurance accepted), and a
  "Back to top" link.
- Each card has `id="svc-<slug>"` for anchor scrolling from Home.

## Interaction (`script.js`)
- Smooth-scroll to the targeted service card on load / hash change, offset for the
  sticky header, plus a brief highlight flash on the arrived-at card.

## Imagery
- `GJSTAFF.png` → resized/optimized into `assets/img/` and used on Home hero + About.
- 7 royalty-free (Unsplash/Pexels) photos for the service cards in `assets/img/`.

## About page (`about.html`)
- Add the storefront/team photo as the team/store image.

## Out of scope
- No prices. No changes to Mobile App, Resources, Contact pages. No brand/color changes.
- Nothing pushed until user review.
