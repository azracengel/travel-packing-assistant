---
--bg: #faf7f2;
--panel: #f5efe7;
--panel-strong: #efe1d0;
--text: #342b26;
--muted: #6a5a51;
--border: rgba(52, 43, 38, 0.2);
--accent: #c8ad91;
--accent-strong: #9e7e5f;
--shadow: rgba(52, 43, 38, 0.08);
--page-max-width: 980px;
--page-padding: 48px 24px 72px;
--body-font: Georgia, "Times New Roman", serif;
--site-header-size: 0.76rem;
--site-header-letter-spacing: 0.18em;
--label-size: 0.78rem;
--label-letter-spacing: 0.08em;
--heading-size: clamp(2.4rem, 4vw, 4.2rem);
--heading-line-height: 0.95;
--heading-weight: 600;
--heading-letter-spacing: -0.04em;
--body-copy-size: 1.08rem;
--field-input-padding: 14px 16px;
--button-padding: 16px 20px;
--button-letter-spacing: 0.02em;
--section-title-size: 1.05rem;
--destination-name-size: clamp(1.8rem, 3vw, 2.5rem);
--destination-name-line-height: 1.1;
--summary-row-size: 0.96rem;
--checklist-item-gap: 12px;
--dot-size: 10px;
--search-form-padding: 26px;
--weather-padding: 24px 26px;
--checklist-padding: 24px 26px;
--planner-gap: 28px;
--mobile-breakpoint: 640px;
---

# Overview

This design direction follows the minimal editorial travel aesthetic selected as the final visual direction. The tone is warm, quiet, and confident: warm cream backgrounds, dark brown text, muted beige accents, elegant serif headings, generous whitespace, and simple borders. The intent is to feel useful and trustworthy without visual clutter.

Travelers need to find the destination search and travel date inputs within the first five seconds. That information is the primary task, so the layout should feel immediate and easy to scan. The form should be visually prominent and the packing recommendations should remain more important than decorative elements.

This design aligns with the goals in the proposal, product requirements, and layout plan: a traveler enters a destination, selects dates, receives a weather summary, and then sees a packing checklist without distraction.

# Colors

The color system is intentionally restrained and editorial. All values below are taken directly from the chosen design.

- Background: #faf7f2
- Panel: #f5efe7
- Panel strong: #efe1d0
- Text: #342b26
- Muted text: #6a5a51
- Border: rgba(52, 43, 38, 0.2)
- Accent: #c8ad91
- Accent strong: #9e7e5f
- Shadow: rgba(52, 43, 38, 0.08)

Use the warm cream as the dominant surface, the dark brown as the primary type color, and the beige tones as the functional accents that guide attention to the search form and checklist. The border and shadow colors stay soft so the interface feels calm and understated.

# Typography

The visual language is serif-led, editorial, and calm.

- Body font: Georgia, "Times New Roman", serif
- Site header: 0.76rem; letter-spacing: 0.18em; uppercase; muted text color (#6a5a51)
- Main heading: clamp(2.4rem, 4vw, 4.2rem); line-height: 0.95; font-weight: 600; letter-spacing: -0.04em
- Intro paragraph: 1.08rem; max-width: 520px; muted text color (#6a5a51)
- Form labels: 0.78rem; letter-spacing: 0.08em; uppercase; muted text color (#6a5a51)
- Input text: 1rem
- Button label: 1rem; font-weight: 600; letter-spacing: 0.02em
- Weather and checklist section titles: 1.05rem; letter-spacing: 0.08em; uppercase; muted text color (#6a5a51)
- Weather destination name: clamp(1.8rem, 3vw, 2.5rem); line-height: 1.1
- Summary row text: 0.96rem; muted text color (#6a5a51)

The typography should feel classic and readable rather than decorative. Headlines carry the editorial tone, while the form and utility text remain clear and unambiguous.

# Layout

The layout follows the structure in LAYOUT.md exactly.

Visitors should see the page in this order:

1. Small website header.
2. Large heading: “Pack for the forecast.”
3. Short description of the tool.
4. Destination and travel date form.
5. Main button: “Create my packing list.”
6. Weather forecast summary.
7. Personalized packing checklist.

The most important elements are the search form and the main action, which should appear before any secondary information. The page is intentionally simple and task-driven: the user enters destination and dates, then sees the recommendation output.

Mobile behavior:

- The page width is capped at 980px and centered.
- The form fields stack vertically.
- The date fields collapse to one column on smaller screens.
- The overall spacing remains generous, and the primary form stays easy to find without crowding the page.
- At max-width: 640px, the page padding is reduced to the top only, and the date fields stack into a single column.

Design states from the PRD should follow the same hierarchy:

- Empty state: the greeting, destination field, and travel date inputs are visible immediately; no packing recommendations appear until the user searches.
- Loading state: a temporary weather-checking message appears while the system prepares the packing list; the action button remains visually clear and the layout does not shift dramatically.
- Error state: display a message near the form area that explains the weather data could not be loaded.
- Invalid input state: if the destination or travel dates are empty or invalid, show a corrective message in the form area without making an API request.
- Successful-result state: show destination, date range, weather summary, and packing checklist in the same order as the layout plan.

# Elevation & Depth

This design uses restrained depth rather than visual drama.

- Page background: flat warm cream, no gradients
- Search form, weather block, and checklist panel: background is rgba(255, 255, 255, 0.24)
- Border: 1px solid rgba(52, 43, 38, 0.2)
- Shadow: 0 10px 26px rgba(52, 43, 38, 0.08)
- Panel surfaces remain soft and quiet so visual depth sits behind content instead of competing with it

The goal is to guide attention without adding unnecessary decoration. The destination and date form should feel anchored and stable; the other surfaces should feel supportive, not elevated above the primary task.

# Shapes

The design uses simple, functional geometry.

- Borders: 1px solid var(--border)
- Border radius: none; the interface is intentionally square and direct
- Checklist bullet dot: 10px diameter, circular
- Form fields and buttons: rectangular and straightforward, with no decorative corner treatment
- Primary task blocks: crisp edges and subtle borders maintain the editorial, minimal character

The shape system should remain quiet and practical: no heavy curves, no ornamental forms, and no decorative treatment that draws attention away from the destination and packing guidance.

# Components

## Site header

- Small uppercase label: 0.76rem, 0.18em letter spacing
- Muted text color: #6a5a51
- Bottom margin: 28px

## Hero section

- Large headline: Pack for the forecast.
- Intro paragraph: max-width 520px; 1.08rem; muted text color
- Padding bottom: 8px

## Search form

- Background: rgba(255, 255, 255, 0.24)
- Border: 1px solid rgba(52, 43, 38, 0.2)
- Box shadow: 0 10px 26px rgba(52, 43, 38, 0.08)
- Padding: 26px
- Field spacing: 10px gap between label and input, 18px margin-bottom
- Input styles: full width, border 1px solid rgba(52, 43, 38, 0.2), transparent-to-cream fill, 14px 16px padding, 1rem font size
- Date layout: two-column desktop grid, gap: 18px
- Button: full width, 16px 20px padding, border 1px solid #9e7e5f, background #c8ad91, text color #342b26, font-weight 600, 0.02em letter-spacing, margin-top 8px

## Weather summary

- Padding: 24px 26px
- Section title: 1.05rem, uppercase, 0.08em letter spacing, muted text
- Destination name: clamp(1.8rem, 3vw, 2.5rem), line-height 1.1
- Summary row: flex-wrap, 10px 16px gap, 0.96rem text, muted color
- Summary note: muted text, 1.6 line-height

## Packing checklist

- Padding: 24px 26px
- List style: no default bullets, 12px grid gap
- Each item: 10px vertical padding, border-bottom 1px solid rgba(52, 43, 38, 0.2)
- Bullet indicator: 10px width, 10px height, circular, background #c8ad91

## Page frame

- Max width: 980px
- Centered with margin: 0 auto
- Padding: 48px 24px 72px
- Vertical stack gap: 28px between hero, form, weather, and checklist

# Do's and Don'ts

## Do

- Keep the destination search and date inputs in the most prominent visual position.
- Maintain generous whitespace to preserve the editorial aesthetic.
- Use warm cream backgrounds and muted beige accents to keep the interface calm and easy to read.
- Keep the serif typography elegant and consistent across headings.
- Prioritize the packing recommendations and weather summary over decorative elements.
- Preserve simple borders and subtle depth so the interface feels useful, not ornamental.
- Make the mobile layout stack in a single column without breaking scan order.
- Support all five PRD states with clear, calm messaging that remains close to the form.

## Don't

- Do not add unnecessary animations or motion effects.
- Do not use gradients, strong shadows, or visual clutter that compete with the task.
- Do not let decorative elements outrank the destination search, date selection, or recommended packing list.
- Do not mix in overly modern or playful styles that conflict with the editorial travel tone.
- Do not reduce whitespace so much that the page feels crowded or rushed.
- Do not add glossy buttons, heavy textures, or visual noise that distract from the practical purpose.
- Do not hide the form below the fold on mobile or reduce the contrast of the primary fields.

This design rule remains non-negotiable: the destination search and packing recommendations must always be more important than decorative elements.
