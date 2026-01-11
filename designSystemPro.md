# Kids Activities Platform - Design System & Style Guide v1.2

## Overview
This design system defines the visual language and UI components for the kids activities platform. Use these specifications when instructing AI code assistants to build interface components.

**Version**: 1.2  
**Last Updated**: January 11, 2026  
**Platform**: Kids Activities Finder (Mobile-First Web App)

---

## Quick Start Guide

### For AI Coding Assistants

#### Step 1: Setup Design Tokens
Create a `tokens.css` file in your project root:

```css
/* Copy all design tokens from the Design Tokens section below */
@import url('tokens.css');
```

#### Step 2: Import in Your Main CSS
```css
/* main.css or index.css */
@import './tokens.css';

/* Now use tokens throughout your app */
.my-component {
  color: var(--color-primary-base);
  padding: var(--spacing-lg);
}
```

#### Step 3: Generate Components
When prompting AI assistants, always reference design tokens:

```
Create a search input component using:
- Background: var(--color-neutral-0)
- Border radius: var(--radius-lg)
- Padding: var(--spacing-md) var(--spacing-lg)
- Font: var(--font-size-body-lg)
- Icon size: var(--size-icon-md)
```

---

## Design Tokens

Design tokens are the foundational variables that store design decisions. Use these tokens instead of hard-coded values to ensure consistency and make the design system scalable and maintainable.

### Token Naming Convention

Follow this hierarchical naming structure:
```
[category]-[property]-[variant]-[state]
```

#### Examples:
- `color-primary-base` - Base primary color
- `color-primary-hover` - Primary color hover state
- `spacing-md` - Medium spacing value
- `font-size-heading-lg` - Large heading font size
- `border-radius-card` - Border radius for cards
- `shadow-elevation-2` - Second level shadow

### Token Categories

#### 1. Color Tokens
```css
/* Primary Colors */
--color-primary-base: #FF6B4A;
--color-primary-hover: #E55A3A;
--color-primary-active: #CC4F2F;
--color-primary-light: #FFF0ED;

--color-secondary-base: #4A7856;
--color-secondary-hover: #3D6447;
--color-secondary-active: #305038;
--color-secondary-light: #EBF3ED;

--color-accent-base: #F5A5C8;
--color-accent-hover: #F290B8;
--color-accent-light: #FEF5F9;

/* Neutral Colors */
--color-neutral-900: #000000;
--color-neutral-800: #333333;
--color-neutral-600: #666666;
--color-neutral-400: #999999;
--color-neutral-300: #CCCCCC;
--color-neutral-200: #E0E0E0;
--color-neutral-100: #F5F5F5;
--color-neutral-0: #FFFFFF;

/* Semantic Colors */
--color-success: #4A7856;
--color-error: #FF4444;
--color-warning: #FF6B4A;
--color-info: #4A9FFF;

/* Text Colors */
--color-text-primary: #000000;
--color-text-secondary: #333333;
--color-text-tertiary: #666666;
--color-text-disabled: #999999;
--color-text-inverse: #FFFFFF;

/* Background Colors */
--color-bg-primary: #FFFFFF;
--color-bg-secondary: #F5F5F5;
--color-bg-tertiary: #EBF3ED;
--color-bg-disabled: #E0E0E0;

/* Border Colors */
--color-border-base: #E0E0E0;
--color-border-focus: #FF6B4A;
--color-border-error: #FF4444;
```

#### 2. Typography Tokens
```css
/* Font Families */
--font-family-primary: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
--font-family-fallback: Arial, sans-serif;

/* Font Sizes */
--font-size-heading-xxl: 34px;
--font-size-heading-xl: 24px;
--font-size-heading-lg: 18px;
--font-size-heading-md: 16px;
--font-size-heading-sm: 14px;
--font-size-heading-xs: 12px;

--font-size-body-lg: 16px;
--font-size-body-md: 14px;
--font-size-body-sm: 12px;

--font-size-caption: 11px;

/* Font Weights */
--font-weight-bold: 700;
--font-weight-semibold: 600;
--font-weight-medium: 500;
--font-weight-regular: 400;
--font-weight-light: 300;

/* Line Heights */
--line-height-tight: 1.2;
--line-height-snug: 1.3;
--line-height-normal: 1.4;
--line-height-relaxed: 1.5;
--line-height-loose: 1.6;

/* Letter Spacing */
--letter-spacing-tight: -0.02em;
--letter-spacing-normal: 0;
--letter-spacing-wide: 0.02em;
--letter-spacing-wider: 0.05em;
```

#### 3. Spacing Tokens
```css
/* Spacing Scale (4px grid) */
--spacing-xs: 4px;
--spacing-sm: 8px;
--spacing-md: 12px;
--spacing-lg: 16px;
--spacing-xl: 24px;
--spacing-2xl: 32px;
--spacing-3xl: 48px;
--spacing-4xl: 64px;

/* Component-Specific Spacing */
--spacing-card-padding: var(--spacing-lg);
--spacing-button-padding-x: 32px;
--spacing-button-padding-y: var(--spacing-lg);
--spacing-button-small-padding-x: 20px;
--spacing-button-small-padding-y: 10px;
--spacing-icon-gap: var(--spacing-sm);
--spacing-card-gap: var(--spacing-lg);
--spacing-input-padding: var(--spacing-md) var(--spacing-lg);
```

#### 4. Size Tokens
```css
/* Button Heights */
--size-button-height-lg: 50px;
--size-button-height-md: 40px;
--size-button-height-sm: 32px;

/* Icon Sizes */
--size-icon-xs: 16px;
--size-icon-sm: 20px;
--size-icon-md: 24px;
--size-icon-lg: 32px;
--size-icon-xl: 48px;

/* Input Heights */
--size-input-height: 48px;
--size-input-height-sm: 40px;

/* Card Dimensions */
--size-card-image-width: 200px;
--size-card-image-height: 160px;
--size-card-popular-width: 300px;
--size-card-popular-image-height: 200px;
--size-card-category-square: 160px;
--size-card-activity-small: 180px;

/* Navigation */
--size-nav-height: 64px;
--size-bottom-nav-height: 72px;

/* Container Widths */
--size-container-max: 1200px;
--size-container-md: 960px;
--size-container-sm: 640px;
```

#### 5. Border Radius Tokens
```css
/* Border Radius Scale */
--radius-sm: 4px;
--radius-md: 8px;
--radius-lg: 12px;
--radius-xl: 16px;
--radius-2xl: 24px;
--radius-round: 50%;
--radius-pill: 999px;

/* Component-Specific Radius */
--radius-button: var(--radius-md);
--radius-card: var(--radius-md);
--radius-card-large: var(--radius-lg);
--radius-input: var(--radius-lg);
--radius-badge: var(--radius-sm);
--radius-chip: var(--radius-pill);
--radius-modal: var(--radius-2xl);
```

#### 6. Shadow Tokens
```css
/* Shadow Elevation Levels */
--shadow-elevation-0: none;
--shadow-elevation-1: 0 2px 8px rgba(0, 0, 0, 0.08);
--shadow-elevation-2: 0 4px 12px rgba(0, 0, 0, 0.12);
--shadow-elevation-3: 0 8px 24px rgba(0, 0, 0, 0.16);
--shadow-elevation-4: 0 12px 32px rgba(0, 0, 0, 0.20);

/* Component-Specific Shadows */
--shadow-card: var(--shadow-elevation-1);
--shadow-card-hover: var(--shadow-elevation-2);
--shadow-modal: var(--shadow-elevation-3);
--shadow-dropdown: var(--shadow-elevation-3);
--shadow-nav: 0 -2px 8px rgba(0, 0, 0, 0.08);
```

#### 7. Transition Tokens
```css
/* Transition Durations */
--transition-fast: 150ms;
--transition-base: 200ms;
--transition-slow: 300ms;

/* Transition Easings */
--easing-standard: cubic-bezier(0.4, 0.0, 0.2, 1);
--easing-decelerate: cubic-bezier(0.0, 0.0, 0.2, 1);
--easing-accelerate: cubic-bezier(0.4, 0.0, 1, 1);

/* Common Transitions */
--transition-color: color var(--transition-base) var(--easing-standard);
--transition-background: background-color var(--transition-base) var(--easing-standard);
--transition-transform: transform var(--transition-base) var(--easing-standard);
--transition-shadow: box-shadow var(--transition-base) var(--easing-standard);
--transition-all: all var(--transition-base) var(--easing-standard);
```

#### 8. Z-Index Tokens
```css
/* Z-Index Scale */
--z-index-base: 0;
--z-index-dropdown: 100;
--z-index-sticky: 200;
--z-index-overlay: 300;
--z-index-modal: 400;
--z-index-popover: 500;
--z-index-tooltip: 600;
```

#### 9. Breakpoint Tokens
```css
/* Responsive Breakpoints */
--breakpoint-mobile: 640px;
--breakpoint-tablet: 1024px;
--breakpoint-desktop: 1280px;
```

---

## Color Palette

### Primary Colors
- **Primary Orange**: `#FF6B4A` / `var(--color-primary-base)` - Primary CTA buttons, active states
- **Primary Green**: `#4A7856` / `var(--color-secondary-base)` - Secondary buttons, backgrounds, brand elements
- **Accent Pink**: `#F5A5C8` / `var(--color-accent-base)` - Decorative elements, background accents

### Neutral Colors
- **Black**: `#000000` / `var(--color-neutral-900)` - Headings, primary text
- **Dark Gray**: `#333333` / `var(--color-neutral-800)` - Body text, secondary headings
- **Medium Gray**: `#666666` / `var(--color-neutral-600)` - Captions, metadata
- **Light Gray**: `#F5F5F5` / `var(--color-neutral-100)` - Backgrounds, inactive states
- **White**: `#FFFFFF` / `var(--color-neutral-0)` - Backgrounds, button text

---

## Typography

### Font Family
- **Primary Font**: Sans-serif (System font stack recommended)
- **Token**: `var(--font-family-primary)`
- **Fallback**: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif

### Text Styles Reference

| Style | Size | Weight | Token |
|-------|------|--------|-------|
| Heading XXL | 34px | Bold (700) | `--font-size-heading-xxl`, `--font-weight-bold` |
| Heading XL | 24px | Medium (500) | `--font-size-heading-xl`, `--font-weight-medium` |
| Heading LG | 18px | Medium (500) | `--font-size-heading-lg`, `--font-weight-medium` |
| Heading MD | 16px | Medium (500) | `--font-size-heading-md`, `--font-weight-medium` |
| Body LG | 16px | Regular (400) | `--font-size-body-lg`, `--font-weight-regular` |
| Body MD | 14px | Regular (400) | `--font-size-body-md`, `--font-weight-regular` |
| Caption | 11px | Regular (400) | `--font-size-caption`, `--font-weight-regular` |

---

## Form Components

### Search Input

A versatile search input component with multiple variants for different contexts.

#### Variants

**1. Standalone Search (Homepage)**
- **Use Case**: Main search bar on hero section
- **Background**: `var(--color-neutral-0)`
- **Border Radius**: `var(--radius-input)` (12px)
- **Height**: `var(--size-input-height)` (48px)
- **Padding**: `var(--spacing-input-padding)` (12px 16px)
- **Icon**: Search magnifying glass, `var(--size-icon-md)`, right-aligned
- **Placeholder**: Light gray `var(--color-neutral-400)`
- **Shadow**: `var(--shadow-elevation-1)`

```html
<div class="search-input">
  <input 
    type="text" 
    placeholder="Search" 
    class="search-input__field"
  />
  <button class="search-input__icon" aria-label="Search">
    <svg width="24" height="24"><!-- search icon --></svg>
  </button>
</div>
```

```css
.search-input {
  position: relative;
  width: 100%;
}

.search-input__field {
  width: 100%;
  height: var(--size-input-height);
  padding: var(--spacing-input-padding);
  padding-right: var(--spacing-3xl);
  background-color: var(--color-neutral-0);
  border: none;
  border-radius: var(--radius-input);
  font-size: var(--font-size-body-lg);
  font-family: var(--font-family-primary);
  color: var(--color-text-primary);
  box-shadow: var(--shadow-elevation-1);
  transition: var(--transition-shadow);
}

.search-input__field::placeholder {
  color: var(--color-neutral-400);
}

.search-input__field:focus {
  outline: 2px solid var(--color-border-focus);
  outline-offset: 2px;
  box-shadow: var(--shadow-elevation-2);
}

.search-input__icon {
  position: absolute;
  right: var(--spacing-md);
  top: 50%;
  transform: translateY(-50%);
  background: none;
  border: none;
  padding: var(--spacing-sm);
  cursor: pointer;
  color: var(--color-neutral-600);
}
```

**2. Search with Back Button**
- **Use Case**: Search location, search results pages
- **Layout**: Back arrow (left) + input + search icon (right)
- **Back Button**: Circular tap target, `var(--size-icon-lg)` (32px)

```html
<div class="search-header">
  <button class="search-header__back" aria-label="Go back">
    <svg width="24" height="24"><!-- chevron left --></svg>
  </button>
  <input 
    type="text" 
    placeholder="What is your location" 
    class="search-header__input"
  />
  <button class="search-header__icon" aria-label="Search">
    <svg width="24" height="24"><!-- search icon --></svg>
  </button>
</div>
```

```css
.search-header {
  display: flex;
  align-items: center;
  gap: var(--spacing-md);
  padding: var(--spacing-md);
  background-color: var(--color-neutral-0);
}

.search-header__back {
  flex-shrink: 0;
  width: var(--size-icon-lg);
  height: var(--size-icon-lg);
  display: flex;
  align-items: center;
  justify-content: center;
  background: none;
  border: none;
  cursor: pointer;
  color: var(--color-text-primary);
}

.search-header__input {
  flex: 1;
  height: var(--size-input-height-sm);
  padding: var(--spacing-sm) var(--spacing-lg);
  border: 1px solid var(--color-border-base);
  border-radius: var(--radius-input);
  font-size: var(--font-size-body-lg);
  font-family: var(--font-family-primary);
}

.search-header__input:focus {
  outline: none;
  border-color: var(--color-border-focus);
}

.search-header__icon {
  flex-shrink: 0;
  background: none;
  border: none;
  padding: var(--spacing-sm);
  cursor: pointer;
  color: var(--color-neutral-600);
}
```

**3. Search in Hero**
- **Use Case**: Integrated into hero background section
- **Styling**: Same as standalone but with context-appropriate shadows

---

### Filter Chips / Pills

Rounded pill-shaped buttons for filtering and categorization.

#### Specifications:
- **Border Radius**: `var(--radius-chip)` (999px - full pill)
- **Height**: `var(--size-button-height-md)` (40px)
- **Padding**: `var(--spacing-sm) var(--spacing-lg)` (8px 16px)
- **Font**: `var(--font-size-body-md)` with `var(--font-weight-medium)`
- **Gap**: `var(--spacing-sm)` between multiple chips

#### States:
- **Default**: White background, gray border
- **Selected**: Green background `var(--color-secondary-base)`, white text
- **Hover**: Subtle shadow elevation

```html
<div class="filter-chips">
  <button class="chip chip--selected">Category</button>
  <button class="chip">Offers</button>
  <button class="chip">More Filters</button>
</div>
```

```css
.filter-chips {
  display: flex;
  gap: var(--spacing-sm);
  flex-wrap: wrap;
}

.chip {
  height: var(--size-button-height-md);
  padding: var(--spacing-sm) var(--spacing-lg);
  background-color: var(--color-neutral-0);
  border: 1px solid var(--color-border-base);
  border-radius: var(--radius-chip);
  font-size: var(--font-size-body-md);
  font-weight: var(--font-weight-medium);
  font-family: var(--font-family-primary);
  color: var(--color-text-primary);
  cursor: pointer;
  transition: var(--transition-all);
  white-space: nowrap;
}

.chip:hover {
  box-shadow: var(--shadow-elevation-1);
}

.chip--selected {
  background-color: var(--color-secondary-base);
  border-color: var(--color-secondary-base);
  color: var(--color-text-inverse);
}

.chip:focus {
  outline: 2px solid var(--color-border-focus);
  outline-offset: 2px;
}
```

---

## Navigation Components

### Bottom Navigation

Fixed bottom navigation bar with 5 tab items and icon-based navigation.

#### Specifications:
- **Height**: `var(--size-bottom-nav-height)` (72px)
- **Background**: `var(--color-neutral-0)`
- **Shadow**: `var(--shadow-nav)` (top shadow)
- **Item Layout**: 5 equal-width columns
- **Icon Size**: `var(--size-icon-md)` (24px)
- **Label Font**: `var(--font-size-caption)`
- **Active State**: Primary orange color
- **Inactive State**: Medium gray color

```html
<nav class="bottom-nav">
  <a href="/" class="bottom-nav__item bottom-nav__item--active" aria-label="Home">
    <svg class="bottom-nav__icon" width="24" height="24"><!-- home icon --></svg>
    <span class="bottom-nav__label">Home</span>
  </a>
  <a href="/calendar" class="bottom-nav__item" aria-label="Calendar">
    <svg class="bottom-nav__icon" width="24" height="24"><!-- calendar icon --></svg>
    <span class="bottom-nav__label">Calendar</span>
  </a>
  <a href="/favorites" class="bottom-nav__item" aria-label="Favorites">
    <svg class="bottom-nav__icon" width="24" height="24"><!-- heart icon --></svg>
    <span class="bottom-nav__label">Saved</span>
  </a>
  <a href="/messages" class="bottom-nav__item" aria-label="Messages">
    <svg class="bottom-nav__icon" width="24" height="24"><!-- chat icon --></svg>
    <span class="bottom-nav__label">Messages</span>
  </a>
  <a href="/profile" class="bottom-nav__item" aria-label="Profile">
    <svg class="bottom-nav__icon" width="24" height="24"><!-- profile icon --></svg>
    <span class="bottom-nav__label">Profile</span>
  </a>
</nav>
```

```css
.bottom-nav {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  height: var(--size-bottom-nav-height);
  background-color: var(--color-neutral-0);
  box-shadow: var(--shadow-nav);
  z-index: var(--z-index-sticky);
  padding-bottom: env(safe-area-inset-bottom);
}

.bottom-nav__item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: var(--spacing-xs);
  color: var(--color-neutral-600);
  text-decoration: none;
  transition: var(--transition-color);
  padding: var(--spacing-sm);
}

.bottom-nav__item:hover {
  color: var(--color-primary-base);
}

.bottom-nav__item--active {
  color: var(--color-primary-base);
}

.bottom-nav__icon {
  width: var(--size-icon-md);
  height: var(--size-icon-md);
}

.bottom-nav__label {
  font-size: var(--font-size-caption);
  font-weight: var(--font-weight-regular);
  text-transform: capitalize;
}
```

---

### Location Bar

A rounded bar displaying the current location with a back button.

#### Specifications:
- **Background**: `var(--color-neutral-0)`
- **Border Radius**: `var(--radius-2xl)` (24px)
- **Height**: 56px
- **Padding**: `var(--spacing-md) var(--spacing-lg)`
- **Shadow**: `var(--shadow-elevation-1)`
- **Layout**: Back arrow + Location text (centered)

```html
<div class="location-bar">
  <button class="location-bar__back" aria-label="Go back">
    <svg width="24" height="24"><!-- chevron left --></svg>
  </button>
  <span class="location-bar__text">Melbourne, Fitzroy</span>
</div>
```

```css
.location-bar {
  display: flex;
  align-items: center;
  gap: var(--spacing-md);
  height: 56px;
  padding: var(--spacing-md) var(--spacing-lg);
  background-color: var(--color-neutral-0);
  border-radius: var(--radius-2xl);
  box-shadow: var(--shadow-elevation-1);
}

.location-bar__back {
  flex-shrink: 0;
  width: var(--size-icon-lg);
  height: var(--size-icon-lg);
  display: flex;
  align-items: center;
  justify-content: center;
  background: none;
  border: none;
  cursor: pointer;
  color: var(--color-text-primary);
}

.location-bar__text {
  flex: 1;
  text-align: center;
  font-size: var(--font-size-heading-md);
  font-weight: var(--font-weight-medium);
  color: var(--color-text-primary);
}
```

---

## Layout Components

### Hero Section

Large hero section with curved organic background and white text overlay.

#### Specifications:
- **Background**: Organic gradient using brand colors
- **Padding**: `var(--spacing-3xl) var(--spacing-lg)`
- **Border Radius**: `var(--radius-2xl)` on bottom
- **Text Color**: `var(--color-text-inverse)` (white)
- **Heading**: `var(--font-size-heading-xxl)` with `var(--font-weight-bold)`

```html
<section class="hero">
  <div class="hero__content">
    <h1 class="hero__heading">Discover</h1>
    <!-- Optional: Integrated search -->
    <div class="search-input">
      <input type="text" placeholder="Search" class="search-input__field" />
      <button class="search-input__icon"><svg><!-- search --></svg></button>
    </div>
  </div>
</section>
```

```css
.hero {
  background: linear-gradient(135deg, 
    var(--color-secondary-base) 0%, 
    var(--color-secondary-base) 60%, 
    var(--color-accent-base) 80%, 
    var(--color-primary-base) 100%);
  padding: var(--spacing-3xl) var(--spacing-lg);
  border-radius: 0 0 var(--radius-2xl) var(--radius-2xl);
  color: var(--color-text-inverse);
}

.hero__content {
  max-width: var(--size-container-sm);
  margin: 0 auto;
}

.hero__heading {
  font-size: var(--font-size-heading-xxl);
  font-weight: var(--font-weight-bold);
  margin-bottom: var(--spacing-xl);
  color: var(--color-text-inverse);
}

/* For hero with larger text like "What are you looking for?" */
.hero--large-text .hero__heading {
  font-size: 48px;
  line-height: var(--line-height-tight);
}
```

---

### Section Header

Uppercase label used to separate content sections with optional "See All" link.

#### Specifications:
- **Font**: `var(--font-size-caption)` (11px)
- **Weight**: `var(--font-weight-bold)` or `var(--font-weight-semibold)`
- **Transform**: Uppercase
- **Letter Spacing**: `var(--letter-spacing-wider)`
- **Color**: `var(--color-text-tertiary)`
- **Margin**: `var(--spacing-xl) 0 var(--spacing-md)`

```html
<div class="section-header">
  <h2 class="section-header__title">UPCOMING EVENT</h2>
  <a href="/events" class="section-header__link">See All</a>
</div>
```

```css
.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: var(--spacing-xl) 0 var(--spacing-md);
}

.section-header__title {
  font-size: var(--font-size-caption);
  font-weight: var(--font-weight-semibold);
  letter-spacing: var(--letter-spacing-wider);
  text-transform: uppercase;
  color: var(--color-text-tertiary);
}

.section-header__link {
  font-size: var(--font-size-body-md);
  font-weight: var(--font-weight-medium);
  color: var(--color-primary-base);
  text-decoration: none;
  display: flex;
  align-items: center;
  gap: var(--spacing-xs);
}

.section-header__link:hover {
  color: var(--color-primary-hover);
}
```

---

## Card Components

### Search Result Card (Existing - Updated)

Horizontal card displaying class information. *[Previously documented, updated with tokens]*

```css
.card-search-result {
  background-color: var(--color-bg-primary);
  border-radius: var(--radius-card);
  box-shadow: var(--shadow-card);
  display: flex;
  padding: var(--spacing-card-padding);
  gap: var(--spacing-lg);
  transition: var(--transition-shadow);
}

.card-search-result:hover {
  box-shadow: var(--shadow-card-hover);
}

.card-image {
  width: var(--size-card-image-width);
  height: var(--size-card-image-height);
  border-radius: var(--radius-md);
  object-fit: cover;
}

.card-title {
  font-size: var(--font-size-heading-xl);
  font-weight: var(--font-weight-medium);
  color: var(--color-text-primary);
}

.rating {
  color: var(--color-primary-base);
  font-size: var(--font-size-body-lg);
  font-weight: var(--font-weight-medium);
  display: flex;
  align-items: center;
  gap: var(--spacing-xs);
}
```

---

### Category Card

Card displaying activity categories with image, title, and class count. Single component with grid and list variants.

#### Grid Variant (Square)
- **Use Case**: Category selection page (2-column grid)
- **Dimensions**: `var(--size-card-category-square)` × `var(--size-card-category-square)` (160px)
- **Border Radius**: `var(--radius-lg)` (12px)
- **Image**: Full card size, object-fit cover
- **Overlay**: Gradient overlay for text readability
- **Text**: Bottom-aligned, white text, title + count

```html
<div class="category-card category-card--grid">
  <img src="active.jpg" alt="Active" class="category-card__image" />
  <div class="category-card__content">
    <h3 class="category-card__title">Active</h3>
    <p class="category-card__count">981 classes</p>
  </div>
</div>
```

```css
.category-card {
  position: relative;
  overflow: hidden;
  background-color: var(--color-neutral-0);
  border-radius: var(--radius-lg);
  cursor: pointer;
  transition: var(--transition-transform);
}

.category-card:hover {
  transform: scale(1.02);
}

.category-card--grid {
  width: var(--size-card-category-square);
  height: var(--size-card-category-square);
}

.category-card__image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.category-card__content {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding: var(--spacing-lg);
  background: linear-gradient(to top, rgba(0,0,0,0.6) 0%, transparent 100%);
  color: var(--color-text-inverse);
}

.category-card__title {
  font-size: var(--font-size-heading-lg);
  font-weight: var(--font-weight-semibold);
  margin-bottom: var(--spacing-xs);
}

.category-card__count {
  font-size: var(--font-size-body-sm);
  font-weight: var(--font-weight-regular);
  opacity: 0.9;
}
```

#### List Variant (Horizontal)
- **Use Case**: Scrollable category list
- **Layout**: Horizontal with thumbnail (80px) + text
- **Height**: 80px
- **Padding**: `var(--spacing-md)`

```html
<div class="category-card category-card--list">
  <img src="active.jpg" alt="Active Recreation" class="category-card__thumbnail" />
  <div class="category-card__info">
    <h3 class="category-card__title">Active Recreation</h3>
    <p class="category-card__count">20 Classes</p>
  </div>
</div>
```

```css
.category-card--list {
  display: flex;
  align-items: center;
  gap: var(--spacing-md);
  padding: var(--spacing-md);
  background-color: var(--color-neutral-0);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-card);
  height: 80px;
}

.category-card__thumbnail {
  width: 64px;
  height: 64px;
  border-radius: var(--radius-md);
  object-fit: cover;
  flex-shrink: 0;
}

.category-card__info {
  flex: 1;
}

.category-card--list .category-card__title {
  font-size: var(--font-size-heading-md);
  font-weight: var(--font-weight-medium);
  color: var(--color-text-primary);
  margin-bottom: var(--spacing-xs);
}

.category-card--list .category-card__count {
  font-size: var(--font-size-body-sm);
  color: var(--color-text-tertiary);
}
```

---

### Activity Card (Small)

Compact square card for horizontal scrolling lists showing popular activities.

#### Specifications:
- **Width**: `var(--size-card-activity-small)` (180px)
- **Image Height**: 120px
- **Border Radius**: `var(--radius-lg)`
- **Padding**: `var(--spacing-md)` for text area
- **Shadow**: `var(--shadow-card)`
- **Layout**: Vertical - image on top, text below

```html
<div class="activity-card-small">
  <img src="boxing.jpg" alt="Non-Contact Boxing" class="activity-card-small__image" />
  <div class="activity-card-small__content">
    <h3 class="activity-card-small__title">Non-Contact Boxin...</h3>
    <p class="activity-card-small__category">Active Recreation</p>
  </div>
</div>
```

```css
.activity-card-small {
  width: var(--size-card-activity-small);
  background-color: var(--color-bg-primary);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-card);
  overflow: hidden;
  transition: var(--transition-shadow);
  flex-shrink: 0;
}

.activity-card-small:hover {
  box-shadow: var(--shadow-card-hover);
}

.activity-card-small__image {
  width: 100%;
  height: 120px;
  object-fit: cover;
}

.activity-card-small__content {
  padding: var(--spacing-md);
}

.activity-card-small__title {
  font-size: var(--font-size-heading-md);
  font-weight: var(--font-weight-medium);
  color: var(--color-text-primary);
  margin-bottom: var(--spacing-xs);
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.activity-card-small__category {
  font-size: var(--font-size-body-sm);
  color: var(--color-text-tertiary);
}
```

---

## List Components

### Search History Item

List item displaying recent searches with clock icon, location, and activity type.

#### Specifications:
- **Height**: ~72px (auto with padding)
- **Layout**: Icon (left) + 2-line text (center)
- **Icon**: Clock icon, `var(--size-icon-md)`, gray circle background
- **Padding**: `var(--spacing-md)`
- **Border**: Bottom border `var(--color-border-base)` (optional)

```html
<button class="search-history-item">
  <div class="search-history-item__icon">
    <svg width="20" height="20"><!-- clock icon --></svg>
  </div>
  <div class="search-history-item__content">
    <p class="search-history-item__location">Fitzroy, Melbourne</p>
    <p class="search-history-item__activity">Active Recreation</p>
  </div>
</button>
```

```css
.search-history-item {
  display: flex;
  align-items: center;
  gap: var(--spacing-md);
  width: 100%;
  padding: var(--spacing-md);
  background: none;
  border: none;
  border-bottom: 1px solid var(--color-border-base);
  text-align: left;
  cursor: pointer;
  transition: var(--transition-background);
}

.search-history-item:hover {
  background-color: var(--color-neutral-100);
}

.search-history-item__icon {
  flex-shrink: 0;
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: var(--color-neutral-100);
  border-radius: var(--radius-round);
  color: var(--color-neutral-600);
}

.search-history-item__content {
  flex: 1;
}

.search-history-item__location {
  font-size: var(--font-size-body-lg);
  font-weight: var(--font-weight-medium);
  color: var(--color-text-primary);
  margin-bottom: var(--spacing-xs);
}

.search-history-item__activity {
  font-size: var(--font-size-body-sm);
  color: var(--color-text-tertiary);
}
```

---

### List Item (Selectable)

Radio-style selectable list item with checkmark for selected state.

#### Specifications:
- **Height**: 56px
- **Layout**: Text (left) + Checkmark icon (right, when selected)
- **Padding**: `var(--spacing-lg)`
- **Border**: Bottom border
- **Selected State**: Checkmark visible, optional background tint

```html
<button class="list-item-selectable list-item-selectable--selected">
  <span class="list-item-selectable__text">Highest Rated</span>
  <svg class="list-item-selectable__check" width="20" height="20">
    <!-- checkmark icon -->
  </svg>
</button>
```

```css
.list-item-selectable {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 56px;
  padding: var(--spacing-lg);
  background: none;
  border: none;
  border-bottom: 1px solid var(--color-border-base);
  text-align: left;
  cursor: pointer;
  transition: var(--transition-background);
}

.list-item-selectable:hover {
  background-color: var(--color-neutral-100);
}

.list-item-selectable__text {
  font-size: var(--font-size-body-lg);
  font-weight: var(--font-weight-regular);
  color: var(--color-text-primary);
}

.list-item-selectable__check {
  opacity: 0;
  color: var(--color-primary-base);
  transition: opacity var(--transition-fast);
}

.list-item-selectable--selected {
  background-color: var(--color-primary-light);
}

.list-item-selectable--selected .list-item-selectable__check {
  opacity: 1;
}
```

---

## Modal Components

### Bottom Sheet Modal

Modal that slides up from the bottom with rounded top corners.

#### Specifications:
- **Border Radius**: `var(--radius-modal)` (24px) on top corners
- **Background**: `var(--color-neutral-0)`
- **Shadow**: `var(--shadow-modal)`
- **Z-Index**: `var(--z-index-modal)`
- **Padding**: `var(--spacing-xl)`
- **Handle**: Optional drag handle at top

**Structure Only** (no animation details):

```html
<div class="modal-overlay">
  <div class="bottom-sheet">
    <div class="bottom-sheet__handle"></div>
    <div class="bottom-sheet__header">
      <h2 class="bottom-sheet__title">Sort by</h2>
      <button class="bottom-sheet__close" aria-label="Close">
        <svg width="24" height="24"><!-- X icon --></svg>
      </button>
    </div>
    <div class="bottom-sheet__content">
      <!-- List items, form content, etc. -->
    </div>
  </div>
</div>
```

```css
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: var(--z-index-overlay);
  display: flex;
  align-items: flex-end;
}

.bottom-sheet {
  width: 100%;
  max-height: 80vh;
  background-color: var(--color-neutral-0);
  border-radius: var(--radius-modal) var(--radius-modal) 0 0;
  box-shadow: var(--shadow-modal);
  z-index: var(--z-index-modal);
  overflow: hidden;
  display: flex;
  flex-direction: column;
}

.bottom-sheet__handle {
  width: 40px;
  height: 4px;
  background-color: var(--color-neutral-300);
  border-radius: var(--radius-pill);
  margin: var(--spacing-md) auto var(--spacing-sm);
}

.bottom-sheet__header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: var(--spacing-lg) var(--spacing-xl);
  border-bottom: 1px solid var(--color-border-base);
}

.bottom-sheet__title {
  font-size: var(--font-size-heading-lg);
  font-weight: var(--font-weight-semibold);
  color: var(--color-text-primary);
}

.bottom-sheet__close {
  width: var(--size-icon-lg);
  height: var(--size-icon-lg);
  display: flex;
  align-items: center;
  justify-content: center;
  background: none;
  border: none;
  cursor: pointer;
  color: var(--color-text-secondary);
}

.bottom-sheet__content {
  flex: 1;
  overflow-y: auto;
  padding: var(--spacing-xl);
}
```

---

## Map Components

### Map Cluster Badge

Circular badge displaying number of clustered map markers.

#### Specifications:
- **Background**: `var(--color-secondary-base)` (green)
- **Text Color**: `var(--color-text-inverse)` (white)
- **Border Radius**: `var(--radius-round)` (50%)
- **Min Width/Height**: 32px
- **Padding**: `var(--spacing-xs) var(--spacing-sm)`
- **Font**: `var(--font-size-body-md)` with `var(--font-weight-bold)`
- **Shadow**: `var(--shadow-elevation-2)`

```html
<div class="map-cluster-badge">12</div>
```

```css
.map-cluster-badge {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-width: 32px;
  min-height: 32px;
  padding: var(--spacing-xs) var(--spacing-sm);
  background-color: var(--color-secondary-base);
  color: var(--color-text-inverse);
  border-radius: var(--radius-round);
  font-size: var(--font-size-body-md);
  font-weight: var(--font-weight-bold);
  box-shadow: var(--shadow-elevation-2);
}

/* Variant for larger clusters */
.map-cluster-badge--large {
  min-width: 48px;
  min-height: 48px;
  font-size: var(--font-size-heading-md);
}
```

---

## Buttons

### Primary Button (Updated with tokens)

```css
.btn-primary {
  background-color: var(--color-primary-base);
  color: var(--color-neutral-0);
  border-radius: var(--radius-button);
  padding: var(--spacing-button-padding-y) var(--spacing-button-padding-x);
  height: var(--size-button-height-lg);
  font-size: var(--font-size-body-lg);
  font-weight: var(--font-weight-semibold);
  font-family: var(--font-family-primary);
  border: none;
  cursor: pointer;
  transition: var(--transition-background), var(--transition-shadow);
}

.btn-primary:hover {
  background-color: var(--color-primary-hover);
  box-shadow: var(--shadow-elevation-1);
}

.btn-primary:active {
  background-color: var(--color-primary-active);
  transform: scale(0.98);
}

.btn-primary:disabled {
  background-color: var(--color-bg-disabled);
  color: var(--color-text-disabled);
  cursor: not-allowed;
}
```

---

## Icons

### Icon System (Updated)

All existing icons plus new context-specific icons:

**Navigation Icons** (24px):
- Home (filled/outline)
- Calendar (filled/outline)
- Heart/Favorites (filled/outline)
- Chat/Messages (filled/outline)
- Profile/User (filled/outline)

**Action Icons** (24px):
- Search/Magnifying glass
- Filter/Funnel
- Close/X
- Back/Chevron left
- Forward/Chevron right
- Sort (up/down arrows)

**Location Icons**:
- Location pin (16px, 24px)
- Nearby/Target location (24px)

**Time Icons**:
- Clock (20px)

**Map Icons**:
- Map pin markers
- Cluster circles (numeric badges)

---

## Spacing System

*[Existing spacing system remains, now with additional component-specific spacing tokens]*

---

## Layout Grid

*[Existing grid system remains]*

---

## Responsive Patterns

### Mobile-First Approach

All components are designed mobile-first with responsive enhancements.

#### Category Grid Pattern
```css
.category-grid {
  display: grid;
  gap: var(--spacing-lg);
  padding: var(--spacing-lg);

  /* Mobile: 2 columns */
  grid-template-columns: repeat(2, 1fr);

  /* Tablet: 3 columns */
  @media (min-width: 640px) {
    grid-template-columns: repeat(3, 1fr);
    padding: var(--spacing-2xl);
  }

  /* Desktop: 4 columns */
  @media (min-width: 1024px) {
    grid-template-columns: repeat(4, 1fr);
    max-width: var(--size-container-max);
    margin: 0 auto;
  }
}
```

#### Horizontal Scroll Pattern
```css
.horizontal-scroll {
  display: flex;
  gap: var(--spacing-lg);
  overflow-x: auto;
  overflow-y: hidden;
  scroll-snap-type: x mandatory;
  scrollbar-width: none;
  -webkit-overflow-scrolling: touch;
  padding: var(--spacing-md) var(--spacing-lg);
}

.horizontal-scroll::-webkit-scrollbar {
  display: none;
}

.horizontal-scroll > * {
  scroll-snap-align: start;
  flex-shrink: 0;
}
```

---

## Accessibility

### Requirements:
- **Color Contrast**: Minimum 4.5:1 for normal text, 3:1 for large text
- **Focus Indicators**: Visible on all interactive elements (2px outline, 2px offset)
- **Alt Text**: Required for all images
- **ARIA Labels**: Required for icon-only buttons
- **Keyboard Navigation**: Full support required
- **Touch Targets**: Minimum 44×44px for mobile

### Interactive Element Focus States:
```css
.interactive-element:focus-visible {
  outline: 2px solid var(--color-border-focus);
  outline-offset: 2px;
}
```

---

## AI Assistant Instructions

### Platform-Specific Prompts

#### For Cursor / Claude / GPT-4

**General Component Generation:**
```
Create a [component name] for a kids activities platform using the design system tokens:

Component: [e.g., Search Input with back button]
Tokens to use:
- Colors: var(--color-primary-base), var(--color-neutral-0)
- Spacing: var(--spacing-input-padding), var(--spacing-md)
- Typography: var(--font-size-body-lg), var(--font-weight-regular)
- Border radius: var(--radius-input)
- Shadow: var(--shadow-elevation-1)
- Transitions: var(--transition-all)

Requirements:
1. Mobile-first responsive
2. All interactive states (hover, focus, active, disabled)
3. ARIA labels for accessibility
4. Semantic HTML
5. BEM naming convention

Output: HTML and CSS using design tokens
```

**Search Results Page Example:**
```
Generate a search results page with:

Layout:
- Search header with back button (use search-header component)
- Filter chips row (Category, Offers, More Filters)
- Results count: "25 classes was found" with sort button
- Grid of search result cards (use card-search-result component)
- Bottom navigation

Styling:
- Container: max-width var(--size-container-md), padding var(--spacing-lg)
- Card grid: 1 column mobile, 2 columns tablet, 3 columns desktop
- Gap: var(--spacing-card-gap)
- Use existing component styles from design system

Include:
- Empty state (no results found)
- Loading skeleton state
- Sort modal (bottom sheet)
```

#### For Google AI Studio / Gemini

**Component with State Management:**
```
Context: Kids activities booking platform with design tokens defined
Task: Create FilterChips component with selection state

Specifications:
- Component: Filter chips (Category, Offers, More Filters)
- Default state: White background, gray border
- Selected state: Green background (var(--color-secondary-base)), white text
- Tokens: Use var(--radius-chip), var(--spacing-sm), var(--font-size-body-md)
- Interaction: Single or multiple selection (specify)
- Accessibility: ARIA selected attribute, keyboard navigation

Technology: [React/Vue/Vanilla JS]
Output: Component code with state handling and design tokens
```

**Form Component:**
```
Create a location search input component:

Features:
- Input field with placeholder "What is your location"
- Back button (left)
- Search icon button (right)
- Recent searches list below
- Location autocomplete suggestions

Tokens:
- Input: var(--size-input-height-sm), var(--radius-input)
- Icons: var(--size-icon-lg), var(--size-icon-md)
- List items: search-history-item component style
- Colors: var(--color-neutral-0) background, var(--color-border-base)

Include:
- Debounced search
- Click handlers for history items
- ARIA live region for autocomplete
```

### Testing Checklist for AI-Generated Code

```markdown
## Component Review Checklist

### Design Tokens ✓
- [ ] All colors use CSS custom properties (no hex codes)
- [ ] Spacing uses var(--spacing-*) tokens
- [ ] Typography uses token font sizes and weights
- [ ] Border radius uses var(--radius-*) tokens
- [ ] Shadows use var(--shadow-*) tokens
- [ ] Transitions use var(--transition-*) tokens

### Responsive Design ✓
- [ ] Mobile-first approach
- [ ] Breakpoints use token values
- [ ] Touch targets minimum 44×44px
- [ ] Horizontal scroll works on mobile

### Accessibility ✓
- [ ] Semantic HTML elements used
- [ ] All images have alt text
- [ ] Icon-only buttons have ARIA labels
- [ ] Focus states visible (2px outline)
- [ ] Keyboard navigation works
- [ ] Color contrast meets WCAG AA (4.5:1)

### Interactive States ✓
- [ ] Hover state defined
- [ ] Active state defined
- [ ] Focus state defined
- [ ] Disabled state defined (if applicable)
- [ ] Loading state defined (if applicable)

### Code Quality ✓
- [ ] BEM naming convention
- [ ] No inline styles
- [ ] No !important declarations
- [ ] Reusable component structure
- [ ] Comments for complex logic only
```

### Common Component Patterns

#### Pattern 1: Card Grid with Horizontal Scroll (Mobile)
```css
.card-container {
  padding: var(--spacing-lg);
}

.card-grid {
  display: grid;
  gap: var(--spacing-lg);
  grid-template-columns: 1fr;
}

/* Mobile: Horizontal scroll */
@media (max-width: 639px) {
  .card-grid--scroll-mobile {
    display: flex;
    overflow-x: auto;
    scroll-snap-type: x mandatory;
    gap: var(--spacing-md);
  }

  .card-grid--scroll-mobile > * {
    scroll-snap-align: start;
    flex-shrink: 0;
  }
}

/* Tablet: 2 columns */
@media (min-width: 640px) {
  .card-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Desktop: 3-4 columns */
@media (min-width: 1024px) {
  .card-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
```

#### Pattern 2: Search Page Layout
```html
<div class="search-page">
  <header class="search-header">
    <!-- Back + Input + Search Icon -->
  </header>

  <div class="search-page__filters">
    <!-- Filter chips -->
  </div>

  <div class="search-page__results">
    <div class="results-header">
      <p class="results-count">25 classes was found</p>
      <button class="results-sort"><!-- Sort icon --></button>
    </div>

    <div class="card-grid">
      <!-- Search result cards -->
    </div>
  </div>

  <nav class="bottom-nav">
    <!-- Bottom navigation -->
  </nav>
</div>
```

#### Pattern 3: Hero with Categories
```html
<div class="homepage">
  <section class="hero">
    <h1 class="hero__heading">Discover</h1>
    <!-- Search input -->

    <div class="category-pills horizontal-scroll">
      <!-- Category icon pills -->
    </div>
  </section>

  <main class="homepage__content">
    <!-- Section headers + content -->
  </main>

  <nav class="bottom-nav">
    <!-- Bottom navigation -->
  </nav>
</div>
```

---

## Component Composition Guide

### Building Complex Layouts from Components

#### Search Results Page
```
Components used:
1. Search Header (search-header)
2. Filter Chips (chip × 3)
3. Section Header (section-header) - for results count
4. Search Result Card (card-search-result) × n
5. Bottom Sheet Modal (bottom-sheet) - for sort options
6. List Item Selectable (list-item-selectable) - inside modal
7. Bottom Navigation (bottom-nav)
```

#### Homepage
```
Components used:
1. Hero Section (hero)
2. Search Input (search-input)
3. Category Pills (horizontal scroll)
4. Section Header (section-header) × multiple
5. Activity Card Small (activity-card-small) × n
6. Bottom Navigation (bottom-nav)
```

#### Category Selection
```
Components used:
1. Hero Section (hero) - with large text variant
2. Location Bar (location-bar)
3. Category Card Grid (category-card--grid) × 6
   OR Category Card List (category-card--list) × n
```

---

## Version History
- **v1.0** - Initial design system (January 10, 2026)
- **v1.1** - Added design tokens and token-based implementation (January 10, 2026)
- **v1.2** - Added 12 new components from screen designs, enhanced AI instructions (January 11, 2026)
  - Search Input (3 variants)
  - Filter Chips
  - Bottom Navigation
  - Location Bar
  - Hero Section
  - Section Header
  - Category Card (Grid & List)
  - Activity Card Small
  - Search History Item
  - List Item Selectable
  - Bottom Sheet Modal
  - Map Cluster Badge

---

## Support & Maintenance

For questions or updates to this style guide, refer to the original design files or contact the design team.

### File References
- Styleguide UI Cards: `Styleguide-UI-Cards-Popular.jpg`, `Styleguide-UI-Cards-Search-Result.jpg`
- Styleguide Components: `Style-Guide-Button.jpg`, `Style-Guide-Text.jpg`, `Style-guide-Icons.jpg`
- Screen Designs: `1.1.1-Home.jpg`, `1.2.1-Search-Location.jpg`, `1.3.1-Search-Categories.jpg`, `2.1.1-Search-Results.jpg`
