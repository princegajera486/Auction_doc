# Cricket Auction Customer Website Components

## 1. NAVBAR / HEADER

### 1. Overview
The primary navigation bar at the top of the website. It provides global access to main pages, login/register entry points, and clear branding.

### 2. Importance
Serves as the main orientation point for users. A clean header builds trust and quickly guides organizers to "Create Auction" and viewers to "Live Auctions".

### 3. Screen Preview
------------------------------------------------
[ LOGO ]    Features   Pricing   Live Auctions   [ LOGIN ] [ CREATE AUCTION ]
------------------------------------------------

### 4. Design Instructions
- Layout: Flexbox with space-between. Left: Logo, Center: Nav Links, Right: Action Buttons.
- Spacing: 24px padding top/bottom.
- Typography: Semi-bold, 14px-16px sans-serif.
- Colors: Background should be White or Very Light Gray with a subtle blur (glassmorphism) if sticky.
- Buttons: "Create Auction" should be a solid primary color (Deep Navy). "Login" should be a ghost/outline button.
- Responsive: Collapse links into a clean hamburger menu on mobile; keep Logo and "Create Auction" button visible.

## 2. HERO SECTION

### 1. Overview
The very first section a visitor sees. It combines a strong value proposition headline with a visual representation of the product in action.

### 2. Importance
This is the main conversion engine. It must immediately communicate that this is a professional tool for running live cricket auctions, capturing both organizers and casual viewers.

### 3. Screen Preview
------------------------------------------------
                 RUN YOUR
            CRICKET AUCTION
               LIKE A PRO

     Create • Manage • Bid • Build Squads

      [ CREATE AUCTION ] [ WATCH LIVE ]

              [LIVE AUCTION UI MOCKUP]
------------------------------------------------

### 4. Design Instructions
- Layout: Single column centered on desktop (Headline -> Subtitle -> CTA -> Large Mockup blooming from bottom).
- Typography: Massive, bold headline (64px+). Deep Navy color.
- Images/Cards: Use a realistic, floating representation of a live player auction card with current bids and team logos. Add a subtle drop shadow to pop from the background.
- Background: Clean white with a faint, abstract geometric pattern or a very soft, large radial gradient (Electric Blue to White).
- Animation: Slide up and fade in for the UI Mockup on initial page load.

## 3. STATISTICS / TRUST METRICS

### 1. Overview
A horizontal bar or grid showcasing key platform numbers (e.g., "1,000+ Tournaments", "50,000+ Players").

### 2. Importance
Builds immediate credibility. Shows tournament organizers that the platform is robust, tested, and actively used by others.

### 3. Screen Preview
------------------------------------------------
  1,500+          10,000+          500k+
Tournaments     Teams Created     Bids Placed
------------------------------------------------

### 4. Design Instructions
- Layout: Horizontal flexbox with subtle dividers (1px solid light gray) between metrics.
- Typography: Huge, bold numbers (Electric Blue or Cricket Green). Smaller, uppercase, subtle text for labels.
- Spacing: Generous padding (60px top/bottom).
- Animation: JS-driven count-up animation when the section scrolls into view.

## 4. TODAY'S AUCTIONS (DISCOVERY)

### 1. Overview
A horizontally scrollable or grid section displaying auctions that are happening *right now*.

### 2. Importance
Drives immediate user engagement for viewers. Shows organizers that the platform is highly active and capable of hosting public events.

### 3. Screen Preview
------------------------------------------------
🔥 HAPPENING TODAY                         [View All]

[ Tournament Logo ]       [ Tournament Logo ]
 Surat Premier League      Mumbai Tech Cup
 🔴 LIVE                   Upcoming: 4:00 PM
 8 Teams • 120 Players     6 Teams • 90 Players
 [ VIEW AUCTION ]          [ SET REMINDER ]
------------------------------------------------

### 4. Design Instructions
- Layout: 3-column CSS Grid on desktop. Horizontal scroll snap container on mobile.
- Cards: White background, subtle border, 12px border radius. Slight Y-axis lift on hover.
- Badges: Use a pulsing red dot animation for the "🔴 LIVE" indicator.
- Typography: Clear hierarchy. Tournament name bold and prominent, stats in muted gray.
- Buttons: Full-width outline button at the bottom of the card.

## 5. HOW IT WORKS

### 1. Overview
A step-by-step visual guide explaining the journey from tournament creation to the final squad generation.

### 2. Importance
Demystifies the software. Helps organizers visualize how easy it is to replace their manual/paper processes with this SaaS tool.

### 3. Screen Preview
------------------------------------------------
1. Create Event --> 2. Add Teams & Players --> 3. Run Live Auction

[ Icon: Setup ]     [ Icon: Database ]         [ Icon: Gavel ]
------------------------------------------------

### 4. Design Instructions
- Layout: Horizontal timeline or an alternating left/right zig-zag section.
- Visuals: Pair each step with a custom icon or a micro-screenshot of that specific step in action.
- Colors: Use Deep Navy for the connecting lines, Electric Blue for active/current steps.
- Spacing: Keep it airy (80px between steps) so users aren't overwhelmed by text.

## 6. FEATURE SHOWCASE

### 1. Overview
A grid of cards highlighting specific capabilities of the platform (Real-Time Bidding, Automated Purse Tracking, Bulk Import).

### 2. Importance
Answers the "What can it do?" question. Critical for convincing experienced organizers that all their edge cases are covered.

### 3. Screen Preview
------------------------------------------------
[⚡ Real-Time Bidding]    [💰 Purse Tracking]
Instant bid updates        Automated budget
across all devices.        calculations.

[📊 Detailed Reports]      [📺 TV Overlay]
Export squads & spend.     Optimized for big
                           screen displays.
------------------------------------------------

### 4. Design Instructions
- Layout: 3x2 or 4x2 CSS Grid. 1 column on mobile.
- Cards: Solid Very Light Gray background (no border) or white with a very subtle shadow. Keep them uniform in height.
- Icons: Use a consistent, modern icon set (line icons colored in Electric Blue).
- Typography: Short, punchy titles (18px bold). 2-line maximum descriptions.

## 7. LIVE AUCTION PREVIEW (PUBLIC VIEWER)

### 1. Overview
A large, highly visual section demonstrating exactly what the public sees when an auction is live.

### 2. Importance
Organizers care deeply about how their tournament looks to their audience. This proves the output is premium and professional.

### 3. Screen Preview
------------------------------------------------
"Give your audience a professional experience."

+----------------------------------------------+
| [Player Photo]  Virat K. | All-Rounder       |
|                                              |
| CURRENT BID: ₹ 2,40,000                      |
| WINNING TEAM: [Logo] Titans                  |
|                                              |
| [ Timer: 00:08 ]                 [ SOLD! ]   |
+----------------------------------------------+
------------------------------------------------

### 4. Design Instructions
- Layout: A massive mock browser-window or TV screen centered on the page.
- Visuals: Use high-contrast colors inside the mockup (e.g., Deep Navy background for the player card, bright Cricket Green for the "SOLD!" badge).
- Animation: Auto-play a subtle CSS animation of a bid increasing (numbers flipping) to simulate live action.
- Spacing: 100px padding around the mockup to isolate it as a showpiece.

## 8. PRICING SECTION

### 1. Overview
Clear tiered pricing options displaying what features and limits apply to each tier.

### 2. Importance
Crucial for SaaS conversion. Users need to immediately understand the cost relative to their tournament size without having to contact sales.

### 3. Screen Preview
------------------------------------------------
[ STARTER ]            [ PRO ] (Highlighted)
For small leagues      For growing tournaments
₹ 999 / event          ₹ 2,499 / event
- Up to 8 Teams        - Up to 16 Teams
- 150 Players          - 500 Players
[ START FREE ]         [ CHOOSE PRO ]
------------------------------------------------

### 4. Design Instructions
- Layout: 3-column flex or grid on desktop. Stacked on mobile.
- Cards: The middle "Pro" or "Recommended" card should scale up slightly (transform: scale(1.05)), have a primary color border (Electric Blue), and a prominent solid CTA button.
- Checkmarks: Use Cricket Green checkmark icons for included features.
- Colors: White cards, dark text.

## 9. TESTIMONIALS

### 1. Overview
Quotes and reviews from tournament organizers who have successfully used the platform.

### 2. Importance
Provides social proof. Overcomes objections by showing that real people trust the software for high-stakes, real-money auctions.

### 3. Screen Preview
------------------------------------------------
"We used to do this on paper. CrickBid saved
us hours and looked amazing on the projector."
- Rahul M., Surat Premier League
------------------------------------------------

### 4. Design Instructions
- Layout: Horizontal masonry grid or a clean, auto-playing horizontal carousel.
- Cards: White background. Add a large, faint quotation mark in the background as a watermark.
- Images: Small circular avatars next to the user's name.
- Typography: Italicized body text for the quote. Bold name and muted organization title.

## 10. FAQ (FREQUENTLY ASKED QUESTIONS)

### 1. Overview
A collapsible list of common questions regarding platform capabilities, setup, and pricing.

### 2. Importance
Reduces friction and support tickets. Helps users self-serve answers to objections right before they decide to sign up.

### 3. Screen Preview
------------------------------------------------
What is a cricket auction software?          [+]
Can I display the auction on a TV?           [-]
  -> Yes! Our TV-mode is optimized for...
Do you support bulk player import?           [+]
------------------------------------------------

### 4. Design Instructions
- Layout: Single column, constrained width (e.g., max-width: 800px) centered on the page for reading comfort.
- Interaction: Smooth accordion expand/collapse using CSS transitions (max-height).
- Borders: Clean 1px solid light gray bottom border between questions. No bulky bounding boxes.
- Typography: Questions bolded (18px). Answers in regular, muted text (16px).

## 11. FINAL CTA

### 1. Overview
A high-impact banner at the very bottom of the page prompting the final conversion action.

### 2. Importance
Captures users who have scrolled to the bottom. This is the last chance to convert them before they leave the site or hit the footer.

### 3. Screen Preview
------------------------------------------------
READY TO RUN YOUR NEXT CRICKET AUCTION?
Create your tournament and start bidding today.

      [ CREATE YOUR AUCTION ]
------------------------------------------------

### 4. Design Instructions
- Layout: Full width block, centered text content.
- Background: Deep Navy.
- Typography: White text. Headline large and commanding (48px+).
- Button: Large, high-contrast button (Cricket Green) with strong hover state (glow/lift).
- Spacing: Massive padding (e.g., 100px top/bottom).

## 12. FOOTER

### 1. Overview
The bottom anchor of the website containing secondary links, legal information, and social media links.

### 2. Importance
Provides necessary SEO links and secondary navigation for users looking for specific resources (T&C, Contact, Blog) without cluttering the main header.

### 3. Screen Preview
------------------------------------------------
[LOGO] CrickBid      Product       Company
Making auctions      - Pricing     - About
simple.              - Features    - Contact

© 2026 CrickBid. All rights reserved.
------------------------------------------------

### 4. Design Instructions
- Layout: 4-column grid on desktop, stacking into a single column on mobile.
- Colors: Very Light Gray background with Dark Slate text.
- Typography: Small (14px), clean, no underlines unless hovered.
- Spacing: Generous margins between link groups. 40px padding top/bottom for the entire footer.
