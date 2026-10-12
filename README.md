# 🌐 SpectraAgora - Enterprise Social Networking Platform

---

## 📑 Table of Contents

- [💎 Core Value Proposition](#-core-value-proposition)
- [📰 Social Feed and Content](#-social-feed-and-content)
- [💬 Direct Messaging](#-direct-messaging)
- [📅 Events and Calendar](#-events-and-calendar)
- [💼 Careers and Job Board](#-careers-and-job-board)
- [🛒 Internal Marketplace](#-internal-marketplace)
- [👤 User Profiles and Networking](#-user-profiles-and-networking)
- [⚙️ Organization Administration](#️-organization-administration)
- [🚀 Organization Onboarding](#-organization-onboarding)
- [🔐 Authentication and Security](#-authentication-and-security)
- [🛡️ Privacy and GDPR Compliance](#️-privacy-and-gdpr-compliance)
- [🔔 Notification System](#-notification-system)
- [📌 Bookmarks and Saved Items](#-bookmarks-and-saved-items)
- [🐛 Bug Reporting and Support](#-bug-reporting-and-support)
- [🔧 Maintenance Windows](#-maintenance-windows)
- [📧 Email Communication System](#-email-communication-system)
- [⏱️ Background Services](#️-background-services)
- [🏗️ Technical Architecture](#️-technical-architecture)
- [🚢 Deployment and Infrastructure](#-deployment-and-infrastructure)
- [📄 License](#-license)

---

## 💎 Core Value Proposition

SpectraAgora replaces fragmented internal tools (email chains, bulletin boards, spreadsheets, separate chat apps) with one unified platform:

| Feature | Description |
|---------|-------------|
| 🗣️ **Unified Communication** | Real-time feed, channels, stories, and direct messaging in one place |
| 🎯 **Talent Mobility** | Internal job board with full application tracking, recommendations, and resume management |
| 🔄 **Resource Sharing** | Internal marketplace with fixed-price and auction-based listings, approval workflow, and bidding |
| 🔒 **Secure Isolation** | Strict multi-tenant architecture ensures complete data isolation between organizations |
| ✅ **Compliance Ready** | Built-in audit trail, GDPR data subject rights, SOC 2 and ISO 27001 technical controls |

---

## 📰 Social Feed and Content

### 📝 Posts and Channels

The feed is organized into channels, which can be public (visible to all members) or private (restricted to specific users or groups).

**Post types:**
- 📄 **Standard Posts** - Rich text content with image and video attachments.
- 📊 **Polls** - Embedded polls with multiple answer choices for team decision-making.
- ❓ **Q&A Posts** - Question-and-answer threads for knowledge sharing.

**Post interactions:**
- 😍 10 reaction types: like, love, celebrate, insightful, support, funny, wow, curious, congrats, thanks.
- 💬 Threaded comments on every post.
- 📌 Pin important posts to the top of a channel.
- 🔖 Save/bookmark posts for personal reference.
- 🔗 Share posts to other channels or via direct message.
- ⭐ Mark posts as important for visibility.
- #️⃣ Hashtag extraction and tracking.

**Channel management:**
- ➕ Create public or private channels.
- 👥 Channel membership based on individual users or user groups.
- 📦 Archive channels when they are no longer active.
- 🔐 Channel-level access control enforced on every request.

### 📖 Stories

Ephemeral 24-hour content inspired by social media stories, adapted for the workplace:

- 🖼️ **Media stories** - Upload images or short videos with text overlay.
- ✍️ **Text stories** - Styled text with customizable background colors.
- 📊 **Poll stories** - Quick polls embedded directly in stories.
- ❓ **Q&A stories** - Open-ended questions for anonymous or named responses.

Stories support emoji reactions, view tracking (who watched each story), and direct message replies.

### 📈 Trending Topics

The platform automatically analyzes feed content and extracts trending hashtags and topics. An AI-powered post idea generator can suggest post topics based on selected categories, helping users contribute to organizational discussions.

---
```mermaid
flowchart LR
  USER["👤 User"] --> CHANNELS["🗂️ Channels"];
  CHANNELS --> POSTS["📝 Posts"];
  CHANNELS --> STORIES["📖 Stories"];
  CHANNELS --> TRENDING["📈 Trending Topics"];

  POSTS --> STANDARD["📄 Standard Post"];
  POSTS --> POLL["📊 Poll"];
  POSTS --> QA["❓ Q&A"];

  POSTS --> REACT["😍 Reactions"];
  POSTS --> COMMENTS["💬 Threaded Comments"];
  POSTS --> SHARE["🔗 Sharing"];
  POSTS --> PIN["📌 Pin"];
  POSTS --> SAVE["🔖 Bookmark"];
  POSTS --> TAGS["#️⃣ Hashtags"];

  STORIES --> MEDIA["🖼️ Media Story"];
  STORIES --> TEXT["✍️ Text Story"];
  STORIES --> STORYPOLL["📊 Poll Story"];
  STORIES --> STORYQA["❓ Q&A Story"];

  STORIES --> VIEWS["👁️ View Tracking"];
  STORIES --> STORYREACT["😄 Emoji Reactions"];
  STORIES --> STORYDM["💬 DM Replies"];
```
---

## 💬 Direct Messaging

One-to-one real-time conversations with the following capabilities:

- ⚡ **Server-Sent Events (SSE)** streaming for instant message delivery.
- ⌨️ **Typing indicators** - See when the other person is composing a message.
- ✅ **Read receipts** - Track which messages have been read.
- ✏️ **Message editing and deletion** - Modify or remove sent messages.
- 😄 **Emoji reactions** on individual messages.
- ↩️ **Message replies** - Reply to a specific message within the conversation.
- 📎 **File attachments** - Send documents and media.
- 🔗 **Shared content** - Share posts, marketplace items, events, and jobs directly in a conversation.
- 🔄 **Sync on reconnection** - Automatically catches up on missed messages after a disconnect.

---

## 📅 Events and Calendar

Create and manage organizational events with full lifecycle support:

- 📋 **Event details** - Title, description, location, date/time range, cover image.
- ✋ **RSVP tracking** - Members can mark going, maybe, or not going.
- ⏰ **Event reminders** - Users set personal reminders for upcoming events.
- 📊 **Event polls** - Embed polls within events (e.g., vote on a lunch venue).
- ✉️ **Invitations** - Invite individual users or entire groups with email notification.
- 🔗 **Event sharing** - Share events via posts or direct messages.
- 🔍 **Filtering and sorting** - Filter by upcoming/past, sort by date or popularity.

---

## 💼 Careers and Job Board

A full internal recruitment module for talent mobility:

- 📝 **Job posting** - Create openings with title, description, requirements, salary range, location, and job type.
- 🚀 **Easy Apply** - Employees submit applications with optional resume/attachment uploads.
- 📊 **Application tracking** - Track application status through stages (applied, reviewed, accepted, rejected).
- 🤝 **Job recommendations** - Recommend a colleague for an open position with a personalized message.
- 🔖 **Saved jobs** - Bookmark jobs for later review.
- 🔗 **Job sharing** - Share openings via posts or direct messages.
- 👨‍💼 **Admin review** - Hiring managers review applicants, view resumes, and update statuses.

---

## 🛒 Internal Marketplace

An internal trading platform for buying, selling, and auctioning items within the organization:

- 🏷️ **Listing types:**
  - 💰 **Fixed price** - Set a price and sell directly.
  - 🔨 **Auction** - Set a starting bid and let members bid. Auctions are automatically processed on expiry.
- 📸 **Item management** - Upload up to 5 images, set condition, category, and description.
- ✅ **Approval workflow** - All listings require admin approval before they become visible.
- 💵 **Bidding system** - Place and track bids on auction items.
- 🔗 **Marketplace sharing** - Share listings via posts or messages.
- 🔖 **Saved items** - Bookmark marketplace items for later.

---
```mermaid
flowchart TB
  HUB["🧩 Organizational Activity Hub"];

  subgraph EVENTS["📅 Events & Calendar"]
    EVENTCRUD["📋 Event Details"];
    RSVP["✋ RSVP Tracking"];
    REM["⏰ Reminders"];
    EPOLL["📊 Event Polls"];
    EINV["✉️ Invitations"];
    ESHARE["🔗 Event Sharing"];
  end

  subgraph JOBS["💼 Careers & Job Board"]
    JOBPOST["📝 Job Posting"];
    APPLY["🚀 Easy Apply"];
    TRACK["📊 Application Tracking"];
    RECOMMEND["🤝 Recommendations"];
    SAVEJOB["🔖 Saved Jobs"];
    REVIEW["👨‍💼 Admin Review"];
  end

  subgraph MARKET["🛒 Internal Marketplace"]
    FIXED["💰 Fixed Price"];
    AUCTION["🔨 Auction"];
    IMAGES["📸 Item Management"];
    APPROVAL["✅ Approval Workflow"];
    BIDS["💵 Bidding"];
    MSHARE["🔗 Marketplace Sharing"];
    SAVEITEM["🔖 Saved Items"];
  end

  HUB --> EVENTS;
  HUB --> JOBS;
  HUB --> MARKET;
```
  ---

## 👤 User Profiles and Networking

### 🪪 Profile Features

Each user has a detailed professional profile:

- 📋 **Basic info** - Name, title, bio, avatar, and cover photo.
- 🛠️ **Skills** - List technical and professional skills. Other users can endorse skills.
- 📜 **Certifications** - Certifications with issuing organization and dates.
- 🏆 **Achievements** - Professional accomplishments and milestones.
- 🎯 **Specializations** - Areas of deep expertise.
- 📚 **Teaching and learning** - Declare skills you can teach and skills you want to learn.
- 💬 **Profile feedback** - Colleagues can leave profile feedback or endorsement notes.
- 👁️ **Visibility controls** - Control which sections are public vs. private (bio, skills, certifications, achievements, etc.).
- 🏅 **Earned badges** - Display badges awarded by the platform.
- 📊 **Recent activity** - Show recent engagement (posts, events, reactions).

### 🤝 Social Connections

- ➕ **Follow system** - Follow other users to see their content in your feed.
- 🔒 **Follow requests** - Optionally require approval before someone can follow you.
- 👥 **Follower management** - Remove followers, accept or reject requests.
- 🚫 **Blocking** - Block users to prevent all interaction.
- 📋 **Connection lists** - View followers, following, and mutual connections.

### 🏅 Badge and Recognition System

Automated recognition system that rewards user engagement:

- 📊 **Metric-based rules** - Badges are awarded when users hit defined thresholds for:
  - 📝 Posts created
  - 💬 Comments made
  - 😍 Reactions received
  - 👍 Skills endorsed
  - 🤝 Connections gained
  - 💬 Feedback received
- ⏰ **Time-windowed rules** - Optionally limit metrics to a rolling time window (e.g., 10 posts in the last 30 days).
- 🎨 **Badge management** - Admins create badges with custom names, icons, and descriptions.
- 🔄 **Automatic recalculation** - Badges can be recalculated on demand.

---
```mermaid
flowchart LR
  PROFILE["👤 User Profile"] --> BASIC["📋 Basic Info"];
  PROFILE --> SKILLS["🛠️ Skills"];
  PROFILE --> CERTS["📜 Certifications"];
  PROFILE --> ACH["🏆 Achievements"];
  PROFILE --> SPEC["🎯 Specializations"];
  PROFILE --> TEACH["📚 Teach / Learn"];
  PROFILE --> FEEDBACK["💬 Profile Feedback"];
  PROFILE --> VIS["👁️ Visibility Controls"];
  PROFILE --> BADGES["🏅 Earned Badges"];
  PROFILE --> ACTIVITY["📊 Recent Activity"];

  PROFILE --> CONNECTIONS["🤝 Social Connections"];
  CONNECTIONS --> FOLLOW["➕ Follow"];
  CONNECTIONS --> REQUESTS["🔒 Follow Requests"];
  CONNECTIONS --> MANAGE["👥 Follower Management"];
  CONNECTIONS --> BLOCK["🚫 Blocking"];
  CONNECTIONS --> LISTS["📋 Connection Lists"];

  BADGES --> RULES["📊 Metric-Based Rules"];
  BADGES --> WINDOW["⏰ Time-Window Rules"];
  BADGES --> BADMIN["🎨 Badge Management"];
  BADGES --> RECALC["🔄 Recalculation"];
```
  ---

## ⚙️ Organization Administration

The admin panel gives organization administrators full control over their tenant:

### 👥 User Management
- ✉️ Invite new users by email (invitation link with password setup).
- ✏️ Edit user details, roles (Admin, Moderator, User), and status.
- ✅ Approve or deny access requests from users who request to join the organization.
- 🚫 Deactivate user accounts.
- 📡 Real-time monitoring via SSE stream for admin events.

### 📂 Group Management
- ➕ Create named user groups (e.g., Engineering, Marketing).
- 🔄 Add or remove members.
- 🎯 Groups are used for channel access, event invitations, and content targeting.

### 🛡️ Content Moderation
- ✅ Approve or reject marketplace listings before they go live.
- 📋 Review job postings.
- 👁️ Monitor feed activity across channels.

### 🔧 Organization Settings
- 📧 **Email notification settings** - Toggle notifications for comments, reactions, admin actions, weekly digest, and event invitations.
- ⚙️ **General settings** - Enable or disable platform features per organization (general feed, events, community, profiles, badges).
- 📋 **Audit logs** - Full audit trail of all admin actions within the organization.

---

## 🚀 Organization Onboarding

The process for a new organization to get started:

1. 📝 **Registration** - Submit organization details (name, owner email).
2. ✅ **Activation** - Organization owner receives an activation email with a secure token link.
3. 🔧 **Account setup** - Owner sets their password and configures initial settings.
4. ✉️ **Invitation** - Owner invites team members, who receive invitation emails with password setup links.
5. 📄 **License info** - Each organization has a license type (free, starter, business, enterprise) with associated user limits and feature sets.
6. 🎁 **Trial support** - Organizations can start with a trial period that includes full feature access.

---

## 🔐 Authentication and Security

### 🔑 Multi-Factor Authentication
- 📧 **Email-based MFA** - After successful login, a 6-digit code is sent to the user's email.
- ⏰ **Code expiry** - Codes expire after 10 minutes.
- 🔄 **Resend support** - Users can request a new code without restarting the login flow.

### 🔒 Password Management
- 🔑 **Forgot password** - Token-based password reset via email.
- ✏️ **Password change** - Authenticated users can change their password from their profile.
- 💪 **Password policy** - Enforced strength requirements (length, complexity).
- 🛡️ **Secure tokens** - Cryptographically random reset tokens with expiry.

### 🚪 Access Control
- 👤 **Role-based access** - Admin, Moderator, and User roles with different permission levels.
- 🏢 **Organization isolation** - Every API request is scoped to the authenticated user's organization.
- 📄 **License enforcement** - Access is blocked if the organization's license is expired.
- 🚫 **Account deactivation** - Suspended accounts cannot access any platform features.
- 🛡️ **Rate limiting** - Protection against brute-force login attempts.

---

## 🛡️ Privacy and GDPR Compliance

Full GDPR compliance built into the platform:

- ✅ **Consent management** - Track consent across four purposes:
  - 🔒 Essential (always required)
  - 📊 Analytics
  - 📢 Marketing
  - 📧 Communications
- ❌ **Consent withdrawal** - Users can withdraw consent per purpose at any time.
- 📦 **Data export** - Users can request a complete export of their personal data (delivered as a ZIP archive).
- 🗑️ **Account deletion** - Right to be forgotten: users can request complete account and data deletion.
- 📋 **Data Subject Requests (DSR)** - Track and manage export and deletion requests with status monitoring.
- 🍪 **Cookie consent banner** - GDPR-compliant cookie notice on first visit.
- 🖥️ **Privacy dashboard** - Dedicated page where users manage their consent, request exports, or initiate deletion.
- 📜 **Audit trail** - All consent changes are recorded in the audit log.

---

## 🔔 Notification System

Real-time notification system delivered via Server-Sent Events:

**Notification types:**
- 😍 Post reactions and comments
- 📅 Event invitations
- 💼 Job recommendations and application updates
- 🤝 Follow requests (new request, accepted)
- 💬 New direct messages
- 💰 Marketplace bids on your listings
- ✅ Access request decisions (approved/denied)
- ⚙️ Admin actions

**Features:**
- ⚡ Real-time push via SSE (no polling).
- ✅ Mark individual notifications as read.
- 📋 Mark all as read / mark all as unread.
- 🗑️ Delete all notifications.
- 🔄 Auto-sync on reconnection.
- 👤 Actor information shown (who triggered the notification).

---

## 📌 Bookmarks and Saved Items

Users can save content across the platform for later:

- 📰 **Saved posts** - Bookmark feed posts.
- 💼 **Saved jobs** - Bookmark job openings.
- 🛒 **Saved marketplace items** - Bookmark marketplace listings.
- 📂 **Organized by category** - Bookmarks are grouped by type on a dedicated page.
- 🧹 **Clear by category** - Bulk-clear bookmarks per category.

---

## 🐛 Bug Reporting and Support

Built-in bug reporting system accessible from within the application:

- 📝 Submit reports with title, description, and issue category (UI, data, performance, API, security, other).
- 📎 Attach up to 5 files (screenshots, logs), 20 MB each.
- 🔢 Each report generates a unique tracking ID.
- 📧 Reports are delivered via email to platform administrators.
- 💬 Optional Slack integration sends report summaries to a designated channel.

---

## 🔧 Maintenance Windows

Scheduled maintenance windows with user-facing communication:

- 📅 Define maintenance windows with start/end times, title, and description.
- 🚧 Active maintenance windows are shown to all users via a banner.
- 🌐 Public endpoint allows checking maintenance status without authentication.
- ✅ Completed maintenance windows show a post-maintenance message.

---

## 📧 Email Communication System

A centralized transactional email system with configurable themes:

**Supported email templates:**
- ✅ Account activation
- 🔑 Password reset
- 🔢 MFA verification code
- ✉️ User invitation
- 🏢 Organization invitation
- 🤝 Follow request notifications
- 📋 Access request decisions (approved/denied)
- 👋 Welcome messages
- ⚠️ Organization inactivity warnings and deletion notices
- 🔔 System alerts (background jobs, backups, security scans)

**Template features:**
- 🎨 Two base themes: **light** and **dark**, with per-template configuration.
- 🎲 **Random / A-B mode** - Randomly alternate between themes for experimentation.
- 👁️ Full preview and side-by-side comparison in the admin UI.
- 📤 SendGrid integration with inline image attachments (logo, social icons).

---

## ⏱️ Background Services

Automated background tasks run on configurable schedules:

| Service | Schedule | Description |
|---------|----------|-------------|
| 💾 Database Backup | Every 8 hours | Automated MySQL backups with retention and cleanup |
| 🔍 NPM Security Audit | Daily at 08:00 UTC | Scans frontend and backend dependencies for known vulnerabilities |
| 📄 License Check | Every hour | Validates organization license status and enforces restrictions |
| 🧹 Data Retention | Daily at 04:00 UTC | Cleans up expired data (old notifications, expired stories, stale tokens) |
| 📊 Organization Inactivity | Every hour | Detects inactive organizations and sends warning emails at 30/60/75/90-day thresholds |
| 🛡️ Security Advisory Sync | Hourly | Syncs npm security advisories from GitHub, evaluates impact against project lockfiles |

All jobs are configurable via environment variables and can be enabled or disabled per environment.

---

## 🏗️ Technical Architecture

### 🛠️ Technology Stack

| Layer | Technology |
|-------|------------|
| 🖥️ Backend | Node.js + Express + TypeScript |
| 🎨 Frontend | React 19 + TypeScript + Tailwind CSS 4 |
| 🗄️ Database | MySQL 8.0 (InnoDB, JSON column support) |
| ⚡ Build Tool | Vite 6 |
| 🔐 Authentication | JWT (JSON Web Tokens) + bcrypt |
| 📧 Email | SendGrid API + Handlebars templating |
| 📁 File Uploads | Multer (local filesystem, S3-compatible) |
| ⏰ Scheduling | node-cron |
| 🛡️ Security Headers | Helmet (CSP, HSTS, X-Frame-Options, Referrer-Policy) |
| 🎯 Icons | Lucide React + React Icons |

### 🏢 Multi-Tenancy Model

SpectraAgora uses a **single-database, shared-schema** multi-tenancy model:

- 🔑 Every table that holds tenant data includes an `organization_id` foreign key.
- 🔒 All API queries are scoped to the authenticated user's organization.
- 🛡️ Middleware enforces tenant boundaries before any business logic executes.
- 🚫 There is no cross-tenant data leakage by design.
- ⚙️ Organization-level settings (email, feature toggles) are stored per-tenant.

### ⚡ Real-Time Architecture

The platform uses **Server-Sent Events (SSE)** for real-time features:

- 🔔 **Notification stream** - Instant delivery of all notification types.
- 💬 **Message stream** - Real-time direct message delivery with typing indicators.
- ⚙️ **Admin stream** - Real-time admin panel updates (new access requests, settings changes).
- 💓 **Keepalive pings** - Periodic heartbeats to maintain connections through proxies.
- 🔄 **Auto-reconnection** - Clients automatically reconnect and sync missed events.

### 🔐 Security Architecture

```
🔒 Security Request Pipeline
═══════════════════════════════════════════════════════════

  👤 User Request
       │
       ▼
  ┌─────────────────────────────┐
  │ 🛡️  Helmet Security Headers │ ── CSP, HSTS, X-Frame-Options
  └─────────────┬───────────────┘
                │
                ▼
  ┌─────────────────────────────┐
  │ 🌐  CORS Validation         │ ── Origin whitelist
  └─────────────┬───────────────┘
                │
                ▼
  ┌─────────────────────────────┐
  │ 🔑  JWT Authentication      │ ── Token verification & expiry
  └─────────────┬───────────────┘
                │
                ▼
  ┌─────────────────────────────┐
  │ 👤  Role-Based Authorization │ ── Admin / Moderator / User
  └─────────────┬───────────────┘
                │
                ▼
  ┌─────────────────────────────┐
  │ 🏢  Organization Isolation   │ ── Tenant boundary enforcement
  └─────────────┬───────────────┘
                │
                ▼
  ┌─────────────────────────────┐
  │ ⚙️  Business Logic           │ ──► 📋 Audit Service
  └─────────────┬───────────────┘
                │
                ▼
  ┌─────────────────────────────┐
  │ 📤  Response                 │
  └─────────────────────────────┘
```

**Key security controls:**
- 🔒 All passwords hashed with bcrypt.
- 🎫 JWT tokens with configurable expiry.
- 🔑 MFA on login for all users.
- 🛡️ Rate limiting on authentication endpoints.
- 🔍 Request correlation IDs for audit tracing.
- 📋 Sensitive data access logging (GDPR Art. 30).
- 🔎 Automated security vulnerability scanning (npm audit + GitHub Security Advisories).

---

## 🗺️ Architecture Blueprints

### 📐 Blueprint 1: High-Level System Architecture

```
╔══════════════════════════════════════════════════════════════════════════╗
║                    🌐 SpectraAgora — System Overview                   ║
╠══════════════════════════════════════════════════════════════════════════╣
║                                                                          ║
║   👤 Users (Browser / Mobile)                                            ║
║        │                                                                 ║
║        ▼                                                                 ║
║   ┌──────────────────────────────────────────────┐                       ║
║   │          🎨 Frontend (React 19 + Vite 6)     │                       ║
║   │   ┌──────────┬──────────┬──────────────────┐ │                       ║
║   │   │  Feed UI │  Chat UI │  Admin Dashboard │ │                       ║
║   │   └──────────┴──────────┴──────────────────┘ │                       ║
║   │        Tailwind CSS 4  •  TypeScript         │                       ║
║   └──────────────────┬───────────────────────────┘                       ║
║                      │  HTTPS / REST API                                 ║
║                      ▼                                                   ║
║   ┌──────────────────────────────────────────────┐                       ║
║   │        🖥️ Backend (Node.js + Express)         │                       ║
║   │   ┌──────────────────────────────────────┐   │                       ║
║   │   │ 🔐 Auth    │ 📰 Feed    │ 💬 Chat    │   │                       ║
║   │   │ 📅 Events  │ 💼 Jobs    │ 🛒 Market  │   │                       ║
║   │   │ 👤 Profile │ 🔔 Notify  │ ⚙️ Admin   │   │                       ║
║   │   └──────────────────────────────────────┘   │                       ║
║   │     Middleware: JWT • CORS • Helmet • RBAC   │                       ║
║   └───────┬──────────────┬───────────────────────┘                       ║
║           │              │                                               ║
║           ▼              ▼                                               ║
║   ┌──────────────┐  ┌──────────────┐  ┌──────────────┐                   ║
║   │ 🗄️ MySQL 8.0 │  │ 📧 SendGrid  │  │ 📁 File Store│                   ║
║   │  (InnoDB)    │  │  (Email API) │  │ (Local / S3) │                   ║
║   └──────────────┘  └──────────────┘  └──────────────┘                   ║
║                                                                          ║
╚══════════════════════════════════════════════════════════════════════════╝
```

### 📐 Blueprint 2: Multi-Tenancy & Data Isolation

```
╔══════════════════════════════════════════════════════════════════════════╗
║              🏢 Multi-Tenancy — Shared Schema, Isolated Data            ║
╠══════════════════════════════════════════════════════════════════════════╣
║                                                                          ║
║   ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐         ║
║   │ 🏢 Org Alpha     │  │ 🏢 Org Beta      │  │ 🏢 Org Gamma    │         ║
║   │   org_id = 1     │  │   org_id = 2     │  │   org_id = 3    │         ║
║   │                  │  │                  │  │                 │         ║
║   │ 👤 Users (12)    │  │ 👤 Users (85)    │  │ 👤 Users (200)  │         ║
║   │ 📰 Posts (340)   │  │ 📰 Posts (1.2K)  │  │ 📰 Posts (5K)   │         ║
║   │ 💬 Messages      │  │ 💬 Messages      │  │ 💬 Messages     │         ║
║   │ 📅 Events        │  │ 📅 Events        │  │ 📅 Events       │         ║
║   │ ⚙️ Settings      │  │ ⚙️ Settings      │  │ ⚙️ Settings     │         ║
║   └────────┬────────┘  └────────┬────────┘  └────────┬────────┘         ║
║            │                    │                     │                   ║
║            ▼                    ▼                     ▼                   ║
║   ┌──────────────────────────────────────────────────────────────┐       ║
║   │                   🗄️ Shared MySQL Database                   │       ║
║   │                                                              │       ║
║   │  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐    │       ║
║   │  │  users   │  │  posts   │  │ messages │  │  events  │    │       ║
║   │  │ org_id ← │  │ org_id ← │  │ org_id ← │  │ org_id ← │    │       ║
║   │  └──────────┘  └──────────┘  └──────────┘  └──────────┘    │       ║
║   │                                                              │       ║
║   │  🔒 Every query includes WHERE organization_id = ?           │       ║
║   │  🛡️ Middleware enforces tenant scope before business logic    │       ║
║   └──────────────────────────────────────────────────────────────┘       ║
║                                                                          ║
╚══════════════════════════════════════════════════════════════════════════╝
```

### 📐 Blueprint 3: Real-Time Communication (SSE)

```
╔══════════════════════════════════════════════════════════════════════════╗
║              ⚡ Real-Time Architecture — Server-Sent Events              ║
╠══════════════════════════════════════════════════════════════════════════╣
║                                                                          ║
║   👤 User A (Browser)               👤 User B (Browser)                  ║
║        │                                  │                              ║
║        │  1. Open SSE Connection          │  1. Open SSE Connection      ║
║        ▼                                  ▼                              ║
║   ┌──────────────────────────────────────────────────────┐               ║
║   │                🖥️ Express Server                      │               ║
║   │                                                      │               ║
║   │   ┌────────────────────────────────────────────┐     │               ║
║   │   │        📡 SSE Connection Manager           │     │               ║
║   │   │                                            │     │               ║
║   │   │  Active Connections:                       │     │               ║
║   │   │   • /notifications/:userId  → 🔔 Alerts   │     │               ║
║   │   │   • /messages/:convId       → 💬 Chat     │     │               ║
║   │   │   • /admin/:orgId           → ⚙️ Admin    │     │               ║
║   │   └────────────────────────────────────────────┘     │               ║
║   │                     │                                │               ║
║   │                     ▼                                │               ║
║   │   ┌────────────────────────────────────────────┐     │               ║
║   │   │         📨 Event Dispatcher                │     │               ║
║   │   │                                            │     │               ║
║   │   │  2. User A sends message to User B         │     │               ║
║   │   │  3. Save to DB                             │     │               ║
║   │   │  4. Push SSE event → User B's connection   │     │               ║
║   │   │  5. Push notification → User B             │     │               ║
║   │   └────────────────────────────────────────────┘     │               ║
║   │                                                      │               ║
║   │   💓 Keepalive ping every 30s                        │               ║
║   │   🔄 Auto-reconnect on disconnect + sync missed      │               ║
║   └──────────────────────────────────────────────────────┘               ║
║                                                                          ║
╚══════════════════════════════════════════════════════════════════════════╝
```

### 📐 Blueprint 4: Database Entity Relationship Map

```
╔══════════════════════════════════════════════════════════════════════════╗
║               🗄️ Core Database Entity Relationships                     ║
╠══════════════════════════════════════════════════════════════════════════╣
║                                                                          ║
║                        ┌──────────────────┐                              ║
║                        │  🏢 Organization  │                              ║
║                        │  ──────────────── │                              ║
║                        │  id, name, slug   │                              ║
║                        │  license_type     │                              ║
║                        │  settings (JSON)  │                              ║
║                        └────────┬─────────┘                              ║
║            ┌────────────────────┼────────────────────┐                   ║
║            │                    │                    │                    ║
║            ▼                    ▼                    ▼                    ║
║   ┌────────────────┐  ┌────────────────┐  ┌────────────────┐            ║
║   │  👤 Users       │  │  📰 Channels   │  │  👥 Groups     │            ║
║   │  ────────────── │  │  ────────────── │  │  ────────────  │            ║
║   │  id, name, role │  │  id, name, type│  │  id, name     │            ║
║   │  email, avatar  │  │  visibility    │  │  members[ ]   │            ║
║   └──┬──────────┬──┘  └──────┬─────────┘  └──────────────┘            ║
║      │          │             │                                          ║
║      │          │             ▼                                          ║
║      │          │    ┌────────────────┐      ┌────────────────┐          ║
║      │          │    │  📝 Posts       │──►   │  💬 Comments   │          ║
║      │          │    │  ────────────── │      │  ────────────  │          ║
║      │          │    │  id, content   │      │  id, text     │          ║
║      │          │    │  type, media   │      │  post_id      │          ║
║      │          │    │  channel_id    │      └────────────────┘          ║
║      │          │    └───────┬────────┘                                  ║
║      │          │            │                                           ║
║      │          │            ▼                                           ║
║      │          │    ┌────────────────┐                                  ║
║      │          │    │  😍 Reactions   │                                  ║
║      │          │    │  ────────────── │                                  ║
║      │          │    │  type, user_id │                                  ║
║      │          │    └────────────────┘                                  ║
║      │          │                                                        ║
║      ▼          ▼                                                        ║
║  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐      ║
║  │💬 DMs    │ │📅 Events │ │💼 Jobs   │ │🛒 Market │ │🔔 Notifs │      ║
║  │──────────│ │──────────│ │──────────│ │──────────│ │──────────│      ║
║  │sender_id │ │title     │ │title     │ │title     │ │type      │      ║
║  │receiver  │ │date, loc │ │salary    │ │price     │ │actor_id  │      ║
║  │content   │ │rsvps[ ]  │ │apps[ ]   │ │bids[ ]   │ │read      │      ║
║  └──────────┘ └──────────┘ └──────────┘ └──────────┘ └──────────┘      ║
║                                                                          ║
╚══════════════════════════════════════════════════════════════════════════╝
```

---

### 🗃️ Database Design

Core entity relationships:

```
🏢 Organization
  ├── 👤 Users (role-based: Admin, Moderator, User)
  ├── 📰 Feed Channels (public / private)
  │     └── 📝 Posts (with reactions, comments, pins)
  ├── 📅 Events (with RSVPs, polls, invitations)
  ├── 💼 Jobs (with applications, recommendations)
  ├── 🛒 Marketplace Items (fixed-price / auction, with bids)
  ├── 👥 User Groups (for channel access, event invitations)
  ├── 🏅 Badges (metric-based, auto-awarded)
  ├── ⚙️ Organization Settings (email, general)
  └── 📋 Audit Logs (immutable action trail)

👤 User
  ├── 🪪 Profile (skills, certifications, achievements)
  ├── 📖 Stories (24h ephemeral content)
  ├── 💬 Messages (1-to-1 conversations)
  ├── 🔔 Notifications (real-time delivery)
  ├── 📌 Bookmarks (posts, jobs, marketplace)
  ├── 🛡️ GDPR Consent (per-purpose tracking)
  └── 🤝 Connections (followers / following / blocked)
```

---

## 🚢 Deployment and Infrastructure

### 📋 Prerequisites
- 🟢 Node.js v18+
- 🗄️ MySQL 8.0+

---

## 📄 License

Distributed under the Proprietary License. See `LICENSE` for more information.

---

<p align="center">
  **Built with ❤️ by the SpectraEYE Team**
</p>

