# How it was rebuilt twice

Gesher has been built three ways. The changes were structural, each for a specific reason.

Version 1: a SaaS project-management workspace. A schema of over 150 fields across nine categories,
a sidebar of sections, three ways to enter data (type, voice, or AI extraction), and a template
wizard that filled the gaps. It modelled a whole project.

Why it changed: the intelligence was in the schema, not in the model, and it made the user do the
data entry. The real pain was one job inside the project, drafting the report. The product was
narrowed to that.

Version 2: an AI that drafts the report. Drop the documents, the model extracts the facts cited to
source, the engineer resolves conflicts, and it drafts the cited report. This was the move to the
model doing the work, with never-invent and full citation.

Why it changed: it kept a fixed per-discipline field schema. Extraction poured documents into
predetermined slots. That drops anything without a slot, assumes which report is being written, and
flags conflicts by key match rather than by reasoning about whether the values are even the same
quantity.

Version 3, the current direction: no fixed fields. The documents are read and retrieved over, the
system answers questions cited to source, and it drafts different report types by reasoning over the
documents with the relevant facts found on demand. The trust constraints do not change: citations,
never-invent, real conflict detection. The retrieval and grounding work is what makes removing the
fields safe rather than ungrounded.

The constant across all three versions: do not make the user fill forms, and do not make the model
fill slots. Let the model do the work, grounded in the documents and checkable.
