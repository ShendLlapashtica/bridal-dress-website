# Bridal Dress Website

A small, free, owned website for a bespoke bridalwear atelier — built directly against the "A website you own — the one channel Instagram cannot be" proposal (Matrix #3), which recommended a paid hosted site builder mainly for lack of a verified open alternative, same pattern as the order-record gap. This is that alternative: static, zero hosting cost, zero maintenance burden, updatable by editing one file and redeploying.

## Scope, taken directly from the proposal

**In scope:** a home page, a page of work (gallery), a page describing how ordering works locally and from abroad, a contact section, links to Instagram/WhatsApp/Viber, the atelier's own domain (not a builder subdomain).

**Out of scope (explicitly, per the proposal):** online sales, payments, deposits, booking calendar, customer login/order tracking, a blog, multilingual translation, custom bespoke development beyond this.

**Non-negotiables respected:**
- No home address published anywhere — only the city served.
- Gallery is meant to hold **only photographs the atelier took itself** (fed by the separate "photograph every finished dress" habit) — never a bride's own wedding photos, which are usually the wedding photographer's copyright, not hers to share.
- Zero recurring cost (a domain registration is the only real expense, typically far under the stated €20-50/month combined tool ceiling).
- Nothing here creates work for the tailor.

## Before this goes live

Every `[bracketed placeholder]` in `index.html` needs a real value: atelier name, city, WhatsApp/Viber numbers, Instagram handle, email. Search for `[` to find them all.

## Updating the gallery

Add real photos as they're taken (per the photo-library habit) by editing `gallery.json`:

```json
[
  { "src": "photos/dress-1.jpg", "alt": "Bridal gown, ivory lace", "caption": "Made-to-measure, 2026" }
]
```

Put the actual image files in a `photos/` folder alongside `index.html`, then redeploy (`vercel --prod`, or push to the connected repo). No build step, no code change needed to add a photo.

## Domain

Per the proposal's own non-negotiable: register the domain in the atelier's own name (not the site builder's or a developer's), so it can never be held hostage by whoever's hosting it.
