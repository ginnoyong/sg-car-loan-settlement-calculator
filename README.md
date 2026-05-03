# sg-car-loan-settlement-calculator
SG CAR LOAN SETTLEMENT CALCULATOR


A free, browser-based calculator for Singapore car buyers to analyse the optimal month to settle a hire-purchase loan early.

No installation. No sign-up. No data sent anywhere. Everything runs locally in your browser.

---

## What it does

When you take a car loan in Singapore, the total interest is pre-calculated upfront and spread across your monthly instalments. If you settle early, you avoid paying future interest — but you may incur an early termination penalty and lose any finance rebate that was tied to completing the full loan term.

This calculator helps you:

- See the full monthly breakdown of your loan — interest portion, principal portion, cumulative totals, and remaining balances
- Find the **optimal month to settle** — the month where your total cost of the car is lowest
- Understand the trade-off between interest saved, termination penalty, and finance rebate clawback at any given settlement month
- Compare three common loan structures used in Singapore

---

## Loan structures supported

| Structure | Description |
|---|---|
| **Rule of 78** | Standard Singapore hire-purchase. Interest is front-loaded — early months consume a larger share of total interest. Early settlement rebate uses the smaller tail-end weights. |
| **Flat rate — pro-rata** | Interest spread equally across all months. Rebate on early settlement is strictly proportional to remaining months. |
| **Reducing balance (EIR)** | Interest accrues on the outstanding principal each month. Common in bank term loans. Payoff amount equals remaining principal only. |

---

## Formula used

```
Penalty          = remaining principal × penalty %

Total car cost   = down payment
                 + loan principal
                 + cumulative interest paid
                 + penalty
                 + clawback

Saving vs full term = total car cost at full term
                    − total car cost at settlement month

Optimal month    = month with lowest total car cost
```

**Note:** The remaining interest you never pay simply disappears when you settle early — it is not added or subtracted from the settlement amount. It is already captured in the saving figure.

---

## How to use

1. Enter your **car price** (after all discounts) and **down payment** — the principal is auto-calculated
2. Enter your **annual flat interest rate** and **loan tenure in months**
3. Select your **loan structure**
4. Set your **early termination penalty %** (check your loan agreement — typically 1.5% to 3% in Singapore)
5. Toggle the **finance rebate clawback** on or off and enter the amount if applicable
6. Click **Find optimal settlement month** — the calculator will identify the month with the lowest total cost and auto-populate the settle month field with the full breakdown
7. To explore a different month, change the **Settle at end of month** field and click **Recalculate**

---

## Inputs

| Field | Description | Default |
|---|---|---|
| Car price | Net price after all dealer discounts and rebates | $177,888 |
| Down payment | Upfront cash payment | $73,955 |
| Annual flat rate % | Interest rate as stated in your loan agreement | 2.28% |
| Tenure (months) | Loan term — typically 84 months (7 years) in Singapore | 84 |
| Loan structure | Rule of 78, flat pro-rata, or reducing balance | Rule of 78 |
| Penalty % | Early termination penalty as % of remaining principal | 1.5% |
| Finance clawback | Whether a finance rebate is clawed back on early settlement | On / $5,000 |
| Penalty from month | Month from which penalty starts applying (0 = always) | 0 |

---

## Output columns

| Column | Description |
|---|---|
| Interest (this month) | Interest portion of this month's instalment |
| Principal (this month) | Principal portion of this month's instalment |
| Cumulative interest | Total interest paid up to and including this month |
| Cumulative principal | Total principal paid up to and including this month |
| Remaining interest | Interest still to be paid if loan runs to full term |
| Remaining principal | Outstanding loan balance after this month's payment |
| Penalty | Early termination penalty if you settle this month |
| Clawback | Finance rebate returned to bank if you settle this month |
| Total car cost | **The key figure** — total amount paid for the car if you settle this month |

---

## Important notes

- **Flat rate vs EIR** — Singapore car loans are quoted as flat rates. The effective interest rate (EIR) is approximately double the flat rate. A 2.28% flat rate is roughly equivalent to a 4.2–4.5% EIR.
- **Rule of 78** — the most common structure for Singapore hire-purchase agreements. Because interest is front-loaded, early settlement yields a smaller rebate than a pro-rata method would.
- **Finance rebate conditions** — dealer finance rebates (e.g. $5,000 cash rebate for taking a loan) typically require you to maintain the loan for the full term. Settling early triggers a clawback of the full rebate amount regardless of how many months have elapsed.
- **Penalty calculation** — penalty is applied to the **remaining principal** at the time of settlement, not the original loan amount.

---

## Disclaimer

This calculator is for illustrative and educational purposes only. Figures are estimates based on the inputs provided. Actual loan terms, rebate calculations, penalty structures, and settlement amounts vary by financial institution and loan agreement.

Always verify your settlement figures directly with your bank or finance company before making any financial decisions.

---

## Tech stack

Pure HTML, CSS, and JavaScript. No frameworks, no dependencies, no build step. The Google Fonts import is the only external request — the calculator works fully offline without it (system fonts are used as fallback).

---

*Built with [Claude](https://claude.ai) by Anthropic*
