# Grounding and citations

Every value in the report traces to its source: which document, which page, and the exact quote.
An engineer, an auditor or a reviewer can follow any number back to where it came from.

Making the model produce that is the obvious half. The half worth writing down is how grounding is
measured.

Early on, grounding was scored by exact text matching: does the value appear, character for
character, in the source. That gives a misleadingly low result. Real engineering values are
reconstructed, not copied. A CBR is read off a lab table, a level is taken from a figure, a value
is assembled from several inputs. None of those appear as a verbatim substring of the source even
when they are correct and traceable. Exact matching fails correct data.

Measuring instead by whether the value traces to its cited source page reflects what is actually
happening.

The rule that came out of it: grade grounding by trace to source, never by exact text match.
Reserve exact matching for one job, confirming that a quoted passage exists in the source, which is
a check against fabrication, not a measure of whether a value is correct.

Limit: trace to source proves a value came from the documents. It does not prove the source itself
is right. That judgement stays with the engineer.
