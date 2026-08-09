MOP — how to use this (no coding needed)

THE SITE (index.html)
----------------------
Lists your PDFs, each with a QR code linking to it. This is what you
put online.

THE STAMP TOOL (stamp-tool.html)
----------------------------------
Use this BEFORE hosting a new PDF. It stamps a small QR code onto
every page of the PDF itself, pointing back to where that file will
live once it's online. That way, even if someone prints the PDF or
it gets separated from this site, scanning the code on the page
takes them straight back to the original hosted copy.

It runs entirely in your browser — nothing is uploaded anywhere.

HOW TO ADD A NEW PDF, START TO FINISH
----------------------------------------
1. Open stamp-tool.html (just double-click it, it opens in your
   browser).

2. Enter your site's base URL — this is the live link your site is
   (or will be) hosted at, e.g.
   https://yourusername.github.io/mop-eservice

3. Choose your PDF file. Confirm/edit the filename it should have
   once hosted.

4. Click "Stamp & download" — a new, stamped copy of the PDF
   downloads to your computer.

5. Move that downloaded file into the "pdfs" folder (delete the
   original unstamped one, or keep it aside — your choice).

6. Open "files.js" in Notepad/TextEdit and add the filename to the
   list, e.g.:

     const FILES = [
       "invoice-march.pdf",
     ];

7. Push the updated project to GitHub (or drag it onto
   https://app.netlify.com/drop) as before.

Once live, scanning the QR code on the site OR the QR code printed
on the PDF page itself both lead to the same hosted file.
