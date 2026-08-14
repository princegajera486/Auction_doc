# Cricket Auction Customer Website Components

This document contains the structural and design requirements for the Cricket Auction SaaS Landing Page, optimized for a pre-launch product focusing on vision, solving pain points, and capturing early users.

## 1. NAVBAR / HEADER

### 1. Component Goal
Provide intuitive navigation that builds immediate trust and funnels users toward the primary conversion action ("Start for Free"). It must feel premium, modern, and sticky.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: Flexbox (Row), `justify-content: space-between`, `align-items: center`.
- **Dimensions**: Width: 100%, Max Content Width: 1280px, Height: 80px.
- **Padding**: `16px` top/bottom, `5%` left/right.
- **Positioning**: Sticky top with `z-index: 50`.

### 3. Styling & Typography
- **Font Family**: Inter, Plus Jakarta Sans, or Outfit (Modern Sans-Serif).
- **Background Theme**: Glassmorphism. `rgba(255, 255, 255, 0.75)` with Background Blur (`backdrop-filter: blur(16px)`).
- **Border**: Subtle bottom hairline border (`1px solid rgba(0,0,0,0.05)`).
- **Nav Links (Center)**: 15px font size, Medium (500) weight, Color: `#4B5563` (Slate Gray).

### 4. Elements & Interactions
- **Left Area (Brand)**: Sleek, high-contrast Logo.
- **Center Area (Navigation)**: Links: *Features, How it Works, Pricing, FAQ*.
  - *Hover State*: Text transitions to `#111827` (Dark Navy) with a crisp micro-animation (e.g., a tiny dot appearing below the active link).
- **Right Area (Actions)**: 
  - *Login Button*: Ghost/Text button. Font weight 600.
  - *Create Auction CTA*: Solid Button. Background: `#0F172A` (Deep Navy) or a vibrant gradient. Text: "Start for Free". Padding: `12px 24px`. Border-radius: `8px` (or pill-shape).
  - *CTA Hover State*: Slight scale-up (`scale: 1.02`) and soft glowing shadow (`box-shadow: 0 8px 16px rgba(15, 23, 42, 0.15)`).

### 5. Screen Preview
```text
--------------------------------------------------------------------------------
[ LOGO ]    Features   How it Works   Pricing   FAQ    [ Login ] [ START FOR FREE ]
--------------------------------------------------------------------------------
```

### 6. Responsive Behavior (Mobile)
- Collapse center links into a clean hamburger menu icon on the far right.
- Maintain the Logo on the left.
- If space permits, keep a smaller, icon-only version of the "Start for Free" CTA next to the hamburger menu.

### 7. AI Generation Prompt
"A premium, modern SaaS website navigation bar. Glassmorphism background with a slight blur. On the far left, a sleek minimalist logo. In the center, evenly spaced modern typography text links. On the far right, a clean login text link next to a prominent, deep navy solid button that says 'Start for Free'. High quality UI, clean aesthetic, Dribbble trending, spacing perfectly balanced."

---

## 2. HERO SECTION (DIGITAL ASCENSION)

### 1. Component Goal
Visually represent the "death of paper" and the transformation into a premium digital experience. It must immediately communicate that the old, messy way of running auctions is over, replaced by a beautiful, high-speed digital workflow.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: Flexbox (Column), `align-items: center`, `text-align: center`.
- **Dimensions**: Min-height: `90vh`, Width: 100%, `overflow: hidden`.
- **Padding**: `120px` top, `0px` bottom (image bleeds off the bottom).

### 3. Styling & Typography
- **Theme**: Light & Soft Mode. Background is a creamy, ultra-light gray (`#FAFAFA`) or pure white, featuring a soft, diffuse glowing aura (like gentle cyan and pastel coral) near the top of the mockup.
- **Headline**: Massive & cinematic (72px+), ExtraBold (900). Color: Deep Navy (`#0F172A`) for maximum high-contrast impact.
- **Subheadline**: 22px, Medium (500), Color: `#6B7280` (Muted Slate). Max-width: 650px.
- **Background Effect**: A gradient transformation. The bottom of the section is slightly muted and cluttered, fading upwards into a pristine, glowing, clean digital space.

### 4. Elements & Interactions
- **Typography Block**: 
  - Headline: "Your Auction, Now at Light Speed."
  - Subheadline: "Leave the spreadsheets behind. Enter the new era of cricket auctions."
- **Action Buttons**:
  - *Primary*: "Start your auction for free" (Large, solid Vivid Blue or Coral button with a soft, glowing drop-shadow).
  - *Secondary*: "Watch the demo" (Ghost button with a subtle gray background on hover and a 'Play' icon).
- **Hero Visual (The Ascension)**: A breathtaking 3D composition showing the exact moment of digital transformation.
  - *The Base*: At the bottom of the screen, messy elements—torn pieces of paper, old calculators, and handwritten lists—are fading out.
  - *The Transformation*: As the eye moves upward, those papers magically morph into glowing, beautiful digital UI cards floating in mid-air.
  - *The Data*: The glowing digital cards feature the player "Zero - The Phenom" and a bidding war between "Azure Royals" and "Crimson Titans".
  - *Animation*: The UI cards gently float up and down, glowing with a soft neon aura, proving the digital way is vastly superior.

### 5. Screen Preview
```text
--------------------------------------------------------------------------------
                     Your Auction, Now at Light Speed.
                  
       Leave the spreadsheets behind. Enter the new era of cricket 
                                 auctions.

         [ START YOUR AUCTION FOR FREE ]   [ Watch the demo ]

                       .   *    ✦    *   .
                    [ GLOWING DIGITAL UI CARDS ]
                    | ZERO - THE PHENOM        |
                    | Azure Royals VS Crimson  |  * (Floating in mid-air
             ✦      | Titans                   |     with a soft neon aura)
                    '--------------------------'
                     ↑       ↑       ↑       ↑
             (Magical Transformation / Ascending particles)
                  _ __ ____ ___ _ _____
                 / /  / _  //_  \ / _  \  <-- (Torn papers, calculators,
                /_/__/__/__/__/__/____ /      messy handwritten lists at bottom)
--------------------------------------------------------------------------------
```

### 6. AI Generation Prompt
"A highly impactful, light and soft SaaS landing page hero section. Massive bold deep navy headline 'Your Auction, Now at Light Speed'. Below, a breathtaking 3D transformation visual: at the bottom, messy torn papers and old calculators are fading away and magically transforming as they rise upwards into glowing, beautiful frosted white glassmorphism UI cards floating in mid-air. The floating UI shows a futuristic cricket player card 'Zero - The Phenom'. Soft, elegant lighting, a gentle neon aura around the cards, clean aesthetic, highly dynamic and magical. Premium Dribbble UI design."

---

## 3. THE PAIN-CRUSHING BENTO GRID (FEATURE HIGHLIGHTS)

### 1. Component Goal
Eliminate the user's biggest pain points without showing ugly paper or "before and afters". Instead, use a centralized, premium, Apple-style Bento Grid of cards. Each card highlights a major headache and immediately shows the beautiful digital solution via micro-animations.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: CSS Grid. Max Content Width: 1280px, centered.
- **Grid Layout**: 
  - Top row: One wide card (spans 2 columns), one square card (1 column).
  - Bottom row: One square card (1 column), one wide card (spans 2 columns).
- **Gap**: `24px` between cards.

### 3. Elements & Interactions
- **Card 1 (Wide): Automated Purse Math**
  - Text: "Never touch a calculator again."
  - Visual: A sleek progress bar filling up automatically, perfectly calculating remaining budget.
- **Card 2 (Square): Instant Squad Exports**
  - Text: "Instant digital squads."
  - Visual: A beautiful PDF icon popping into existence showing generated teams.
- **Card 3 (Square): Dispute-Free Logs**
  - Text: "Perfect bid history."
  - Visual: A clean, scrolling live-log showing exactly who bid what.
- **Card 4 (Wide): TV Mode Sync**
  - Text: "Always perfectly synced."
  - Visual: A laptop and a TV screen glowing and updating simultaneously.
- **Styling**: Cards have frosted glass backgrounds (`rgba(255, 255, 255, 0.8)`), subtle white borders (`1px solid rgba(255,255,255,0.2)`), and a soft shadow. On hover, the cards lift slightly (`transform: translateY(-4px)`) and the micro-animation plays.

### 4. Screen Preview
```text
--------------------------------------------------------------------------------
         +------------------------------------+ +--------------------+
         |  Never touch a calculator again.   | |  Instant digital   |
         |                                    | |  squads.           |
         |    [=== 80% Purse Remaining ===]   | |                    |
         |    (Auto-calculating progress bar) | |   [ PDF Icon ]     |
         +------------------------------------+ +--------------------+
         
         +--------------------+ +------------------------------------+
         |  Perfect bid       | |  Always perfectly synced.          |
         |  history.          | |                                    |
         |                    | |       [ Laptop ] <--> [ TV ]       |
         |  > Alchemists: 2M  | |                                    |
         |  > Titans: 1.5M    | |       (Glowing sync animation)     |
         +--------------------+ +------------------------------------+
--------------------------------------------------------------------------------
```

---

## 4. THE LIVE LINK EXPERIENCE (REAL-TIME VIEWING)

### 1. Component Goal
Showcase the power of the "Live Link." Clarify that this isn't a heavy video stream, but a lightweight, real-time web URL that organizers can share with anyone to follow the auction data (current bids, player stats, sold status) instantly on any device.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: Flexbox (Row or 2-column Grid), centered. Light, airy theme (`#F9FAFB`).
- **Padding**: `100px` top and bottom.

### 3. Elements & Interactions
- **Typography Block** (Left side): 
  - Headline: "Share the thrill with a single link." 
  - Subtext: "No app downloads. No video streaming delays. Just send your unique Live Link to players, team owners, and fans. They can watch the bids update instantly from their phones, anywhere in the world."
  - *Interaction*: A visual URL bar (`yourwebsite.com/live/match-01`) with a "Copy Link" button beside it.
- **Visual Mockup** (Right side): An isometric composition showing a Laptop (the organizer controlling the auction) and a Mobile Phone (a fan watching from home). Both screens show the exact same "Live" player card perfectly synchronized.

### 4. Screen Preview
```text
--------------------------------------------------------------------------------
   Share the thrill with a 
   single link.                                   [ LAPTOP ]
                                              +-----------------+
   No app downloads. No video                 |  APEX PREDATOR  |
   streaming delays. Just send                |  Current: ₹8.5M |
   your unique Live Link to                   +-----------------+
   players and fans.                                   \
                                                        \  (Instant Sync)
   [ yoursite.com/live/surat-pl ] [ COPY ]               \
                                                    [ PHONE ]
                                                   +---------+
                                                   | APEX P. |
                                                   | ₹8.5M   |
                                                   +---------+
--------------------------------------------------------------------------------
```

---

## 5. OUR FEATURES (INTERACTIVE TABS)

### 1. Component Goal
Provide a comprehensive deep-dive into the platform's capabilities without overwhelming the user with a massive list. Use a modern, interactive tabbed interface (similar to Stripe or Linear) that feels incredibly high-end.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: Flexbox (Row), 2-column layout. Max Content Width: 1280px, centered.
- **Left Column (Navigation)**: `35%` width. Vertical list of feature tabs.
- **Right Column (Dynamic Visual)**: `65%` width. A large, sticky container displaying the UI associated with the active tab.

### 3. Elements & Interactions
- **Left Column Tabs**:
  - *Tab 1*: "Player Database & Import" (Active state: Dark text with a neon blue vertical indicator bar).
  - *Tab 2*: "Automated Team Finances" (Inactive state: Muted gray text).
  - *Tab 3*: "Live Broadcast Mode" (Inactive state: Muted gray text).
  - *Tab 4*: "Post-Auction PDF Exports" (Inactive state: Muted gray text).
- **Right Column Visuals**:
  - Displays a high-fidelity, floating glassmorphism UI card that perfectly illustrates the active tab.
  - *Animation*: When a user clicks a new tab on the left, the visual on the right smoothly cross-fades and slightly scales up (`transform: scale(1.02)`) into view.

### 4. Screen Preview
```text
--------------------------------------------------------------------------------
   EVERYTHING YOU NEED TO RUN A PRO AUCTION

   [|] Player Database         +---------------------------------------+
                               |                                       |
       Automated Finances      |     [ CSV UPLOAD WIDGET ]             |
                               |     ✓ 500 Players Imported            |
       Live Broadcast Mode     |     ✓ Base Prices Configured          |
                               |     ✓ Roles Assigned                  |
       Post-Auction Exports    |                                       |
                               +---------------------------------------+
--------------------------------------------------------------------------------
```

---

## 6. HOW IT WORKS (3-STEP SETUP)

### 1. Component Goal
Prove that the software is incredibly easy to learn and requires zero technical skill to set up.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: Horizontal timeline (Desktop) or Vertical stack (Mobile).
- **Elements**: 3 steps connected by a subtle dotted line.
  1. **Create Tournament**: Set your purse limit and rules.
  2. **Add Players**: Import your player list in seconds.
  3. **Start Bidding**: Connect to the big screen and go live.
- **Icons**: Large, custom illustrative icons in primary brand colors for each step.

---

## 7. FLEXIBLE PRICING (START FOR FREE)

### 1. Component Goal
Remove the risk of trying a new product. Emphasize that they can start for free, establishing a freemium model that converts curious visitors into actual users.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: 2 or 3 pricing cards centered.
- **Styling**: The "Free" or "Starter" tier should be welcoming. The "Pro" tier should stand out slightly (larger size, colored border).

### 3. Elements & Interactions
- **Free Tier (Highlighted)**: 
  - Headline: "Start your auction for free"
  - Price: ₹0
  - Features: Basic auction setup, limited players/teams.
  - CTA: "Start for Free"
- **Pro Tier**: 
  - Headline: "For Growing Tournaments"
  - Price: Reasonable flat fee per event.
  - Features: Unlimited players, TV Mode, PDF Exports.
  - CTA: "Upgrade to Pro"

---

## 8. INTERACTIVE SNEAK PEEK

### 1. Component Goal
Ignite curiosity by showing the software in action. An auto-playing high-quality GIF or interactive widget.

### 2. Elements
- **Visual**: A focused snippet of the UI showing a player being bought. E.g., a "SOLD" stamp slamming down on a player's card, or the bid amount rapidly ticking up. 
- **Text**: "Experience the thrill of the bid."

---

## 9. FAQ (OBJECTION HANDLING)

### 1. Component Goal
Address common doubts new users might have before committing to a new software platform.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: Max-width `800px`, centered.
- **Elements**: Accordion style list. 
- **Sample Questions**: "Is it really free to start?", "Do I need internet to run the auction?", "Can I project it on a TV?"

---

## 10. FINAL HIGH-IMPACT CTA

### 1. Component Goal
Capture users who have scrolled to the bottom. The last chance to convert.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: Full width, Deep Navy background. Large padding (`100px`+).
- **Elements**: 
  - Headline: "Ready to step into the digital era?"
  - Button: Large, high-contrast button (Cricket Green or Vibrant Blue) saying "Start your auction for free".

---

## 11. FOOTER

### 1. Component Goal
Secondary links and trust anchors.
- **Elements**: Brand Logo, Links (T&C, Privacy Policy, Contact), Copyright info. Simple 4-column grid.
