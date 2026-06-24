# Preventing hallucination

An invented or mis-cited value in an engineering report is worse than no report, because someone
can build on it. So Gesher is designed not to state an engineering value unless that value comes
from the documents, or is flagged for the engineer to confirm.

This is handled in layers, so a miss in one is caught by another.

1. Grounded generation. The model states a value only if it comes from the engineer's documents or
a retrieved standard. It is instructed to prefer retrieved text over its own memory, and not to
assert a standard or clause it cannot retrieve.

2. Provenance on every value. Facts are extracted with their source attached: the document, the
page, and the exact quote. The source travels with the value through to the final report.

3. A deterministic check after drafting. A non-model check scans the draft and flags any
engineering value that does not trace to a source, before the engineer sees it. The check is
deterministic on purpose. Asking the model whether it invented something just produces another
answer you cannot trust, so the model does not grade its own output.

4. Conflicts are flagged, not resolved. When two sources give different values for the same thing,
the engineer decides. The system does not silently pick one.

5. Gaps are marked, not filled. Where a value is missing or interpretive, it is marked for the
engineer to confirm rather than guessed.

Limit: this reduces hallucination, it does not make the output correct on its own. A registered
engineer still reviews and signs. The design makes that review fast and every value checkable, not
optional.
