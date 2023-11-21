---
Title: RAG vs Fine Tuning
---

I want to address some of the most common misconceptions when it comes to RAG, prompt engineering, and fine tunning LLMs.  One of the most common blog posts or articles I see these days on things like "How to decide between using RAG or fine tuning" or discussions on which one is better.  

All of which are bad discussions because they simply are not comparable things because they solve completely different problems and have completely different functionality.  Let's briefly review these concepts:

- RAG
Retrieval augmented generation is a system that uses a retrieval method to provide contextual information, typically information not inlcuded in training data, directly within a prompt that will be used with your LLM.  This can be domain specific information or proprietary information, typically found somewhere within textual documents.

- Prompt Engineering
Initially made popular by the job posts posted claiming to be hiring "Prompt Engineers" at a 400k salary, and often demonstrated as clever prompts that incorprate role playing or chain of thought methods to get better responses from things like ChatGPT. In reality it is neither of these things, it is not a role, nor is it a list of the "Top 10 prompts to use ChatGPT".  It is now a common skill that most smart people develop after using ChatGPT for some time, typically a combination of instructing, context provision, and conversational flow, that allow for high quality conversations with ChatGPT.  The concept is then built up to develop chat applications in ways that handle LLMs without users seeing the additional prompting that takes place in the backend.  This can include RAG, conversation history management, prompt structuring, and more.

- Fine Tuning
While probably the most straightforward out of these concepts, it is also the hardest and most technical to implement.  Mostly because it is an actual machine learning task, which requires a lot more technical domain knowledge on the concepts of models and training data.  And in the case of LLMs, fine tuning is even a level beyond typical ML, due to requirements to implement SOTA methods to handle the scale of LLM sizes, things like quantization, low rank adaptation, parameter efficient fine tuning, transformer architecture, distributed training, and more. As well as keeping up with new methods that come out as research papers, and being able to implement them in your code.

Now what are scenarios that you would use each of them?

Prompt engineering has the lowest level of implementation requirement and solves the simplest but most direct problems.  Things that don't require any additional information or domain knowledge.  Maybe you want an LLM to be better about not assuming details like the often do, or you want it to help you tackle specific tasks in a specific way, or you just want to increase its ability to help you when your current prompting does not achieve it.  Often you can improve responses just by including concise intstructions before asking your question, simply starting a conversation with "We are going to be working on *this* kind of problem" or "Do not assume anything, if you need additional information just ask me for it." You can also use techniques like role playing or chain of thought, simply by telling the LLM to play the part of a senior software engineer experienced with Javascript who is helping me, someone who has limited Javascript experience, it will do much better at explaining things to you, as well as writing code that is better suited for an application versus just a learning scenario. Starting a conversation by overviewing the plan will allow the LLM to develop on top of the plan rather than having to assume details and provide you things you don't want.

** I need to finish this
