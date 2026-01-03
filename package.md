# CodeCanyon Paketleme Rehberi

---

## ADIM 1: Klasör Yapısını Oluştur

Masaüstünde veya istediğin bir yerde boş bir klasör oluştur:

```
C:\CodeCanyon_Package\
│
├── documentation\
└── source_code\
    ├── tera_live\
    ├── tera_live_api\
    ├── tera_admin\
    └── tera_agency\
```

**Windows CMD:**
```cmd
mkdir C:\CodeCanyon_Package
mkdir C:\CodeCanyon_Package\documentation
mkdir C:\CodeCanyon_Package\source_code
```

---

## ADIM 2: Dokümantasyon Dosyalarını Kopyala

`codecanyon` klasöründeki HTML dosyalarını `documentation` klasörüne kopyala:

### Kopyalanacak HTML'ler:
| Kaynak | Hedef |
|--------|-------|
| `C:\Projects\codecanyon\teralive_documentation.html` | `documentation\index.html` |
| `C:\Projects\codecanyon\teralive_app.html` | `documentation\app.html` |
| `C:\Projects\codecanyon\teralive_admin.html` | `documentation\admin.html` |
| `C:\Projects\codecanyon\teralive_agency.html` | `documentation\agency.html` |
| `C:\Projects\codecanyon\teralive_api.html` | `documentation\api.html` |

### Kopyalanacak Screenshot Klasörleri:
| Kaynak | Hedef |
|--------|-------|
| `C:\Projects\codecanyon\appscreens\` | `documentation\appscreens\` |
| `C:\Projects\codecanyon\adminscreens\` | `documentation\adminscreens\` |
| `C:\Projects\codecanyon\agencyscreens\` | `documentation\agencyscreens\` |

---

## ADIM 3: Kaynak Kodları Temizle ve Kopyala

### 3.1 Flutter App (tera_live)

**Önce temizle:**
```bash
cd C:\Projects\tera_live
flutter clean
```

**Silinecek dosya/klasörler:**
```
tera_live\.dart_tool\          (SİL)
tera_live\build\               (SİL)
tera_live\.flutter-plugins     (SİL)
tera_live\.flutter-plugins-dependencies  (SİL)
tera_live\ios\Pods\            (SİL)
tera_live\ios\.symlinks\       (SİL)
tera_live\.env                 (SİL - varsa)
tera_live\.idea\               (SİL - opsiyonel)
```

**Sonra kopyala:**
```
C:\Projects\tera_live\  →  source_code\tera_live\
```

---

### 3.2 Node.js API (tera_live_api)

**Silinecek dosya/klasörler:**
```
tera_live_api\node_modules\    (SİL)
tera_live_api\.env             (SİL)
tera_live_api\uploads\*        (içindeki dosyalar silinsin, klasör kalsın)
```

**Sonra kopyala:**
```
C:\Projects\tera_live_api\  →  source_code\tera_live_api\
```

---

### 3.3 React Admin (tera_admin)

**Silinecek dosya/klasörler:**
```
tera_admin\node_modules\       (SİL)
tera_admin\dist\               (SİL)
tera_admin\.env                (SİL)
```

**Sonra kopyala:**
```
C:\Projects\tera_admin\  →  source_code\tera_admin\
```

---

### 3.4 React Agency (tera_agency) - Varsa

**Silinecek dosya/klasörler:**
```
tera_agency\node_modules\      (SİL)
tera_agency\dist\              (SİL)
tera_agency\.env               (SİL)
```

**Sonra kopyala:**
```
C:\Projects\tera_agency\  →  source_code\tera_agency\
```

---

## ADIM 4: .env.example Dosyalarını Oluştur

Her projede `.env.example` dosyası olmalı.

### 4.1 tera_live/.env.example
```env
# API Configuration
API_BASE_URL=https://your-api-domain.com
SOCKET_URL=https://your-api-domain.com

# ZEGOCLOUD Configuration
ZEGO_APP_ID=your_zego_app_id
ZEGO_APP_SIGN=your_zego_app_sign

# Firebase Configuration (for Android)
# Download google-services.json from Firebase Console

# Firebase Configuration (for iOS)
# Download GoogleService-Info.plist from Firebase Console
```

### 4.2 tera_live_api/.env.example
```env
# Server Configuration
PORT=3000
NODE_ENV=production

# Database Configuration
DB_HOST=localhost
DB_PORT=5432
DB_NAME=teralive
DB_USER=postgres
DB_PASSWORD=your_password

# JWT Configuration
JWT_SECRET=your_super_secret_jwt_key_min_32_characters
JWT_EXPIRES_IN=7d

# ZEGOCLOUD Configuration
ZEGO_APP_ID=your_zego_app_id
ZEGO_SERVER_SECRET=your_zego_server_secret

# Firebase Admin SDK
FIREBASE_PROJECT_ID=your_firebase_project_id
FIREBASE_CLIENT_EMAIL=your_firebase_client_email
FIREBASE_PRIVATE_KEY=your_firebase_private_key

# Google OAuth (Optional)
GOOGLE_CLIENT_ID=your_google_client_id

# File Upload
UPLOAD_PATH=./uploads
MAX_FILE_SIZE=10485760

# CORS
ALLOWED_ORIGINS=http://localhost:3000,https://your-admin-domain.com
```

### 4.3 tera_admin/.env.example
```env
# API Configuration
VITE_API_URL=https://your-api-domain.com/api
VITE_SOCKET_URL=https://your-api-domain.com
```

### 4.4 tera_agency/.env.example
```env
# API Configuration
VITE_API_URL=https://your-api-domain.com/api
VITE_SOCKET_URL=https://your-api-domain.com
```

---

## ADIM 5: README.md Dosyalarını Oluştur

### 5.1 source_code/tera_live/README.md
```markdown
# TeraLIVE - Flutter Mobile App

## Requirements
- Flutter SDK 3.x
- Dart SDK
- Android Studio / Xcode
- ZEGOCLOUD Account
- Firebase Project

## Setup

1. Copy `.env.example` to `.env` and fill in your credentials

2. Install dependencies:
\`\`\`bash
flutter pub get
\`\`\`

3. For Android, add `google-services.json` to `android/app/`

4. For iOS, add `GoogleService-Info.plist` to `ios/Runner/`

5. Run the app:
\`\`\`bash
flutter run
\`\`\`

## Build

### Android APK
\`\`\`bash
flutter build apk --release
\`\`\`

### iOS
\`\`\`bash
flutter build ios --release
\`\`\`

## Documentation
See /documentation/app.html for detailed setup guide.
```

### 5.2 source_code/tera_live_api/README.md
```markdown
# TeraLIVE API - Node.js Backend

## Requirements
- Node.js 18+
- PostgreSQL 14+
- npm or yarn

## Setup

1. Copy `.env.example` to `.env` and fill in your credentials

2. Install dependencies:
\`\`\`bash
npm install
\`\`\`

3. Create database and run schema:
\`\`\`bash
psql -U postgres -c "CREATE DATABASE teralive"
psql -U postgres -d teralive -f src/config/schema.sql
\`\`\`

4. Run migrations:
\`\`\`bash
npm run migrate
\`\`\`

5. Seed default data (optional):
\`\`\`bash
npm run seed
\`\`\`

6. Start server:
\`\`\`bash
# Development
npm run dev

# Production
npm start
\`\`\`

## API Documentation
See /documentation/api.html for endpoint reference.
```

### 5.3 source_code/tera_admin/README.md
```markdown
# TeraLIVE Admin Panel - React

## Requirements
- Node.js 18+
- npm or yarn

## Setup

1. Copy `.env.example` to `.env` and configure API URL

2. Install dependencies:
\`\`\`bash
npm install
\`\`\`

3. Start development server:
\`\`\`bash
npm run dev
\`\`\`

4. Build for production:
\`\`\`bash
npm run build
\`\`\`

## Deployment
Upload the `dist/` folder to your web server.

## Documentation
See /documentation/admin.html for features guide.
```

### 5.4 source_code/tera_agency/README.md
```markdown
# TeraLIVE Agency Panel - React

## Requirements
- Node.js 18+
- npm or yarn

## Setup

1. Copy `.env.example` to `.env` and configure API URL

2. Install dependencies:
\`\`\`bash
npm install
\`\`\`

3. Start development server:
\`\`\`bash
npm run dev
\`\`\`

4. Build for production:
\`\`\`bash
npm run build
\`\`\`

## Deployment
Upload the `dist/` folder to your web server.

## Documentation
See /documentation/agency.html for features guide.
```

---

## ADIM 6: Ana README ve CHANGELOG Oluştur

### CodeCanyon_Package/README.txt
```
============================================
TeraLIVE - Complete Live Streaming Platform
Version: 1.0.0
Date: January 2026
============================================

Thank you for purchasing TeraLIVE!

PACKAGE CONTENTS
----------------
/documentation
  - index.html      : Complete setup documentation
  - app.html        : Mobile app features & setup
  - admin.html      : Admin panel features & setup
  - agency.html     : Agency panel features
  - api.html        : API reference

/source_code
  /tera_live        : Flutter mobile app (iOS & Android)
  /tera_live_api    : Node.js backend API
  /tera_admin       : React admin panel
  /tera_agency      : React agency panel

QUICK START
-----------
1. Open documentation/index.html in your browser
2. Follow the step-by-step installation guide
3. Configure your environment files (.env)
4. Deploy and launch!

REQUIREMENTS
------------
- Flutter SDK 3.x
- Node.js 18+
- PostgreSQL 14+
- ZEGOCLOUD Account (for video/audio)
- Firebase Project (for push notifications)
- VPS Server (Ubuntu 20.04+ recommended)

SUPPORT
-------
Email: [your-email@domain.com]
Response Time: 24-48 business hours

Please include your purchase code when contacting support.

CHANGELOG
---------
See CHANGELOG.md for version history.

============================================
(c) 2026 TeraLIVE. All rights reserved.
============================================
```

### CodeCanyon_Package/CHANGELOG.md
```markdown
# Changelog

All notable changes to TeraLIVE will be documented in this file.

## [1.0.0] - 2026-01-03

### Initial Release
- Flutter mobile app with TikTok-style UI
- Live streaming with ZEGOCLOUD SDK
- Voice rooms (8 seats) with DJ mode
- Party rooms (video group chat)
- Random video matching
- PK battle system
- Virtual gift system with animations
- Coin wallet and packages
- VIP membership system
- Family/Guild system (10 levels)
- Agency system (5 tiers)
- Social feed (posts, likes, comments)
- Direct messaging
- Push notifications (Firebase)
- React admin panel (50+ pages)
- React agency panel
- Node.js REST API
- Socket.IO real-time events
- PostgreSQL database
- Complete documentation
```

---

## ADIM 7: Son Kontrol Listesi

Paketlemeden önce kontrol et:

### documentation/ klasörü
- [ ] index.html var mı?
- [ ] app.html var mı?
- [ ] admin.html var mı?
- [ ] agency.html var mı?
- [ ] api.html var mı?
- [ ] appscreens/ klasörü var mı?
- [ ] adminscreens/ klasörü var mı?
- [ ] agencyscreens/ klasörü var mı?

### source_code/tera_live/
- [ ] node_modules YOK
- [ ] build/ YOK
- [ ] .dart_tool/ YOK
- [ ] ios/Pods/ YOK
- [ ] .env YOK
- [ ] .env.example VAR
- [ ] README.md VAR
- [ ] pubspec.yaml VAR

### source_code/tera_live_api/
- [ ] node_modules/ YOK
- [ ] .env YOK
- [ ] .env.example VAR
- [ ] README.md VAR
- [ ] package.json VAR
- [ ] src/config/schema.sql VAR

### source_code/tera_admin/
- [ ] node_modules/ YOK
- [ ] dist/ YOK
- [ ] .env YOK
- [ ] .env.example VAR
- [ ] README.md VAR
- [ ] package.json VAR

### source_code/tera_agency/
- [ ] node_modules/ YOK
- [ ] dist/ YOK
- [ ] .env YOK
- [ ] .env.example VAR
- [ ] README.md VAR
- [ ] package.json VAR

### Ana klasör
- [ ] README.txt VAR
- [ ] CHANGELOG.md VAR

---

## ADIM 8: ZIP Oluştur

**Windows'ta:**
1. CodeCanyon_Package klasörüne sağ tıkla
2. "Sıkıştırılmış klasöre gönder" veya 7-Zip kullan
3. Dosya adı: `teralive_v1.0.zip`

**PowerShell ile:**
```powershell
Compress-Archive -Path "C:\CodeCanyon_Package\*" -DestinationPath "C:\teralive_v1.0.zip"
```

---

## ADIM 9: ZIP Boyutunu Kontrol Et

| Boyut | Durum |
|-------|-------|
| 50-100 MB | İdeal |
| 100-200 MB | Kabul edilebilir |
| 200+ MB | Sorunlu (node_modules veya build kalmış) |

---

## Final Klasör Yapısı

```
CodeCanyon_Package/
│
├── README.txt
├── CHANGELOG.md
│
├── documentation/
│   ├── index.html
│   ├── app.html
│   ├── admin.html
│   ├── agency.html
│   ├── api.html
│   ├── appscreens/
│   │   └── (50 PNG dosyası)
│   ├── adminscreens/
│   │   └── (50 PNG dosyası)
│   └── agencyscreens/
│       └── (7 PNG dosyası)
│
└── source_code/
    │
    ├── tera_live/
    │   ├── lib/
    │   ├── android/
    │   ├── ios/
    │   ├── assets/
    │   ├── pubspec.yaml
    │   ├── .env.example
    │   └── README.md
    │
    ├── tera_live_api/
    │   ├── src/
    │   ├── uploads/ (boş)
    │   ├── package.json
    │   ├── server.js
    │   ├── .env.example
    │   └── README.md
    │
    ├── tera_admin/
    │   ├── src/
    │   ├── public/
    │   ├── package.json
    │   ├── vite.config.js
    │   ├── .env.example
    │   └── README.md
    │
    └── tera_agency/
        ├── src/
        ├── public/
        ├── package.json
        ├── vite.config.js
        ├── .env.example
        └── README.md
```

---

## Özet: Yapılacaklar Sırası

1. Boş klasör yapısı oluştur
2. Dokümantasyon dosyalarını kopyala (HTML + screenshots)
3. Her projeyi temizle (node_modules, build, .env sil)
4. Temiz projeleri kopyala
5. Her projeye .env.example ekle
6. Her projeye README.md ekle
7. Ana README.txt ve CHANGELOG.md ekle
8. Son kontrolleri yap
9. ZIP oluştur
10. Boyutu kontrol et
