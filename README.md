Run instructions:

For using fetch or finder MCP servers:

0. `cp mcp_agent.secrets.yaml.example mcp_agent.secrets.yaml` --> then update with your API key (openai api key is enough)
1. `uv sync`
2. `uv run streamlit run main.py`


For using QDrant for RAG:

0. Uncomment line 63-70 in main.py, and comment out the current `instruction` and `server_names`
1. `docker pull qdrant/qdrant`
2. `docker run -p 6333:6333 -v $(pwd)/qdrant_storage:/qdrant/storage qdrant/qdrant`
3. `uv run streamlit run main.py`