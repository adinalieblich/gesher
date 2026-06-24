# Retrieval

A language model carries a lot of plausible engineering knowledge, and almost none of it is safe to
use here. It will recall a likely clause number or a typical value from training. In this domain a
plausible but unsourced value is exactly the failure to avoid. So the rule is blunt: Gesher does
not answer an engineering fact from model memory. Every value, clause and citation comes from a
retrieved source, either the engineer's own documents or a corpus of public standards and
road-authority guidelines.

How it works:
- Ingest. The documents are uploaded, parsed, and indexed for retrieval at the page level.
- Retrieve. To draft a section or answer a question, the system retrieves the relevant passages and
  works from those, not from memory.
- Cite. The answer is grounded in the retrieved text and cited back to document, page and quote.
- Refuse. If the answer is not in the documents, it says so rather than fill the gap.

Standards are handled the same way. The model is told to prefer retrieved clause text over memory,
and to flag "verify against AS XXXX" rather than assert a clause it cannot retrieve. Licensed
standards stay with the client and are not shipped in the product.

Direction: the earlier version extracted documents into a fixed field schema up front, which drops
anything without a slot and assumes which report is being written. The current direction reads the
documents in full and retrieves on demand, so it can answer across the documents and draft
different report types from the same set. See "How it was rebuilt twice".

Limit: retrieval quality bounds answer quality. A value buried in a scanned image with no text
layer has to be made readable first. Retrieval does not recover what was never captured.
