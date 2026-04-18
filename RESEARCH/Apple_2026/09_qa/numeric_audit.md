# Numeric Audit

## Checks Performed

| Calculation | Formula | Result | Expected | Match? |
|-------------|---------|--------|---------|--------|
| Total revenue segments sum | $209,586+$33,708+$28,023+$35,686+$109,158 | $416,161M | $416,161M | ✅ |
| Geographic revenue sum | $178,353+$111,032+$64,377+$28,703+$33,696 | $416,161M | $416,161M | ✅ |
| Products GM% | ($307,003−$194,116)/$307,003 | 36.76% ≈ 36.8% | 36.8% | ✅ |
| Services GM% | ($109,158−$26,844)/$109,158 | 75.41% ≈ 75.4% | 75.4% | ✅ |
| Total GM% | $195,201/$416,161 | 46.90% | 46.9% | ✅ |
| FCF | $111,482−$12,715 | $98,767M | $98,767M | ✅ |
| Net cash | $132,420−$98,657 | $33,763M ≈ $34B | ~$34B | ✅ |
| Capital returned | $90,711+$15,421 | $106,132M | $106,132M | ✅ |
| Services CAGR FY23-FY25 | ($109,158/$85,200)^0.5−1 | 13.16% ≈ 13.2% | 13.2% | ✅ |
| iPhone % of total FY2025 | $209,586/$416,161 | 50.36% ≈ 50.4% | 50.4% | ✅ |
| Services % of total FY2025 | $109,158/$416,161 | 26.23% ≈ 26.2% | 26.2% | ✅ |
| Americas % of total FY2025 | $178,353/$416,161 | 42.85% ≈ 42.9% | 42.9% | ✅ |
| China % of total FY2025 | $64,377/$416,161 | 15.47% ≈ 15.5% | 15.5% | ✅ |
| Op margin FY2025 | $133,050/$416,161 | 31.97% ≈ 32.0% | 32.0% | ✅ |
| Net margin FY2025 | $112,010/$416,161 | 26.92% ≈ 26.9% | 26.9% | ✅ |

**All 15 numeric checks pass. No arithmetic errors found.**

## Units and Currency Verification
- All financial statement figures: USD millions ✅
- EU DMA fine: EUR millions (explicitly labeled) ✅
- iPhone ASP: USD per unit (explicitly stated) ✅
- Market share: percentage points (explicitly stated) ✅
- App Store GMV: USD billions (explicitly stated as $406 billion) ✅

## Period Consistency
- FY2025 = 12 months ended September 27, 2025 ✅
- Q1 FY2026 = 3 months ended December 28, 2025 ✅
- CY2025 smartphone data = Calendar year 2025 (IDC) — distinguished from fiscal year ✅

**Numeric audit: PASS**
