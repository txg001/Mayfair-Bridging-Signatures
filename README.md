# Mayfair Bridging — Email Signatures

HTML email signatures for the Mayfair Bridging team, styled to the brand
(navy `#0F2B46`, Georgia serif, champagne-gold accents) and built email-safe:
table layout, inline styles, no web fonts, no SVG.

## Files

| File | Purpose |
|---|---|
| `index.html` | Preview all four signatures with one-click **Copy signature** buttons |
| `paul-munford.html` | Paul Munford — Co-CEO |
| `freddie-munford.html` | Freddie Munford — Origination Director |
| `david-rundell.html` | David Rundell — Co-CEO & CTO |
| `marie-brown.html` | Marie Brown — Chief Operating Officer |
| `email-logo.png` | Logo rasterised from the SVG (1208×305, transparent) — local copy of the hosted file |
| `Mayfair bridging concept 2.svg` | Source logo artwork |

## Installing a signature

1. Open `index.html` in a browser.
2. Click **Copy signature** for the relevant person.
3. Paste into the email client's signature editor:
   - **Gmail**: Settings → See all settings → General → Signature
   - **Outlook**: Settings → Mail → Compose and reply → Email signature
   - **Apple Mail**: Settings → Signatures

## Logo hosting

Email clients cannot load images from local files, so every signature
references the logo at its hosted URL:

```
https://www.mayfairbridging.co.uk/email-logo.png
```

This is live. Use the `www.` form — the bare domain 301-redirects, and some
email clients won't follow a redirect for an image. If the logo ever moves,
update the `HOSTED_LOGO` constant in `index.html` and the `img src` in each
person's file.

The logo displays at 190×48 px but the PNG is ~4× that size, so it stays crisp
on retina screens.

## Notes

- Phone numbers are `tel:` links and the email address is a `mailto:` link.
- The pre-registration email disclaimer is intentionally **not** included in
  the signatures, per the brief.
