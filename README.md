# YardScout Showcase Website & Enthusiast Lead Engine

This directory contains the standalone, high-impact showcase and marketing landing page for **YardScout** ("Turn Salvage Rust Into Cold Cash").

---

## 🚀 Live Preview Options

1. **Standalone Portable File (Zero Dependencies):**
   - Simply double-click `index.html` (or run `Open YardScout Showcase.bat` on your Desktop) to open it in Chrome, Edge, or Brave.
   - Includes full offline interactivity, vehicle simulator HUD, and local lead storage in browser storage.

2. **Inside YardScout Server (FastAPI + SQLite + Docker):**
   - When running `app.py` or Docker, navigate to:
     - Showcase Site: `http://localhost:8080/showcase`
     - 2026 Profit Playbook: `http://localhost:8080/playbook`
     - Subscriber Hub & CSV Export: `http://localhost:8080/subscribers`

---

## 🌟 Key Features of the Showcase Site

### 1. Interactive Yard Simulation HUD ("Possibilities Live Simulator")
- Visitors can toggle between real vehicles:
  - **2008 Acura MDX Base 3.7L V6** (Bluetooth HFL, ELS Factory Amplifier, Master Window Switch)
  - **2004 Chevy Tahoe LT 5.3L V8** (LS PCM 12589463, Transfer Case Control Module, Climate Panel)
  - **2010 Toyota Prius Two 1.8L Hybrid** (Inverter Electric Coolant Pump, Combination Meter Cluster)
  - **2012 Honda Civic EX 1.8L i-VTEC** (Keihin Engine Control Module, Dual Tier Speedometer)
  - **2011 Dodge Ram 1500 Quad Cab 5.7L HEMI** (TIPM Fuse Box Module, Clock Spring Angle Sensor)
- Displays verified LKQ flat-rate pricing, recent eBay sold velocity, USPS Ground Advantage postage, net in-pocket profit, and ROI %.
- Includes required tools (e.g., Phillips #2, trim pry tool, 10mm socket, 6" extension), pull difficulty, and puller pro tips.
- **Dynamic Trip Ledger:** Automatically updates haul totals in real time (e.g. `3 Targets Pulled = +$315 In-Pocket Profit`) with full cost vs. revenue breakdown.

### 2. The 4 Pillars Breakdown
Visual showcase featuring real Android application screenshots:
1. **Pillar 01: Barcode & Optical Scanner HUD** - Sub-second VIN scanner with laser reticle tuned for dusty door jambs and harsh yard sunlight.
2. **Pillar 02: LKQ vs. eBay Arbitrage Engine** - Instant margin calculation deducting yard fees, eBay category commission, and USPS shipping.
3. **Pillar 03: 100% Offline Yard Vault** - SQLite local database built specifically for remote pick-and-pull yards with zero cellular signal.
4. **Pillar 04: Live Haul Ledger** - Real-time running tally of parts pulled, total cashier cost, and net flip profit before leaving the yard.

### 3. Built-in Lead Magnet: "The 2026 Junkyard Profit Playbook"
- Field manual detailing **30 under-the-radar OEM electronics and modules** under $25 at LKQ that sell for $100–$300+ on eBay.
- Accessible online via `playbook.html` or `/playbook`, styled with print-friendly CSS for instant PDF saving.
- Validates user email, logs to `yard_scout.db` (or `localStorage`), and delivers immediate digital access.

### 4. Google Play Closed Alpha Tester Guide
- Direct onboarding track for package `com.radday.yardscout` (v1.0.0.1 Closed Alpha, Build 4).
- 3-step instructions for Android users to join the testing roster and install the app.

---

## 💌 Email Marketing Integration (MailerLite & Beehiiv)

Both platforms offer generous free tiers with clean mobile delivery and automated welcome sequences:
- **MailerLite:** Free up to 1,000 subscribers.
- **Beehiiv:** Free up to 2,500 subscribers.

### How to Export & Sync Your Subscribers (1-Click)

#### From the FastAPI Server:
1. Navigate to `http://localhost:8080/subscribers`
2. Click **"📥 Export CSV for MailerLite / Beehiiv"** (or hit `/api/subscribers/export`).
3. You will receive `yardscout_subscribers.csv` formatted with columns: `email`, `name`, `interest`, `source`, `created_at`.

#### From the Standalone Website (`index.html`):
1. In the footer, click **"🔒 Lead Admin & Export"** (or use the admin modal).
2. Click **"📥 Download CSV"** to immediately save all captured browser leads.

### Step-by-Step Setup Guide

#### Option A: MailerLite (Recommended for High Deliverability)
1. Sign up for free at [MailerLite.com](https://www.mailerlite.com).
2. Go to **Subscribers** ➔ **Add Subscribers** ➔ **Import from CSV**.
3. Upload `yardscout_subscribers.csv` and map the fields (`Email`, `Name`, `Interest`).
4. Go to **Automations** ➔ **Create Automation**:
   - **Trigger:** When a subscriber joins your group.
   - **Action:** Send Welcome Email (use template below).

#### Option B: Beehiiv (Recommended for Newsletter & Community)
1. Sign up for free at [Beehiiv.com](https://www.beehiiv.com).
2. Go to **Audience** ➔ **Subscribers** ➔ **Import Subscribers**.
3. Upload `yardscout_subscribers.csv`.
4. Under **Settings** ➔ **Publication** ➔ **Welcome Email**, configure your automatic greeting.

### Copy-and-Paste Welcome Email Template

```text
Subject: 🛠️ [Playbook Inside] Welcome to YardScout & Your Alpha Invite

Hey {name|there},

Welcome to the YardScout insider roster!

As promised, here is your digital access to the field manual:
👉 The 2026 Junkyard Profit Playbook: https://radday5.github.io/yardscout/playbook.html
(Tip: Hit Ctrl+P or the "Print / Save PDF" button at the top to save it to your phone).

Inside, you'll find 30 OEM modules under $25 at LKQ that flip for $100-$300+ on eBay—plus the 8-item minimal tool kit to carry in your pack.

Google Play Closed Alpha Status:
We are currently rolling out closed test builds for YardScout v1.0.0.1 (Build 4). We have queued your email ({email}) into the developer whitelist. Keep an eye out for a direct Google Play Store invitation link from Google Play.

In the meantime, what's your favorite salvage yard to wrench at? Just hit reply and let me know!

Best,
The YardScout Crew
"Turn Salvage Rust Into Cold Cash"
```

---

## 🌐 1-Click Free Web Hosting Options

### 1. GitHub Pages (Free, Zero Maintenance)
1. Create a repository on GitHub named `yardscout`.
2. Push the contents of this `website/` directory to the repository (or branch `gh-pages`).
3. In GitHub Settings ➔ **Pages** ➔ set branch to `main` and folder to `/`.
4. Your site is instantly live at:
   `https://radday5.github.io/yardscout/`

### 2. Cloudflare Pages (Free, Lightning Fast)
1. In Cloudflare Dashboard ➔ **Workers & Pages** ➔ **Create application** ➔ **Pages** ➔ **Upload assets**.
2. Drag and drop this `website/` folder.
3. You will receive an instant custom URL like `yardscout.pages.dev` with automatic SSL and DDoS protection.

### 3. Docker (Local or VPS Deployment)
Run with Docker Compose:
```bash
docker compose up --build -d
```
The server will bind to port `8080` with the `/showcase`, `/playbook`, and `/subscribers` routes live.
