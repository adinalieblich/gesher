# Architecture and deployment

The design is shaped by what an engineering firm's IT and procurement will accept. Three decisions
follow from that.

1. Single-tenant. Engineering firms hold confidential client and project data, and many will not
put it in a shared multi-tenant service. The delivery model is single-tenant: each client gets
their own isolated instance, deployable into their own cloud, packaged as a portable container.
This is the delivery model. The managed, in-region, zero-retention version is the target, not a
finished claim today.

2. Model choice as a deployment option. Most engineering firms run Microsoft and will want AI on
Azure OpenAI. Others are on AWS. The LLM sits behind a single interface, so the model is a
deployment choice rather than a rewrite. Today the prototype runs on one provider. The adapter
layer is what makes another provider a configuration change instead of a rebuild.

3. Standards handled by licence, not by shipping the text. The product references a standard by
number and flags it for verification. It does not ship paid standards text. A client connects their
own licence.

Stack: Python, FastAPI, AWS Lambda or a container for any cloud, full-text retrieval over the
client's documents, structured fact extraction with provenance, DOCX output.

Wiring a language model to a document is easy. The decisions that make it deployable in a regulated
industry are the actual work: data location, model choice, licence handling, and a checkable output.
