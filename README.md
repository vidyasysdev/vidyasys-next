# VIDYASYS (ACAVORA) — Polytechnic Academic Ecosystem & Marketplace

A modern, student-focused academic ecosystem and marketplace connecting diploma engineering and polytechnic college students (MSBTE I & K Schemes, Vidyalankar Polytechnic, GPM, VJTI, etc.) to senior notes, hardware kits, peer tutoring, and campus ambassador order fulfillment.

Built with **Next.js 15 (App Router)**, **React 19**, **Tailwind CSS v4**, and **Lucide Icons**.

---

## 🚀 Getting Started

### 1. Prerequisites
- **Node.js** 18.17+ or 20+ installed
- Windows PowerShell / Bash terminal

### 2. Install Dependencies
```bash
npm install
```
*(On Windows PowerShell, use `npm.cmd install` if script execution policies apply)*

### 3. Run Development Server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

### 4. Build for Production
```bash
npm run build
npm run start
```

---

## 📁 Project Architecture (Next.js App Router)

```text
├── src/
│   ├── app/                               # Next.js 15 App Router Routes
│   │   ├── layout.tsx                     # Root Server Layout with metadata & Plus Jakarta Sans
│   │   ├── globals.css                    # Tailwind CSS v4 styling & dark mode variants
│   │   ├── page.tsx                       # Home page (/)
│   │   ├── notes/page.tsx                 # MSBTE Diploma Notes (/notes)
│   │   ├── projects/page.tsx              # Hardware Projects & Capstone Kits (/projects)
│   │   ├── tutors/page.tsx                # Senior Peer Tutors (/tutors)
│   │   ├── dashboard/page.tsx             # Student Dashboard & Order tracking (/dashboard)
│   │   ├── contributor-studio/page.tsx    # Contributor Studio for listings (/contributor-studio)
│   │   ├── college-partnership/page.tsx   # Polytechnic Campus Partnership (/college-partnership)
│   │   ├── about/page.tsx                 # About VIDYASYS & Founders (/about)
│   │   ├── trust-safety/page.tsx          # Trust, Safety & Academic Integrity (/trust-safety)
│   │   ├── admin/page.tsx                 # Super Admin & Ambassador Console (/admin)
│   │   └── messages/page.tsx              # Campus Direct Peer Messages (/messages)
│   ├── components/
│   │   ├── cards/                         # NoteCard, ProjectCard, TutorCard
│   │   ├── common/                        # Navbar, Footer, BottomNav, ClientLayout, Logo, Toast, Modals
│   │   └── modals/                        # NotePreviewModal, ProjectDetailModal, TutorBookingModal, AuthModal, NextExportModal
│   ├── views/                             # Full interactive view components
│   ├── context/
│   │   └── AppContext.tsx                 # Global state, cart, orders, role switching, SSR-safe localStorage sync
│   ├── data/
│   │   └── mockData.ts                    # Realistic MSBTE colleges, branches, notes, hardware, tutors
│   ├── types/
│   │   └── index.ts                       # Complete TypeScript interfaces
│   └── utils/
│       └── currency.ts                    # INR currency formatter (₹)
├── public/
│   ├── acavora-logo.svg
│   ├── vidyasys-logo.svg
│   └── images/logo.png
├── package.json
├── next.config.ts
├── tsconfig.json
└── postcss.config.mjs
```

---

## 🌟 Key Features

1. **Diploma & Polytechnic Focus**: Pre-configured with MSBTE I & K Schemes, Semesters 1 to 6, and Branches (Computer, IT, Mechanical, Electrical, Civil, Electronics).
2. **Campus Order Tracking & OTP Handovers**:
   - Order Placed ➔ Assigned to College Ambassador ➔ Packed ➔ In Transit ➔ Campus Pickup (Library/Canteen) ➔ Completed via 4-digit OTP.
3. **Role Switching**:
   - Switch live between **Admin (Super Admin - Raj Bhosale)**, **Faculty Moderator**, **College Brand Ambassador**, and **Student Scholar**.
4. **Interactive Modals**:
   - PDF Note Viewer with Table of Contents & sample pages
   - Hardware Bill of Materials (BOM) & difficulty tags
   - Tutor slot booking with Google Meet & campus physical locations
   - Escrow checkout & student wallet balance
5. **Theme Support**: Seamless dark mode and light mode with system preference detection and localStorage persistence.
6. **Zero Hydration Mismatches**: Safe SSR architecture with client hydration after mount.
