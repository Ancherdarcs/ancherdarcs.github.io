# AGENTS.md — Ancherd Arcs

Guidance for AI agents working on this repository.

## What this project is

Ancherd Arcs is a ministry-first community platform. The mission: help
believers stay anchored in Christ through every season of life, share their
arcs (testimonies), gather for Bible study and fellowship, and wear clothing
that opens doors for the Gospel.

## Prime directive: mission over merchandise

**Always lead with the mission, not the pieces.** The clothing collection is a
means, not the end. When writing copy, designing layouts, prioritizing work,
or restructuring the site, the order of emphasis is:

1. The mission — Scripture, testimonies ("arcs"), community, support
2. The connection — the badge that links like-minded believers to real people
   and real stories (the long-term networking vision)
3. The collection — specific garments exist to serve #1 and #2

Never turn the site into a standard e-commerce storefront. If a change would
make Ancherd Arcs feel like a shop with a blog attached, it is wrong. It
should feel like a ministry with a wardrobe.

## Current goals (in order)

- Polish and properly launch the live site (style refresh, performance, SEO)
- Strengthen arcs/community features (Supabase-backed)
- Design the badge experience: tap/scan → a believer's arc → connection
- Build out collection pieces last, in service of the above

## Technical context

- Static multi-page site (plain HTML/CSS/JS) deployed on GitHub Pages
  (repo: Ancherdarcs/ancherdarcs.github.io)
- Backend: Supabase (auth + arcs storage). The `sb_publishable_` key in
  `js/main.js` is meant to be public; all security depends on Row Level
  Security being enabled on every table in the Supabase dashboard.
- Newsletter: Mailchimp form in the footer.
- The stray root-level `main.js` is legacy — `js/main.js` is the real one.

## Conventions

- Keep it dependency-light: plain HTML/CSS/JS unless a build step is
  explicitly approved.
- Warm, reverent copy. Scripture references are welcome and expected.
- Accessibility is non-negotiable: semantic HTML, alt text, aria states,
  keyboard-friendly navigation.
- Mobile-first: most visitors will arrive on phones, often via the badge.
