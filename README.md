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

Source of truth for both lives in the private app repo under
`Elite app/docs/release/`:

- `account-deletion-page.html` → copy here as `index.html`.
- `privacy-policy.html` → generated here as `privacy.html` via
  `node tool/inject_mark.mjs` (the tracked source keeps a placeholder for the
  embedded brand mark; the tool injects the real data URI at copy time).

Edit there, copy/generate here, push — Vercel redeploys.
