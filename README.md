Langchain - Framework for developing applications powered by Large Language Models (LLM's)

# Components of Langchain
1. Models
2. Prompt
3. Chain
4. Memory
5. Indexes
6. Agents

### Models

LLM's solved the problem of NLU (Natural Language Understanding) and context aware text generation.
Models is a component where we can interact with AI models, the problem is models are basically trained on internet data so they have bollions of parameters and they are very very huge in size so we can not load them in our local machine so companies decided to keep them on their server and built an API around it so that users can use it but again there was an issue like different companies were creating api's in different manner so it was quite difficult to work with them so langchain built a model component (standardize the api jargons) so that we can use any connect with any model and switch b/w diff models by making minimal changes in code. So its kind of interface where instead of directly connecting to models with their resp api's we will use langchain framework.

<b>Types of models:
- language model</b> : take text as ip and return text as op
- <b>embedding model</b> : take text as ip and return vector as op, mainly used for semantic search

### Prompt

Whatever the input we give to llm's that is nothing but prompt. And the models output majorly depends upon the prompt. 

<b>There are 3 types of prompt:
- Dynamic Re-usuable prompts
- Role based prompts
- Few shot prompting</b>

### Chains
This is basically used to build pipelines similar we were doing using DVC, if we wont use chains then manually we need to call the methods and feed the op of one stage to another stage as ip, which will be offcourse automated by chains no heavy-lifting anymore. We can even build very complex pipelines using chains like conditional chaining.

### Indexes

  
