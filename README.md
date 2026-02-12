# GMROII & GMROS Calculator

A single-file HTML calculator for booksellers to evaluate restocking decisions using **Gross Margin Return on Inventory Investment (GMROII)** and **Gross Margin Return on Sales (GMROS)**. Based on Leonard Shatzkin's *The Mathematics of Bookselling*.

## Features

- **Supply-constrained GMROII** — order quantity optimization accounts for reorder frequency. The calculator caps effective sales by supply capacity per cycle, so the "best" order naturally matches real-world demand instead of always favoring minimal inventory.
- **Order Quantity Comparison** — side-by-side table comparing GMROII, annual margin, coverage, and days to recover across multiple order quantities. Overstock rows past the GMROII peak are flagged.
- **Coverage Tracking** — shows whether stock + order covers the full reorder cycle or signals stockout risk.
- **Earning Power Decline Chart** — SVG line chart showing how a copy's annualized earning power drops the longer it sits on the shelf.
- **Discount Step Advisor** — should you order more copies to reach the next discount tier? Uses the exact GMROII break-even formula (not Shatzkin's fixed 4% approximation).
- **Configurable Payment Terms** — set invoice payment days to see if sales revenue covers the order cost within your payment window.
- **Flexible Reorder Interval** — set any number of days, weeks, or months as your reorder cycle.
- **Responsive Design** — works on desktop, tablet, and mobile.

## Usage

Open `index.html` in any browser. No server, no build step, no dependencies.

Set your title details:
- **Retail Price** and **Vendor Discount**
- **Stock on Hand** and **Avg Weekly Sales**
- **Order Quantity**, **Payment Terms**, and **Reorder Interval**

The calculator updates all metrics, the comparison table, and the chart in real time.

## Key Metrics Explained

| Metric | Formula | Meaning |
|--------|---------|---------|
| GMROII | Markup x Stock Turn | Dollars earned per dollar invested per year |
| GMROS | Discount % | Margin on sales (equals the vendor discount) |
| Stock Turn | Annual COGS / Avg Inventory at Cost | How many times inventory turns over per year |
| Markup | Discount / (1 - Discount) | Margin earned per dollar of cost |
| Coverage | min(1, supply / demand per cycle) | Whether stock covers the reorder cycle |

## License

This project is licensed under the GNU General Public License v3.0 — see the [LICENSE](LICENSE) file for details.
