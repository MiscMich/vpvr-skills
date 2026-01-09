---
name: vpvr-brand
description: Villa Paraiso Vacation Rentals brand styling for documents. Apply VPVR brand colors, typography (Helvetica Neue), and logo to any document (docx, pptx, xlsx, pdf). Use when creating documents for Villa Paraiso, VPVR, vacation rental agreements, owner communications, SOPs, onboarding materials, spreadsheets, reports, or any branded company document.
---

# Villa Paraiso Vacation Rentals Brand Styling

## Quick Reference

| Element | Value |
|---------|-------|
| Primary Color (Teal) | `#48a1aa` / RGB(72, 161, 170) |
| Secondary (Cream) | `#eee5c7` / RGB(238, 229, 199) |
| Font | Helvetica Neue (fallback: Arial) |
| Logo Size | **Always square** (e.g., 80×80px) |
| Logo Path | `./assets/VillaParaisoLogoBlueTransparent_2.png` |

## Brand Identity

**Company:** Villa Paraiso Vacation Rentals LLC  
**Tagline:** *A Partnership in Premier Hospitality*

## Brand Colors

| Color | Hex | RGB | Usage |
|-------|-----|-----|-------|
| Teal | `#48a1aa` | (72, 161, 170) | Primary accent, headers, logo, links |
| Cream | `#eee5c7` | (238, 229, 199) | Secondary accent, backgrounds, logo on dark |
| Off-White | `#f1ecec` | (241, 236, 236) | Light backgrounds, subtle accents |
| Black | `#000000` | (0, 0, 0) | Body text |
| Dark Gray | `#333333` | (51, 51, 51) | Secondary text |

## Typography

**Primary Font:** Helvetica Neue (fallback: Arial, Helvetica, sans-serif)

| Element | Size | Weight | Color |
|---------|------|--------|-------|
| Document Title | 28pt | Bold | `#48a1aa` (Teal) |
| Company Name | 24pt | Bold | `#000000` or `#48a1aa` |
| Tagline | 14pt | Italic | `#333333` |
| Heading 1 | 16pt | Bold | `#000000` |
| Heading 2 | 14pt | Bold | `#000000` |
| Heading 3 | 12pt | Bold | `#000000` |
| Body Text | 11pt | Regular | `#000000` |
| Footer | 10pt | Regular | `#333333` |

## Logo Assets

Located in `assets/`:
- `VillaParaisoLogoBlueTransparent_2.png` — Teal logo on transparent (for light backgrounds)
- `VillaParaisoLogo_2.jpg` — Cream logo on teal (for headers/dark backgrounds)
- `Socials_Logo__1.png` — Square VP icon for social/small use

### ⚠️ CRITICAL: Logo Dimensions

**All VPVR logos are SQUARE (1:1 aspect ratio). ALWAYS use equal width and height.**

| Logo File | Native Size | Format |
|-----------|-------------|--------|
| VillaParaisoLogoBlueTransparent_2.png | 1092 × 1092 px | JPEG (despite .png extension) |
| VillaParaisoLogo_2.jpg | 1092 × 1092 px | JPEG |
| Socials_Logo__1.png | 504 × 504 px | JPEG (despite .png extension) |

### Logo Sizing by Use Case

| Use Case | Size |
|----------|------|
| Document header | 60–100 px square |
| Presentation title slide | 150 px square |
| Full page / cover | 200 px square |

### ❌ WRONG vs ✅ CORRECT

```javascript
// ❌ WRONG - Different width/height distorts logo
transformation: { width: 180, height: 60 }

// ✅ CORRECT - Equal dimensions preserve square ratio
transformation: { width: 80, height: 80 }
```

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
- Header row: `#48a1aa` background, white text
- Border: `#48a1aa`
- Alternating rows: White / `#f1ecec`

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

## Implementation Examples

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
  default: { document: { run: { font: "Helvetica Neue", size: 22 } } },
  paragraphStyles: [
    { id: "Title", run: { size: 56, bold: true, color: "48a1aa", font: "Helvetica Neue" },
      paragraph: { spacing: { before: 240, after: 120 }, alignment: AlignmentType.CENTER } },
    { id: "Heading1", run: { size: 32, bold: true, color: "000000", font: "Helvetica Neue" },
      paragraph: { spacing: { before: 240, after: 120 } } },
    { id: "Heading2", run: { size: 28, bold: true, color: "000000", font: "Helvetica Neue" },
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
      x: 1.2, y: 0.35, fontSize: 14, bold: true, color: '48a1aa' } } }
  ]
});

// Title slide
slide.addImage({ path: logoPath, x: 4, y: 1.5, w: 1.5, h: 1.5 });  // Centered, square
slide.addText('Presentation Title', { x: 1, y: 3.5, w: 8, fontSize: 36, bold: true, color: '48a1aa' });
```

### Python (python-docx / python-pptx)

```python
VPVR_TEAL = RGBColor(72, 161, 170)      # #48a1aa
VPVR_CREAM = RGBColor(238, 229, 199)    # #eee5c7
VPVR_OFF_WHITE = RGBColor(241, 236, 236) # #f1ecec
VPVR_FONT = "Helvetica Neue"
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
headerRow.font = { name: 'Helvetica Neue', bold: true, color: { argb: 'FFFFFFFF' } };
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
      cell.font = { name: 'Helvetica Neue', size: 11 };
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
VPVR_FONT = Font(name='Helvetica Neue', size=11)
VPVR_HEADER_FONT = Font(name='Helvetica Neue', size=11, bold=True, color='FFFFFF')

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
