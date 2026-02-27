# cllctd earn — Contributor PWA

Progressive Web App for the cllctd contributor platform.

## Files

```
index.html      — Full app (React via CDN, no build step)
manifest.json   — PWA manifest (install prompt, icons, theme)
sw.js           — Service worker (offline support, caching)
icon-192.svg    — App icon 192px
icon-512.svg    — App icon 512px
vercel.json     — Vercel routing config
```

## Deploy to Vercel (30 seconds)

1. Push this folder to a GitHub repo
2. Go to vercel.com → New Project → Import your repo
3. Framework preset: **Other** (no build command needed)
4. Deploy

Live at `your-project.vercel.app` — add custom domain `earn.cllctd.ai` in Vercel settings.

## Install as PWA

**Android:** Chrome shows "Add to Home Screen" banner automatically.

**iOS (Safari):** Tap Share → Add to Home Screen.

## Screens

| Screen | Route key |
|--------|-----------|
| Splash / Install | `splash` |
| Phone Entry | `phone` |
| OTP | `otp` |
| Profile Setup | `profileSetup` |
| Payout Setup | `payout` |
| Home / Task Feed | `home` |
| Task Detail | `detail` |
| Voice Recording | `voice` |
| Video Task | `video` |
| Photo Upload | `photo` |
| Text Labels | `text` |
| Submission Success | `success` |
| Earnings & Wallet | `earnings` |
| Profile & Settings | `profile` |

## For Production

Replace the mock data and state in `index.html` with:

- **Auth:** Supabase Auth (phone + OTP)
- **Database:** Supabase Postgres
- **Media upload:** Supabase Storage (signed URLs)
- **Payouts:** Razorpay Payout API
- **SMS OTP:** MSG91 or Twilio

See `cllctd-app-spec.docx` for full technical specification.
