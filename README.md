# Linanthus Labs

Scientific consulting in AI, data analysis, and assay development. A static website with dark forest greens, cream and lavender accents, and custom Linanthus flower artwork.

## Publish with GitHub Pages

1. Upload this folder's contents to `rrenslow/linanthus` on `main`. The repository should contain `docs/index.html` directly, with no extra enclosing folder.
2. In **Settings → Pages**, choose **Deploy from a branch → main → /docs → Save**.
3. Set **Custom domain** to `linanthus.com`, then connect the GoDaddy DNS records and enable HTTPS as described in [LAUNCH.md](LAUNCH.md).

GitHub serves the website. GoDaddy remains the domain registrar and DNS provider. No paid hosting plan or additional hosting provider is required for this setup. Future commits to `docs/` on `main` update the site automatically after a successful Pages deployment.

The site is plain HTML, CSS, and JavaScript, with local fonts and artwork. No package installation or build command is needed. Navigation, service details, and email links work without JavaScript.

## Contact

The business email is **linanthuslabs@gmail.com**, confirmed by the owner. All website email links and the privacy page use this address. Forwarding is configured separately in Gmail; the website does not forward mail.

## Edit or preview

| Item | File |
| --- | --- |
| Page copy and services | `docs/index.html` |
| Colors and layout | `docs/styles.css` |
| Menu and email-copy button | `docs/script.js` |
| Privacy notice | `docs/privacy.html` |
| Logo, artwork, and fonts | `docs/assets/` |
| Domain and publishing instructions | `LAUNCH.md` |
| Brand notes and asset provenance | `BRAND.md` |

For a local preview, run `python3 -m http.server 8080 --directory docs`, then open `http://localhost:8080`.

## Notes

- Publish only `docs/` through Pages. The repository is public, so keep CVs, private documents, credentials, and client material out of the entire repository.
- The copy describes collective professional experience, not former employers' endorsement or a track record of the newly formed company.
- The public brand is “Linanthus Labs.” Update any legal entity wording only after formation is confirmed.
- GitHub's restrictions on business use still apply. The absence of checkout does not by itself establish that a consulting site is exempt. See the short policy note in [LAUNCH.md](LAUNCH.md).
- No open-source license is granted for the branding, copy, or custom artwork by making the repository public. The fonts retain their SIL Open Font Licenses in `docs/assets/fonts/`.
