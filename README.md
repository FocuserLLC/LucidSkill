# LucidSkill — Legal Documents

Plain-markdown copies of the three legal documents shown inside the LucidSkill app,
kept here so they can be published and updated without an app release.

| Document | File | Where it's used |
| --- | --- | --- |
| Safety Notice & Legal Disclaimer | [safety-and-disclaimer.md](safety-and-disclaimer.md) | Acceptance gate on first launch; Settings → Legal |
| Privacy Policy | [privacy-policy.md](privacy-policy.md) | App Store Connect "Privacy Policy URL"; paywall footer |
| Terms of Use (EULA) | [terms-of-use.md](terms-of-use.md) | App Store Connect "EULA"; paywall footer |

## Publishing

Uploading these to a GitHub repo with Pages enabled turns each one into a page
automatically — `privacy-policy.md` is served at `/privacy-policy`, and so on.
Those are the URLs to paste into App Store Connect and the Play Console.

## Keeping copies in sync

The in-app wording lives in `expo/constants/legal.ts` (privacy + EULA + disclaimer terms)
and `expo/constants/safety.ts` (the safety notice). If the published text changes here,
change it there too — App Review compares the two.

Materially changing the safety notice also means bumping `DISCLAIMER_VERSION` in
`expo/constants/safety.ts`, which re-prompts existing users to read and accept it again.

## Notes on the current text

- Legal entity: **Focuser LLC**. Last-updated date: **August 2026**.
- Contact is `support@lucidskill.app`. The in-app versions deliberately point to the
  store listing's support contact instead, so it stays correct without an app update.
- Terms § 15 says "the state in which Focuser LLC is organised" — worth replacing with
  the actual state in both this file and `expo/constants/legal.ts`.
