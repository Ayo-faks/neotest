# LangChain and Neo4j Integration for Conversational AI

## Overview

This GitHub repository demonstrates the integration of LangChain, CHATGPT, and Neo4j to create intelligent chat interfaces powered by graph databases. Elevate your conversational AI experiences, unlock data-driven insights, and seamlessly connect with your graph database using this innovative solution.

## Features

- **CHATGPT Magic:** Leverage the power of CHATGPT language models for intelligent and natural conversations.
- **LangChain Templates:** Utilize LangChain templates to build chat interfaces effortlessly.
- **Neo4j Graph Database:** Supercharge your data interactions with Neo4j's robust graph database.

## Getting Started

Follow these steps to set up and explore the integration:

1. Install LangChain: `pip install -U langchain-cli`
2. Create a new LangChain project: `langchain app new your-app-name --package neo4j-cypher-ft`
3. Set up your environment variables (OPENAI_API_KEY, NEO4J_URI, NEO4J_USERNAME, NEO4J_PASSWORD).
4. Ingest data into Neo4j: Run `python ingest.py` to populate your Neo4j database with sample data.
5. Configure LangSmith (optional): Set up LangSmith for tracing, monitoring, and debugging LangChain applications.
   - `export LANGCHAIN_TRACING_V2=true`
   - `export LANGCHAIN_API_KEY=<your-api-key>`
   - `export LANGCHAIN_PROJECT=<your-project>` (optional, defaults to "default")
6. Serve the app: Run `langchain serve` inside your application directory.

## Testing

Test your app using curl commands, such as:

```bash
curl -X POST -H "Content-Type: application/json" -d '{"input": {"question": "Who are the co-actors of Tom Cruise in any movie?"}}' http://localhost:8000/neo4j-cypher-ft/invoke
```

Feel free to explore more questions and interactions with the chat interface.

## Docker Support

Containerize your app with Docker:

1. Build the image: `docker build . -t my-langserve-app`
2. Run the image locally: `docker run -e OPENAI_API_KEY=$OPENAI_API_KEY -p 8080:8080 my-langserve-app`

## Contribution

Contributions are welcome! Feel free to open issues, submit pull requests, or provide feedback.

## License

This project is licensed under the [MIT License](LICENSE).

---

**Happy Conversations with LangChain and Neo4j!**
