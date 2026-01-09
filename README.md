<p align="center">
  <img src="https://paraisovacationrentals.com/wp-content/uploads/2026/01/vpvr-logo-teal@2x.png" alt="Villa Paraiso Logo" width="280">
</p>

<h1 align="center">VPVR Skills Hub</h1>

<p align="center">
  <strong>A Partnership in Premier Hospitality</strong><br>
  AI-powered content skills for the Villa Paraiso team
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Updated-January%202026-48A1AA?style=flat-square" alt="Updated January 2026">
  <img src="https://img.shields.io/badge/Skills-9%20Available-48A1AA?style=flat-square" alt="9 Skills">
  <img src="https://img.shields.io/badge/Platform-Claude%20AI-48A1AA?style=flat-square" alt="Claude AI">
</p>

---

## What Are Skills?

**Skills are instruction manuals for Claude.** They teach the AI exactly how to create VPVR content using our brand voice, proven frameworks, and expert methodologies.

| Without Skills | With Skills |
|----------------|-------------|
| Generic vacation rental content | VPVR brand voice & style |
| Basic suggestions | Expert frameworks (StoryBrand, Challenger Sale) |
| Inconsistent quality | Professional, consistent output |
| Time spent explaining | Just ask and get results |

---

## Installation Guide

### Method 1: Claude.ai Projects (Recommended)

This is the easiest way to use skills. Works in your web browser.

<details open>
<summary><strong>Step-by-Step Instructions</strong></summary>

#### Step 1: Go to Claude

Open **[claude.ai](https://claude.ai)** in your browser and sign in with your account.

#### Step 2: Create a Project

1. Click **"Projects"** in the left sidebar
2. Click the **"+ New Project"** button
3. Give your project a name (e.g., "VPVR Marketing")

#### Step 3: Add Skills to Your Project

1. Inside your project, click **"+ Add content"** at the bottom
2. Select **"Add from URL"**
3. Paste one of the skill URLs from the table below
4. Click **"Add"**
5. Repeat for each skill you need

#### Step 4: Start Using Skills

1. Open a new chat inside your project
2. Ask Claude to help with any task
3. Claude automatically uses all loaded skills

**Example prompts to try:**
- "Write a blog post about fishing in Marathon FL"
- "Create a pre-arrival email for Blue Pearl"
- "What are the VPVR brand colors?"

</details>

---

### Method 2: Claude Code (Terminal)

For developers using Claude in the terminal.

```bash
# Clone the skills repository
git clone https://github.com/MiscMich/vpvr-skills.git

# Skills are automatically available when working in this directory
cd vpvr-skills

# Ask Claude to use any skill
# Example: "Use the stayfi-emails skill to write a welcome email"
```

---

## Available Skills

### Brand & Design

| Skill | What It Does | Add This URL |
|-------|--------------|--------------|
| **VPVR Brand** | Colors (#48A1AA, #EEE5C7), fonts, logos, styling | `https://raw.githubusercontent.com/MiscMich/vpvr-skills/main/marketing/vpvr-brand/SKILL.md` |
| **AI Images** | Prompts for Gemini 3 Pro, Midjourney V7, DALL-E | `https://raw.githubusercontent.com/MiscMich/vpvr-skills/main/marketing/gemini-images/SKILL.md` |

### Content Creation

| Skill | What It Does | Add This URL |
|-------|--------------|--------------|
| **Blog Posts** | SEO-optimized articles with RankMath fields | `https://raw.githubusercontent.com/MiscMich/vpvr-skills/main/marketing/vpvr-blog-posts/SKILL.md` |
| **Property Listings** | Airbnb, VRBO, and direct booking descriptions | `https://raw.githubusercontent.com/MiscMich/vpvr-skills/main/marketing/property-descriptions/SKILL.md` |
| **Social Content** | Instagram, TikTok, Facebook posts & calendars | `https://raw.githubusercontent.com/MiscMich/vpvr-skills/main/marketing/social-content/SKILL.md` |

### Communications

| Skill | What It Does | Add This URL |
|-------|--------------|--------------|
| **StayFi Emails** | HTML email templates for guest journey | `https://raw.githubusercontent.com/MiscMich/vpvr-skills/main/marketing/stayfi-emails/SKILL.md` |
| **Owner Comms** | Reports, pitches, onboarding for property owners | `https://raw.githubusercontent.com/MiscMich/vpvr-skills/main/marketing/owner-comms/SKILL.md` |
| **LinkedIn (Michel)** | Thought leadership posts for CEO | `https://raw.githubusercontent.com/MiscMich/vpvr-skills/main/marketing/linkedin-ceo/SKILL.md` |

### SEO & Optimization

| Skill | What It Does | Add This URL |
|-------|--------------|--------------|
| **SEO/AEO** | Search optimization for Google & AI engines | `https://raw.githubusercontent.com/MiscMich/vpvr-skills/main/marketing/vpvr-seo-aeo/SKILL.md` |

---

## Quick Start by Role

Choose the skills that match your work:

| Your Role | Recommended Skills | What You Can Create |
|-----------|-------------------|---------------------|
| **Marketing Manager** | vpvr-brand + social-content + vpvr-blog-posts | Social calendars, blog posts, branded content |
| **Property Listings** | property-descriptions + gemini-images | Airbnb/VRBO listings, property photos |
| **Owner Relations** | owner-comms + vpvr-brand | Monthly reports, acquisition pitches |
| **Email Marketing** | stayfi-emails + vpvr-brand | Guest emails, drip campaigns |
| **Content Writer** | vpvr-blog-posts + vpvr-seo-aeo | SEO articles, guides, FAQs |

---

## Example Prompts

Once skills are loaded, try these:

| Task | Example Prompt |
|------|----------------|
| **Guest Email** | "Create a pre-arrival email for Blue Pearl with check-in instructions" |
| **Blog Post** | "Write a 1500-word blog about the best fishing spots in Marathon FL" |
| **Property Listing** | "Write an Airbnb listing for Ocean Muse highlighting the pool and dock" |
| **Social Calendar** | "Create a week's content calendar for Instagram focusing on sunset photos" |
| **Owner Report** | "Create a monthly performance report for Blue Pearl for December 2025" |
| **AI Image** | "Create a Gemini prompt for a sunset pool shot at our Marathon property" |
| **LinkedIn Post** | "Write a LinkedIn post about vacation rental trends for 2026" |

---

## Troubleshooting

<details>
<summary><strong>Claude doesn't seem to know the skill</strong></summary>

- Make sure you're chatting **inside the Project** where you added the skill
- Try starting a **new conversation** within that Project
- Verify the skill was added: ask "What skills do you have loaded?"

</details>

<details>
<summary><strong>Can I use multiple skills at once?</strong></summary>

**Yes!** Add as many skills as you need to the same Project. Claude uses them all together. Skills are designed to reference each other (e.g., StayFi Emails uses Brand colors automatically).

</details>

<details>
<summary><strong>How do I update a skill?</strong></summary>

Skills update automatically when we push changes to GitHub. If you added via URL, you'll always get the latest version.

</details>

<details>
<summary><strong>I need a skill that doesn't exist</strong></summary>

Use the **Skill Creator** to build new skills:
```
https://raw.githubusercontent.com/MiscMich/vpvr-skills/main/skill-from-masters/SKILL.md
```

</details>

---

## Recently Updated

| Date | Skill | What Changed |
|------|-------|--------------|
| Jan 2026 | vpvr-brand | v2.1 - Comprehensive logo library with selection guide, new 2026 horizontal wordmarks |
| Jan 2026 | stayfi-emails | v2.3 - Email logo selection guide, updated to 2026 logo system |
| Jan 2026 | vpvr-seo-aeo | Property Data Source section, AI citation optimization |
| Jan 2026 | gemini-images | Gemini 3 Pro (Nano Banana) multi-image reference system |
| Jan 2026 | linkedin-ceo | Multi-image posts (6.60% engagement rate) |
| Jan 2026 | owner-comms | JOLT Effect framework for overcoming indecision |

---

## Repository Structure

```
vpvr-skills/
├── marketing/                   # All marketing skills
│   ├── vpvr-brand/             # Brand colors, fonts, styling
│   ├── vpvr-blog-posts/        # SEO blog content
│   ├── stayfi-emails/          # Guest email templates
│   ├── social-content/         # Social media posts
│   ├── property-descriptions/  # Listing copy
│   ├── gemini-images/          # AI image prompts
│   ├── owner-comms/            # Owner communications
│   ├── linkedin-ceo/           # Michel's LinkedIn
│   └── vpvr-seo-aeo/           # Search optimization
├── skill-from-masters/         # Create new skills
└── claudedocs/                 # Reports & analysis
```

---

## Need Help?

**Contact:** Michel or the Operations team

We're happy to help you get set up or create new skills for your work!

---

<p align="center">
  <strong>Villa Paraiso Vacation Rentals</strong><br>
  <em>A Partnership in Premier Hospitality</em><br><br>
  <img src="https://img.shields.io/badge/Brand%20Color-48A1AA-48A1AA?style=flat-square" alt="Teal">
  <img src="https://img.shields.io/badge/Accent-EEE5C7-EEE5C7?style=flat-square" alt="Cream">
</p>

---

*Last updated: January 2026*
