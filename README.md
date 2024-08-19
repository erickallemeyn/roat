## What is roat.ai
Roat is designed to preserve LLM outputs over time, allowing for historical analysis and data tracability. It follows an immutable data principle, where the outputs of a query at a point in time will *never* be changed or modified. Roat will always be open source and available for local installation in your own tech stack, or also available via hosted Software-as-a-Service.

## Access Patterns
The primary interaction with Roat will be via APIs - all historical data will be available via RESTful interfaces with JSON responses. Future interaction methods will include other methods (Web UIs, GraphQL, gRPC, etc). 

## Interoperability
Roat will interface with the top hosted LLM services such as ChatGPT, Claude, Gemini and others. It will also have the ability to interface with self-hosted open source LLMs such as LLaMA.

## Limitations
Roat is not intended to be your chatbot. Use roat when you need to preserve and analyze the results of an unchanging (or slowly-changing) query over time. As LLMs continue to evolve and improve, the results of any prompt or query will change over time - even from one hour to the next as fine-tuning is performed more frequently, Retrieval Augmented Generation (RAG) is adopted and context windows are increased. Roat allows you to see and analyze this drift and perform your own root-cause analysis of shifting prompts. It also allows you to guage model performance against your queries over time, to see if they are becoming more or less accurate across different versions, models and companies. 

## Example Use cases:
- "What is the weather in New York today?"
    * Tracking this response and cross-referencing with a truth set (the actual weather) can demonstrate the recency abilities of LLMs
- "How can I keep my cheese from sliding off my pizza?"
    * Historically a challenging query for some LLMs (pro-tip: Don't use elmers glue)
- "Are skinny jeans in style again yet?"
    * What goes around comes around
- Numerical / Math problems
    * A rapidly improving area of LLMs

##Tech Stack components
- Python + FastAPI
- Pytorch
- MongoDB + Mongoose
- PostgreSQL & SQLAlchemy
- Podman (containerization)
- NextJS
- Kubernetes
- Helm
- Github CI/CD
- OpenTofu (IaC)
- Infiscal (Secret Management)

## Codebase
Contributions are welcome! You are also free to fork the codebase for your own purposes. If this project interests you, send me an email at erickallemeyn@gmail.com and lets talk more.
