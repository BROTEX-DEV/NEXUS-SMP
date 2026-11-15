# NEXUS SMP

The official public website for **NEXUS SMP** — a Minecraft server project.

## Current status

This repository currently contains a single-page static website in `index.html`.

- Default branch: `main`
- Website source: `index.html`
- GitHub Pages: enabled in repository settings (the live deployment was not browser-tested during this review)
- Project version: **not formally assigned yet**. There is no version file or published release to use as the current version.
- Backend: **not connected**. The website does not currently provide real account authentication, order storage, order tracking, or an admin dashboard.

## Current website features

- Dark purple/black NEXUS SMP landing page.
- Rank cards generated from a static JavaScript list.
- Rank request message sharing, clipboard, and manual-copy fallback.
- Player login dialog shown as a disabled “Coming soon” placeholder.
- Server IP status message; the actual server address has not been configured.
- Responsive layout and basic keyboard/accessibility support.

## Rank catalogue

The prices below are the values currently written in the website. Do not change them without approval.

| Rank | Current price |
| --- | ---: |
| LEGEND | 250,000 Toman |
| MVP | 150,000 Toman |
| VIP | 100,000 Toman |
| KNIGHT | 75,000 Toman |
| MEMBER | 50,000 Toman |

These are displayed prices only. The current “Request rank” flow prepares a message; it does not process payments or confirm purchases.

## GitHub Pages

The site is designed to be hosted as a static GitHub Pages site:

1. Open the repository's **Settings → Pages**.
2. Check the existing publishing source before changing anything.
3. If Pages has not been configured, select **Deploy from a branch**, then choose `main` and `/(root)`.
4. Keep `index.html` at the repository root.

Do not change the current Pages configuration unless necessary and approved.

## Planned work

- Connect a dedicated Supabase project after its ownership, status, and security settings have been verified.
- Add secure user registration and sign-in.
- Store rank orders and provide order tracking.
- Add an admin dashboard with server-side authorization.
- Configure the real Minecraft server address and supported edition(s).

## Security notes

- Never commit Supabase secret keys, `service_role` keys, passwords, access tokens, or other private credentials.
- A browser client may use only the project's publishable/anon key, with Row Level Security (RLS) enabled and correctly tested on every exposed table.
- Privileged actions must be enforced server-side (for example, with a secured Edge Function); never trust a role or admin flag supplied by the browser.
- Do not reuse another project's backend without explicit approval and a security review.
- No payment gateway is configured. Do not represent a rank request as a completed purchase.

## Development

For the current static version, edit `index.html`. Preserve the listed rank names and prices unless a change is explicitly approved.

Before publishing a change, check the HTML, JavaScript, responsive layout, keyboard navigation, and reduced-motion behavior.
