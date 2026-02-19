# 🏠 Rentora BD

> Bangladesh's most trusted AI-powered room rental platform. Built with React, designed for the future.

---

## 📸 Screenshots

### 🏠 Home Page

![Home Page](./screenshots/RentRoom_BD.png)

### 🛏️ Rooms Page — AI Search & Filter

![Rooms Page](./screenshots/RentRoom_BD__1_.png)

### 🗺️ Map View

![Map View](./screenshots/RentRoom_BD__2_.png)

### 💬 Chat System

![Chat](./screenshots/RentRoom_BD__3_.png)

---

## 🚀 Live Preview Features

### 🔍 Smart Search & Filter

- Real-time search by name or area
- Filter by: Dhanmondi, Mirpur, Gulshan, Banani, Mohammadpur, Azimpur
- Room type filter: Single / Shared / Studio
- **Advanced panel:** Budget range (৳), Amenities, Gender preference, Availability
- Sort: Price Low→High, High→Low, Top Rated

### 🤖 AI Features

- **"Best Match For You"** — 94% match score with progress bar
- **AI Price Insight** — "This listing is 8% below market average"
- **AI Profile Insights** in Dashboard — personalized suggestions
- AI fraud detection & description generator _(backend ready)_

### 💬 Real-time Chat System

- Landlord ↔ Tenant direct messaging
- Live typing indicator (animated dots)
- File sharing button (📎)
- Contact list with online status

### 🔐 Auth System

- Google OAuth button
- Facebook OAuth button
- Email + Password login/register
- Forgot password flow

### 📅 Booking System

- Booking request with status: **Approved / Pending / Rejected**
- Digital agreement signing button (📝)
- Room availability display

### ❤️ Wishlist & Notifications

- Heart button on every room card
- Wishlist count badge in navbar
- 🔔 Notification bell with unread count
- Notification dropdown with timestamps

### 📊 Dashboard

- Stats: Saved Rooms, Bookings, Messages, Profile Score
- Tabs: Overview | Bookings | Wishlist
- AI insights panel

### 🗺️ Map View

- Price heatmap UI
- Near Universities filter
- Metro station proximity
- Area price markers

### 🌙 Dark Mode

- Full dark/light toggle — every component themed

### ⭐ Reviews & Ratings

- Tenant review cards
- Star ratings
- Verified stay badges

---

## 🛠️ Tech Stack (Current — Frontend Only)

| Layer        | Technology                          |
| ------------ | ----------------------------------- |
| UI Framework | React 18 (Hooks)                    |
| Styling      | CSS-in-JS (custom design system)    |
| Fonts        | Sora + DM Sans (Google Fonts)       |
| Icons        | Emoji-based (no dependency)         |
| State        | React Context API                   |
| Routing      | `page` state (swap to React Router) |

---

## ⚙️ Recommended Full Stack (2025 Standard)

```
Frontend:          Next.js 14+ / TypeScript / TailwindCSS
Backend:           Django 5+ / DRF / PostgreSQL
Cache:             Redis
Background Tasks:  Celery
Auth:              JWT + OAuth (Google, Facebook)
Payments:          SSLCommerz + bKash/Nagad + Stripe
Maps:              OpenStreetMap (Leaflet.js)
Real-time Chat:    Django Channels (WebSocket)
Deployment:        Docker + Nginx + GitHub Actions CI/CD
Hosting:           AWS / DigitalOcean
```

---

## 📁 File Structure

```
rent-room/
├── src/
│   ├── context/
│   │   └── AppContext.jsx       ← Global state (rooms, user, darkMode, wishlist)
│   ├── data/
│   │   └── mockData.js          ← Mock data (replace with API later)
│   ├── components/
│   │   ├── Navbar/
│   │   ├── RoomCard/
│   │   ├── RoomModal/
│   │   ├── SearchFilter/
│   │   ├── ChatWindow/
│   │   ├── AIRecommendations/
│   │   └── Footer/
│   ├── pages/
│   │   ├── Home/
│   │   ├── Rooms/
│   │   ├── Map/
│   │   ├── Chat/
│   │   ├── Dashboard/
│   │   └── Auth/
│   ├── styles/
│   │   └── global.css
│   └── App.jsx
├── public/
└── package.json
```

---

## 🔌 Backend API Endpoints (To Build)

```
Authentication:
  POST /api/auth/register/
  POST /api/auth/login/
  POST /api/auth/google/
  POST /api/auth/refresh/

Rooms:
  GET  /api/rooms/              ← list + filter + search
  POST /api/rooms/              ← create listing
  GET  /api/rooms/:id/          ← single room detail
  PUT  /api/rooms/:id/          ← update listing
  DEL  /api/rooms/:id/          ← delete listing

Bookings:
  POST /api/bookings/           ← create booking request
  GET  /api/bookings/mine/      ← my bookings
  PUT  /api/bookings/:id/       ← approve/reject

Chat:
  GET  /api/chat/conversations/
  POST /api/chat/messages/
  WS   /ws/chat/:room_id/       ← WebSocket

Reviews:
  POST /api/reviews/
  GET  /api/reviews/?room=:id

Payments:
  POST /api/payments/initiate/   ← SSLCommerz
  POST /api/payments/verify/
```

---

## 💳 Payment Integration Plan

```python
# SSLCommerz (Bangladesh)
pip install sslcommerz-python

# bKash API
# Nagad API

# Stripe (International)
pip install stripe
```

---

## 🚀 Quick Start

```bash
# Clone
git clone https://github.com/SadManFahIm/Rentora.git
cd Rentora

# Dependencies install
npm install

# Run
npm start
```

---

## 📦 Required npm Packages (Full Version)

```bash
npm install react-router-dom axios leaflet react-leaflet \
            framer-motion zustand react-query \
            @headlessui/react react-hook-form \
            date-fns socket.io-client
```

---

## 🗓️ Development Roadmap

| Phase   | Features                             | Status       |
| ------- | ------------------------------------ | ------------ |
| Phase 1 | UI/UX + Search + Filter + Dark Mode  | ✅ Done      |
| Phase 2 | Auth (JWT + OAuth) + Dashboard       | ✅ Done (UI) |
| Phase 3 | Django Backend + PostgreSQL + API    | 🔧 Next      |
| Phase 4 | Chat (WebSocket) + Notifications     | 🔧 Next      |
| Phase 5 | Payment (SSLCommerz + bKash)         | 📋 Planned   |
| Phase 6 | AI Features (Recommendation + Fraud) | 📋 Planned   |
| Phase 7 | Map (Leaflet.js + Heatmap)           | 📋 Planned   |
| Phase 8 | Docker + CI/CD + Deployment          | 📋 Planned   |

---

## 👨‍💻 Author

- **[@SadManFahIm](https://github.com/SadManFahIm)**
- Original Stack: React 16 + Contentful CMS
- Upgraded to: React 18 + Custom Design System

---

## 📄 License

MIT License — Free to use and modify.
