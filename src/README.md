# Source Code Snapshot

> **⚠️ Point-in-time snapshot** — This code was captured from the maintained workshop repository on May 2025.
> For the **latest version**, always refer to the maintained repo:
>
> 👉 **[AzureCosmosDB/travel-multi-agent-workshop (branch: `agent_memory_toolkit`)](https://github.com/AzureCosmosDB/travel-multi-agent-workshop/tree/agent_memory_toolkit)**

## What's Here

This snapshot includes the key components that demonstrate the session's core concept — **designing reliable multi-agent applications with Azure Cosmos DB**.

```
src/
├── azure.yaml                        # Azure Developer CLI configuration
├── python/
│   ├── requirements.txt              # Python dependencies
│   ├── src/app/
│   │   ├── travel_agents_api.py      # FastAPI REST API endpoints
│   │   ├── travel_agents.py          # LangGraph multi-agent orchestration
│   │   └── services/
│   │       ├── azure_open_ai.py      # Azure OpenAI integration
│   │       ├── azure_cosmos_db.py    # Cosmos DB operations (CRUD, queries)
│   │       └── agent_memory.py       # Agent memory toolkit integration
│   ├── prompts/
│   │   ├── orchestrator.prompty      # Main coordinator agent prompt
│   │   ├── hotel_agent.prompty       # Hotel booking specialist
│   │   ├── dining_agent.prompty      # Restaurant/dining recommendations
│   │   ├── activity_agent.prompty    # Activity planning specialist
│   │   └── itinerary_generator.prompty  # Trip itinerary generation
│   └── data/
│       ├── seed_data.py              # Database seeding script
│       ├── users.json                # Sample user profiles
│       ├── hotels_all_cities.json    # Sample hotel data (5 examples)
│       ├── restaurants_all_cities.json  # Sample restaurant data (5 examples)
│       ├── activities_all_cities.json   # Sample activity data (5 examples)
│       └── trips.json                # Sample trip itineraries
└── infra/
    ├── main.bicep                    # Main Bicep orchestration template
    └── shared/
        ├── cosmosdb.bicep            # Azure Cosmos DB deployment
        ├── openai.bicep              # Azure OpenAI deployment
        ├── managedidentity.bicep     # Managed Identity setup
        ├── assignroles.bicep         # RBAC role assignments
        └── main.parameters.json      # Deployment parameters
```

## Sample Data

The JSON data files under `data/` contain **5 example records each** to illustrate the data schema. In these snapshot files, `embedding` values are intentionally set to `null` because they are not required for understanding the schema or sample flow. For the full dataset (~490 hotels, ~977 restaurants, ~1470 activities) with generated embeddings, see the [maintained workshop repo](https://github.com/AzureCosmosDB/travel-multi-agent-workshop/tree/agent_memory_toolkit/02_completed/python/data).

## What's NOT Included

The maintained repo also includes components not snapshotted here:

- **Angular frontend** — Full web UI ("Cosmos Voyager") for the chat interface
- **MCP server** — Model Context Protocol HTTP server for tool integration
- **Workshop modules** — 7 progressive learning modules with step-by-step guides
- **Evaluation framework** — LLM judges and heuristic evaluators for agent testing
- **Media assets** — 45+ screenshots and visual guides

Visit the [maintained repo](https://github.com/AzureCosmosDB/travel-multi-agent-workshop/tree/agent_memory_toolkit) for the complete experience.
