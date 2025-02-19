# PGAI's Use with LLMs

### Summary
PGAI, built upon PostgreSQL, is great because it offers BOTH embeddings and nearest neighbor search. This makes it a great tool to connect an LLM to a vector database and lowers the use of wrappers, like those of Langchain.

The cons of using it, however, include the high barrier of entry.

### Context and Details
The model is based on PostgreSQL, which is an ACID compliant model for databases.

(PS. Reminder: ACID stands for Atomicity, which means the process completes successfully or doesn't complete at all; Consistency, which means the database is always consistent; Isolation, which means that no transaction will affect another transaction; and Durability, which means the commit is either completed successfully or the previous commit continues to be used in the database.)

PostgreSQL is also open source and an **object-relational database management system** (ORDBMS). Being open source, it supports a wide variety of features through community extensions and libraries.

It is heavily used in government and banking sectors due to its reliability and high performance.

PostgreSQL is widely used even when applying RAGs because work teams are usually more familiar with it and as such prefer it over switching to a specialized vector database such as Pinecone.

Timescale has built a useful extension for PostgreSQL in order to serve as an AI tool for LLM, mainly RAGs, to reliably use the database and connect the extension's pipeline to the LLM.

What makes PGAI so good is that it is:
1. Built on PostgreSQL and as such reliable
2. Can do **both** embeddings and nearest neighbor search (NN search through the PGVector extension)
3. Supports multiple LLMs like Ollama and OpenAI

The cons of using PGAI is that the barrier for entry is quite high since it requires a fair amount of knowledge in DBMS and PostgreSQL in particular. It is possible to write code that leverages PGAI without that knowledge, but it would not be optimal and would cause issues both long-term and short-term.

NOTE: An example of wrappers used in Langchain is "OpenAIEmbeddings", which isn't the official OpenAI client but rather LangChain's wrapper.

### Sources
- [Timescale, the creators of PGAI](https://www.timescale.com/blog/stop-over-engineering-ai-apps)
- [Reddit post on r/LocalLLaMA discussing it](https://www.reddit.com/r/LocalLLaMA/comments/1isiyl1/stop_overengineering_ai_apps_just_use_postgres/)
