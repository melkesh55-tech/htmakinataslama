# HT Makina Taşlama — Kurulum Rehberi
### MK Software tarafından geliştirilmiştir

---

## 📁 Dosya Listesi

```
ht-makina/
├── index.html           ← Ana site
├── admin.html           ← Müşteri admin paneli (PWA)
├── manifest.json        ← PWA manifest (ana site)
├── admin-manifest.json  ← PWA manifest (admin)
├── sw.js                ← Service Worker
├── supabase-setup.sql   ← Veritabanı kurulum scripti
└── README.md            ← Bu dosya
```

---

## 1️⃣ SUPABASE KURULUMU

1. https://supabase.com → GitHub ile ücretsiz kayıt
2. **New project** → Ad: `ht-makina` → Bölge: **Frankfurt**
3. Sol menü → **SQL Editor** → `supabase-setup.sql` içeriğini yapıştır → **RUN**
4. **Settings → API** → şunları kopyala:
   - `Project URL` → `https://xxxxx.supabase.co`
   - `anon public key` → `eyJhbGciOiJIUzI1NiIs...`

---

## 2️⃣ DEVELOPER PANELİ — İLK KURULUM

`admin.html` → giriş ekranında **"Geliştirici Girişi"** → Şifre: `mksoft2026`

Developer panelinde sırayla doldur:

| Alan | Nereden Alınır |
|------|---------------|
| Supabase URL | Supabase → Settings → API |
| Supabase Key | Supabase → Settings → API → anon public |
| Telegram Bot Token | @BotFather → /newbot |
| Telegram Chat ID | @userinfobot veya grup negatif ID |
| ImgBB API Key | imgbb.com → API (ücretsiz) |
| Admin şifresi | İstediğin şifreyle değiştir |
| MK Software URL | Domain alınınca gir |

**"Kaydet ve Yenile"** → Bitti, sistem çalışıyor.

---

## 3️⃣ IMGBB API KEY

1. https://imgbb.com → ücretsiz hesap
2. Sağ üst → kullanıcı adı → **API**
3. API key'i kopyala
4. Developer paneli → ImgBB bölümüne yapıştır → Kaydet

---

## 4️⃣ NETLIFY YAYINLAMA

1. https://netlify.com → ücretsiz hesap
2. **Sites** → tüm `ht-makina` klasörünü sürükle-bırak
3. Hazır! `https://random.netlify.app` adresi verilir

---

## 5️⃣ MÜŞTERİYE TESLİM

Müşteriye verilecekler:
- Site adresi: `https://xxx.netlify.app`
- Admin adresi: `https://xxx.netlify.app/admin.html`
- Kullanıcı adı: `admin`
- Şifre: *(developer panelinden belirlediğin şifre)*

**Müşteri yalnızca şunları yapacak:**
- Yeni teklifleri görüp arama/WhatsApp
- Fotoğraf yükle/sil (tek tıkla)
- Hizmet aç/kapat

---

## 6️⃣ BAKIM MODU

Developer paneli → **Bakım Modu** toggle → Aç

Ziyaretçiler "Bakım çalışması" sayfasını görür.
Kapatmak için toggle → Kapat.

---

## 7️⃣ DOMAIN BAĞLAMA (İLERİDE)

Netlify → Site → **Domain management** → Add custom domain
DNS: A kaydı `75.2.60.5` | CNAME `www` → `siteniz.netlify.app`

---

## 🔐 ŞİFRELER

| Panel | Kullanıcı | Şifre |
|-------|-----------|-------|
| Admin (müşteri) | admin | 123 *(değiştir!)* |
| Developer (MK) | — | mksoft2026 |

---

*MK Software — v1.0.0 — 2026*
