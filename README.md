# DedupeX

DedupeX is a privacy-first, open-source Android app for detecting duplicate files and analyzing unnecessary media on your device.

No ads.  
No tracking.  
No fake performance boosts.  
Just transparent storage intelligence.

---

## 🚀 Core Features

- 🔍 Media scan using Android MediaStore (Android 11+ compliant)
- 🧠 True duplicate detection using SHA-256 hashing
- 📊 Large file identification
- 🖼 Screenshot and redundant media discovery
- 🗑 Safe file deletion via ContentResolver
- 🔒 Fully offline (no internet permission)

---

## 🧠 Duplicate Detection Strategy

DedupeX avoids naive full hashing to protect performance and battery life.

Algorithm:

1. Query files via MediaStore
2. Group files by identical file size
3. Hash only files with matching sizes
4. Generate SHA-256 hash
5. Group by hash
6. Display only true duplicate groups

This dramatically reduces unnecessary CPU usage.

---

## 🏗 Architecture

DedupeX follows Clean Architecture principles:

presentation → domain → data → core

**Presentation**
- Jetpack Compose
- ViewModels
- StateFlow

**Domain**
- Pure Kotlin use cases
- Business logic only

**Data**
- MediaStore integration
- Room (scan caching)
- Repository implementations

**Core**
- Hashing engine
- Coroutine dispatchers
- Utilities

---

## 🔐 Privacy Philosophy

DedupeX is built with strict boundaries:

- No internet permission
- No analytics SDKs
- No background tracking
- No hidden services

All file processing happens locally on your device.

Your data never leaves your phone.

---

## ❌ What DedupeX Will Never Include

- RAM boosters
- CPU optimizers
- Fake speed meters
- Private app sandbox access
- System-level cleaning tricks
- Aggressive ad integrations

Android already manages memory and system performance efficiently.

---

## 📦 Tech Stack

- Kotlin
- Jetpack Compose
- Coroutines + Flow
- MediaStore API
- Room
- WorkManager (planned incremental scanning)

Min SDK: 26  
Target SDK: Latest stable Android version

---

## 🗺 Roadmap

### v0.1
- Media scan
- Duplicate detection
- Large file listing
- Safe deletion

### v0.5
- Hash caching
- Incremental scan optimization
- Performance tuning

### v1.0
- Storage analytics dashboard
- Folder size insights
- Media growth tracking

---

## ⚠ Limitations

- Cannot access private app directories (/data/data/)
- Fully compliant with Android scoped storage
- Does not require root

---

## 🤝 Contributing

Contributions are welcome.

Please keep contributions:
- Privacy-first
- Efficient
- Minimal in permissions
- Free from ads and tracking SDKs

---

## 📜 License

Licensed under the Apache License, Version 2.0.

See the LICENSE file for details.

---

## Why DedupeX Exists

Many cleaner apps:

- Overpromise
- Request unnecessary permissions
- Use aggressive advertising
- Provide misleading statistics

DedupeX exists to prove storage analysis can be:

- Honest
- Transparent
- Efficient
- Fully open-source
- Respectful of users

---

Built for clarity. Not marketing.
