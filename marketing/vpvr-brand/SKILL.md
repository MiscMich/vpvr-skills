---
name: vpvr-brand
description: Villa Paraiso Vacation Rentals brand styling for documents, web, emails, social, and video using expert brand methodology. Apply VPVR brand colors, typography (Montserrat/Cormorant for web, Helvetica Neue for print), logo, and 2025/26 platform specifications to any content. Includes accessibility standards, dark mode, video branding, and AI image integration.
---

# Villa Paraiso Vacation Rentals Brand Styling

Apply consistent VPVR brand identity across all channels and formats.

## Property & Asset Sources

**Fetch current assets from the VPVR website.** Properties and assets are updated regularly.

| Resource | URL | What You Get |
|----------|-----|--------------|
| **Logo SVG** | `https://paraisovacationrentals.com/wp-content/uploads/2024/03/villa-paraiso-logo.svg` | Current logo |
| **All Properties** | `https://paraisovacationrentals.com/properties/` | Current property list with photos |
| **Individual Property** | `https://paraisovacationrentals.com/property/[slug]/` | Property photos for branded materials |

**For branded materials**: Fetch property pages to get current photos and ensure consistency with live website.

---

## Expert Methodologies Incorporated

| Expert | Framework | Application |
|--------|-----------|-------------|
| **Marty Neumeier** | Brand Gap | Visual identity that bridges strategy and execution |
| **David Airey** | Logo Design Love | Logo usage, sizing, and protection zones |
| **Apple HIG** | Human Interface Guidelines | Accessibility, dark mode, responsive design |
| **Google Material** | Material Design 3 | Color systems, typography hierarchy |
| **WCAG 2.1** | Accessibility Guidelines | Contrast ratios, text sizing, color usage |

---

## Quick Reference

| Element | Value |
|---------|-------|
| Primary Color (Teal) | `#48A1AA` / RGB(72, 161, 170) |
| Secondary (Cream) | `#EEE5C7` / RGB(238, 229, 199) |
| Web/Email Font | **Montserrat** (fallback: Arial) |
| Heading Font | **Cormorant** (fallback: Georgia) |
| Print Font | Helvetica Neue (fallback: Arial) |
| Logo Size | **Always square** (e.g., 80×80px) |

---

## Brand Identity

**Company:** Villa Paraiso Vacation Rentals LLC
**Tagline:** *A Partnership in Premier Hospitality*
**Brand Voice:** "Four Seasons of vacation rentals" - luxury without pretension, warm but professional

### Brand Personality (2025/26)

| Trait | Expression | Avoid |
|-------|------------|-------|
| **Luxurious** | Premium imagery, quality materials | Gaudy, excessive, pretentious |
| **Warm** | Personal touches, local stories | Cold, corporate, distant |
| **Professional** | Consistent, reliable, polished | Casual, sloppy, inconsistent |
| **Local** | Keys-specific, insider knowledge | Generic, cookie-cutter |
| **Authentic** | Real properties, real experiences | Stock photos, fake reviews |

---

## Brand Colors

### Primary Palette

| Color | Hex | RGB | Usage |
|-------|-----|-----|-------|
| Teal | `#48A1AA` | (72, 161, 170) | Primary accent, headers, logo, links, buttons |
| Accent Teal | `#44949C` | (68, 148, 156) | Hover states, secondary accents |
| Cream | `#EEE5C7` | (238, 229, 199) | Secondary accent, backgrounds, logo on dark |
| Off-White | `#F1ECEC` | (241, 236, 236) | Light backgrounds, subtle accents, email footers |
| Black | `#000000` | (0, 0, 0) | Body text |
| Dark Gray | `#333333` | (51, 51, 51) | Secondary text |

### Extended Palette (2025/26)

| Color | Hex | Usage |
|-------|-----|-------|
| Deep Teal | `#3A858C` | Dark mode primary, emphasis |
| Light Teal | `#7BC4CB` | Highlights, success states |
| Warm Sand | `#D4C9A8` | Backgrounds, warmth accents |
| Ocean Blue | `#2E6E7A` | Links on light backgrounds |
| Sunset Orange | `#E8945A` | Calls-to-action, urgency (sparingly) |

### Accessibility Color Pairings (WCAG AA Compliant)

| Background | Text Color | Contrast Ratio | Use Case |
|------------|------------|----------------|----------|
| White `#FFFFFF` | Teal `#48A1AA` | 3.4:1 | Large text only |
| White `#FFFFFF` | Black `#000000` | 21:1 | Body text ✅ |
| Teal `#48A1AA` | White `#FFFFFF` | 3.4:1 | Large text, buttons |
| Teal `#48A1AA` | Cream `#EEE5C7` | 2.5:1 | ❌ Avoid for text |
| Off-White `#F1ECEC` | Black `#000000` | 17.8:1 | Body text ✅ |

**Rule:** Body text must use Black (#000000) or Dark Gray (#333333) on light backgrounds for accessibility.

---

## Typography

### Web, Email, Social Media
```css
/* Primary (Body) */
font-family: 'Montserrat', Arial, sans-serif;

/* Headings */
font-family: 'Cormorant', Georgia, serif;
```

### Print Documents (Legacy)
```css
font-family: 'Helvetica Neue', Arial, sans-serif;
```

### Size Hierarchy

| Element | Size | Weight | Color | Font |
|---------|------|--------|-------|------|
| Document Title | 28pt | Bold | `#48A1AA` | Cormorant |
| Company Name | 24pt | Bold | `#000000` or `#48A1AA` | Cormorant |
| Tagline | 14pt | Italic | `#333333` | Montserrat |
| Heading 1 | 16pt | Bold | `#000000` | Cormorant |
| Heading 2 | 14pt | Bold | `#000000` | Cormorant |
| Heading 3 | 12pt | Bold | `#000000` | Montserrat |
| Body Text | 11pt | Regular | `#000000` | Montserrat |
| Footer | 10pt | Regular | `#333333` | Montserrat |

### Responsive Typography (2025/26)

| Viewport | Base Font | Scale Ratio |
|----------|-----------|-------------|
| Mobile (< 480px) | 16px | 1.2 (Minor Third) |
| Tablet (480-1024px) | 17px | 1.25 (Major Third) |
| Desktop (> 1024px) | 18px | 1.333 (Perfect Fourth) |

---

## Platform Dimensions (2025/26)

### Social Media Image Sizes

| Platform | Format | Dimensions | Aspect Ratio |
|----------|--------|------------|--------------|
| **Instagram Feed** | Square | 1080 × 1080 px | 1:1 |
| **Instagram Feed** | Portrait | 1080 × 1350 px | 4:5 |
| **Instagram Feed** | Landscape | 1080 × 566 px | 1.91:1 |
| **Instagram Story/Reel** | Vertical | 1080 × 1920 px | 9:16 |
| **TikTok** | Vertical | 1080 × 1920 px | 9:16 |
| **Facebook Post** | Landscape | 1200 × 630 px | 1.91:1 |
| **Facebook Cover** | Wide | 820 × 312 px | 2.63:1 |
| **LinkedIn Post** | Landscape | 1200 × 627 px | 1.91:1 |
| **YouTube Thumbnail** | Landscape | 1280 × 720 px | 16:9 |
| **YouTube Shorts** | Vertical | 1080 × 1920 px | 9:16 |
| **Pinterest Pin** | Vertical | 1000 × 1500 px | 2:3 |
| **Twitter/X Post** | Landscape | 1600 × 900 px | 16:9 |

### Safe Zones for Text Overlay

| Platform | Top Safe | Bottom Safe | Side Safe |
|----------|----------|-------------|-----------|
| Instagram Reels | 250px | 400px | 50px |
| TikTok | 150px | 500px | 50px |
| YouTube Shorts | 200px | 300px | 60px |

### Email Dimensions

| Element | Width | Height |
|---------|-------|--------|
| Email max-width | 600px | — |
| Header image | 600px | 200px |
| Hero image | 600px | 300-400px |
| Product image | 280px | 280px |
| Logo | 80px | 80px (square) |

---

## Video Branding (2025/26)

### Video Intro/Outro

| Element | Specification |
|---------|---------------|
| Duration | 2-3 seconds (intro), 3-5 seconds (outro) |
| Logo animation | Fade in, scale 0.8→1.0 |
| Background | Teal `#48A1AA` or property footage |
| Audio | Soft wave/chime (optional) |
| Text | "Villa Paraiso Vacation Rentals" in Cormorant |

### Lower Thirds

```
┌────────────────────────────────────┐
│  ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ │  ← Teal bar #48A1AA
│  Property Name                      │  ← Montserrat Bold, White
│  Marathon, Florida Keys             │  ← Montserrat Regular, Cream
└────────────────────────────────────┘
```

| Element | Font | Size | Color |
|---------|------|------|-------|
| Primary text | Montserrat Bold | 36px | White |
| Secondary text | Montserrat Regular | 24px | Cream `#EEE5C7` |
| Background bar | — | — | Teal `#48A1AA` (80% opacity) |

### Video Text Guidelines

| Usage | Font | Size (1080p) | Position |
|-------|------|--------------|----------|
| Hook text | Montserrat Bold | 48-64px | Center, upper third |
| Feature callout | Montserrat Semibold | 36-48px | Lower third |
| CTA | Montserrat Bold | 40px | Center bottom |
| Caption text | Montserrat Regular | 28-32px | Bottom safe zone |

### Video Overlay Colors

| Purpose | Background | Text | Opacity |
|---------|------------|------|---------|
| Property feature | Teal `#48A1AA` | White | 85% |
| CTA button | Sunset Orange `#E8945A` | White | 100% |
| Info box | Black | White | 70% |
| Subtle label | White | Black | 90% |

---

## Dark Mode (2025/26)

### Color Mapping

| Light Mode | Dark Mode |
|------------|-----------|
| White `#FFFFFF` | Dark Charcoal `#1C1C1E` |
| Off-White `#F1ECEC` | Dark Gray `#2C2C2E` |
| Black text `#000000` | White text `#FFFFFF` |
| Teal `#48A1AA` | Light Teal `#7BC4CB` |
| Cream `#EEE5C7` | Muted Cream `#A89F80` |

### Implementation

```css
/* Dark mode CSS variables */
@media (prefers-color-scheme: dark) {
  :root {
    --vpvr-bg: #1C1C1E;
    --vpvr-surface: #2C2C2E;
    --vpvr-text: #FFFFFF;
    --vpvr-text-secondary: #A1A1A6;
    --vpvr-teal: #7BC4CB;
    --vpvr-cream: #A89F80;
  }
}
```

---

## Web Assets (Hotlinks)

| Asset | URL |
|-------|-----|
| Logo SVG | `https://paraisovacationrentals.com/wp-content/uploads/2024/03/villa-paraiso-logo.svg` |
| Favicon | `https://paraisovacationrentals.com/wp-content/uploads/2024/03/favicon.png` |
| OG Image | `https://paraisovacationrentals.com/wp-content/uploads/2024/03/villa-paraiso-OG-img.jpg` |

---

## Logo Assets

### Local Files (in `assets/`)
- `VillaParaisoLogoBlueTransparent_2.png` — Teal logo on transparent (for light backgrounds)
- `VillaParaisoLogo_2.jpg` — Cream logo on teal (for headers/dark backgrounds)
- `Socials_Logo__1.png` — Square VP icon for social/small use

### CRITICAL: Logo Dimensions

**All VPVR logos are SQUARE (1:1 aspect ratio). ALWAYS use equal width and height.**

| Logo File | Native Size | Format |
|-----------|-------------|--------|
| VillaParaisoLogoBlueTransparent_2.png | 1092 × 1092 px | JPEG (despite .png extension) |
| VillaParaisoLogo_2.jpg | 1092 × 1092 px | JPEG |
| Socials_Logo__1.png | 504 × 504 px | JPEG (despite .png extension) |

### Logo Sizing by Use Case

| Use Case | Size |
|----------|------|
| Email header | 80 px square |
| Document header | 60–100 px square |
| Presentation title slide | 150 px square |
| Full page / cover | 200 px square |
| Social media profile | 504 px square |
| Video watermark | 60 px square (10% opacity) |
| Favicon | 32 px square |

### Logo Clear Space

Minimum clear space around logo = 25% of logo width on all sides.

```
     ┌─────────────────┐
     │                 │  ← Clear space (25% of logo width)
     │   ┌─────────┐   │
     │   │  LOGO   │   │
     │   └─────────┘   │
     │                 │
     └─────────────────┘
```

### WRONG vs CORRECT

```javascript
// WRONG - Different width/height distorts logo
transformation: { width: 180, height: 60 }

// CORRECT - Equal dimensions preserve square ratio
transformation: { width: 80, height: 80 }
```

---

## Property Lookup Table

When you need property data, use this mapping to find the correct URL slug:

| Property Name | URL Slug |
|---------------|----------|
| Deep Blue | `deep-blue` |
| Mermaid's Paradise | `mermaids-paradise-pool-dock-games-views` |
| Ocean Muse | `ocean-muse-lux-waterfront-escape-pool-dock` |
| Mermaid Manor | `mermaid-manor-waterfront-haven-w-hot-tub-dock` |
| Emerald Oasis | `emerald-oasis-lux-waterfront-gem-heated-pool-kayaks` |
| Isla Sol | `isla-sol` |
| Luna Light | `luna-light-waterfront-pool-dock-views` |
| Azul Paradise | `azul-paradise-waterfront-heated-pool-dock` |
| Blue Pearl | `blue-pearl-waterfront-oasis-w-pool-70-dock` |
| Sunset Harbor | `sunset-harbor` |
| Aqua Verde | `aqua-verde` |
| Seaside Escape | `luxury-seaside-escape-pool-dock-scenic-views` |
| Seabreeze Cove | `seabreeze-cove-waterfront-gem-38-foot-dock-cabana-club` |
| The Salty Coconut | `the-salty-coconut` |
| Villa Paradise | `villa-paradise-miami-lux-gem-heated-pool-game-room` |
| Isla Luna | `isla-luna-1` |
| Vista Del Mar | `luxury-waterfront-oasis-w-heated-pool-and-50-dock` |
| Saltwater Social | `aviation-1` |

**Lookup Behavior**: Try property name match first. If unclear, ask for the URL. New properties require URL until this table is updated.

---

## Fetching Live Property Data

When property content is needed, fetch current data from the website:

1. Use the property lookup table above to find the URL slug
2. Fetch from: `https://paraisovacationrentals.com/property/[slug]/`
3. Extract: images, description, amenities, pricing
4. **Note**: Content may change over time - always fetch fresh data when needed

Example:
```
Property: "Blue Pearl"
URL: https://paraisovacationrentals.com/property/blue-pearl-waterfront-oasis-w-pool-70-dock/
```

---

## Document Structure

### Header Block
```
[LOGO - centered or left-aligned, 60-100px square]
Villa Paraiso Vacation Rentals
A Partnership in Premier Hospitality.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Footer Block
```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Villa Paraiso Vacation Rentals LLC
13359 SW 59th Terr, Miami, Florida 33183
1154 Camino Del Vientos, Marathon, FL 33050
(786) 348-1396 • info@paraisovacationrentals.com
paraisovacationrentals.com
```

---

## Document Styling Rules

### Margins & Spacing
- Margins: 1 inch all sides (1.25 inch left/right for formal docs)
- Paragraph spacing: 6pt before/after
- Line spacing: 1.15

### Section Numbering (legal/formal)
- Major: 1. 2. 3. (bold, 14pt)
- Sub: (a) (b) (c)
- Sub-sub: (i) (ii) (iii)

### Tables
- Header row: `#48A1AA` background, white text
- Border: `#48A1AA`
- Alternating rows: White / `#F1ECEC`

---

## Contact Information

| Type | Value |
|------|-------|
| Phone | (786) 348-1396 |
| Email | info@paraisovacationrentals.com |
| Operations | operations@paraisovacationrentals.com |
| Accounting | accounting@paraisovacationrentals.com |
| Website | paraisovacationrentals.com |
| Miami | 13359 SW 59th Terr, Miami, FL 33183 |
| Keys | 1154 Camino Del Vientos, Marathon, FL 33050 |

---

## Implementation Examples

### HTML/CSS (Web & Email)

```html
<!-- Email-safe inline CSS -->
<body style="font-family: 'Montserrat', Arial, sans-serif; margin: 0; padding: 0; background-color: #ffffff;">
  <table style="width: 100%; max-width: 600px; margin: 0 auto;">
    <tr>
      <td style="background-color: #48A1AA; padding: 20px; text-align: center;">
        <img src="https://paraisovacationrentals.com/wp-content/uploads/2024/03/villa-paraiso-logo.svg"
             alt="Villa Paraiso" style="width: 80px; height: 80px;">
      </td>
    </tr>
    <tr>
      <td style="padding: 30px; color: #333333; font-size: 16px; line-height: 1.6;">
        <!-- Content -->
      </td>
    </tr>
    <tr>
      <td style="background-color: #F1ECEC; padding: 20px; text-align: center; font-size: 12px; color: #333333;">
        Villa Paraiso Vacation Rentals<br>
        (786) 348-1396 | info@paraisovacationrentals.com
      </td>
    </tr>
  </table>
</body>
```

### docx-js Logo (Complete)

```javascript
const logoBuffer = fs.readFileSync('./assets/VillaParaisoLogoBlueTransparent_2.png');

new ImageRun({
  type: "jpg",  // All VPVR logos are JPEG despite extension
  data: logoBuffer,
  transformation: { width: 80, height: 80 },  // MUST be equal (square)
  altText: { title: "VPVR Logo", description: "Villa Paraiso Vacation Rentals", name: "Logo" }
})
```

### docx-js Styles

```javascript
styles: {
  default: { document: { run: { font: "Montserrat", size: 22 } } },
  paragraphStyles: [
    { id: "Title", run: { size: 56, bold: true, color: "48A1AA", font: "Cormorant" },
      paragraph: { spacing: { before: 240, after: 120 }, alignment: AlignmentType.CENTER } },
    { id: "Heading1", run: { size: 32, bold: true, color: "000000", font: "Cormorant" },
      paragraph: { spacing: { before: 240, after: 120 } } },
    { id: "Heading2", run: { size: 28, bold: true, color: "000000", font: "Cormorant" },
      paragraph: { spacing: { before: 180, after: 90 } } }
  ]
}
```

### pptx (PptxGenJS)

```javascript
// Slide master colors
pptx.defineSlideMaster({
  title: 'VPVR_MASTER',
  background: { color: 'FFFFFF' },
  objects: [
    { image: { x: 0.3, y: 0.2, w: 0.8, h: 0.8, path: logoPath } },  // Square!
    { text: { text: 'Villa Paraiso Vacation Rentals', options: {
      x: 1.2, y: 0.35, fontSize: 14, bold: true, color: '48A1AA', fontFace: 'Cormorant' } } }
  ]
});

// Title slide
slide.addImage({ path: logoPath, x: 4, y: 1.5, w: 1.5, h: 1.5 });  // Centered, square
slide.addText('Presentation Title', { x: 1, y: 3.5, w: 8, fontSize: 36, bold: true, color: '48A1AA', fontFace: 'Cormorant' });
```

### Python (python-docx / python-pptx)

```python
VPVR_TEAL = RGBColor(72, 161, 170)      # #48A1AA
VPVR_CREAM = RGBColor(238, 229, 199)    # #EEE5C7
VPVR_OFF_WHITE = RGBColor(241, 236, 236) # #F1ECEC
VPVR_FONT = "Montserrat"
VPVR_HEADING_FONT = "Cormorant"
VPVR_LOGO_PATH = "./assets/VillaParaisoLogoBlueTransparent_2.png"

# Logo - always use equal width/height (square)
from docx.shared import Inches
doc.add_picture(VPVR_LOGO_PATH, width=Inches(1), height=Inches(1))
```

### xlsx (ExcelJS)

```javascript
const ExcelJS = require('exceljs');
const workbook = new ExcelJS.Workbook();
const sheet = workbook.addWorksheet('Sheet1');

// VPVR brand colors (ARGB format)
const VPVR_TEAL = 'FF48A1AA';
const VPVR_OFF_WHITE = 'FFF1ECEC';

// Header row styling
const headerRow = sheet.getRow(1);
headerRow.font = { name: 'Montserrat', bold: true, color: { argb: 'FFFFFFFF' } };
headerRow.fill = { type: 'pattern', pattern: 'solid', fgColor: { argb: VPVR_TEAL } };
headerRow.alignment = { vertical: 'middle', horizontal: 'center' };

// Alternating row colors (zebra striping)
sheet.eachRow((row, rowNum) => {
  if (rowNum > 1 && rowNum % 2 === 0) {
    row.fill = { type: 'pattern', pattern: 'solid', fgColor: { argb: VPVR_OFF_WHITE } };
  }
});

// Default font for all cells
workbook.eachSheet(ws => {
  ws.eachRow(row => {
    row.eachCell(cell => {
      cell.font = { name: 'Montserrat', size: 11 };
    });
  });
});

// Add logo (top-left, square)
const logoPath = './assets/VillaParaisoLogoBlueTransparent_2.png';
const logoId = workbook.addImage({ filename: logoPath, extension: 'jpeg' });
sheet.addImage(logoId, {
  tl: { col: 0, row: 0 },
  ext: { width: 80, height: 80 }  // MUST be equal (square)
});

// Teal borders for data range
sheet.eachRow((row, rowNum) => {
  row.eachCell(cell => {
    cell.border = {
      top: { style: 'thin', color: { argb: VPVR_TEAL } },
      left: { style: 'thin', color: { argb: VPVR_TEAL } },
      bottom: { style: 'thin', color: { argb: VPVR_TEAL } },
      right: { style: 'thin', color: { argb: VPVR_TEAL } }
    };
  });
});
```

### xlsx (Python openpyxl)

```python
from openpyxl import Workbook
from openpyxl.styles import Font, PatternFill, Alignment, Border, Side
from openpyxl.drawing.image import Image

# VPVR brand colors
VPVR_TEAL_FILL = PatternFill(start_color='48A1AA', end_color='48A1AA', fill_type='solid')
VPVR_OFF_WHITE_FILL = PatternFill(start_color='F1ECEC', end_color='F1ECEC', fill_type='solid')
VPVR_TEAL_BORDER = Side(style='thin', color='48A1AA')
VPVR_FONT = Font(name='Montserrat', size=11)
VPVR_HEADER_FONT = Font(name='Montserrat', size=11, bold=True, color='FFFFFF')

wb = Workbook()
ws = wb.active

# Header row styling
for cell in ws[1]:
    cell.font = VPVR_HEADER_FONT
    cell.fill = VPVR_TEAL_FILL
    cell.alignment = Alignment(horizontal='center', vertical='center')

# Add logo (square dimensions)
logo = Image('./assets/VillaParaisoLogoBlueTransparent_2.png')
logo.width = 80
logo.height = 80  # MUST equal width (square)
ws.add_image(logo, 'A1')
```

---

## AI Image Brand Integration

When using AI image generation (Gemini, DALL-E, Midjourney), incorporate VPVR brand:

### Color Prompts
```
Include turquoise/teal water tones (#48A1AA),
warm cream sandy areas (#EEE5C7),
tropical Keys aesthetic
```

### Style Keywords
```
Luxury resort marketing style,
magazine-quality real estate photography,
aspirational vacation lifestyle,
warm golden hour lighting
```

### Brand Consistency Elements
- Always include: Palm trees, turquoise water, private dock
- Preferred lighting: Golden hour (80% of images)
- Mood: Aspirational, warm, inviting
- Avoid: Oversaturated, HDR look, stock photo feel

---

## Canva Brand Kit

When using Canva, apply these settings:

| Element | Value |
|---------|-------|
| Primary Color | #48A1AA |
| Secondary Color | #EEE5C7 |
| Accent Color | #F1ECEC |
| Body Font | Montserrat |
| Heading Font | Cormorant |
| Logo | Upload square versions only |

---

## Brand Don'ts

| Don't | Why |
|-------|-----|
| ❌ Stretch or distort logo | Always maintain 1:1 square ratio |
| ❌ Use low-contrast text | Fails accessibility standards |
| ❌ Mix font styles randomly | Undermines brand consistency |
| ❌ Use non-brand colors | Creates confusion with brand identity |
| ❌ Place logo on busy backgrounds | Reduces visibility and recognition |
| ❌ Add effects to logo | Shadows, glows, etc. degrade quality |

---

## Related VPVR Skills

This brand guide is used by:
- **stayfi-emails**: Email template styling
- **social-content**: Social media visual guidelines
- **property-descriptions**: Listing formatting
- **vpvr-blog-posts**: Blog styling and schema
- **gemini-images**: AI image generation with brand colors
- **owner-comms**: Homeowner communication styling
- **linkedin-ceo**: Thought leadership content
- **vpvr-seo-aeo**: SEO optimization with brand consistency
