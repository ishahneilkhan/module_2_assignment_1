---
created: 2026-07-27
type: brief
status: draft
tags: [edubridge, class-3, brief]
project: EduBridge Bangladesh
brief-version: "3: interrogated synthesis"
---

# EduBridge BD: Interrogated Brief

### Who is actually using this

The parent, not the student, is the real user. v1 named the student as primary, but
Rafi confirmed the client agrees parents hold the money and make the decision — the
brief was just never updated. They're on a basic Android, mobile is a must (not
"responsive is nice to have," as v1 said — Jamie confirmed this on the call after
the brief went out). They're afraid of paying for a tutor who isn't actually
qualified, which is why v2 flags a verification badge as the thing that matters most
("trust is the main thing"). They won't finish a booking if the total cost isn't
clear upfront.

### What the contradictions actually were

1. **Device.** v1: desktop-first, mobile "nice to have." v2: Rafi says mobile is a
   must, confirmed on a call v1 doesn't reflect. Decision: mobile-first. The brief
   document is simply out of date on this point, not actually contested.

2. **Payment.** v1: one card checkout (Stripe/SSLCOMMERZ), same as UK/Australia.
   v2: Rafi says card stays for the minority who use it, but bKash/Nagad has to be
   the main path — and it isn't one screen with a different logo, it's app-switch,
   PIN, OTP, hand-typed transaction ID, then an async wait for verification.
   Decision: both paths, bKash-first. Jamie's team is treating this as a logo swap;
   the actual gap is 3-4 extra screens and new error states his UK conversion data
   (19%) never had to account for. **[Confidence: confident — this is the flow shape
   from direct personal experience paying with bKash, not a guess.]**

3. **Language.** v1: English-only, Bengali "later." v2: Jamie's manager says Bengali
   is "strongly preferred" for MVP, Jamie himself said optional. Decision: design
   Bengali UI strings now, ship English first if needed. **[Confidence: do not know —
   Jamie and his manager disagree with each other in the thread itself, so there's no
   client-side answer to defer to yet. This stays an open question, not a decision I
   can make for them.]**

4. **Primary user.** v1: student primary, parent secondary. v2: Rafi says the client
   privately agrees parents are the real decision-makers, brief wasn't updated.
   Decision: design for the parent. This exposes the biggest problem in v1 — its own
   success metric (tutor signups) doesn't measure the person actually making the
   booking decision. **[Confidence: confident — Rafi states the client already agrees
   on this; the brief is just unupdated, not actually contested.]**

5. **Scope creep.** v1: search, profile, booking, payment only. v2: client saw
   Preply and now wants video calling in the booking flow; a verification badge was
   also added. Decision: neither goes into this design cycle. Both surfaced after
   the 3-lakh/3-week budget was agreed, so they're new scope, not MVP — this goes
   into engagement.md, not just the brief.

### Scope: what I am building first, and what I am not

Building: one screen — the parent-facing tutor booking request (tutor name, subject,
verified badge, qualifications, hourly rate in BDT, single CTA) — plus the bKash
payment flow and its confirmation/receipt screen.

Not building: video calling, search and discovery, tutor onboarding, translation of
tutor-authored profile content.

### Assumptions I am carrying forward

- bKash is priority #1; Nagad is likely #2, not confirmed by Rafi yet.
- Someone on EduBridge's side verifies tutor NID/qualification documents before a
  badge is issued — not designed by me, just displayed.
- "Bengali" means UI strings only, not translating tutor-written bios.
- The 3-lakh budget covers the original MVP scope only — video calling and the
  badge are additions that weren't priced into it.

### Open questions for Rafi or Jamie

1. Who issues the verified badge and checks tutor documents? Without a named owner,
   the badge on screen has nothing behind it.
2. Bengali: Jamie says optional, his manager says strongly preferred. Which one is
   actually MVP?
3. Video calling and the trust badge both landed after the 3-lakh scope was agreed —
   is either one now in this cycle, or in a later one?
