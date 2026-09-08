# KLAVE — Waitlist

Landing page for **KLAVE**, the underground beat marketplace where AI does the work producers hate most — finding the right audience. Meet NERO 🖤

> Formerly known as SPLICE.

## What this is

A single-page waitlist site. Visitors enter their email, NERO "reaches out when the doors open." That's it — no backend beyond email capture.

## Stack

- Plain HTML/CSS/JS — no framework, no build step
- Firebase (Firestore) for storing waitlist emails
- Google Fonts: Bebas Neue, Space Mono, DM Sans
- Deployed on Vercel

## Structure

```
index.html   → entire site (markup, styles, and waitlist logic in one file)
```

## Firebase

Waitlist submissions are written to a `waitlist` collection in Firestore:

```js
{
  email: string,
  joinedAt: serverTimestamp(),
  source: "splice-waitlist-page"
}
```

Firebase config is inline in `index.html`. The project is still registered under the old name (`splice-waitlist`) — renaming it would mean migrating to a new Firebase project, so it's left as-is for now.

## Local dev

No build step. Just open `index.html` in a browser, or serve it locally:

```bash
npx serve .
```

## Deploy

Push to the connected GitHub repo — Vercel auto-deploys on push to `main`.

## Brand

- **KLAVE** wordmark: white text, blue "A" (`#7CB9FF`)
- Palette: near-black background (`#0A0A0A`), white/silver text, blue accent
- By Northhhern Labs
