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
