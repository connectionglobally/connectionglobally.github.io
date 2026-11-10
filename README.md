# DateZone — dating platform prototype

DateZone is an adults-only (18+) dating platform concept. This repository has been redesigned from the former QuickSales storefront into a responsive dating-site interface.

## Current interface
- Discover member-style profiles and filter by city or interests
- Like profiles and review your likes
- Preview matches and open a conversation screen
- Edit a sample profile form
- Safety centre with dating safety guidance
- Responsive desktop and mobile navigation

## Important: prototype, not yet a live dating service
This version is a front-end prototype. Sample profiles and photos are illustrative. Likes, sample matches and messages are held only in the current browser session. Messages are NOT delivered to another person. There is no real registration, login, identity/age verification, persistent database, photo upload, moderation, blocking/reporting workflow, or private multi-user chat yet.

Before inviting members, connect a secure backend such as Supabase: Auth for registration and email verification; PostgreSQL for profiles, preferences, likes, matches, blocks, reports and messages; Row Level Security so only matched members can read and send each other's messages; private Storage for photos; realtime message delivery; rate limits and moderation. DateZone is intended for adults aged 18+ only. Never put service-role keys or secrets in browser JavaScript.

## Publish
Keep the current repository name for now. Configure GitHub Pages in Settings → Pages and check the URL shown there. The repository address can be changed later.

Files: index.html (page shell), styles.css (design), app.js (prototype interactions).