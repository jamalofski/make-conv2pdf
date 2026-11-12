# Changelog

## Unreleased

- New modules, so that every Conv2pdf API tool is available in Make: Convert an XPS document to PDF (`xps-to-pdf`), for XPS and OpenXPS documents (.xps, .oxps); Convert a PostScript file to PDF (`ps-to-pdf`), for PS and EPS files; Convert an HTML file to PDF (`html-to-pdf`); Convert a web page to PDF (`url-to-pdf`), which takes the address of a public page and no file; and Split a PDF (`split-pdf`), which puts every page of a PDF in its own PDF file, returned in a ZIP file.
- Extract pages from a PDF calls the `extract-pages` tool. It called `split-pdf` with a `ranges` field, which the API still serves as an extraction.
- A file that another module expects, such as an XPS document, a PostScript file or an HTML file, gets a message that names that module.
- A document with too many pages gets a message with its page count and the limit of the module, when Conv2pdf returns them.
- The errors of the new tools get their own messages: a refused web page address says why, and a page that answers with an error gives its HTTP status.
