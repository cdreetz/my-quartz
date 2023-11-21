---
title: Apple App Platform
---

## Generative AI Powered Developer Experience

Most use cases at the given moment can be developed with strong retrieval systems and well developed agent systems.  Agents are powerful for forward passes of code, enabling AI to plan the necessary steps and then act on them.  Retrieval is necessary for the backward movement we often aim to achieve on written code, providing AI with the information it needs to then generate code while considering dependencies it needs to know about.


## Gen AI Use Cases For Empowering Developers

<b> In line code generation (Copilot) </b>
- Merely next token prediction uses, given what a user has written so far, predict what they are going to write, allowing them to write more without having to write it out themselves.

<b>From scratch project starter (Text-To-FileSystem, solves boilerplate)</b>
- Here an agent system can take a user prompt, plan the project out including the file structure and required components, determine a starting point of each of those files, and then one at a time write out each of the files.  This basically gets users from step 0 to something they can just begin adding features to without having to write all the boilerplate.

<b>Pseudo Project, Code Generation</b>
- Pseudo code can be used as a next step to project starters, where instead of a user only providing a prompt explaining the project as a whole, the user merely writes out the methods they want with doc strings explaining what the function is to do, and the bulk of the code is generated based on the descriptions.

<b>Large repo/directory Q&A/ debugging</b>
- Debugging can be intricate. If a user needs assistance with a particular function, the AI's effectiveness hinges on its awareness of the input sources, which might be housed in a separate file entirely. This is where retrieval systems become invaluable. Upon receiving a debugging prompt, the AI must discern which files and functions are pivotal to address the query. An efficient retrieval system can pinpoint and present the most relevant documents, streamlining the debugging process.

<b>Other</b>
- Automated test generation
- Automated documentation generation
- Dynamic code optimization

## The Problem 

While generative AI has already begun to accelerate a large portion of developer’s daily experiences, there are a few current roadblocks that make it the truly powerful tool it will be in the coming years.  

The biggest challenge to be solved at the time for AI to be able to write well developed codebases instead of just simple functions, is its ability to keep awareness over long context windows.  The most commonly used models today have a sweet spot around 4k-8k tokens, some extending to 16k all the way up to 100k.  While long context windows are claimed, there is a decent amount of research on the fact that at these longer contexts, there is greater loss of recall to information in the middle of these windows.  This directly impacts AI’s ability to efficiently generate or even Q&A on entire codebases.  Even in cases where you can prompt AI in a way that helps it understand the goal at hand, and results in it writing what appears to be a well written and complex file, it will likely result in bugs within imported methods, where the problem ends up becoming how to show AI all the necessary dependencies, without exceeding its token limits.  

<b>Context Solution:</b>
There are a number of approaches to solving the general idea of providing the necessary context to AI, allowing it to write extended, bug free code.  Some rely on long context models to be able to use entire codebases or long files as context, and some use retrieval systems that allow for pulling specific portions of the codebase as context.  While the long context capabilities of models will continue to increase, the more immediate solution is through retrieval and good old fashion software engineering skills.  That leads us to a second layer of problems, how to best retrieve the most relevant and important information from large documents or code bases?  Current retrieval systems are typically developed with the goal of returning the most similar documents, by shortest cosine distance between the prompt and the documents.  Typically this is used for text prompt to text documents, but some models like ADA-002 do have code search capability.  Yet due to the high variability in code styles, similarity from text prompt to code documents is not always efficient.  A secondary stage to retrieval can boost performance significantly, one way is by a reranking system.  This results in a retrieval system comprised of a first stage using cosine similarity between text prompt and code document to produce candidate documents, and a second stage that then ranks the candidate documents on relevance to the prompt.  This two stage system is common in recommendation systems that first determine candidate content for a user, of which are then ranked in better detail for relevancy to that particular user.  To improve performance even with a reranking system, metadata can also be used to further filter.  Most vector databases offer embedding storage with metadata that can be additional labels, data sources, or categories.  

To summarize, there is no single method of determining the best context, but the best system is a well orchestrated combination of several methods that efficiently narrow down documents until we have the absolute most relevant and important information needed to answer a prompt.  The hardest part is doing extensive experimentation to determine what works best for your goal.  
