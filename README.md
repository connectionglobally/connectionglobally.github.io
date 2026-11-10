# DateZone — Connection Globally

A mobile-friendly dating platform for adults aged 18+.

## Implemented
- Supabase Auth email/password registration, sign-in and email confirmation
- Profile onboarding, age gate (18+), profile editing and avatar uploads
- Member discovery, likes and automatic mutual matches
- Private match-only message storage
- Blocking and reporting actions
- PostgreSQL Row Level Security policies for application tables
- Supabase Storage avatar bucket and per-user upload paths

## Backend
The app connects to the Supabase project configured in `app.js` using its public publishable key. Publishable keys are designed for browser use. Never put a Supabase secret/service-role key in client code.

Migrations created:
- `create_dating_platform_core`
- `tighten_function_permissions_and_indexes`

Tables: `profiles`, `likes`, `matches`, `messages`, `blocks`, `reports`.

## Local preview
Open `index.html` with a static server, or run `npm install` then `npm run dev`.

## Free GitHub Pages deployment
The workflow in `.github/workflows/deploy.yml` builds and deploys the site when commits reach `main`.

1. Open repository **Settings → Pages**.
2. Under **Build and deployment**, choose **GitHub Actions** as the source.
3. Wait for the workflow in the **Actions** tab to finish.

Expected project URL: https://connectionglobally.github.io/connectionglobally/

## Required Supabase production setup
1. In Supabase Authentication → URL Configuration, set Site URL to the GitHub Pages URL and add it to the Redirect URLs allow-list.
2. Configure email confirmation and a reliable custom SMTP provider before public signups.
3. Test registration, confirmation, sign-in, profile completion, image uploads, likes, mutual matches, chat, block and report using two separate test accounts.
4. Add and publish Privacy Policy, Terms, Community Guidelines, moderation contact details and a process to handle reports.
5. Add abuse controls such as rate limits, anti-spam protections and moderation review before promoting the site publicly.

## Important limitations before a public launch
This is a working first product implementation, not a claim of production certification. Email deliverability, age/identity verification, live message notifications, moderation tooling, full privacy/legal pages, accessibility, abuse prevention and end-to-end testing still need to be completed. GitHub Pages is static hosting; it does not run a private server.