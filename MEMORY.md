# Shared Memory — Idea Generation

## Akshay's Unfair Advantages
- AI verification systems (built eClean)
- Payment pipeline engineering
- Geolocation/worker marketplace expertise
- Lives in Hyderabad — ground-level understanding of Indian urban chaos
- Honeywell GenAI experience
- Brother is a data scientist
- Can build full-stack MVP solo in weeks

## Ideas KILLED (don't repeat)
- Hyperlocal commerce (exists: Dunzo, Zepto, Blinkit)
- Text-to-SQL (DataBridge — for brother, name conflicts)
- Regulation conflict detector (RuleLint — prototyping)
- Informal income proof engine (proposed but not validated)
- Price discrimination exposer (proposed but not validated)
- RERA construction verification (Aeroyantra, RERA 2.0)
- Government scheme eligibility (myScheme.gov.in)
- Compliance monitoring (TeamLease RegTech, Lawrbit)
- Court case prediction (Pre/Dicta, Manupatra, Kanoon.ai)
- Address verification API (Google Maps, GeoIQ, Mappls)
- UPI merchant disputes (NPCI UDIR)
- Environmental compliance (GeoAI/UNDP, Blue Sky Analytics)
- D2C delivery fraud (Shipfast, Pragma, CODShield AI)
- Apartment snag list (SnagEasy India)
- B2B credit scoring GST (Lendingkart, Perfios, OCEN)
- Tender bid optimizer (Minaions)
- GST audit risk scorer (C-Score, ProAnalyser, GSTHero)
- Housing society accounting (MyGate 27K+, ApnaComplex)
- BIS certificate verification (BIS CARE app)
- Commercial rent benchmark (CRE Matrix + IIMB)
- DPDPA compliance (OneTrust, Leegality)
- MSME payment delay (MSME SAMADHAAN)
- ONDC seller analytics (SellerApp, CostBo)
- Subcontractor escrow (Castler)
- Worker attendance verification (Truein)

## Ideas Under Discussion
- **PayPulse** — Recurring Payment Pre-Failure Intelligence API. SELECTED as strongest idea. No competitor globally (verified 30+ searches). Phased approach: Phase 1 uses merchant historical data only (no FIU license needed), Phase 2 partners with FIU for AA data, Phase 3 own FIU license.

## Ideas Weakened (not killed, but deprioritized)
- **BuilderCheck** — RERAScore.in exists (Maharashtra, project-level scoring). MahaRERA has official grading. Liases Foras has B2B Developer Rating. Government portal instability risk. Score: 5/10.
- **VendorLens** — Zero competitors confirmed, but execution nightmare: committee turnover, vendor political resistance, ₹500/month pricing requires 10K societies. Needs sales team, not solo dev. Score: 6/10.

## Key Discovery
- FIU license (needed for Account Aggregator access) requires ₹2cr net worth, compliance officer, 6-12 month approval. PayPulse MVP must NOT depend on AA data.
- **UPDATE (Turn 3):** Butter Payments launched "Payments Score" (Jan 2026) — predicts which FAILED subscribers will pay before recovery. Still post-failure, still US/card-based, NOT pre-debit prevention. But direction is converging. 12-18 month window.
- Razorpay launched Intelligent Retry Engine (FTX 2026, beta) — configurable retry cadence, WhatsApp recovery nudges. Still post-failure. Smart retry recovers 30% of failures.
- UPI AutoPay failure rates hit 55-90% in Aug 2025. 20M mandates revoked monthly due to low balances. Massive pain point.
- Most insurance/NBFCs DON'T use Razorpay for recurring — they use direct NACH/BillDesk/PayU NACH with ZERO intelligent retry. This is PayPulse's wedge.
- India has structural advantage: AA (2.61B accounts) + UPI AutoPay (175M txn/month, 53% of recurring) enables pre-debit intelligence impossible in card-based Western markets.
- Go-to-market: Target InsurTech (Acko, Digit) for fast pilot, not legacy insurers. Zero-risk retroactive pilot model proposed.

## Technical Decisions (Turn 4)
- Phase 1 API: POST /predict (single), /predict/batch (bulk), /webhook/outcome (learning flywheel)
- Merchant sends own historical data only — no AA/FIU dependency
- Synthetic data model (Harish): XGBoost on 100K×24mo synthetic dataset, target AUC-ROC >0.75
- Pricing: Free retroactive pilot → ₹0.50/mandate/month → ₹2 with AA → 5% success fee at scale
- UPI AutoPay mandate dates are FIXED — can't shift debit date without revoke+re-register. eNACH has flexible execution windows. Must lead with eNACH or reframe UPI value prop as pre-debit reminders.
- DPDPA compliance needed before enterprise sales. AWS India + encrypt-at-rest + process-and-delete is minimum.
- Razorpay Sprint 2026 has cash position prediction for payouts — ML infra exists, could pivot to recurring. 12-18 month window estimate may be optimistic.
- UPI AutoPay business decline rate: 74% average across top 50 banks (worse than previously noted 55-90% outlier)

## Criteria Checklist
- [ ] Nobody has built it (web search verified)
- [ ] Creates monopoly/data moat
- [ ] Buildable by 1 dev in 4 weeks (MVP)
- [ ] Clear first buyer
- [ ] India-first, global potential
- [ ] Makes people say "why hasn't anyone done this?"
