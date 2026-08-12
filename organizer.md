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
