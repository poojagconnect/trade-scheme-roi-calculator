# Trade Scheme and Promotion ROI Calculator

Most trade schemes get judged on one thing: did sales go up? They nearly always do. What I wanted to practise is the harder question a brand manager actually has to answer: did we make more profit than if we had done nothing?

This is an Excel model that tests that for one SKU and compares six different schemes side by side.

**All the numbers are made up.** The SKU, prices, margins and uplift figures are invented so I could practise the method. If you use it for a real brand, swap in real figures, and use uplift from past schemes rather than a hopeful guess.

## What the model accounts for

A basic "sales went up" view misses a few things, so I built these in:

- **Leakage.** The discount is paid on every unit sold during the scheme, including the ones that would have sold anyway.
- **Pull-forward.** Some of the extra volume is just the trade buying early, so the next period dips.
- **Cannibalisation.** Some of the extra volume is taken from the brand's own other SKUs, which is not new demand.
- **Free goods vs price-offs.** Free units cost the company COGS and freight, not the selling price. So "buy 10 get 1 free" and a price-off are not the same cost.
- **Break-even uplift.** The minimum volume lift a scheme needs just to pay for itself. This ended up being the most useful number in the whole file.

## Workbook sheets

| Sheet | What it does |
|---|---|
| Read Me | Why the model exists, assumptions and colour legend |
| Assumptions | MRP to company net realisation (price waterfall) and the main inputs |
| Scheme Comparison | Six schemes: volume, cost, profit, ROI, break-even uplift, verdict and rank, with a chart |
| Sensitivity | Two grids: profit by discount and uplift, and break-even by discount and pull-forward |
| Post-Mortem | Plan vs actual for a finished scheme, including channel stock build |
| Decision Guide | Which scheme fits which goal, a go/no-go checklist and common mistakes |

Blue text is an input, black is a formula, green is a link from another sheet, and yellow cells are settings to change. The scheme type is a drop-down and the verdict updates by itself.

## What the sample data shows

For a soap SKU with a baseline of 200,000 units in four weeks:

- **Four of the six schemes lose money.** Only the display incentive clearly pays: about Rs 3.56 lakh extra profit, a 178% return, and it only needs a 5.4% volume lift to break even against 15% expected.
- **The 3% price-off loses about Rs 3.24 lakh.** It would need roughly a 26% uplift to break even and only 12% was assumed. Around 89% of the discount cost goes on units that would have sold anyway.
- **Buy 10 get 1 free is cheaper per rupee of benefit than a price-off** (about 0.73 of cost for each rupee of perceived value, against 1.00), but 9% is such a deep offer that it still loses about Rs 6.66 lakh.
- **The 2% slab rebate is marginal.** Its return is 19.7%, just under my 20% hurdle, so the verdict is "rework" and not "run".
- **Post-mortem example.** The display scheme beat zero but missed plan: about Rs 2.50 lakh profit against Rs 3.56 lakh planned, with fixed spend over by Rs 15,000 and 12,000 units (5.3% of sell-in) sitting as extra channel stock.

My main takeaway: broad discounts rarely pay, and spending that is targeted and verifiable usually does.

## Limits

- One SKU and one four-week promo period at a time.
- It does not model competitor reaction or how repeated schemes change what the trade expects.
- GST is assumed at 18%. Check the right rate for the category.
- Results depend heavily on the uplift and pull-forward inputs, which is why the Sensitivity sheet is there.

## Tools

Microsoft Excel: formulas, drop-downs, conditional formatting and a chart. Checked for formula errors before uploading.

## Using it

Download the `.xlsx` and open it in Excel. Change the blue cells on Assumptions and Scheme Comparison. The verdicts, ranking and chart update automatically.
