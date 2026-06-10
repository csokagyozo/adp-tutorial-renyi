# Prompting and workflow patterns for mathematical work
## a useful prompt structure

A good prompt does not need to be long, but it should give the model enough orientation. For mathematical work, it is usually helpful to include five things: the goal, the context, the assumptions, what you have already tried, and the desired form of the answer.

For example, instead of writing “Can you solve this?”, it is often better to write something like: “I am trying to prove the following lemma in extremal graph theory. Here are the definitions and assumptions. My current proof attempt breaks down at this step. Please check whether the argument can be repaired, or suggest a counterexample. First give a short diagnosis, not a full proof.” This tells the model what role it should play and what kind of answer is useful.

The desired output format matters. You can ask for a proof sketch, a list of possible strategies, a line-by-line critique, a table of examples, LaTeX code, pseudocode, or a short explanation for a non-specialist. You can also ask the model to separate rigorous conclusions from guesses, or to state explicitly where it is uncertain.

## start broad, then narrow down

It is usually inefficient to ask for a complete solution immediately. A better pattern is to start with a broad but controlled question, then narrow down. For instance, you can first ask for possible approaches, then choose one approach and ask for details. Or you can first ask the model to identify the main obstruction in a proof attempt, and only afterwards ask how to fix that obstruction.

This is especially useful for open-ended research questions. ChatGPT may be helpful in exploration: suggesting examples, reformulating a conjecture, identifying related concepts, proposing computational tests, or pointing out possible failure modes. But exploration should be separated from verification. A suggestion that sounds plausible is only a lead; it becomes useful mathematics only after it has been checked.

## A practical workflow is:

clarify the problem and notation;
ask for examples, special cases, or possible approaches;
test promising ideas on small cases;
ask for a proof sketch or obstruction;
inspect the details yourself;
ask for a line-by-line critique;
write a clean summary of what survived verification.
useful mathematical tasks

ChatGPT is often useful for tasks around the main act of proving, even when it does not solve the problem itself. It can help generate examples, search for counterexamples, explain definitions, compare formulations, translate intuition into notation, rewrite exposition, produce LaTeX, design small computations, or identify possible gaps in an argument.

For proof work, it is often better to ask for checking rather than solving. Good prompts include: “Where exactly does this proof use assumption X?”, “Can you find a counterexample if assumption Y is removed?”, “Please check this argument line by line and mark any unjustified step,” or “Give me the simplest nontrivial examples satisfying these definitions.”

For exposition, useful prompts include: “Rewrite this paragraph more clearly while preserving the mathematical meaning,” “Suggest notation that makes the dependencies more visible,” or “Explain this definition to a mathematician from a neighboring field.” For coding or computations, useful prompts include: “Write code to test this conjecture for small values,” “Explain what the code is checking,” and “Suggest edge cases where this test may fail.”

## ask for uncertainty and edge cases

By default, ChatGPT may answer confidently even when the situation is unclear. It is often useful to explicitly ask it to mark uncertainty. For example: “Separate what follows rigorously from what is only a heuristic,” “List possible hidden assumptions,” “Check edge cases,” or “Try to construct a counterexample before trying to prove the statement.”

In mathematics, edge cases are often where mistakes hide. Ask about empty sets, equality cases, small parameters, degenerate configurations, non-generic examples, boundary values, and cases where an assumption is removed. When working with definitions, ask for minimal examples and non-examples. When working with a conjecture, ask the model to test whether each assumption is necessary.

## keep control of the conversation

A long conversation can become unfocused. The model may continue using old notation, old assumptions, or an earlier mistaken direction. When this happens, it is usually better to reset the context. Ask for a compact summary of the useful part of the conversation: the problem, definitions, assumptions, confirmed facts, failed attempts, and the next question. Then start a new chat with that summary.

It is also useful to correct the model explicitly. If it makes a mistake, say exactly what is wrong and ask it to continue from the corrected version. Do not assume that a correction has been fully absorbed in all later answers. For serious work, keep your own notes outside the chat: definitions, verified claims, examples, references, and open questions should remain under your control.

The main principle is to treat prompting as steering a collaboration. Give the model enough context to be useful, ask for the kind of output you need, check the answer, then refine the next prompt. Good use of ChatGPT is less about finding a magic sentence and more about designing a good research workflow.