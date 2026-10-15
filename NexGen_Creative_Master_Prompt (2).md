# MASTER BUILD PROMPT — NexGen Creative Website

Use everything below to set up and deploy this site on **Netlify**, following the build notes in Sections 9 and 12 for how Netlify's own tools (Netlify Forms, Netlify Identity, Decap CMS) map to each requirement.

---

## 1. Project Summary

Build an **ultra-premium, interactive website** for **NexGen Creative**, a full-service creative agency that helps businesses across 7 industries turn their ideas into reality through design, marketing, technology, and AI-powered automation.

The site must feel high-end, cinematic, and confident — not a generic template. Visitors should immediately sense "this agency builds premium things," and the site itself should double as proof of that promise.

---

## 2. Brand Identity

- **Company Name:** NexGen Creative
- **Tagline:** Design • Marketing • Technology • Innovation
- **Logo:** A monogram combining "N" and "G" in brushed gold and brushed silver metal, on a pure black background. Use the uploaded logo file as-is (do not recreate or alter it).
- **A working visual reference build already exists** — a published front-end preview at: `https://claude.ai/artifact/NBn77JKBD6Bu1LVyFMRGJY`. Treat this as the locked design spec. Match its layout, palette, typography, motion, and 3D treatment exactly — do not reinterpret or default to a generic template. Where anything below is ambiguous, the reference build is the source of truth.
- **Color Palette (vibrant, not metallic gold/silver — this supersedes any muted/metallic direction):**
  - Background base: Deep space navy/near-black (#0B0A1A), secondary panel background (#120F26 / #17142E)
  - Primary accent: Electric violet (#7C3AFF)
  - Secondary accent: Hot magenta/pink (#FF3D9A)
  - Tertiary accent: Bright cyan (#22E7FF)
  - Supporting accents: Amber (#FFB020) and lime (#A6FF4D), used sparingly for icons/highlights
  - Text: Off-white (#F4F2FF) primary, muted lavender-grey (#B7B2D6) for secondary text
  - Gradients: Diagonal gradients combining violet→magenta, cyan→violet, and amber→magenta are used throughout for buttons, icon badges, and headline accents
- **Typography:** "Unbounded" (bold, geometric, display weight) for all headings/logo-adjacent text; "Manrope" for body copy. Both loaded from Google Fonts. Headline accent words are highlighted using a gradient text-fill (violet→magenta), not bold/italic/color-block treatments.
- **Visual Style — vibrant + 3D, not flat/minimal:**
  - Dark, saturated background with a genuinely three-dimensional, animated centerpiece in the hero (an interactive rotating 3D object built with Three.js/WebGL — e.g., a torus-knot or abstract geometric form in the brand gradient colors, lit with colored point lights, subtly responsive to cursor movement)
  - Service and industry cards use real 3D perspective tilt on hover/pointer movement (not just a flat drop-shadow hover), giving a tactile, dimensional feel
  - Rounded, soft-edged cards (20px radius) on dark glass-like surfaces, with glow/blur accent shapes bleeding out of card corners
  - One deliberate animated moment on page load (hero), rather than scroll-triggered fade-ins scattered across every section
  - Avoid flat corporate/SaaS-template aesthetics, avoid muted/pastel palettes, avoid all-caps eyebrow labels — this should feel energetic, modern, and a little futuristic, appropriate for a studio that builds AI and creative work.

---

## 3. Target Audience (Who We Serve)

The site should speak directly to decision-makers in these industries, ideally via a dedicated "Industries We Serve" section with tailored messaging/icons for each:

1. Real Estate companies
2. Event Management companies
3. Manufacturing (MFCG) companies
4. Medicine / Pharma companies
5. Cafés & Restaurants
6. Marketing Agencies (partner/white-label work)
7. Film Production Houses

Each industry card/section should briefly show "what we can do for you" pulling from the services list below, so a visitor from any of these sectors immediately sees relevance.

---

## 4. Services Offered (What We Do)

Build a clear, visually rich Services section covering:

1. **Website Design & Development**
2. **Marketing Materials Design** (brochures, catalogs, letterheads, etc.)
3. **Poster, Banner & Billboard Design**
4. **Social Media Marketing** (content, strategy, management)
5. **Mobile App Development** (for client organizations)
6. **AI-Powered Application Automation & Agentic AI Creation** (highlight this as a cutting-edge differentiator)
7. **Promotional Video Production** (for marketing/ad campaigns)

Each service should have its own short description, a relevant icon/visual, and a CTA ("Get a Quote" / "Discuss Your Project") linking to the contact/quote form — **no pricing or packages displayed anywhere on the public site**; all pricing is quote-on-request.

---

## 5. Brand Promise / Messaging Pillars

Weave these into hero sections, about page, and CTAs (not as a literal bullet list, but as brand voice):

- "You dream it, we build it" — we turn imagination into real-world results.
- Reliable, on-time delivery.
- Dedicated after-sales support/service.
- We solve problems, not just deliver designs.

---

## 6. Site Structure (Pages)

1. **Home** — Hero (logo/animated intro), brand promise, services overview, industries served, featured work/portfolio teaser, testimonials, AI/tech differentiator highlight, final CTA.
2. **About Us** — Company story, founder (Anirban Das) profile, mission/vision, why "NexGen."
3. **Services** — Full breakdown of all 7 service offerings (see Section 4).
4. **Industries We Serve** — Dedicated section/page for the 7 target sectors (see Section 3).
5. **Portfolio / Our Work** — Case studies and project showcases, filterable by industry or service type.
6. **AI & Automation** — A standout page/section specifically showcasing agentic AI and automation capabilities (this is a key differentiator — make it feel futuristic and interactive, e.g., an embedded chatbot demo or interactive workflow visual).
7. **Blog / Insights** (optional but recommended for SEO) — Articles on design, marketing, and AI trends.
8. **Contact Us** — Contact form (Get a Quote), map, direct contact details, social links.

---

## 7. Interactivity & "Problem-Solver" Feel

- The site should not be static — include a 3D animated hero centerpiece, 3D pointer-tilt on service/industry cards, and micro-interactions on buttons.
- Include at least one genuinely interactive tool that demonstrates the agency's own capability, for example:
  - An AI chatbot widget (front-and-center on the AI & Automation page) that can answer visitor questions about services and capture leads — this doubles as a live demo of "agentic AI" work.
  - An interactive "Get a Quote" flow that asks visitors a few guided questions (industry, service needed, budget-free) and routes it as a qualified lead to the admin panel, rather than a plain static form.
- All photography should be premium/cinematic (real client work where available, high-quality stock/AI-generated elsewhere — see content notes below), consistent with the vibrant color grading used across the rest of the site rather than desaturated/neutral stock imagery.

---

## 8. Content Strategy

- Use a **mix of real content and premium placeholder content**:
  - Real: company logo, founder details, actual contact info (see Section 10), and any real project photos/case studies once supplied.
  - Placeholder: where real portfolio images aren't yet available, use high-quality stock or AI-generated imagery that matches the industries served (real estate exteriors, event setups, restaurant interiors, film sets, etc.) so the site never looks empty.
- Structure all content sections so that placeholder items can be swapped for real ones later via the admin panel without a rebuild.

---

## 9. Admin / Backend Requirements (Content Management) — Netlify Implementation

Netlify is a hosting/deployment platform, not an all-in-one app builder — it doesn't generate a custom database and admin panel from a prompt the way an AI app builder would. To get the "only I can add/delete content" outcome you asked for, wire the site up using Netlify's own building blocks:

- **Content management → Decap CMS (formerly Netlify CMS):** Install Decap CMS at a route like `/admin`, backed by a `config.yml` that defines editable collections for: services, industries, portfolio/case studies, blog posts (if included), the About/founder bio, and contact/social details. This gives a real add/edit/delete interface for every content type without a developer touching code, with changes committed straight to the site's Git repository and auto-deployed by Netlify.
- **Authentication → Netlify Identity:** Use Netlify Identity (confirmed as a currently supported, actively maintained Netlify feature) to gate the `/admin` route so only invited users — starting with Anirban Das — can log in and edit content. Additional editors can be invited later from the Netlify dashboard.
- **Lead / Inquiry capture → Netlify Forms:** Build the "Get a Quote" and Contact forms as native Netlify Forms (a plain HTML `<form>` with a `data-netlify="true"` attribute — no separate backend needed). Every submission is automatically stored and viewable in the Netlify dashboard under Forms, with name, email, phone, message, and selected industry/service captured as fields.
- **Notifications:** Configure a Netlify Forms notification (via the dashboard, or a Slack/email/Zapier outgoing webhook) so Anirban Das gets an email the moment a new inquiry comes in.
- **Lead status tracking (new/contacted/closed):** Netlify Forms itself doesn't have a status field. If tracking lead status is important, connect form submissions to a lightweight external tool (e.g., a connected Google Sheet, Airtable, or a simple Netlify Function writing to a small database such as Supabase) rather than expecting this inside Netlify's own UI.
- The `/admin` login should not appear in the public navigation — link to it only directly.

---

## 10. Contact Information (To Be Used Exactly As-Is)

- **Company Name:** NexGen Creative
- **Founder/Promoter:** Anirban Das
- **Email:** anirbanaichamp@gmail.com
- **Mobile:** +91 96742 77797
- **Address:** 3/126, Paschim Putiary, Kolkata – 700041, West Bengal, India

Include these in the footer (every page), the Contact page, and structured data (for SEO/local search/Google Maps embed).

---

## 11. Technical & SEO Requirements

- Fully responsive across mobile, tablet, and desktop.
- Fast load times — optimize all images/media.
- SEO-friendly structure (meta titles/descriptions per page, semantic HTML, alt text on images).
- Google Maps embed on the Contact page using the address above.
- Social media links in the footer (placeholder icons if handles aren't provided yet — admin should be able to update these).
- Secure contact/quote forms with spam protection.

---

## 12. Build & Deployment Notes (Netlify)

Build this as a flagship agency portfolio site — think premium creative studio, not a small business template. Prioritize visual impact, smooth interactivity, and a content workflow that gives the owner full independent control over every piece of content without needing a developer for updates.

- Use the published reference build linked in Section 2 as the definitive visual target: same palette, same 3D hero treatment, same tilt-card interactivity, same typography.
- Structure the site as a static site (plain HTML/CSS/JS, or a static-site generator such as Eleventy/Astro/Next.js static export — any of these deploy cleanly on Netlify) so it's Decap-CMS-compatible and deploys instantly on every content change.
- Connect the project's Git repository to Netlify for continuous deployment: every edit made through the `/admin` CMS commits to the repo, and Netlify automatically rebuilds and republishes the live site within moments.
- Once deployed, connect your own domain (e.g., `nexgencreative.com`) under Netlify's domain settings, with free automatic HTTPS.
