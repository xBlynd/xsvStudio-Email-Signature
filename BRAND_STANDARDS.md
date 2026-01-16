# xsvStudio Email Signature Brand Standards
## Visual Identity & Technical Specifications

**Document Status:** Active Reference  
**Last Updated:** January 16, 2026  
**Applies To:** All email signatures across xsvStudio divisions

---

## 🎨 Logo Specifications

### Primary Logo: "xsvStudio."

**Text Composition:**
- Full text: `xsvStudio.` (period is critical)
- Three color segments:
  - "xsv" → Arctic Steel
  - "Studio" → Violet
  - "." (period) → Burnt Coral

**Typography:**
- Font Family: Inter (primary), Arial Bold (fallback)
- Font Weight: 700 (bold)
- Letter Spacing: -1px (tight, modern)
- Style: Geometric sans-serif

---

## 🌈 Official Color Palette

### Core Brand Colors

| Element | Color Name | Hex Code | RGB | Usage |
|---------|-----------|----------|-----|-------|
| "xsv" text | Arctic Steel | `#8b9dc3` | RGB(139, 157, 195) | Logo first segment |
| "Studio" text | Violet | `#5c5edc` | RGB(92, 94, 220) | Logo main segment, accent color |
| "." period | Burnt Coral | `#ff6b6b` | RGB(255, 107, 107) | Logo period, call-to-action |
| Primary Background | Charcoal | `#121212` | RGB(18, 18, 18) | Dark mode primary |
| Text Primary | White | `#ffffff` | RGB(255, 255, 255) | Main text on dark |
| Text Secondary | Light Gray | `#e0e0e0` | RGB(224, 224, 224) | Secondary text |

### Supporting Colors

| Purpose | Color Name | Hex Code | Usage |
|---------|-----------|----------|-------|
| Links | Link Blue | `#5c5edc` | Hyperlinks (matches Violet) |
| Hover State | Bright Violet | `#7678e8` | Interactive element hover |
| Divider | Steel Gray | `#444444` | Horizontal rules, borders |

---

## 📐 Logo Dimensions & Formats

### Email Signature Specific Sizes

**Desktop Email:**
- Primary logo: 200px × 50px (PNG/SVG)
- Social icons: 24px × 24px (PNG)
- Profile picture: 80px × 80px (1:1 ratio, square)

**Mobile Email:**
- Primary logo: 150px × 38px (scales down)
- Social icons: 20px × 20px
- Profile picture: 60px × 60px

**File Size Limits:**
- Each image: <50KB (strict)
- Total signature assets: <150KB combined
- Use TinyPNG or ImageOptim for compression

---

## 🖼️ Logo Variants Required

### 1. Primary Logo (xsvStudio.)
```
Filename: xsvstudio-logo-primary-200px.png
Size: 200px × 50px
Background: Transparent
Format: PNG (24-bit with alpha)
Usage: Main email signature logo
Special: White stroke (2px) on all text for dark mode
```

### 2. Compact Logo (xsv.)
```
Filename: xsvstudio-logo-compact-100px.png
Size: 100px × 30px
Background: Transparent
Format: PNG (24-bit with alpha)
Usage: Mobile email signatures
Special: Same white stroke treatment
```

### 3. Division Logos
**Format:** xsvStudio.[Division]

Examples:
- xsvStudio.healthcare
- xsvStudio.industrial
- xsvStudio.technology
- xsvStudio.legal

**Specifications:**
- Base logo + division name in secondary color
- Division text: 60% opacity of Violet (#5c5edc)
- Size: 250px × 60px
- Same white stroke treatment

---

## 🌗 Dark Mode Adaptation Strategy

### The Problem
Email clients automatically invert colors in dark mode, which can:
- Make white-background logos appear as bright boxes
- Cause dark text to disappear on dark backgrounds
- Break visual hierarchy

### The Solution
**White Stroke/Glow Technique:**
1. Use transparent PNG backgrounds (never white)
2. Add 2px white stroke to ALL text elements
3. White stroke is invisible on light backgrounds
4. White stroke creates contrast on dark backgrounds

**Implementation:**
```css
/* SVG method */
stroke="#ffffff" 
stroke-width="2" 
paint-order="stroke fill"

/* Or export from design software with stroke */
```

**Color Choices:**
- Our Violet (#5c5edc) works on BOTH light and dark
- Our Coral (#ff6b6b) works on BOTH light and dark
- Our Arctic Steel (#8b9dc3) needs white stroke for dark mode

---

## 🔤 Typography Rules

### Email Body Text
- Font Family: Arial, Helvetica, sans-serif (web-safe)
- Font Size: 14px (body text)
- Line Height: 1.5 (readable)
- Color: #333333 (light mode), #e0e0e0 (dark mode)

### Name/Title Text
- Font Weight: 700 (bold)
- Font Size: 16px (name), 14px (title)
- Color: #1a1d29 (light mode), #ffffff (dark mode)

### Links
- Font Weight: 400 (regular)
- Color: #5c5edc (our brand Violet)
- Text Decoration: none (remove underline)
- Hover: #7678e8 (lighter violet)

---

## 📏 Layout Standards

### Desktop Signature Layout
```
┌─────────────────────────────────────┐
│ [LOGO]   Name                       │
│          Title | Division            │
│          ────────────────            │
│          📧 email | 📞 phone         │
│          🌐 website                  │
│          [social icons]              │
└─────────────────────────────────────┘

Max Width: 600px
Table-based layout (for email compatibility)
```

### Mobile Signature Layout
```
┌──────────────────┐
│    [LOGO]        │
│    Name          │
│    Title         │
│    ───────       │
│    📧 email      │
│    🌐 website    │
│    [icons]       │
└──────────────────┘

Max Width: 320px
Stacked layout
```

---

## 🎯 Social Media Icons

### Required Icons (To Be Designed)
- [ ] LinkedIn (primary)
- [ ] Website link (custom icon)
- [ ] Optional: Twitter/X, GitHub (if applicable)

**Specifications:**
- Size: 24px × 24px (desktop), 20px × 20px (mobile)
- Style: Line icons (not filled)
- Colors: Match brand palette
- Background: Transparent PNG
- Hover state: Violet (#5c5edc)

**Naming Convention:**
```
icon-linkedin-24px.png
icon-website-24px.png
icon-linkedin-hover-24px.png
```

---

## 📦 File Naming Conventions

### Standard Format
```
[brand]-[type]-[variant]-[size].[ext]

Examples:
xsvstudio-logo-primary-200px.png
xsvstudio-logo-primary-200px.svg
xsvstudio-logo-division-healthcare-250px.png
xsvstudio-icon-linkedin-24px.png
```

### Asset Organization
```
assets/
├── logos/
│   ├── primary/
│   │   ├── xsvstudio-logo-primary-200px.png
│   │   ├── xsvstudio-logo-primary-200px.svg
│   │   ├── xsvstudio-logo-primary-150px.png (mobile)
│   │   └── xsvstudio-logo-compact-100px.png
│   └── divisions/
│       ├── xsvstudio-logo-healthcare-250px.png
│       ├── xsvstudio-logo-industrial-250px.png
│       └── xsvstudio-logo-technology-250px.png
├── icons/
│   ├── social/
│   │   ├── icon-linkedin-24px.png
│   │   ├── icon-linkedin-20px.png (mobile)
│   │   └── icon-website-24px.png
│   └── utility/
│       ├── icon-email-16px.png
│       └── icon-phone-16px.png
└── optimized/
    └── [production-ready compressed versions]
```

---

## ✅ Quality Checklist

Before any asset is considered "complete":

**Visual:**
- [ ] Colors match exact hex codes
- [ ] Typography follows specifications
- [ ] White stroke applied to dark elements
- [ ] Transparent background (no white box)
- [ ] Tested on both light and dark backgrounds

**Technical:**
- [ ] File size <50KB per image
- [ ] Correct dimensions (exact pixels)
- [ ] PNG: 24-bit with alpha channel
- [ ] SVG: Clean code, no unnecessary elements
- [ ] Optimized with TinyPNG or ImageOptim

**Testing:**
- [ ] Renders correctly in email preview
- [ ] Looks good on light mode
- [ ] Looks good on dark mode
- [ ] Scales properly on mobile
- [ ] No blurriness or artifacts

---

## 🚫 What NOT to Do

**❌ NEVER:**
- Use white or solid color backgrounds (breaks dark mode)
- Use pure black text (#000000) - disappears in dark mode
- Mix font weights inconsistently
- Use Comic Sans or non-web-safe fonts
- Create logos without white stroke on dark elements
- Exceed 50KB per image file
- Use JPG for logos (PNG or SVG only)
- Center-align everything (asymmetry = custom)

**✅ ALWAYS:**
- Use transparent backgrounds
- Include white stroke on dark colors
- Test on both light and dark mode
- Optimize file sizes
- Follow naming conventions
- Maintain brand color accuracy

---

## 🔗 External References

**Design Inspiration:**
- [xsvstudio.com](https://www.xsvstudio.com) - Main website aesthetic
- CustomEsignature.com - Animation inspiration
- Stripe.com - Clean signature design
- Linear.app - Minimalist approach

**Technical Resources:**
- [Dark Mode Email Guide](https://signature.email/guides/how-to-prepare-email-signature-dark-mode)
- [Litmus Dark Mode Guide](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers)
- [Mobile Email Best Practices](https://signature.email/guides/how-to-make-mobile-email-signature)

---

## 📝 Version History

| Version | Date | Changes | Author |
|---------|------|---------|--------|
| 1.0.0 | 2026-01-16 | Initial brand standards document | Ian Martin |

---

**Maintained By:** xsvStudio Digital Design Team  
**Questions?** Create a GitHub Issue or contact Ian Martin  
**Last Review:** January 16, 2026