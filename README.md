# Payments to Uncle Tony

A small web app for tracking the monthly property installments from the buyer, their conversion to USD by the SPA, the SPA's service fees, and the remittances sent to Uncle Tony. Everything runs in the browser; there is no server or database.

## What it tracks

- 14 monthly installments of ₱368,103.37 (₱4,950,000 at 6.5% compounded monthly), each due on the last day of the month
- The date the buyer paid, and a 2% late penalty when the payment is late
- The BPI rate and date the SPA converted the pesos to USD
- The SPA's $200 service fee per remittance and the net amount sent to Uncle Tony
- Reference numbers and notes for each transfer

All terms (amount, rate, fee, penalty, grace period, first due month) can be changed under **Settings and backup**.

## Excel export

**Export to Excel** downloads a workbook with four sheets:

| Sheet | Contents |
| --- | --- |
| Summary | Terms and running totals |
| Payment Ledger | One row per installment, with formulas for USD and net amounts |
| SPA Service Fees | Each fee, its peso equivalent at that day's rate, and a running total |
| Amortization | Interest, principal, and balance for every month |

## Put it on GitHub Pages

1. Create a new repository on GitHub (for example `uncle-tony-payments`).
2. Upload `index.html` and this `README.md` (Add file, then Upload files, then Commit).
3. Open **Settings → Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, and save.
4. After a minute the app is live at `https://<your-username>.github.io/uncle-tony-payments/`.

If the repository is public, the app's code is public, but your payment records are not: they are saved only in the browser you use.

## Keeping your records safe

Records live in your browser's local storage, so they stay on that one device and browser. Use **Download backup** regularly, and **Restore from backup** to move them to another computer or phone. Clearing your browser data will erase them.
