# Tarikh — Landing Page Prompt for Claude Code

Paste this entire document into Claude Code. Follow every instruction exactly.

---

## What You Are Building

A landing page for **Tarikh** — an AI WhatsApp assistant that helps solo Indian lawyers never miss a court hearing date. This is a top 1% product landing page. Aesthetic reference: Linear.app, Stripe.com. Not a template. Not a SaaS boilerplate.

---

## Tech Stack

- Single `index.html` file — embedded CSS and vanilla JS only
- No frameworks. No CDN imports. No external dependencies.
- Opens and works perfectly by double-clicking the file in a browser.

---

## Brand Identity

### Logo Mark
Embed this SVG exactly as written. Use `currentColor` so it inherits text color:

```svg
<svg width="36" height="36" viewBox="0 0 100 100">
  <rect x="18" y="17" width="64" height="10" rx="5" fill="currentColor"/>
  <path d="M 25,24 L 25,80 Q 25,87 32,87 L 37,87 Q 43,87 43,80 L 43,24 Z" fill="currentColor"/>
  <path d="M 57,24 L 57,80 Q 57,87 63,87 L 68,87 Q 75,87 75,80 L 75,24 Z" fill="currentColor"/>
</svg>
```

### Wordmark
"Tarikh" — Georgia serif, letter-spacing: 4px, font-weight: 500

### Colors (CSS variables)
```css
--bg: #FAFAF8;
--bg-dark: #0C0C0C;
--bg-surface: #F2F1EE;
--bg-card-dark: #161616;
--text-primary: #0C0C0C;
--text-secondary: #6B6B6B;
--text-muted: #9B9B9B;
--accent: #C8820E;
--border: #E4E3DF;
--border-dark: #242424;
--white: #FFFFFF;
```

### Typography
- **Headings:** Georgia, "Times New Roman", serif
- **Body:** "Helvetica Neue", Helvetica, Arial, sans-serif
- **Never use:** Inter, Roboto, system-ui

### Design Rules (non-negotiable)
1. Sharp corners everywhere — `border-radius: 0` on all buttons and inputs. Pills/bubbles are the only exception.
2. No gradients. No box-shadows. No glow. Completely flat.
3. Accent gold `#C8820E` used only on: the period in the tagline, the bottom CTA button, stat numbers in problem section.
4. Serif for ALL headings. Sans for body and UI.
5. Minimum section padding: 110px top and bottom.
6. Button hover: invert — black button becomes white with 1.5px black border, black text. 200ms ease transition.
7. Mobile responsive below 768px — single column, reduced heading sizes, full-width buttons.
8. Smooth scroll on nav links.

---

## CTA Strategy (read carefully — this is intentional)

**Two-stage trust building. No waitlist. No form on first ask.**

**Stage 1 — Zero commitment CTA (in hero):**
Button label: `"See how it works ↓"`
Action: Smooth scroll to the WhatsApp demo section on the page.
No number. No click away. Just scroll.

**Stage 2 — Earned conversion CTA (at bottom of page):**
A simple form — two fields only:
- Name (placeholder: "Your name")
- WhatsApp number (placeholder: "Your WhatsApp number")

Button label: `"Set me up →"`
Button style: Background `#C8820E`, white text, sharp corners, padding 14px 28px.

Below the button, small text: `"We'll personally message you on WhatsApp to get you started."` — #9B9B9B, 13px, italic.

This line does the trust work. It tells them exactly what happens next.

On form submit — just show a confirmation message in place of the form:
`"Done. We'll WhatsApp you within 24 hours."` — no backend needed.

---

## Page Sections

### Section 1 — Navbar
- **Left:** Logo mark SVG (color: #0C0C0C) + "Tarikh" wordmark (Georgia, letter-spacing: 4px, 18px, color: #0C0C0C). Gap between mark and wordmark: 10px.
- **Right:** Single button — `"See how it works"` — border: 1.5px solid #0C0C0C, background: transparent, color: #0C0C0C, padding: 9px 22px, border-radius: 0, font-size: 14px. On hover: background #0C0C0C, color white.
- Navbar: background #FAFAF8, border-bottom: 1px solid #E4E3DF, sticky top, padding: 0 5%.

---

### Section 2 — Hero
Full viewport height. All content centered vertically and horizontally.

**Pre-headline badge:**
Small pill — text: `"Now in early access"` with a tiny filled circle (6px, color #C8820E) to its left.
Style: background #F2F1EE, border: 1px solid #E4E3DF, border-radius: 100px, padding: 6px 16px, font-size: 12px, color: #6B6B6B, letter-spacing: 0.5px, display: inline-flex, align-items: center, gap: 8px.

**Headline:**
```
"The judge said next date.
Did you write it down?"
```
Georgia serif. Font-size: clamp(40px, 5.5vw, 72px). Line-height: 1.08. Font-weight: 500. Color: #0C0C0C. Letter-spacing: -1.5px. Max-width: 700px. Centered. Two lines — use `<br>` to force the break.

**Sub-headline:**
```
"Tarikh sits on WhatsApp. After every hearing, send one message — case name, date, court. We'll remind you the evening before and the morning of. No app. No form. Just a message."
```
Font-size: 17px. Color: #6B6B6B. Max-width: 500px. Line-height: 1.75. Centered. Margin-top: 24px.

**CTA:**
Button: `"See how it works ↓"` — background: #0C0C0C, color: white, padding: 14px 32px, border-radius: 0, font-size: 15px, letter-spacing: 0.3px. On hover: background white, color #0C0C0C, border: 1.5px solid #0C0C0C.
Below button: `"47 advocates are already tracking their cases"` — color: #9B9B9B, font-size: 13px, margin-top: 14px.

Scroll indicator at very bottom of hero: a small animated down-arrow or thin vertical line that pulses. Subtle. CSS only.

---

### Section 3 — WhatsApp Demo
ID: `demo` (navbar and hero CTA scroll here)
Background: #0C0C0C

**Section label:** `"See it work"` — font-size: 11px, letter-spacing: 3px, color: #C8820E, text-transform: uppercase, font-weight: 500.

**Heading:** `"One message after court. That's it."` — Georgia serif, font-size: clamp(28px, 3.5vw, 46px), color: white, font-weight: 500, margin-top: 12px.

**The phone mockup — centered, max-width 360px:**

A phone frame: just a rounded rectangle. Border: 2px solid #2A2A2A. Border-radius: 40px. Background: #111111. Padding: 20px 16px. No images — pure CSS/HTML.

Inside the phone, a WhatsApp-style chat UI:

Header bar inside phone: Dark bar (#1A1A1A) showing "Tarikh" name with the logo mark in white (16px) and a green online dot.

Chat messages (build these as styled divs):

**Message 1 — User (right side, sent):**
Background: #005C4B (WhatsApp green-dark). Color: white. Border-radius: 12px 12px 2px 12px. Padding: 10px 14px. Max-width: 75%. Align right. Font-size: 14px. Line-height: 1.5.
Text: `"sharma vs state civil court next date 15 jan"`
Timestamp below: `"11:42 AM  ✓✓"` — font-size: 11px, color: rgba(255,255,255,0.6).

**Message 2 — Tarikh (left side, received):**
Background: #1F2C34. Color: #E9EDEF. Border-radius: 12px 12px 12px 2px. Padding: 10px 14px. Max-width: 82%. Align left. Font-size: 14px. Line-height: 1.5.
Text: `"Got it. Sharma vs State, Civil Court — 15th January. I'll remind you the evening before and the morning of. You have 3 other hearings this week. Want a summary?"` 
Timestamp: `"11:42 AM"` — font-size: 11px, color: rgba(255,255,255,0.4).

**Message 3 — Tarikh reminder (left side):**
Background: #1F2C34. Same styling.
Text: `"🔔 Tomorrow — Sharma vs State, Civil Court, 10:00 AM. You've got this."`
Timestamp: `"Jan 14, 8:00 PM"` — font-size: 11px.

Below the phone mockup, a small caption in white:
`"Tarikh understands Hinglish, typos, and incomplete messages."` — #555, font-size: 13px, italic, text-align: center, margin-top: 24px.

---

### Section 4 — The Problem
Background: #0C0C0C, continuing from demo section. Add a thin 1px rule in #1E1E1E to separate.

**Section label:** `"The problem"` — font-size: 11px, letter-spacing: 3px, color: #C8820E, uppercase.

**Heading:**
```
"Every lawyer has missed a tarikh.
Most won't admit it."
```
Georgia serif, white, font-size: clamp(30px, 3.5vw, 48px), font-weight: 500, line-height: 1.15, letter-spacing: -0.5px.

**Three cards in a row** (stack on mobile):
Card style: background #161616, border: 1px solid #242424, border-radius: 0, padding: 36px 32px.

Card 1:
- Stat: `"87%"` — Georgia, font-size: 52px, color: #C8820E, font-weight: 500, line-height: 1, letter-spacing: -1px
- Label: `"of India's pending cases are in district courts"` — white, font-size: 16px, font-weight: 500, margin-top: 12px
- Sub: `"The lawyers with the most cases have the least support."` — #666, font-size: 14px, line-height: 1.6, margin-top: 8px

Card 2:
- Stat: `"0"` — same style as above, color: #C8820E
- Label: `"proactive reminders from the court system"` — white
- Sub: `"The cause list tells you today. Nothing tells you what's coming next week."` — #666

Card 3:
- Stat: `"1"` — same style
- Label: `"missed date can change everything"` — white
- Sub: `"One missed hearing. One broken client relationship. One reputation that takes years to rebuild."` — #666

---

### Section 5 — How It Works
Background: #FAFAF8

**Section label:** `"How it works"` — 11px, letter-spaced, #9B9B9B, uppercase.

**Heading:** `"Three messages a week. Never miss a hearing."` — Georgia serif, font-size: clamp(28px, 3vw, 44px), #0C0C0C, font-weight: 500, letter-spacing: -0.5px.

**Three steps in a row** (stack on mobile). Between steps 1→2 and 2→3, a thin horizontal connector line in #E4E3DF. On mobile, hide the connector.

Step 1 — **After court, just message**
Icon: A simple speech bubble shape — pure CSS. 40px circle, background #F2F1EE, with a small CSS speech bubble drawn inside using borders.
Title: `"After court, just message"` — 500 weight, 17px, #0C0C0C, Georgia
Body: `"Case name, date, court. Any order. Any format. Hinglish is fine. Typos are fine. Just send it."` — 15px, #6B6B6B, line-height: 1.7

Step 2 — **We confirm it back**
Icon: A checkmark in a circle — pure CSS/SVG.
Title: `"We confirm it back"`
Body: `"Tarikh reads your message, picks out the details, and sends you a confirmation immediately. If something looks off, you'll know."` — same style

Step 3 — **You get reminded**
Icon: A bell — pure SVG inline.
Title: `"You get reminded"`
Body: `"Evening before. Morning of. Two WhatsApp messages with the case name, court, and time. That's it."` — same style

---

### Section 6 — Feature Pills Strip
Background: #F2F1EE
Padding: 32px 5%. Single centered row of pills, wrapping on mobile.

Pills (each one):
Style: background white, border: 1px solid #E4E3DF, border-radius: 100px, padding: 9px 20px, font-size: 13px, color: #0C0C0C, letter-spacing: 0.2px, display: inline-flex.

Content:
- `"Works in Hinglish"`
- `"No app to download"`
- `"District + High Court"`
- `"Works on any phone"`
- `"Free to start"`

Gap between pills: 10px. Wrap: wrap.

---

### Section 7 — Get Started (Conversion)
Background: #0C0C0C

**Heading:**
```
"Your next tarikh is already set.
Are you tracking it?"
```
Georgia serif, white, font-size: clamp(28px, 3.5vw, 48px), font-weight: 500, line-height: 1.15, letter-spacing: -0.5px, max-width: 580px, centered.

**Sub:**
`"Send us your name and WhatsApp number. We'll personally message you to get you started."` — color: #666, font-size: 16px, line-height: 1.7, margin-top: 16px, max-width: 420px, centered.

**Form (id="signup-form"):**
Two inputs stacked, max-width: 360px, centered, margin-top: 36px.

Input 1 — Name:
placeholder: `"Your name"`, background: #161616, border: 1px solid #2A2A2A, color: white, padding: 14px 18px, border-radius: 0, font-size: 15px, width: 100%. On focus: border-color #C8820E, outline: none.

Input 2 — WhatsApp:
placeholder: `"Your WhatsApp number"`, same styles.

Button: `"Set me up →"` — background: #C8820E, color: white, border: none, padding: 15px 28px, border-radius: 0, font-size: 15px, letter-spacing: 0.3px, width: 100%, margin-top: 2px, cursor: pointer. On hover: background #A06A0A.

Below form:
`"We'll personally message you on WhatsApp within 24 hours."` — color: #555, font-size: 13px, font-style: italic, margin-top: 16px, text-align: center.

**On form submit — JS behavior:**
Prevent default. Hide the form. Show in its place:
```
"Done. We'll WhatsApp you within 24 hours."
```
Style: Georgia serif, white, font-size: 22px, text-align: center. Fade in smoothly.

---

### Section 8 — Footer
Background: #0C0C0C. Border-top: 1px solid #1E1E1E. Padding: 32px 5%.
Single row, space-between.

Left: Logo mark SVG (color: white, 28px) + "Tarikh" wordmark (Georgia, white, letter-spacing: 4px, 16px). Gap: 10px. Aligned center vertically.

Right: `"Made for the lawyer who runs his practice alone."` — color: #444, font-size: 13px, font-style: italic.

On mobile: stack center-aligned, gap 12px.

---

## Animations (CSS only, no JS libraries)

1. **Hero content:** Fade up on load — `opacity: 0 → 1`, `translateY: 20px → 0`, duration 0.7s, ease-out. Stagger: badge first, then headline (0.1s delay), then sub (0.2s), then button (0.3s).

2. **WhatsApp messages:** Each message slides in from its side with a 0.3s delay between them. Use `@keyframes slideInRight` and `@keyframes slideInLeft`. Trigger on page load with animation-delay.

3. **Problem cards:** On scroll into view — use `IntersectionObserver` in JS (small, no library). Cards fade up one by one with 100ms stagger between them.

4. **Scroll indicator in hero:** A thin vertical line (2px wide, 40px tall, color #0C0C0C) that pulses up and down using `@keyframes`. Centers at bottom of hero.

---

## Final Instructions to Claude Code

1. Build this as a single `index.html` file. Everything embedded.
2. Test every section visually in your head before outputting. No placeholder text anywhere.
3. The WhatsApp mockup must look real — not cartoonish, not generic.
4. Every line of copy must be used exactly as written above. Do not paraphrase or "improve" it.
5. The two-stage CTA is intentional. Do not add a CTA button in the hero that goes to a form. Hero CTA scrolls to demo only.
6. This page should feel like it was designed by a studio that charges ₹10 lakh for a landing page. Craft every detail.
7. When in doubt — add whitespace. Never crowd elements.
8. Output the complete file. No truncation. No "continue this yourself."
