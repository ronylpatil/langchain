**Langchain** - Framework for developing applications powered by Large Language Models (LLM's)

# Components of Langchain
**1. Models\
2. Prompt\
3. Chain\
4. Memory\
5. Indexes\
6. Agents**

### Models

LLM's solved the problem of NLU (Natural Language Understanding) and context aware text generation.
Models is a component where we can interact with AI models, the problem is models are basically trained on internet data so they have billions of parameters and they are very very huge in size so we can not load them in our local machine so companies decided to keep them on their server and built an API around it so that users can use it but again there was an issue like different companies were creating api's in different manner so it was quite difficult to work with them so langchain built a model component (standardize the api jargons) so that we can connect with any model and switch b/w diff models by making minimal changes in code. So its kind of uniform interface where instead of directly connecting to models with their resp api's we will use langchain framework. This make it easier to build application that rely on AI-generated text, text embedding for similarity search, and RAG (Retrival Augmented Generation)

<b>Types of models:
- language model</b> : take text as ip and return text as op
    <b>
  - Types of language model:
    - LLM's </b>: Majorly used for text generation, summarization, and translation etc
    - <b>chat models </b>: Specially for conversations, it also maintain context and provide structured rensposes.
- <b>embedding model</b> : take text as ip and return vector as op, mainly used for semantic search

### Prompt

Whatever the input we give to llm's that is nothing but prompt. And the models output majorly depends upon the prompt. 

<b>There are 3 types of prompt:
- Dynamic re-usuable prompts
- Role based prompts
- Few shot prompting</b>

### Chains
This is basically used to build pipelines similar we were doing using DVC, if we wont use chains then manually we need to call the methods and feed the op of one stage to another stage as ip, which will be offcourse automated by chains no heavy-lifting anymore. We can even build very complex pipelines using chains like conditional chaining.

### Indexes
Using Indexes we can give external knowledge source to our LLM application. Like we can give our company internal policy document access to LLM and it will also search the user query inside that doc because it was not trained on that doc. This external data source can be anything like pdf, any website or any database.
Indexex has 4 components:
- Doc Loader
- Text Splitter
- Vector Store
- Retriever

### Memory
LLM's api calls are stateless.
When we hit on LLM api every call is basically independent of each other, there wont be any context of previous conversation.
Ex. 1. Who is Narendra Modi? - llm api will give some response
    2. How old is he? - here llm wont understand that we are talking about narendra modi, context of previous request will be missed 

To mitigate this issue langchain introduce concept of Memory. 
<b>
Types of memory in langchain:
- ConversationBufferMemory:</b> We store the transcript of conversation, when we hit the api we send this whole conversation so that our model understand the context from it. But once the chat size will increase then total cost will also increase because it need to process this previous conversation as well to understand the context.
- <b>ConversationBufferWindowMemory:</b> Here instead of keeping all conversation we will keep only last N no of conversation.
- <b>Summarizer-Based Memory:</b> Here we will summarize the whole conversation and then send it with api call, it will reduce the processing.
- <b>Custom Memory:</b> This is basically used for advance usecase, here instead of keeping all info it store specilized info like user preferences and facts.

### Agents
Agents are just a evolved form of chatbot which have reasoning capabilities and tools access which can be used to perform any action.

### RAG Workflow
![e__MLOps_langchain_workflow_RAG](https://github.com/user-attachments/assets/a9c84674-c3b2-42f5-87fc-5f8b2843d780)







