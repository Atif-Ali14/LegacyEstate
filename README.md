---

# 🏠 LegacyEstate – Premium Real Estate Platform

[![Built with Next.js](https://img.shields.io/badge/Next.js-16-blue?style=flat-square&logo=nextdotjs)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19-blue?style=flat-square&logo=react)](https://reactjs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-v4-blue?style=flat-square&logo=tailwind-css)](https://tailwindcss.com/)
[![Supabase](https://img.shields.io/badge/Supabase-PostgreSQL-green?style=flat-square&logo=supabase)](https://supabase.com/)
[![License](https://img.shields.io/badge/License-CipherDevs-blue?style=flat-square)](#license)

**LegacyEstate** is a modern, feature-rich real estate platform connecting property owners, dealers, and potential buyers or renters across UK.

---

## 🌟 Features

### 🔒 Authentication & User Management

- Secure **email/password login**
- **Roles**:
  - 👤 **Regular Users** – Browse listings, save favorites, contact dealers
  - 🏢 **Dealer Users** – Manage listings (add/edit/delete)
  - 🛡 **Admin Users** – Approve/reject listings, manage content

### 🏡 Property Listings

- Types: **House, Apartment, Plot, Commercial**
- Detailed info: bedrooms, bathrooms, furnishing, price, location
- Multiple images per listing 📸
- Status tracking: **Available / Sold / Rented**

### 🔍 Search & Discovery

- Advanced filtering: property type, city, area, price, bedrooms, furnishing
- Sorting options: price (low → high, high → low), latest listings
- Fully **responsive design** for all devices 📱💻

### 📞 Communication

- Direct dealer contact via **phone/email**
- User & dealer profiles with agency info 🏢
- Save properties as **favorites** ❤️

### 🛠 Administration

- Listing approvals by admin ✅
- Content management for dealers and admins ✏️🗑

---

## 🛠 Tech Stack

| Layer    | Technology                       |
| -------- | -------------------------------- |
| Frontend | Next.js 16, React 19, TypeScript |
| Styling  | Tailwind CSS v4                  |
| Backend  | Supabase (PostgreSQL)            |
| Auth     | Supabase Auth                    |
| Storage  | Supabase Storage (images)        |

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- Supabase account

### Installation

```bash
# Clone the repo
git clone https://github.com/CipherDevsLabs/LegacyEstate.git
cd LegacyEstate

# Install dependencies
npm install

# Create .env.local with your Supabase keys
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_anon_key

# Start dev server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 📂 Project Structure

```
LegacyEstate/
├── src/
│   ├── app/
│   │   ├── page.tsx       # Home page
│   │   ├── login/         # Login
│   │   ├── signup/        # Signup
│   │   ├── properties/    # Property details & new
│   │   ├── dashboard/     # Dealer dashboard
│   │   ├── admin/         # Admin panel
│   │   └── profile/       # User profile
│   ├── components/        # Reusable UI components
│   ├── lib/               # Supabase client & auth utilities
│   └── types/             # TypeScript types
```

---

## 👥 User Roles

| Role             | Capabilities                                                         |
| ---------------- | -------------------------------------------------------------------- |
| **Regular User** | Browse approved listings, save favorites, contact dealers            |
| **Dealer**       | All Regular features + add/edit/delete properties, view status       |
| **Admin**        | All Dealer features + approve/reject listings, manage all properties |

---

## ⚡ Build & Deployment

### Build for production

```bash
npm run build
npm start
```

### Deploy to Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

---

## 🗄 Database Schema

- **profiles** – User profile info
- **properties** – Property listings
- **property_images** – Multiple images per property
- **contacts** – Track user-dealer communications
- **favorites** – Saved properties

**Security:**

- Row Level Security (RLS) enabled
- Role-based access control: user, dealer, admin
- Secure image storage
