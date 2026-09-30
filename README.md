# CredBridge

> **Embedded credit infrastructure for lenders.**

CredBridge is a lender-embedded software layer for thin-file lending. It turns a borrower's consented cash-flow data into an explainable credit profile, a multilingual borrower journey, and an audit trail that the lender can use inside its own lending process.

CredBridge is **not a lender** and is not positioned as a standalone borrower product. The lender keeps the regulated lending decision, licence, loan agreement and disbursement responsibility.

## Product

CredBridge plugs into a lender's existing credit flow and adds a borrower-friendly cash-flow layer.

```text
Lender system
     │
     ├── API / SDK
     ├── White-label link / QR
     └── Lender dashboard
             │
             ▼
     Borrower journey
     Language → Consent → Cash flow →
     Factors → Explanation → Safe instalment
             │
             ▼
     Lender policy bands
             │
             ▼
     Matched offer + audit trail
```

## Who We Serve

### Customers
Banks, co-operative banks, small finance banks and NBFCs.

### End users
Kirana owners, small merchants and later gig workers whose income reaches a bank account through UPI or platform payouts but who may have a thin or incomplete conventional credit file.

## The Lender Problem

Thin-file borrowers can be expensive to assess. A conventional credit number also does not explain the underlying cash-flow story to a borrower in a language they understand. Lenders need a clearer view, borrower-friendly explanations and an auditable journey without giving up control of the decision.

## The Borrower Problem

A loan offer can show a price without showing a clear reason. CredBridge adds reason codes, plain-language explanations and multilingual voice so the borrower can understand the signals being used.

## Delivery Model

1. **API / SDK** — embedded inside the lender's existing loan system.
2. **White-label link / QR** — the lender or field agent shares a lender-branded journey.
3. **Lender dashboard** — internal workspace for profiles, explanations and matched offers.

The borrower reaches the journey through the lender's channel.

## Core Capabilities

- Consent-led cash-flow analysis
- Explainable 0–900 prototype credit profile
- Four transparent score factors
- Multilingual borrower explanations
- English, Hindi and Tamil voice support in the demo
- Safe-instalment calculation
- Offer matching inside lender-set bands
- Lender-side profile and audit view
- Automatic re-scoring after simulated transactions
- No borrower fee in the proposed business model
- No handling of loan funds

## Two Innovations

### 1. Borrower-language explanation layer

CredBridge generates plain-language reason codes and voice explanations so the lender can show the borrower why the profile looks the way it does. The explanation can be retained as part of the audit trail.

### 2. Policy-bounded offer matching

CredBridge does not make an autonomous lending decision or bargain with lenders. It matches the borrower's requested amount and repayment capacity against lender-defined policy bands and surfaces an illustrative offer.

## Demo Score

The current prototype calculates a transparent score from four simulated signals:

- Income consistency
- Repayment rhythm
- Cash-flow buffer
- Transaction activity

The score is intentionally rule-based for the hackathon. AI services are used for wording, lender briefs, matching support and text-to-speech; the lender remains the decision-maker.

## Business Model

**Customer:** lenders.

**Revenue:** platform fee per lender plus per-journey fee.

**Borrower price:** proposed to be zero.

**Validation status:** pricing and lender demand are unvalidated and should be described as **tested in pilot** only when a real pilot has occurred.

## Go-to-Market

Start with one lender and one 90-day pilot targeting the small-merchant / kirana segment. The proposed pilot size is 50–200 applicants. Gig-worker use cases follow through partner lenders.

A practical prospecting list can start with regulated entities already active in the Account Aggregator ecosystem and lending use cases.

## Regulatory Positioning

The product is designed around a lender-led model: the regulated lender owns the lending decision and customer relationship. CredBridge supplies software and workflow support.

Relevant areas to validate before production include:

- RBI Digital Lending Directions, 2025 and Key Fact Statement requirements
- Multi-lender offer disclosure requirements
- Lending service provider responsibilities
- Direct movement of loan funds between borrower and lender accounts where required
- RBI FREE-AI recommendations on responsible AI
- RBI draft guidance on model risk management
- Digital Personal Data Protection Act / Rules requirements
- Account Aggregator consent and data-flow requirements

This README is a product-positioning summary, not legal advice. Clause-level regulatory claims should be checked against the primary RBI and MeitY texts before presentation or deployment.

## Market Signals

### UPI
NPCI reports **24,508.96 million UPI transactions in August 2026**, equivalent to about **24.51 billion transactions**.

### MSME credit gap
Public estimates vary materially by methodology and year. A lender pitch can describe the opportunity as roughly **₹25 lakh crore to ₹80 lakh crore**, but the underlying Deloitte and NITI Aayog estimates should be cited separately rather than presented as one single measured figure.

### Gig economy
The Economic Survey 2025–26 reports approximately **120 lakh gig workers in FY25** and cites a projection of **2.35 crore by 2029–30**.

## Pilot Metrics

A first lender pilot should measure:

- time taken to explain key terms
- borrower repeat-back / comprehension of terms
- journey completion rate
- drop-off at consent
- explanation delivery success
- lender processing time
- match rate within lender policy
- documentation / audit completeness

## Tech Stack

The hackathon prototype uses:

- HTML / CSS / vanilla JavaScript
- Vercel-compatible static deployment
- Groq Llama 3.3 70B for wording in the planned AI layer
- Sarvam voice for multilingual speech in the planned AI layer
- simulated transaction data

## Running Locally

```bash
git clone https://github.com/YOUR_USERNAME/credbridge.git
cd credbridge
python3 -m http.server 8000
```

Open `http://localhost:8000`.

The current frontend expects optional API routes for AI functions. Without those routes, the demo can still use its local rule-based behaviour and browser voice fallback.

## Demo Disclosure

This is a hackathon prototype.

- No real UPI account is connected.
- No real lender is connected.
- No real loan is issued.
- All borrower transactions are simulated.
- All lender profiles and terms are fictional.
- The score is not a production underwriting model.
- The lender, not CredBridge, makes the final lending decision.

## Sources

- NPCI — UPI Product Statistics: https://www.npci.org.in/product/upi/product-statistics
- Economic Survey 2025–26 — Government of India: https://www.indiabudget.gov.in/economicsurvey/
- NITI Aayog — Enhancing Competitiveness of MSMEs in India: https://www.niti.gov.in/
- RBI — Digital Lending / Digital Lending Directions, 2025: https://www.rbi.org.in/
- RBI — FREE-AI Committee Report: https://www.rbi.org.in/
- MeitY — Digital Personal Data Protection Rules, 2025: https://www.meity.gov.in/
- Sahamati — Account Aggregator ecosystem: https://sahamati.org.in/

## Team

**Doomsday Hackathon · Fintech Track**

**Team:** For_Doom

**Team Lead:** Rishe S

**Team Members:** Rishe S, Krisshiv M, K. Hitesh Sai, Aditya R

## License

MIT
