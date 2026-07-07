# HubSpot Pipeline + Lead Tracking

> **🔧 Confirm with Marcel/HubSpot admin:** everything below is a recommended default. If your portal already has a pipeline or properties set up differently, map this framework onto the existing setup rather than duplicating stages/fields.

---

## 1. Recommended Pipeline

**Pipeline name:** SDR/Closer Sales Pipeline

| Stage | What It Means |
|---|---|
| 1. New Lead (Sourced) | Pulled from Maps/search/directories/competitor research, not yet contacted |
| 2. Attempted Contact | At least one outreach touch made, no live conversation yet |
| 3. Contacted / Qualifying | Live conversation happened, LEAK scoring in progress |
| 4. Discovery Scheduled | Discovery appointment booked |
| 5. Discovery Completed — Pending Marcel Pricing | Handoff Summary sent, awaiting pricing/direction |
| 6. Offer Presented | Close call held, pricing presented |
| 7. Contract Sent (Stripe) | Contract + deposit link sent, awaiting signature/payment |
| 8. Closed Won | Contract signed + deposit collected |
| 9. Closed Lost | Include a "Lost Reason" property (see below) |

---

## 2. Recommended Custom Properties

| Property Name | Field Type | Options / Format | Purpose |
|---|---|---|---|
| Niche/Vertical | Dropdown | Behavioral Health / Law Firm / Home Services / Other | Reporting by niche |
| LEAK Score | Number | 0–12 | Qualifying strength at a glance |
| LEAK Notes | Text | Free text | L/E/A/K evidence detail |
| Deal Type | Dropdown | Website Build / Retainer / Both | What's actually being sold |
| Website Tier (if applicable) | Dropdown | Starter / Standard / Premium | Reporting + Marcel's pricing reference |
| Retainer Tier (if applicable) | Dropdown | Care ($500) / Growth ($1,200) / Premium Growth ($3,000) | Reporting + Marcel's pricing reference |
| Ad Spend Interest | Dropdown | Yes / No / Unsure | Flags paid-ads conversations for Marcel |
| Lead Source | Dropdown | Google Maps / Search / Directory / Competitor Research / Referral | Sourcing channel reporting |
| Decision-Maker Role | Text | e.g., Owner, Partner, GM | Confirms right-person targeting |
| Lost Reason | Dropdown | No Budget / Bad Timing / Chose Competitor / Unresponsive / Not Qualified / Other | Loss-pattern reporting |

These fields mirror the Marcel Handoff Summary fields in `07_Closing_Mechanics_and_Marcel_Handoff.md` — fill in both consistently, at the same time, so nothing lives only in an email.

---

## 3. Cadences / Sequences

If your HubSpot plan includes **Sequences** (Sales Hub Pro+), build one sequence matching the Multi-Touch Cadence in `11_Outreach_Templates_Multichannel.md`:

| Day | Sequence Step |
|---|---|
| 1 | Call + Email 1 |
| 2 | SMS 1 |
| 3 | Call 2 |
| 5 | LinkedIn touch |
| 7 | Call 3 + Email 2 |
| 10 | Call 4 + Breakup Email |

If Sequences aren't available on your plan, replicate this cadence manually using **Tasks** tied to each contact/deal — the cadence discipline matters more than the specific tool.

---

## 4. Lead Sourcing Tracker

Sourcing happens outside HubSpot (Google Maps, search, directories, competitor research) — this is the workflow for getting sourced leads *into* HubSpot cleanly.

### Sourcing Log (build this list before each dial block, then import/enter into HubSpot)

```
Business Name: ______________________
Niche: ______________________
City/Area: ______________________
Source: [Google Maps / Search / Directory / Competitor Research]
Phone: ______________________
Website: ______________________
Quick Pre-Call Read (Look/Appear at a glance): ______________________
```

**Workflow:**
1. Build a batch of 15–20 prospects using the Pre-Call Research Checklist in `03_ICP_and_Qualifying_Framework.md`.
2. Enter each as a new Contact/Company in HubSpot, stage = "New Lead (Sourced)," with Niche and Lead Source filled in immediately.
3. Move stage to "Attempted Contact" the moment the first outreach touch happens — don't batch this at end of day, do it live so the pipeline reflects reality.

---

*Related files: `07_Closing_Mechanics_and_Marcel_Handoff.md` (Handoff Summary field parity), `15_Daily_Time_Blocks_and_Scorecard.md` (daily logging rhythm).*
