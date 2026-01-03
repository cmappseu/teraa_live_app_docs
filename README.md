# TeraLIVE - Complete Live Streaming & Social Platform

[![Flutter](https://img.shields.io/badge/Flutter-3.38.5-02569B?logo=flutter)](https://flutter.dev)
[![Node.js](https://img.shields.io/badge/Node.js-22.x-339933?logo=node.js)](https://nodejs.org)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-17-336791?logo=postgresql)](https://postgresql.org)
[![React](https://img.shields.io/badge/React-18.x-61DAFB?logo=react)](https://reactjs.org)
[![License](https://img.shields.io/badge/License-CodeCanyon-green)](https://codecanyon.net)

> **Build your own TikTok-style live streaming empire** - A production-ready Flutter live streaming app with Node.js backend, React admin panel, and agency dashboard. Perfect for creating video chat apps, live broadcasting platforms, and social streaming networks.

---

## Overview

**TeraLIVE** is a complete, full-stack **live streaming and social media platform** solution designed for entrepreneurs, startups, and developers who want to launch their own **TikTok clone**, **Bigo Live alternative**, or **live video streaming app**.

This all-in-one package includes everything you need: a beautiful **Flutter mobile application** for iOS and Android, a scalable **Node.js REST API** backend, a comprehensive **React admin dashboard**, and a dedicated **agency management panel**.

---

## What's Included

| Component | Technology | Description |
|-----------|------------|-------------|
| **Mobile App** | Flutter 3.38.5 | Cross-platform iOS & Android app with TikTok-style UI |
| **Backend API** | Node.js 22 + Express.js | RESTful API with Socket.IO real-time events |
| **Admin Panel** | React 18 + Vite | 50+ pages for complete platform management |
| **Agency Panel** | React 18 + Vite | Host management and earnings dashboard |
| **Database** | PostgreSQL 17 | Optimized schema with 25+ tables |
| **Documentation** | HTML | Step-by-step setup guides with 100+ screenshots |

---

## Key Features

### Live Streaming Features
- **HD Live Streaming** - Crystal clear video broadcasting with ZEGOCLOUD SDK
- **Voice Rooms** - 8-seat audio rooms with DJ mode and YouTube music integration
- **Party Rooms** - Multi-user video chat rooms for group streaming
- **Random Video Matching** - Omegle-style 1-on-1 video matching
- **PK Battles** - Streamer vs streamer live competition with real-time scoring
- **Private Rooms** - Premium paid entry rooms for exclusive content
- **Live Gifts** - Send and receive animated virtual gifts during streams

### Social Network Features
- **Social Feed** - Instagram-style posts with likes, comments, and shares
- **Stories** - 24-hour disappearing content
- **Direct Messaging** - Real-time private chat with media sharing
- **Follow System** - Follow/followers with activity feeds
- **User Profiles** - Customizable profiles with badges and achievements
- **Hashtags & Discovery** - Content discovery through hashtags and explore page

### Monetization System
- **Virtual Gift Economy** - 100+ animated gifts with Lottie and SVG animations
- **Coin Wallet** - In-app currency system with multiple coin packages
- **VIP Membership** - Tiered subscription system with exclusive perks
- **Agency System** - 5-tier agency structure with commission management
- **Host Earnings** - Transparent earnings tracking and withdrawal system
- **Diamond Exchange** - Convert gifts to withdrawable currency

### Gamification & Engagement
- **User Levels** - XP-based progression system (1-100)
- **Daily Tasks** - Engagement rewards for daily activities
- **Leaderboards** - Daily, weekly, and monthly rankings
- **Achievements** - Unlockable badges and rewards
- **Lucky Wheel** - Spin-to-win coin rewards
- **Family/Guild System** - 10-level clan system with group benefits

### Admin Panel Features
- **Real-time Dashboard** - Live statistics and analytics
- **User Management** - Ban, verify, VIP control, and user moderation
- **Gift Management** - Upload and manage virtual gifts
- **Room Monitoring** - Live room moderation and control
- **Transaction Reports** - Revenue and earnings analytics
- **Banner Management** - Promotional banners and announcements
- **Agency Management** - Approve and manage agencies
- **Content Moderation** - Report handling and content review
- **System Settings** - Platform-wide configuration

---

## Technical Specifications

### Mobile App (Flutter)
```
- Flutter SDK 3.38.5+ (Latest Stable)
- Dart 3.x
- State Management: GetX
- Video SDK: ZEGOCLOUD
- Push Notifications: Firebase Cloud Messaging
- Local Storage: Hive & SharedPreferences
- HTTP Client: Dio
- Animation: Lottie, Rive
- Image Processing: cached_network_image
- Architecture: Clean Architecture + MVC
```

### Backend API (Node.js)
```
- Node.js 22.x LTS
- Express.js 4.x
- Socket.IO 4.x (Real-time)
- PostgreSQL 17 (Database)
- JWT Authentication
- Multer (File Upload)
- Sharp (Image Processing)
- Node-cron (Scheduled Tasks)
- Winston (Logging)
- Helmet + CORS (Security)
```

### Admin & Agency Panels (React)
```
- React 18.x
- Vite 5.x (Build Tool)
- React Router 6
- Axios (HTTP Client)
- TailwindCSS (Styling)
- Chart.js (Analytics)
- React Query (Data Fetching)
- Zustand (State Management)
```

### Database Schema
```
- 25+ Optimized Tables
- Indexed Queries
- Foreign Key Relationships
- Soft Delete Support
- Audit Logging
- Migration Scripts
```

---

## Screenshots

### Mobile App
| Home Feed | Live Room | Voice Room | Profile |
|-----------|-----------|------------|---------|
| TikTok-style scroll | HD streaming with gifts | 8-seat audio room | User profile page |

### Admin Panel
| Dashboard | User Management | Gift Management | Reports |
|-----------|-----------------|-----------------|---------|
| Real-time stats | Full user control | Gift upload & edit | Revenue analytics |

---

## System Requirements

### Development Environment
- **Flutter SDK:** 3.38.5 or higher
- **Node.js:** 22.x LTS or higher
- **PostgreSQL:** 17.x or higher
- **npm/yarn:** Latest version
- **Android Studio:** For Android builds
- **Xcode:** For iOS builds (Mac only)

### Production Server
- **OS:** Ubuntu 22.04 LTS (Recommended)
- **RAM:** 4GB minimum, 8GB recommended
- **CPU:** 2 vCPU minimum, 4 vCPU recommended
- **Storage:** 50GB SSD minimum
- **Bandwidth:** Unlimited recommended

### Third-Party Services
- **ZEGOCLOUD:** Video/audio streaming SDK
- **Firebase:** Push notifications & authentication
- **Payment Gateway:** Stripe, PayPal, or local providers

---

## Installation

### Quick Start

1. **Clone and Setup Backend**
```bash
cd tera_live_api
cp .env.example .env
npm install
npm run migrate
npm start
```

2. **Setup Admin Panel**
```bash
cd tera_admin
cp .env.example .env
npm install
npm run dev
```

3. **Setup Mobile App**
```bash
cd tera_live
cp .env.example .env
flutter pub get
flutter run
```

### Detailed Documentation
Complete step-by-step installation guides are included in the `/documentation` folder with:
- Server deployment guide
- Firebase configuration
- ZEGOCLOUD setup
- Payment integration
- SSL certificate setup
- Domain configuration
- Troubleshooting guide

---

## Use Cases

TeraLIVE is perfect for building:

- **Live Streaming Platforms** - Like TikTok Live, Bigo Live, or Twitch
- **Video Chat Apps** - Random video matching like Omegle or Chatroulette
- **Social Networks** - Community platforms with live features
- **Dating Apps** - Video dating with live streaming
- **Entertainment Apps** - Talent shows and live performances
- **Gaming Platforms** - Game streaming with viewer interaction
- **E-commerce Live** - Live shopping and product demonstrations
- **Education Platforms** - Live tutoring and webinars
- **Religious Apps** - Live sermon streaming
- **Fitness Apps** - Live workout sessions

---

## Why Choose TeraLIVE?

| Feature | TeraLIVE | Competitors |
|---------|----------|-------------|
| Complete Solution | Full stack included | Often partial |
| Modern Tech Stack | Flutter 3.38 + Node 22 | Outdated versions |
| Real-time Features | Socket.IO built-in | Extra cost |
| Admin Panel | 50+ pages included | Basic or none |
| Agency System | 5-tier structure | Not available |
| Documentation | 100+ screenshots | Minimal docs |
| Code Quality | Clean & commented | Often messy |
| Support | 6 months included | Limited |

---

## Changelog

### Version 1.0.0 (January 2026)
- Initial release
- Flutter mobile app for iOS & Android
- Node.js REST API with Socket.IO
- React admin panel (50+ pages)
- React agency panel
- PostgreSQL database schema
- Complete documentation

---

## Support

We provide **6 months of support** including:
- Bug fixes and patches
- Installation assistance
- Configuration help
- General questions
- Response within 24-48 business hours

**Support does NOT include:**
- Customization requests
- Third-party integration
- Server management
- Feature additions

---

## Frequently Asked Questions

**Q: Is this a one-time purchase?**
A: Yes! Pay once and own the code forever. No recurring fees.

**Q: Can I resell this to my clients?**
A: With an Extended License, yes. Regular License is for single end-use only.

**Q: What streaming service does this use?**
A: ZEGOCLOUD SDK for reliable, low-latency video and audio streaming.

**Q: Is the code encrypted or obfuscated?**
A: No! You get 100% clean, readable, and editable source code.

**Q: Can I change the app name and branding?**
A: Absolutely! Full white-label customization is supported.

**Q: Do I need coding knowledge?**
A: Basic Flutter, Node.js, and React knowledge is recommended. Documentation covers setup.

---

## License

This project is licensed under the [CodeCanyon Regular/Extended License](https://codecanyon.net/licenses/standard).

- **Regular License:** Single end product, free or paid, not for resale
- **Extended License:** SaaS use, multiple end users, resale permitted

---

## Keywords

`live streaming app` `flutter live streaming` `tiktok clone` `bigo live clone` `video chat app` `voice room app` `flutter social app` `live video app` `streaming platform` `social media app` `flutter video call` `nodejs live streaming` `react admin panel` `live broadcast app` `video matching app` `omegle clone` `chatroulette clone` `live gifts app` `virtual gifts` `flutter app source code` `live streaming source code` `social app template` `video streaming flutter` `audio room app` `clubhouse clone` `twitter spaces clone` `live shopping app` `streamer app` `broadcaster app` `entertainment app` `flutter firebase` `socket.io app` `postgresql flutter` `zegocloud flutter` `agora alternative` `twilio alternative` `full stack app` `mobile app template` `ios android app` `cross platform app`

---

## Demo

**Live Demo:** [https://teraa.live](https://teraa.live)

**Demo Credentials:**
- User App: Download from demo site
- Admin Panel: Available on request

---

## Contact & Support

- **Developer:** [cmapps.eu](https://cmapps.eu)
- **Support Email:** destek@cmapps.com.tr
- **Documentation:** Included in package
- **Updates:** Free lifetime updates

---

<p align="center">
  <strong>TeraLIVE</strong> - The Complete Live Streaming Solution<br>
  Built with Flutter, Node.js, React & PostgreSQL<br>
  <br>
  Developed by <a href="https://cmapps.eu">cmapps.eu</a><br>
  <a href="https://codecanyon.net">Purchase on CodeCanyon</a>
</p>
