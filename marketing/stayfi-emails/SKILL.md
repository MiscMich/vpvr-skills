---
name: stayfi-emails
description: Create extremely high-converting, beautiful HTML email templates for StayFi guest communication using expert methodologies (Joanna Wiebe, Chase Dimond, Val Geisler, Litmus, Email on Acid). Includes complete guest journey sequences from pre-arrival through win-back. Features luxury editorial design with distinctive typography, and professional inline CSS templates ready for StayFi upload. All property data, images, and links are dynamically sourced and validated before delivery.
---

# VPVR StayFi Email Templates

Create extremely high-converting, beautiful emails using proven email marketing expert methodologies combined with luxury editorial design principles. **All content is dynamically sourced from the live VPVR website.**

---

## CRITICAL: Read These Skills First

Before creating any email, Claude MUST read:

1. **Frontend Design Skill** (`/mnt/skills/public/frontend-design/SKILL.md`)
   - Provides bold aesthetic direction and design thinking
   - Typography, color, motion, and spatial composition principles
   - Ensures emails avoid generic "AI slop" aesthetics

2. **VPVR Brand Skill** (`/mnt/skills/user/vpvr-brand/SKILL.md`)
   - Brand colors, typography, logo specifications
   - Voice: "Four Seasons of vacation rentals" — luxury without pretension

**Design Philosophy**: Every VPVR email should feel like a luxury editorial piece — magazine-quality design with intentional typography, generous whitespace, and memorable visual moments.

---

## Quick Reference

| Specification | Value |
|---------------|-------|
| **Max width** | 600px |
| **Body font** | Montserrat, 16px minimum |
| **Heading font** | Cormorant (Georgia fallback) |
| **CTA button** | 44px minimum height |
| **Logo folder** | `/wp-content/uploads/2026/01/` |
| **Dark bg → Cream logos** | `vpvr-logo-cream@2x.png` (header 280×47), `vpvr-icon-cream@2x.png` (footer 70×70) |
| **Light bg → Teal logos** | `vpvr-logo-teal@2x.png` (header 280×47), `vpvr-icon-teal@2x.png` (footer 70×70) |
| **Primary color** | `#48A1AA` (Teal) |
| **Accent** | `#EEE5C7` (Cream) |
| **Ocean Blue** | `#2E6E7A` (headers, footers) |
| **Header/Footer bg** | `#2E6E7A` solid (never black, no gradients) |

---

## MANDATORY: Dynamic Content Sourcing

### Step 1: Fetch Property Data

**Claude MUST fetch current property information before creating any email.** Never use assumed data.

```
WORKFLOW:
1. web_fetch https://paraisovacationrentals.com/properties/ to get current property list
2. Identify the target property from the listing
3. web_fetch the individual property page: https://paraisovacationrentals.com/property/[slug]/
4. Extract hero image URLs and property details from the page
5. Use this live data in the email
```

### Step 2: Extract Images

From each property page, extract:
- **Hero image**: The main large photo (usually first in gallery)
- **Gallery images**: Additional photos for multi-image layouts
- **Property details**: Bedrooms, bathrooms, amenities, location

**Image URLs will be in format**: `https://paraisovacationrentals.com/wp-content/uploads/...`

These WordPress-hosted images are reliable for email hotlinking.

### Step 3: Validate Before Delivery

Use `web_fetch` to confirm:
- [ ] All image URLs load correctly
- [ ] Property page is live
- [ ] CTA destination links work

### If Property Data Cannot Be Found

If a property page fails to load:
1. **Flag to user**: "I couldn't load [property name]. Please verify the property URL or upload photos directly."
2. Provide partial email with `[UPLOAD PROPERTY IMAGE]` placeholders
3. **Never invent or assume property details**

---

## Current VPVR Properties

Fetch fresh data, but here are the known property slugs for reference:

| Property Name | URL Slug | Location |
|---------------|----------|----------|
| Blue Pearl | `blue-pearl` | Key Colony Beach |
| Ocean Muse | `ocean-muse` | Marathon |
| Isla Sol | `isla-sol` | Marathon |
| Isla Luna | `isla-luna` | Marathon |
| Aqua Verde | `aqua-verde` | Key Colony Beach |
| Casa Coral | `casa-coral` | Key Colony Beach |

**Always fetch the properties page to get the current list** — properties are added and removed.

---

## Expert Methodologies

| Expert | Framework | Application |
|--------|-----------|-------------|
| **Joanna Wiebe** (Copyhackers) | Voice of Customer | Use guest language in subject lines |
| **Chase Dimond** | Retention Flow Optimization | Behavior-triggered sequences |
| **Val Geisler** | Fix My Churn | Onboarding that builds anticipation |
| **Litmus** | 2025 Email Design Standards | Technical compliance, dark mode |
| **Email on Acid** | Deliverability Best Practices | Image ratios, spam avoidance |

---

## Design System

### Typography Hierarchy

| Element | Font | Size | Weight | Color |
|---------|------|------|--------|-------|
| Newsletter Title | Cormorant | 42px | 500 | White |
| Section Label | Cormorant | 14px | 600 | `#48A1AA` |
| Section Heading | Cormorant | 28-32px | 500 | Black |
| Body Copy | Montserrat | 15-16px | 400 | `#333333` |
| CTA Button | Montserrat | 12px | 600 | White |
| Footer | Montserrat | 11-12px | 400 | Various |

**Typography Pattern**: Section label (small caps, teal) → Large heading (Cormorant) → Body (Montserrat)

### Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| **Teal** | `#48A1AA` | Headers, buttons, links, labels |
| **Deep Teal** | `#3A858C` | Gradients, hover states |
| **Ocean Blue** | `#2E6E7A` | Footer backgrounds, depth |
| **Cream** | `#EEE5C7` | Outer wrapper, decorative |
| **Off-White** | `#F1ECEC` | Section backgrounds |
| **Warm Sand** | `#F9F7F3` | Info boxes |
| **Black** | `#000000` | Headlines |
| **Dark Gray** | `#333333` | Body text |

### ⚠️ Email Client Compatibility (CRITICAL)

**These rules prevent rendering failures in Gmail, Outlook, Apple Mail, and Yahoo.**

#### NEVER USE (Will Break)

| ❌ Don't Use | ✅ Use Instead | Why |
|-------------|----------------|-----|
| SVG images/icons | PNG images | SVG stripped by Gmail/Outlook |
| `linear-gradient()` | Solid `background-color` | Fails in Outlook |
| `rgba()` colors | Solid hex colors | Not supported |
| `filter: invert()` | Pre-made white logo PNG | CSS filters stripped |
| `box-shadow` | `border: 1px solid #e0e0e0` | Inconsistent support |
| `border-radius` on images | Rectangular images | Stripped by Outlook |
| Inline `<svg>` elements | Hosted image or accent bar | Completely stripped |
| Unicode symbols (✦ · —) | HTML entities | May not render |
| Black footer (`#1a1a1a`) | Ocean Blue `#2E6E7A` | Off-brand |

#### HTML Entity Reference

| Character | HTML Entity | Usage |
|-----------|-------------|-------|
| Bullet (·) | `&bull;` | Lists, separators |
| Star (✦) | `&#10022;` | Decorative dividers |
| Em dash (—) | `&mdash;` | Attribution |
| Right arrow (→) | `&rarr;` | CTAs |
| Left quote (") | `&ldquo;` | Testimonials |
| Right quote (") | `&rdquo;` | Testimonials |
| Copyright (©) | `&copy;` | Footer |
| Ampersand (&) | `&amp;` | Always escape |

#### Logo Requirements

**Logo Library (Jan 2026) — All in `/wp-content/uploads/2026/01/`**

**Base URL:** `https://paraisovacationrentals.com/wp-content/uploads/2026/01/`

**HORIZONTAL WORDMARK — Wide format (6:1 ratio):**
| File | Dimensions | Logo Color | Use On |
|------|------------|------------|--------|
| `vpvr-logo-cream@2x.png` | 3384×570 | Cream | Dark backgrounds (Ocean Blue, Teal) ✅ |
| `vpvr-logo-cream.png` | 1692×285 | Cream | Dark backgrounds (standard res) |
| `vpvr-logo-teal@2x.png` | 3384×570 | Teal | Light backgrounds (White, Cream) ✅ |
| `vpvr-logo-teal.png` | 1692×285 | Teal | Light backgrounds (standard res) |

**ICONS (Palm tree only) — Square format:**
| File | Dimensions | Logo Color | Use On |
|------|------------|------------|--------|
| `vpvr-icon-cream@2x.png` | 570×570 | Cream | Dark backgrounds ✅ |
| `vpvr-icon-cream.png` | 285×285 | Cream | Dark backgrounds (standard res) |
| `vpvr-icon-teal@2x.png` | 570×570 | Teal | Light backgrounds ✅ |
| `vpvr-icon-teal.png` | 285×285 | Teal | Light backgrounds (standard res) |

---

**Email Logo Selection Guide:**

| Email Section | Background Color | Logo File | Size |
|---------------|------------------|-----------|------|
| **Header (standard)** | Ocean Blue `#2E6E7A` | `vpvr-logo-cream@2x.png` | 280×47px |
| **Header (light variant)** | White/Cream | `vpvr-logo-teal@2x.png` | 280×47px |
| **Footer (standard)** | Ocean Blue `#2E6E7A` | `vpvr-icon-cream@2x.png` | 70×70px |
| **Footer (light variant)** | White/Cream | `vpvr-icon-teal@2x.png` | 70×70px |
| **CTA section** | Teal `#48A1AA` | `vpvr-icon-cream@2x.png` | 60×60px |
| **Testimonial block** | Teal `#48A1AA` | (no logo, use quote mark) | — |
| **Content section** | White `#FFFFFF` | `vpvr-icon-teal@2x.png` | 50×50px (if needed) |

---

**Code Examples:**

```html
<!-- DARK BACKGROUND (Ocean Blue #2E6E7A or Teal #48A1AA) -->

<!-- Header: Horizontal wordmark - CREAM logo on dark -->
<td style="background-color: #2E6E7A; padding: 45px 40px; text-align: center;">
  <img src="https://paraisovacationrentals.com/wp-content/uploads/2026/01/vpvr-logo-cream@2x.png" 
       alt="Villa Paraiso Vacation Rentals" 
       width="280" height="47" 
       style="display: block; margin: 0 auto 30px auto; width: 280px; height: 47px;">
</td>

<!-- Footer: Icon only - CREAM logo on dark -->
<td style="background-color: #2E6E7A; padding: 40px; text-align: center;">
  <img src="https://paraisovacationrentals.com/wp-content/uploads/2026/01/vpvr-icon-cream@2x.png" 
       alt="Villa Paraiso" 
       width="70" height="70" 
       style="display: block; margin: 0 auto 20px auto; width: 70px; height: 70px;">
</td>


<!-- LIGHT BACKGROUND (White #FFFFFF or Cream #EEE5C7) -->

<!-- Header: Horizontal wordmark - TEAL logo on light -->
<td style="background-color: #FFFFFF; padding: 45px 40px; text-align: center;">
  <img src="https://paraisovacationrentals.com/wp-content/uploads/2026/01/vpvr-logo-teal@2x.png" 
       alt="Villa Paraiso Vacation Rentals" 
       width="280" height="47" 
       style="display: block; margin: 0 auto 30px auto; width: 280px; height: 47px;">
</td>

<!-- Footer: Icon only - TEAL logo on light -->
<td style="background-color: #F8F6F3; padding: 40px; text-align: center;">
  <img src="https://paraisovacationrentals.com/wp-content/uploads/2026/01/vpvr-icon-teal@2x.png" 
       alt="Villa Paraiso" 
       width="70" height="70" 
       style="display: block; margin: 0 auto 20px auto; width: 70px; height: 70px;">
</td>
```

**Quick Decision:**
- Dark background? → Use **cream** logos
- Light background? → Use **teal** logos
- Need full brand name? → Use **wordmark** (horizontal)
- Space limited or secondary? → Use **icon** (palm tree)

**Legacy logos** (stacked format in `/2024/03/` and `/2026/01/VillaParaisoLogo-*.png`) should NOT be used — they display too small at email-appropriate sizes.

---

### Signature Design Elements

1. **Accent Bar** (header to content transition — replaces SVG wave):
```html
<!-- Simple colored bar - works everywhere -->
<tr>
  <td style="background-color: #48A1AA; height: 6px; font-size: 1px; line-height: 1px;">&nbsp;</td>
</tr>
```

2. **Decorative Divider** (between sections):
```html
<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
  <tr>
    <td style="width: 60px; height: 1px; background-color: #EEE5C7;"></td>
    <td style="width: 60px; text-align: center; padding: 0 15px;">
      <span style="font-family: 'Cormorant', Georgia, serif; font-size: 24px; color: #48A1AA;">&#10022;</span>
    </td>
    <td style="width: 60px; height: 1px; background-color: #EEE5C7;"></td>
  </tr>
</table>
```

3. **Section Label Pattern**:
```html
<p style="margin: 0 0 5px 0; font-family: 'Cormorant', Georgia, serif; font-size: 14px; font-weight: 600; color: #48A1AA; letter-spacing: 3px; text-transform: uppercase;">
  Section Label
</p>
<h2 style="margin: 0 0 20px 0; font-family: 'Cormorant', Georgia, serif; font-size: 28px; font-weight: 500; color: #000000; line-height: 1.2;">
  Main Heading Goes Here
</h2>
```

4. **Header Background** (solid color for Outlook compatibility):
```html
<!-- Use Ocean Blue solid - gradients fail in Outlook -->
background-color: #2E6E7A;
```

5. **Testimonial Block** (full-width teal):
```html
<tr>
  <td style="background-color: #48A1AA; padding: 50px;">
    <!-- Use HTML entity for quote mark, solid color instead of rgba -->
    <span style="font-family: 'Cormorant', Georgia, serif; font-size: 72px; color: #7BC4CB; line-height: 0;">&ldquo;</span>
    <p style="font-family: 'Cormorant', Georgia, serif; font-size: 22px; color: #ffffff; line-height: 1.6; font-style: italic;">
      [Quote text]
    </p>
    <p style="font-family: 'Montserrat', Arial, sans-serif; font-size: 12px; font-weight: 600; color: #EEE5C7; letter-spacing: 2px; text-transform: uppercase;">
      &mdash; Guest Name, City
    </p>
  </td>
</tr>
```

6. **Footer** (MUST use Ocean Blue, not black):
```html
<tr>
  <td style="background-color: #2E6E7A; padding: 40px;">
    <!-- Use cream icon on dark backgrounds -->
    <img src="https://paraisovacationrentals.com/wp-content/uploads/2026/01/vpvr-icon-cream@2x.png"
         alt="Villa Paraiso" width="70" height="70" style="display: block; margin: 0 auto;">
    <!-- Footer text in white/cream on Ocean Blue -->
  </td>
</tr>
```

---

## StayFi/Campaign Monitor Technical Requirements

### Merge Tags

```
%%FIRSTNAME%%     - Guest first name
%%LASTNAME%%      - Guest last name
%%PROPERTYNAME%%  - Property name
%%EMAIL%%         - Guest email
%%CHECKIN%%       - Check-in date
%%CHECKOUT%%      - Check-out date
%%RESERVATIONID%% - Booking reference
```

### Important Links

| Purpose | URL |
|---------|-----|
| Homepage | `https://paraisovacationrentals.com/` |
| All Properties | `https://paraisovacationrentals.com/properties/` |
| Google Reviews | `https://maps.app.goo.gl/aYcTTj4BC4cJhEnt5` |
| Instagram | `https://www.instagram.com/villaparaisorentals/` |
| Facebook | `https://www.facebook.com/people/Villa-Paraiso-Vacation-Rentals/100090096057720/` |

---

## Master Email Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="color-scheme" content="light dark">
  <meta name="supported-color-schemes" content="light dark">
  <title>%%PROPERTYNAME%% - Villa Paraiso</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant:wght@400;500;600;700&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">
  <!--[if mso]>
  <style type="text/css">
    body, table, td {font-family: Arial, Helvetica, sans-serif !important;}
  </style>
  <![endif]-->
</head>
<body style="margin: 0; padding: 0; background-color: #EEE5C7; font-family: 'Montserrat', Arial, sans-serif;">
  
  <!-- Preheader Text -->
  <div style="display: none; max-height: 0; overflow: hidden; mso-hide: all;">
    [PREHEADER_TEXT - 85-100 characters] ✦
  </div>
  
  <!-- Email Container -->
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="background-color: #EEE5C7;">
    <tr>
      <td align="center" style="padding: 30px 15px;">
        
        <!-- Main Content Table -->
        <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="600" style="max-width: 600px; background-color: #ffffff;">
          
          <!-- Gradient Header -->
          <tr>
            <td style="background: linear-gradient(135deg, #48A1AA 0%, #3A858C 50%, #2E6E7A 100%); padding: 0;">
              <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
                <tr>
                  <td style="padding: 40px 40px 30px 40px; text-align: center;">
                    <!-- Logo (cream icon on teal gradient) -->
                    <img src="https://paraisovacationrentals.com/wp-content/uploads/2026/01/vpvr-icon-cream@2x.png"
                         alt="Villa Paraiso"
                         width="90" height="90"
                         style="display: block; margin: 0 auto 20px auto; border: 3px solid rgba(238, 229, 199, 0.3); border-radius: 50%; padding: 10px; background: rgba(255,255,255,0.1);">
                    
                    <!-- Decorative Line -->
                    <div style="width: 60px; height: 1px; background-color: #EEE5C7; margin: 0 auto 25px auto; opacity: 0.6;"></div>
                    
                    <!-- Email Title -->
                    <h1 style="margin: 0; font-family: 'Cormorant', Georgia, serif; font-size: 36px; font-weight: 500; color: #ffffff; letter-spacing: 2px;">
                      [EMAIL_TITLE]
                    </h1>
                    <p style="margin: 8px 0 0 0; font-family: 'Montserrat', Arial, sans-serif; font-size: 13px; font-weight: 300; color: #EEE5C7; letter-spacing: 3px; text-transform: uppercase;">
                      [SUBTITLE_OR_DATE]
                    </p>
                  </td>
                </tr>
                
                <!-- Wave Divider -->
                <tr>
                  <td style="font-size: 0; line-height: 0;">
                    <svg viewBox="0 0 600 40" style="display: block; width: 100%;" preserveAspectRatio="none">
                      <path d="M0,40 L0,20 Q150,0 300,20 Q450,40 600,20 L600,40 Z" fill="#ffffff"/>
                    </svg>
                  </td>
                </tr>
              </table>
            </td>
          </tr>
          
          <!-- Body Content -->
          <tr>
            <td style="padding: 35px 50px 40px 50px;">
              <p style="margin: 0 0 5px 0; font-family: 'Cormorant', Georgia, serif; font-size: 14px; font-weight: 600; color: #48A1AA; letter-spacing: 3px; text-transform: uppercase;">
                [SECTION_LABEL]
              </p>
              <h2 style="margin: 0 0 20px 0; font-family: 'Cormorant', Georgia, serif; font-size: 28px; font-weight: 500; color: #000000; line-height: 1.2;">
                [MAIN_HEADLINE]
              </h2>
              <p style="margin: 0 0 20px 0; font-family: 'Montserrat', Arial, sans-serif; font-size: 15px; font-weight: 400; color: #333333; line-height: 1.8;">
                Hi %%FIRSTNAME%%,
              </p>
              <p style="margin: 0; font-family: 'Montserrat', Arial, sans-serif; font-size: 15px; font-weight: 400; color: #333333; line-height: 1.8;">
                [BODY_CONTENT]
              </p>
            </td>
          </tr>
          
          <!-- Hero Image (if applicable) -->
          <tr>
            <td style="padding: 0;">
              <img src="[PROPERTY_HERO_IMAGE_URL]" 
                   alt="[PROPERTY_NAME]" 
                   width="600" 
                   style="display: block; width: 100%; height: auto;">
            </td>
          </tr>
          
          <!-- CTA Section -->
          <tr>
            <td style="padding: 40px 50px; text-align: center;">
              <table role="presentation" cellspacing="0" cellpadding="0" border="0" align="center">
                <tr>
                  <td style="background-color: #48A1AA;">
                    <a href="[CTA_LINK]" 
                       target="_blank" 
                       style="display: inline-block; padding: 16px 40px; font-family: 'Montserrat', Arial, sans-serif; font-size: 12px; font-weight: 600; color: #ffffff; text-decoration: none; letter-spacing: 2px; text-transform: uppercase;">
                      [CTA_TEXT] →
                    </a>
                  </td>
                </tr>
              </table>
            </td>
          </tr>
          
          <!-- Footer -->
          <tr>
            <td style="background-color: #2E6E7A; padding: 40px 50px;">
              <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
                <tr>
                  <td style="text-align: center;">
                    <img src="https://paraisovacationrentals.com/wp-content/uploads/2026/01/vpvr-icon-cream@2x.png"
                         alt="Villa Paraiso"
                         width="60" height="60"
                         style="display: inline-block; margin-bottom: 15px; opacity: 0.9;">
                    
                    <p style="margin: 0 0 5px 0; font-family: 'Cormorant', Georgia, serif; font-size: 18px; font-weight: 500; color: #ffffff; letter-spacing: 1px;">
                      Villa Paraiso Vacation Rentals
                    </p>
                    <p style="margin: 0 0 20px 0; font-family: 'Montserrat', Arial, sans-serif; font-size: 11px; font-weight: 400; color: #EEE5C7; font-style: italic;">
                      A Partnership in Premier Hospitality
                    </p>
                    
                    <!-- Social Links -->
                    <table role="presentation" cellspacing="0" cellpadding="0" border="0" align="center" style="margin-bottom: 20px;">
                      <tr>
                        <td style="padding: 0 10px;">
                          <a href="https://www.instagram.com/villaparaisorentals/" style="font-family: 'Montserrat', Arial, sans-serif; font-size: 11px; color: #EEE5C7; text-decoration: none; letter-spacing: 1px;">
                            INSTAGRAM
                          </a>
                        </td>
                        <td style="padding: 0 10px;">
                          <a href="https://www.facebook.com/people/Villa-Paraiso-Vacation-Rentals/100090096057720/" style="font-family: 'Montserrat', Arial, sans-serif; font-size: 11px; color: #EEE5C7; text-decoration: none; letter-spacing: 1px;">
                            FACEBOOK
                          </a>
                        </td>
                        <td style="padding: 0 10px;">
                          <a href="https://paraisovacationrentals.com/" style="font-family: 'Montserrat', Arial, sans-serif; font-size: 11px; color: #EEE5C7; text-decoration: none; letter-spacing: 1px;">
                            WEBSITE
                          </a>
                        </td>
                      </tr>
                    </table>
                    
                    <!-- Contact -->
                    <p style="margin: 0 0 15px 0; font-family: 'Montserrat', Arial, sans-serif; font-size: 11px; font-weight: 400; color: rgba(238, 229, 199, 0.7); line-height: 1.6;">
                      Marathon & Key Colony Beach, Florida Keys<br>
                      <a href="tel:7863481396" style="color: rgba(238, 229, 199, 0.9); text-decoration: none;">(786) 348-1396</a> · 
                      <a href="mailto:info@paraisovacationrentals.com" style="color: rgba(238, 229, 199, 0.9); text-decoration: none;">info@paraisovacationrentals.com</a>
                    </p>
                    
                    <!-- Unsubscribe -->
                    <p style="margin: 0; font-family: 'Montserrat', Arial, sans-serif; font-size: 10px; font-weight: 400; color: rgba(238, 229, 199, 0.5);">
                      <a href="[Unsubscribe]" style="color: rgba(238, 229, 199, 0.7); text-decoration: underline;">Unsubscribe</a> · 
                      <a href="#" style="color: rgba(238, 229, 199, 0.7); text-decoration: underline;">View in Browser</a>
                    </p>
                  </td>
                </tr>
              </table>
            </td>
          </tr>
          
        </table>
      </td>
    </tr>
  </table>
</body>
</html>
```

---

## Module Library

### Three-Column Property Grid

```html
<tr>
  <td style="background-color: #F1ECEC; padding: 45px 30px;">
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
      <tr>
        <td style="text-align: center; padding-bottom: 30px;">
          <p style="margin: 0 0 5px 0; font-family: 'Cormorant', Georgia, serif; font-size: 14px; font-weight: 600; color: #48A1AA; letter-spacing: 3px; text-transform: uppercase;">
            [LABEL]
          </p>
          <h2 style="margin: 0; font-family: 'Cormorant', Georgia, serif; font-size: 28px; font-weight: 500; color: #000000;">
            [HEADING]
          </h2>
        </td>
      </tr>
      <tr>
        <td>
          <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
            <tr>
              <!-- Property 1 -->
              <td width="33%" valign="top" style="padding: 0 8px;">
                <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="background-color: #ffffff;">
                  <tr>
                    <td>
                      <img src="[PROPERTY_1_IMAGE]" alt="[PROPERTY_1_NAME]" width="100%" style="display: block;">
                    </td>
                  </tr>
                  <tr>
                    <td style="padding: 15px 12px;">
                      <h3 style="margin: 0 0 5px 0; font-family: 'Cormorant', Georgia, serif; font-size: 18px; font-weight: 600; color: #000000;">
                        [PROPERTY_1_NAME]
                      </h3>
                      <p style="margin: 0 0 8px 0; font-family: 'Montserrat', Arial, sans-serif; font-size: 11px; color: #48A1AA; font-weight: 500;">
                        [PROPERTY_1_LOCATION]
                      </p>
                      <p style="margin: 0; font-family: 'Montserrat', Arial, sans-serif; font-size: 12px; color: #333333;">
                        [PROPERTY_1_DETAILS]
                      </p>
                    </td>
                  </tr>
                </table>
              </td>
              <!-- Property 2 -->
              <td width="33%" valign="top" style="padding: 0 8px;">
                <!-- Same structure as Property 1 -->
              </td>
              <!-- Property 3 -->
              <td width="33%" valign="top" style="padding: 0 8px;">
                <!-- Same structure as Property 1 -->
              </td>
            </tr>
          </table>
        </td>
      </tr>
    </table>
  </td>
</tr>
```

### Local Insider Block

```html
<tr>
  <td style="padding: 50px;">
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
      <tr>
        <td width="60" valign="top">
          <div style="width: 50px; height: 50px; background-color: #48A1AA; border-radius: 50%; text-align: center; line-height: 50px;">
            <span style="font-family: 'Cormorant', Georgia, serif; font-size: 24px; color: #ffffff;">✦</span>
          </div>
        </td>
        <td valign="top" style="padding-left: 20px;">
          <p style="margin: 0 0 5px 0; font-family: 'Cormorant', Georgia, serif; font-size: 14px; font-weight: 600; color: #48A1AA; letter-spacing: 3px; text-transform: uppercase;">
            Local Insider
          </p>
          <h2 style="margin: 0 0 15px 0; font-family: 'Cormorant', Georgia, serif; font-size: 24px; font-weight: 500; color: #000000; line-height: 1.3;">
            [INSIDER_HEADING]
          </h2>
          <p style="margin: 0; font-family: 'Montserrat', Arial, sans-serif; font-size: 14px; font-weight: 400; color: #333333; line-height: 1.7;">
            [INSIDER_CONTENT]
          </p>
        </td>
      </tr>
    </table>
  </td>
</tr>
```

### Info Box

```html
<table role="presentation" width="100%" cellpadding="0" cellspacing="0" style="background-color: #F9F7F3; margin: 25px 0;">
  <tr>
    <td style="padding: 25px; border-left: 4px solid #48A1AA;">
      <p style="margin: 0 0 10px 0; font-family: 'Cormorant', Georgia, serif; font-size: 14px; font-weight: 600; color: #48A1AA; letter-spacing: 2px; text-transform: uppercase;">
        [INFO_TITLE]
      </p>
      <p style="margin: 0; font-family: 'Montserrat', Arial, sans-serif; font-size: 15px; color: #333333; line-height: 1.6;">
        [INFO_CONTENT]
      </p>
    </td>
  </tr>
</table>
```

### Outline Button (Secondary CTA)

```html
<table role="presentation" cellspacing="0" cellpadding="0" border="0">
  <tr>
    <td style="background-color: transparent; border: 1px solid #48A1AA;">
      <a href="[LINK]" 
         target="_blank" 
         style="display: inline-block; padding: 12px 25px; font-family: 'Montserrat', Arial, sans-serif; font-size: 11px; font-weight: 600; color: #48A1AA; text-decoration: none; letter-spacing: 2px; text-transform: uppercase;">
        [BUTTON_TEXT]
      </a>
    </td>
  </tr>
</table>
```

---

## Email Types & The Guest Journey

### Sequence Overview

```
Booking → 7 Days Before → 3 Days Before → Day Of → Day 2 → Checkout → 24h After → 6 Months
   ↓           ↓              ↓            ↓         ↓        ↓          ↓           ↓
Confirm    Excitement     Logistics    Access    Check-in   Farewell   Review    Win-Back
```

### Email-Specific Guidelines

| Email Type | Tone | Hero Image | Primary CTA |
|------------|------|------------|-------------|
| Booking Confirmation | Celebratory | Property hero | View Reservation |
| Excitement Builder | Aspirational | Sunset/lifestyle | Explore the Keys |
| Logistics | Helpful, clear | Property exterior | View Check-In Details |
| Access Details | Practical | Property entrance | Get Directions |
| Check-In Follow-Up | Warm, attentive | Amenity shot | Book an Activity |
| Farewell | Grateful, warm | Sunset | Book Your Return |
| Review Request | Personal | Best property shot | Share Your Experience |
| Win-Back | Nostalgic | Multiple properties | Book Direct & Save |
| Newsletter | Editorial, curated | Lifestyle/seasonal | Multiple CTAs |

---

## Subject Line Formulas

### The 8 Proven Formulas

1. **Question**: "Ready for your Florida Keys escape?"
2. **How-To**: "How to check in (takes 60 seconds)"
3. **Scarcity**: "Last chance: Book your return at 15% off"
4. **Announcement**: "Your access code is ready"
5. **Number**: "7 days until your toes hit Keys sand"
6. **Curiosity Gap**: "The one thing most guests forget..."
7. **Surprise**: "A little thank you from the team"
8. **Personalization**: "%%FIRSTNAME%%, your Keys adventure awaits"

### The Four U's Scorecard

Rate each subject line 1-4 on:
- **Useful**: Does it promise value?
- **Urgent**: Is there a time element?
- **Ultra-specific**: Are details concrete?
- **Unique**: Does it stand out?

Target: **Score 10+** out of 16

---

## Pre-Delivery Checklist

Before presenting ANY email, Claude must verify:

### Links & Images
- [ ] Logo URL loads (web_fetch to confirm)
- [ ] Hero image URL loads
- [ ] All gallery images load
- [ ] CTA destination is valid
- [ ] Social links work
- [ ] Property page is live

### Email Client Compatibility ⚠️
- [ ] Logo is PNG format (not SVG)
- [ ] No inline SVG elements
- [ ] No CSS gradients (solid colors only)
- [ ] No rgba() colors (solid hex only)
- [ ] No CSS filters (brightness, invert)
- [ ] No box-shadow (use border instead)
- [ ] Footer uses Ocean Blue #2E6E7A (not black)
- [ ] Special characters use HTML entities (&bull; &mdash; &#10022;)

### Design Quality
- [ ] Follows luxury editorial aesthetic (not generic)
- [ ] Typography hierarchy is correct (Cormorant headings, Montserrat body)
- [ ] Brand colors are accurate
- [ ] Accent bar or decorative elements included
- [ ] Footer uses deep ocean blue (#2E6E7A)

### Technical
- [ ] All CSS is inline
- [ ] Images have alt text
- [ ] Merge tags use %%FORMAT%%
- [ ] MSO conditionals for Outlook
- [ ] Preheader text included
- [ ] Unsubscribe link present

### Content
- [ ] Subject line uses proven formula
- [ ] Preview text is 85-100 characters
- [ ] Copy is warm, not corporate
- [ ] Single clear primary CTA
- [ ] Personalization tokens included

---

## Audit Report Format

Present results to user:

```
## Email Audit Complete ✓

### Content
- Subject: [SUBJECT LINE]
- Four U's Score: [X]/16
- Preview: [PREVIEW TEXT]

### Links Validated
✅ Logo: Confirmed
✅ Hero Image: [URL confirmed]
✅ CTA: [Destination confirmed]
✅ Social: Instagram, Facebook
✅ Property Page: [URL confirmed]

### Design
✅ Luxury editorial aesthetic applied
✅ Cormorant/Montserrat typography
✅ Brand colors consistent
✅ Wave divider included

### Technical
✅ Inline CSS only
✅ Outlook fallbacks included
✅ Dark mode meta tags
✅ Mobile responsive

**Ready for StayFi upload.**
```

---

## Handling Failures

### If property page doesn't load:
"I couldn't load [property name] from paraisovacationrentals.com. Please verify the property URL or upload photos directly."

### If image URL is broken:
Mark with placeholder and flag:
```html
<td style="background-color: #F9F7F3; padding: 40px; text-align: center;">
  <p style="color: #666; font-size: 14px;">
    ⚠️ [IMAGE NEEDED: Property hero photo]<br>
    <small>Upload image or provide URL</small>
  </p>
</td>
```

### If external link is down:
"The [service] link appears temporarily unavailable. I've kept it in the email but recommend testing before sending."

---

## Example Prompts

- "Create a welcome email for guests arriving at Blue Pearl next week"
- "Write a review request email that goes to our Google page"
- "Design a win-back email for guests who stayed 6 months ago"
- "Create a January newsletter featuring winter fishing season"
- "Build a check-in details email for Ocean Muse"
- "Make a farewell email with a direct booking CTA"

---

## Related VPVR Skills

| Skill | Use For |
|-------|---------|
| **frontend-design** | Bold aesthetic direction, design thinking |
| **vpvr-brand** | Colors, fonts, logos, brand voice |
| **property-descriptions** | Property details and amenity lists |
| **gemini-images** | Generate custom header images |
| **social-content** | Repurpose email content for social |

---

## Changelog

- **v2.3** (Jan 2026): Comprehensive logo documentation with Email Logo Selection Guide. Added code examples for both dark AND light background variations. Clear decision framework: dark bg → cream logos, light bg → teal logos. Added CTA section and content section logo guidance.
- **v2.2** (Jan 2026): Added complete logo library with 8 variants (icons + horizontal wordmarks in cream/teal, @1x/@2x). Header now uses horizontal wordmark `vpvr-logo-cream@2x.png` at 280×47px. Footer uses icon `vpvr-icon-cream@2x.png` at 70×70px. Deprecated stacked logos that displayed too small.
- **v2.1** (Jan 2026): Added Email Client Compatibility section with critical rules for Gmail/Outlook support. Fixed: SVG logos → PNG, CSS gradients → solid colors, rgba() → hex, inline SVG → accent bars, unicode → HTML entities, black footer → Ocean Blue. Updated Pre-Delivery Checklist with compatibility checks.
- **v2.0** (Jan 2026): Complete redesign with luxury editorial aesthetic, frontend-design skill integration, updated templates with wave dividers and Cormorant typography, simplified property sourcing workflow