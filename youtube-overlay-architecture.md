# YouTube Broadcast Overlay Architecture

## 1. Overview
The Live Broadcast Overlay is a specialized, read-only web view designed exclusively for integration into live streaming software (like OBS Studio or vMix). It allows organizers to stream their cricket auctions to YouTube with professional, real-time, television-grade lower-third graphics without needing expensive hardware or dedicated graphics teams.

## 2. Technical Stack & Development Process
The overlay is not a static video file; it is built entirely using standard web technologies:
- **Design**: Figma (for creating the static UI/UX mockups).
- **Structure & Styling**: HTML and CSS. The layout uses CSS absolute positioning to anchor elements to the bottom of the screen (commonly known as a "Lower Third").
- **Transparency**: The `<body>` of the page uses `background-color: transparent;` ensuring the HTML background is invisible, allowing the camera feed to pass through in the broadcasting software.
- **Interactivity**: React or Vanilla JavaScript handles the dynamic text injection and CSS animations (like number counters or flashing colors).
- **Real-Time Communication**: WebSockets (e.g., Socket.io) are used to push instant updates from the backend.

## 3. The Real-Time Data Pipeline (WebSockets)
Here is how the data flows from the organizer's laptop to the YouTube audience in milliseconds:
1. **Initial Load**: When the overlay link is opened, an API call fetches the current state of the live auction (active player, base value, current bid).
2. **WebSocket Connection**: The JavaScript on the overlay establishes a continuous, two-way connection tunnel with the backend server.
3. **Organizer Action**: The organizer clicks a button (e.g., "Raise Bid to ₹ 9.00L") on their Manage Auction Dashboard.
4. **Server Broadcast**: The backend saves the new bid to the database and instantly emits a `NEW_BID` WebSocket event.
5. **Overlay Update**: The overlay's JavaScript receives the event instantly and updates the specific HTML text elements on the screen without ever reloading the webpage.

## 4. Broadcasting Integration (OBS Studio Workflow)
How the organizer actually uses the overlay during a live stream:
1. The platform generates a unique, secure overlay URL for the tournament (e.g., `cricketauction.com/overlay/{auction_id}`).
2. The organizer opens their broadcasting software (e.g., **OBS Studio**).
3. They add a new **"Browser Source"** to their scene and paste the URL.
4. OBS renders the HTML/CSS graphics over their camera feed.
5. OBS encodes the final composed video and sends it to YouTube Live via RTMP.

## 5. Visual Component Breakdown
Based on the required graphic design, the layout consists of the following dynamic elements anchored to the bottom of the screen:

### 5.1 Current Bid Box (Left)
- **Header**: Text reading "CURRENT BID" (Yellow accent).
- **Value**: Large typography displaying the highest bid amount (e.g., `1.00.000`). 
- **Animation**: This element will trigger a CSS animation (e.g., a green flash or a scale pop) every time a new bid is received via WebSockets to create visual excitement.

### 5.2 Player Profile Card (Center)
- **Style**: Slanted edges using CSS `transform: skewX()`.
- **Photo**: A circular, masked photo of the active player currently on the block.
- **Name**: The full name of the active player (e.g., "GAJERA ASHISH GOVINDBHAI").
- **Base Value**: The starting price of the player, displayed in a pill badge (e.g., `BASE VALUE 🪙 100000`).

### 5.3 Team Leaderboard (Right)
- **Columns**: `TEAM`, `TEAM BAL.`, and `MAX BID`.
- **Rows**: Displays dynamic data for the top 2-3 teams currently engaged in the auction. It shows their remaining purse and maximum bid capacity to build tension for the viewers.
- **Progress Bars**: Visual CSS progress bars showing how much of their total budget they have spent.

### 5.4 Information Ticker (Bottom Full-Width)
- A continuous, scrolling CSS-animated ticker bar running across the absolute bottom of the screen.
- Used to display sponsor text, contact numbers, tournament news, or upcoming players.
