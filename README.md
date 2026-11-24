# QuoteRelay AI

Turn customer product requests into reviewable, priced quotations.

## Status

Proposal and implementation planning for the Decentralize AI Hackathon.
The application and Nosana deployment are planned.

## Problem

Small wholesalers receive customer requests as PDFs, screenshots,
and product lists. Staff must manually identify products, check
spreadsheet prices and stock, and prepare quotations.

## Proposed Solution

QuoteRelay AI will:

- Extract product descriptions, part numbers, quantities, and units.
- Match requested products against an uploaded catalogue.
- Retrieve prices and stock from the merchant’s spreadsheet.
- Flag ambiguous matches and missing information.
- Calculate quotation totals using application code.
- Export quotations after staff review.

Prices will come from catalogue records. Uncertain product matches
will require confirmation.

## Initial Customers

Small industrial-parts wholesalers that manage their catalogues
and pricing in spreadsheets.

## Planned Technology

- Python and FastAPI
- Lightweight web interface
- Spreadsheet catalogue imports
- Qwen3-VL-8B-Instruct through Ollama
- Dockerized GPU inference on Nosana
- PDF and CSV quotation exports

## Nosana Integration

Nosana will host the vision-language inference worker for extracting
customer requests and assisting with product matching.

The project will publish deployment configuration, extraction schemas,
and evaluation instructions.

## MVP Roadmap

- [ ] Import a sample catalogue.
- [ ] Extract line items from customer requests.
- [ ] Implement catalogue matching.
- [ ] Build the quotation review screen.
- [ ] Add quotation export.
- [ ] Deploy inference on Nosana.
- [ ] Measure accuracy, correction time, and compute cost.

## Evaluation

Use synthetic or explicitly permissioned requests. Measure extraction
accuracy, matching errors, unresolved-item detection, review time,
and compute cost per request.

## License

Original project code: MIT.
Third-party models and dependencies retain their respective licenses.
