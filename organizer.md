# Screen 1: Organizer Side — Login Screen

## 1. Overview

The Organizer Login Screen is the secure entry point for tournament organizers/auction administrators.

The screen allows an existing organizer to access the Cricket Auction Management System using:

- Email ID
- Password
- Google Login

The login screen should be simple, professional, and focused on quick authentication.

After successful authentication, the organizer should be redirected to the Organizer Dashboard.

---

## 2. Screen Preview

Create a clean, premium SaaS-style login screen.

### Desktop Layout

Use a centered authentication card.

```text
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│                    [ AUCTION LOGO ]                         │
│                                                             │
│                Welcome Back, Organizer                     │
│        Login to manage your cricket auctions               │
│                                                             │
│  Email Address                                               │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Enter your email address                              │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  Password                                                    │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Enter your password                              👁   │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│                         Forgot Password?                     │
│                                                             │
│  ┌───────────────────────────────────────────────────────┐  │
│  │                     LOGIN                              │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│                         ─── OR ───                           │
│                                                             │
│  ┌───────────────────────────────────────────────────────┐  │
│  │  [Google Icon]       Continue with Google             │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│             Don't have an account? Register                 │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## 3. Form Fields

| Field Name | Type | Description | Mandatory |
| :--- | :--- | :--- | :--- |
| Email Address | Email | Organizer's registered email address | Yes |
| Password | Password | Organizer's account password | Yes |
| Google Login | Button | Initiates OAuth2 Google login flow | No |

## 4. Validations

- **Email Address**:
  - Must not be empty.
  - Must be a valid email format (e.g., `organizer@example.com`).
- **Password**:
  - Must not be empty.

## 5. Business Rules

- **Authentication**: The system must verify the provided email and password against the Organizer database.
- **Google Login**: If "Continue with Google" is used, the system should authenticate via OAuth2 and map the Google email to an existing organizer account. If no account exists, display an error or redirect to registration.
- **Forgot Password**: Clicking "Forgot Password?" should redirect the user to the password recovery flow.
- **Registration**: Clicking "Register" should redirect the user to the Organizer Registration screen.
- **Successful Login**: On successful authentication, create a secure session/token and redirect the organizer to the Organizer Dashboard.
- **Failed Login**: On invalid credentials or authentication failure, show a clear error message (e.g., "Invalid email or password").

---

# Screen 2: Organizer Side — Registration Screen

## 1. Overview

The Organizer Registration Screen allows new tournament organizers/auction administrators to create an account in the Cricket Auction Management System.

This screen captures essential details required to set up an organizer profile, ensuring that only verified individuals can host and manage auctions.

---

## 2. Screen Preview

Create a clean, scrollable authentication card for registration.

### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│                    [ AUCTION LOGO ]                         │
│                                                             │
│                Create an Organizer Account                 │
│          Join us to manage your cricket auctions           │
│                                                             │
│  ┌───────────────────────────────────────────────────────┐  │
│  │                    ( Upload Photo )                   │  │
│  │                     [ Camera Icon ]                   │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  Full Name                                                   │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Enter your full name                                  │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  Email Address                                               │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Enter your email address                              │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  Phone Number                                                │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Enter your phone number                               │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  City                                                        │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Enter your city                                       │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  Password                                                    │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Create a password                                👁   │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  Confirm Password                                            │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Confirm your password                            👁   │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  ┌───────────────────────────────────────────────────────┐  │
│  │                     SIGN UP                            │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│             Already have an account? Login                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## 3. Form Fields

| Field Name | Type | Description | Mandatory |
| :--- | :--- | :--- | :--- |
| Profile Photo | Image/File | Organizer's profile picture | No |
| Name | Text | Full name of the organizer | Yes |
| Email Address | Email | Organizer's email address | Yes |
| Phone Number | Phone/Text | Contact number of the organizer | Yes |
| City | Text | City of residence/operation | Yes |
| Password | Password | Secure password for the account | Yes |
| Confirm Password | Password | Confirmation of the password | Yes |

## 4. Validations

- **Profile Photo**:
  - Must be a valid image format (e.g., JPG, PNG).
  - Size should not exceed a specific limit (e.g., 5MB).
- **Name**:
  - Must not be empty.
  - Must contain only letters and spaces.
- **Email Address**:
  - Must not be empty.
  - Must be a valid email format (e.g., `organizer@example.com`).
  - Must be unique (not already registered).
- **Phone Number**:
  - Must not be empty.
  - Must be a valid format (e.g., 10 digits).
  - Must be unique (not already registered).
- **City**:
  - Must not be empty.
- **Password**:
  - Must be at least 8 characters long.
  - Should include a mix of uppercase, lowercase, numbers, and special characters.
- **Confirm Password**:
  - Must exactly match the Password field.

## 5. Business Rules

- **Account Creation**: Upon successful submission, a new Organizer account is created in the database.
- **Data Uniqueness**: The system must check if the Email Address or Phone Number is already registered. If so, display an error ("Email/Phone already in use").
- **Redirection**:
  - Clicking "Login" redirects the user to the Organizer Login screen.
  - On successful registration, redirect to the Organizer Login screen with a success message, or directly log them in and redirect to the Organizer Dashboard.
- **Email Verification (Optional)**: An OTP or verification link may be sent to the registered email address to verify the account before granting full access.

---

# Screen 3: Organizer Side — Profile Setup (Google Login)

## 1. Overview

The Profile Setup Screen is displayed when an organizer logs into the system for the first time using their Google account.

Since Google authentication only provides the user's name and email address, this screen is required to capture the remaining mandatory details (Phone Number, City, and an optional Profile Picture) to complete the organizer's profile before granting access to the dashboard.

---

## 2. Screen Preview

Create a clean, continuous onboarding card layout.

### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│                    [ AUCTION LOGO ]                         │
│                                                             │
│                 Complete Your Profile                      │
│        Just a few more details to set up your account      │
│                                                             │
│  ┌───────────────────────────────────────────────────────┐  │
│  │                    ( Upload Photo )                   │  │
│  │                     [ Camera Icon ]                   │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  Full Name (Pre-filled)                                      │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ John Doe                                       [ ✓ ]  │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  Email Address (Pre-filled)                                  │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ john.doe@example.com                           [ ✓ ]  │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  Phone Number                                                │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Enter your phone number                               │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  City                                                        │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Enter your city                                       │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
│  ┌───────────────────────────────────────────────────────┐  │
│  │                   COMPLETE PROFILE                     │  │
│  └───────────────────────────────────────────────────────┘  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## 3. Form Fields

| Field Name | Type | Description | Mandatory | Pre-filled |
| :--- | :--- | :--- | :--- | :--- |
| Profile Photo | Image/File | Organizer's profile picture | No | Optional (from Google) |
| Name | Text | Full name of the organizer | Yes | Yes (Read-only) |
| Email Address | Email | Organizer's email address | Yes | Yes (Read-only) |
| Phone Number | Phone/Text | Contact number of the organizer | Yes | No |
| City | Text | City of residence/operation | Yes | No |

## 4. Validations

- **Profile Photo**:
  - Must be a valid image format (e.g., JPG, PNG).
  - Size should not exceed a specific limit (e.g., 5MB).
- **Phone Number**:
  - Must not be empty.
  - Must be a valid format (e.g., 10 digits).
  - Must be unique (not already registered).
- **City**:
  - Must not be empty.

## 5. Business Rules

- **Data Fetching**: The Name and Email fields are pre-filled automatically using the data received from the Google OAuth2 provider and should be marked as read-only.
- **Profile Completion**: The user cannot access the Organizer Dashboard until this form is successfully submitted.
- **Data Uniqueness**: The system must ensure the entered Phone Number is not already linked to another Organizer account.
- **Successful Submission**: Once the form is submitted, the Organizer's profile is marked as complete, a secure session is established, and the user is redirected to the Organizer Dashboard.
- **Cancellation**: If the user drops off or closes the browser at this screen, their account remains in an "incomplete" state and they will be prompted with this screen on their next Google login attempt.

---

# Screen 4: Organizer Side — Top Navbar

## 1. Overview

The Top Navbar is a persistent global navigation component visible across all Organizer authenticated screens (e.g., Dashboard, Auction management pages).

It provides quick access to core features of the platform, a global search functionality, and the organizer's profile settings, ensuring seamless navigation without losing context.

---

## 2. Screen Preview

Create a clean, horizontal navigation bar spanning the full width of the screen.

### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│                                                                                             │
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
│                                                                                             │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

## 3. Elements Table

| Element Name | Type | Description | Visibility |
| :--- | :--- | :--- | :--- |
| Logo | Image/Link | Platform logo acting as a home button | Always visible |
| Dashboard | Navigation Link | Directs the organizer to the main overview dashboard | Always visible |
| Auctions | Navigation Link | Directs the organizer to the auctions management list | Always visible |
| Search | Input Field | Global search bar for finding auctions, players, or teams | Always visible |
| Profile | Dropdown Menu | Organizer's profile avatar/menu (Settings, Logout) | Always visible |

## 4. Validations

- **Search Input**:
  - Should accept alphanumeric characters.
  - Triggers search automatically upon typing (debounce) or on pressing Enter.
- **Active State**:
  - The navigation link for the currently viewed page (e.g., Dashboard or Auctions) must be visually highlighted (active state).

## 5. Business Rules

- **Routing**:
  - Clicking the **Logo** redirects to the Dashboard.
  - Clicking **Dashboard** redirects to the Dashboard page.
  - Clicking **Auctions** redirects to the Auctions management page.
- **Search Execution**: Entering a query in the Search bar searches across the organizer's active, upcoming, and past auctions, as well as registered players.
- **Profile Dropdown**:
  - Clicking the Profile element opens a dropdown menu containing options such as:
    - Edit Profile
    - Settings
    - Logout
- **Logout Action**: Selecting "Logout" from the Profile dropdown ends the active session, clears authentication tokens, and redirects the user to the Organizer Login Screen.
- **Sticky Behavior**: The navbar should remain sticky/fixed at the top of the viewport when scrolling down long pages for easy access.

---

# Screen 5: Organizer Side — Dashboard

## 1. Overview

The Organizer Dashboard is the central command center for the tournament organizer. 

It provides a high-level summary of their auction activities, quick access to create new events, and highlights ongoing or upcoming auctions. The dashboard is designed to deliver immediate value through insightful metrics and quick actions.

---

## 2. Screen Preview

Create a spacious, widget-based dashboard layout.

### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  Welcome back, Organizer! 👋                                    [ + CREATE AUCTION ]      │
│  Here is what's happening with your tournaments today.                                      │
│                                                                                             │
│  📊 INSIGHTS                                                                                │
│  ┌───────────────┐ ┌───────────────┐ ┌───────────────┐ ┌───────────────┐                    │
│  │ Total Auctions│ │ Total Players │ │ Total Teams   │ │ Total Spent   │                    │
│  │      12       │ │     450       │ │      24       │ │   $1.2M       │                    │
│  └───────────────┘ └───────────────┘ └───────────────┘ └───────────────┘                    │
│                                                                                             │
│  🔥 LIVE & UPCOMING AUCTIONS                                                                │
│  [ < ] ─── ┌───────────────────────┐ ┌───────────────────────┐ ─── [ > ]                    │
│            │ 🔴 LIVE               │ │ ⏳ Starts in 2h       │                              │
│            │ Premier League 2026   │ │ Super Cup T20         │                              │
│            │ Teams: 8 | Players: 12│ │ Teams: 6 | Players: 90│                              │
│            │ [ Go to Auction ]     │ │ [ View Details ]      │                              │
│            └───────────────────────┘ └───────────────────────┘                              │
│                                                                                             │
│  📈 RECENT ACTIVITY                                                                         │
│  - Player 'Virat K.' sold to 'Mumbai Indians' for $100,000.                                 │
│  - New team 'Chennai Super Kings' registered for Premier League 2026.                       │
│                                                                                             │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

## 3. Elements Table

| Element Name | Type | Description | Visibility |
| :--- | :--- | :--- | :--- |
| Create Auction | Primary Button | Button to initiate the flow for creating a new auction | Always visible |
| Insights Widgets | Information Cards | Key metrics (Total Auctions, Players, Teams, Spent) | Always visible |
| Live/Upcoming Carousel | Card Slider | Rotating cards displaying currently live or soon-to-start auctions | Visible if auctions exist |
| Carousel Controls | Buttons | Left/Right arrows to scroll through the auction cards | Visible if > 2 auctions |
| Recent Activity | List/Feed | A chronological feed of recent events across all managed auctions | Always visible |

## 4. Validations

- **Create Auction Button**:
  - Should be prominent (primary color) to attract attention.
- **Insights Data**:
  - Must display `0` instead of breaking if no data is available.
  - Currency values (e.g., Total Spent) should be formatted based on the user's locale/preferences.
- **Carousel Rules**:
  - Auto-rotate every 5 seconds.
  - Pause rotation when the user hovers over an auction card.

## 5. Business Rules

- **Create Auction Routing**: Clicking the "+ CREATE AUCTION" button redirects the user to the multi-step "Create Auction" wizard.
- **Insights Calculation**:
  - Metrics are calculated only from auctions owned/managed by the currently logged-in organizer.
- **Live/Upcoming Logic**:
  - Auctions with a status of "Live" appear first in the carousel, followed by "Upcoming" (sorted by nearest start time).
  - Past or completed auctions should not appear in this specific carousel.
- **Card Actions**:
  - Clicking "Go to Auction" on a Live card redirects directly to the Live Auction Dashboard.
  - Clicking "View Details" on an Upcoming card redirects to that auction's setup/details page.
- **Recent Activity**: The feed pulls logs from the organizer's active tournaments (e.g., player sold, team registered) and displays the most recent 5-10 entries.

---

# Screen 6: Organizer Side — Create Auction

## 1. Overview

The Create Auction Screen allows an organizer to configure and launch a new cricket auction tournament.

This form captures all essential rules and metadata required to set up the bidding environment, including team budgets, bid increments, schedule, and visibility settings.

---

## 2. Screen Preview

Create a clean, scrollable form layout with logically grouped sections.

### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  ← Back to Dashboard                                                                        │
│                                                                                             │
│  Create New Auction                                                                         │
│  Fill out the details below to set up your tournament.                                      │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────┐                                  │
│  │                    ( Upload Logo )                    │                                  │
│  │                    [ Camera Icon ]                    │                                  │
│  └───────────────────────────────────────────────────────┘                                  │
│                                                                                             │
│  Auction Name                                   Venue                                       │
│  ┌─────────────────────────────┐                ┌─────────────────────────────┐             │
│  │ e.g., Premier League 2026   │                │ e.g., City Stadium          │             │
│  └─────────────────────────────┘                └─────────────────────────────┘             │
│                                                                                             │
│  Auction Date                                   Auction Time                                │
│  ┌─────────────────────────────┐                ┌─────────────────────────────┐             │
│  │ DD/MM/YYYY           [📅]   │                │ HH:MM AM/PM          [🕒]   │             │
│  └─────────────────────────────┘                └─────────────────────────────┘             │
│                                                                                             │
│  Balance Per Team                               Players Per Team                            │
│  ┌─────────────────────────────┐                ┌─────────────────────────────┐             │
│  │ e.g., 100,000               │                │ e.g., 15                    │             │
│  └─────────────────────────────┘                └─────────────────────────────┘             │
│                                                                                             │
│  Minimum Bid                                    Bid Increase By                             │
│  ┌─────────────────────────────┐                ┌─────────────────────────────┐             │
│  │ e.g., 500                   │                │ e.g., 100                   │             │
│  └─────────────────────────────┘                └─────────────────────────────┘             │
│                                                                                             │
│  Auction Visibility                                                                         │
│  ( ) Public (Visible to everyone)                                                           │
│  ( ) Private (Invite only)                                                                  │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────┐                                  │
│  │                   CREATE AUCTION                       │                                  │
│  └───────────────────────────────────────────────────────┘                                  │
│                                                                                             │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

## 3. Fields Table

| Field Name | Type | Description | Mandatory |
| :--- | :--- | :--- | :--- |
| Auction ID | Hidden (Auto) | Unique system-generated ID for backend tracking | Yes (Backend) |
| Tournament Logo | Image/File | Logo for the tournament/auction | No |
| Auction Name | Text | Name of the tournament or auction event | Yes |
| Venue | Text | Location where the auction/tournament is held | Yes |
| Auction Date | Date Picker | Scheduled date for the live auction | Yes |
| Auction Time | Time Picker | Scheduled start time for the live auction | Yes |
| Balance Per Team | Number | Total virtual money allocated to each team | Yes |
| Players Per Team | Number | Maximum number of players a team can buy | Yes |
| Minimum Bid | Number | Default starting base price for a player | Yes |
| Bid Increase By | Number | Default incremental value for each new bid | Yes |
| Auction Visibility | Radio Button | Sets if the auction is 'Public' or 'Private' | Yes |

## 4. Validations

- **Date and Time**: 
  - Auction Date must be today or a future date.
  - If Auction Date is today, Auction Time must be in the future.
- **Numeric Fields (Balance, Min Bid, Bid Increase, Players)**:
  - Must be greater than 0.
  - Must not contain alphabets or special characters.
- **Tournament Logo**:
  - Valid image formats only (JPG, PNG, WebP).
  - Max file size (e.g., 5MB).
- **Auction Visibility**:
  - A selection must be made (default can be 'Public').

## 5. Business Rules

- **Auction ID Generation**: Upon successful submission, the backend automatically generates a unique UUID or sequential ID for the `Auction ID` field (hidden from UI).
- **Visibility Logic**:
  - **Public**: The auction will be listed in global search results and accessible via a public URL.
  - **Private**: The auction is hidden from global search and can only be accessed via a specific invite link or by manually adding teams/users.
- **Financial Rules**: The backend must enforce that `Minimum Bid` is less than or equal to `Balance Per Team`.
- **Post-Creation Routing**: Once the auction is created successfully:
  - Display a success toast/notification.
  - Redirect the organizer to the **Auction Details / Setup Dashboard** for this specific auction, where they can begin adding Teams and Players.

---

# Screen 7: Organizer Side — Manage Auction

## 1. Overview

The Manage Auction screen serves as the detailed control center for a specific auction event. 

It provides organizers with a comprehensive header containing key auction details, quick actions to start or view the auction, and a multi-tabbed interface to manage various entities associated with the event (Teams, Players, Sponsors, etc.).

---

## 2. Screen Preview

Create a detail-rich header with a sticky tabbed navigation below it.

### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  ← Back to Auctions                                                                         │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                                                                                       │  │
│  │   ( LOGO )    Auction Name: Premier League 2026          [ START AUCTION ]            │  │
│  │               Auction Code: PL-2026-X8F                  [ VIEW AUCTION ]             │  │
│  │               Date & Time: 15 Oct 2026, 10:00 AM                                      │  │
│  │               Players Per Team: 15                                                    │  │
│  │                                                                                       │  │
│  │   Plan: Free          Live Link: [ Copy Link ]                                        │  │
│  │   Views: 1.2K         [ Upgrade Now ]                                                 │  │
│  │                                                                                       │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
│                                                                                             │
│  [ Teams ]  [ Players ]  [ MVP ]  [ Sponsors ]  [ Link ]  [ About ]                         │
│  ────────────────────────────────────────────────────────────────────────────────────────── │
│                                                                                             │
│   ( Tab Content Area - specific to the selected tab, e.g., list of teams )                  │
│                                                                                             │
│                                                                                             │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

## 3. Fields Table

| Element Name | Type | Description | Visibility |
| :--- | :--- | :--- | :--- |
| Logo | Image | The uploaded logo for this specific tournament | Always visible |
| Auction Name | Text (Display) | Name of the auction | Always visible |
| Auction Code | Text (Display) | Unique identifier/code to join the auction | Always visible |
| Date & Time | Text (Display) | Scheduled start date and time | Always visible |
| Players Per Team | Text (Display) | Max allowed players per team | Always visible |
| Plan & Views | Text (Display) | Current subscription plan and public views count | Always visible |
| Start Auction | Primary Button | Triggers the live auction bidding screen | Always visible |
| View Auction | Secondary Button | Previews the public-facing view of the auction | Always visible |
| Live Link / Copy | Action Link | Copies the public URL to share with participants | Always visible |
| Upgrade Now | Action Link | Prompt to upgrade the current plan (if applicable) | Visible if on lower plan |
| Navigation Tabs | Tabs | Switches between internal management sections | Always visible |

## 4. Validations

- **Start Auction Button**:
  - Should be disabled (or show a warning) if there are no teams or players added yet.
  - Optionally, only enable if the current time is close to the `Date & Time` scheduled.
- **Tabs**:
  - The currently active tab must be visually distinct (e.g., underlined or highlighted).
- **Live Link**:
  - Must copy a valid, functioning URL to the user's clipboard upon clicking.

## 5. Business Rules

- **Header Data Fetching**: The data in the header is read-only on this screen and must be fetched directly from the Auction's configuration data.
- **Tab Routing/State**:
  - **Teams**: Manage (add/edit/delete) the franchise teams participating.
  - **Players**: Manage the player pool, categorize them, and set base prices.
  - **MVP**: Manage Most Valuable Player leaderboards or awards configurations.
  - **Sponsors**: Add sponsor logos and details to display during the live auction.
  - **Link**: Manage specific deep-links, invite codes, or sharing options.
  - **About**: View or edit the description, rules, and venue details of the auction.
- **Action 'Start Auction'**: 
  - Clicking this initiates the WebSockets/Live Sync session. It changes the auction status to "Live" and routes the organizer to the Live Bidding Dashboard.
- **Action 'View Auction'**:
  - Opens a new browser tab showing the public view of the auction as a guest/spectator would see it.
- **Upgrade Flow**: Clicking "Upgrade Now" redirects the organizer to the billing/subscription management page.

---

## 7.1 Internal Section — Teams

This section contains all the views and functionalities related to managing franchise teams within the auction.

### Screen 7.1.1: Team List Table

#### 1. Overview

The Team List Table is the default view when the organizer clicks on the "Teams" tab in the Manage Auction screen.

It provides a tabular overview of all franchise teams registered for the current auction, displaying their essential details (like logo, name, and remaining balance), and providing quick action buttons to view, edit, or delete a team.

---

#### 2. Screen Preview

A clean data table displaying the team records with an "Add Team" button on the top right.

##### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  ← Back to Auctions                                                                         │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                                                                                       │  │
│  │   ( LOGO )    Auction Name: Premier League 2026          [ START AUCTION ]            │  │
│  │               Auction Code: PL-2026-X8F                  [ VIEW AUCTION ]             │  │
│  │               Date & Time: 15 Oct 2026, 10:00 AM                                      │  │
│  │               Players Per Team: 15                                                    │  │
│  │                                                                                       │  │
│  │   Plan: Free          Live Link: [ Copy Link ]                                        │  │
│  │   Views: 1.2K         [ Upgrade Now ]                                                 │  │
│  │                                                                                       │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
│                                                                                             │
│  [ ━━ Teams ━━ ]  [ Players ]  [ MVP ]  [ Sponsors ]  [ Link ]  [ About ]                   │
│  ────────────────────────────────────────────────────────────────────────────────────────── │
│                                                                                             │
│     Teams (8)                                        [ + ADD TEAM ]                         │
│                                                                                             │
│     ┌────┬────────────────────────┬─────────────┬─────────────┬─────────┐                   │
│     │ No │ Team Logo & Name       │ Short Name  │ Balance     │ Actions │                   │
│     ├────┼────────────────────────┼─────────────┼─────────────┼─────────┤                   │
│     │ 1  │ (LOGO) Mumbai Indians  │ MI          │ $ 100,000   │ 👁 ✏️ 🗑️ │                   │
│     ├────┼────────────────────────┼─────────────┼─────────────┼─────────┤                   │
│     │ 2  │ (LOGO) Chennai S.K.    │ CSK         │ $ 95,000    │ 👁 ✏️ 🗑️ │                   │
│     ├────┼────────────────────────┼─────────────┼─────────────┼─────────┤                   │
│     │ 3  │ (LOGO) Royal C.B.      │ RCB         │ $ 100,000   │ 👁 ✏️ 🗑️ │                   │
│     └────┴────────────────────────┴─────────────┴─────────────┴─────────┘                   │
│                                                                                             │
│     Showing 1 to 3 of 8 Teams                                                               │
│                                                                                             │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Column Name | Type | Description | Visibility |
| :--- | :--- | :--- | :--- |
| No | Number | Sequential serial number for the list | Always visible |
| Team Logo & Name | Text + Image | The franchise logo followed by the full team name | Always visible |
| Short Name | Text | The abbreviation of the team (e.g., MI, CSK) | Always visible |
| Balance | Currency | The current remaining purse/balance for the team | Always visible |
| Actions | Buttons/Icons | Quick actions: View (Eye), Edit (Pencil), Delete (Trash) | Always visible |

#### 4. Validations

- **Empty State**: 
  - If no teams are added yet, the table should be hidden and replaced with an "Empty State" graphic and a prompt to "Add your first team".
- **Delete Confirmation**:
  - Clicking the Delete (Trash) icon must trigger a confirmation modal (e.g., "Are you sure you want to delete this team?").

#### 5. Business Rules

- **Default Balance**: When a team is newly added and no players have been bought, their `Balance` must exactly match the `Balance Per Team` defined in the Auction settings.
- **Routing**:
  - Clicking **Add Team** opens the "Add Team" form or modal.
  - Clicking **View (👁)** redirects to a detailed Team Profile page, showing their bought players and statistics.
  - Clicking **Edit (✏️)** opens an "Edit Team" form pre-filled with the team's current data.
  - Clicking **Delete (🗑️)** removes the team from the auction. A team cannot be deleted if the auction is currently "Live" or if they have already purchased players.

---

### Screen 7.1.2: Add Team (Modal)

#### 1. Overview

The Add Team Modal is a quick-entry popup form that allows the organizer to register a new franchise team for the auction.

Because there are only three essential details required to create a team, a modal keeps the user in context on the Manage Auction page rather than redirecting them to a separate screen.

---

#### 2. Screen Preview

The modal appears centered over a darkened, blurred background of the Team List Table.

##### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                         │
│  [Darkened Background / Overlay of the Team List Table]                 │
│                                                                         │
│      ┌───────────────────────────────────────────────────────────┐      │
│      │                                                           │      │
│      │   Add New Team                                      [ X ] │      │
│      │   ─────────────────────────────────────────────────────   │      │
│      │                                                           │      │
│      │   ┌───────────────────────────────────────────────────┐   │      │
│      │   │                  ( Upload Logo )                  │   │      │
│      │   │                  [ Camera Icon ]                  │   │      │
│      │   └───────────────────────────────────────────────────┘   │      │
│      │                                                           │      │
│      │   Team Name                                               │      │
│      │   ┌───────────────────────────────────────────────────┐   │      │
│      │   │ e.g., Mumbai Indians                              │   │      │
│      │   └───────────────────────────────────────────────────┘   │      │
│      │                                                           │      │
│      │   Short Name                                              │      │
│      │   ┌───────────────────────────────────────────────────┐   │      │
│      │   │ e.g., MI                                          │   │      │
│      │   └───────────────────────────────────────────────────┘   │      │
│      │                                                           │      │
│      │                                                           │      │
│      │   [ Cancel ]                             [ ADD TEAM ]     │      │
│      │                                                           │      │
│      └───────────────────────────────────────────────────────────┘      │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Field Name | Type | Description | Mandatory |
| :--- | :--- | :--- | :--- |
| Logo | Image/File | The franchise's official logo or emblem | No (can use placeholder) |
| Team Name | Text | The full name of the franchise | Yes |
| Short Name | Text | The abbreviation or acronym of the team name | Yes |

#### 4. Validations

- **Team Name**:
  - Must not be empty.
  - Must be unique within this specific auction (cannot have two teams with the exact same name).
- **Short Name**:
  - Must not be empty.
  - Should ideally be restricted to 2-4 uppercase characters (e.g., MI, RCB).
  - Must be unique within this specific auction.
- **Logo**:
  - Valid image formats only (JPG, PNG, WebP).
  - Max file size (e.g., 2MB).

#### 5. Business Rules

- **Default State**: When the modal opens, all fields are empty.
- **Save Action**: Clicking `[ ADD TEAM ]` validates the inputs, creates the team in the database, attaches it to the current Auction ID, and assigns the team an initial `Balance` equal to the auction's `Balance Per Team`.
- **UI Update**: Upon successful save, the modal closes automatically, a success toast appears, and the Team List Table (Screen 7.1.1) refreshes to display the newly added team.
- **Cancel Action**: Clicking `[ Cancel ]` or the `[ X ]` icon closes the modal without saving and discards any entered data.

---

### Screen 7.1.3: Edit Team (Modal)

#### 1. Overview

The Edit Team Modal is triggered when the organizer clicks the Edit (✏️) icon on a specific team in the Team List Table.

It shares the exact same layout as the Add Team Modal, but the fields are pre-filled with the team's existing data, allowing the organizer to quickly update the team name, short name, or logo.

---

#### 2. Screen Preview

The modal appears centered over a darkened background, showing pre-filled data.

##### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                         │
│  [Darkened Background / Overlay of the Team List Table]                 │
│                                                                         │
│      ┌───────────────────────────────────────────────────────────┐      │
│      │                                                           │      │
│      │   Edit Team                                         [ X ] │      │
│      │   ─────────────────────────────────────────────────────   │      │
│      │                                                           │      │
│      │   ┌───────────────────────────────────────────────────┐   │      │
│      │   │                   ( Current Logo )                │   │      │
│      │   │                   [ Change Logo ]                 │   │      │
│      │   └───────────────────────────────────────────────────┘   │      │
│      │                                                           │      │
│      │   Team Name                                               │      │
│      │   ┌───────────────────────────────────────────────────┐   │      │
│      │   │ Mumbai Indians                                    │   │      │
│      │   └───────────────────────────────────────────────────┘   │      │
│      │                                                           │      │
│      │   Short Name                                              │      │
│      │   ┌───────────────────────────────────────────────────┐   │      │
│      │   │ MI                                                │   │      │
│      │   └───────────────────────────────────────────────────┘   │      │
│      │                                                           │      │
│      │                                                           │      │
│      │   [ Cancel ]                            [ SAVE CHANGES ]  │      │
│      │                                                           │      │
│      └───────────────────────────────────────────────────────────┘      │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Field Name | Type | Description | Mandatory | Pre-filled |
| :--- | :--- | :--- | :--- | :--- |
| Logo | Image/File | The franchise's current logo | No | Yes (Existing image) |
| Team Name | Text | The full name of the franchise | Yes | Yes (Existing name) |
| Short Name | Text | The abbreviation or acronym of the team | Yes | Yes (Existing abbreviation) |

#### 4. Validations

- **Team Name**:
  - Must not be empty.
  - Must be unique within this specific auction (excluding the team's own current name).
- **Short Name**:
  - Must not be empty.
  - Should ideally be restricted to 2-4 uppercase characters.
  - Must be unique within this specific auction (excluding the team's own current short name).
- **Logo**:
  - Valid image formats only (JPG, PNG, WebP). Max file size (e.g., 2MB).

#### 5. Business Rules

- **Default State**: When the modal opens, it makes an API call (or uses locally cached state) to fetch and pre-fill the form with the team's existing data.
- **Save Action**: Clicking `[ SAVE CHANGES ]` validates the inputs and updates the team's record in the database.
- **UI Update**: Upon successful update, the modal closes automatically, a success toast appears (e.g., "Team updated successfully"), and the Team List Table refreshes to display the new information.
- **Cancel Action**: Clicking `[ Cancel ]` or the `[ X ]` icon closes the modal without saving, discarding any modifications made.

---

### Screen 7.1.4: View Team Profile

#### 1. Overview

The View Team Profile screen is accessed by clicking the View (👁) icon on the Team List Table.

It provides a comprehensive overview of a specific franchise. Organizers can track the team's financial health (KPIs), view the roster of players they have purchased, track their balance history, and export various reports or squad posters for social media.

---

#### 2. Screen Preview

A detailed dashboard-style layout specific to the selected team.

##### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  ← Back to Team List                                                                        │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │   ( LOGO )    Mumbai Indians (MI)                                                     │  │
│  │                                                                                       │  │
│  │   [ ⬇️ Excel Report ]  [ ⬇️ PDF Export ]  [ ⬇️ T-Shirt Excel ]  [ ⬇️ Balance Report ] │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
│                                                                                             │
│  📊 KPIs                                                                                    │
│  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐       │
│  │ Total Points │ │ Used Points  │ │ Avail. Points│ │ Max Bid Pts. │ │ Total Players│       │
│  │   100,000    │ │    45,000    │ │    55,000    │ │    40,000    │ │   5 / 15     │       │
│  └──────────────┘ └──────────────┘ └──────────────┘ └──────────────┘ └──────────────┘       │
│  (Total Reserved Players: 2)                                                                │
│                                                                                             │
│  [ Sold Players ]  [ Balance History ]  [ Squad Poster ]                                    │
│  ────────────────────────────────────────────────────────────────────────────────────────── │
│                                                                                             │
│   ┌────┬────────────────────────────┬─────────────┬───────────────┐                         │
│   │ No │ Photo & Name               │ Phone       │ Sold Amount   │                         │
│   ├────┼────────────────────────────┼─────────────┼───────────────┤                         │
│   │ 1  │ (PHOTO) Virat Kohli        │ 9876543210  │ $ 25,000      │                         │
│   ├────┼────────────────────────────┼─────────────┼───────────────┤                         │
│   │ 2  │ (PHOTO) MS Dhoni           │ 9123456780  │ $ 20,000      │                         │
│   └────┴────────────────────────────┴─────────────┴───────────────┘                         │
│                                                                                             │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Element Name | Type | Description | Visibility |
| :--- | :--- | :--- | :--- |
| Logo, Name & Short Name | Display Text/Image | Basic identity of the team | Always visible |
| Export Buttons | Action Buttons | Downloads reports (Excel, PDF, T-Shirt Data, Balance) | Always visible |
| KPIs (Points & Players) | Data Widgets | Real-time tracking of the team's budget and roster limits | Always visible |
| Sold Player List | Data Table | List of players purchased by the team (No, Name, Phone, Amount) | Visible in Sold Players Tab |
| Team Balance History | Data Log / Table | Chronological log of deductions/additions to the team's purse | Visible in Balance History Tab |
| Squad Poster | Visual Grid/Gallery | Auto-generated promotional posters featuring the bought players | Visible in Squad Poster Tab |

#### 4. Validations

- **KPI Calculations**:
  - `Available Points` must exactly equal `Total Points` - `Used Points`.
  - `Max Bid Points` must be calculated dynamically: `Available Points` - ((`Min Players Required` - `Current Total Players`) * `Minimum Bid`).
  - Total Players cannot exceed the max players allowed per team.
- **Exports**:
  - If no players are sold to the team yet, the Export buttons (like T-Shirt details) should generate an empty template or display a warning toast ("No data to export").

#### 5. Business Rules

- **Data Fetching**: All KPI and Player data on this screen must be fetched in real-time or synced via WebSockets if the auction is currently "Live".
- **Team Balance History**: Every time a player is sold to this team, a ledger entry must be created recording the timestamp, the player bought, and the exact points deducted.
- **Squad Poster Generation**: The system dynamically combines the Team Logo, Player Photo, and Player Name into predefined poster templates that the organizer can download and share on social media.
- **T-Shirt Detail Export**: This specific report must pull the T-shirt sizes (if collected during player registration) for all players in the `Sold Player List`.

---

## 7.2 Internal Section — Players

This section contains all the views and functionalities related to managing the pool of players available for the auction.

### Screen 7.2.1: Player List Table

#### 1. Overview

The Player List Table is the default view when the organizer clicks on the "Players" tab in the Manage Auction screen.

It provides a tabular overview of all players registered for the current auction. Organizers can quickly review player details (like category and age), and perform actions such as viewing full profiles, editing details, or removing players from the auction pool.

---

#### 2. Screen Preview

The full layout with the `Players` tab selected and a data table displaying player records.

##### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  ← Back to Auctions                                                                         │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                                                                                       │  │
│  │   ( LOGO )    Auction Name: Premier League 2026          [ START AUCTION ]            │  │
│  │               Auction Code: PL-2026-X8F                  [ VIEW AUCTION ]             │  │
│  │               Date & Time: 15 Oct 2026, 10:00 AM                                      │  │
│  │               Players Per Team: 15                                                    │  │
│  │                                                                                       │  │
│  │   Plan: Free          Live Link: [ Copy Link ]                                        │  │
│  │   Views: 1.2K         [ Upgrade Now ]                                                 │  │
│  │                                                                                       │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
│                                                                                             │
│  [ Teams ]  [ ━━ Players ━━ ]  [ MVP ]  [ Sponsors ]  [ Link ]  [ About ]                   │
│  ────────────────────────────────────────────────────────────────────────────────────────── │
│                                                                                             │
│     Players (120)                         [⬇️ Export]  [ + ADD PLAYER ]                     │
│                                                                                             │
│     ┌────┬────────────────────────┬─────────────┬─────┬─────────────┬─────────┐             │
│     │ No │ Player Photo & Name    │ Category    │ Age │ Phone No.   │ Actions │             │
│     ├────┼────────────────────────┼─────────────┼─────┼─────────────┼─────────┤             │
│     │ 1  │ (PHOTO) Virat Kohli    │ Batsman     │ 35  │ 9876543210  │ 👁 ✏️ 🗑️ │             │
│     ├────┼────────────────────────┼─────────────┼─────┼─────────────┼─────────┤             │
│     │ 2  │ (PHOTO) Jasprit B.     │ Bowler      │ 30  │ 9123456789  │ 👁 ✏️ 🗑️ │             │
│     ├────┼────────────────────────┼─────────────┼─────┼─────────────┼─────────┤             │
│     │ 3  │ (PHOTO) Ben Stokes     │ All-Rounder │ 32  │ 9988776655  │ 👁 ✏️ 🗑️ │             │
│     └────┴────────────────────────┴─────────────┴─────┴─────────────┴─────────┘             │
│                                                                                             │
│     Showing 1 to 3 of 120 Players                                                           │
│                                                                                             │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Column Name | Type | Description | Visibility |
| :--- | :--- | :--- | :--- |
| No | Number | Sequential serial number for the list | Always visible |
| Player Photo & Name | Text + Image | The player's profile photo followed by their full name | Always visible |
| Category | Text | The playing role of the player (e.g., Batsman, Bowler) | Always visible |
| Age | Number | The age of the player | Always visible |
| Phone Number | Text/Number | Contact number of the player | Always visible |
| Actions | Buttons/Icons | Quick actions: View (Eye), Edit (Pencil), Delete (Trash) | Always visible |

#### 4. Validations

- **Empty State**: 
  - If no players are registered yet, the table should be hidden and replaced with an "Empty State" graphic and a prompt to "Add your first player".
- **Delete Confirmation**:
  - Clicking the Delete (Trash) icon must trigger a confirmation modal (e.g., "Are you sure you want to delete this player?").

#### 5. Business Rules

- **Sorting/Pagination**: The player list should be sortable (e.g., by Name, Category, or Age) and paginated if the list is long (e.g., 20 players per page).
- **Routing**:
  - Clicking **Add Player** redirects to a dedicated "Add Player" form (or modal, depending on the complexity of fields).
  - Clicking **View (👁)** redirects to a detailed Player Profile page, showing their full stats, base price, and auction status (Sold/Unsold).
  - Clicking **Edit (✏️)** opens an "Edit Player" form pre-filled with the player's current data.
  - Clicking **Delete (🗑️)** removes the player from the auction pool. A player cannot be deleted if the auction is "Live" and they are currently on the block, or if they have already been sold to a team.

---

### Screen 7.2.2: Add Player

#### 1. Overview

The Add Player Screen is a comprehensive form used to register a new player into the auction pool. 

To provide organizers with flexibility, this screen offers three distinct methods to onboard players:
1. **Add from Form**: The default view where the organizer manually enters the player's details.
2. **Add Via Link**: Generates a shareable registration link that players can fill out themselves.
3. **Bulk Upload**: Allows uploading multiple players at once via an Excel/CSV template.

Additionally, this form features a **Dynamic Customization** capability. Organizers can toggle the visibility of predefined fields and add brand new custom fields if the default form is missing anything they require.

---

#### 2. Screen Preview

A long scrolling form layout with alternative onboarding methods and a field customization option.

##### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  ← Back to Players                                                                          │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │   Add New Player                                                                      │  │
│  │   [🔗 Add via link ]          [⚙️ Customize Fields]               [⬆️ Bulk Upload]    │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                                                                                       │  │
│  │   ( Upload Photo )                                                                    │  │
│  │   [ Camera Icon  ]                                                                    │  │
│  │                                                                                       │  │
│  │   Full Name *                         Mobile No *                                     │  │
│  │   [ e.g., Virat Kohli              ]  [ e.g., 9876543210               ]              │  │
│  │                                                                                       │  │
│  │   Age *                               Category *                                      │  │
│  │   [ e.g., 35                       ]  [ Select Category ▼              ]              │  │
│  │                                                                                       │  │
│  │   Batting Spec (Spec 1)               Bowling Spec (Spec 2)                           │  │
│  │   [ Select Batting Style ▼         ]  [ Select Bowling Style ▼         ]              │  │
│  │                                                                                       │  │
│  │   Player Role (Spec 3)                Base Value *                                    │  │
│  │   [ Select Role ▼                  ]  [ e.g., 20000                    ]              │  │
│  │                                                                                       │  │
│  │   Jersey Size                         Trouser Size                                    │  │
│  │   [ Select Size (XS to 5XL) ▼      ]  [ Select Size (26 to 48) ▼       ]              │  │
│  │                                                                                       │  │
│  │   Jersey Name                         Jersey Number                                   │  │
│  │   [ e.g., VIRAT                    ]  [ e.g., 18                       ]              │  │
│  │                                                                                       │  │
│  │   Matches                             Runs                                            │  │
│  │   [ e.g., 250                      ]  [ e.g., 12000                    ]              │  │
│  │                                                                                       │  │
│  │   Wickets                             Status                                          │  │
│  │   [ e.g., 4                        ]  [ Available ▼                    ]              │  │
│  │                                                                                       │  │
│  │   [ + Add Custom Field ] (e.g., "Food Preference", "Shoe Size")                       │  │
│  │                                                                                       │  │
│  │   Extra Details                                                                       │  │
│  │   [ Enter any additional info or notes...                                           ] │  │
│  │                                                                                       │  │
│  │                                 [ Cancel ]  [ SAVE PLAYER ]                           │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

**Customize Fields Drawer/Modal (Triggered by ⚙️ Customize Fields)**
```text
┌───────────────────────────────────────┐
│  Manage Form Fields             [ X ] │
│  ───────────────────────────────────  │
│  Select fields to display on form:    │
│  [☑] Player Photo                     │
│  [☑] Full Name (Mandatory)            │
│  [☑] Mobile No (Mandatory)            │
│  [☑] Age (Mandatory)                  │
│  [☑] Category (Mandatory)             │
│  [☑] Specification 1 (Batting)        │
│  [ ] Specification 2 (Bowling)        │
│  [☑] Specification 3 (Role)           │
│  [☑] Base Value (Mandatory)           │
│  [ ] Jersey Size                      │
│  [ ] Trouser Size                     │
│  [ ] Jersey Name                      │
│  ... (all other fields)               │
│                                       │
│  [ SAVE PREFERENCES ]                 │
└───────────────────────────────────────┘
```

#### 3. Fields Table

| Field Name | Type | Description | Mandatory |
| :--- | :--- | :--- | :--- |
| Player Photo | Image/File | Profile picture of the player | No |
| Full Name | Text | Complete name of the player | Yes |
| Mobile No | Number/Text | Contact number | Yes |
| Age | Number | Age in years | Yes |
| Category | Dropdown | Broad category classification | Yes |
| Specification 1 | Dropdown | Batting Style (e.g., Right Hand, Opener, Finisher, etc.) | No |
| Specification 2 | Dropdown | Bowling Style (e.g., Right Arm Fast, Left Arm Orthodox, etc.) | No |
| Specification 3 | Dropdown | Player Role (e.g., Pure Batsman, Wicket Keeper, Captain, etc.) | No |
| Base Value | Number/Currency| The starting bid amount for the player | Yes |
| Jersey Size | Dropdown | Size from XS to 5XL, or Other | No |
| Trouser Size | Dropdown | Size from 26 to 48, or Other | No |
| Jersey Name | Text | Name to be printed on the jersey | No |
| Jersey Number| Number | Preferred jersey number | No |
| Match | Number | Total matches played | No |
| Run | Number | Total runs scored | No |
| Wickets | Number | Total wickets taken | No |
| Extra Details | Text Area | Any additional notes or background info | No |
| Status | Dropdown | 'Available', 'Sold', or 'Unsold' | Yes (Default: Available) |
| **Custom Fields** | Dynamic | Any additional field created by the user | Configurable |

#### 4. Validations

- **Dropdown Values**:
  - **Spec 1 (Batting)**: Right Hand Batsman, Left Hand Batsman, Opener, Top Order, Middle Order, Finisher, Anchor, Power Hitter, Other.
  - **Spec 2 (Bowling)**: Right Arm Fast, Right Arm Fast-Medium, Right Arm Medium, Left Arm Fast, Left Arm Fast-Medium, Left Arm Medium, Right Arm Off Spin (Off Break), Right Arm Leg Spin (Leg Break), Left Arm Orthodox, Left Arm Chinaman (Unorthodox), Other.
  - **Spec 3 (Role)**: Pure Batsman, Pure Bowler, All Rounder, Batting All Rounder, Bowling All Rounder, Wicket Keeper, Wicket Keeper Batsman, Captain, Vice Captain, Other.
- **Mobile No**: Must follow a valid phone number regex pattern (e.g., 10 digits).
- **Age, Base Value, Match, Run, Wickets**: Must be positive numeric values. Negative numbers are invalid.
- **Jersey & Trouser Size**: Restricted to the defined dropdown ranges.

#### 5. Business Rules

- **Dynamic Form Configuration**:
  - All default fields have an associated checkbox in the "Customize Fields" settings.
  - By default, all checkboxes are **checked**.
  - If a user unchecks a specific field (e.g., "Trouser Size"), that field is completely hidden from the Add Player form. (Note: Mandatory fields like Full Name or Base Value cannot be unchecked/hidden).
- **Add Custom Field**: 
  - If the user needs to collect data not covered by the default form (e.g., "Food Preference", "Shoe Size"), they can click `[ + Add Custom Field ]`. 
  - This prompts them to define a Field Name and Input Type (Text, Number, Dropdown). The new field is then appended to the form dynamically.
- **Alternative Onboarding Actions**:
  - Clicking `[🔗 Add via link ]` copies a unique, public-facing registration URL to the organizer's clipboard. This public form will mirror the exact field visibility and custom fields configured by the organizer.
  - Clicking `[⬆️ Bulk Upload]` opens a modal where the user can download a CSV template and upload a filled CSV to import multiple players simultaneously.
- **Default Status**: When a player is manually added via this form, their `Status` automatically defaults to "Available" unless specifically overridden.
- **Save Action**: Clicking `[ SAVE PLAYER ]` validates all visible mandatory fields. If successful, the player is added to the auction pool, and the user is redirected back to the Player List Table (Screen 7.2.1).
- **Cancel Action**: Clicking `[ Cancel ]` redirects the user back to the Player List Table without saving any data.

---

### Screen 7.2.2.1: Bulk Upload Players (Modal)

#### 1. Overview

The Bulk Upload Players Modal is triggered when the organizer clicks the `[⬆️ Bulk Upload]` button on the Add Player screen.

This modal is designed to streamline the onboarding process for large tournaments. It allows the organizer to download a standardized Excel template, fill it offline, and upload it to import dozens or hundreds of players at once.

---

#### 2. Screen Preview

A centered modal over a darkened background, focusing on the file upload interaction.

##### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                         │
│  [Darkened Background / Overlay of the Add Player Screen]               │
│                                                                         │
│      ┌───────────────────────────────────────────────────────────┐      │
│      │                                                           │      │
│      │   Bulk Upload Players                               [ X ] │      │
│      │   ─────────────────────────────────────────────────────   │      │
│      │                                                           │      │
│      │   Step 1: Download Template                               │      │
│      │   [⬇️ Download Sample Excel Template ]                     │      │
│      │                                                           │      │
│      │                                                           │      │
│      │   Step 2: Upload Filled Data                              │      │
│      │   ┌───────────────────────────────────────────────────┐   │      │
│      │   │                                                   │   │      │
│      │   │                  [ Upload Icon ]                  │   │      │
│      │   │          Drag & Drop your Excel file here         │   │      │
│      │   │                        or                         │   │      │
│      │   │                 [ Browse Files ]                  │   │      │
│      │   │                                                   │   │      │
│      │   └───────────────────────────────────────────────────┘   │      │
│      │                                                           │      │
│      │                                                           │      │
│      │   [ Cancel ]                             [ ADD PLAYERS ]  │      │
│      │                                                           │      │
│      └───────────────────────────────────────────────────────────┘      │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Element Name | Type | Description | Mandatory |
| :--- | :--- | :--- | :--- |
| Download Sample Link | Hyperlink/Button | Downloads the standardized `.xlsx` template | N/A |
| Upload Area | File Dropzone | Area to drag and drop or browse for the filled Excel file | Yes |

#### 4. Validations

- **File Type**: Only `.xls` or `.xlsx` files are permitted. If a user uploads a PDF or Image, show an error: "Invalid file type. Please upload an Excel file."
- **File Size**: Restrict the maximum file size (e.g., 5MB or 10MB) to prevent server timeouts.
- **Data Integrity**: 
  - The uploaded file must match the column headers of the sample template exactly.
  - Mandatory fields (e.g., Name, Category, Base Price) within the Excel rows must not be blank.

#### 5. Business Rules

- **Sample Template**: The downloaded template contains column headers mapping directly to the player fields (Name, Mobile No, Category, Specs, Base Value, etc.) along with a "Read Me" sheet explaining the valid dropdown values.
- **Save/Add Action**: 
  - Clicking `[ ADD PLAYERS ]` sends the file to the backend for parsing.
  - The backend validates the rows. If errors are found (e.g., invalid category names), the process is halted, and the organizer is presented with a summary of which rows failed and why.
  - If successful, the players are imported into the auction, the modal closes, and the user is redirected to the Player List Table with a success message (e.g., "50 Players Imported Successfully").
- **Cancel Action**: Clicking `[ Cancel ]` or the `[ X ]` icon closes the modal without uploading any data.

---

### Screen 7.2.1.1: Export Players (Modal)

#### 1. Overview

The Export Players Modal is triggered when the organizer clicks the `[⬇️ Export]` button on the Player List Table.

This modal gives the organizer complete control over exporting the player pool data into either an Excel file or a highly customizable PDF report, allowing them to filter, sort, and select exactly which data columns they want to include.

---

#### 2. Screen Preview

The modal overlays the Player List Table with various configuration options for the PDF export.

##### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                         │
│  [Darkened Background / Overlay of the Player List Table]               │
│                                                                         │
│      ┌───────────────────────────────────────────────────────────┐      │
│      │                                                           │      │
│      │   Export Players                                    [ X ] │      │
│      │   ─────────────────────────────────────────────────────   │      │
│      │                                                           │      │
│      │   [⬇️ Export Player Excel ]                                │      │
│      │   (Exports all fields as a raw data spreadsheet)          │      │
│      │                                                           │      │
│      │   ─────────────────────────────────────────────────────   │      │
│      │   Export Player PDF Configuration                         │      │
│      │                                                           │      │
│      │   PDF Option                                              │      │
│      │   [ Select Option ▼                                     ] │      │
│      │                                                           │      │
│      │   Order By                                                │      │
│      │   [ Select Order By ▼                                   ] │      │
│      │                                                           │      │
│      │   No. Of Columns                    Status                │      │
│      │   [ Two ▼                         ] [ All ▼             ] │      │
│      │                                                           │      │
│      │   ▼ Manage Data (Columns to Include)                      │      │
│      │   ┌───────────────────────────────────────────────────┐   │      │
│      │   │ [☑] Photo              [☑] Specialization 1       │   │      │
│      │   │ [☑] Number             [☑] Specialization 2       │   │      │
│      │   │ [☑] Category           [☑] Specialization 3       │   │      │
│      │   │ [☑] Team               [ ] Age                    │   │      │
│      │   │ [☑] Info (Name/Stats)  [ ] Base Value             │   │      │
│      │   │ [ ] Mobile No          [ ] Match/Run/Wickets      │   │      │
│      │   └───────────────────────────────────────────────────┘   │      │
│      │                                                           │      │
│      │                                                           │      │
│      │   [ Cancel ]                        [ ⬇️ EXPORT PDF ]      │      │
│      │                                                           │      │
│      └───────────────────────────────────────────────────────────┘      │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Element Name | Type | Description |
| :--- | :--- | :--- |
| Export Player Excel | Button | Quickly downloads an `.xlsx` file containing all player records and all fields. |
| PDF Option | Dropdown | Filters the PDF scope: `All`, `Category Wise`, `Team Wise`. |
| Order By | Dropdown | Sorts the PDF: `Player Name`, `Player Number`, `Sold Value`, `Sold Sequence`, `Category Wise`. |
| No. Of Columns | Dropdown | Layout structure of the PDF: `Two` (Default), `Three`. |
| Status | Dropdown | Filters by availability: `All`, `Available`, `Sold`, `Unsold`. |
| Manage Data | Collapsible | Expanding this reveals checkboxes for every player data field. |
| Manage Data Checkboxes| Checkboxes | Dictates which data points appear on the generated PDF. |

#### 4. Validations

- **Manage Data Selection**:
  - At least one checkbox must be selected in the "Manage Data" section to generate a PDF. If none are selected, disable the `[ ⬇️ EXPORT PDF ]` button or show an error toast.
- **Empty State**:
  - If the filter combination (e.g., Status: Sold + PDF Option: Category Wise) yields zero players, show a toast notification ("No players found for the selected criteria").

#### 5. Business Rules

- **Excel Export Behavior**: Clicking `[⬇️ Export Player Excel]` bypasses the PDF configurations entirely and immediately downloads a `.xlsx` file containing every single data field for all players in the pool.
- **Default Manage Data State**: When the "Manage Data" section is expanded, the following checkboxes are ticked by default: `Photo`, `Number`, `Category`, `Team`, `Info` (basic stats/name), `Specialization 1`, `Specialization 2`, and `Specialization 3`. All other fields (from the Add Player form) are unchecked by default.
- **PDF Layout Generation (No. of Columns)**:
  - If `Two` is selected, the PDF generates a grid with two player profiles per row.
  - If `Three` is selected, the PDF generates a grid with three slightly smaller player profiles per row.
- **Save/Export Action**: Clicking `[ ⬇️ EXPORT PDF ]` sends the configuration to the backend server, which renders a styled PDF document matching the exact selections, and triggers a download in the organizer's browser.
- **Cancel Action**: Clicking `[ Cancel ]` or the `[ X ]` icon closes the modal without generating any exports.

---

### Screen 7.2.3: Edit Player

#### 1. Overview
Triggered by clicking the `[ ✏️ ]` icon on a specific player in the Player List Table. This screen is identical to the Add Player form (Screen 7.2.2), but all fields are pre-filled with the player's existing data so the organizer can make updates.

#### 2. Screen Preview
*(Same UI structure as Screen 7.2.2, but the title reads "Edit Player", and the fields already contain the player's data. The submit button reads `[ UPDATE PLAYER ]`)*.

#### 3. Fields Table
*(Same fields as Screen 7.2.2)*

#### 4. Validations
- **Data Integrity**: Mandatory fields cannot be cleared and left blank upon saving. 
- **Status Change**: If the organizer manually changes the Status from "Sold" to "Available", any associated team linkages must be cleared.

#### 5. Business Rules
- **Update Action**: Clicking `[ UPDATE PLAYER ]` overrides the existing data in the database and redirects the user back to the Player List Table with a success toast.

---

### Screen 7.2.4: View Player

#### 1. Overview
Triggered by clicking the `[ 👁 ]` icon on a specific player in the Player List Table. It provides a clean, comprehensive, read-only profile of the player, summarizing all their stats and auction status.

#### 2. Screen Preview

##### Desktop Layout
```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  ← Back to Players                                                                          │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │   Player Profile                                                                      │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                                                                                       │  │
│  │   [ LARGE PLAYER PHOTO ]                                                              │  │
│  │                                                                                       │  │
│  │   Virat Kohli                                                                         │  │
│  │   Mobile No: 9876543210                                                               │  │
│  │   Age: 35  |  Category: Batsman                                                       │  │
│  │                                                                                       │  │
│  │   --- Specifications ---                                                              │  │
│  │   Batting: Right Hand Batsman                                                         │  │
│  │   Bowling: Right Arm Medium                                                           │  │
│  │   Role: Top Order                                                                     │  │
│  │                                                                                       │  │
│  │   --- Sizing ---                                                                      │  │
│  │   Jersey Name: VIRAT        Jersey Number: 18                                         │  │
│  │   Jersey Size: L            Trouser Size: 32                                          │  │
│  │                                                                                       │  │
│  │   --- Statistics ---                                                                  │  │
│  │   Matches: 250              Runs: 12000               Wickets: 4                      │  │
│  │                                                                                       │  │
│  │   --- Auction Status ---                                                              │  │
│  │   Base Value: $ 20,000                                                                │  │
│  │   Current Status: Sold (to Royal Challengers)                                         │  │
│  │   Sold Price: $ 25,000                                                                │  │
│  │                                                                                       │  │
│  │   Extra Details:                                                                      │  │
│  │   Available for the full season.                                                      │  │
│  │                                                                                       │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table
- **All Fields from Add Player**: Displayed in a read-only format.
- **Auction Data**: If sold, displays the `Sold Price` and the `Team` they were sold to.

#### 4. Validations
- None (Read-only state).

#### 5. Business Rules
- **Data Display**: If an optional field (like Wickets or Jersey Number) was not provided during registration, it should be hidden from the profile view to maintain a clean layout.
- **Navigation**: The back button returns the user to the exact page they were on in the Player List Table (preserving pagination state).

---

## 7.3 Internal Section — MVP (Most Valuable Player)

This section focuses on the financial highlights of the auction, automatically tracking the highest-paid players across the tournament.

### Screen 7.3: MVP Leaderboard

#### 1. Overview

The MVP Leaderboard is accessed via the "MVP" tab on the Manage Auction screen. 

It acts as a dynamic leaderboard. As soon as a player is sold to any team during the live auction, they are automatically listed here. The list is strictly ordered by the `Sold Price`, showcasing the most expensive players at the top.

---

#### 2. Screen Preview

The layout highlights the "MVP" tab and features a clean, read-only data table focused on player valuation.

##### Desktop Layout

```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  ← Back to Auctions                                                                         │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                                                                                       │  │
│  │   ( LOGO )    Auction Name: Premier League 2026          [ START AUCTION ]            │  │
│  │               Auction Code: PL-2026-X8F                  [ VIEW AUCTION ]             │  │
│  │               Date & Time: 15 Oct 2026, 10:00 AM                                      │  │
│  │               Players Per Team: 15                                                    │  │
│  │                                                                                       │  │
│  │   Plan: Free          Live Link: [ Copy Link ]                                        │  │
│  │   Views: 1.2K         [ Upgrade Now ]                                                 │  │
│  │                                                                                       │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
│                                                                                             │
│  [ Teams ]  [ Players ]  [ ━━ MVP ━━ ]  [ Sponsors ]  [ Link ]  [ About ]                   │
│  ────────────────────────────────────────────────────────────────────────────────────────── │
│                                                                                             │
│     Top Sold Players (Leaderboard)                                                          │
│                                                                                             │
│     ┌────┬────────────────────────┬─────────────┬──────────────────┐                        │
│     │ No │ Player Photo & Name    │ Mobile No   │ Sold Price       │                        │
│     ├────┼────────────────────────┼─────────────┼──────────────────┤                        │
│     │ 1  │ (PHOTO) Virat Kohli    │ 9876543210  │ $ 25,000         │                        │
│     ├────┼────────────────────────┼─────────────┼──────────────────┤                        │
│     │ 2  │ (PHOTO) Jasprit B.     │ 9123456789  │ $ 22,500         │                        │
│     ├────┼────────────────────────┼─────────────┼──────────────────┤                        │
│     │ 3  │ (PHOTO) Ben Stokes     │ 9988776655  │ $ 18,000         │                        │
│     └────┴────────────────────────┴─────────────┴──────────────────┘                        │
│                                                                                             │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Column Name | Type | Description | Visibility |
| :--- | :--- | :--- | :--- |
| No | Number | Sequential rank (1 being the highest paid) | Always visible |
| Player Photo & Name | Text + Image | Profile picture followed by the player's full name | Always visible |
| Mobile No | Text/Number | Contact number of the player | Always visible |
| Sold Price | Currency | The final winning bid amount for the player | Always visible |

#### 4. Validations

- **Empty State**: 
  - If no players have been sold yet (e.g., the auction hasn't started), display an empty state graphic with the text: "No players sold yet. The leaderboard will populate once the auction begins."
- **Exclusions**:
  - Players with a status of `Available` or `Unsold` must never appear in this table.

#### 5. Business Rules

- **Auto-Sorting**: The table must automatically and strictly sort by `Sold Price` in descending order (Highest to Lowest).
- **Real-Time Sync**: If the auction is currently "Live", this table must update dynamically via WebSockets every time a player's auction concludes and they are marked as "Sold".
- **Tie-Breaker Logic**: If two players are sold for the exact same amount, the tie should be broken chronologically (the player who was sold *first* takes the higher rank/lower No).
- **Read-Only View**: Unlike the Players tab, the MVP table does not have action buttons (Edit, Delete). It is strictly a reporting and visualization tool for the organizer.

---

## 7.4 Internal Section — Sponsors

This section allows the organizer to manage and display tournament sponsors. Sponsors can be assigned to specific parts of the auction (e.g., "Title Sponsor", "Drinks Sponsor", "Man of the Match Sponsor").

### Screen 7.4.1: Sponsor List Table

#### 1. Overview
The default view when navigating to the "Sponsors" tab. It displays a tabular list of all sponsors currently associated with the tournament.

#### 2. Screen Preview

##### Desktop Layout
```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  ← Back to Auctions                                                                         │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                                                                                       │  │
│  │   ( LOGO )    Auction Name: Premier League 2026          [ START AUCTION ]            │  │
│  │               Auction Code: PL-2026-X8F                  [ VIEW AUCTION ]             │  │
│  │               Date & Time: 15 Oct 2026, 10:00 AM                                      │  │
│  │               Players Per Team: 15                                                    │  │
│  │                                                                                       │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
│                                                                                             │
│  [ Teams ]  [ Players ]  [ MVP ]  [ ━━ Sponsors ━━ ]  [ Link ]  [ About ]                   │
│  ────────────────────────────────────────────────────────────────────────────────────────── │
│                                                                                             │
│     Sponsors (4)                                       [ + ADD SPONSOR ]                    │
│                                                                                             │
│     ┌────┬────────────────────────────┬─────────────────────────────┬─────────┐             │
│     │ No │ Sponsor Photo & Name       │ Sponsor For                 │ Actions │             │
│     ├────┼────────────────────────────┼─────────────────────────────┼─────────┤             │
│     │ 1  │ (LOGO) Dream11             │ Title Sponsor               │ 👁 ✏️ 🗑️ │             │
│     ├────┼────────────────────────────┼─────────────────────────────┼─────────┤             │
│     │ 2  │ (LOGO) Gatorade            │ Official Beverage Partner   │ 👁 ✏️ 🗑️ │             │
│     └────┴────────────────────────────┴─────────────────────────────┴─────────┘             │
│                                                                                             │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Column Name | Type | Description |
| :--- | :--- | :--- |
| No | Number | Sequential index |
| Sponsor Photo & Name | Text + Image | Logo of the sponsoring brand and their company name |
| Sponsor For | Text | The specific category/title they are sponsoring |
| Actions | Buttons | `View (👁)`, `Edit (✏️)`, `Delete (🗑️)` actions |

#### 4. Validations
- **Empty State**: If no sponsors have been added, display a message: "No Sponsors added yet. Click '+ Add Sponsor' to create one."

#### 5. Business Rules
- **Routing**: All action buttons (`Add`, `View`, `Edit`, `Delete`) trigger popup modals rather than redirecting to full-page screens to keep the user in context.

---

### Screen 7.4.2: Add Sponsor (Modal)

#### 1. Overview
Triggered by clicking `[ + ADD SPONSOR ]` in the list table. It is a lightweight popup modal used to quickly register a new sponsor.

#### 2. Screen Preview

##### Modal Layout
```text
┌───────────────────────────────────────────────────────────┐
│   Add New Sponsor                                   [ X ] │
│   ─────────────────────────────────────────────────────   │
│                                                           │
│   ( Upload Logo )                                         │
│   [ Camera Icon ]                                         │
│                                                           │
│   Sponsor Name *                                          │
│   [ e.g., Dream11                                       ] │
│                                                           │
│   Sponsor For *                                           │
│   [ e.g., Title Sponsor, Beverage Partner               ] │
│                                                           │
│                                                           │
│   [ Cancel ]                            [ SAVE SPONSOR ]  │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Field Name | Type | Mandatory |
| :--- | :--- | :--- |
| Sponsor Photo | File/Image | No |
| Name | Text | Yes |
| Sponsor For | Text | Yes |

#### 4. Validations
- Both `Name` and `Sponsor For` cannot be blank.

#### 5. Business Rules
- **Save Action**: Clicking `[ SAVE SPONSOR ]` commits the record, closes the modal, and refreshes the sponsor list table with a success toast.

---

### Screen 7.4.3: Edit Sponsor (Modal)

#### 1. Overview
Triggered by clicking the `[ ✏️ ]` icon on a specific row. It uses the exact same modal layout as "Add Sponsor", but the fields are pre-filled with the sponsor's existing data.

#### 2. Screen Preview
*(Same UI structure as Screen 7.4.2, but the title reads "Edit Sponsor" and fields contain existing data).*

#### 3. Fields Table
*(Same as Screen 7.4.2)*

#### 4. Validations
- Fields cannot be cleared of existing data and left blank upon saving.

#### 5. Business Rules
- **Update Action**: Clicking `[ UPDATE SPONSOR ]` overrides the existing data, closes the popup, and refreshes the list table.

---

### Screen 7.4.4: View Sponsor (Modal)

#### 1. Overview
Triggered by clicking the `[ 👁 ]` icon on a specific row. It opens a read-only popup displaying the sponsor's details cleanly.

#### 2. Screen Preview

##### Modal Layout
```text
┌───────────────────────────────────────────────────────────┐
│   Sponsor Details                                   [ X ] │
│   ─────────────────────────────────────────────────────   │
│                                                           │
│            [ LARGE SPONSOR LOGO / PHOTO ]                 │
│                                                           │
│   Name                                                    │
│   Dream11                                                 │
│                                                           │
│   Sponsor For                                             │
│   Title Sponsor                                           │
│                                                           │
│                                        [ CLOSE ]          │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

#### 3. Fields Table
- **Sponsor Photo**: Read-only display.
- **Name**: Read-only text.
- **Sponsor For**: Read-only text.

#### 4. Validations
- None (Read-only state).

#### 5. Business Rules
- **Close Action**: Clicking `[ CLOSE ]` or `[ X ]` simply dismisses the modal and returns the user to the list table.

---

## 7.5 Internal Section — Link

This section serves as a centralized hub for all public-facing and integration URLs related to the auction. Organizers can quickly grab these links to share with players, audiences, or broadcasters.

### Screen 7.5: Links Management

#### 1. Overview
The "Link" tab displays a clean list of copyable URLs. It provides access to the public live view of the auction, the self-service player registration form, and graphical overlays intended for live broadcasting on platforms like YouTube.

#### 2. Screen Preview

##### Desktop Layout
```text
┌─────────────────────────────────────────────────────────────────────────────────────────────┐
│  [ AUCTION LOGO ]    Dashboard    Auctions         [🔍 Search...]       [🔔]  (Profile ▼)   │
├─────────────────────────────────────────────────────────────────────────────────────────────┤
│                                                                                             │
│  ← Back to Auctions                                                                         │
│                                                                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                                                                                       │  │
│  │   ( LOGO )    Auction Name: Premier League 2026          [ START AUCTION ]            │  │
│  │               Auction Code: PL-2026-X8F                  [ VIEW AUCTION ]             │  │
│  │               Date & Time: 15 Oct 2026, 10:00 AM                                      │  │
│  │               Players Per Team: 15                                                    │  │
│  │                                                                                       │  │
│  └───────────────────────────────────────────────────────────────────────────────────────┘  │
│                                                                                             │
│  [ Teams ]  [ Players ]  [ MVP ]  [ Sponsors ]  [ ━━ Link ━━ ]  [ About ]                   │
│  ────────────────────────────────────────────────────────────────────────────────────────── │
│                                                                                             │
│     Important Auction Links                                                                 │
│                                                                                             │
│     ┌───────────────────────────────────────────────────────────────────────────┐           │
│     │  🌐 Live Web View                                                         │           │
│     │  Share this link with audiences to watch the live auction leaderboard.    │           │
│     │  [ https://cricketauction.com/live/PL-2026-X8F ]           [ COPY LINK ]  │           │
│     └───────────────────────────────────────────────────────────────────────────┘           │
│                                                                                             │
│     ┌───────────────────────────────────────────────────────────────────────────┐           │
│     │  📝 Player Registration Link                                              │           │
│     │  Share this link with players to allow them to register themselves.       │           │
│     │  [ https://cricketauction.com/register/PL-2026-X8F ]       [ COPY LINK ]  │           │
│     └───────────────────────────────────────────────────────────────────────────┘           │
│                                                                                             │
│     ┌───────────────────────────────────────────────────────────────────────────┐           │
│     │  📺 YouTube Overlay Links                                                 │           │
│     │  Use this transparent browser source link in OBS / vMix for broadcasting. │           │
│     │  [ https://cricketauction.com/overlay/PL-2026-X8F ]        [ COPY LINK ]  │           │
│     └───────────────────────────────────────────────────────────────────────────┘           │
│                                                                                             │
└─────────────────────────────────────────────────────────────────────────────────────────────┘
```

#### 3. Fields Table

| Element Name | Type | Description |
| :--- | :--- | :--- |
| Live Web View URL | Read-Only Text | The URL pointing to the customer-facing live auction dashboard. |
| Player Registration URL | Read-Only Text | The URL pointing to the public player registration form. |
| YouTube Overlay URL | Read-Only Text | The URL pointing to a transparent screen overlay used for live streaming software (e.g., OBS). |
| Copy Link | Button | Copies the respective URL to the user's clipboard. |

#### 4. Validations
- **Link Integrity**: Links must accurately reflect the specific `Auction Code` of the currently managed auction. 

#### 5. Business Rules
- **Copy Action**: Clicking `[ COPY LINK ]` silently copies the text to the clipboard and triggers a brief success toast (e.g., "Link copied to clipboard!").
- **YouTube Overlay**: This specific link renders a transparent UI designed explicitly to be added as a "Browser Source" in streaming software. It strips away organizer controls and focuses purely on live bidding graphics.

