# MyPetFriends Design System Guide

## Brand Identity

- **Brand Name:** MyPetFriends
- **Tagline:** Building a better way for local pet sitters to connect with pet owners
- **Location:** Cape Town
- **Emoji/Icon:** 🐾 (paw print - always precedes brand name)

---

## Color Palette

### Primary Colors

| Color | Hex | Usage |
|-------|-----|-------|
| Pink | `#FFB6C1` | Primary brand color, used for CTAs, navigation bar, feature cards |
| Blue | `#A8D8EA` | Secondary color, used for feature cards, CTA sections |
| Sage Green | `#B8D4B8` | Accent color, used for feature cards, success messages |

### Supporting Colors

| Color | Hex | Usage |
|-------|-----|-------|
| Yellow/Cream | `#F4D49E` | Used for feature cards, "How It Works" section backgrounds |
| Cream/Off-white | `#FFF5E6` | Light background for About section |
| White | `#FFFFFF` | Main background, hero section, form backgrounds |
| Dark Gray | `#2C2C2C` | Primary text color |
| Medium Gray | `#555555` | Secondary text color |
| Light Gray | `#999999` | Placeholder text, disabled states |

### Color Usage Rules

- Never use gradients or color transitions - always use solid color blocks
- Color blocking style: Sections should have clean, flat colors that butt up against each other without transitions
- Pastels only: Keep all colors soft and pastel - nothing harsh or saturated
- No consecutive same colors: When using multiple colored elements (like carousel or cards), alternate colors so no two of the same color appear next to each other

---

## Typography

### Font Families

**Primary (Headings): Poppins**
- Weights: 400 (regular), 500 (medium), 600 (semi-bold), 700 (bold)
- Import: `https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap`

**Secondary (Body): Montserrat**
- Weights: 400 (regular), 500 (medium), 600 (semi-bold)
- Import: `https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600&display=swap`

### Font Sizes & Usage

#### Desktop

| Element | Size | Font |
|---------|------|------|
| H1 (Hero) | 3.5rem (56px) | Poppins Bold |
| H2 (Sections) | 2.5rem (40px) | Poppins Semi-bold |
| H3 (Cards/Features) | 1.5rem (24px) | Poppins Semi-bold |
| Body Large | 1.25rem (20px) | Montserrat Regular |
| Body Regular | 1.15rem (18.4px) | Montserrat Regular |
| Body Default | 1rem (16px) | Montserrat Regular |
| Small Text | 0.9rem (14.4px) | Montserrat Regular |

#### Tablet (max-width: 768px)

| Element | Size |
|---------|------|
| H1 | 2rem (32px) |
| H2 | Keep at 2.5rem |
| Body | 1rem |

#### Mobile (max-width: 480px)

| Element | Size |
|---------|------|
| H1 | 1.75rem (28px) |
| Body | 1rem |

### Line Height

- Headings: `1.2`
- Body text: `1.6`
- Success/error messages: `1.8`

---

## Spacing & Layout

### Section Padding

#### Desktop
- Vertical: 6rem (96px) top and bottom
- Horizontal: 2rem (32px) left and right

#### Tablet
- Vertical: 3rem (48px)
- Horizontal: 1rem (16px)

#### Mobile
- Vertical: 3rem
- Horizontal: 1rem

### Content Width

- Maximum container width: `1200px`
- Centered content (text-focused sections): `800px - 1000px`
- Form containers: `700px` max-width
- Always center content with `margin: 0 auto`

### Element Spacing

- Between sections: Natural flow (padding handles this)
- Within sections: `3rem - 4rem` between major elements
- Card gaps: `2rem - 3rem`
- Form field margins: `1.5rem` bottom margin

### Border Radius

| Element | Radius |
|---------|--------|
| Buttons | 50px (fully rounded) |
| Cards/Containers | 20px |
| Form inputs | 10px |
| Carousel items | 15px |
| Success/error messages | 10px |

---

## Components

### Buttons (CTAs)

```css
background: #FFB6C1; /* pink */
color: white;
padding: 1rem 2.5rem;
font-family: Poppins;
font-size: 1.1rem;
font-weight: 600;
border-radius: 50px;
box-shadow: 0 4px 15px rgba(255, 182, 193, 0.3);
transition: all 0.3s;
```

**Hover state:**
```css
transform: translateY(-2px);
box-shadow: 0 6px 20px rgba(255, 182, 193, 0.4);
background: #FF9FB0; /* slightly darker pink */
```

**Mobile adjustments:**
- Font-size: `1rem`
- Padding: `0.875rem 2rem`

### Navigation Bar

```css
background: #FFB6C1; /* pink */
padding: 1.5rem 2rem;
position: sticky;
top: 0;
box-shadow: 0 2px 10px rgba(0,0,0,0.08);
```

**Logo:**
```css
font-family: Poppins;
font-size: 1.5rem;
font-weight: 600;
color: white;
```

**Links:**
```css
color: white;
font-weight: 500;
transition: opacity 0.3s;
```

**Hover:** `opacity: 0.8`

**Mobile:** Hide nav links, show only logo

### Cards/Feature Blocks

```css
padding: 2.5rem;
border-radius: 20px;
text-align: center;
transition: transform 0.3s;
```

**Hover:** `transform: translateY(-5px)`

**Backgrounds:** Rotate between pink, blue, sage green

**Title:**
```css
font-size: 1.5rem;
font-family: Poppins;
font-weight: 600;
color: white;
margin-bottom: 1rem;
```

**Body:**
```css
font-size: 1rem;
color: white;
opacity: 0.95;
```

### Form Inputs

```css
width: 100%;
padding: 0.875rem 1rem;
font-family: Montserrat;
font-size: 1rem;
border: 2px solid #E0E0E0;
border-radius: 10px;
transition: border-color 0.3s;
background: white;
```

**Focus state:**
```css
outline: none;
border-color: #FFB6C1; /* pink */
```

**Labels:**
```css
font-family: Poppins;
font-size: 1rem;
font-weight: 500;
color: #2C2C2C;
margin-bottom: 0.5rem;
```

**Required indicator (*):** `color: #FFB6C1` (pink)

### Success Messages

```css
background: #B8D4B8; /* sage */
color: white;
padding: 2.5rem;
border-radius: 10px;
text-align: center;
font-size: 1.1rem;
line-height: 1.8;
animation: slideDown 0.5s ease;
```

---

## Shadows

| Type | Value |
|------|-------|
| Light shadow (cards, buttons) | `0 4px 15px rgba(0, 0, 0, 0.1)` |
| Medium shadow (hover states) | `0 6px 20px rgba(0, 0, 0, 0.15)` |
| Colored shadow (pink buttons) | `0 4px 15px rgba(255, 182, 193, 0.3)` |
| Nav shadow | `0 2px 10px rgba(0,0,0,0.08)` |

---

## Responsive Breakpoints

```css
/* Tablet */
@media (max-width: 768px) {
    /* Adjust font sizes, hide nav links, reduce padding */
}

/* Mobile */
@media (max-width: 480px) {
    /* Further reduce font sizes, minimal padding */
}
```

### Key Responsive Rules

1. Always test on mobile first
2. Stack grid layouts to single column on mobile
3. Reduce padding progressively (desktop → tablet → mobile)
4. Scale down font sizes but maintain readability
5. Hide navigation links on mobile (or use hamburger menu)
6. Ensure touch targets are at least 44px × 44px on mobile

---

## Design Principles

### 1. Minimalism & Cleanliness
- Lots of white space
- Don't overcrowd sections
- Let content breathe
- Avoid clutter

### 2. Color Blocking
- Use solid, flat colors for section backgrounds
- No gradients or smooth transitions between colors
- Sections should have clear, distinct color boundaries
- Alternate colors to create visual interest

### 3. Authenticity
- Avoid corporate/marketing speak
- Write conversationally, like talking to a friend
- Be honest about where you are (early stage)
- Use real language, not buzzwords

### 4. Warmth & Friendliness
- Pastel colors create a soft, approachable feel
- Pet emojis (🐾) add personality
- Rounded corners everywhere (never sharp edges)
- Gentle shadows (never harsh)

### 5. Centered & Balanced
- Most content is centered
- Use max-widths to prevent content from stretching too wide
- Equal padding on left and right
- Maintain visual hierarchy

### 6. Smooth Interactions
- All transitions: `0.3s` ease or `0.3s`
- Hover states should be subtle (slight lift, color change, opacity)
- Animations should be purposeful, not distracting
- Use `transform: translateY(-2px)` for lift effect

---

## Animations

### Hover Effects

```css
transition: all 0.3s;
transform: translateY(-2px); /* lift effect */
opacity: 0.8; /* fade effect */
```

### Slide Down (messages)

```css
@keyframes slideDown {
    from {
        opacity: 0;
        transform: translateY(-10px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
```

### Carousel Scroll

```css
animation: scroll 50s linear infinite;

@keyframes scroll {
    0% { transform: translateX(0); }
    100% { transform: translateX(calc(-180px * 10 - 1rem * 10)); }
}
```

---

## Footer

```css
background: #2C2C2C; /* dark gray */
color: white;
padding: 3rem 2rem 2rem;
text-align: center;
```

- **Logo:** Poppins, 1.5rem, weight 600
- **Body:** Opacity 0.8
- **Links:** Opacity 0.8, transition opacity 0.3s
- **Copyright:** 0.9rem, margin-top 2rem

---

## Content Guidelines

### Voice & Tone

- **Conversational:** Write like you're talking to a friend
- **Honest:** Be transparent about being early-stage
- **Warm:** Welcoming and inclusive
- **Not salesy:** Avoid hype, marketing jargon, or corporate speak

### Writing Style

- Use short paragraphs (2-3 sentences max)
- Break up text with spacing
- Use "we" when talking about the team
- Use "you" when addressing pet sitters
- Emoji usage: Sparingly - only the 🐾 paw print for brand consistency

### Example Good Copy

✅ "We're at the very beginning, and we want to build this WITH you, not just FOR you."

✅ "Full transparency: We're very early."

✅ "Let's build something better together."

### Example Bad Copy

❌ "Join thousands of satisfied pet sitters!"

❌ "Revolutionary platform disrupting the pet care industry"

❌ "Maximize your earning potential with our innovative solution"

---

## Image Guidelines

### Carousel/Featured Images

- Use real pet photos (no stock photos if possible)
- Pastel color backgrounds (pink, blue, sage, yellow/cream)
- Square format (maintain 1:1 ratio)
- Clean, uncluttered backgrounds
- Alternate background colors so no two of the same color appear consecutively

### Image Treatment

- Rounded corners: `15px` border-radius
- Subtle shadows: `0 4px 15px rgba(0, 0, 0, 0.1)`
- Size: 180px × 180px (desktop), scale down for mobile

---

## Grid Layouts

### Feature Cards

```css
display: grid;
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
gap: 2rem;
```

**Mobile:** `grid-template-columns: 1fr;`

### Two-Column Layouts

- Use `display: flex` with equal width columns
- Gap: `4rem` between columns
- Stack on mobile (switch to `flex-direction: column`)

---

## Don'ts (What to Avoid)

### ❌ Don't use:

- Gradients or color transitions
- Stock corporate imagery
- Harsh, saturated colors
- Sharp corners (everything should be rounded)
- Heavy, dark shadows
- Multiple font families (stick to Poppins + Montserrat)
- Marketing jargon or hype language
- Animated GIFs or flashy effects
- Auto-playing videos
- Pop-ups or intrusive modals

### ❌ Don't:

- Make the user feel pressured
- Over-promise features you don't have yet
- Use all caps for headings (except acronyms)
- Put too much text in one paragraph
- Use bullet points unless listing specific items
- Create forms with more than 6 fields

---

## File Structure Best Practices

If creating multiple pages:

```
index.html (landing page)
about.html (about/story page)
how-it-works.html (how it works page)
styles.css (shared styles - extract from inline)
```

### Keep Consistent:

- Same navigation on every page
- Same footer on every page
- Same color palette across all pages
- Same font usage
- Same spacing rules

---

## Testing Checklist

Before launching any new page, test:

- [ ] Desktop (1920px, 1440px, 1280px)
- [ ] Tablet (768px)
- [ ] Mobile (480px, 375px, 320px)
- [ ] All links work
- [ ] All forms submit correctly
- [ ] All images load
- [ ] Text is readable on all backgrounds
- [ ] Buttons are clickable on mobile
- [ ] No horizontal scroll on any device
- [ ] Consistent spacing throughout

---

## Quick Reference

### Brand Colors

| Name | Hex |
|------|-----|
| Pink | `#FFB6C1` |
| Blue | `#A8D8EA` |
| Sage | `#B8D4B8` |
| Yellow | `#F4D49E` |
| Dark | `#2C2C2C` |

### Fonts

- **Headings:** Poppins
- **Body:** Montserrat

### Key Sizes

| Element | Size |
|---------|------|
| Max content width | 1200px |
| Section padding | 6rem vertical |
| Button radius | 50px |
| Card radius | 20px |
| Input radius | 10px |

### Shadows

| Type | Value |
|------|-------|
| Light | `0 4px 15px rgba(0, 0, 0, 0.1)` |
| Medium | `0 6px 20px rgba(0, 0, 0, 0.15)` |

### Transitions

- **Standard:** `all 0.3s`
- **Hover lift:** `transform: translateY(-2px)`
