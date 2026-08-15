# Elite — Account Deletion & Privacy Pages

The public compliance pages for the Elite habit tracker (`com.eliteapp.tracker`).
Two static, self-contained pages (brand mark embedded, no external requests,
no scripts), deployed on Vercel:

- `index.html` — the account-deletion request page, required by Google Play's
  account-deletion policy (and referenced from App Store Connect's privacy
  section). Production URL goes into Play Console → App content → Data safety →
  Account deletion.
- `privacy.html` — the privacy policy. Production URL goes into Play Console →
  App content → Privacy policy AND App Store Connect → App Privacy → Privacy
  Policy URL.

## Edit contract

- `privacy.html` — **this repo is the source of truth** (relocated from the app
  repo 2026-08-15; the app repo carries no copy). Edit here, push, Vercel
  redeploys. The Elite app repo's `CLAUDE.md` carries the standing rule that
  keeps it current: any app change that alters what data is collected, shared,
  stored, or which permissions ship must update this page in the same session.
- `index.html` — source of truth is
  `Elite app/docs/release/account-deletion-page.html` in the private app repo:
  edit there, copy here, push.
