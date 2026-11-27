# Mishaal Noor

I'm a CS student at the PU Lahore.
I make web and mobile apps with AI coding tools (mostly Claude Code), and I spend a lot of my time testing what comes out.

Lately I've been interested in the unglamorous parts of AI features: what happens when the input is bad, how a person can override the model, and how you prove it still works after the next change.

Portfolio: https://mishaal-portfolio.vercel.app/

LinkedIn: https://linkedin.com/in/mishaal-noor-132503433

Email: mishaalnoor32@gmail.com

I'm looking for AI assisted development roles and projects.

## Baseera

Sep to Nov 2026. I was the QA tester and a developer on a two-person team.

Baseera is a rental platform for Pakistan. Instead of sending a field agent to check a property, it runs a Claude vision model and some rule-based checks on the listing, and an admin makes the final decision. My teammate wrote the core pipeline. I tested the platform against a defect list (D01 to D32), then worked on the parts around the model:

- Locked down how images get fetched: trusted hosts only, 8 second timeout, 6 MB limit, no redirects, and 60 second signed URLs for private CNIC documents.
- Built the admin side of AI verification: an endpoint for requesting more evidence, an audit log for every AI decision, safe concurrent status updates, and the web and mobile screens that show the risk score, the risk factors and the model's summary.
- Tested the decision flow (auto-approve, needs review, auto-reject, rerun, admin override) against the thresholds of 25 and 75.
- Redid the web and mobile UI in React 19 and Expo, and fixed some backend bugs in the TypeScript/Express/Prisma API (payments, agreements, validation).
- Wrote the QA reports and tested things like stale responses, logout races and expired sessions with Playwright and Jest.

## Other projects

**FlavorVault** ([demo](https://flavorvault.ai.studio/)) is an offline-first recipe app. It's a PWA with Workbox caching, 133 recipes across 7 categories, filtering, serving size scaling, and a cooking timer based on system timestamps so it doesn't drift. React 19, TypeScript, Tailwind v4, Vite.

**KiddieSpark** ([demo](https://kiddiespark.ai.studio/)) is a learning app for kids aged 2 to 8, with phonics, counting, stories, tracing, coloring and shape matching. The tracing screen scores your strokes live on a canvas. I put effort into accessibility too: contrast, large touch targets, reduced motion and screen reader support. React, TypeScript, Canvas, Web Speech API.

## Stack

Python, C++, TypeScript, JavaScript, Dart
React, React Native / Expo, Flutter, Tailwind CSS
Express, Prisma, PostgreSQL
Claude API (vision), Playwright, Jest, Git

Based in Lahore, Pakistan.
