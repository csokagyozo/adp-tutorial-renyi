# Behind the scenes: model requests, tokens, credits, and cost intuition 

## model requests and context

When you have a conversation in ChatGPT, behind the scenes each answer is produced by a model request. Roughly speaking, when you send a message, the system sends the model your new message together with the relevant context from the conversation, and the model generates the next answer. The model reacts when a request is made.

This also explains why long conversations can become expensive or difficult to control. If the relevant context contains many previous messages, definitions, proof attempts, examples, or uploaded text, then the model has more material to process. Sometimes this is useful, because the model can build on previous work. Sometimes it is better to start a new chat and paste in a short, clean summary of the current state.

## tokens

The text sent to and produced by the model is measured in tokens. A token is not exactly a word: it may be a word, part of a word, punctuation, a piece of code, or part of a formula. Different languages, notation, code, and LaTeX may be split into tokens differently. For practical purposes, it is enough to remember that longer input and longer output usually mean more tokens.

Both sides matter: your prompt consumes input tokens, and the answer consumes output tokens. If you paste a long paper, ask for a long explanation, or request several alternative solutions, the number of tokens increases. If you ask for a concise answer, a list of possible approaches, or a short proof sketch first, the request is usually smaller and easier to evaluate.

## credits and cost intuition

Credits are a way of paying for model use. The exact cost of a request depends on the model and on what the request involves. Longer prompts, longer answers, large uploaded files, tool use, and stronger reasoning models may all consume more credit. In some settings, a reasoning model may also spend additional computation on the problem before producing the visible answer.

The practical lesson is not to minimize every single request, but to use the right amount of context and reasoning for the task. For routine rewriting, translation, summarization, or formatting, a faster and cheaper model is often sufficient. For checking a difficult proof, searching for counterexamples, or debugging a subtle mathematical argument, a stronger model may be more efficient overall, because fewer failed attempts are needed.

A good habit is to work in stages. First ask for a short overview, a plan, or a list of possible approaches. Then choose the promising direction and ask a more focused question. When using files, first ask the model to identify the relevant sections or summarize the structure, and only then ask detailed questions about a particular lemma, definition, proof, table, or figure.

## API calls

The API is the programmable version of the same mechanism. Instead of typing into a chat window, a program sends requests to a model and receives answers. This is useful when one wants to automate repeated tasks: for example, running the same prompt on many examples, processing many documents, integrating a model into code, or building a custom tool.

Most workshop participants will not need the API. Still, it is useful to know the basic idea, because the chat interface, ADP, and the API all rely on the same underlying concepts: requests, models, context, tokens, and credits.