<div align="center">

# ⚽ Futbol Arkadaşım

### *Sahaya Çık, Arkadaşını Bul, Maçını Yap!*

---

![Platform](https://img.shields.io/badge/Platform-Web-green?style=for-the-badge&logo=google-chrome)
![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react)
![Node.js](https://img.shields.io/badge/Node.js-Express-339933?style=for-the-badge&logo=node.js)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Prisma-4169E1?style=for-the-badge&logo=postgresql)
![Status](https://img.shields.io/badge/Status-Aktif%20Geliştirme-brightgreen?style=for-the-badge)

</div>

---

## 🎯 Proje Hakkında

**Futbol Arkadaşım**, futbol severler için tasarlanmış kapsamlı bir sosyal medya ve organizasyon platformudur. Halı saha oynamak isteyip takım kuramayan ya da eksik oyuncularını dolduramayan herkese yönelik olan bu platform; oyuncu eşleştirme, takım kurma, saha rezervasyonu ve sosyal etkileşim özelliklerini tek bir çatı altında sunar.

> *"Artık WhatsApp gruplarında 'bu hafta kim var?' diye sormak zorunda değilsiniz."*

---

## ✨ Özellikler

### 🏟️ Ana Feed & Sosyal Medya
Platform, bir sosyal medya akışıyla başlar. Kullanıcılar maç anlarını, gol videolarını ve sahadan fotoğrafları paylaşabilir. Beğeni ve yorum sistemiyle topluluk etkileşimi ön planda tutulur.

### 👥 Oyuncu Eşleştirme Sistemi
Projenin en güçlü özelliği olan **PlayerMatcher**, oyuncuları mevkisine, puanına ve müsaitlik durumuna göre akıllıca eşleştirir. Eksik oyuncunuz mu var? Sistem size en uygun isimleri önerir.

- 📍 Konuma göre yakın oyuncu arama
- 🎯 Mevki filtresi (Kaleci, Defans, Orta Saha, Forvet)
- ⭐ Oyuncu puanlama ve değerlendirme
- 📊 Detaylı oyuncu istatistikleri (maç, gol, asist)

### 🏆 Takım Yönetimi
Kendi takımınızı kurun veya mevcut takımlara katılın. Takımınızı yönetin, üyelerinizi görün ve birlikte maç organize edin.

- ➕ Yeni takım oluşturma
- 👤 Takım kaptanlığı sistemi
- 📋 Takım üye yönetimi
- 🔍 Takım arama ve filtreleme

### 📅 Saha Rezervasyon Sistemi
Anlaşmalı halı saha tesisleriyle entegre çalışan rezervasyon modülü sayesinde sahayı uygulama üzerinden kolayca ayırtabilirsiniz.

- 🕐 Gerçek zamanlı müsait saat görüntüleme
- 💳 Çevrimiçi rezervasyon onayı
- 🗓️ Haftalık program planlama
- 📍 Tesis konumu ve iletişim bilgileri
- ⭐ Tesis puanlama ve yorum sistemi

### 📊 Maç Sonuçları & İstatistikler
Her maçın ardından sonuçları kaydedin, bireysel ve takım istatistiklerinizi takip edin.

- 📈 Kişisel istatistik paneli (gol, asist, maç)
- 🏅 Sezon bazlı performans takibi
- 📉 Recharts ile görsel grafik raporları
- 🥇 En iyi oyuncu & gol krallığı sıralaması

### 🎬 Video Paylaşım
Maçlarınızdan aldığınız video kliplerinizi platforma yükleyin. Supabase altyapısıyla desteklenen video saklama sistemi yüksek kaliteli içerik desteği sunar.

### 🌍 Çok Dil Desteği
Platform, **i18next** kütüphanesi ile çok dil desteği sunmaktadır. Kullanıcılar dil tercihini istedikleri zaman değiştirebilir.

### 🛡️ Admin Paneli
Tesis sahipleri ve yöneticiler için özel bir admin dashboard mevcuttur:

- 🏟️ Tesis yönetimi (ekleme, düzenleme, silme)
- 💰 Finansal raporlar ve gelir takibi
- 🔧 Bakım yönetimi ve arıza takibi
- 👥 Kullanıcı yönetimi

---

## 🗂️ Proje Yapısı

```
Futbol_Arkadasim/
│
├── 📁 src/                          # React Frontend
│   ├── 📁 components/               # Yeniden kullanılabilir bileşenler
│   │   ├── Auth/                    # Giriş & Kayıt ekranları
│   │   ├── Admin/                   # Admin paneli bileşenleri
│   │   ├── Feed/                    # Ana akış bileşenleri
│   │   ├── Video/                   # Video listesi & detay
│   │   ├── PlayerMatcher.js         # 🌟 Oyuncu eşleştirme motoru
│   │   ├── ReservationSystem.js     # 📅 Rezervasyon sistemi
│   │   ├── Teams.js                 # 🏆 Takım yönetimi
│   │   ├── MatchResults.js          # 📊 Maç sonuçları
│   │   ├── Profile.js               # 👤 Kullanıcı profili
│   │   └── Navbar.js                # 🧭 Navigasyon çubuğu
│   │
│   ├── 📁 pages/                    # Sayfa bileşenleri
│   │   ├── Stats.js                 # İstatistik paneli
│   │   ├── Settings.js              # Kullanıcı ayarları
│   │   ├── About.js                 # Hakkında sayfası
│   │   ├── AdminDashboard.js        # Admin kontrol paneli
│   │   └── ReviewsPage.js           # Tesis yorumları
│   │
│   └── 📁 locales/                  # Çok dil desteği dosyaları
│
├── 📁 backend/                      # Node.js + Express API
│   ├── 📁 routes/                   # API route tanımları
│   │   ├── authRoutes.js            # Kimlik doğrulama
│   │   ├── teamRoutes.js            # Takım işlemleri
│   │   ├── matchRoutes.js           # Maç yönetimi
│   │   ├── reservationRoutes.js     # Rezervasyonlar
│   │   ├── venueRoutes.js           # Halı saha tesisleri
│   │   ├── playerRoutes.js          # Oyuncu işlemleri
│   │   ├── videoRoutes.js           # Video yönetimi
│   │   └── reviewRoutes.js          # Yorum sistemi
│   │
│   ├── 📁 controllers/              # İş mantığı katmanı
│   ├── 📁 middleware/               # Auth & hata yönetimi
│   ├── 📁 prisma/                   # Veritabanı şeması (ORM)
│   ├── 📁 services/                 # Supabase storage servisi
│   └── server.js                    # Express sunucu giriş noktası
│
└── 📁 app/                          # Android (Kotlin/Gradle) modülü
```

---

## 🧠 Teknoloji Yığını

### Frontend
| Teknoloji | Kullanım Amacı |
|-----------|----------------|
| **React 18** | Kullanıcı arayüzü çerçevesi |
| **Material UI (MUI)** | Hazır UI bileşen kütüphanesi |
| **React Router v6** | Sayfa yönlendirme |
| **Axios** | HTTP istek yönetimi |
| **Recharts** | Grafik ve istatistik görselleri |
| **react-player** | Video oynatıcı |
| **i18next** | Çok dil desteği |
| **date-fns** | Tarih/saat işlemleri |

### Backend
| Teknoloji | Kullanım Amacı |
|-----------|----------------|
| **Node.js + Express** | REST API sunucusu |
| **Prisma ORM** | Veritabanı sorgu katmanı |
| **PostgreSQL** | İlişkisel veritabanı |
| **JWT** | Token tabanlı kimlik doğrulama |
| **bcryptjs** | Şifre şifreleme |
| **Multer** | Dosya yükleme yönetimi |
| **Supabase Storage** | Bulut tabanlı medya depolama |

---

## 🔐 Güvenlik & Kimlik Doğrulama

Platform, güvenli bir kimlik doğrulama mimarisi üzerine inşa edilmiştir:

- **JWT (JSON Web Token)** ile oturum yönetimi
- **bcryptjs** ile şifrelerin güvenli şekilde hashlenmesi
- **Korumalı rotalar** — giriş yapılmadan erişilemeyen sayfalar
- **Token bazlı API erişimi** — her istek doğrulanır
- **Admin rolleri** — özel yetkili kullanıcı yönetimi

---

## 📱 Sayfalar & Rotalar

| Rota | Sayfa | Erişim |
|------|-------|--------|
| `/` | Ana Feed | Herkese açık |
| `/login` | Giriş Yap | Herkese açık |
| `/register` | Kayıt Ol | Herkese açık |
| `/about` | Hakkında | Herkese açık |
| `/videos` | Videolar | Herkese açık |
| `/matches` | Maç Sonuçları | 🔒 Giriş gerekli |
| `/teams` | Takımlar | 🔒 Giriş gerekli |
| `/reservations` | Rezervasyonlar | 🔒 Giriş gerekli |
| `/profile` | Profil | 🔒 Giriş gerekli |
| `/stats` | İstatistikler | 🔒 Giriş gerekli |
| `/settings` | Ayarlar | 🔒 Giriş gerekli |
| `/admin` | Admin Paneli | 🔒 Admin gerekli |

---

## 👤 Geliştirici

**NurettinKaradag**
[![GitHub](https://img.shields.io/badge/GitHub-NurettinKaradag-181717?style=flat-square&logo=github)](https://github.com/NurettinKaradag)

---

<div align="center">

*⚽ Futbol sadece bir oyun değil, bir kültürdür. Bu platform o kültürü dijitale taşır.*

**Futbol Arkadaşım** © 2025 — Tüm hakları saklıdır.

</div>
