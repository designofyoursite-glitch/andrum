# Meta Ads Test Log — Free SOS Practice Launch 01

Date logged: 2026-06-15  
Traffic period analyzed: approximately 3 days  
Channel: Meta Ads  
Offer: free SOS practice lead magnet  
Main landing page: `andrum-website/index.html`  
Product: SOS Practices, 7 guided breathwork audios for acute anxious-attachment moments

## Purpose

This document is the shared source of truth for the first Meta Ads test around the free SOS practice.

Use it before creating new ads, changing the landing page, reviewing funnel performance, or briefing anyone on what has already been tested.

The current goal is not scale. The goal is to validate whether cold traffic can move through:

`Meta ad -> landing page -> free practice opt-in -> Teachable practice access -> paid SOS Practices purchase`

## How To Store Marketing Data Going Forward

The project now needs a repeatable storage system for performance data, not just one-off analysis notes.

### Option 1: One File Per Test

Store every campaign, ad test, landing page test, email test, or launch test as a separate dated file.

Example:

- `outputs/marketing/2026-06-15-meta-ads-free-practice-launch-01.md`
- `outputs/marketing/2026-06-22-meta-ads-free-practice-modal-test.md`
- `outputs/marketing/2026-06-29-free-practice-email-followup-test.md`

Pros:

- Easy to commit.
- Easy for a teammate to read.
- Keeps context, screenshots, numbers, interpretation, and decisions together.
- Works well for MVP-stage learning.

Cons:

- Harder to compare many tests unless someone creates a summary table later.

Best use:

- Early-stage MVP testing.
- Tests where qualitative interpretation matters as much as numbers.

### Option 2: Central Funnel Dashboard File

Keep one master file that summarizes all tests and links out to detailed notes.

Example:

- `outputs/marketing/funnel-dashboard.md`

Possible sections:

- current funnel snapshot;
- latest campaign metrics;
- test history table;
- active hypotheses;
- open data gaps;
- next decisions.

Pros:

- Best for a quick overview.
- Helps avoid rereading every test file.
- Useful for weekly marketing reviews.

Cons:

- Needs discipline to update after every test.
- Can become too long if detailed analysis lives there instead of linked files.

Best use:

- Once there are 3+ tests to compare.
- When more than one person works on marketing.

### Option 3: Structured CSV / Spreadsheet For Metrics

Store raw campaign metrics in a spreadsheet or CSV, with analysis in markdown files.

Example:

- `research/analytics/meta-ads-tests.csv`
- `outputs/marketing/2026-06-15-meta-ads-free-practice-launch-01.md`

Possible columns:

- date range;
- campaign;
- ad set;
- ad name;
- spend;
- impressions;
- reach;
- link clicks;
- landing page views;
- leads;
- purchases;
- CTR;
- CPC;
- CPL;
- notes file.

Pros:

- Best for comparing numbers over time.
- Easier to calculate trends.
- Easier to import into spreadsheets later.

Cons:

- Does not capture enough qualitative context by itself.
- Needs clean data entry.

Best use:

- After the first few tests, when trend analysis starts mattering.

### Option 4: Split By Funnel Area

Store files by workstream:

- `outputs/ads/` for ad creative tests and scripts;
- `outputs/landing-pages/` for landing page copy and conversion tests;
- `outputs/email/` for email sequence performance;
- `outputs/marketing/` for cross-funnel analysis.

Pros:

- Matches existing folder logic.
- Good when different collaborators own different areas.

Cons:

- A single test can touch multiple folders.
- Harder to reconstruct the full funnel story unless there is a central summary.

Best use:

- Mature workflow with clear ownership.

## Recommended Storage System

Use a hybrid of Option 1 and Option 2 now, then add Option 3 when there are more tests.

Recommended operating structure:

1. Keep one detailed markdown file per test in `outputs/marketing/`.
2. Create a future master dashboard in `outputs/marketing/funnel-dashboard.md` once there are at least 3 tests.
3. Later add `research/analytics/meta-ads-tests.csv` when comparison across tests becomes painful in markdown.
4. Keep ad scripts and new creative concepts in `outputs/ads/`, but link to them from the relevant test log.
5. Keep landing page copy changes in `outputs/landing-pages/` only if they are draft copy; keep performance conclusions in `outputs/marketing/`.

For now, this file is the canonical record for Launch 01.

## What Every Test Log Should Include

Each future test log should contain:

- date range;
- objective;
- offer;
- traffic source;
- campaign/ad set/ad names;
- creative copy or screenshot description;
- landing page URL or file state;
- spend;
- impressions;
- reach;
- clicks;
- CTR;
- CPC;
- landing page views;
- leads;
- purchases, if available;
- revenue, if available;
- facts;
- hypotheses;
- what cannot be concluded yet;
- main bottleneck;
- next action;
- decision made.

This prevents the team from repeating the same analysis from screenshots.

## Project Context

Andrum is currently testing a specific entry point:

- acute relationship anxiety;
- anxious attachment spirals;
- the moment after a message, silence, or delayed reply;
- body-first support through a short guided breathwork practice.

The strongest strategic frame from the repository:

- lead with emotional recognition, not education;
- make the viewer feel "this is exactly what happens inside me";
- do not sell breathwork as a concept before the person recognizes the moment;
- for the acute segment, reduce decision-making and make the next action feel immediate.

Relevant internal sources:

- `strategy/current-instagram-strategy.md`
- `strategy/content-performance-rules.md`
- `brand/ANDRUM — Brand Platform 3227c43c1eb18010a3fdf1a45e883f9b.md`
- `product/sos-practices/SOS Practices — Guide & How it works d530afaad51240ceb15f2e5c246204b5.md`
- `research/customer-journey/CJM (путь клиента) 2ec7c43c1eb18192a31ad3a392d8559f.md`

## Landing Page State At Time Of Test

The landing page on GitHub matched the local file at the time of review.

Repository checked:

- GitHub remote: `https://github.com/designofyoursite-glitch/andrum-website.git`
- Branch: `main`
- File: `andrum-website/index.html`

Important landing page elements:

- Hero headline: `He's read it. He hasn't replied. Here's what to do right now.`
- Hero CTA: `Try the first practice free`
- Secondary paid CTA above the fold: `Get all 7 practices — $19`
- Free practice form appears in a modal.
- MailerLite form submits to form ID `41481387`.
- On successful MailerLite submit, the site tracks Meta `Lead`.
- After submit, the site redirects to the Teachable lecture page for the free practice.
- Paid checkout CTA tracks `InitiateCheckout` before sending the user to Teachable checkout.

Relevant implementation details in `andrum-website/index.html`:

- Meta Pixel PageView is initialized in the page head.
- `trackMetaLeadOnce()` sends `fbq('track', 'Lead')`.
- `ml_webform_success_41481387()` redirects to the free practice on Teachable.
- `data-checkout-link` clicks send `InitiateCheckout`.

## Ad Creative Tested

Known winning/primary creative from the test:

Ad name in Meta:

- `Free SOS Practice Reel – I'm too much`

Visible creative text:

```text
He hasn't replied.

And suddenly it feels like proof:
"I'm too much."
"I did something wrong."
"He's pulling away."

It was just silence. But your body read it as rejection.

TRY THE FREE 6-MINUTE SOS PRACTICE
```

Other ads visible in the test:

- `Free SOS Practice Reel – He's read`
- `Free SOS Practice Reel – Pattern`

## Meta Ads Results

Overall results from the screenshots:

| Metric | Result |
| --- | ---: |
| Amount spent | $20.74 |
| Impressions | 3,985 |
| Reach | 3,488 |
| Frequency | 1.14 |
| Link clicks | 281 |
| Landing page views | 248 |
| CPC, link click | $0.07 |
| CTR, link click | 7.05% |
| CTR, all | 9.39% |
| CPC, all | $0.06 |
| CPM | $5.20 |
| Cost per landing page view | $0.08 |

Derived metric:

- Landing page view rate from link clicks: `248 / 281 = 88.3%`

Interpretation:

- The ad-to-page handoff is technically healthy enough.
- A large majority of link clicks become landing page views.
- The traffic is inexpensive.
- The creative is generating attention and curiosity.

## Ad-Level Results

| Ad | Spend | Impressions | Reach | Frequency | Link clicks | CTR link | CPC link | LPV | Cost / LPV |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Free SOS Practice Reel – He's read | $3.10 | 642 | 539 | 1.19 | 40 | 6.23% | $0.08 | 36 | $0.09 |
| Free SOS Practice Reel – Pattern | $1.13 | 225 | 210 | 1.07 | 15 | 6.67% | $0.08 | 16 | $0.07 |
| Free SOS Practice Reel – I'm too much | $16.51 | 3,118 | 2,852 | 1.09 | 226 | 7.25% | $0.07 | 196 | $0.08 |

Quality diagnostics shown by Meta:

- For `He's read` and `I'm too much`:
  - Quality ranking: below average, bottom 35%.
  - Engagement rate ranking: above average.
  - Conversion rate ranking: below average, bottom 35%.
- For `Pattern`, rankings were not available in the screenshot, likely because the sample was too small.

Interpretation:

- `I'm too much` received most spend and maintained the best CTR link.
- Meta had enough signal to favor it.
- Engagement is not the problem.
- Conversion rate ranking suggests post-click or lead conversion is weak relative to similar ads.

## MailerLite / Form Results

MailerLite form shown:

- Form: `Free Practice Form`
- Created: 2026-05-19
- Last registration at screenshot time: 19 hours ago

MailerLite reported:

| Metric | Result |
| --- | ---: |
| Visitors | 562 |
| Subscribers | 8 |
| Conversion | 1.42% |

Derived against Meta LPV only:

- `8 subscribers / 248 Meta LPV = 3.2%`

Important caveat:

- MailerLite visitors and Meta landing page views may not use the same attribution window or counting method.
- The true cold Meta opt-in rate is probably between 1.42% and 3.2%, based on the available screenshots.

## Funnel Diagnosis

Current observed funnel:

| Stage | Count | Notes |
| --- | ---: | --- |
| Impressions | 3,985 | Meta |
| Link clicks | 281 | Strong CTR for cold traffic |
| Landing page views | 248 | 88.3% of link clicks |
| MailerLite visitors | 562 | Different source/definition from Meta |
| Subscribers | 8 | Weak opt-in volume |

Main bottleneck:

`landing page / form visitor -> email subscriber`

The top of funnel is working better than the lead capture step.

## Facts

- CTR link is high for cold traffic at 7.05%.
- CPC link is low at $0.07.
- Cost per landing page view is low at $0.08.
- Landing page views are 88.3% of link clicks, so click quality and page loading are not the first suspected issue.
- Opt-in is low: 1.42% by MailerLite visitor data or 3.2% against Meta LPV.
- Meta's engagement ranking is above average for the main ads.
- Meta's conversion ranking is below average for the main ads.

## Hypotheses

These are not facts yet.

1. The ad promise is more emotionally specific than the modal.
   - Ad: silence feels like rejection, "I'm too much", body reaction.
   - Modal: `Get the free SOS practice.`
   - This may feel like a generic lead magnet after a very specific emotional click.

2. The modal may feel like an email signup instead of instant SOS access.
   - The acute segment needs one button and low friction.
   - The user came for immediate relief, not a newsletter relationship.

3. The paid CTA above the fold may split the first action.
   - Cold traffic may need one primary action first: get the free practice.
   - Purchase can be introduced after the practice or in follow-up.

4. The landing page is strong as a product page but may be too broad for ad traffic.
   - It introduces the full 7-practice product early.
   - The ad traffic may need a shorter, free-practice-specific page.

5. The creative may be attracting emotionally curious clicks that are not yet ready to exchange email.
   - This is why the next test should not change creative first.
   - First isolate the landing/modal conversion problem.

## What We Cannot Conclude Yet

- We cannot conclude that paid acquisition is profitable.
- We do not yet have purchase conversion from subscribers.
- We do not yet have Teachable practice consumption data.
- We do not know how many people opened the modal.
- We do not know how many people started typing in the form.
- We do not know how many users reached the free practice after redirect.
- We cannot make reliable conclusions about the `Pattern` ad because spend and sample are too small.

## Current Working Conclusion

The first Meta Ads test produced a promising top-of-funnel signal but did not yet validate the full funnel.

The immediate priority is not finding a new creative. The immediate priority is improving and measuring the opt-in step.

Target:

- First milestone: raise cold LPV -> lead from approximately 1.4-3.2% to 6-8%.
- Next milestone: raise cold LPV -> lead to 8-15%.

## Recommended Next Test

Keep the strongest ad creative active as the traffic control:

- `Free SOS Practice Reel – I'm too much`

Do not change the creative and landing experience at the same time unless clearly marked as a new test.

### Test 01: Modal Message Match

Control modal:

```text
Get the free SOS practice.
Leave your email and the free practice will arrive in your inbox. No card needed.
CTA: Get Instant Access
```

Variant modal:

```text
He hasn't replied.
Open this before you text again.

Enter your email and go straight to the 6-minute practice for the moment your body reads silence as rejection.

CTA: Open the practice now

No card. No app. Opens immediately after signup.
```

Reason:

- This keeps the visitor inside the same emotional moment that made them click.
- It reframes email as the access step, not as a subscription.

### Test 02: Ad-Specific Landing Page

Create a short ad traffic page, for example:

- `/free-practice.html`
- `/sos-free.html`

Recommended structure:

1. Hero repeats the ad scenario.
2. Embedded email field or immediate CTA.
3. 20-second audio preview.
4. Three bullets explaining exactly what happens after email.
5. One proof/review tied to the free practice.
6. Final CTA.

For this ad-specific page, remove the paid CTA above the fold.

Reason:

- The cold traffic job is to get the free practice.
- The paid product can be sold after the practice or in email.

### Test 03: Modal vs Embedded Form

Test:

- Variant A: modal after CTA click.
- Variant B: email field embedded in the hero.

Example embedded hero:

```text
He's read it. He hasn't replied.

Try the 6-minute practice before your body turns silence into rejection.

[Email field]
[Open the practice now]

No card. Opens immediately.
```

Reason:

- If embedded form wins, the issue is partly extra click / modal friction.
- If modal wins, the issue is more likely copy, trust, or offer framing.

## Measurement Plan

Add or confirm these events:

| Event | Why it matters |
| --- | --- |
| `free_practice_click` | Measures CTA/modal open intent |
| `form_start` | Measures whether users begin the email step |
| `Lead` | Measures successful signup |
| `redirect_to_practice` | Confirms successful handoff to Teachable |
| `InitiateCheckout` | Measures paid CTA intent |
| `Purchase` | Needed for profitability analysis |

Implementation update, 2026-06-15:

- `FreePracticeClick` Meta custom event added on free practice CTA/modal open.
- `free_practice_click` GA4 event already existed and remains active.
- `FreePracticeFormStart` Meta custom event added on first email input focus or input.
- `form_start` GA4 event added on first email input focus or input.
- `RedirectToPractice` Meta custom event added immediately before redirect to Teachable free practice.
- `redirect_to_practice` GA4 event added immediately before redirect to Teachable free practice.
- `Lead` Meta standard event remains active after successful MailerLite submit.
- `InitiateCheckout` Meta standard event remains active on paid checkout clicks.
- Website implementation commit: `58e9228 Add free practice funnel tracking` in `designofyoursite-glitch/andrum-website`.

Core ratios:

- CTA click rate: `free_practice_click / landing_page_view`
- Form start rate: `form_start / free_practice_click`
- Form completion rate: `Lead / form_start`
- Modal conversion rate: `Lead / free_practice_click`
- Total opt-in rate: `Lead / landing_page_view`
- Paid intent rate: `InitiateCheckout / Lead`
- Purchase conversion: `Purchase / Lead`

## Decision Rules

Do not make strong conclusions before there is enough sample.

Minimum directional sample:

- 100-150 landing page views per landing/modal variant.

Better sample:

- 250+ landing page views per variant.

If CTA click rate is low:

- Hero, CTA, or page motivation is the issue.

If CTA click is healthy but form start is low:

- Modal/form trust and message match are the issue.

If form start is healthy but lead completion is low:

- Email friction, MailerLite form behavior, mobile usability, or submit trust is the issue.

If lead rate improves but purchases do not:

- The next bottleneck is free practice experience, email follow-up, Teachable product page, or paid offer.

## Quality Gate Notes

### Critic Subagent

Performance diagnosis:

- Strong as an internal marketing log because it separates facts, hypotheses, and missing data.
- The original analysis risked over-weighting the success message text even though the site redirects after submit.
- The most important fix was to make the bottleneck precise and avoid treating a likely invisible success message as the main issue.

Required fixes applied:

- Clarified that redirect happens after successful submit.
- Kept the success-message note out of the main diagnosis.
- Added measurement events to locate the actual drop-off.
- Marked MailerLite vs Meta count mismatch as a caveat.

Final critic verdict: PASS WITH MINOR EDITS.

### Acceptance Subagent

Fix verification:

- FIXED: Data and screenshots are summarized in one reusable place.
- FIXED: Facts are separated from hypotheses.
- FIXED: The current landing implementation is captured.
- FIXED: The redirect behavior is acknowledged correctly.
- FIXED: Next actions are concrete and tied to funnel measurement.

Final gate: APPROVED.
