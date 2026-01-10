# 🧭 Web Application Style Guide

This style guide defines the visual language and reusable UI components for your platform. It ensures consistency across screens, supports vibe‑coding tools, and accelerates development by standardizing design tokens and interaction patterns.

---

## 🎨 Color System

### Main Brand Colors

| Name            | Hex       | Usage                          |
|-----------------|-----------|--------------------------------|
| Brand Green     | #447750   | Primary CTA, accents           |
| Brand Orange    | #F26638   | Highlights, active buttons     |
| Brand Pink      | #F8A2D0   | Friendly accents, badges       |
| Brand Brown     | #BE6B3F   | Secondary CTA, hover states    |
| Text Dark       | #041D24   | Primary text                   |
| Text Mid Grey   | #4F6166   | Subtext, labels                |
| Text Light Grey | #A6AFB1   | Placeholder, disabled elements |

### Additional Colors

| Name                  | Hex       | Usage                         |
|-----------------------|-----------|-------------------------------|
| White                 | #FFFFFF   | Backgrounds, buttons          |
| Background            | #FAFAFA   | Page background               |
| Additional Background | #F5F5F5   | Cards, containers             |
| Borders               | #DCDDE0   | Dividers, outlines            |
| Additional Blue       | #38B4F2   | Alerts, links                 |
| Additional Purple     | #38B4F2   | Tags, highlights              |

### Brand Tints

| Name        | Hex       | Usage                          |
|-------------|-----------|--------------------------------|
| Green Tint  | #E3EBE5   | Hover, soft backgrounds        |
| Orange Tint | #E3EBE5   | Notification backgrounds       |
| Brown Tint  | #F5E9E2   | Card accents, soft CTA         |

---

## 🔠 Typography System

### Headings

| Style        | Size | Weight | Usage                        |
|--------------|------|--------|------------------------------|
| Heading XL   | 34px | Bold   | Page titles, hero sections   |
| Heading L    | 24px | Medium | Section headers              |
| Heading M    | 18px | Medium | Subsection titles            |
| Heading S    | 16px | Medium | Card titles, modals          |
| Heading XS   | 14px | Medium | Small headers, labels        |
| Heading XXS  | 12px | Bold   | Compact headers              |

### Subheadings

| Style         | Size | Weight  | Usage                        |
|---------------|------|---------|------------------------------|
| Subheading M  | 16px | Regular | Card subtitles               |
| Subheading S  | 14px | Regular | Supporting text              |
| Subheading XS | 12px | Regular | Metadata, captions           |

### Body Text

| Style   | Size | Weight | Usage                        |
|---------|------|--------|------------------------------|
| Body M  | 16px | Light  | Paragraphs, descriptions     |
| Body S  | 14px | Light  | Secondary content            |
| Body XS | 12px | Light  | Legal, footnotes             |

### Caption

| Style   | Size | Weight  | Usage                        |
|---------|------|---------|------------------------------|
| Caption | 11px | Regular | Timestamps, microcopy        |

---

## 🧱 UI Components

### Class Search Result Card

| Element    | Style/Value                     |
|------------|---------------------------------|
| Thumbnail  | 1:1 image, rounded corners      |
| Rating     | Star icon + numeric (e.g., 4.5) |
| Category   | Subheading S                    |
| Class Name | Heading S, bold                 |
| Price      | Body M                          |
| Location   | Pin icon + location name        |

**Usage:** Search results, category pages, featured listings.

---

### Buttons

| Label Example                | Style Category     | Size  | Color     | Icon | State        |
|-----------------------------|--------------------|-------|-----------|------|--------------|
| Book                        | Default            | 50px  | Orange    | No   | Active       |
| Log In                      | White              | 50px  | White     | No   | Active       |
| Log In                      | Transparent        | 50px  | Green     | No   | Active       |
| Pay $250                    | Icon               | 50px  | Orange    | Lock | Active       |
| Chat with Karate for Kids   | Icon White         | 50px  | White     | Chat | Active       |
| Cancel                      | Inactive           | 50px  | Grey      | No   | Disabled     |
| Follow                      | Default            | 40px  | Orange    | No   | Active       |
| Add Poll                    | Icon White         | 40px  | White     | Poll | Active       |
| QR Code                     | Icon White         | 40px  | White     | QR   | Active       |
| Sign Up Next                | Circular CTA       | 50px  | Orange    | Arrow| Primary CTA  |

**States:** Default, Hover, Active, Disabled  
**Corner Radius:** 8px standard, circular for icon buttons  
**Font:** Heading XS or Body S depending on size

---

## 🖼 Backgrounds

Use abstract backgrounds with curved, overlapping shapes in green, orange, and pink. Ideal for:

- Hero sections  
- Empty states  
- Promotional banners  
- Onboarding screens  

**Design Tip:** Use 2–3 layered shapes with brand tints for depth.

---

# 🧿 Icon System

The icon system provides a unified visual language across the platform. Icons support quick recognition, reinforce meaning, and enhance usability.

---

## 🗂 Icon Categories

### Social & Communication
- Facebook  
- WhatsApp  
- Email  
- Phone  
- Chat bubbles  
- Share  

### User Interface (Core UI)
- Camera  
- Calendar  
- Location pin  
- Clock  
- Filter  
- Search  
- Upload / Download  
- Close / Cancel  
- Edit / Delete  
- Notifications  
- Settings  

### Reactions & Ratings
- Star (filled + outline)  
- Heart (filled + outline)  
- Emoji-style icons  

### Payments & Commerce
- Mastercard  
- Visa  
- Apple Pay  
- Lock (secure payment)  
- Cart / Bag  

### Activities & Categories
- Sports (soccer, basketball, tennis, boxing gloves)  
- Science (microscope, atom)  
- Art (palette, brush)  
- Music (note, instrument)  
- Food (apple, snack)  

---

## 🎨 Icon Styles

### Primary Style (Recommended)
- Outline / line art  
- Clean, modern, scalable  
- Ideal for navigation, lists, cards  

### Secondary Style
- Filled icons  
- Use for active states or emphasis  

### Decorative Icons
- Full-color illustrations  
- Use only in category tiles, empty states, onboarding, marketing  

---

## 📏 Icon Sizing Rules

| Usage Context          | Size     |
|------------------------|----------|
| Inline with text       | 16–20px  |
| Buttons                | 20–24px  |
| Navigation bar         | 24px     |
| Cards & lists          | 20–24px  |
| Category tiles         | 32–48px  |
| Hero / decorative      | 64px+    |

**Scaling:** Maintain proportional scaling and consistent stroke width.  
**Touch Target:** Minimum 44px.

---

## 🎨 Color Usage

### Default Icon Color
- Text Dark (#041D24)

### Secondary / Muted Icons
- Text Mid Grey (#4F6166)  
- Text Light Grey (#A6AFB1) for disabled  

### Accent Icons (use sparingly)
- Brand Orange (#F26638)  
- Brand Green (#447750)  
- Brand Pink (#F8A2D0)  

---

## 🧭 Usage Guidelines

- Pair icons with text for clarity  
- Maintain 8px spacing between icon and label  
- Use semantic icons (chat bubble for messaging, lock for secure payment)  
- Provide `aria-label` or `title` for accessibility  
- Ensure WCAG AA contrast  

---

## 🔗 Icon Library Reference

If hosting your own icons:
- Store SVGs in `/assets/icons/`  
- Reference by consistent naming conventions  

If using third‑party libraries (optional):
- **Phosphor Icons** — https://phosphoricons.com  
- **Heroicons** — https://heroicons.com  
- **Font Awesome** — https://fontawesome.com  

Use third‑party icons only when your custom set lacks a required symbol.

---

## 🧪 Icon States

| State    | Style Rules                         |
|----------|--------------------------------------|
| Default  | Outline, Text Dark                   |
| Hover    | Brand Orange or Brand Green          |
| Active   | Filled icon or bold color            |
| Disabled | Text Light Grey, 40% opacity         |

---

## 📁 Usage Notes

- All components are mobile‑first and scalable  
- Use an 8px spacing system  
- Icons should be SVGs for crisp rendering  
- Maintain accessibility with semantic HTML and contrast
