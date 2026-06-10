# cheat sheet: reusable prompts and habits

This section collects prompt patterns and practical habits that are useful after the workshop. Replace the bracketed parts with your own problem, notation, assumptions, file names, or draft text.

## General prompt structure

A useful prompt often contains five elements:

1. Goal: what you want to achieve.
2. Context: definitions, notation, background, or uploaded files.
3. Assumptions: what should be taken as given.
4. Attempt: what you have already tried, if anything.
5. Output format: proof sketch, critique, table, LaTeX, code, summary, etc.

## Proof checking

Use ChatGPT as a skeptical reader, not as a certificate of correctness.

> Please check the following proof attempt line by line.
Mark each step as “justified”, “unclear”, or “incorrect”.
For every unclear or incorrect step, explain exactly what assumption is missing or what could go wrong.
Do not try to rewrite the proof yet.

A more targeted version:

> In the following argument, I think the problematic step is [step].
Can this step be justified under the stated assumptions?
If not, give a counterexample or explain what extra assumption would make it true.

To test assumptions:

> Which assumptions of the lemma are used in this proof?
For each assumption, say where it is used.
If an assumption seems unused, try to find a counterexample without it.

## Counterexamples and examples

For conjectures, ask for examples early.

>I am considering the following conjecture: [conjecture].
Please try to disprove it before trying to prove it.
Start with small, degenerate, boundary, or non-generic cases.
Give explicit examples or explain why a proposed counterexample fails.

## For building intuition:

>Give several small examples and non-examples of objects satisfying the following definition: [definition].
Include at least one edge case and one example showing why each assumption matters.

## For classification-style exploration:

>Please make a table of small cases for [objects/parameters].
For each case, record [properties].
Then suggest possible patterns, but clearly label them as conjectural.

## Proof strategies and reformulation

When you do not want a full proof immediately:

>Suggest possible strategies for proving the following statement: [statement].
Do not give a full proof yet.
For each strategy, say what the main obstacle might be and what known technique it resembles.

## For reformulation:

>Reformulate the following statement in several equivalent or near-equivalent ways.
Try formulations using [graphs / linear algebra / topology / probability / order theory / category language / etc.], if appropriate.
Mark which reformulations are genuinely equivalent and which are only heuristically related.

## For obstruction-finding:

>I am stuck at the following point: [obstruction].
Please diagnose the obstruction.
Is it a technical gap, a false statement, a missing lemma, a bad choice of notation, or a sign that the approach may not work?

## Working with uploaded files

Start with orientation before asking detailed questions.

>Please give me a structural overview of the uploaded file.
Identify the main definitions, theorems, examples, and proof dependencies.
Do not summarize every paragraph; focus on the mathematical structure.

### For local questions:

>In the uploaded file, focus only on [section / theorem / lemma / proof / paragraph].
Explain the role of this part in the overall argument.
Then identify any assumptions, notation, or previous results it depends on.

### For comparing drafts:

>Compare the two uploaded versions of the draft.
Focus on mathematical changes, changed assumptions, changed notation, and possible inconsistencies.
Ignore purely stylistic differences unless they affect meaning.

### For rewriting without changing mathematics:

>Rewrite the following paragraph to make it clearer and more concise.
Preserve the mathematical meaning exactly.
Do not introduce new claims.
Keep the notation unchanged unless you explicitly explain a suggested notation change.

### For a different audience:

>Explain the following definition/result to a mathematician from a neighboring field.
Keep the explanation precise, but reduce unnecessary technical detail.
Include one simple example.

### For LaTeX:

>Please improve the LaTeX formatting of the following text.
Preserve the mathematical content.
Make notation consistent, fix obvious LaTeX errors, and explain any nontrivial changes.

## Code, computations, and plots

### For computational experiments:

>Write code to test the following conjecture for small values of [parameters].
Explain what the code is checking.
Include edge cases.
Do not treat the computation as a proof.

### For debugging:

>Here is my code and the error/output I get.
Please identify the likely cause.
Suggest a minimal fix first, then suggest a cleaner version if appropriate.

### For plots or data:

>Generate a plot/table illustrating [phenomenon].
Explain what the axes/columns mean.
State what the plot suggests, but separate visual evidence from proof.

## References and literature leads

Treat references suggested by ChatGPT as leads, not as citations ready to use.

>Suggest possible keywords, theorem names, or areas of literature related to the following problem.
Do not invent bibliographic details.
If you mention a specific paper or author, clearly indicate whether you are certain or only suggesting a lead.

## For checking a claimed reference:

>I have the following claimed reference: [reference].
What should I verify to make sure this citation is real and relevant?
Suggest reliable places to check, such as the journal page, arXiv, MathSciNet, zbMATH, or the author’s webpage.

## Summarizing and restarting a chat

When a conversation becomes long or confused:

>Please summarize the useful state of this conversation so I can start a new chat.
Include: the problem, notation, assumptions, verified facts, failed attempts, open questions, and the next concrete task.
Do not include ideas that were later rejected unless they are useful warnings.

Then start a new chat with the summary and continue from there.

## Model-choice habits

Use a fast or cheaper model for routine work: rewriting, summarizing, translating, formatting, simple LaTeX help, or first-pass brainstorming.

Use a stronger reasoning model for tasks where correctness and multi-step reasoning matter: proof checking, counterexample search, subtle definitions, debugging mathematical arguments, and planning computations.

Do not optimize every request, but do match the model to the task. The strongest model is not always necessary, and the cheapest model is not always cheapest if it leads to many failed attempts.

## Good working habits

- Keep prompts focused.
- Upload only the material that is relevant.
- Ask for short diagnostic answers before long solutions.
- Separate exploration from verification.
- Check all mathematical claims yourself.
- Check references externally.
- Keep your own notes outside the chat.
- Start a new chat when the context becomes messy.
- Do not upload confidential or personal data unless you know that you are allowed to do so.
- Use ChatGPT as an assistant, not as an authority.