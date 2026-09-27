---
layout: default
title: Privacy Policy
permalink: /privacy-en.html
---

# Margino Privacy Policy

**Effective date:** 8 May 2026
**Last updated:** 27 September 2026

This Privacy Policy explains how Margino ("App", "Service") collects, uses, stores, and protects your personal data. It is provided in compliance with the EU General Data Protection Regulation (GDPR) and Türkiye's Personal Data Protection Law (KVKK).

## 1. Data Controller

**Cemal Yılmaz**, sole proprietor registered in Türkiye.

Contact: [cemalyilmazsmmm@gmail.com](mailto:cemalyilmazsmmm@gmail.com)

We have not appointed a Data Protection Officer (DPO) — Margino's processing volume and risk profile do not meet the GDPR Article 37 thresholds. The Data Controller above is the point of contact for all data subject requests.

## 2. Personal Data We Collect

When you use the App, we process the following data:

| Category | Content | Source |
|---|---|---|
| Identity | Google account ID (sub), name, profile picture | Google OAuth |
| Contact | Email associated with your Google account | Google OAuth |
| Service Usage | Receipt/invoice images you upload (transient), parsed line items (vendor, items, prices, totals, tax), your product list (product names, suppliers, pack sizes, latest and previous unit cost), your target profit margin and delivery-app commission preferences, your Google Sheet ID if you connect one | App use |
| Technical / Device | IP address, request timestamp | Cloudflare access logs |
| Notifications (optional) | Push notification token and app language, only if you allow notifications — used for the weekly supplier-cost alert | App (iOS) |
| Billing (future) | RevenueCat subscription state | App Store / Play Store |

## 3. Purposes and Legal Bases (GDPR Article 6)

| Purpose | Legal Basis |
|---|---|
| OCR-parsing your receipt, keeping your product list and suggested prices in the App, and — only if you connect it — writing them to your own Google Sheet | Performance of contract (Art. 6(1)(b)) |
| Account authentication and session management | Performance of contract (Art. 6(1)(b)) |
| Preventing service abuse (rate-limit, error logs) | Legitimate interest (Art. 6(1)(f)) |
| Anonymous regional price benchmarking | Legitimate interest (Art. 6(1)(f)) — no user identifier attached |
| Product analytics (PostHog — usage metrics) | Consent (Art. 6(1)(a)) — collected via in-app consent |

## 4. Data Flow and Third-Party Recipients

We share your data with the following service providers solely to operate Margino. We do not sell or share data for marketing.

| Recipient | Location | Purpose | Data Type |
|---|---|---|---|
| Anthropic, PBC | USA | AI parsing of receipt images (Claude API) | Receipt images (transient, deleted after parse) |
| Google LLC | Global | Google OAuth, Sheets API (writing to your own sheet), Drive metadata | Google profile, encrypted refresh token |
| Cloudflare, Inc. | USA (edge POPs are global) | App backend (Workers), queue processing, access logs | All request payloads (transient in RAM, no persistent storage) |
| Supabase, Inc. | USA (us-east-1) | Postgres database (user records, parsed receipts, your product list, encrypted refresh token), Vault (key management) | Identity, contact, parsed receipt content, product list, encrypted refresh token |
| PostHog, Inc. | USA | Product analytics (coming soon) | Anonymous events |
| RevenueCat, Inc. | USA | Subscription management (post-Apple approval) | Anonymous subscription state |

**International transfers:** Data is transferred to the USA and other regions outside the EEA / Türkiye. These transfers are protected by Standard Contractual Clauses (SCCs) under each provider's Data Processing Agreement (DPA). Where we rely on consent for the transfer (e.g. KVKK Article 9), it is collected when you start using the App.

## 5. Retention Periods

| Data | Retention |
|---|---|
| Receipt images | Until parsed (seconds); never persisted |
| Parsed receipt content and your product list | While your account is active; cascade-deleted on account deletion. If you connect Google Sheets, a copy also lives in your own Sheet, which you own |
| Encrypted refresh token (Supabase) | While account is active; deleted immediately on account deletion |
| User record (Supabase users table) | While account is active; cascade-deleted on account deletion |
| Receipt log (timestamp, success/failure) | While account is active; cascade-deleted on account deletion |
| Cloudflare access logs | Cloudflare default 30 days |
| Anonymous regional benchmarks | Indefinitely (no user identifier; cannot be traced back) |

## 6. Your Rights (GDPR Articles 15–22)

You have the following rights regarding your personal data:

- **Right of access** (Art. 15): request a copy of the data we hold about you
- **Right to rectification** (Art. 16): correct inaccurate data
- **Right to erasure** (Art. 17): delete your data — available instantly via **Settings → Delete Account** in the App
- **Right to restriction** (Art. 18): limit how we process your data
- **Right to data portability** (Art. 20): export your products and prices to your own Google Sheet from **Settings → Export to Google Sheets**, or email us for a copy
- **Right to object** (Art. 21): object to processing based on legitimate interest
- **Right to withdraw consent** (Art. 7(3)): for any processing relying on consent
- **Right to lodge a complaint**: with the Türkiye KVKK Authority (kvkk.gov.tr) or your local EU Data Protection Authority

To exercise any of these rights, email [cemalyilmazsmmm@gmail.com](mailto:cemalyilmazsmmm@gmail.com). We respond within 30 days (GDPR Article 12(3)).

## 7. Children's Data

Margino is not intended for users under 13. If we discover data has been collected from a user under 13, we will delete the account immediately.

## 8. Security

- All client-server traffic is encrypted with TLS 1.3
- Refresh tokens are stored in Supabase Vault encrypted with KMS-managed keys
- Session JWTs are signed with HMAC-SHA256: 1-hour access token + refresh token that expires after 180 days without use; each refresh rotates it and a reused refresh token signs the session out
- All third-party providers are SOC 2 Type II or ISO 27001 certified

## 9. Changes to this Policy

When we update this policy, the "Last updated" date changes and we notify you in-app. Material changes require re-consent from existing users.

## 10. Contact

Reach the Data Controller (Cemal Yılmaz) at:

📧 [cemalyilmazsmmm@gmail.com](mailto:cemalyilmazsmmm@gmail.com)
