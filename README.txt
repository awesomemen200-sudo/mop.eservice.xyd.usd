# Define the HTML template with CSS styling matching official receipts
html_content = """
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <style>
        body {
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            font-size: 11px;
            color: #333;
            margin: 0;
            padding: 20px;
        }
        .header {
            text-align: center;
            border-bottom: 2px solid #333;
            padding-bottom: 10px;
            margin-bottom: 15px;
        }
        .header h3 {
            margin: 2px 0;
            font-size: 13px;
            text-transform: uppercase;
        }
        .header h4 {
            margin: 2px 0;
            font-size: 11px;
            color: #555;
        }
        .section-title {
            background-color: #f2f2f2;
            font-weight: bold;
            padding: 5px;
            margin-top: 15px;
            margin-bottom: 5px;
            border-left: 3px solid #333;
        }
        .grid-2 {
            width: 100%;
            display: table;
            margin-bottom: 10px;
        }
        .grid-col {
            display: table-cell;
            width: 50%;
        }
        table.data-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 5px;
        }
        table.data-table th, table.data-table td {
            padding: 6px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        table.data-table th {
            background-color: #fafafa;
            font-weight: bold;
        }
        .text-right {
            text-align: right;
        }
        .footer-notice {
            font-size: 9px;
            color: #666;
            text-align: center;
            margin-top: 20px;
            border-top: 1px dashed #ccc;
            padding-top: 10px;
        }
        .total-box {
            background-color: #fbebee;
            color: #a94442;
            font-weight: bold;
            text-align: right;
            padding: 8px;
            margin-top: 10px;
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <div class="header">
        <h3>CUSTOMS V.2 SYSTEM</h3>
        <h4>MOP-USD</h4>
        <br>
        <strong>THE REPUBLIC OF SOUTH SUDAN</strong>
        <h3>SOUTH SUDAN REVENUE AUTHORITY</h3>
        <h4>CUSTOMS DIVISION</h4>
    </div>

    <!-- Payment & Reference Info -->
    <div class="section-title">Payment Instructions & Details</div>
    <div class="grid-2">
        <div class="grid-col">
            <strong>REFERENCE NO:</strong><br>
            EQ-98521Q<br><br>
            <strong>TAXPAYER NAME:</strong><br>
            SALWO GENERAL TRADING CO
        </div>
        <div class="grid-col">
            <strong>DATE DECLARED:</strong><br>
            18 September 2026<br><br>
            <strong>TIN / PHONE:</strong><br>
            B20240705V918Q0 / +211922348900
        </div>
    </div>

    <!-- Entry & Cargo Details -->
    <div class="section-title">Revenue Division Details</div>
    <table class="data-table">
        <tr>
            <th>ENTRY NUMBER</th>
            <th>CARGO DETAILS</th>
            <th>VEHICLE REG NO</th>
        </tr>
        <tr>
            <td>26MBATR806275051</td>
            <td>Gasoline 40000 m3</td>
            <td>KDU811Q/ZJ4653</td>
        </tr>
    </table>

    <!-- Tax Details -->
    <div class="section-title">Tax Details</div>
    <table class="data-table">
        <tr>
            <th>Tax</th>
            <th class="text-right">Amount</th>
        </tr>
        <tr>
            <td>Custom Duty</td>
            <td class="text-right">USD 7327.00</td>
        </tr>
        <tr>
            <td>Tax Stamp fee</td>
            <td class="text-right">USD 1.00</td>
        </tr>
        <tr>
            <td>Police Stamp Fee</td>
            <td class="text-right">USD 1.00</td>
        </tr>
        <tr>
            <td>Business Stamp Fee</td>
            <td class="text-right">USD 1.00</td>
        </tr>
        <tr>
            <td>Sale Form Fee</td>
            <td class="text-right">USD 14.00</td>
        </tr>
        <tr>
            <td>Supervision Fees</td>
            <td class="text-right">USD 7.00</td>
        </tr>
        <tr>
            <td>e-Petroleum Accreditation Certificate Fee</td>
            <td class="text-right">USD 1200.00</td>
        </tr>
        <tr>
            <td>Fuel Marking Fees</td>
            <td class="text-right">USD 960.00</td>
        </tr>
    </table>

    <!-- Total Box -->
    <div class="total-box">
        TOTAL TAX: USD 9511.00
    </div>

    <!-- Disclaimer Footer -->
    <div class="footer-notice">
        THIS DOCUMENT IS COMPUTER GENERATED AND THEREFORE NOT SIGNED. IT IS A VALID DOCUMENT ISSUED UNDER THE AUTHORITY OF SOUTH SUDAN REVENUE AUTHORITY, CUSTOMS.
    </div>

</body>
</html>
"""

# Render the HTML content into a PDF file
HTML(string=html_content).write_pdf("customs_receipt.pdf")
print("PDF generated successfully as 'customs_receipt.pdf'!")
