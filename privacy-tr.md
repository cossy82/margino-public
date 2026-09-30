---
layout: default
title: Gizlilik Politikası
permalink: /privacy-tr.html
---

# Margino Gizlilik Politikası

**Yürürlük tarihi:** 8 Mayıs 2026
**Son güncelleme:** 30 Eylül 2026

Bu Gizlilik Politikası, Margino mobil uygulamasını ("Uygulama") ve ilgili hizmetleri ("Hizmet") kullanırken kişisel verilerinizin nasıl toplandığını, kullanıldığını, saklandığını ve korunduğunu açıklar. 6698 sayılı Kişisel Verilerin Korunması Kanunu ("KVKK") kapsamında bilgilendirme niteliğindedir.

## 1. Veri Sorumlusu

**Cemal Yılmaz** (Türkiye Cumhuriyeti'nde tescilli şahıs işletmesi).

İletişim: [cemalyilmazsmmm@gmail.com](mailto:cemalyilmazsmmm@gmail.com)

## 2. Toplanan Kişisel Veriler

Uygulamayı kullandığınızda aşağıdaki veriler işlenir:

| Veri Kategorisi | İçerik | Kaynak |
|---|---|---|
| Kimlik | Google hesap kimliği (sub), ad, profil resmi | Google OAuth |
| İletişim | Google hesabınızla bağlı e-posta adresi | Google OAuth |
| Hizmet Kullanımı | Yüklediğiniz fatura/makbuz görselleri (geçici), parse edilen satır bilgileri (satıcı, ürün, fiyat, toplam, KDV), ürün listeniz (ürün adı, tedarikçi, paket, son ve önceki birim maliyet), hedef kâr marjı ve teslimat uygulaması komisyon tercihleriniz, bağlarsanız Google Sheet ID'niz | Uygulama kullanımı |
| Teknik/Cihaz | IP adresi, istek zaman damgası | Cloudflare erişim logları |
| Bildirimler (isteğe bağlı) | Push bildirim token'ı ve uygulama dili — yalnızca bildirimlere izin verirseniz; haftalık tedarikçi maliyet uyarısı için | Uygulama (iOS) |
| Square (isteğe bağlı) | Yalnız Square'i bağlarsanız: Square işletme kimliğiniz, şifrelenmiş erişim ve yenileme token'ları ve bir yemeği bağladığınızda okunan Square menü ürünleriniz (ad, varyasyon, fiyat). Bağlanan ürün kimliği ve menü fiyatı o yemekte saklanır | Square (OAuth) |
| Faturalandırma (gelecekte) | RevenueCat abonelik durumu | App Store / Play Store |

## 3. İşleme Amaçları ve Hukuki Sebepler

| Amaç | Hukuki Sebep (KVKK m.5) |
|---|---|
| Faturanın OCR ile okunması, ürün listesi ve önerilen fiyatların uygulamada tutulması ve — yalnız bağlarsanız — kendi Google Sheet'inize yazılması | Sözleşmenin ifası (m.5/2/c) |
| Hesap kimlik doğrulaması ve oturum yönetimi | Sözleşmenin ifası (m.5/2/c) |
| Hizmet kötüye kullanımının önlenmesi (rate-limit, hata logları) | Meşru menfaat (m.5/2/f) |
| Anonim bölgesel piyasa fiyatı kıyaslaması | Meşru menfaat (m.5/2/f) — kişi tanımlayıcı bilgi olmadan |
| Ürün analitikleri (PostHog — kullanım metrikleri) | Açık rıza (uygulama içi onay alındığında) |
| Hangi reklamlarımızın uygulama yüklemesi, kayıt ve aboneliğe dönüştüğünü ölçmek (Meta App Events) | Meşru menfaat (m.5/2/f) |
| Yemeğin menü fiyatının Square menünüzden doldurulması — yalnız Square'i bağlarsanız | Sözleşmenin ifası (m.5/2/c) |

## 4. Veri Akışı ve Üçüncü Kişilere Aktarım

Uygulama, kişisel verilerinizi aşağıdaki hizmet sağlayıcılarla paylaşır. Hepsinin kullanım amacı **sadece Margino hizmetinin işlemesi** içindir; pazarlama amaçlı paylaşım yapılmaz.

| Alıcı | Konum | Amaç | Veri Türü |
|---|---|---|---|
| Anthropic, PBC | ABD | Fatura görselinin AI ile parse edilmesi (Claude API) | Fatura görseli (geçici, parse sonrası silinir) |
| Google LLC | Global | Google OAuth, Sheets API (kullanıcının kendi sheet'ine yazma), Drive metadata | Google profili, refresh token (şifreli) |
| Cloudflare, Inc. | ABD (edge POP'ları globaldir) | Uygulama backend'i (Workers), kuyruk işleme, erişim logları | Tüm istek payload'ları (RAM'de geçici, persistent storage yok) |
| Supabase, Inc. | ABD (us-east-1) | Postgres veritabanı (kullanıcı kayıtları, parse edilmiş faturalar, ürün listeniz, şifrelenmiş refresh token), Vault (anahtar yönetimi) | Kimlik, iletişim, fatura içeriği, ürün listesi, refresh token (şifreli) |
| PostHog, Inc. | ABD | Ürün analitikleri (yakında etkin) | Anonim event'ler |
| RevenueCat, Inc. | ABD | Abonelik yönetimi (Apple onayı sonrası) | Anonim abonelik durumu |
| Meta Platforms, Inc. | ABD | Margino'nun kendi reklamlarının ölçümü (Meta App Events SDK) | Uygulama olayları (yükleme, ilk giriş, ilk fiş, fiyat ve para birimiyle abonelik), cihaz ve uygulama bilgisi (model, işletim sistemi ve uygulama sürümü, dil, saat dilimi), IP adresi. Adınız, e-postanız, fişleriniz veya ürün listeniz asla gönderilmez. |
| Block, Inc. (Square) | ABD | İsteğe bağlı Square POS bağlantısı (OAuth, Catalog API) | OAuth token'larını Square ile değiş tokuş ederiz ve Square menünüzdeki ürün ve fiyatları okuruz. Fişlerinizi, maliyetlerinizi veya ürün listenizi Square'e asla göndermeyiz. |

**Yurt dışına aktarım:** KVKK m.9 kapsamında, ABD ve Global hizmet sağlayıcılara aktarım, Standard Contractual Clauses (SCC) ve hizmet sağlayıcıların DPA (Data Processing Agreement) çerçevesinde gerçekleşir. KVKK kapsamında yurt dışına aktarıma açık rızanız Uygulamayı kullanmaya başlamakla alınmış sayılır.

Margino sizi başka şirketlerin uygulama ve web sitelerinde izlemez. Uygulama İzleme Şeffaflığı (ATT) izni istemiyoruz ve cihazınızın reklam kimliğini (IDFA/AAID) toplamıyoruz. iOS'ta Apple'ın SKAdNetwork'ü, bir yüklemenin reklamdan geldiğini sizi tanımlamadan Meta'ya bildirir.

## 5. Saklama Süreleri

| Veri | Saklama Süresi |
|---|---|
| Fatura görselleri | İşlenene kadar (saniyeler); kalıcı saklama yok |
| Parse edilmiş fatura verisi ve ürün listesi | Hesap aktif olduğu sürece; hesap silinmesinde cascade delete. Google Sheets bağlarsanız bir kopyası da size ait Sheet'te durur |
| Şifrelenmiş refresh token (Supabase) | Hesap aktif olduğu sürece; hesap silinmesinde anında silinir |
| Kullanıcı kayıt verisi (Supabase users tablosu) | Hesap aktif olduğu sürece; hesap silinmesinde cascade delete |
| Receipt log (zaman damgası, başarı/başarısızlık) | Hesap aktif olduğu sürece; cascade delete |
| Square bağlantısı (işletme kimliği, şifreli token'lar) | Ayarlar'dan Square bağlantısını kesene veya hesabınızı silene kadar; bağlantıyı kesince Square'deki erişimimiz de iptal edilir |
| Cloudflare erişim logları | Cloudflare default 30 gün |
| Anonim regional benchmark | Süresiz (kişi tanımlayıcı bilgi yok, geri silinemez) |

## 6. KVKK m.11 Kapsamında Haklarınız

Kişisel verilerinizle ilgili aşağıdaki haklara sahipsiniz:

1. Kişisel verilerinizin işlenip işlenmediğini öğrenme
2. İşlendiğine ilişkin bilgi talep etme
3. İşleme amacını ve amacına uygun kullanılıp kullanılmadığını öğrenme
4. Yurt içi/yurt dışı aktarıldığı kişileri öğrenme
5. Eksik veya yanlış işlenmişse düzeltilmesini isteme
6. Silinmesini veya yok edilmesini isteme — Uygulama içinde **Ayarlar → Hesabı Sil** seçeneğiyle anında gerçekleşir
7. Düzeltme/silme işlemlerinin aktarıldığı kişilere bildirilmesini isteme
8. Otomatik sistemlerle analiz edilerek aleyhinize sonuç çıktığında itiraz etme
9. Zarar halinde tazminat talep etme

Başvurularınızı [cemalyilmazsmmm@gmail.com](mailto:cemalyilmazsmmm@gmail.com) adresine iletebilirsiniz. KVKK m.13 kapsamında talebiniz en geç 30 gün içinde sonuçlandırılır.

## 7. Çocukların Verileri

Margino 13 yaş altına yönelik bir hizmet değildir. 13 yaş altı bir kullanıcıdan veri toplandığını fark edersek hesabı derhal sileriz.

## 8. Veri Güvenliği

- Tüm istemci-sunucu trafiği TLS 1.3 ile şifrelenir
- Refresh token'lar Supabase Vault'ta KMS-yönetimli anahtarla şifrelenmiş halde saklanır
- Kullanıcı oturum JWT'si HMAC-SHA256 ile imzalanır: 1 saatlik erişim anahtarı + 180 gün kullanılmazsa sona eren yenileme anahtarı; her yenilemede değişir, tekrar kullanılan anahtar oturumu kapatır
- Üçüncü taraf hizmet sağlayıcılarının hepsi SOC 2 Type II veya ISO 27001 sertifikalıdır

## 9. Politikadaki Değişiklikler

Bu politikayı güncellediğimizde "Son güncelleme" tarihi değişir ve uygulama içi bildirimle haberdar ederiz. Önemli değişikliklerde mevcut kullanıcılardan yeniden açık rıza alınır.

## 10. İletişim

Veri sorumlusu Cemal Yılmaz'a aşağıdaki kanaldan ulaşabilirsiniz:

📧 [cemalyilmazsmmm@gmail.com](mailto:cemalyilmazsmmm@gmail.com)
