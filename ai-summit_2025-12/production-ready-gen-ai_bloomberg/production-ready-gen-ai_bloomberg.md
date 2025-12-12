Production-Ready GenAI: The Reality of Customer-facing LLM Apps in a Data-Rich Enterprise

## RG Leads to Great Products

- Retrieval-Augemented Generation pairs with LLM with a vector DB that injects documents associated with the questions into the answer.
- Useful for relevancy. make sure we are pulling the latest documents
- Advantages over fine-tuning
    - Use info that is not in fine-tuned dataset
    - Allows use of latest off-the-shelf models

## Prompt Regsitry

Prompts should never be commited in the codebase.

Use a Prompt Registry instead.

A prompt registry is a centralized repository that stores, manages, and organizes prompts used for interacting with large language models (LLMs) in an enterprise setting. It allows teams to share and reuse effective prompts, track their performance, and ensure consistency across applications. A well-maintained prompt registry can help improve the quality of AI-generated responses, streamline development processes, and facilitate collaboration among different teams working with LLMs.

Problems with hardcoding prompts:
LLM, it only tries to solve a problem. It keeps going through the cycle. 

## Guardrails are Critical for the Business

- Guardrails systems should not only evaluate safely, but also relevancy
- A hallucinated case citation that never happended is **not** relevant to the issue at hand.
- All answers need to go through the guardreals service before making to users - this can lead to annoying UX