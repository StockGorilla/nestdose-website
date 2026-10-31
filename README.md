# nestdose-website

Static marketing + legal site for [Nestdose](https://nestdose.com), the
family-shared medication reminder for iOS.

## Pages

| Path          | Purpose |
|---------------|---------|
| `/`           | Landing page: tagline, free vs paid feature list, "Private by architecture" pitch |
| `/privacy/`   | Privacy policy — mirrors the App Store privacy label |
| `/support/`   | Support, including how to delete data (App Review requirement) |
| `/terms/`     | Terms of service |
| `/404.html`   | Soft 404 |

## Deploy

Netlify auto-deploys `main`. No build step — files are served from the
repo root. See `netlify.toml` for config.

To preview locally:

```sh
python3 -m http.server 4000
# open http://localhost:4000
```

## Updating the privacy policy

The policy at `/privacy/` must stay in sync with the App Store privacy
nutrition label and with the TelemetryDeck integration in the app. If
either changes, update this policy and the App Store label the same day
— mismatches are a 5.1.1(iv) rejection risk.

## Design tokens

The CSS tokens in `style.css` mirror
`Nestdose/DesignSystem/Tokens.swift` from the iOS app so the website
reads as the app on landing. Keep in sync when the app tokens move.
