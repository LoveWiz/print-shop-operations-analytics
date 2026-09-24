# When three busy print shops ran on paper — and trust started to fray

A print-shop owner with **three high-traffic locations** could not answer a simple question with confidence:

**What did we actually make yesterday — and does the till match it?**

Staff filled **paper daily report sheets**. When the manager or owner was away, those sheets piled up. Revenue and spending were hard to reconcile. Performance felt opaque. Disputes crept in. Salaries ran late because the numbers weren’t ready.

This case study is about replacing that fog with a **clear daily story** the owner could open on a screen.

---

## The problem, in human terms

Paper wasn’t just slow — it was fragile.

- Nobody could trust the day if the person holding the sheets was offline  
- “What did this shop sell?” turned into argument, not evidence  
- Accounting swallowed **about 24 hours a month** chasing and stitching reports  

The owner needed to **see sales and costs the same day**, refresh them when morning printer counters landed, and run payroll without guessing.

---

## What I set out to build

Not a pile of charts for their own sake — a **daily rhythm**:

1. Capture what matters, the same way, every day  
2. Store it in one place (**SQL**) so it doesn’t live in someone’s notebook  
3. Show the owner a living picture: **what we expected vs what was reported**

I owned that loop end to end: **how the day gets recorded**, **how the data is cleaned and structured**, and **the web dashboard and reports** the business actually uses.

---

## Making the day measurable

Together with how the shops work, we defined what “a day” means in numbers:

- Sales **per shop**, and sales broken into real services (colored A4, comb binding, lamination, and the rest)  
- Cash in the till — electronic and physical  
- Expenses, discounts, errors, inventory  
- Printer reality: every photocopy, print, and scan  
- A crucial distinction: **intentional** printouts vs mistakes — so errors and intentional work don’t quietly inflate “sales”

Staff enter cash and adjustments through **simple web forms**. Printer counters arrive through **daily CSV jobs** from the shop PCs. Both streams land in the same database.

![Daily cash — the till count that used to live on paper](./screenshots/employee-form-1.png)

![Discounts and error costs — so waste doesn’t look like revenue](./screenshots/employee-form-2.png)

![Intentional printouts — marked so they can be left out of final sales](./screenshots/employee-form-3.png)

When counters were missing for a couple of days, the story didn’t have to break: a **baseline reset** let the next good reading start the day’s calculation cleanly again.

---

## What the owner sees

By close of day, the owner can review **yesterday’s sales and costs**.  
Next morning, when counter reports upload, the picture updates — expected production against what was reported in the till.

![Reconciliation — expected, reported, and what’s eating the gap](./screenshots/admin-dashboard-1.png)

![The trend — expected vs reported across days and shops](./screenshots/admin-dashboard-2.png)

The dashboards answer the questions that used to start fights:

- Are we short or over against what the machines and services imply?  
- Which shop is carrying the day?  
- Which services are earning?  
- Are stock or missing reports about to become tomorrow’s surprise?

Shop staff see a lighter version: enter the day’s figures, upload printer reports, and check **their shop’s** expected-vs-reported trend — not a wall of admin tools.

---

## The result

| Before | After |
|--------|--------|
| Paper sheets, delayed truth | Same-day view, refreshed after morning counters |
| Distrust and payroll friction | Clearer daily expectations; fewer sales disputes |
| ~**24 hours**/month on accounting | ~**4 hours**/month |

---

## The story in one line

**I turned three print shops’ paper chaos into a daily expected-vs-reported story the owner can trust — and cut monthly accounting from about a day to about half a morning.**

---

### Read next

- [How the numbers work (plain language)](./02-metrics-glossary.md)  
- [What appears on screen](./03-dashboard-sitemap.md)  
- [How data travels from shop floor to dashboard](./04-data-pipeline.md)
