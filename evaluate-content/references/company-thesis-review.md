# Company Thesis / Category Essay Review

Use this reference when reviewing company blog posts or founder essays that are trying to make a market/category argument, especially when the user asks if the piece has "everything" or asks you to read a sequence of related posts.

## Review move that worked

Fetch the full article text, not just a generated summary. For Next.js/blog pages, web extract may summarize or truncate. If so, pull the page HTML with `requests`, strip scripts/styles with BeautifulSoup, and review the visible article text directly.

## What to look for beyond normal prose quality

1. **Thesis completeness**: Can the argument be reduced to one sharp sentence? Does every section support it?
2. **Wedge clarity**: Does the essay identify the first product or narrow entry point, not just a giant abstract platform?
3. **Trust machinery**: For finance, healthcare, legal, AI infrastructure, and other trust-sensitive domains, look for auditability, compliance, verification, human accountability, and buyer proof requirements.
4. **Buyer/allocator POV**: Name who needs to believe this, what evidence they require, what creates hesitation, and what converts them.
5. **Workflow concreteness**: Convert broad claims into a lifecycle, e.g. idea → research → backtest → risk report → compliance log → allocator-ready memo.
6. **Category boundaries**: Add a "what this is not" section when readers may confuse the product with adjacent categories.
7. **Proof quality**: Separate strong proof points from weak anecdotes. Flag reported/experimental examples that should not be overweighted.
8. **Prediction hygiene**: Bold forecasts are good, but they need a model, source, or explicit "this is our bet" framing.

## Useful feedback shape

Keep the reply concise and strategic:
- Verdict: whether the piece has the bones or still lacks a layer.
- What works: 3-5 bullets tied to exact parts of the piece.
- What is missing: 3-5 bullets, focused on product/category clarity and trust.
- Cuts: where to compress repeated sections.
- Sharpest sentence/positioning: extract or propose the line that could anchor the company.

## Example positioning lenses from the Podium review

- "The bottleneck is no longer generating strategies. It is proving which strategies deserve capital."
- "The real gap is between strategy experimentation and institutional credibility."
- "Not Bloomberg for hedge funds. Not Robinhood for PMs. The formation layer where serious strategy builders become allocator-trustable."
- "Podium is where PM behavior becomes observable before capital is at risk."
