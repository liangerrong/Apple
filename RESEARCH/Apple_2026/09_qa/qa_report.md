# QA Report — Apple Deep Research 2026

**Date**: 2026-04-18 | **Research version**: 1.0

---

## 1. Scope Audit — Report Completeness

| Section | File | Status | Lines (est.) |
|---------|------|--------|-------------|
| §00 Executive Summary | 00_executive_summary.md | ✅ COMPLETE | ~90 |
| §01 Company and Scope | 01_company_scope.md | ✅ COMPLETE | ~120 |
| §02 Business Breakdown | 02_business_breakdown.md | ✅ COMPLETE | ~110 |
| §03 Business Model Canvas | 03_bmc.md | ✅ COMPLETE | ~130 |
| §04 Competitive Landscape | 04_competitive_landscape.md | ✅ COMPLETE | ~130 |
| §05 Moat and Sustainability | 05_moat_sustainability.md | ✅ COMPLETE | ~150 |
| §06 Outlook and Valuation | 06_outlook_valuation.md | ✅ COMPLETE | ~140 |
| §07 Risks | 07_risks.md | ✅ COMPLETE | ~130 |
| §08 Red Team | 08_red_team.md | ✅ COMPLETE (subagent) | ~140 |
| §09 References | 09_references.md | ✅ COMPLETE | ~60 |

**Scope audit**: PASS — all 10 required sections present. No section exceeds 1,500 lines.

---

## 2. Assertion Coverage — C1 Critical Assertions

| Assertion | Source Count | Independence Groups | Status |
|-----------|-------------|-------------------|--------|
| FY2025 total revenue $416.2B | 2 (S01, S02) | G1 | ✅ VERIFIED |
| iPhone revenue $209.6B | 2 (S01, S02) | G1 | ✅ VERIFIED |
| Services revenue $109.2B | 2 (S01, S02) | G1 | ✅ VERIFIED |
| Services GM% 75.4% | 2 (S01, S03) | G1, G2 | ✅ VERIFIED |
| Total GM% 46.9% | 2 (S01, S09) | G1, G2 | ✅ VERIFIED |
| Net income $112B | 2 (S09, S06) | G2, G5 | ✅ VERIFIED |
| FCF $98.8B | 2 (S01, S10) | G1 | ✅ VERIFIED |
| Share buybacks $90.7B | 2 (S01, S10) | G1 | ✅ VERIFIED |
| Cash $132.4B | 2 (S01, S10) | G1 | ✅ VERIFIED |
| Smartphone share 20% | 2 (S04, S05) | G3, G4 | ✅ VERIFIED |
| iPhone ASP $1,032 | 2 (S08, S15) | G3, G4 | ✅ VERIFIED |
| Premium share 62% | 2 (S05, S08) | G3, G4 | ✅ VERIFIED |
| EU DMA fine €500M | 2 (S01, S17) | G1, G8 | ✅ VERIFIED |
| Tariff cost $1.1B Q4 FY2025 | 2 (S01, S10) | G1 | ✅ VERIFIED |
| App Store GMV $406B | 1 (S22) | G1 (Apple primary) | ✅ VERIFIED (single primary source — Apple official disclosure) |
| Google deal material risk | 2 (S01, S17) | G1, G8 | ✅ VERIFIED |
| Q1 FY2026 revenue $143.8B | 2 (S03, S12) | G2, G6 | ✅ VERIFIED |

**C1 assertion coverage**: PASS — all C1 assertions have ≥2 sources or are from a primary official disclosure.

---

## 3. Numeric Audit

| Check | Result |
|-------|--------|
| Currency consistency | ✅ All USD millions unless noted (EU fine in EUR, explicitly labeled) |
| Fiscal year periods | ✅ FY2025 = 12 months ended Sep 27, 2025 consistently applied |
| YoY calculations | ✅ Spot-checked: Services $109.2B/$96.2B = +13.5% ✓; iPhone $209.6B/$201.2B = +4.2% ✓ |
| FCF calculation | ✅ $111,482M OCF − $12,715M CapEx = $98,767M ✓ |
| Net cash calculation | ✅ $132,420M cash − $98,657M debt = $33,763M ≈ $34B ✓ |
| EPS growth | ✅ FY2025 EPS $7.46 vs FY2024 (adjusted) ~$6.11 = ~22% ✓ (note FY2024 depressed by EU tax) |
| Services CAGR | ✅ ($109.2/$85.2)^(1/2) − 1 = 13.2% ✓ |
| Geographic total | ✅ $178.4 + $111.0 + $64.4 + $28.7 + $33.7 = $416.2B ✓ |
| Segment total | ✅ $209.6 + $33.7 + $28.0 + $35.7 + $109.2 = $416.2B ✓ |
| Products gross margin | ✅ ($307.0 − $194.1)/$307.0 = 36.8% ✓ |
| Services gross margin | ✅ ($109.2 − $26.8)/$109.2 = 75.4% ✓ |

**Numeric audit**: PASS — all key calculations verified correct.

---

## 4. Citation Match Audit

| Claim | Citation | Match? |
|-------|---------|--------|
| "Services gross margin 75.4%" | S01 (10-K) | ✅ MATCH |
| "Apple #1 globally at 20% smartphone share" | S04 (IDC) | ✅ MATCH |
| "iPhone ASP $1,032 Q4 2025" | S08 (SAG) | ✅ MATCH |
| "EU DMA fine €500M April 2025" | S17 (ProMarket) | ✅ MATCH |
| "Tariff cost $1.1B Q4 FY2025" | S10 (Motley Fool earnings call) | ✅ MATCH |
| "Google deal could materially adversely affect revenue" | S01 (10-K direct quote) | ✅ MATCH |
| "Full AI Siri delayed to 2026" | S20 (CNBC) | ✅ MATCH |
| "Q1 FY2026 revenue $143.8B (+15.7%)" | S03, S12 | ✅ MATCH |
| "ROIC 52-85%" range with buyback distortion caveat | S06, S07, S19 | ✅ MATCH — range reflects methodologies; caveat noted |
| "App Store GMV $406B US 2024" | S22 (Apple Newsroom) | ✅ MATCH |
| "FY2026 consensus EPS $7.92" | S12 (MarketBeat) | ✅ MATCH |

**Citation audit**: PASS — all cited figures match source content reviewed.

---

## 5. Uncertainty Labeling Audit

| Item | Label Used | Correct? |
|------|-----------|---------|
| FY2026 EPS forecasts | C2 — analyst estimates | ✅ |
| ROIC (all methodologies) | C2 — with buyback distortion caveat | ✅ |
| Google TAC dollar estimate ($15-20B) | C2 — third-party estimate, undisclosed by Apple | ✅ |
| AI Siri competitive capability | C2 — qualitative | ✅ |
| Installed base 2.5B devices | C2 — TIKR estimate, not disclosed by Apple | ✅ |
| Probability weights in valuation | C2 — analyst judgment | ✅ |
| WACC | C2 — multiple estimates, consensus ~9% | ✅ |

**Uncertainty labeling**: PASS

---

## 6. Contradictions Resolution Audit

| Conflict | Resolution | Adequate? |
|---------|-----------|---------|
| ROIC divergence (56% vs 85%) | Methodology difference; both exceed WACC by >40 ppts | ✅ |
| iPhone ASP: global $1,032 vs US $1,077 | Different geographies; not a conflict | ✅ |
| AI supercycle: Cook "users engaged" vs CNBC "didn't materialize" | iPhone 16 vs iPhone 17; specific to product cycle | ✅ |
| China share: full-year Huawei #1 vs Q4 Apple #1 | Time period difference; not a conflict | ✅ |

**Contradictions**: PASS — all 4 logged conflicts resolved

---

## 7. Red Team Integration Audit

| Requirement | Status |
|-------------|--------|
| ≥3 rebuttals | ✅ 4 rebuttals delivered |
| Red Team did NOT read §01–§07 | ✅ Confirmed in §08 opening statement |
| All rebuttals have evidence from raw data | ✅ Each cites specific metric/assertion IDs |
| Arbitration table complete in synthesis_notes.md | ✅ 4 rulings with rationale |
| Accept/Partial Accept items led to §06/§00 revisions | ✅ FY2027 EPS revised; P/E reduced; price target revised |
| Reject has ≥2 counter-evidence items | ✅ RR-03 rejected with 2 counter-evidence items |

**Red Team integration**: PASS

---

## Overall QA Result

| Check | Result |
|-------|--------|
| Scope audit | ✅ PASS |
| C1 assertion coverage | ✅ PASS |
| Numeric audit | ✅ PASS |
| Citation match | ✅ PASS |
| Uncertainty labeling | ✅ PASS |
| Contradictions | ✅ PASS |
| Red team integration | ✅ PASS |

**OVERALL: ✅ ALL CHECKS PASS**

---

*QA completed: 2026-04-18*
