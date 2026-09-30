---
layout: default
title: Account & Data Deletion
permalink: /account-deletion.html
---

# Account & Data Deletion / Hesap ve Veri Silme

## English

You can delete your Margino account and all associated personal data at any time. Two options:

### Option 1 — In-app (instant, recommended)

1. Open the Margino app
2. Tap **Settings** (gear icon, top-right of Home)
3. Scroll to **Delete Account**
4. Type `DELETE` in the confirmation field, tap **Delete my account**
5. Your account, encrypted refresh tokens, receipt log, and all related rows in our database are deleted immediately (cascade-delete via foreign keys)

**What is NOT deleted automatically:**
- Your **own Google Sheet** — you own it. Delete it from your Google Drive if you want it removed.
- **Anonymous regional benchmarks** — once aggregated, they have no link back to you and cannot be traced/deleted individually (our Privacy Policy §5).

### Option 2 — Email request (if you can't access the app)

Email **[support@usemargino.com](mailto:support@usemargino.com)** from the email address associated with your Margino account.

Subject: `Margino account deletion request`

Body should include:
- Your Google account email used to sign into Margino
- Confirmation: "I request deletion of my Margino account and all associated personal data"

We respond within **30 days** (typically within 1-3 business days). Deletion is permanent and cannot be undone.

### What gets deleted

| Data | Deleted? | Where |
|---|---|---|
| User record (Google sub, email, name, picture, sheet ID, target margin) | ✅ Yes | Supabase `users` table |
| Encrypted refresh token | ✅ Yes | Supabase Vault |
| Refresh token rotation log | ✅ Yes | Supabase `refresh_token_jti` |
| Receipt processing log (timestamps, success/fail counters) | ✅ Yes | Supabase `receipt_log` |
| Receipt images | N/A | Never persisted in the first place; deleted seconds after parsing |
| Parsed receipt content (vendor/items/prices) | N/A | Never on our servers — lives in your own Google Sheet |
| Your Google Sheet | ❌ No (you control it) | Delete manually from Google Drive |
| Anonymous regional benchmarks | ❌ No (irreversibly aggregated) | No user identifier; can't trace |
| Cloudflare access logs (IP + timestamp) | ⏳ 30 days | Cloudflare default rolling window |

---

## Türkçe

Margino hesabınızı ve ilişkili tüm kişisel verilerinizi istediğiniz zaman silebilirsiniz. İki yol:

### Seçenek 1 — Uygulama içinden (anında, önerilen)

1. Margino uygulamasını açın
2. **Ayarlar** simgesine basın (anasayfanın sağ üstünde dişli ikonu)
3. **Hesabı Sil** seçeneğine ilerleyin
4. Onay alanına `DELETE` yazın → **Hesabımı sil** butonuna basın
5. Hesabınız, şifreli refresh token'larınız, receipt log'unuz ve veritabanımızdaki tüm ilişkili kayıtlar anında silinir (cascade-delete)

**Otomatik silinmeyen:**
- **Kendi Google Sheet'iniz** — onun sahibi sizsiniz. Silmek isterseniz Google Drive'ınızdan elinizle silin.
- **Anonim bölgesel benchmark'lar** — toplu hale geldiğinde sizinle bağlantısı kalmaz, geri tek tek silinemez (Gizlilik Politikamız §5).

### Seçenek 2 — E-posta ile talep (uygulamaya erişemiyorsanız)

Margino hesabınızla ilişkili e-posta adresinden **[support@usemargino.com](mailto:support@usemargino.com)** adresine yazın.

Konu: `Margino hesap silme talebi`

İçerik:
- Margino'ya giriş için kullandığınız Google hesabı e-postası
- Onay: "Margino hesabımın ve tüm ilişkili kişisel verilerimin silinmesini talep ediyorum"

**30 gün içinde** (genelde 1-3 iş günü) cevaplarız. Silme kalıcıdır, geri alınamaz.

---

## Contact / İletişim

📧 [support@usemargino.com](mailto:support@usemargino.com)
🔒 [Privacy Policy (English)](privacy-en.html) / [Gizlilik Politikası (Türkçe)](privacy-tr.html)
🏠 [Home](/)
