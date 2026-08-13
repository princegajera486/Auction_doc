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

## 2. HERO SECTION (THE HEARTBEAT)

### 1. Component Goal
The beating heart of the website. It must immediately make the user feel the intense adrenaline and drama of a high-stakes, broadcast-quality live auction.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: Flexbox (Column), `align-items: center`, `text-align: center`.
- **Dimensions**: Min-height: `90vh`, Width: 100%, `overflow: hidden`.
- **Padding**: `120px` top, `0px` bottom (image bleeds off the bottom).

### 3. Styling & Typography
- **Theme**: Light & Soft Mode. Background is a creamy, ultra-light gray (`#FAFAFA`) or pure white, featuring a very soft, diffuse radial glow in the center (like a gentle pastel coral or electric blue).
- **Headline**: Massive & cinematic (72px+), ExtraBold (900). Color: Deep Navy (`#0F172A`) for maximum high-contrast impact.
- **Subheadline**: 22px, Medium (500), Color: `#6B7280` (Muted Slate). Max-width: 650px.
- **Background Effect**: A sleek, elegant, animated ECG (heartbeat) line stretching across the background. Instead of aggressive red, it's a soft glowing coral (`#FF6B6B`) or vibrant cyan that spikes beautifully behind the mockup.

### 4. Elements & Interactions
- **Typography Block**: 
  - Headline: "Where Every Bid is a Heartbeat."
  - Subheadline: "Experience the adrenaline of a flawless, broadcast-quality auction. Silence the room and command the bidding war."
- **Action Buttons**:
  - *Primary*: "Start your auction for free" (Large, solid Vivid Blue or Coral button with a soft, glowing drop-shadow).
  - *Secondary*: "Watch the demo" (Ghost button with a subtle gray background on hover and a 'Play' icon).
- **Hero Image (The Climax)**: A stunning, high-quality 3D image of a live auction in progress.
  - *The Visual*: A dramatic 3D scene showing bids actively raising (e.g., floating numbers ticking upward, a high-tech auction podium, or dynamic bid indicators).
  - *Note*: An external, pre-rendered 3D image will be sourced and placed here to serve as the visual anchor.
  - *Animation*: The elegant heartbeat line in the background spikes sharply behind this 3D image.

### 5. Screen Preview
```text
--------------------------------------------------------------------------------
                         Where Every Bid 
                         is a Heartbeat.
                  
      Experience the adrenaline of a flawless, broadcast-quality 
           auction. Silence the room and command the bidding war.

         [ START YOUR AUCTION FOR FREE ]   [ Watch the demo ]

              -- soft glowing pastel coral heartbeat line --
           /^\       /^\       /^\       /^\       /^\       /^\
   _______/   \_____/   \_____/   \_____/   \_____/   \_____/   \_______

          +-------------------------------------------------------------+
          |                                                             |
          |                                                             |
          |         [ 3D AUCTION IMAGE: BIDS ACTIVELY RAISING ]         |
          |           (High-quality pre-rendered 3D asset)              |
          |                                                             |
          |                                                             |
          +-------------------------------------------------------------+
--------------------------------------------------------------------------------
```

### 6. AI Generation Prompt
"A highly impactful, light and soft SaaS landing page hero section. Massive bold deep navy headline 'Where Every Bid is a Heartbeat'. In the clean white background, a sleek, soft glowing pastel coral ECG heartbeat monitor line. In the center, a hyper-realistic, bright 3D frosted white glassmorphism mockup of a live auction bidding screen showing a countdown timer and intense bidding war between fictional epic teams. Soft, elegant lighting, clean aesthetic, but highly dynamic and thrilling. Premium Dribbble UI design."

---

## 3. THE PAIN POINT (THE OLD WAY VS. THE NEW WAY)

### 1. Component Goal
Connect with the organizer's pain points. Visually contrast the stress of manual auctions against the ease of using CrickBid.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: Flexbox (Row), 2 equally sized columns. `gap: 40px`.
- **Dimensions**: Max Content Width: 1280px.

### 3. Elements & Interactions
- **Left Column (The Old Way)**: 
  - Visual: A messy graphic of crossed-out paper, calculators, and tangled spreadsheets. Muted, dull colors.
  - Text: "Stressful calculations, disputed bids, and messy team squads."
- **Right Column (The New Way)**: 
  - Visual: Your clean, automated, beautiful software interface. Bright, vibrant colors.
  - Text: "Automated purse math, instant Live Links, and beautiful digital squads."

### 4. Screen Preview
```text
--------------------------------------------------------------------------------
                     [ THE OLD WAY ]                [ THE NEW WAY ]

                  (Muted, Messy Graphics)       (Vibrant, Clean Graphics)
                 +-----------------------+     +-----------------------+
                 | \  | /                |     |                       |
                 | - PAPER & PENS -      |     |  [ CRICKBID UI ]      |
                 | /  | \                |     |  ✓ Auto-Purse Math    |
                 |  CALCULATOR ERRORS    |     |  ✓ Live Link          |
                 |  MESSY SQUADS         |     |  ✓ Digital Squads     |
                 +-----------------------+     +-----------------------+

                   "Stressful math &            "Automated, instant,
                   disputed bids."              and beautiful."
--------------------------------------------------------------------------------
```

---

## 4. PROFESSIONAL TV PRESENTATION (THE WOW FACTOR)

### 1. Component Goal
Demonstrate how the software elevates the status of the tournament by providing a premium, broadcast-quality experience for the audience and team owners in the room.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: Flexbox (Column), centered. Dark Mode theme.
- **Background**: Deep rich dark color (e.g., `#0B0F19`) to simulate a dark auction room.
- **Padding**: `100px` top and bottom.

### 3. Elements & Interactions
- **Visual Mockup**: A large, edge-to-edge image of a TV or projector screen displaying the "Live Auction Mode". 
- **Typography**: White text. 
  - Headline: "Give them the IPL experience." 
  - Subtext: "Project your auction onto the big screen. Complete with player stats, live bid tracking, and dramatic 'SOLD' animations."
- **Effects**: Add a soft glow behind the TV mockup to make the screen "pop" off the dark background.

---

## 5. FEATURE SHOWCASE (BENTO BOX UI)

### 1. Component Goal
Highlight the core capabilities that save the organizer time, presented in a highly scannable, modern "Bento Box" grid layout.

### 2. Layout & Structure (Figma Auto Layout Specs)
- **Container**: CSS Grid (or Figma Auto Layout wrapping), typically 3-4 distinct cards of varying sizes.
- **Gap**: `24px`.

### 3. Elements
- **Card 1 (Large)**: "Auto-Purse Calculation" - visual of a budget bar draining.
- **Card 2 (Medium)**: "Real-Time Sync" - icons of a laptop and phone connected.
- **Card 3 (Medium)**: "Instant Squad Exports" - visual of a PDF icon with team logos.
- **Styling**: Cards have very light gray backgrounds (`#F8FAFC`), 16px border-radius, and a soft hover-lift effect.

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
