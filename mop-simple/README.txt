MOP — how to use this (no coding needed)

1. Open the "pdfs" folder. Delete "sample-report.pdf" and drag your own
   PDF files into that folder instead.

2. Open "files.js" in any text editor (Notepad, TextEdit, VS Code —
   whatever you have). List your PDF filenames exactly as they're
   named, one per line, keeping the quotes and commas, like this:

   const FILES = [
     "invoice-march.pdf",
     "meeting-notes.pdf",
   ];

3. Put this whole folder online. Easiest free option, no account
   strictly required:

     - Go to https://app.netlify.com/drop in your browser
     - Drag the ENTIRE "mop-simple" folder onto the page
     - Netlify gives you a live link in a few seconds, e.g.
       https://random-name-123.netlify.app

4. Open that link — you'll see every PDF listed with its own QR code.
   Scanning a code with a phone camera opens that PDF directly.

That's it — no installing, no terminal, no build step. Whenever you
add or remove a PDF, just repeat steps 1–3 (drag the updated folder
onto https://app.netlify.com/drop again — it replaces the old version
with the same link if you're logged in, or gives a fresh link if not).
