# Fynix Education Website

A lightweight, mobile-first proposal website for Fynix Edu, built as a static GitHub Pages site.

## What the site does

- Presents Fynix Edu as an online tuition brand for Science & Mathematics, Year 4 to Form 5.
- Provides direct WhatsApp enrolment CTAs for tuition enquiries.
- Consolidates existing digital worksheets into one catalogue.
- Links each verified worksheet directly to its existing ToyyibPay checkout page.
- Makes FPX / DuitNow payment access clear without requiring a custom backend.
- Adds a founder profile, programme overview, FAQ, responsive navigation and mobile CTA.

## Verified public research used

- Fynix Edu Linktree: https://linktr.ee/farhaneem.n
- Public Fynix Edu / Farhaneem professional profile information was cross-checked via search results.
- Existing ToyyibPay checkout pages were used for product names, prices and page counts.
- Public business contact used by the existing ToyyibPay bills: 013-229 1612.

### Existing checkout mapping

| Product | Price | Pages | Checkout |
|---|---:|---:|---|
| Preschool's Worksheet | RM6 | 108 | https://toyyibpay.com/PRESCHOOL-S-WORKSHEET |
| Ulangkaji Sains Tahun 2 | RM8 | 26 | https://toyyibpay.com/ULANGKAJI-SAINS-TAHUN-2 |
| Ulangkaji Sains Tahun 3 | RM8 | 26 | https://toyyibpay.com/WORKSHEET-TAHUN3 |
| Transisi Tahun 1 English | RM3 | 20 | https://toyyibpay.com/TRANSISI-TAHUN-1-ENGLISH |
| Transisi Tahun 1 Sains | RM3 | 20 | https://toyyibpay.com/TRANSISI-TAHUN-1-SAINS |
| Transisi Tahun 1 Matematik | RM3 | 30 | https://toyyibpay.com/TRANSISI-TAHUN-1-MATEMATIK |
| Transisi Tahun 1 Bahasa Melayu | RM3 | 20 | https://toyyibpay.com/TRANSISI-TAHUN-1-BAHASA-MELAYU |

The current Linktree also lists a Science Year 4 worksheet. Its direct ToyyibPay URL was not reliably discoverable, so the proposal links that product back to the official Linktree rather than inventing a checkout URL.

## Payment architecture

For this proposal, the safest zero-backend implementation is to keep ToyyibPay as the payment processor and make the website the catalogue / conversion layer.

Flow:

1. Parent selects a worksheet on the website.
2. Website sends them to the corresponding official ToyyibPay bill.
3. ToyyibPay handles FPX / DuitNow payment and receipt.
4. Fynix Edu keeps its existing fulfilment process.

For tuition fees, the website currently sends parents to WhatsApp because no verified class-fee bill / price was found publicly. Once the class fee and ToyyibPay bill are confirmed, that CTA can become direct online checkout too.

## GitHub Pages

The project is intentionally static and can run directly from GitHub Pages with no build step.

If Pages is not enabled yet:

1. Open repository **Settings**.
2. Open **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select `main` and `/ (root)`.
5. Save.

Expected project URL once enabled:

`https://shukritobi.github.io/Fynix-Education/`

## Notes before client handover

- Confirm current tuition schedule and class fees.
- Confirm whether Science Year 4 has a direct ToyyibPay bill.
- Replace the lightweight vector-inspired mark with the original high-resolution brand logo if supplied.
- Add official class screenshots / tutor photos only after the client approves the assets.
- If Fynix Edu later wants a true multi-item cart and automatic digital delivery, move checkout creation to a small serverless backend instead of exposing payment API secrets in the frontend.
