# Mishaal Noor

I'm a CS student at  PU Lahore.
I make web and mobile apps with AI coding tools (mostly Claude Code , antigravity etc), and I spend a lot of my time testing what comes out.

Lately I've been interested in the unglamorous parts of AI features: what happens when the input is bad, how a person can override the model, and how you prove it still works after the next change.

Portfolio: https://mishaal-portfolio.vercel.app/

LinkedIn: https://linkedin.com/in/mishaal-noor-132503433

Email: mishaalnoor32@gmail.com

I'm looking for AI assisted development roles and projects.

## Baseera

Sep to Nov 2026. worked as a QA tester and  AI assisted developer on an experience based contract .

## Baseera

Sep to Nov 2026. QA tester and developer on a two-person team.

Baseera is a rental platform in Pakistan where owners list properties for tenants. Normally someone from the company would visit each property to check it's real. Baseera does that check with software instead. First it runs simple rule checks, like missing documents, duplicate photos and the photo's GPS location. Then a Claude vision model looks at the property photos and the owner's CNIC (national ID). All of this gives the listing a risk score, and the score decides one of three things: approve it, send it to an admin, or reject it. A real person (the admin) always has the final say.

My teammate built the main verification pipeline. I had two jobs: testing the whole platform, and building the parts around the AI.

**Testing**
- Checked the platform against a list of 32 known problems (D01 to D32) and kept written QA reports on what was fixed and what was left.
- Verified every AI decision state—auto-approve, needs review, auto-reject, re-evaluation, and admin override—ensuring accurate routing across configurable confidence thresholds.
- Tested what happens when things go wrong: old responses arriving late, logging out in the middle of a request, and sessions expiring. I used Playwright for browser tests and Jest for code tests.

**Making the AI part safer**
- The system downloads images from links, which can be risky. I limited it to trusted sources only, a timeout of 8 seconds, a 6 MB size limit, and no redirects.
- CNIC photos are private, so they are shared only through signed links that stop working after 60 seconds.

**Admin tools**
- Built the way an admin can ask the owner for more evidence, using a fixed list of allowed request types.
- Added a log that records every AI decision, so it's clear what happened and when.
- Made status updates safe when two people change the same listing at once.
- Built the web and mobile screens where the admin sees the risk score, the reasons behind it, and the model's summary.

**App and backend work**
- Redesigned the web and mobile apps (React 19 and Expo) with light and dark themes, different screens for different user roles, a notification bell and a chat panel.
- Fixed bugs in the backend (TypeScript, Express, Prisma), including payments, agreements, input checks, creating a listing safely when a request is sent twice, and clearer error messages.

Stack: Claude API, TypeScript, Express, Prisma, React 19, Expo, Playwright, Jest

## Other projects

## FlavorVault

A recipe app that works offline and can be installed on a phone like a normal app. I built it with AI coding tools and directed the development.

Live demo: https://flavorvault.ai.studio/

What I decided and designed:
- The recipe data. I designed a dataset of 133 recipes in 7 categories, with quantities in a consistent format, nutrition info, tags and the time for each step. This is what lets the app filter by several things at once and scale ingredients when you change the servings.
- The data is structured so an AI feature could be added later.
- How the cooking timer should behave: it uses the system clock so it doesn't drift, it can be paused and adjusted, and it gives a chime and vibration at the end.
- That preferences, favorites, collections and checklists are saved between visits.

Tools used: React 19, TypeScript, Tailwind CSS v4, Vite 6, Workbox.

## KiddieSpark

A learning app for kids aged 2 to 8 that can be installed on a phone. It has phonics, counting, read-along stories, tracing, coloring and shape matching. I built it with AI coding tools and directed the development.

Live demo: https://kiddiespark.ai.studio/

What I decided and asked for:
- The six learning modules and that it should be mobile-first.
- A tracing screen that scores a child's stroke right away.
- Read-aloud stories with an auto-read switch that can be turned off, for children who find sound too much.
- Accessibility from the start: good colour contrast, large touch targets, reduced-motion support and screen reader support.
- Safe saving of progress, with a fallback if the browser blocks storage.

Tools used: React, TypeScript, Tailwind CSS, Motion, HTML5 Canvas.
## Stack

Python, C++, TypeScript, JavaScript, Dart
React, React Native / Expo, Flutter, Tailwind CSS
Express, Prisma, PostgreSQL
Claude API (vision), Playwright, Jest, Git

Based in Lahore, Pakistan.
