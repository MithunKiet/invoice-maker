# Invoice Maker

A simple, single-file HTML invoice/receipt generator for **Touch Net India Teleservices**, an internet service provider. It renders a printable invoice with tax breakdown, service plan summary, receipt details, terms & conditions, and an acknowledgment slip — all in the browser, with no backend or build step required.

## Features

- **One-click invoice generation** — generates a random Invoice No. and Account No. for each new invoice.
- **Bill date picker** — set the invoice date via a date input.
- **Tax details table** — shows taxable amount, CGST/SGST rates and amounts, and total.
- **Service plan summary** — displays plan speed, package, validity, discount, and amount.
- **Receipt details** — invoice number and amount paid.
- **Terms & conditions** section.
- **Acknowledgment slip** — tear-off style summary with account/invoice number and payment method.
- **Print-friendly layout** — a dedicated print stylesheet hides input controls and adjusts backgrounds/shadows for clean printed output.

## Getting Started

No installation or build process is needed — this is a static HTML page that uses [Bootstrap 5](https://getbootstrap.com/) via CDN.

1. Clone or download this repository.
2. Open `index.html` directly in your web browser (double-click it, or run a local static server).
3. Use the controls at the top of the page:
   - **Enter Bill Date** → pick a date, then click **Set Date**.
   - **New Invoice** → generates a new random Invoice No. and Account No.
   - **Print Invoice** → opens the browser print dialog (requires the bill date to be set first).

## Project Structure

| File         | Description                                      |
|--------------|---------------------------------------------------|
| `index.html` | The entire application — markup, styles, and JS.  |
| `cn.png`     | Company logo displayed on the invoice.            |

## Customization

Since everything lives in `index.html`, you can customize the invoice by editing the HTML/JS directly:

- **Company info & logo** — update the company name, address, and `cn.png` logo in the first row of the invoice.
- **Customer details** — update the `Name` and `Address` fields.
- **Tax details, plan summary, and receipt amounts** — edit the table rows in the respective `<table>` sections.
- **Terms and conditions** — edit the list items inside the `.terms` section.
- **Invoice/Account number format** — modify the `generateInvoiceNo()` and `generateAccountNo()` functions in the `<script>` block.

## Tech Stack

- HTML5 / CSS3
- [Bootstrap 5.3](https://getbootstrap.com/) (via CDN)
- Vanilla JavaScript (no build tools or dependencies)

## License

This project is licensed under the [MIT License](LICENSE).
