# Reliability, verification, and references

## Verification checklist for mathematical output

When ChatGPT proposes a proof or argument, check:

1. Are all definitions used consistently?
2. Are all assumptions stated and used?
3. Are there hidden regularity, finiteness, non-emptiness, or genericity assumptions?
4. What happens in small, degenerate, equality, and boundary cases?
5. Can the claimed implication be tested on minimal examples?
6. Can each nontrivial step be justified independently?
7. Are citations real, relevant, and checked in external sources?

ChatGPT can be very useful, but it can also produce plausible false statements. In mathematics this may mean an invalid proof step, a false theorem, a missed edge case, an incorrect computation, a buggy program, or a reference that looks real but is not. Confidence of style is not the same as correctness.

For this reason, mathematical claims must be independently verified. Ask for details, test small cases, inspect equality and degenerate cases, check whether all assumptions are used, and compare different approaches. When ChatGPT gives code, read it and test it. When it gives a proof, check each step as you would check a proof written by a student or collaborator.

References require special care. Treat suggested papers, theorem names, bibliographic data, and historical attributions as leads, not as ready-to-use citations. Check them in reliable external sources before relying on them. If web search or current database access is not available, the model may also be unaware of recent papers, policy changes, software updates, or newly published results.

The right mental model is: ChatGPT is a research assistant, not an oracle. It can help generate ideas, organize material, expose possible mistakes, and speed up routine work, but the responsibility for correctness remains with the researcher.