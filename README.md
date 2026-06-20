# 🚂 IndianRail — Railway Reservation System

<div align="center">

![IndianRail Banner](https://images.unsplash.com/photo-1474487548417-781cb71495f3?w=1200&h=300&fit=crop&q=80)

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Font Awesome](https://img.shields.io/badge/Font_Awesome-528DD7?style=for-the-badge&logo=font-awesome&logoColor=white)](https://fontawesome.com)

**A fully responsive, modern Indian Railway Reservation System built with pure HTML, CSS & JavaScript.**

[🏠 Home](#) · [🚆 Train Search](#) · [🎫 Book Ticket](#) · [🔍 PNR Status](#)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Pages](#-pages)
- [Train Database](#-train-database)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)

---

## 🌟 Overview

**IndianRail** is a front-end simulation of the Indian Railway online reservation system (IRCTC). It provides a rich, dark-themed UI inspired by modern travel booking platforms — with 144+ real Indian trains, complete ticket booking flow, PNR status tracking, and a full login/signup system. Everything runs entirely in the browser with no backend required, using `localStorage` to persist session data.

> Built as a showcase of real-world UI/UX design using only vanilla web technologies.

---

## ✨ Features

### 🔐 Authentication
- Login / Sign Up modal with form validation
- Session persistence via `localStorage`
- User greeting shown in the navbar after login
- Login state carried across all pages

### 🔎 Train Search
- Search by **From** and **To** station (partial match supported)
- Filter by train **category** — Rajdhani, Shatabdi, Vande Bharat, Duronto, Superfast, Express
- Filter by **travel class** — SL, 3A, 2A, 1A, CC, 2S
- Live train count display
- **Paginated results** — 20 trains per page with "Load More"

### 🎫 Ticket Booking
- Displays selected train details (name, number, timings, route)
- Class selection with live fare calculation
- Up to **6 passengers** per booking with berth preferences
- Quota selection — General, Ladies, Senior Citizen, Tatkal, Premium Tatkal
- Payment method selection — UPI/GPay, Card, Net Banking, IRCTC Wallet
- GST (5%), reservation charge, and service fee breakdown
- **Instant PNR generation** on confirmation
- Animated booking success screen

### 📋 PNR Status
- Look up any PNR number (real bookings stored in `localStorage`)
- Demo mode — any unknown PNR shows a realistic result
- Per-passenger seat/berth/coach assignment
- Full journey timeline display
- **Recent Bookings** history panel with one-click re-check

### 🎨 UI/UX
- Deep navy dark theme with gradient accents
- Fully responsive — works on mobile, tablet, and desktop
- Smooth hover animations and transitions
- Sticky navigation bar
- Real-time fare calculator
- Font Awesome icons throughout

---

## 📄 Pages

| Page | File | Description |
|------|------|-------------|
| **Home** | `index.html` | Hero section with train search, stats bar, feature cards, login/signup modals |
| **Train Search** | `train.html` | Full train listing with search, filters, class badges, and booking |
| **Book Ticket** | `booking.html` | Complete booking form — passengers, class, payment, and confirmation |
| **PNR Status** | `pnr.html` | PNR lookup, passenger status table, booking history |

---

## 🚆 Train Database

The system includes **144+ real Indian trains** spanning all major categories and routes:

| Category | Count | Examples |
|----------|-------|---------|
| 🟣 Rajdhani Express | 20+ | Howrah Rajdhani, Mumbai Rajdhani, Trivandrum Rajdhani |
| 🟢 Shatabdi Express | 12+ | Bhopal Shatabdi, Kalka Shatabdi, Chennai Shatabdi |
| 🟡 Vande Bharat Express | 3+ | Delhi–Varanasi, Delhi–Jammu, Mumbai–Gandhinagar |
| 🔴 Duronto Express | 8+ | Sealdah Duronto, Mumbai Duronto, Howrah Duronto |
| 🟠 Superfast Express | 40+ | Tamil Nadu Exp, Kerala Exp, Karnataka Exp, Punjab Mail |
| 🔵 Express | 35+ | Golden Temple Mail, Kalka Mail, Goa Express, Himsagar |
| 🩵 Garib Rath | 3+ | Gorakhpur Garib Rath, Saharsa Garib Rath |

**Notable trains included:**
- 🏆 **Vivek Express** (15905) — longest railway route in India (Dibrugarh → Kanyakumari, 82h 30m)
- 🏆 **Himsagar Express** (16317) — second longest route (Jammu Tawi → Kanyakumari, 71h)
- 🏆 **Gatimaan Express** (12049) — India's fastest train (Delhi → Agra in 1h 40m)
- 🏆 **Rapti Sagar Express** (12521) — 80h 05m journey (Barauni → Ernakulam)

---

## 🛠 Tech Stack

| Technology | Purpose |
|-----------|---------|
| **HTML5** | Page structure and semantic markup |
| **CSS3** | Styling, animations, grid/flexbox layouts |
| **Vanilla JavaScript (ES6+)** | All interactivity, data rendering, routing |
| **localStorage API** | Session management, booking persistence |
| **Font Awesome 6.5** | Icon library (CDN) |
| **CSS Backdrop Filter** | Glassmorphism effects on modals and cards |
| **CSS Grid** | Train card and booking layout |

> **No frameworks. No build tools. No dependencies to install.**

---

## 📁 Project Structure

```
projects/
│
├── index.html        # Home page — hero, search, login/signup
├── train.html        # Train search results with 144+ trains
├── booking.html      # Ticket booking form and confirmation
├── pnr.html          # PNR status checker and history
└── README.md         # This file
```

---

## 🚀 Getting Started

### Prerequisites

All you need is a modern web browser. No server, no Node.js, no installation required.

### Running Locally

**Option 1 — Open directly**
```
Double-click index.html
```

**Option 2 — VS Code Live Server**
1. Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension
2. Right-click `index.html` → **Open with Live Server**

**Option 3 — Python HTTP server**
```bash
# Python 3
python -m http.server 8000

# Then open: http://localhost:8000
```

**Option 4 — Node.js**
```bash
npx serve .
```

---

## 📖 Usage

### Booking a Ticket

1. Open `index.html` — enter **From**, **To** station and a **date**, click **Search**
2. On the train list, use filters to narrow results by type or class
3. Click a **class badge** (e.g. `3A ₹2080`) or **Book Now** on any train card
4. Fill in **passenger details**, select **payment method**, review **fare summary**
5. Click **Confirm & Pay** — a PNR number is generated instantly
6. You're redirected to the **PNR Status** page automatically

### Checking PNR

1. Navigate to `pnr.html`
2. Enter your **10-digit PNR number** and click **Check Status**
3. Your booking history is shown below for quick re-check

### Login / Sign Up

1. Click **Login / Sign Up** in the top-right navbar
2. Enter credentials — your name/email is saved to `localStorage`
3. Your username appears in the navbar and persists across all pages

---

## 🗺 Page Flow

```
index.html (Search)
     │
     ▼
train.html (Results + Filters)
     │
     ▼ (click Book Now / class badge)
booking.html (Passenger details + Payment)
     │
     ▼ (after confirmation)
pnr.html (PNR Status + History)
```

---

## 🔒 Data & Privacy

All data in this project is stored **locally in your browser** via `localStorage`. No data is sent to any server. Clearing browser data resets all bookings and login state.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/add-seat-map`
3. Commit your changes: `git commit -m 'Add seat map view'`
4. Push to the branch: `git push origin feature/add-seat-map`
5. Open a Pull Request

### Ideas for Enhancement
- [ ] Interactive seat/berth map
- [ ] Train running status with live delay simulation
- [ ] Cancellation and refund flow
- [ ] Print / download e-ticket as PDF
- [ ] Dark/light mode toggle
- [ ] Station autocomplete with full IRCTC station list
- [ ] Multi-city journey planner

---

## 📞 Railway Helpline Numbers

| Service | Number |
|---------|--------|
| General Enquiry | **139** |
| Security / Emergency | **182** |
| Vigilance Helpline | **1800-111-321** |
| Medical Emergency | **138** |

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<div align="center">

**Made with ❤️ for Indian Railways**

*© 2024 IndianRail — Ministry of Railways, Government of India (Simulation)*

⭐ Star this repo if you found it useful!

</div>
