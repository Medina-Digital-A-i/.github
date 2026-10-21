# Idea Scoring Framework

Every business idea the company considers gets scored on the same six criteria, 1 to 5, so
ideas from different research lenses can be ranked against each other. The weights reflect what
the Owner has said matters: speed to $1M, low capital, and as little cold selling as possible.

| Criterion | 1 | 5 | Weight |
|-----------|---|---|--------|
| Capital needed | over $50k | under $1k | 1.0 |
| Speed to $10k/month | over 24 months | under 3 months | 1.5 |
| Probability of $1M net worth in 7 years | under 2% | over 30% | 2.0 |
| Share of work AI agents can do | under 30% | over 85% | 1.0 |
| Cold-selling burden (inverted: 5 = none) | daily cold calls | fully inbound or marketplace | 1.5 |
| Evidence quality | guru claims | peer-reviewed or verified revenue | 1.0 |

Weighted score = sum(score x weight). Maximum 40.

Rules:
- Probability estimates must cite the base rate they are derived from.
- "Evidence quality" caps the score: an idea with evidence quality 1 cannot rank above an idea
  with evidence quality 4, whatever the other numbers say.
- Any idea requiring a license the Owner does not hold is flagged, not excluded.
- Ideas can be combined. A cash-flow idea paired with an asset idea is a strategy, not a conflict.
